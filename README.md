# Kotlin-FAQ

### Language idioms
[idioms](https://kotlinlang.org/docs/reference/idioms.html)

--
### What does `data class` keyword stands for?<br>
[reference](https://kotlinlang.org/docs/reference/data-classes.html)

--
### What does `open class` keyword stands for?<br>
The open annotation on a class is the opposite of Java's final: it allows others to inherit from this class. By default, all classes in Kotlin are final, which corresponds to Effective Java, 3rd Edition, Item 19: Design and document for inheritance or else prohibit it.
 [reference](https://kotlinlang.org/docs/reference/classes.html#inheritance)
 
--
### How to write static class functions?
####Important note:
>Note that, even though the members of companion objects look like
static members in other languages, **at runtime those are still
instance members of real objects**

> However, on the JVM you can have members of companion objects generated **as real static methods and fields**, if you use the `@JvmStatic` annotation

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

--
### Switch statement in Kotlin
Kotlin doesn't have `switch` keyword, instead, it uses `when` keyword, and in a different way like so:
```
when (x) {
    1 -> print("x == 1")
    2 -> print("x == 2")
    else -> { // Note the block
        print("x is neither 1 nor 2")
    }
}
```
