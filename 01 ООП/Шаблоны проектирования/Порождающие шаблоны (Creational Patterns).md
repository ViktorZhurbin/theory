
## Порождающие шаблоны проектирования

### Фабричный метод (Factory Method)

(https://sourcemaking.com/design_patterns/factory_method)
https://refactoring.guru/design-patterns/factory-method
https://www.tutorialspoint.com/design_pattern/factory_pattern.htm

Задача: определить интерфейс для создания объектов в суперклассе, и позволить подклассам решать, экземпляр какого класса создавать.

Часто испозьзуется для создания объектов.
Фабричный метод часто определяют как статический метод класса, который возвращает объект того же типа.

В отличие от конструктора:
- возвращаемый объект может быть экземпляром подкласса
- объект можно переиспользовать (и не создавать новый)

Клиент не связан с реализацией производных классов, что позоволяет использовать полиморфизм.


### Одиночка/Синглетон (Singleton)

Шаблон проектирования, при котором у класса может быть только один экземпляр. За создание этого экземпляра отвечает сам класс с помощью public static метода (`Singleton.getInstance()`), а скрытый (private) конструктор гарантирует, что экземпляр не может быть создан извне.

Используется в паттернах абстрактная фабрика, строитель, прототип, фасад, состояние.

Синглетон часто предпочитают глобальным переменным, потому что:
- не засоряют пространство имён
- позволяют ленивое назначение ресурсов и инициализацию

