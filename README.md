### Learning Rust With Entirely Too Many Linked Lists
Completed most of: https://rust-unofficial.github.io/too-many-lists/index.html

Notes:

* Better understanding role of ownership:
    * Values (self)
    * Shared References (&self)
    * Mutable References(&mut self)

* Better understand of Lifetimes
    * 'a ties to memory deallocation
    * use with "helper" that share references with an owner.
    * lifetimes are implicit in most functions:
    * making it explicit helps the compiler check to ensure that a variable is valid as long as other variables with the same lifetime.
    * Helps to ensure that helper does not use a value after it has been freed by the owner. 

* Reference Counters
    * single vs. shared ownership
    * Rc is like Box, but it can be copied. Its memory is deallocated only when all references are gone.
    * Sharing doesn't necessitate thread safety.
    * Arc guarantees atomicity when reference countering, but involves overhead.
    * Inherited mutability is mutability inherited from the container. (What does this mean?)
    * Interior mutability allows mutability through a shared reference.
        * Two Classses: single thread, multi-threaded.
