Governator provides an easy to use JUnit @Rule that simplifies testing.  The rule can be easily configured using the {@link LifecycleInjectorBuilder} or by grouping sets of operations with a {@link LifecycleInjectorBuilderSuite}

```java
public class MyUnitTest {
    @Rule
    public LifecycleTester tester = new LifecycleTester(new FooTestSuite());
    
    @Test
    public void test() {
        // Test specific setup 
        tester.builder().
           withAdditionalModule(new BarModule());
        
        // Create the injector and start LifecycleManager
        tester.start();
         
        // ... Your test code goes here
          
    } // On termination the LifecycleTester will shutdown LifecycleManager
}
```
