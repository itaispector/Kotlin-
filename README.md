# Kotlin-FAQ

## What does `data class` keyword stands for?<br>
[https://kotlinlang.org/docs/reference/data-classes.html](reference)

## What does `open class` keyword stands for?<br>
The open annotation on a class is the opposite of Java's final: it allows others to inherit from this class. By default, all classes in Kotlin are final, which corresponds to Effective Java, 3rd Edition, Item 19: Design and document for inheritance or else prohibit it.

## How to write static class functions?
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
