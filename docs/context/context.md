# Контекст решения

<!-- Окружение системы (роли, участники, внешние системы) и связи системы с ним. Диаграмма контекста C4 и текстовое описание. 
Подробнее: https://confluence.mts.ru/pages/viewpage.action?pageId=375783261
-->

```plantuml
@startuml
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Context.puml
LAYOUT_LEFT_RIGHT()

Boundary(usrs, "Пользователи"){
    Person(spk, "Докладчик", "Тот, кто рассказывает свой доклад")
    Person(lst, "Слушатель", "Тот, кто наблюдает за конференцией")
    Person(mod, "Модератор", "Тот, кто составляет программу конференции")
}

System_Boundary(sys, "Система обеспечения конференции"){

    System(conf, "Web Application", "Позволяет пользователям получать информацию о конференциях и взаимодействовать с ними.")
    System_Ext(ns, "Communicator", "Подсистема для взаимодействия с пользователями")
   System_Ext(data, "Data Accessor", "Подсистема доступа к данным конференций")
}

Rel(usrs, conf, "Uses")
Rel(data, ns, "Notifies")
BiRel(conf, data, "Uses")
Rel(ns, usrs, "Sends message")
Rel(conf, ns, "Uses")
@enduml
```