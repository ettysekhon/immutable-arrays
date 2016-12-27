# Immutable Arrays

Push
---
```
// es5
const push = (arr, newItem) => [].concat(arr, newItem);
```
or
```
// es2015
const push = (arr, newItem) => [ ...arr, newItem ];
```

Pop
---
```
// es5
const pop = (arr) => arr.slice(0, -1);
```

Shift
---
```
// es5
const shift = (arr) => arr.slice(1);
```

Unshift
---
```
// es5
const unshift = (arr, newItem) => [].concat(newItem, arr);
```
or
```
// es2015
const unshift = (arr, newItem) => [ newItem, ...arr ];
```
Splice
---
```
// es2015
const splice = (arr, start, deleteCount, ...item) => [ ...arr.slice(0, start), ...items, ...arr.slice(start + deleteCount);
```
or
```
// es5
const splice = (arr, start, deleteCount) => {
  const len = arguments.length;
  let items = Array(len > 3 ? len - 3 : 0);
  for (let key = 3; key < len; key++) {
    items[key - 3] = arguments[key];
  }
  return [].concat(arr.slice(0, start), items, arr.slice(start + deleteCount));
}
```
Delete
---
```
// es5
const delete  = (arr, index) => arr.slice(0,index).concat(arr.slice(index+1));
```

Copy
---
```
// es5
const copy = (arr) => [].concat(arr);
```
or
```
// es2015
const copy = (arr) => [ ...arr ];
