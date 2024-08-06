# README.md for Collections::Array

# Hi There 

## 🌟 Detailed Explanation of the Array Class 🌟

The `Array` class is a custom implementation that provides a versatile and dynamic way to manage a collection of elements. Below is a comprehensive breakdown of its components and functionalities.

### Overview

The `Array` class allows you to create and manage an array with various features such as adding, removing, and manipulating elements. It includes methods to perform operations like checking for the presence of an element, converting elements to different types, and more.

#### Key Components

**Attributes:**
- `ActualArray:` This is the underlying storage for array elements. It starts as an empty array and grows as needed.
- `Size:` This keeps track of the number of elements currently in the array.

**Methods:**
- `init(size): Initializes the array with a specified size, filling it with "Empty" values. This method prepares the array for use by setting its size.

- `Puts():` Prints the current state of the ActualArray. This method is useful for debugging and viewing the contents of the array.

- `Clear():` Empties the array and resets the size to zero. This is useful when you need to start fresh with a new array.

- `ToString():` Converts the array into a string representation. It joins all elements with a comma and space, providing a readable format of the array's contents.

- `Append(value):` Adds a new element to the end of the array and updates the size. This method is useful for dynamically growing the array.

- `RemoveAt(index):` Removes the element at the specified index and adjusts the array. If the index is out of bounds, it prints an error message.

- `InsertAt(index, value):` Inserts a new element at the specified index. It shifts existing elements as needed. If the index is out of bounds, it prints an error message.

- `Contains(value):` Checks if the array contains a specific value. It returns true if found, otherwise false.

- `IndexOf(value):` Finds the index of a specific value in the array. It returns the index if the value is found, or -1 if not.

- `Count():` Returns the number of elements currently in the array.

- `Count_not_empty():` Counts the number of elements in the array that are not "Empty". This method is useful for determining how many meaningful elements are in the array.

- `ToInt():` Converts numeric elements of the array to integers. Non-numeric values are skipped, and a message is printed if a value cannot be converted.

- `ToFloat():` Converts numeric elements of the array to floats. Similar to ToInt(), non-numeric values are skipped, and a message is printed for any conversion issues.

- `isNumeric(value):` A helper function to check if a value is numeric. This function supports the conversion of values to numeric types.

- `Splice(index, count, values...):` Removes a specified number of elements starting from the given index and then inserts new values. This method allows for complex manipulations of the array.

### Summary

The `Array` class provides a robust set of methods for managing a collection of items. Whether you need to initialize an array, manipulate its contents, or query its state, this class has the functionality to meet your needs. Use it to handle dynamic data and perform various array operations efficiently.

Feel free to explore and experiment with the `Array` class to leverage its full potential in your projects!


## 🌟 Detailed Explanation of the Complex Array Class 🌟

The `ComplexArray` class is a versatile base class designed to handle various types of arrays. It provides a foundational structure and methods that can be extended by derived classes to manage different data types and functionalities. Below is a comprehensive breakdown of its components and how they work.

### Overview

The `ComplexArray` class offers an abstraction for managing arrays with multiple functionalities, such as adding, removing, and querying elements. It supports various operations and provides utility methods to manipulate and convert data types.

### Key Components

1. **Attributes:**
   - `ActualArray`: Stores the elements of the array.
   - `Size`: Represents the size of the array.
   - `gSize`: A dynamic size indicator that changes as elements are added or removed.

2. **Methods:**

   - **`init(size)`**: Initializes the array with the given size. By default, it fills the array with `"Empty"` values.
   - **`Puts()`**: Prints the current state of the array to the console.
   - **`Clear()`**: Clears the array and resets its size.
   - **`ToStringArray()`**: Converts the array to a string representation where elements are separated by commas.
   - **`ToIntArray_unsafe()`**: Converts the array to an integer array, potentially causing errors with non-integer values.
   - **`ToFloatArray_unsafe()`**: Converts the array to a float array, similar to the integer conversion but for floating-point values.
   - **`ComplexToIntArray()`**: Safely converts the array to an integer array, handling various data types and exceptions.
   - **`ComplexToFloatArray()`**: Safely converts the array to a float array, with similar handling as the integer conversion.
   - **`property this[index]`**: Provides access to elements by index with bounds checking.
   - **`Append(value)`**: Adds a new element to the end of the array.
   - **`RemoveAt(index)`**: Removes an element at a specific index and adjusts the size accordingly.
   - **`InsertAt(index, value)`**: Inserts a new element at a specified index, shifting existing elements if necessary.
   - **`Contains(value)`**: Checks if a value exists in the array and returns `true` or `false`.
   - **`IndexOf(value)`**: Finds the index of a value in the array, returning `-1` if not found.
   - **`Count()`**: Returns the current size of the array.
   - **`Splice(index, count, values...)`**: Removes a portion of the array and optionally inserts new values.
   - **`ToSimpleArray()`**: Converts the complex array to a simple array of values.

### Derived Classes

The `ComplexArray` class is extended by various derived classes to handle specific types of arrays:

- **`StringArray`**: Manages arrays of strings and includes methods for converting to integer and float arrays.
- **`IntArray`**: Handles arrays of integers with similar conversion methods as `StringArray`.
- **`FloatArray`**: Manages arrays of floating-point numbers, also with conversion methods.
- **`HashArray`**: Designed for arrays of hash maps or dictionaries.
- **`ArrayArray`**: Manages arrays of arrays.
- **`TupleArray`**: Handles arrays of tuples.
- **`MatrixArray`**: Manages two-dimensional arrays (matrices) with methods for converting to integer and float arrays.
- **`Vector2Array`**: Handles arrays of `Vector2` objects.
- **`Vector3Array`**: Manages arrays of `Vector3` objects with additional conversion methods.

### Factory Functions

Factory functions are provided to create instances of these array types:

- `NewStringArray(size)`
- `NewIntArray(size)`
- `NewFloatArray(size)`
- `NewHashArray(size)`
- `NewArrayArray(size)`
- `NewTupleArray(size)`
- `NewMatrixArray(rows, cols)`
- `NewVector2Array(size)`
- `NewVector3Array(size)`


This class structure allows for flexible management of different data types in arrays, with a robust set of methods for data manipulation and conversion.


# Example Usage

## *collections_array/array.pkg**
```cpp
# Let's create a magical array of names! 🎩✨
namesObj = Array(7)  # We're summoning an array with 7 slots!

