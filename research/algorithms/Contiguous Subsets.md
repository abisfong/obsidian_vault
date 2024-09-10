The contiguous subsets of a list of elements are all the unique tuples that can be derived by removing 0 or more elements of the list, up to all elements, while maintaining the neighbors each element, with exception to the ends of the list.
# Code

```
function generateSubsetsRecursively (arr, res, subset, idx, latestIdxPushed = 0) {
    res.push([...subset]);

    for (let i = idx; i < arr.length; i++) {
        if (latestIdxPushed >= i - 1 || idx === 0) {
            subset.push(arr[i]);
            generateSubsetsRecursively(arr, res, subset, i + 1, i);
            subset.pop();
        }
    }

    // Add the current subset to the result list
    res.push([...subset]);

    // Generate subsets by recursively including and excluding elements
    for (let i = idx; i < arr.length; i++) {
        // Prevent adding element to subset and recursive call if previously 
        // inserted element is not a neighbor of the element at i
	    if (latestIdxPushed >= i - 1) {
	        // Include the current element in the subset
	        subset.push(arr[i]);
	
	        // Recursively generate subsets with the current element included
	        generateSubsetsRecursively(arr, res, subset, i + 1, i);
	        
	        // Exclude the current element from the subset (backtracking)
	        subset.pop();
	    }
    }
}
```