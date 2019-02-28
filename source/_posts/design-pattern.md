---
title: 设计模式 - Design Pattern
date: 2019-02-14 11:40:58
tags:
- java
- 设计模式
- Design Pattern
categories: 
- java
---

https://en.wikipedia.org/wiki/Software_design_pattern

**OOP特性**：封装、继承、多态

**OOP原则**：单一职责原则、开放封闭原则、里氏替换原则、依赖倒置原则、接口隔离原则、最小知识原则

**OOP好处**：易维护、易复用、易扩展、灵活性好

设计模式就是利用OOP特性，遵循OOP原则，达到OOP好处的最佳实践。

## 设计原则

- **单一职责原则**： 一个类应该仅有一个引起它变化的原因。
- **开放封闭原则**：模块应对扩展开放，而对修改关闭。
- **里氏替换原则**：子类只能去扩展基类，而不是隐藏或覆盖基类。
- **依赖倒置原则**：高层模块不依赖底层模块，两个都应该依赖抽象；抽象不依赖细节，细节依赖抽象。
- **接口隔离原则**：将大的接口打散成多个小接口。
- **最小知识原则**：一个对象应当尽可能少的去了解其他对象。
- **合成复用原则**：要尽量使用合成，尽量不要使用继承。

<!-- more -->

## 模式列表

### 创建型模式

#### 单例 - Singleton

确保一个类只有一个实例，并提供对该实例的全局访问。

{% asset_img Singleton_UML.svg %}

#### 原型 - Prototype

用原型实例指定创建对象的种类，并且通过拷贝这些原型，创建新的对象。

{% asset_img Prototype_UML.svg %}

#### 建造者 - Builder

将一个复杂对象的构建与它的表示分离，使得同样的构建过程可以创建不同的表示。

{% asset_img Builder_UML.svg %}

#### 工厂方法 - Factory Method

定义一个接口用于创建对象，但是让子类决定初始化哪个类。工厂方法把一个类的初始化下放到子类。

{% asset_img FactoryMethod_UML.svg %}

#### 抽象工厂 - Abstract Factory

为一个产品族提供了统一的创建接口。当需要这个产品族的某一系列的时候，可以从抽象工厂中选出相应的系列创建一个具体的工厂类。

{% asset_img AbstractFactory_UML.svg %}

### 结构型模式

#### 适配器 - Adapter

将某个类的接口转换成客户端期望的另一个接口表示。适配器模式可以消除由于接口不匹配所造成的类兼容性问题。

{% asset_img ObjectAdapter.png %}

#### 桥接 - Birdge

将一个抽象与实现解耦，以便两者可以独立的变化。

{% asset_img Bridge_UML.svg %}

#### 组合 - Composite

把多个对象组成树状结构来表示局部与整体，这样用户可以一样的对待单个对象和对象的组合。

{% asset_img Composite_UML.svg %}

#### 装饰 - Decorator

向某个对象动态地添加更多的功能。修饰模式是除类继承外另一种扩展功能的方法。

{% asset_img Decorator_UML.svg %}

#### 外观 - Facade

为子系统中的一组接口提供一个一致的界面， 外观模式定义了一个高层接口，这个接口使得这一子系统更加容易使用。

{% asset_img Facade_UML.png %}

#### 享元 - Flyweight

通过共享以便有效的支持大量小颗粒对象。

{% asset_img Flyweight_UML.jpg %}

#### 代理 - Proxy

为其他对象提供一个代理以控制对这个对象的访问。

{% asset_img Proxy_UML.svg %}

### 行为型模式

#### 观察者 - Observer

在对象间定义一个一对多的联系性，由此当一个对象改变了状态，所有其他相关的对象会被通知并且自动刷新。

{% asset_img Observer_UML.svg %}

#### 模板方法 - Template Method

模板方法模式准备一个抽象类，将部分逻辑以具体方法及具体构造子类的形式实现，然后声明一些抽象方法来迫使子类实现剩余的逻辑。不同的子类可以以不同的方式实现这些抽象方法，从而对剩余的逻辑有不同的实现。先构建一个顶级逻辑框架，而将逻辑的细节留给具体的子类去实现。

