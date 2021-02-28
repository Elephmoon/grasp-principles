# General responsibility software patterns (распределение ответственности)

## <a name="list"></a> Список принципов
1. [Low coupling](#coupling-coheison)
2. [High cohesion](#coupling-coheison)
3. [Information expert](#information-expert)
4. [Creator](#creator)
5. [Controller](#controller)
6. [Polymorphism](#polymorphism)
7. Pure fabrication
8. [Indirection](#indirection)
9. Protected variations

### <a name="information-expert"></a> Information expert [^](#list)
#### Проблема 
Как распределить ответственность между классами?
#### Решение
Назначить ответсвенность классу, который имеет всю необходимую информацию
#### Зачем
Снижает зацепление, упрощает код, повышает возможность переиспользования

### <a name="creator"></a> Creator [^](#list)
#### Проблема 
Кто отвечает за создание инстанса? (хранение и очищение ссылки на инстанс)
#### Решение
Тот, кто содержит или агрегирует инстансы, кто много работает с инстансами, кто владеет необходимой для инициализации информацией
#### Зачем
Снижает зацепление
#### Пример
Конструктор, фабрика

### <a name="coupling-coheison"></a> Low coupling, High coheison [^](#list)
#### High coheison 
Связность внутри модуля/компонента/класса, должна быть сильной.  
Внутри модуля функции могут работать со структурами данных, полями, функциями напрямую.
#### Low coupling
Зацепление между компонентами, должно быть слабым.  
Модули могут общаться друг с другом только через экспортируемые интерфейсы.  
Модули не должны обращаться к структурам данных или полям другого модуля напрямую.

### <a name="controller"></a> Controller [^](#list)
#### Проблема 
Кто и как взаимодействует с запросами?(http, запросы от UI).  
Основная задача Controller изолировать бизнес логику от внешнего мира.
#### Зачем
Защита от событий, конкурентности, ассинхронности и параллельности.
#### Пример
Фасад, изоляция слоев

### <a name="polymorphism"></a> Polymorphism [^](#list)
#### Проблема 
Как поступать в ситуации когда от типа зависит поведение?
#### Решение
Заменяем if на полиморфизм и наследование, обращаемся через интерфейс.

### <a name="indirection"></a> Indirection [^](#list)
#### Проблема 
Снизить зацепление между абстракциям.
#### Зачем
Снижает зацепление, улучшает переиспользование.
#### Пример
Медиатор, в MVC посредником является Controller.

