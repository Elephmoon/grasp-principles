# General responsibility software patterns (распределение ответсвенности)

## <a name="list"></a> Список принципов
1. Low coupling
2. High cohesion
3. [Information expert](#information-expert)
4. Creator
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


