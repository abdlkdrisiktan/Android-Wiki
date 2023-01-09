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

