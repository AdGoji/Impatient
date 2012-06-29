Cascading for the Impatient, Part 1
===================================
The goal is to create the simplest [Cascading 2.0](http://www.cascading.org/) app possible, while following best practices.

Here's a brief Java program which copies lines of text from file "A" to file "B". We'll keep building on this example until we have a MapReduce implementation of [TF-IDF](http://en.wikipedia.org/wiki/Tf*idf).

More detailed background information and step-by-step documentation is provided at https://github.com/ConcurrentCore/impatient/wiki

Build Instructions
==================
To generate an IntelliJ project use:

    gradle ideaModule

To build the sample app from the command line use:

    gradle clean jar

Before running this sample app, be sure to set your `HADOOP_HOME` environment variable. Then clear the `output` directory, then to run on a desktop/laptop with Apache Hadoop in standalone mode:

    rm -rf output
    hadoop jar ./build/libs/impatient.jar data/rain.txt output/rain

To view the results:

    more output/rain/part-00000

An example of log captured from a successful build+run is at https://gist.github.com/2911686

For more discussion, see the [cascading-user](https://groups.google.com/forum/?fromgroups#!forum/cascading-user) email forum.

Stay tuned for the next installments of our *Cascading for the Impatient* series.
