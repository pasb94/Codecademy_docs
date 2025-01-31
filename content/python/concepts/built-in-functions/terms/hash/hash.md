---
Title: 'hash()'
Description: 'Returns the hash value as a fixed sized integer'
Subjects:
- 'Data Science'
- 'Computer Science'
Tags:
- 'Integers'
- 'Functions'
- 'Input'
- 'Methods'
- 'Output'
- 'Print'
CatalogContent:
- 'Learn Python 3'
- 'Learn Data Structures and Algorithms with Python'

---

The built-in **hash()** function returns the hash value of an **object** as a **fixed sized integer**. The object can be of various types, including **numbers, strings, tuples, or custom objects** that have implemented the **hash()** method. The hash value is computed using a specific hashing algorithm based on the object's type. It's worth noting that the **hash()** function is a built-in function in Python and doesn't require any import statements. Hash values are useful for efficient comparison of dictionary keys during lookups.

## Syntax

```pseudo
hash(object)
```

The **hash()** function takes a single argument, object, which represents the object for which you want to obtain the hash value.
The object can be of any hashable type, such as numbers, strings, tuples, or custom objects that implement the **hash()** method.

## Example

In the example below, we have a class called **MyClass** with an **attribute** called value. The **hash()** method is implemented to customize the hashing behavior based on the value **attribute** using the **hash()** function.

Two instances of **MyClass** obj1 and obj2, are created with different values. The **hash()** function is used to calculate the hash values of these objects.

Then, we print the hash values of these objects using the **print(hash(obj1)) and print(hash(obj))** (https://www.codecademy.com/resources/docs/python/built-in-functions/print) command.

This example demonstrates how to customize the hash function for a class using the **hash()** method. The **hash()** function allows us to obtain the hash value of an object, which is an integer used for quick comparison and dictionary key lookups.

```py
# Define a class
class MyClass:
    def __init__(self, value):
        self.value = value

    def __hash__(self):
        return hash(self.value)

# Create instances of MyClass
obj1 = MyClass(42)
obj2 = MyClass("Hello")

# Check the hash values
print(hash(obj1))
print(hash(obj2))
```

## Codebyte Example

In the example below, we define **my_tuple** as "1, 2, 3". Subsequently, we use the **hash()** function to obtain the hash value of the input **my_tuple**. Followed by using the **print()** function in order to print the output of the **hash()** function.

```codebyte/python
my_tuple = (1, 2, 3)
hash_value = hash(my_tuple)
print(hash_value)
