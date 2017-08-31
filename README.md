# Hadoop-udacity1
In this  project some mapper and reducer codes are written to extract  some information from large data file .

 Hadoop  is an open-source software framework used for distributed storage and processing of dataset of big data using the MapReduce programming model. It consists of computer clusters built from commodity hardware.
 
Hadoop Distributed File System (HDFS) – a distributed file-system that stores data on commodity machines, providing very high aggregate bandwidth across the cluster

If the data is already in the RDBMS and the information you need is stored in a way that facilitates the data retrieval from the RDBMS side, then it might not be worth it going through the overhead of exporting the data, importing it into Hadoop/Mapreduce, writing the program to gather the statistics you're interested in and, finally, running it and getting those statistics .


MapReduce
And that’s MapReduce! The Mappers  are programs which each deal with a relatively small
amount of data, and they all work in parallel. The Mappers output what we call ‘intermediate
records’, which in this case were our index cards. Hadoop deals with all data in the form of
records, and records are key value pairs. In this example, the key was the store name, and the
value was the sale total for that particular piece of input. Once the Mappers have finished, a
phase of MapReduce called the ‘Shuffle and Sort’ takes place. The shuffle is the movement of
the intermediate data from the Mappers to
the Reducers and the combination of all the
small sets of records together, and the sort
is the fact that the Reducers will organize
the sets of records  the piles of index
cards in our example  into order. Finally,
the Reduce phase works on one set of
records   one pile of cards  at a time; it
gets the key, and then a list of all the values,
it processes those values in some way
(adding them up in our case) and then it
writes out its final data for that key
