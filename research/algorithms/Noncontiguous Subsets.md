The noncontiguous subsets of a list of elements are all the unique tuples that can be derived by removing 0 or more elements of the list, up to all elements.

```
function generateSubsetsRecursively (arr, res, subset, idx) {
    // Add the current subset to the result list
    res.push([...subset]);

    // Generate subsets by recursively including and excluding elements
    for (let i = idx; i < arr.length; i++) {
        // Include the current element in the subset
        subset.push(arr[i]);

        // Recursively generate subsets with the current element included
        generateSubsetsRecursively(arr, res, subset, i + 1);
        
        // Exclude the current element from the subset (backtracking)
        subset.pop();
    }
}
```