# Time to fill our array with some fabulous names! 👯‍♀️👯‍♂️
namesObj[0] = "Zara"     # Fashion icon alert! 👗
namesObj[1] = "Riz"      # Short name, big personality! 💥
namesObj[2] = "Nuha"     # Sounds like a sneeze, but it's a name! 🤧
namesObj[3] = "Asif"     # As if by magic, this name appeared! 🔮
namesObj[4] = "Davinder" # Defender of the Dave-kind! 🦸‍♂️
namesObj[5] = "Sunil"    # Bringing sunshine to our array! ☀️
namesObj[6] = "Rubic"    # Cube-solving champion! 🧊

# Let's see what we've conjured up! 👀
namesObj.Puts()

# Time for a roll call! Who's in our magical array? 📢
for i in range(namesObj.Size):
    print(namesObj[i])  # Shout out loud, array elements! 🗣️

# Let's spice things up with some array acrobatics! 🤸‍♀️

# New name just dropped! 🎤
namesObj.Append("NewName")  # Making room for one more!

# Oops, someone's gotta go! 👋
namesObj.RemoveAt(2)  # Sorry, Nuha, you've been voted off the island!

# Surprise entrance! 🎭
namesObj.InsertAt(1, "InsertedName")  # Squeezing in like it's the last seat on a bus!

# Splice and dice! 🔪
namesObj.Splice(3, 2, "SplicedName1", "SplicedName2")  # Chop chop, swap swap!

# Let's play detective! 🕵️‍♀️
print("Contains 'Sunil':", namesObj.Contains("Sunil"))  # Is Sunil still hanging around?
print("Index of 'Asif':", namesObj.IndexOf("Asif"))  # Where oh where has Asif gone?

# Time for a headcount! 🧮
print("Count:", namesObj.Count())  # How many names are partying in our array?
print("Count (not empty):", namesObj.Count_not_empty())  # Who actually showed up to the party?

# Let's get numerical! 🔢
namesObj.Append(123)     # Sneaking in a number, are we? 😏
namesObj.Append(456.78)  # Ooh, fancy decimal! 💅
namesObj.Append("abc")   # ABC, easy as 123! 🎶

# Time to separate the numbers from the letters! 📊
print("ToInt:", namesObj.ToInt())    # Only the strong (numbers) survive!
print("ToFloat:", namesObj.ToFloat())  # Floaty floats, unite!

