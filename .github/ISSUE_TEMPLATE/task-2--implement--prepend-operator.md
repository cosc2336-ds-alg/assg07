---
name: 'Task 2: Implement `prepend()` and Overload `operator<<()`'
about: Task 2 for Students
title: 'Task 2: Implement `prepend()` and Overload `operator<<()`'
labels: enhancement
assignees: ''

---

**Description**

Implement the described member function to prepend items onto the front of the list and provide an overloaded prepend operator for the `List` type.  Perform this task in 2 steps.  Implement a member function named `prepend()` as described which does the actual work of prepending items to the beginning of the list.  Then overload the `operator<<()` and simply call the `prepend()` function to implement this overloaded operator.

**Suggested Solution**

This method is slightly more complicated than `append()` because you have an additional step to perform before you can prepend onto the front of a C/C++ array.  You still need to grow the memory allocation if needed to prepend the new value.  But also, you must shift all items in the list up 1 position, to free up index 0 of the `values` array, so that you can add the new value into index 0.  Be careful to correctly shift all items.  Remember that the size of the list is growing by 1 when doing this prepend.

**Additional Requirements**

- Your `append()` member function must correctly return a reference to `this` item, so that it can be used to chain together appen operations in expressions correctly.
- You are required to correctly manage and update memory allocation to hold the list.  You are required to use the existing `growListIfNeeded()` private member function to do this.
