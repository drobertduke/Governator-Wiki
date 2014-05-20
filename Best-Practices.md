This page provides examples and best practices guidelines to follow when writing DI friendly code

h2. Best Practices

h3. Modules should be side effect free

Don't allocate data or have any conditional logic in a Guice module.  

h3. Don't inject the Injector

Unless you are writing a generic framework most situations in which you want to Inject the injector can be solved by writing a Provider.

h3. Be careful with AutoBindSingleton

When writing libraries keep in mind that classpath scanning of AutoBindSingleton classes will result in those classes being created eagerly when the injector is created.  Too broad a set of a packages to scan can result in unwanted singletons being created.  
 
h2. Examples

h3. Configuration driven binding

Comings soon...

h3. Plugin architecture using multi-bindings

Coming soon..