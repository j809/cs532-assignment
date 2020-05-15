# Problem Statement

Wordcount is famously the “Hello, world!” of many data science platforms (e.g., MapReduce and Spark). This project is to implement a distributed, fault tolerant version of wordcount in Java.

Your distributed wordcount will consist of a number of processes. All communication across processes will be via sockets. You will use the master-worker paradigm: there should be one master and N workers. The master must ensure that all N workers are up by pinging them periodically with a heartbeat message every 3 seconds. If a worker stops responding, then the master must spawn another worker. (You should test the fault-tolerance of your system by invoking kill to stop processes.)

Workers should repeatedly ask the master which file they should work on (until they learn there is no work left to do). They should perform wordcount and output results to a file. When all input files have been processed, the master should inform the workers that all work has concluded; upon receiving this message, the workers should exit. The master will then read all of the files produced by the workers, combine the results, and output them.

Your program should print the word counts in reverse order by frequency (so, most frequent word first) - each line should list a word and its frequency.
