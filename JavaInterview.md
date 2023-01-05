# Java Interview Questions

### Primitive Type ve Reference Type Nedir / Reference Type vs Value type?
Value type tipe direkt olarak değeri atadığımız işlemdir 
Reference type ise value type atanan değişkenin yeni değişkene value type edilmiş değişken üzerinden atanmasıdır.
Ama eğer ki bir sınıftan nesne türetiyorsak bu Reference Type değişkenidir.

Arasında ki farklar ise;
- Value Type değişkenler değeri direk olarak içerisinde taşır, Reference Type değişkenleri ise adından da anlaşılacağı gibi sadece referansı tutar.

- Value Type değişkenler null değer alamazken, Reference Type değişkenler ise null değeri alabilir.
 
- Value Type değişkenler Ram’de stack bölgesinde tutulurken, Reference Type değişkenler ise Ram’in heap bölgesinde tutulur.

### Integer ile int arasındaki fark nedir ?

### EqualsTo() ile '==' fark nedir ?

### Is String reference type? [answer](https://www.tutorialsteacher.com/csharp/csharp-value-type-and-reference-type#:~:text=String%20is%20a%20reference%20type,to%20the%20new%20memory%20location.)
- Yes String is reference type but it is immutable. It means once we assigned a value, it cannot be changed. If we change a string value, then the compiler creates a new string object in the memory and point a variable to the new memory location.
