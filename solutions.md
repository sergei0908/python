645. Несовпадение наборов

![условие задачи](images/645.png)

```python
class Solution:
    def findErrorNums(self, nums: list[int]) -> list[int]:
        n = len(nums)
        sm = sum(set(nums))
        return [sum(nums) - sm, n * (n + 1) // 2 - sm]
```
