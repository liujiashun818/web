关于设计模式的总结

1.抽象工厂: Factory

提供一个创建一系列或相关依赖对象的接口，而无需指定他们具体的类。针对多级结构.

抽象工厂模式除了具有工厂方法模式的优点外，最主要的优点就是可以在类的内部对产品族进行约束。

产品族的扩展将是一件十分费力的事情，假如产品族中需要增加一个新的产品，

则几乎所有的工厂类都需要进行修改。

适用场景

当需要创建的对象是一系列相互关联或相互依赖的产品族时，便可以使用抽象工厂模式。

2.建造者: Builder

将一个复杂对象的构建与它的表示分离，使得同样的构建过程可以创建不同的表示。

使用建造者模式的好处

1.使用建造者模式可以使客户端不必知道产品内部组成的细节。

2.具体的建造者类之间是相互独立的，对系统的扩展非常有利。

3.由于具体的建造者是独立的，因此可以对建造过程逐步细化，而不对其他的模块产生任何影响。

使用建造者模式的场合:

1.创建一些复杂的对象时，这些对象的内部组成构件间的建造顺序是稳定的，但是

对象的内部组成构件面临着复杂的变化。

2.要创建的复杂对象的算法，独立于该对象的组成部分，也独立于组成部分的装配方法时。

3.工厂方法:Factory Method

定义一个用于创建对象的接口，让子类决定实例化哪一个类，工厂模式使一个类的

实例化延迟到其子类。针对单一结构系统.

适用场景：

作为一种创建类模式，在任何需要生成复杂对象的地方，都可以使用工厂方法模式

假如调用者自己组装产品需要增加依赖关系时，可以考虑使用工厂模式。

当需要系统有比较好的扩展性时，可以考虑工厂模式

4.原型:Prototype

用原型实例指定创建对象的种类，并且通过拷贝这些原型创建新的对象。

使用原型模式创建对象比直接new一个对象在性能上要好的多，因为Object类的clone方法是一个本地方法，

它直接操作内存中的二进制流，特别是复制大对象时，性能的差别非常明显。

使用原型模式的另一个好处是简化对象的创建，使得创建对象就像我们在编辑文档时的复制粘贴一样简单。

因为以上优点，所以在需要重复地创建相似对象时可以考虑使用原型模式。比如需要在一个

循环体内创建对象，假如对象创建过程比较复杂或者循环次数很多的话，使用原型模式不但可以简化创建过程，

而且可以使系统的整体性能提高很多。

5.单例:Singleton

保证一个类仅有一个实例，并提供一个访问它的全局访问点.

让类自身负责保存它的唯一实例，这个类可以保证没有其他实例可以被创建，

并且我还提供了一个访问该实例的方法。这样就使得对唯一的实例可以严格

地控制客户怎样以及何时访问它。

6.适配器:Adapter

将一个类的接口转换成客户希望的另外一个接口。适配器模式使得原本由于

接口不兼容而不能一起工作的那些类可以一起工作。

优点:

通过适配器，客户端可以调用同一接口，因而对客户端来说是透明的。这样做更简单、更直接、更紧凑。

复用了现存的类，解决了现存类和复用环境要求不一致的问题。

将目标类和适配者类解耦，通过引入一个适配器类重用现有的适配者类，而无需修改原有代码。

一个对象适配器可以把多个不同的适配者类适配到同一个目标，也就是说，

同一个适配器可以把适配者类和它的子类都适配到目标接口。

缺点:

对于对象适配器来说，更换适配器的实现过程比较复杂。

适用场景:

系统需要使用现有的类，而这些类的接口不符合系统的接口。

想要建立一个可以重用的类，用于与一些彼此之间没有太大关联的一些类，包括一些可能在将来引进的类一起工作。

两个类所做的事情相同或相似，但是具有不同接口的时候。

旧的系统开发的类已经实现了一些功能，但是客户端却只能以另外接口的形式访问，

但我们不希望手动更改原有类的时候。

使用第三方组件，组件接口定义和自己定义的不同，不希望修改自己的接口，但是要使用第三方组件接口的功能。

7.桥接:Bridge

将抽象不笨与它的实现部分分离，使它们都可以独立地变化.

桥接模式的使用场景:

1、当一个对象有多个变化因素的时候，通过抽象这些变化因素，将依赖具体实现，修改为依赖抽象。

2、当某个变化因素在多个对象中共享时。我们可以抽象出这个变化因素，然后实现这些不同的变化因素。

