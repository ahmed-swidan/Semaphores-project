# semaphores-project
This program is a modification to the reader writer problem solved by using semaphores where there is a writer that rights in one place ( counter ) a reader that reads from this place ( monitor ) then writes in a buffer.
Another reader reads from this buffer ( collector ) and gets the output.
Its similar to a mailbox messaging system where monitor is the mailbox, counter is the sender and collector is the receiver.
# Problem statment
this program is intended to solve the following synchronization problem using POSIX and “semaphore.h” libraries.
N mcounter threads count independent incoming messages in a system, and another thread mmonitor gets the count of threads at time intervals of size t1, and then resets the counter to 0. The mmonitor then places this value in a buffer of size b, and a mmcollector thread reads the values from the buffer.
Any thread will have to wait if the counter is being locked by any other thread. Also, the mmonitor and mcollecttor threads will not be able to access the buffer at the same time or to add another entry if the buffer is full.
