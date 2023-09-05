# CPE423A
## Class repo for CPE-423-A


*Assignment 0 for CPE 423-A*


**Need to finish this assignment by _Saturday January 28_ for full credit**


Sample git code
```
git pull
git add .
git commit -m "add message"
git push
```
Sample rust code [Source](https://github.com/ProgrammingRust/examples/blob/master/generic-queue/src/lib.rs)
```

pub struct Queue<T> {
    older: Vec<T>,
    younger: Vec<T>
}

impl<T> Queue<T> {
    pub fn new() -> Self {
        Queue { older: Vec::new(), younger: Vec::new() }
    }

    pub fn push(&mut self, t: T) {
        self.younger.push(t);
    }

    pub fn is_empty(&self) -> bool {
        self.older.is_empty() && self.younger.is_empty()
    }

    pub fn pop(&mut self) -> Option<T> {
        if self.older.is_empty() {
            use std::mem::swap;

            if self.younger.is_empty() {
                return None;
            }

            // Bring the elements in younger over to older, and put them in
            // the promised order.
            swap(&mut self.older, &mut self.younger);
            self.older.reverse();
        }

        // Now older is guaranteed to have something. Vec's pop method
        // already returns an Option, so we're set.
        self.older.pop()
    }

    pub fn split(self) -> (Vec<T>, Vec<T>) {
        (self.older, self.younger)
    }
}

```
[Class Canvas Page](https://sit.instructure.com/courses/67795)

A Sample Image 

![SteamOS](https://github.com/mdigeron/CPE423A/assets/97755080/d6b9d6d2-f00b-4043-bd91-0eaddef70a79)

By the end of class will have finished
+ Milestone 1.1: Customers
+ Milestone 1.2: Needs
+ Milestone 1.3: Requirements
+ Milestone 1.4: Needs-Requirement Mapping
+ Milestone 2.1: Project Plan
+ Milestone 2.2: Concepts
+ Milestone 2.3: Concept Selection
+ Milestone 2.4: Design
+ Milestone 2.5: Analysis
+ Milestone 2.6: Test Plan


> this is a quote using markdown


A Kea Parrot



![Kea Parrot](http://i.imgur.com/CJjIDlJ.gif)
