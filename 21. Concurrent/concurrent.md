# Concurrent Programming
## Parallel and Concurrency
where are many terminologies.
- concurrent
- parallel
- multitasking
- multiprocessing
- multithreading
- distributed systems

there is a lecture to explain
[from concurrent to parallel](https://www.youtube.com/watch?v=NsDE7E8sIdQ)

- Concurrency is about correctly and efficiently controlling access
to shared resources
    - concurrency is about race-condition which involve occupy and wait
    - concurrency is hard
    - concurrency often means 'more than one task is making progress'
- Parallelism uses additional resources to produce and answer faster
    - parallelism is about partition which divide task to sub-task 
        without contention
    - parallelism is much easier
    - parallelism means 'more than one task is executing simultaneously'
    - parallelism is limited by dataflow dependency
    - pure parallelism require more than one process


## Why
### Advantage
- faster execution in certain environment

### Disadvantage
- you can not control the execution
- java's thread is preemptive and with context-switch


# Coroutine
cooperative with multiple tasks.