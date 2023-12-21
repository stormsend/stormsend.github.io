二分
```java
public int binaryQuery(int[] nums, int target){
	int left = 0;
	int right = nums.length -1;
	while(left<=right){
		int mid = (left+right)/2;
		if (nums[mid] == target) {
			return mid;
		}else if(nums[mid]> target){
			right = mid-1;

		}else if(nums[mid]< target){
			left = mid +1;
		}
	}
	return -1;
}
```
快排
```java
public void sort(int[] nums){
	quickSort(nums,0,nums.length-1);
}
publice void quickSort(int[] nums,int left,int right){
	if (left<right) {
		right = partition(nums,left,right);
		quickSort(nums,left,right-1);
		quickSort(nums,left+1,right);
	}
}
public int partition(int[] nums,int left,int right){
	int base = nums[left];
	while(left<right) {
		while(left < right && nums[right] > base){
			right --;
		}
		nums[left] = nums[right];
		while (left<right && nums[left] < base) {
			left++;
		}
		nums[right] = nums[left];
	}
	nums[left] = base;
	return left;
}
```

滑动窗口
```java
public void windows(int[] nums){
   int left = 0;
   // k 代表一个窗口的范围
   int right = k;

   while(left < right){
	   	while(left < right && check()){
	   		//缩小窗口
	   		left++;
	   	}
	   	// 增加窗口
	   	right++;

   }
}
```


