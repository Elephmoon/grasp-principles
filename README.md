# General responsibility software patterns (распределение ответственности)

## <a name="list"></a> Список принципов
1. Low coupling
2. High cohesion
3. [Information expert](#information-expert)
4. [Creator](#creator)
5. Controller
6. Polymorphism
7. Pure fabrication
8. Indirection
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
Тот, кто содержит агрегирует инстансы, кто много работает с инстансами, кто владеет необходимой для инициализации информацией
#### Зачем
Снижает зацепление
#### Пример
Конструктор, фабрика
