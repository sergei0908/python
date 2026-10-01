645. Несовпадение наборов

![условие задачи](645.png)

```python
class Solution:
    def findErrorNums(self, nums: list[int]) -> list[int]:
        n = len(nums)
        sm = sum(set(nums))
        return [sum(nums) - sm, n * (n + 1) // 2 - sm]
```


189. Rotate Array

![условие задачи](189.png)

```python
class Solution:
    def rotate(self, nums: list[int], k: int) -> None:
        n = len(nums)
        k %= n

        def mirror(l, r):
            while l < r:
                nums[r], nums[l] = nums[l], nums[r]
                l += 1
                r -= 1
        
        mirror(0, n - 1)
        mirror(0, k - 1)
        mirror(k, n - 1)
```
