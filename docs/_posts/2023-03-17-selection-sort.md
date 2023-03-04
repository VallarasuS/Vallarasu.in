---
layout: post
category: Algorithms
---

### Algorithm

Seek from left to right for min element. Move min element to the left, and repeat with sub un-sorted list till the end.

![Selection Sort Example](https://raw.githubusercontent.com/VallarasuS/Vallarasu.in/master/docs/_screenshots/selection-sort.png)

```
    public void selectionSort(int[] nums) {

        for(int i = 0; i < nums.length; i++) {
           int min = i;

           for(int j = i; j < nums.length; j ++) {
               if(nums[min] > nums[j]) {
                   min = j;
               }
           }

           int item = nums[i];
           nums[i] = nums[min];
           nums[min] = item;
        }
    }

```