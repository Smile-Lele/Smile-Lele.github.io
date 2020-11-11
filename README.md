# Smile-Lele.github.io

常听说 设计模式 和 设计原则，从此开始总结一下。
设计原则 vs 设计模式
符合 设计模式 的代码，不一定是好代码
设计原则 被用来衡量代码质量
设计模式（Design pattern）是一套被反复使用、多数人知晓的、经过分类编码的、代码设计经验的总结。使用设计模式是为了可重用代码、让代码更容易被他人理解、保证代码可靠性。
 设计原则 则是设计模式所遵循的规则，设计模式就是实现了这些原则，从而达到了代码复用、增加可维护性的目的。设计模式 是基于设计原则的
设计原则（6大原则，SOLID）
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
总结：在继承类是，务必重写（override）父类中所有的方法，尤其需要注意父类的protected方法（它们往往是让你重写的），子类尽量不要暴露自己的public方法供外界调用。


最少知识原则 L east Knowledge Principle - LKP
接口隔离原则 I nterface Segregation Principle - ISP
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
