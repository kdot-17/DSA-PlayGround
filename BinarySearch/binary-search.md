# Binary Search

Binary Search is an algorithm used for finding a target value in a sorted collection of entities by repeatedly halving the search range: compare the target to the middle element, and if it does not match, eliminate the half that cannot contain the target; repeat until it is found or the range is empty.

- The collection must be sorted, as the algorithm relies on order to decide which half to discard: on unsorted data it may discard the half containing the target and fail silently.

- The worst case time complexity in Binary Search is O(log N). Since the searching is in place and the iterative version only keeps track of a few variables, the space complexity is O(1).