3、当我们期望一个对象的多个变化因素可以动态的变化，而且不影响客户的程序的使用时。

8.组合(合成):

将对象组合成树形结构以表示‘部分-整体’的层次结构，组合模式使得用户

对单个对象和组合对象的使用具有一致性。

使用场景:

当发现需求中是体现部分与整体层次结构时，以及你希望用户可以忽略组合对象与单个对象的不同，

统一地使用组合结构中的所有对象时，就应该考虑组合模式了。

9.装饰:Decorator

动态地给一个对象添加一些额外的职责。就增加功能来说，装饰模式相比生成子类更加灵活。

1.在不影响其他对象的情况下，以动态、透明的方式给单个对象添加职责。

2 处理那些可以撤消的职责。

3.当不能采用生成子类的方法进行扩充时。一种情况是，可能有大量独立的扩展，

为支持每一种组合将产生大量的子类，使得子类数目呈爆炸性增长。

另一种情况可能是因为类定义被隐藏，或类定义不能用于生成子类。

10.外观:Facade

为子系统中的一组接口提供一个一致的界面，外观模式定义了一个高层接口，

这个接口使得这一子系统更加容易使用。

适用环境:

在开发阶段，子系统往往因为不断的重构演化而变得越来越复杂，

增加外观Facade可以提供一个简单的接口，减少它们之间的依赖.

在维护一个遗留的大型系统时，可能这个系统已经非常难以维护和扩展了，可以为

新系统开发一个外观Facade类，来提供设计粗糙或高度复杂的遗留代码的比较清晰

简单的接口，让新系统与Facade对象交互，Facade与遗留代码交互所有复杂的工作。

优点:

实现了子系统与客户端之间的松耦合关系。

客户端屏蔽了子系统组件，减少了客户端所需处理的对象数目，并使得子系统使用起来更加容易。

11.享元:Flyweight

为运用共享技术有效地支持大量细粒度的对象。

优点:

1、享元模式的优点在于它能够极大的减少系统中对象的个数。

2、享元模式由于使用了外部状态，外部状态相对独立，不会影响到内部状态，

所以享元模式使得享元对象能够在不同的环境被共享。

缺点

1、由于享元模式需要区分外部状态和内部状态，使得应用程序在某种程度上来说更加复杂化了。

2、为了使对象可以共享，享元模式需要将享元对象的状态外部化，而读取外部状态使得运行时间变长。

模式适用场景

1、如果一个系统中存在大量的相同或者相似的对象，由于这类对象的大量使用，会造成系统内存的耗费，

可以使用享元模式来减少系统中对象的数量。

2、对象的大部分状态都可以外部化，可以将这些外部状态传入对象中。

12.代理:Proxy

为其他对象提供一种代理以控制对这个对象的访问。在某些情况下，一个对象不适合或者不能直接引用

另一个对象，而代理对象可以在客户端和目标对象之间起到中介的作用。

代理模式常被分为远程代理、虚拟代理、保护代理等等。

优点：

1)代理模式能将代理对象与真正被调用的对象分离，在一定程度上降低了系统的耦合度。

2)代理模式在客户端和目标对象之间起到一个中介作用，这样可以起到保护目标对象的作用。

代理对象也可以对目标对象调用之前进行其他操作。

缺点：

1)在客户端和目标对象增加一个代理对象，会造成请求处理速度变慢。

2)增加了系统的复杂度。

使用场景：

1)远程代理，也就是为一个对象在不同的地址空间提供局部代表。这样可以隐藏一个对象存在于

不同地址空间的事实。

2)虚拟代理，根据需要创建开销很大的对象。通过它来存放实例化需要很长时间的对象。

3)安全代理，用来控制真实对象访问时的权限。

4)智能指引，当调用目标对象时，代理可以处理其他的一些操作。

13.观察者:Observer

定义对象间的一种一对多的依赖关系，当一个对象的状态发生改变时，所有

依赖与它的对象都得到通知并被自动更新.

优点:

观察者模式解除了主题和具体观察者的耦合，让耦合的双方都依赖于抽象，而不是依赖具体。

从而使得各自的变化都不会影响另一边的变化。

缺点:

依赖关系并未完全解除，抽象通知者依旧依赖抽象的观察者。

适用场景:

当一个对象的改变需要给变其它对象时，而且它不知道具体有多少个对象有待改变时。

一个抽象某型有两个方面，当其中一个方面依赖于另一个方面，这时用观察者模式可以将

