# majority_Elements

**Problem**

Given an integer array arr[], find the element that appears more than n/2 times, where n is the length of the array.

If no such element exists, return -1.

**Example**
Input
arr = [3, 1, 3, 3, 2]
**Output**
3
Explanation

The array length is 5.

n/2 = 5/2 = 2

The element 3 appears 3 times, which is greater than 2.

Therefore, the majority element is 3.

**Approach**

I used a nested loop approach.

Calculate n/2.
Take each element one by one.
Count how many times that element occurs in the array.
If its count is greater than n/2, return that element.
If no element satisfies the condition, return -1.

**Code**
class Solution {
    int majorityElement(int arr[]) {
        // code here
        int mid=arr.length/2;
        for(int i=0;i<arr.length;i++){
            int count=0;
            for(int j=0;j<arr.length;j++){
                if(arr[i]==arr[j]){
                    count++;
                }
            }
        if(count>mid){
            return arr[i];
        }
        
        }
        return -1;
    }
}
