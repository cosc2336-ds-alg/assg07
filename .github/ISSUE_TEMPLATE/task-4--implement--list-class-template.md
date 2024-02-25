---
name: 'Task 4: Templatize the `List` Class'
about: Task 4 for Students
title: 'Task 4: Templatize the `List` Class'
labels: enhancement
assignees: ''

---

**Description**

The fourth task is to turn the `List` class into a template class, and make all of its member functions into template member functions.  You will need to create a new branch in your repository named `template`, and put all work for task 4 into this branch.  You will need to modify the build system slightly on this branch, to use alternate tests that are expecting a templatized version of the `List` class.

**Suggested Solution**

It is suggested that you continue to practice incremental development.  Making the `List` class into a template class involves first correctly specifying the class declaration as a template. The `values` array/pointer needs to become a template type instead of a concrete `int` type.   Then you need to make each member function (including constructors, destructors and private member functions) into templates.

If you have difficulty, you should remove all functions from the class declaration and their implementations (put them in a temporary file somewhere).  Then templatize the class declaration and member variables first, and make sure the code can be compiled.  Then templatize the member functions 1 by 1.  Start by templatizing the member functions for the first unit test of the test file.  Get the project to a compilable state, and then see if the tests can run and pass.  Once you are this far, uncomment the next unit test and templatize further member functions until you have templatized all member functions.

**Additional Requirements**

- You are required to gather all work for this task in a separate branch named `template`.  This branch should start from your last commit of task 3 that implements all of the operator overloading.
- You are required to correctly set back up the build system of the project so that the `test-int-template.cpp` and `test-string-template.cpp` files are being compiled and the unit tests for int and string templatized lists are being run.
- You are required to fix/implement templatization for existing methods, like `getSize()` and others first in the `List.[hpp|cpp]` files.
- And finally, you need to reimplement your tasks 1-3 to add appending, prepending and concatenation, templatizing your code correctly to support these operations.
