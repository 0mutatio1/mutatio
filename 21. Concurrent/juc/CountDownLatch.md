# CountDownLatch

This is used to synchronize one or more tasks by forcing them to 
wait for the completion of a set of operations being performed by other tasks.

You give an initial count to a CountDownLatch object, 
and any task that calls await( ) on that object will block 
until the count reaches zero