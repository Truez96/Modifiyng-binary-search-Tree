# Project-4

First modify a binary search tree so that it allows duplicates. Then, use this new binary search tree
to organize records from a big data set.

This project has two parts. In Part A, you will write the binary search tree class. In Part B, you'll use
the class to analyze a data set.

The class BinarySearchTreeWithDups represents a binary search tree in which duplicate
     entries are allowed.
Process for Adding Duplicates
     A duplicate entry is placed in the entry's left subtree. The process for adding to this new binary
     tree is:
          1 Compare the new element to the current element.
               a. If the new element is smaller, go into the left subtree. Return to step 1
               b. If the new element is larger, go into the right subtree. Return to step 1
               Note: This is the same process used in a regular binary search tree.
          2 If the new element is equal to the current element:
               a. Go into the left subtree. Return to step 1
Review the provided tree picture that uses data from the driver to make sure you understand
how the duplicates are added.

The BinarySearchTreeWithDups Class
We will assume the getEntry method returns the first match it finds and the remove method
removes the first match it finds. So the only modification required is the add method.
The class BinarySearchTreeWithDups extends BinarySearchTree,
- The class shell is provided with empty methods that you will modify.
- There are many classes required to get this lab to compile.
     All are included in the provided zip.
     Use the versions provided with this project!
     Only modify the BinarySearchTreeWithDups class.
        Do not modify other classes.
- Begin by closely reviewing BinarySearchTree and BinaryTree classes.
     Make sure you understand how these classes work before you implement BinarySeachTreeWithDups.

You will implement four methods.
Important Note: For full credit, take advantage of the sorted nature of a binary search tree to
write efficient code. Consider whether you always need to search both branches of a tree!
- Write a addEntryHelperNonRecursive(T) method.
     Override the add method to call a new private addEntryHelperNonRecursive method.
     The helper method allows duplicate entries to be added, using the algorithm described above.
     Important: This method must be written without recursion in order for Part B to run.
     Hint: review the addEntry method in BinarySearchTree class.
- Write a countEntriesNonRecursive(T) method.
     The method counts the number of times an element appears in the tree.
     Important: This method must be written without recursion in order for Part B to run.
- Write a countGreaterRecursive(T) method.
     The method counts the number of elements in the tree greater than the parameter.
     The elements in the tree implement Comparable, so you can invoke the compareTo method on the data inside of any node.
     This method uses recursion. You can add a private helper method if necessary. It's okay if the countGreaterRecursive method isn't actually recursive, but the helper method is recursive.
- Write a countGreaterWithStack(T) method.
     The method does the same as the method above, but is not recursive.
     The method uses a stack in a meaningful way.
