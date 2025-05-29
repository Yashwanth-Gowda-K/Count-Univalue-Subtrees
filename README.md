# Count-Univalue-Subtrees

# Problem Explanation
We need to count how many subtrees in a binary tree have all nodes containing the same value. A subtree consists of any node and all its descendants.

# Solution Approach
This solution uses a post-order depth-first search (DFS) traversal to efficiently count univalue subtrees from the bottom up.

# Key Logic:
Base Case: Empty nodes are automatically considered univalue

# Recursive Check:
First verify if left and right subtrees are univalue
Then confirm current node's value matches its children's values
Counting: Increment count whenever all conditions are met

# Important Edge Cases Handled:
Nodes with only one child (must match the existing child's value)
Leaf nodes (always count as univalue subtrees)
Empty trees (return 0)

# Complexity Analysis
Time Complexity: O(N) - We visit each node exactly once
Space Complexity: O(H) - Where H is tree height, for recursion stack

# Example Walkthrough
Consider this tree:

      5
     / \
    1   5
   / \   \
  5   5   5
  
The three leaf nodes (5, 5, 5) each count
The right subtree (5→5) counts
The left subtree doesn't count (contains 1)
The full tree doesn't count (contains 1)
Total univalue subtrees: 4

# Why This Matters
This problem teaches:
Bottom-up tree traversal
Careful handling of node relationships
Efficient counting with recursion

# Perfect for strengthening your tree algorithm skills!
