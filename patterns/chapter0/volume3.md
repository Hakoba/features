# SOLID

Agile Software Development,
Principles, Patterns, and Practices

> В реальной жизни, пожалуй, нет
такого кода, в котором бы соблюдались все эти принципы
сразу. Поэтому помните о балансе и не воспринимайте всё
изложенное как догму.

## S
Принцип единственной ответственности
Single Responsibility Principle

>У класса должен быть только один мотив для
изменения.

## O
Принцип открытости/закрытости
open/Closed Principle

>Расширяйте классы, но не изменяйте их первоначальный код

Главная идея этого
принципа в том, чтобы не ломать существующий код при
внесении изменений в программу.

Открытый класс -- его можно расширять, добавлять поля, создавать подклассы

Закрытй класс ( законченный ) - он утвержден и его лучше не менять, его могут использовать другие классы

кст. Пример если у класса в функции много if ов, то каждый вариант этого if`а можно вывести в отедльные классы с общим интерфейсом
и при добавления новго условия (типа, способа, свойства) мы реализуем новый класс интерфейса, не трогая 1 класс.

## L
Принцип подстановки Лисков1
liskov Substitution Principle

>Подклассы должны дополнять, а не замещать поведение базового класса.

Типы параметров метода подкласса должны совпадать или
быть более абстрактными, чем типы параметров базового
метода

Тип возвращаемого значения метода подкласса должен совпадать или быть подтипом возвращаемого значения базового метода. 


>Метод не должен выбрасывать исключения, которые не
свойственны базовому методу. Типы исключений в переопределённом методе должны совпадать или быть подтипами исключений, которые выбрасывает базовый метод.
Блоки try-catch в клиентском коде нацелены на конкретные типы исключений, выбрасываемые базовым методом.
Поэтому неожиданное исключение, выброшенное подклассом, может проскочить сквозь обработчики клиентского
кода и обрушить программу

^КАКАЯ же жиза^ когда ожидаешь пустой массив, а прилетает nil (null), или, [""]

Инварианты класса должны остаться без изменений. Инвариант — это набор условий, при которых объект имеет
смысл

# Подкласс *не должен* изменять значения приватных полей базового класса.

## I
Принцип разделения интерфейса
Interface Segregation Principle

>Клиенты не должны зависеть от методов, которые они
не используют.

Одним классом реализовывать несколько интерфейсов, а не расширять один интерфейс, а после не использвать половину его возможностей

## D
Принцип инверсии зависимостей
Dependency Inversion Principle

Классы верхних уровней не должны зависеть от классов нижних уровней. Оба должны зависеть от абстракций. Абстракции не должны зависеть от деталей.
Детали должны зависеть от абстракций.

Крч, добавляешь прослойку в виде интерфейса для низкоуровневых операций, между высокоуровневыми и низкоуровневыми классами, по итогу низкоуровневый класс зависит от интерфейса, который определят бизнес, а бизнес зависит, от от низкого чуть меньше так как работает с тем же интерфейсом, так, изменяя низкий уровень ты не сможешь его сильно поломать так как он, в случаее чего не сможет работать если не будет реализовн его интерфейс
