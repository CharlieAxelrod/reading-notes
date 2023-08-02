# Designing Data-Intensive Applications

## Part 1: Foundations of Data Systems

### Chapter 1: Reliable, Scalable, and Maintainable Applications

A data-intensive application is one in which data operations and quantity are a limiting factor. Data operations could include database reads and writes, searches, caches, batch processing, and stream processing.

Complex data systems often combine multiple data storage and processing tools, each of which performs distinct tasks. Application code then stitches these tools together, seeking to ensure the **reliability**, **scalability**, and **maintainability** of the composite data system. 

A **reliable** system is one that works correctly, even when things go wrong. It can tolerate user error and prevents unauthorized access and abuse. A _fault-tolerant_ system can handle the breakdown of individual components. In most cases, it is better to tolerate faults than attempt to prevent them; security breaches, which are irreversible, are an exception.

_Hardware faults_ could historically be handled by making individual components redundant, such as having dual power supplies for a server. Nowadays, a typical application relies on more machines, and often on unreliable cloud VMs, making it necessary to become fault-tolerant to the loss of an entire machine. Machine failure is better handled through software fault-tolerance techniques. 

_Software faults_, which can result in broad system failures, are more difficult to build tolerance around. Software bugs that cause system-wide failure are often difficult to detect and may lie dormant. Testing, monitoring, and careful analysis of the interactions within the system are useful steps towards software fault-tolerance.

Humans are the leading cause of error. _Human error_ can be mitigated by building strong internal interfaces and APIs, creating sandbox environments, and testing. Enabling easy roll back and recovery, along with error and performance monitoring, are also good steps. 
