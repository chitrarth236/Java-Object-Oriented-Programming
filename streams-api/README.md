Stream API is used to process collections of objects.

A stream is a sequence of objects.

Stream API contains lots of methods which can be pipelined to produce desired result on streams.

Stream is used to process the elements as per pipelined methods without altering the original value of the object.

Two types of operations:
1. Intermidiate Operations: If operation returns another stream to which you could apply a further operation, it is an intermidiate operation(e.g. map, filter, sorted).an intermediate operation is always lazily executed. That is to say they are not run until the point a terminal operation is reached.
2. Terminal Operations: If operation outputs a concrete type or produces a side effect, it is a terminal operation(e.g. collect, forEach, reduce). A terminal operation is always eagerly executed. This operation will kick off the execution of all previous lazy operations present in the stream.

