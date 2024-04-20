# Events

Events are a way for the contract to communicate that something happened on chain to the application's front-end, listening for certain events to take action when they happen.

Example:

```solidity
event IntegersAdded(uint x, uint y, uint result);

function add(uint _x, uint _y) public pure returns (uint) {
    uint result = _x + _y;
    emit IntegersAdded(_x, _y, result);
    return result;
}
```

With the front-end implementation listening, the JavaScript code could look something like:

```javascript
YourContract.IntegersAdded(function(error, result) {
})
```
