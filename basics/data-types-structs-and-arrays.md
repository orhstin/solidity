# Data types, structs and arrays

Other than the normal primitive data types of a typical programming language; uint, string etc

structs -> a data type that can contain multiple properties

Types of arrays in Solidity include fixed arrays and dynamic arrays.

Fixed Arrays include a declaration of the length of the array, where it would be blank in a dynamic array.

{% code lineNumbers="true" %}
```solidity
uint[2] fixedArray;
string[5] stringArray;
uint[] dynamicArray;
```
{% endcode %}

An array declaration also comes with the intended data type, hence an array of structs is also possible.

{% code lineNumbers="true" %}
```solidity
Person[] people;
Person[] public people;
```
{% endcode %}

Since state variables are permanently stored in the blockchain, a dynamic array of structs is useful when storing structured data in a contract, like a database of sorts.

When storing public data, a visibility modifier like public can be declared, like in Line 2. Solidity creates a getter method for it.
