# Kotlin-FAQ

## What does `data class` keyword stands for?<br>
[https://kotlinlang.org/docs/reference/data-classes.html](reference)


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
