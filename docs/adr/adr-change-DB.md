# ADR.003 Целесообразность замены реляционной базы данных системы на документарную (MongoDB)

<!-- Название ADR состоит из [ADR.###] [Коротко суть принятого решения] -->

* Статус: Предложено
* Владелец: sabratch@mts.ru

## Контекст

<!-- Описание проблемы, требующей решения, причин, побудивших принять решение, ограничений, действовавших на момент принятия решения -->

Появилось новое, неожиданное ранее Бизнес-требование, которое гласит о желании применять разрабатываемую систему управелния конференциями в качестве LMS-системы. Это означает, что необходимо расширение доменной модели, появление новых сущностей. Что в своб очередь означает, что необходимо хранить новые данные, возможно менять структуру БД.

В то же время, система активно развивается, доходность растет, новые Бизнес-Требования появляются, существует вероятность появления аналогичных требований.

## Варианты решения

<!-- Описание рассмотренных вариантов c их плюсами и минусами -->

### Вариант 1. Изменить реляционную БД на документарную (MongoDB)

<!-- Описание варианта 1 -->

* **Плюсы**
  * Легкость адаптации к изменениям в структуре данных.
  * Возможность горизонтального масштабирования для удовлетворения новых Бизнес-Требований. (Например, выносить новые сущности и агрегаты в шарды)
  * Возможность повысить производительность в случае реализации работы БЛ как с атомарными, полными документами, без необходимости сложных запросов и джоинов.
* **Минусы**
  * Требуется минимум спринт только для перевода кода сервисов на испрользование клиента MongoDB вместо клиента реляционнной БД.
  * Сущствуют риски необходимости доработки валидации на стороне Бизнес-Логики при реализации новых Бизнес-Требований в связи с необходимостью поддерживать разные структуры документов.
  * Требуется выделение дополнительных ресурсов во всех средах, первоначальная настройка инфраструктуры, постановка на мониторинг, разработка механизмов бэкапирования.
  * При фиксации модели данных и выхода из стадии MVP необходимо будет обратно переходить на реляционную БД.
  * Поскольку команда изначально работала с реляционной БД - для работы с MongoDB потребуется время на адаптацию.
  * В случае работы с модификацией существующих данных - может быт просадка по производительности относительно релационной БД.

### Вариант 2. Не изменять реляционную БД на документарную (MongoDB)

<!-- Описание варианта 2 -->

* **Плюсы**
  * Отсутствие затрат на переход (перепроверка кода, выделение ресурсов, настройка инфораструктуры, отвлечение от Roadmap, обучение команды)
* **Минусы**
  * Относительно медленная реакция на существенные изенения в Бизнес-Требованиях.
  * В случае работы с простыми запросами на чтение и организации Бизнес-Логики на чтение возможны просадки в производительности.

## Решение

<!-- Описание выбранного решения. Решение должно быть сформулировано чётко ("Мы используем...", "Мы не используем", а не "Желательно.." или "Предлагается..."). 
Должна быть понятна связь между решением и проблемой, почему выбрали именно это решение из вариантов -->

Не меняем БД.

Конечно, вероятность появления новых БТ существует, однако это происходит относительно редко. И скорость реакции на эти изменения не так необходима в отличие от необходимости выполнить их и обеспечить их надежную работу.

Описанные даже в этом случае изменения Бизнес-Требований не так страшны для реляционной БД и решаются довольно простой миграцией и добавлением по сути дополнительных столбцов. Выглядит так, что даже новые таблицы не понадобятся.

После реализации требований на MongoDB все равно рекомендовано будет обратно переехать на реляционную БД. Таким образом, текущий перевод будет стоить лишних ресурсов и практически будет не сильно полезен.

Значительных преимещуств при использовании MongoDB, которые могли бы ощутимо сократить T2M или снизить затраты ресурсов - не обнаружено.

## Последствия

<!-- Положительные и отрицательные последствия (trade-offs). Арх. решения, которые потребуется принять как следствие принятого решения. Если решение содержит риски, то описано, как с ними планируют поступить (за счет чего снижать, почему принять). -->

Возможные снижения в произвоительности на чтение - это не так страшно, поскольку время отклика системы не критичный показатель.

Относительная медленная скорость реакции на новые БТ - не так страшно, поскольку они приходят редко и с должным умением команды работать с реляционными БД это также не проблема.