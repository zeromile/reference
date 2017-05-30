REF: LIBRARY, FRAMEWORK, MODULE

from: http://stackoverflow.com/questions/4099975/difference-between-a-module-library-and-a-framework

All three of those provide functionality.
However, there are important differences.
A library is just a collection of related functionality. Nothing more, but also nothing less. The defining characteristic of a library is that you are in control, you call the library.
The defining characteristic of a framework is Inversion of Control. The framework calls you, not the other way round. (This is known as the Hollywood Principle: "Don't call us, we'll call you.") The framework is in control. The flow of control and the flow of data is managed by the framework.
You can think of it this way: in both cases, you have an application, and this application has holes in it, where code has been left out, and these holes need to be filled in. The difference between a library and a framework is
* who writes the application,
* what are the holes and
* who fills in the holes.
With a library, you write the application, and you leave out the boring details, which gets filled in by a library.
With a framework, the framework writer writes the application, and leaves out the interestingdetails, which you fill in.
This can be a little confusing at times, because the framework itself might also contain boring details, that the framework author filled in with libraries, the parts that you write might contain boring details, that you fill in with libraries, and the framework might provide a set of bundled libraries that either work well with the framework or that are often needed in conjunction with the framework. For example, you might use an XML generator library when writing a web application using a web framework, and that XML library might have been provided by the framework or even be an integral part of it.
That doesn't mean, however, that there is no distinction between a library and a framework. The distinction is very clear: Inversion of Control is what it's all about.
The defining characteristic of a module is information hiding. A module has an interface, which explicitly, but abstractly specifies both the functionality it provides as well as the functionality it depends on. (Often called the exported and imported functionality.) This interface has animplementation (or multiple implementations, actually), which, from the user of a module are a black box.
Also, a library is a collection of related functionality, whereas a module only provides a single pieceof functionality. Which means that, if you have a system with both modules and libraries, a library will typically contain multiple modules. For example, you might have a collections library which contains a List module, a Set module and a Map module.
While you can certainly write modules without a module system, ideally you want your modules to be separately compilable (for languages and execution environments where that notion even makes sense), separately deployable, and you want module composition to be safe (i.e. composing modules should either work or trigger an error before runtime, but never lead to an runtime error or unexpected behavior). For this, you need a module system, like Racket's units, Standard ML's modules and functors or Newspeak's top-level classes.
So, let's recap:
* library: collection of related functionality
* framework: Inversion of Control
* module: abstract interface with explicit exports and imports, implementation and interface are separate, there may be multiple implementations and the implementation is hidden
