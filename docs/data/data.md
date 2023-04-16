# Модель предметной области

<!-- Логическая модель, содержащая бизнес-сущности предметной области, атрибуты и связи между ними. 
Подробнее: https://confluence.mts.ru/pages/viewpage.action?pageId=375782602

Используется диаграмма классов UML. Документация: https://plantuml.com/class-diagram 
-->

```plantuml
@startuml Model
' Логическая модель данных в варианте UML Class Diagram (альтернатива ER-диаграмме).
namespace Conference{
class Conference
{
    id : string
    date : DataTime
}

class ConfContent
{
    id: string
    description : string
}

Translation --* ConfContent
Media --* ConfContent
ConfContent --* Conference
}

namespace UX{
enum UserType
{
    Watcher
    Moderator
    Speaker
}

class User
{
    id : string
    type : UserType
    relatedConferences : Conference
}

User -- UserType
Conference.Conference ..> "1..*" User
}
@enduml
```
