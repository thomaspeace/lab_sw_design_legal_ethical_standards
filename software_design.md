# Software Design

---

#### 1. What do we mean by **coupling** and **cohesion** when discussing structured design?

- **Coupling** refers to the degree of interdependence between software modules. **High coupling** means that modules are closely connected and changes in one module may affect other modules. **Low coupling** means that modules are independent, and changes in one module have little impact on other modules.

- **Cohesion** refers to the degree to which elements within a module work together to fulfill a single, well-defined purpose. A class containing methods that have nothing to do with each other exhibits **low cohesion**, whereas a class containing methods that are logically similar exhibits **high cohesion**. High cohesion leads to focused classes that serve a well-defined purpose.

Code should aim to have a *high degree of cohesion* and a *low degree of coupling*.

---

#### 2. What is the difference between **top-down** and **bottom-up** design? Which best describes a function oriented design?

- **Top-down** (stepwise refinement) takes a high level definition of the problem and dividides it into abstract subproblems (decompostion), which can be then be iteratively divided into smaller subproblems.

- **Bottom-up** design begins with basic and fundamental components and integrates them to form higher-level systems. This approach emphasises coeding and early testing.

**Function orientated design** is besst deployed with a **top-down** approach. High-level functions of the system are defined first, and then these functions are decomposed into smaller sub-functions or modules.

---

#### 3. In which design methodology would a class diagram be most useful?

Class diagrams would be more useful in **Object-orientated design** as it focusing on building objectsm which are instances of classes.

---

#### 3. In which design methodology would a class diagram be most useful?

Class diagrams would be more useful in **Object-orientated design** as it focusing on building objectsm which are instances of classes.

---

#### 4. What are the four pillars of object oriented programming? Give a single-sentence description of each.

- **Abstraction:** Simplifying complexity by providing a high-level view of an object (only show the necessary details to the user).
- **Polymorphism:** Objects of different types can be treated as instances of a common superclass (a child class can define its own unique behavior and still share the same methods or behavior of its parent class).
- **Inheritance:** A class can inherit the attributes and behaviors of another class, adding additional properties and methods if required.
- **Encapsulation:** Ensuring data within objects is only accessed within objects (unless specified), safeguarding it from unauthorized access.

---

#### 5. What is the strategy pattern? How would its implementation differ between a functional and object oriented system?

The **Strategy patern** (also known as policy pattern) is a behavioral design pattern that enables selecting an algorithm's behavior at runtime. Instead of implementing a single algorithm, run-time instructions specify which of a family of algorithms to use. This pattern defines a family of algorithms, encapsulates each one, and makes them interchangeable. This means the algorithm can vary depending on the client that uses it.

The different implementations in **OOD** and **Functional Design** are:

- **Encapsulation:** In *OOP*, algorithms would be encapsulated within classes, each algorithm would be a concrete class. In *Functional Proramming*, algorithms would be encapsualted within higher-order functions, with each algorithm being a function.

- **Context Handling:** In *OOP* the context holds a reference to a strategy object and calls its method., In *Functional Programming*, the context is often a function that takes another function (the strategy) as an argument and calls it.

- **State and Mutability:** In *OOP*, context and strategy can maintain state within objects. **Functional Programming** is typically stateless and focuses on the transformation of data through pure functions.

- **Flexibility:** *OOP* is more structured, which might provide better organisation for large systems with complex interactions. *Functional programming* is more flexible, allows easy composition and higher-order functions.

---

#### 6. Imagine your creating a new online payment system. Not tied to particular sector. Which design methodology would you suggest following?

I would suggest following **Object orientated design**. Since the code would be applied to multiple sectors, we can take advantage of inheritance and polymorphism to create new classes for different types of transactions, and add class variable and methods depending on what is being sold.

OOP would mean the code is modular and resuable, so creating new transactions systems for a new sector would take much less time than Functional and let the storefront be deployed sooner. This also means the code is maintainable.

OOP is also scalable as new classes can easily be added as well as extended. 