# Java



## Polymorphism

many form 的意思 一个事物多个形式  随机应变 处理不同情况

可以用基类指针统一管理派生类数组 然后在派生类中重载相同的函数 就可以不同的派生类执行不同的内容 

但是是使用同一个指针指向 非常natural

重载 添加@Override标记

有时一些函数和类并不需要创建实例 而是完全用来派生 就可以用abstract类 或者 abstract method

纯虚函数和虚基类

```public abstract xxx```

如果你编写的类完全成熟了 不需要别人来继承和重载它 你就可以使用**final**进行修饰 此时不该类不可以拓展

例如 String 类 内置的类就不可以继承 保证不会修改其关键功能

如果你编写的函数不希望被inherited后修改 同样可以添加final 表示该函数不可以扩展

two much good things are making bad things

因此不要创建过多的继承 会导致一个很深的继承树 代码很难维护 上层基类的改变会影响下方继承的所有子类的修改

因此继承1-2 level 就行了 不要超过3层

Java 不支持多继承 这样太复杂了 一个类继承了多个类的特性 容易冲突 **菱形继承** 但我们不需要这种复杂技术

C++中的解决方法就是明确指出菱形继承中的函数到底所属谁 Student:: 还是 Teacher::



## Interfaces

A使用B的功能 那么B就提供给A interface

- loose-coupling 减少 API 的数量 避免形成过于依赖的局面 否则将难以维护

- extensible 两者应该都有自己独立的生活圈 扩展性强

- testable

A 和 B 不应该直接相连 而是应该通过一个Interface作为中间人进行连接

但是Interface不具体实现该内容 而是理所应当认为该内容已经被实现

Interface: What should be done

Classes: How it should be done

e.g.

在例子中 我们如果直接使用该类 private double taxableIncome  xxxx

相当于直接在内部使用了该类 如果该类的一丁点发生变化 该函数 或者使用该类的所有函数都会发生变化

蝴蝶效应 导致代码更改困难

所以我们需要interface

public interface TaxCalculator xxx

其中的代码不需要声明为public 因为interface本来就是给人使用的 全都是public

在你要实现该Interface的类中声明 implements 

需要实现的函数在Interface中声明 在实现时使用@Override



使用时不需要关心创建 只需要关心如何使用 separate

### dependency injection

- #### Constructor injection

```java
// constructor injection
public TaxReport(TaxCalculator calculator) {
    this.calculator = calculator;
}
```

​	不在TaxReport内部创建TaxCalculator接口 而是通过参数传递的方式传入 我们就无需在类中关心该类的创建 而只在main中考虑该参数传递如何进行

- #### Setter Injection

tips ：alt + shift + 上下 可以拖动代码

```java
public void setCalculator(TaxCalculator calculator) {
    this.calculator = calculator;
}
```

​	通过接口进行set 而不是依赖于某个特定的类

- #### Method Injection

```java
public void show(TaxCalculator calculator) {
    var tax = calculator.calculateTax();
    System.out.println(tax);
}
```

​	利用传入的interface来show 而不是利用已有的内容 进一步解除依赖



确保Interface small 以及 lightweight  目的就是让他们变化得不是那么频繁



## Interface Segregation Principle

把复杂的内容 切分成一个一个小的interface

如果将一个巨大的内容都整合成一个interface 那么在其中一部分内容需要修改时 就需要改动全局 这样就丧失了interface的优越性

一个interface最好专注于一个功能

interface 可以有多个继承对象 例如从一个大功能切分出去多个interface 你可以将一个派生类 利用多继承的方式统一该接口 即做到了接口的分离开发 又做到了统一使用 各个interface独立 均继承于派生类

统一的接口又该如何初始化？应该是无法初始化

因为无法定义一个统一的类去包含所有元素 这样做也不太好 就把它们合并了 但是没有分开

