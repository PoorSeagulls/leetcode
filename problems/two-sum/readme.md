### Solutions

O(n^2)

```go
func twoSum(nums []int, target int) []int {
    for i := 0; i < len(nums) - 1; i++ {
        for j := i + 1; j < len(nums); j++ {
            if nums[i] + nums[j] == target {
                return []int{i, j}
            }
        }
    }
    
    return []int{}
}
```

O(n)

```go
func twoSum(nums []int, target int) []int {
    m := make(map[int]int)
    for i := 0; i < len(nums); i++ {
        comp := target - nums[i]
        if val, ok := m[comp]; ok {
            return []int{val, i}
        }
        m[nums[i]] = i
    }
    
    return []int{}
}
```
