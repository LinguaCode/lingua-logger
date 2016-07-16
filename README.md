# lingua-logger

## Description
Package **lingua-logger** is a hyper recursive logging tool which helps to create simple charts for a complex hyper recursions.

## Screenshot
![Screenshot](https://raw.githubusercontent.com/LinguaCode/lingua-logger/master/screenshots/image.png)

## How to install

```sh
$ npm install https://github.com/LinguaCode/lingua-logger --save
```

### Usage

##### require the **lingua-logger** module.
```javascript
var logger = require('lingua-logger');
```

##### prints single `message`.
```javascript
logger.log(message)
```

##### same as `logger.log`.
```javascript
console.llog(message)
```

##### prints single collapse's first `message`.
```javascript
console.llog(message, 'begin')
```

##### prints single collapse's last `message`.
```javascript
console.llog(message, 'end')
```

##### reset the indent level.
```javascript
logger.init()
```


## Example

### Code

```javascript
var logger = require('lingua-logger');

console.llog('single');
console.llog('1st level', 'begin');
console.llog('2nd level', 'begin');
console.llog('3rd level', 'begin');
console.llog('single');
console.llog('3rd level', 'end');
console.llog('2nd level', 'end');
console.llog('1st level', 'end');
console.llog('single');
```

### Output
```
single
1st level
    2nd level
        3rd level
            single
        3rd level
    2nd level
1st level
single
```

##License
LinguaCode is [licensed under GPLv3](https://github.com/LinguaCode/lingua-logger/blob/master/LICENSE).
