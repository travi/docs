# Overview

## What is stampit

`stampit` is a JavaScript module which implements the [**stamp** specification](https://www.gitbook.com/book/stampit-org/docs/edit#). **Stamps** are composable factory functions.

**Think of **_**stamps**_** as classic classes but without any limits, boundaries, or rules.**

The stamps brag large amount of features and things you can do with your objects and/or stamps.

Head straight to the [Quick Start](https://github.com/stampit-org/docs/tree/cb1b11dcef3e3b0b3aa5212adcf9047a2f882b06/start.md) page for code examples.

![](../.gitbook/assets/class_vs_stamp.png)

## Differences from classes

* Inheritance
  * Classes
    * Classes do child+parent+parent+parent... inheritance chains. See picture above.
    * When you extend a class you link class prototypes.
  * Stamps
    * Stamp are single object + single prototype. See picture above.
    * When you "extend" you separately merge [methods](https://github.com/stampit-org/docs/tree/cb1b11dcef3e3b0b3aa5212adcf9047a2f882b06/methods.md), separately merge [properties](https://github.com/stampit-org/docs/tree/cb1b11dcef3e3b0b3aa5212adcf9047a2f882b06/properties.md), separately merge [static properties](https://github.com/stampit-org/docs/tree/cb1b11dcef3e3b0b3aa5212adcf9047a2f882b06/static-properties.md), separately merge [initializers](https://github.com/stampit-org/docs/tree/cb1b11dcef3e3b0b3aa5212adcf9047a2f882b06/initializers.md) \(aka constructors\), etc etc etc.
    * That's why it is not just inheritance, but special type of object composition. The stamp composition algorithm is [standardized](specification/merging-algorithm.md).
    * You can influence composition result with your code at runtime using the [composers](https://github.com/stampit-org/docs/tree/cb1b11dcef3e3b0b3aa5212adcf9047a2f882b06/composers.md) feature.
* Object creation
  * Classes
    * In most programming languages you execute only one constructor per class.
    * To pass data to the parent constructor you have to manually call parent constructor `this.super(data)`.
    * To create an object you need to use the `new` keyword: `const object = new MyClass()`.
  * Stamps
    * Stamp executes every initializer \(aka constructor\) it has.
    * All initializers receive exactly the same set of arguments, no need to manually pass data.
    * The initializer execution sequence is the same as the stamp composition sequence.
    * To create an object you [call stamp](https://github.com/stampit-org/docs/tree/cb1b11dcef3e3b0b3aa5212adcf9047a2f882b06/start.md) as a function: `const object = MyStamp()`.

## History

The original idea of Stamps belongs to [Eric Elliott](https://ericelliottjs.com/). See his [first commit](https://github.com/stampit-org/stampit/commit/ac330e8537e349a9640bbe4a34c63150db445a20) from 11 Feb 2013 in the stampit repository. Since then the idea evolved to the [specification](https://github.com/stampit-org/docs/tree/cb1b11dcef3e3b0b3aa5212adcf9047a2f882b06/specification.md) and a whole [ecosystem](https://github.com/stampit-org/docs/tree/cb1b11dcef3e3b0b3aa5212adcf9047a2f882b06/ecosystem.md) of mini modules.

## Using Stamps

Head straight to the [Quick start](https://github.com/stampit-org/docs/tree/cb1b11dcef3e3b0b3aa5212adcf9047a2f882b06/start.md) for code examples.

## Ecosystem

Stampit have a lot of helper modules. You can always find the list of official NPM packages here: [https://www.npmjs.com/~stamp](https://www.npmjs.com/~stamp)

See more information on the [Ecosystem](https://github.com/stampit-org/docs/tree/cb1b11dcef3e3b0b3aa5212adcf9047a2f882b06/ecosystem.md) page.
