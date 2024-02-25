---
name: 'Task 3: Implement `concatenate()` and Overload `operator+()`'
about: Task 3 for Students
title: 'Task 3: Implement `concatenate()` and Overload `operator+()`'
labels: enhancement
assignees: ''

---

**Description**

Implement the described member function to perform concatenation of two lists and create and return a new `List` instance.  Also provide an overloaded `operator+()` operation for the `List` type that will perform this concatenation operation on lists.  Perform this task in 2 steps.  Implement the member function `concatenate()` as described which does the actual work of concatenating the lists, creating a new list, and returning it.  Then overload the `operator+()` and simply call the `concatenate()` function to implement this overloaded operator.

**Suggested Solution**

The approach you should use for `concatenate` is as follows:

1. Start by allocating a new array of `int` values that is large
   enough to hold both `this` size plus the right hand side `size` values
   once you concatenate them together.
2. Copy all of the values of `this` from its array of `values` to the beginning
   of this new array of values.
3. Likewise copy all of the values from the right hand side list after these in the
   new array.
4. Then it is important to dynamically create a new `List` of values that is initialized
   with this array of the concatenated values you just created.
5. Once you have dynamically allocated your new `List` you don't need the array 
   from step 1 anymore, so `delete` it.
6. You should return th newly dynamically allocated `List` object as a reference from
   your function.
   
   
**Additional Requirements**

- Your `concatenate()` member method must return a reference to a list, e.g. a `List&` as its result.
- Your `concatenate()` member function must correctly return a reference to `this` item, so that it can be used to chain together append operations in expressions correctly.
- The returned reference to a new `List` must be **dynamically** allocated and returned as expected by the tests.
- You must free up any dynamically allocated memory that is not longer in use.  From the suggested solution, this means that the array of values you first create to then dynamically crate a new `List` should be freed after the new concatenated `List` has been created.
- Your overloaded `operator+()` must have the same signature as the `concatenate()` member function.  And your `operator+()` must be implemented by simply calling and reusing the `concatenate()` method.



