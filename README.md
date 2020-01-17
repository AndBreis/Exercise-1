# Exercise-1 Anders B

What is concurrency? What is parallelism? What's the difference?

    Concurrency means that multiple calculations run at the same time on a single
    prossessor. parallelism means that multiple canculations runs at the same time on
    multiple prosessors.

Why have machines become increasingly multicore in the past decade?

    In order to run more programs/tasks parallel

What kinds of problems motivates the need for concurrent execution?

(Or phrased differently: What problems do concurrency help in solving?)

    Concurrency is used to create isolation for data through conflicting datachanges

Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?

(Come back to this after you have worked on part 4 of this exercise)

    Concurrent programs make altering the same data easier for the programmer.|

What are the differences between processes, threads, green threads, and coroutines?

    A process is a computer program consisting of one or many threads. A thread is a set of
    instructions that can be executed independently, a green thread is a thread that is
    scheduled by something other than the OS, and a coroutine is a program component
    that can be suspended and resumed

Which one of these do pthread_create() (C/POSIX), threading.Thread() (Python), go (Go) create?

    Pthread_create() creates a thread
    Threading.thread() creates a thread
    Go creates a coroutine

How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?

    The GIL is a lock that only allows one thread to be in execution at the same time.

With this in mind: What is the workaround for the GIL (Hint: it's another module)?

    Thread extensions in C, like NumPy allows you to run your code without the fear of GIL
    locking threads

What does func GOMAXPROCS(n int) int change?

    The number of prosessors in use