{% asset_img TemplateMethod_UML.svg %}

#### 命令 - Command

将一个请求封装为一个对象，从而使你可用不同的请求对客户进行参数化；对请求排队或记录请求日志，以及支持可取消的操作。

{% asset_img Command_UML.svg %}

#### 状态 - State

让一个对象在其内部状态改变的时候，其行为也随之改变。状态模式需要对每一个系统可能获取的状态创立一个状态类的子类。当系统的状态变化时，系统便改变所选的子类。

{% asset_img State_UML.svg %}

#### 职责链 - Chain of Responsibility

为解除请求的发送者和接收者之间耦合，而使多个对象都有机会处理这个请求。将这些对象连成一条链，并沿着这条链传递该请求，直到有一个对象处理它。

{% asset_img Chain_of_responsibility_UML.png %}

#### 解释器 - Interpreter

给定一个语言, 定义它的文法的一种表示，并定义一个解释器, 该解释器使用该表示来解释语言中的句子。

{% asset_img Interpreter_UML.svg %}

#### 中介者 - Mediator

包装了一系列对象相互作用的方式，使得这些对象不必相互明显作用，从而使它们可以松散偶合。当某些对象之间的作用发生改变时，不会立即影响其他的一些对象之间的作用，保证这些作用可以彼此独立的变化。

{% asset_img Mediator_UML.png %}

#### 访问者 - Visitor

封装一些施加于某种数据结构元素之上的操作。一旦这些操作需要修改，接受这个操作的数据结构可以保持不变。访问者模式适用于数据结构相对未定的系统，它把数据结构和作用于结构上的操作之间的耦合解脱开，使得操作集合可以相对自由的演化。

{% asset_img Visitor_UML.svg %}

#### 策略 - Strategy

定义一个算法的系列，将其各个分装，并且使他们有交互性。策略模式使得算法在用户使用的时候能独立的改变。

{% asset_img Strategy_UML.svg %}

#### 备忘录 - Memento

备忘录对象是一个用来存储另外一个对象内部状态的快照的对象。备忘录模式的用意是在不破坏封装的条件下，将一个对象的状态捉住，并外部化，存储起来，从而可以在将来合适的时候把这个对象还原到存储起来的状态。

{% asset_img Memento_UML.png %}

#### 迭代器 - Iterator

提供一种方法顺序访问一个聚合对象中各个元素, 而又不需暴露该对象的内部表示。

{% asset_img Iterator_UML.svg %}

### 并发性模式

#### 主动对象 - Active Object

将方法执行放在自己的控制线程中与方法调用解耦。其目的是通过异步方法调用或用于处理请求的调度器来引入并发。

```java
// java 8
public class MyClass {
    private double val; 
    
    // container for tasks
    // decides which request to execute next 
    // asyncMode=true means our worker thread processes its local task queue in the FIFO order 
    // only single thread may modify internal state
    private final ForkJoinPool fj = new ForkJoinPool(1, ForkJoinPool.defaultForkJoinWorkerThreadFactory, null, true);
    
    // implementation of active object method
    public void doSomething() throws InterruptedException {
        fj.execute(() -> {val = 1.0;});
    }
 
    // implementation of active object method
    public void doSomethingElse() throws InterruptedException {
        fj.execute(() -> {val = 2.0;});
    }
}
```

#### 阻碍 - Balking

只在对象处于特定状态时对该对象执行操作。

```java
public class Example {
    private boolean jobInProgress = false;

    public void job() {
        synchronized(this) {
           if (jobInProgress) {
               return;
           }
           jobInProgress = true;
        }
        // Code to execute job goes here
        // ...
        jobCompleted();
    }

    void jobCompleted() {
        synchronized(this) {
            jobInProgress = false;
        }
    }
}
```

#### 绑定属性 - Binding properties

组合多个观察者以某种方式强制同步或协调不同对象中的属性。

绑定有两种类型：当其属性是只读的时，应该应用单向绑定；在其他情况下，必须应用双向绑定。

#### 双重检测锁 - Double-checked locking

首先以不安全的方式测试锁定标准，从而减少获取锁的开销；实际的锁定逻辑只有再次检测成功才会继续。



