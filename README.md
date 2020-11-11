# Smile-Lele.github.io

> 常听说 设计模式 和 设计原则，从此开始总结一下。
设计原则 vs 设计模式
符合 设计模式 的代码，不一定是好代码
设计原则 被用来衡量代码质量
设计模式（Design pattern）是一套被反复使用、多数人知晓的、经过分类编码的、代码设计经验的总结。使用设计模式是为了可重用代码、让代码更容易被他人理解、保证代码可靠性。
 设计原则 则是设计模式所遵循的规则，设计模式就是实现了这些原则，从而达到了代码复用、增加可维护性的目的。设计模式 是基于设计原则的

设计原则（6大原则，SOLID）
Source：http://www.uml.org.cn/sjms/201211023.asp

单一设计原则 S ingle Responsibility Principle - SRP
There should never be more than one reason for a class to change. 
只有一个原因导致类发生变化，也就是一个类承担一个职责。
E.g. 
1. 逻辑与界面分离
2. 一个变量穿梭整个代码，这会使得代码有很强的耦合性

开放封闭原则 O pen Close Principle - OCP
Software entities like classes,modules and functions should be open for extension but closed for modifications. 
软件实体， 例如类、模块、函数，对于扩展是开放的，对于修改是封闭的。如果要修改代码，尽量用 组合 or 继承 的方式来扩展类的功能（组合优于继承），而不是直接修改类的代码。
如果出现 产品需求的变更，此时修改类的代码也是必要的。

里式替换原则 L iskov Substitution Principle - LSP
Functions that use pointers or references to base classes must be able to use objects of derived classes without knowing it. 
父类可被子类替换，但反之不一定成立。也就是说，代码中可以将父类全部替换为子类，程序不会出现异常，但反过来就不一定了。
可以理解为，子类可以随意替换父类而不带来任何副作用，换言之，子类可以扩展父类的功能，但不能改变父类原有的功能。它包含以下4层含义：

副作用：表现出的行为与预期不符；在客户端需要很庞大的判断语句

子类可以实现父类的抽象方法，但不能覆盖父类的非抽象方法。
子类中可以增加自己特有的方法。
当子类的方法重载父类的方法时，方法的前置条件（即方法的形参）要比父类方法的输入参数更宽松。
当子类的方法实现父类的抽象方法时，方法的后置条件（即方法的返回值）要比父类更严格。

重载（Overload）和重写（Override）的区别？
方法的重载和重写都是实现多态的方式，区别在于前者实现的是编译时的多态性，而后者实现的是运行时的多态性。
重载发生在一个类中，同名的方法如果有不同的参数列表（参数类型不同、参数个数不同或者二者都不同）则视为重载；
重写发生在子类与父类之间，重写要求子类被重写方法与父类被重写方法有相同的参数列表，有兼容的返回类型，比父类被重写方法更好访问，不能比父类被重写方法声明更多的异常（里氏代换原则）。
重载对返回类型没有特殊的要求，不能根据返回类型进行区分。

最少知识原则 L east Knowledge Principle - LKP
接口隔离原则 I nterface Segregation Principle - ISP
The dependency of one class to another one should depend on the smallest possible interface.
客户端不应该依赖它不需要的接口；一个类对另一个类的依赖应该建立在最小的接口上。

依赖倒置原则 D ependence Inversion Principle - DIP




 目的
可维护性
可扩展性
可测试性
高内聚，低耦合，但也不是非黑即白的，要寻求一个动态平衡。
 重构


设计模式（3大类，共23种）
创建型模式（5种）：工厂方法模式、抽象工厂模式、单例模式、建造者模式、原型模式。
结构型模式（7种）：适配器模式、装饰器模式、代理模式、外观模式、桥接模式、组合模式、享元模式。
行为型模式（11种）：策略模式、模板方法模式、观察者模式、迭代子模式、责任链模式、命令模式、备忘录模式、状态模式、访问者模式、中介者模式、解释器模式
