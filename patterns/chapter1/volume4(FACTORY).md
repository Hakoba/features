# Фабричный метод 
— это порождающий паттерн
проектирования, который определяет общий интерфейс для
создания объектов в суперклассе, позволяя подклассам
изменять тип создаваемых объектов.

Крч, создаем объекты не вручную, а через прокладку,

!если мы хотим, чтобы создавались классы из чутка измененного фабрачичного класса, то делаем подкласс из фабрики, где переопределяем нужный метод, или проп, затем используем этот подкласс, как фабрику. Наверняка есть подводные, но хз

Шаги реализации
1. Приведите все
интерфейсу.
создаваемые
продукты
2. В классе, который производит продукты, создайте пустой
фабричный метод. В качестве возвращаемого типа укажите
общий интерфейс продукта.
3. Затем пройдитесь по коду класса и найдите все участки,
создающие продукты. Поочерёдно замените эти участки
вызовами фабричного метода, перенося в него код создания
различных продуктов.
В фабричный метод, возможно, придётся добавить несколько параметров, контролирующих, какой из продуктов нужно
создать.
4. Для каждого типа продуктов заведите подкласс и переопределите в нём фабричный метод. Переместите туда код
создания соответствующего продукта из суперкласса.
5. Если создаваемых продуктов слишком много для существующих подклассов создателя, вы можете подумать о введении параметров в фабричный метод, которые позволят
возвращать различные продукты в пределах одного
подкласса.

Преимущества и недостатки

**ПЛЮС**
- Избавляет класс от привязки к конкретным классам
продуктов.
- Выделяет код производства продуктов в одно место, упро-
щая поддержку кода.
- Упрощает добавление новых продуктов в программу.
- Реализует принцип открытости/закрытости.

**МИНУС**
 -  Может привести к созданию больших параллельных иерар-
хий классов, так как для каждого класса продукта надо
создать свой подкласс создателя.