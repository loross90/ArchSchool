# Контекст решения

<!-- Окружение системы (роли, участники, внешние системы) и связи системы с ним. Диаграмма контекста C4 и текстовое описание. 
Подробнее: https://confluence.mts.ru/pages/viewpage.action?pageId=375783261
-->

```plantuml
@startuml
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Context.puml


LAYOUT_TOP_DOWN()
LAYOUT_WITH_LEGEND()

System_Boundary(sys, "Helloconf MTS (Proto)"){
    Boundary(kernel, "Конференция"){
        System(conf, "Конференция")
        System(content, "Контент конференции")
        System(date, "Дата конференции")
        System(participator, "Участник")

        Rel(conf, content,)
        Rel(conf, date,)
        Rel(conf, participator,)
    }
   
   Boundary(not, "Уведомления о конференциях"){
        System(notification, "Уведомление")
        System(not_cont, "Контент уведомления")
        System(adressat, "Адресат уведомления")
        System(parameters, "Параметры уведомления (Период)")

        Rel(notification, not_cont,)
        Rel(notification, adressat,)
        Rel(notification, parameters,)
   }
}

Boundary(transl, "Трансляция конференции"){
        System(translation, "Трансляция")
        System(trans_users, "Пользователи трансляции")
        System(chat, "Чат трансляции")

        Rel(translation, trans_users,)
        Rel(translation, chat,)
   }

BiRel(kernel, not, "")
BiRel(transl, kernel, "")


@enduml
```