A [[Max Heap Tree]] is a [[Binary Heap Tree]] where the key at the root is the minimum among all keys present. The same property must be recursively true for all nodes in tree.

# Modifiers
## Insert
Insert at end of [[Max Heap Tree]] array, then swap with parent as long as the new element is greater.

## Delete
Replace the root with the last element of [[Max Heap Tree]] array, then, starting from the root, recursively compare the children and replace the parent with the largest child if it is bigger than the parent.
