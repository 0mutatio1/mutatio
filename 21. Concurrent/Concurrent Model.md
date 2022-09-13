# Concurrent Model


## actors
active objects or actors

So with active objects, we serialize messages rather than methods, 
which means we no longer need to guard against problems 
that happen when a task is interrupted midway through its loop.

C.A.R. Hoare’s theory of Communicating Sequential Processes (CSP)