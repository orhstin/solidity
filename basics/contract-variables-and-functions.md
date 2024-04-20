# Contract, variables and functions

Terminology

version pragma -> a declaration of the version of the Solidity compiler

Contract -> a fundamental building block of ETH applications.

State variables -> permanently stored in contract storage, written to the Ethereum blockchain

Function -> a function declaration would look something like this

<pre class="language-solidity"><code class="lang-solidity">function eatHamburgers(string memory <a data-footnote-ref href="#user-content-fn-1">_name</a>, uint _amount) public {
}
</code></pre>

The current structure of a function includes the name of the function, its parameters and the visibility. The _<mark style="color:yellow;">`memory`</mark>_ keyword serves as an instruction to store the variable in memory. This is required for all reference types such as arrays, structs, mappings and strings.

Reference type ->

1. By value, Solidity compiler creates a new copy of the parameter's value and passes it to the function. The function then modifies the value without changing the value of the initial parameter.
2. By reference, which means the function is called with a reference to the original variable. Hence if the function changes the value of the variable it receives, the value of the original variable gets changed.



A contract should contain variables and functions to perform certain operations pertaining to the purpose of the smart contract.

[^1]: Starting function parameter variable names with an underscore differentiates them from global variables. This is a convention.
