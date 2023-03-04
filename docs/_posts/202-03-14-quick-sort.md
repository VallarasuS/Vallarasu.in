---
layout: post
category: Algorithms
---

### Algorithm

Quick sort is a divide and conquer algorithm, and it works like this
- Given an array, **pick a pivot point**. (middle element might just work)
- **Move items smaller than pivot to the left**
- **Move items bigger than pivot to the right**
- Now the items are arranged in a way the pivot is in it's final position
- Repeat above steps for items to the left of pivot, and to the right of pivot
- **Until left and right pointers meet**

### Implementation in Java

Quick sort happens in-place. So when I say move, technically it's a swap.

```
    public void quickSort(int[] nums, int left, int right) {
        
        if(left >= right) {
            return;
        }

        int pivot = this.partition(nums, left, right);

        this.quickSort(nums, left, pivot - 1);
        this.quickSort(nums, pivot + 1, right);
    }

    public int partition(int[] nums, int left, int right) {
        
        int pivot = nums[right];
        int pointer = left;

        while (left < right) {

            if(nums[left] <= pivot) {

                this.swap(nums, pointer++, left);
            }

            left++;
        }

        this.swap(nums, pointer, right);
        return pointer;
    }

    public void swap(int[] a, int i, int j) {
        int n = a[i];
        a[i] = a[j];
        a[j] = n;
    }
```
