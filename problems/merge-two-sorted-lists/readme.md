### Solutions

O(n)

```javascript
/**
 * @param {ListNode} list1
 * @param {ListNode} list2
 * @return {ListNode}
 */
const mergeTwoLists = function (list1, list2) {
    const result = { next: null }
    let pointer = result
    while (list1 && list2) {
        if (list1.val < list2.val) {
            pointer.next = list1
            list1 = list1.next
        } else {
            pointer.next = list2
            list2 = list2.next
        }
        pointer = pointer.next
    }
    pointer.next = list1 || list2
    return result.next
}
```
