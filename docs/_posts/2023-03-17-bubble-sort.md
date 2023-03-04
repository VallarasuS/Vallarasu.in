---
layout: post
category: Algorithms
---

### Algorithm

- Start with one element in the list and compare it with immediate next element.
- If it is greater than next element, move it right
- Repate it with each element next to it, like the name says bubble up.

Same as [selection sort](selection-sort.html), except selection sort swaps max / min

```

    public void bubbleSort(int[] nums) {

        for(int i = 1; i < nums.length; i ++) {

            for(int j = 1; j < nums.length; j++) {

                if(nums[j - 1] > nums[j]) {
                    int item = nums[j];
                    nums[j] = nums[j - 1];
                    nums[j - 1] = item;
                }
            }
        }
    }

```