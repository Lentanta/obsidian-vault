[[Data structures & Algorithms]]
# How it work
![[binary-search.png]]
## Code
```javascript
const search = (nums, target) => {
    let low = 0;
    let high = nums.length -1;

    while(low <= high){
        var mid = Math.floor((low+high)/2)
				
        if(nums[mid] === target){
            return mid;
        }
        if (nums[mid] < target){
            low = mid + 1;
        }
        if (nums[mid] > target){
            high = mid - 1;
        }
    }
    return -1
};
```