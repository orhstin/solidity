# Built-in functions/variables

`keccak256` is a built-in hash function that maps an input to a random 256-bit hexadecimal number. A slight change in the input results in a large change in the hash. Its useful for many purposes in Ethereum, but the main use would be to pseudo-randomness.

It expects a single parameter of type bytes, meaning any parameters have to be packed before calling it, with abi.encodePacked("insertStringValue");



## Global Variables

### msg.sender

Refers to the address of the person/smart contract that called the current function.

In Solidity, function executions always start with an external caller. There will \*_ALWAYS_\* be a msg.sender.

Example of using msg.sender in a context

```solidity
mapping (address => uint) favoriteNumber;

function setMyNumber(uint _myNumber) public {
    favoriteNumber[msg.sender] = _myNumber;
    // Setting the key to be the msg.sender address, and the value to be the number
}

function getMyNumber() public view returns (uint) {
    return favoriteNumber[msg.sender];
}
```