这两者封装在独立的对象中使它们各自独立地改变和复用。

14.模版方法:Template Method

定义一个操作的算法骨架，而将一些步骤延迟到子类中，模版方法

使得子类可以不改变一个算法的结构即可重定义该算法的某些特定步骤.

优点:

模板方法模式通过把不变的行为搬移到超类，去除了子类中的重复代码。

子类实现算法的某些细节，有助于算法的扩展。

通过一个父类调用子类实现的操作，通过子类扩展增加新的行为，符合“开放-封闭原则”。

缺点:

每个不同的实现都需要定义一个子类，这会导致类的个数的增加，设计更加抽象。

适用场景:

在某些类的算法中，用了相同的方法，造成代码的重复。

控制子类扩展，子类必须遵守算法规则。

15.命令:Command

将一个请求封装为一个对象，从而使你可用不同的请求对客户进行

参数化; 可以对请求排队或请求日志，以及支持可撤销的操作。

优点：

* 1 他能较容易地设计一个命令队列

* 2 在需要的情况下，可以较容易地将命令记入日志

* 3 允许接收请求的一方决定是否要否决请求

* 4 可以容易地实现对请求的撤销和重做

* 5 由于加进新的具体命令类不影响其他的类 因此新的具体命令类很容易

适用场景：

1. 命令的发送者和命令执行者有不同的生命周期。命令发送了并不是立即执行。

2. 命令需要进行各种管理逻辑。

3. 需要支持撤消\重做操作(这种状况的代码大家可以上网搜索下，有很多，这里不进行详细解读)。

16.状态:State

允许一个对象在其内部状态改变时改变它的行为，让对象看起来似乎

修改了它的类。

优点:

状态模式将与特定状态相关的行为局部化，并且将不同状态的行为分割开来。

所有状态相关的代码都存在于某个ConcereteState中，所以通过定义新的子类很容易地增加新的状态和转换。

状态模式通过把各种状态转移逻辑分不到State的子类之间，来减少相互间的依赖。

缺点:

导致较多的ConcreteState子类

适用场景:

当一个对象的行为取决于它的状态，并且它必须在运行时刻根据状态改变它的行为时，就可以考虑使用状态模式来。

一个操作中含有庞大的分支结构，并且这些分支决定于对象的状态。

17.职责链:Chain Of Responsibleity

使多个对象都有机会处理请求，从而避免请求的发送者和接收者之间

的耦合关系。将这些对象连成一条链，并沿着这条链传递该请求 ，直到有

一个对象处理它为止。

职责链模式的优点:

降低耦合度

可简化对象的相互连接

增强给对象指派职责的灵活性

增加新的请求处理类很方便

职责链模式的缺点:

不能保证请求一定被接收。

系统性能将受到一定影响，而且在进行代码调试时不太方便;可能会造成循环调用。

在以下情况下可以使用职责链模式：

有多个对象可以处理同一个请求，具体哪个对象处理该请求由运行时刻自动确定。

在不明确指定接收者的情况下，向多个对象中的一个提交一个请求。

可动态指定一组对象处理请求。

18.解释器:Interpreter

给定一个语言，定义它的文法的一种表示，并定义一个解释器，这个

解释器，使用该表示来解释语言中的句子。

好处：

* 可以很容易地改变和拓展文法，因为该模式使用类

* 来表示文法规则，你可使用集成来改变或拓展该

* 文法。也比较容易实现文法，因为定义抽象语法树

* 中各个节点的类的实现大体类似，这些类都易于直接编写。

不足:

* 解释器模式为文法中的每一条规则至少定义了一个类

* 因此包含许多规则的文法可能难以管理和维护

* 建议当文法非常复杂时，使用其他的技术如语法

* 分析程序或编译器生成器来处理

适用环境：

①重复发生的问题可以使用解释器模式

②一个简单语法需要解释的场景

19.中介者:Mediator

用一个中介对象来封装一系列的对象交互。中介者使各对象不需要显

式地相互引用，从而使其耦合松散，而且可以独立地改变它们之间的交互。

中介者模式优点:

* 1.Mediator的出现减少了各个 Colleague 的耦合，使得

* 可以独立地改变和复用各个 Colleague类和Mediator

* 2由于把对象如何协作进行了抽象，将中介作为一个独立的

* 概念并将其封装在了一个对象中，这样关注的对象就从对象

* 各自本身的行为转移到它们之间的交互上来，也就是站在一个更宏观的角度去看待系统

