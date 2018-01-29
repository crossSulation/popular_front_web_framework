
# setTimeout

Synax: 语法
* var timeoutID = scope.setTimeout(function[, delay, param1, param2, ...]);
* var timeoutID = scope.setTimeout(function[, delay]);
* var timeoutID = scope.setTimeout(code[, delay]);

## Parameters

### function
A function to be executed after the timer expires.

### code
An alternative syntax that allows you to include a string instead of a function, which is compiled and executed when the timer expires. This syntax is not recommended for the same reasons that make using eval() a security risk.

### delay Optional
The time, in milliseconds (thousandths of a second), the timer should wait before the specified function or code is executed. If this parameter is omitted, a value of 0 is used, meaning execute "immediately", or more accurately, as soon as possible. Note that in either case, the actual delay may be longer than intended; see Reasons for delays longer than specified below.

### param1, ..., paramN Optional
Additional parameters which are passed through to the function specified by function or code once the timer expires.

## Return value:
The returned timeoutID is a positive integer value which identifies the timer created by the call to setTimeout(); this value can be passed to clearTimeout() to cancel the timeout.

It may be helpful to be aware that setTimeout() and setInterval() share the same pool of IDs, and that clearTimeout() and clearInterval() can technically be used interchangeably. For clarity, however, you should try to always match them to avoid confusion when maintaining your code.

It is guaranteed that a timeout ID will never be reused by a subsequent call to setTimeout() or setInterval() on the same object (a window or a worker). However, different objects use separate pools of IDs.

# setInterval