# Grand finale: The great string reveal! 🎭
print(namesObj.ToString())  # All together now, in one harmonious string!
print(type(namesObj.ToString()))  # What kind of beast have we created? 🧟‍♂️
```

## **collections_array/cArray.pkg**

```cpp
void ExampleUsage() {
    // Example for StringArray
    let stringArray = NewStringArray(5)  // Create a new StringArray with 5 elements
    stringArray[0] = "10"
    stringArray[1] = "20.5"
    stringArray[2] = "hello"
    stringArray[3] = "30"
    stringArray[4] = "40.7"

    console.Println("StringArray:", stringArray.Puts())  // Display the array contents
    console.Println("StringArray to IntArray:", stringArray.ToIntArray())  // Attempt to convert to integers
    console.Println("StringArray to FloatArray:", stringArray.ToFloatArray())  // Attempt to convert to floats

    // Example for IntArray
    let intArray = NewIntArray(3)  // Create a new IntArray with 3 elements
    intArray[0] = 1
    intArray[1] = 2
    intArray[2] = 3

    console.Println("IntArray:", intArray.Puts())
    console.Println("IntArray to StringArray:", intArray.ToStringArray())  // Convert to string representation
    console.Println("IntArray to FloatArray:", intArray.ToFloatArray())  // Convert to float values

    // Example for FloatArray
    let floatArray = NewFloatArray(4)  // Create a new FloatArray with 4 elements
    floatArray[0] = 1.5
    floatArray[1] = 2.5
    floatArray[2] = 3.5
    floatArray[3] = 4.5

    console.Println("FloatArray:", floatArray.Puts())
    console.Println("FloatArray to StringArray:", floatArray.ToStringArray())
    console.Println("FloatArray to IntArray:", floatArray.ToIntArray())  // Convert to integer values (truncating)

    // Example for HashArray
    let hashArray = NewHashArray(2)  // Create a new HashArray with 2 elements
    hashArray[0] = {"key1": "value1"}
    hashArray[1] = {"key2": "value2"}

    console.Println("HashArray:", hashArray.Puts())

    // Example for ArrayArray
    let arrayArray = NewArrayArray(3)  // Create a new ArrayArray with 3 elements
    arrayArray[0] = [1, 2]
    arrayArray[1] = [3, 4]
    arrayArray[2] = [5, 6]

    console.Println("ArrayArray:", arrayArray.Puts())

    // Example for TupleArray
    let tupleArray = NewTupleArray(3)  // Create a new TupleArray with 3 elements
    tupleArray[0] = (1, "a")
    tupleArray[1] = (2, "b")
    tupleArray[2] = (3, "c")

    console.Println("TupleArray:", tupleArray.Puts())

    // Example for MatrixArray
    let matrixArray = NewMatrixArray(2, 3)  // Create a new MatrixArray with 2 rows and 3 columns
    matrixArray[0][0] = 1
    matrixArray[0][1] = 2
    matrixArray[0][2] = 3
    matrixArray[1][0] = 4
    matrixArray[1][1] = 5
    matrixArray[1][2] = 6

    console.Println("MatrixArray:", matrixArray.Puts())
    console.Println("MatrixArray to IntArray:", matrixArray.ToIntArray())
    console.Println("MatrixArray to FloatArray:", matrixArray.ToFloatArray())

    // Example for Vector2Array
    let vector2Array = NewVector2Array(2)  // Create a new Vector2Array with 2 elements
    vector2Array[0] = new Vector2(1, 2)
    vector2Array[1] = new Vector2(3, 4)

    console.Println("Vector2Array:", vector2Array.Puts())
    console.Println("Vector2Array to SimpleArray:", vector2Array.ToSimpleArray())

    // Example for Vector3Array
    let vector3Array = NewVector3Array(2)  // Create a new Vector3Array with 2 elements
    vector3Array[0] = new Vector3(1, 2, 3)
    vector3Array[1] = new Vector3(4, 5, 6)

    console.Println("Vector3Array:", vector3Array.Puts())
    console.Println("Vector3Array to SimpleArray:", vector3Array.ToSimpleArray())
    console.Println("Vector3Array to IntArray:", vector3Array.ToIntArray())
    console.Println("Vector3Array to FloatArray:", vector3Array.ToFloatArray())

    // Example usage of Vector2 and Vector3 classes
    let vector2 = new Vector2(1, 2)
    let vector3 = new Vector3(3, 4, 5)
    console.Println("Vector2:", vector2.String())  // Display Vector2 as string
    console.Println("Vector3:", vector3.String())  // Display Vector3 as string

    let sumVector2 = vector2 + 5  // Add scalar to Vector2
    let sumVector3 = vector3 + 10  // Add scalar to Vector3
    console.Println("Vector2 + 5:", sumVector2.String())
    console.Println("Vector3 + 10:", sumVector3.String())

    let vector2FromVector3 = vector3 + vector2  // Add Vector2 to Vector3
    console.Println("Vector3 + Vector2:", vector2FromVector3.String())
}
```