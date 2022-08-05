### Solutions

O(n)

```javascript
/**
 * @param {number} n
 * @return {boolean}
 */
const isPalindrome = (n) => {
  let _n = n
  let c = 0
  while (_n > 0) {
    c = c * 10 + (_n % 10)
    _n = Math.floor(_n / 10)
  }
  return c === n
}
```