缺点:

* 由于ConcreteMediator 控制了集中化，于是就把交互复杂性

* 变为了中介者的复杂性，这就使得中介者会变得比任何一个ConcreteColleague 都复杂

使用终结者模式的场合:

1.一组定义良好的对象，现在要进行复杂的通信。

2.定制一个分布在多个类中的行为，而又不想生成太多的子类。

中介对象主要是用来封装行为的，行为的参与者就是那些对象，但是通过中介者，这些对象不用相互知道。

20.访问者:Visitor

一个作用于某对象结构中的各元素的操作。它使你可以在不改变元素

的类的前提下定义作用于这些元素的新操作。

优点:

1、使得新增新的访问操作变得更加简单。

2、能够使得用户在不修改现有类的层次结构下，定义该类层次结构的操作。

3、将有关元素对象的访问行为集中到一个访问者对象中，而不是分散搞一个个的元素类中。

缺点:

1、增加新的元素类很困难。在访问者模式中，每增加一个新的元素类都意味着要在抽象访问者角色中

增加一个新的抽象操作，并在每一个具体访问者类中增加相应的具体操作，违背了“开闭原则”的要求。

2、破坏封装。当采用访问者模式的时候，就会打破组合类的封装。

3、比较难理解。貌似是最难的设计模式了。

模式适用场景:

1、对象结构中对象对应的类很少改变，但经常需要在此对象结构上定义新的操作。

2、需要对一个对象结构中的对象进行很多不同的并且不相关的操作，而需要避免让

这些操作“污染”这些对象的类，也不希望在增加新操作时修改这些类。

21.策略:Strategy

定义一系列算法，把它们一个个封装起来，并且使它们可替换。本模

式使得算法可独立于使用它的客户而变化。

优点:

策略类之间可以自由切换，由于策略类实现自同一个抽象，所以他们之间可以自由切换。

易于扩展，增加一个新的策略对策略模式来说非常容易，基本上可以在不改变原有代码的基础上进行扩展。

避免使用多重条件.

缺点:

维护各个策略类会给开发带来额外开销

必须对客户端(调用者)暴露所有的策略类

模式适用场景:

1)许多相关的类仅仅是行为有异。

2)需要使用一个算法的不同变体。

3)算法使用客户不应该知道的数据。

4)一个类定义了多种行为 , 并且这些行为在这个类的操作中以多个条件语句的形式出现。

22.备忘录:Memento

不破坏封装性的前提下，捕获一个对象的内部状态，并在该对象之外

保持这个状态。这样以后就可将该对象恢复到原先保存的状态。

使用备忘录模式的好处：

1)有时一些发起人对象的内部信息必须保存在发起人对象以外的地方，但是必须要由发起人对象自己读取，

这时使用备忘录模式可以把复杂的发起人内部信息对其他的对象屏蔽起来，从而可以恰当地保持封装的边界。

2)本模式简化了发起人类。发起人不再需要管理和保存其内部状态的一个个版本，客户端可以自

行管理他们所需要的这些状态的版本。

3)当发起人角色的状态改变的时候，有可能这个状态无效，这时候就可以使用暂时存储起来的备忘录将状态复原。

使用备忘录模式的缺点：

1)如果发起人角色的状态需要完整地存储到备忘录对象中，那么在资源消耗上面备忘录对象会很昂贵。

2)当负责人角色将一个备忘录存储起来的时候，负责人可能并不知道这个状态会占用多大的存储空间，

从而无法提醒用户一个操作是否很昂贵。

使用备忘录模式的场合：

1)功能比较复杂的，但是需要维护或记录属性历史的类。

2)需要保存的属性只是众多属性的一小部分时。

23.迭代器:Iterator

提供一种方法顺序访问一个聚合对象中各个元素，而又不需暴露该对

象的内部表示。

迭代器模式的优点有：

1、它支持以不同的方式遍历一个聚合对象。

2、迭代器简化了聚合类。

3、在同一个聚合上可以有多个遍历。

4、在迭代器模式中，增加新的聚合类和迭代器类都很方便，无须修改原有代码。

迭代器模式的缺点：

对于比较简单的遍历(像数组或者有序列表)，使用迭代器方式遍历较为繁琐

迭代器模式的适用场景:

1、访问一个聚合对象的内容而无须暴露它的内部表示。

2、需要为聚合对象提供多种遍历方式。

3、为遍历不同的聚合结构提供一个统一的接口。