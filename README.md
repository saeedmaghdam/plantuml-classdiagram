# Relations in Class Diagram

## Has
The "has" keyword is used to represent an ownership or containment relationship between two classes. For example, if a "Person" class has one or more "Address" objects associated with it, you can represent this relationship as follows:

```
Person --> Address: has >
```

![has](./assets/has.png)

## Uses
The "uses" keyword is used to represent a dependency relationship between two classes. For example, if a "Car" class uses a "Engine" object, you can represent this relationship as follows:

```
Car --> Engine: uses >
```

![Uses](./assets/uses.png)

## Takes
The "takes" keyword is used to represent a one-to-one relationship between two classes, where one class takes another as input or parameter. For example, if a "Calculator" class takes two "Number" objects and performs a calculation on them, you can represent this relationship as follows:

```
Calculator --> Number: takes >
```

![Takes](./assets/takes.png)

## Places
The "places" keyword is used to represent a one-to-many relationship between two classes, where one class places or creates many instances of another class. For example, if a "Customer" class places many "Order" objects, you can represent this relationship as follows:

```
Customer -- Order: places >
```

![Places](./assets/places.png)

## Extends
The "extends" keyword is used to represent an inheritance relationship between two classes, where one class is a subclass of another class. For example:

```
class Animal {
  ...
}

class Cat extends Animal {
  ...
}
```

![Extends](./assets/extends.png)

## Implements
The "implements" keyword is used to represent an interface implementation relationship between two classes, where one class implements the methods defined in an interface. For example:

```
interface Drawable {
  void draw();
}

class Circle implements Drawable {
  void draw() {
    // draw circle
  }
}
```

![Implements](./assets/implements.png)

## Associates
The "associates" keyword is used to represent a bidirectional association between two classes, where each class has a reference to the other class. For example:

```
class Person {
  private List<Address> addresses;
}

class Address {
  private Person owner;
  ...
}

Person <-> Address: associates
```

![Associates](./assets/associates.png)

## Aggregates
The "aggregates" keyword is used to represent a unidirectional association between two classes, where one class contains a collection of instances of the other class. For example:

```
class Library {
  private List<Book> books;
}

class Book {
  ...
}

Library --> Book: aggregates
```

![Aggregates](./assets/aggregates.png)

## Composes
The "composes" keyword is used to represent a composition relationship between two classes, where one class is composed of instances of the other class. This is similar to aggregation, but in composition, the lifetime of the composed objects is tied to the lifetime of the composite object. For example:

```
class Car {
  private Engine engine;
}

class Engine {
  ...
}

Car --> Engine: composes
```

![Composes](./assets/composes.png)

## Uses/Composes/Aggregates:
The "uses/composes/aggregates" keyword is used to represent a combination of relationships between two classes. This can be useful when the relationship between the classes is not clearly one type or another. For example:

```
class Zoo {
  private List<Animal> animals;
}

class Animal {
  ...
}

Zoo --> Animal: uses/composes/aggregates
```

![Uses/Composes/Aggregates](./assets/uses-composes-aggregates.png)