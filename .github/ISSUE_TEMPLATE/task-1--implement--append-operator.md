---
name: 'Task 1: Implement `append()` and Overload `operator>>()`'
about: Task 1 for Students
title: 'Task 1: Implement `append()` and Overload `operator>>()`'
labels: enhancement, good first issue
assignees: ''

---

**Description**

Implement the append operation for the List class.  Perform this task in 2 steps.  Implement a member function named `append()` as described which does the actual work of appending items to the end of the list.  Then overload the `operator>>()` and simply call the `append()` function to implement this overloaded operator.


**Suggested Solution**

Appending is a relatively easy operation if there is room in the `values` array to simply add the new value to the end of the list of values.  However, since arrays are fixed sized blocks of memory, you may need to first grow the list before you can add on a new value, which compilicates the solution a bit.  However there is already a `growListIfNeeded()` private member function defined in the `List` class, which you should reuse in order to do the work of detecting and growing the memory allocation as needed for the `List`.


**Additional Requirements**

- Your `append()` member function must correctly return a reference to `this` item, so that it can be used to chain together appen operations in expressions correctly.
- You are required to correctly manage and update memory allocation to hold the list.  You are required to use the existing `growListIfNeeded()` private member function to do this.
