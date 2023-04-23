# Компонентная архитектура
<!-- Состав и взаимосвязи компонентов системы между собой и внешними системами с указанием протоколов, ключевые технологии, используемые для реализации компонентов.
Диаграмма контейнеров C4 и текстовое описание. 
Подробнее: https://confluence.mts.ru/pages/viewpage.action?pageId=375783368
-->
## Контейнерная диаграмма
```plantuml
@startuml
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Component.puml

Person(moderator, "Модератор")
Person(speaker, "Докладчик")
Person(listner, "Слушатель")

System_Boundary(conf, "Helloconf MTS (Proto)"){
   Container(front, "Клиентское веб-приложение", "html, JavaScript, React", "Веб-форма конференции")

   Container(back, "Клиентское веб-приложение", ".NET Core, C#", "Сервис управления данными о конференциях")

   ComponentDb(database, "База данных", "MongoDB")
}

System_Ext(stream_service, "Stream service", "Стриминговый сервис (YouTube)") 

Lay_R(front, stream_service)
Lay_U(conf, moderator)
Lay_U(back, front)

Rel(front, stream_service, "Показывает трансляцию", "Web-Socket")
Rel(moderator, front, "Модерирует выступления", "HTTPS")
Rel(speaker, front, "Управляет контентом", "HTTPS")
Rel(listner, front, "Просматривает конференцию", "HTTPS")
Rel(front, back, "Запрос информации о пользователях и конференциях", "JSON,REST,HTTP")
Rel_L(back, database, "Хранение данных о пользователях и конференциях", "MongoDB driver")

@enduml
```

## Список компонентов
| Компонент             | Роль/назначение                  |
|:----------------------|:---------------------------------|
| *Название компонента* | *Описание назначения компонента* |