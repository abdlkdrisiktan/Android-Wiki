# Kotlin Interview Questions

### Does kotlin have primitive types? [answer](https://stackoverflow.com/a/57408889/8356498)

### Lateinit vs Lazy 

Things to consider when we use the lateinit property:

    private lateinit var message: String

• Can be only used with the var keyword.

• Can be only used with a non-nullable variable.

• Should be used if the variable is mutable and can be initialized later.

• Should be used if you are sure about the initialization before use.

• lateinit properties can't be of primitive data types whereas lazy properties can be of primitive date types also. exp : Int is primitive types

• A lazy property can be of nullable type but a lateinit property can't be of nullable type.

Things to consider when we use the lazy property:

    private val message by lazy {
        println("creating the message")
        "hi"
    }
    
• Message print for once but variable always accessable.

• Can be only used with the val keyword, hence the read-only property.

• We want the variable to be initialized only if we need it for the first time.

• Must understand that it only creates the object when we access it for the very first time and then in the subsequent access, it returns the same object.

### What is Dispatchers in Kotlin?

Dispatchers in Kotlin Coroutines are like Schedulers in RxJava. There are 4 type of dispatchers have;

+ Dispatchers.Default

    * Doing heavy calculations
    
    * Doing any operations on bigger list present in memory; sorting, filtering, searching
    
    * Parsing JSON
    
    * You can not reading disk or drawing something on the view these fucntions have to be in main dispatchers.
    
    * Finally, if you have CPU-intensive task than you can use Dispatchers.Default.

+ Dispatchers.IO
    * Perform disk or network I/O related tasks.
    
    * Any network operations like making a netwwork call
    
    * Creating file or compressing file or moving file
    
    * Reading and writing a file
    
    * Reading database query

+ Dispatchers.Main

    * Performing UI-Related tasks

+ Dispatchers.Unconfined
    * If you dont care about the thread on which it should run

    


