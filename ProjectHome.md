# T`*`-tree library #

**libttree** is a C library providing an API to T`*`-tree data structure.

## `About T-trees` ##
Wikipedia says:
_A T-tree is a balanced index tree data structure optimized for cases where both the index and the actual data are fully kept in memory, just as a B-tree is an index structure optimized for storage on block oriented secondary storage devices like hard disks. T-trees seek to gain the performance benefits of in-memory tree structures such as AVL trees while avoiding the large storage space overhead which is common to them.
T-trees do not keep copies of the indexed data fields within the index tree nodes themselves. Instead, they take advantage of the fact that the actual data is always in main memory together with the index so that they just contain pointers to the actual data fields._

## `The difference between T-tree and T*-tree` ##
T-tree looks like simple balanced binary tree where each tree node holds more than one key. Actually each T-tree's node holds an array of keys and three pointers: one to parent node and two to right and left child respectively. Thus T-tree node looks like _T_ letter:


![http://wiki.ttree.googlecode.com/hg/T-tree-1.png](http://wiki.ttree.googlecode.com/hg/T-tree-1.png)

T`*`-tree is much like simple T-tree except all its nodes linked together from the smallest one to the largest one. This means that T`*`-tree can be easily represented as a sorted list:


![http://wiki.ttree.googlecode.com/hg/T-mul-tree-1.png](http://wiki.ttree.googlecode.com/hg/T-mul-tree-1.png)