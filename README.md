# Objective-C Delegate Deallocation Bug
This repository demonstrates a common Objective-C bug related to premature object deallocation when using delegates. The bug leads to an EXC_BAD_ACCESS error. The solution shows how to correctly manage object lifecycles and prevent this crash.

## Bug Description
The `bug.m` file contains code that showcases how using delegates without proper memory management leads to a crash when an object is deallocated before its delegate finishes its operation. 

## Solution
The `bugSolution.m` file provides a corrected version of the code. This solution uses weak references to prevent the delegate from retaining the object and causing premature deallocation.  This ensures that the delegate doesn't keep the object alive longer than necessary.