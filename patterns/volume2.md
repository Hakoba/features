# Базовые принципы проектирования


## Инкапсулирой то, что меняется

>Определите аспекты программы, класса или метода,
которые меняются чаще всего, и отделите их от того,
что остаётся постоянным.

это уменьшит последствия, которые влекут собой изменения


## Программируй на уровне интерфейса

>Программируйте на уровне интерфейса, а не на
уровне реализации. Код должен зависеть от абстракций, а не конкретных классов.

1. Определите, что именно нужно одному объекту от другого,
какие методы он вызывает.
2. Затем опишите эти методы в отдельном интерфейсе.
3. Сделайте так, чтобы класс-зависимость следовал этому
интерфейсу. Скорее всего, нужно будет только добавить этот
интерфейс в описание класса.
4. Теперь вы можете сделать и второй класс зависимым от
интерфейса, а не конкретного класса.

## Предпочитайте композицию наследованию


Наследование самое простое, но не есть аболютное добро

нужно реализоваыывать все абстрактные методы родителя, даже если они не нужны. Редактируюя родителя, можно сломать поведение его базовых функций, как суперкласса. Суперклассы могут стать зависимыми од подклассов если в суперклассы внести общие методы или пропы подкласса, для  того чтобы облегчить наследолвание, КРЧ, связывать слишком сильно нельзя, плюс иерархия пухнет пздц.


### Отличия композиции от наследования
 Двачер *является* животным

 Двачер *содержит* комплексы
 