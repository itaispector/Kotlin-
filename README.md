# Kotlin-FAQ

### Language idioms
[idioms](https://kotlinlang.org/docs/reference/idioms.html)

### What does `data class` keyword stands for?<br>
[reference](https://kotlinlang.org/docs/reference/data-classes.html)

### What does `open class` keyword stands for?<br>
The open annotation on a class is the opposite of Java's final: it allows others to inherit from this class. By default, all classes in Kotlin are final, which corresponds to Effective Java, 3rd Edition, Item 19: Design and document for inheritance or else prohibit it.
 [reference](https://kotlinlang.org/docs/reference/classes.html#inheritance)

### How to write static class functions?
Here's an example:

```
class ExampleClass{

  companion object {
  
    val exampleVar = 0  
    
    // here is where you place all static functions, or variables.
    fun exampleFunction(){
      // do something
    }
  }
}
```

Then from another class:
```
...
ExampleClass.exampleFunction()
ExampleClass.exampleVar
```
