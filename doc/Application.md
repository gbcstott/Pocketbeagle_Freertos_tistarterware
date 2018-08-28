The Application (src/main.c) that this port runs does the following:

Sets up a Semaphore.

Creates two Tasks

Starts the Scheduler

Loops.

Task 1 does the following:

Takes the Semaphore.
Prints a message
Gives the Semaphore
Delays for 1000.


Task 2 does the following:

Takes the Semaphore.
Prints a message
Gives the Semaphore
Delays for 500.
