### Bitwise

> expert

```js
const bob = { name: 'Bob', permission: 0 };

const permissions = ['read', 'write', 'execute', 'delete'];

const getPermissionValue = (permArray) => {
  return permArray.reduce((acc, value) => {
    let index = permissions.indexOf(value);
    return index === -1 ? acc : acc | (1 << index);
  }, 0);
};

bob.permission = getPermissionValue(['read', 'execute', 'delete']); // 3
bob; // { name: 'Bob', permission: 3 }
bob.permission.toString(2) // 1101 it means the permissions array from right to left

const verifyOperation = (permission, permissions) => {
  return permission === (permission | getPermissionValue(permissions));
};

verifyOperation(bob.permission, ['read']); // true
verifyOperation(bob.permission, ['write']); // false
verifyOperation(bob.permission, ['execute']); // true
verifyOperation(bob.permission, ['execute', 'read']); // true
verifyOperation(bob.permission, ['read', 'write']); // false
```
