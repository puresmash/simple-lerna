
## Install

```shell
npm i -g lerna
git init simple-lerna
cd simple-lerna
lerna init
```

## Test Mechanism

### Setup Environment First

**my-lib**

```
mkdir my-lib
cd my-lib
npm init
touch index.js
```

index.js

```
module.exports = function add(a, b) {
    return a + b;
}
```

**my-app**

```
mkdir my-app
cd my-app
npm init
touch index.js
```

index.js

```
const add = require('my-lib');
console.log(add(1, 2));

```

package.json

```
"dependencies": {
  "my-lib": "1.0.0"
},
```

### Maintain Dependencies Automatically

```
lerna bootstrap
```

### Run to Test

```
node packages/my-app/index.js
```
