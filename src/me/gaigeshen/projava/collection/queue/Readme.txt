The Queue Interface:

> The java.util.Queue interface is a collection designed for holding elements prior to processing.
	a. Besides basic Collection operations, queues provide additional insertion, extraction, and inspection operations.
	b. Queues can implement FIFO (queue), LIFO (stack), and priority ordering.
	c. Queues generally do not accept null elements.
> Queue operations include:
	a. Inserting elements: add() and offer()
	b. Removing and returning elements: remove() and poll()
	c. Returning elements without removal: element() and peek()


The java.util.concurrent.BlockingQueue interfaces declare additional blocking put() and take() methods,
designed for concurrent access by multiple threads. 


General-purpose Queue implementations:
1. java.util.LinkedList
2. java.util.PriorityQueue
Concurrency-specific BlockingQueue implementations:
1. java.util.concurrent.ArrayBlockingQueue
2. java.util.concurrent.ConcurrentLinkedQueue
3. java.util.concurrent.DelayQueue
4. java.util.concurrent.LinkedBlockingQueue
5. java.util.concurrent.PriorityBlockingQueue
6. java.util.concurrent.SynchronousQueue