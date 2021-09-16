# big_data_and_analytics_workshop1

## First part
###### Installation and setup of virtualbox version 6.1, Ubuntu version 21.04 and Hadoop was performed successfully

## Second part

###### What results generated the program and what are the MapReduce steps implemented?

First, it is important to generate inside the dfs, the user file and the hdoop file, to make reference to the hdoop user and inside this file there are gonna be the input and the output file too.

![part2-1-1](/screenshots/part2-1-1.png?raw=true "part2-1-1.png")

Once done, I’ve moved everything on the operating system to the hadoop file to the input file that was just created, and just to test if everything is working, I executed one the examples of the jar mapreduce and grep all files that started with dfs.

![part2-1-2](/screenshots/part2-1-2.png?raw=true "part2-1-2.png")

Now at running these commands over dfs I was able to copy the output files to the distributed files system and I have as a result the files that started with dfs.

![part2-1-3](/screenshots/part2-1-3.png?raw=true "part2-1-3.png")

![part2-1-4](/screenshots/part2-1-4.png?raw=true "part2-1-4.png")

![part2-1-5](/screenshots/part2-1-5.png?raw=true "part2-1-5.png")

###### What results generated the program and what are the MapReduce steps implemented?

First I created a .txt file with a song.

![part2-2-1](/screenshots/part2-2-1.png?raw=true "part2-2-1.png")

After create the text file I needed to copy it into the input file that was generated earlier in the distributed files system.

![part2-2-2](/screenshots/part2-2-2.png?raw=true "part2-2-2.png")

With that done, it is possible to run the command to execute the mapreduce wordcount example in my input Hozier.txt file. 

![part2-2-3](/screenshots/part2-2-3.png?raw=true "part2-2-3.png")

And finally we can see as a result of the mapreduce wordcount example, the count of  every word of the song used for the exercise.

![part2-2-4](/screenshots/part2-2-4.png?raw=true "part2-2-4.png")

## Third part

###### SPARK installation and configuration evidence

![part3-1-1](/screenshots/part3-1-1.png?raw=true "part3-1-1.png")

###### Understanding the wordcount pyspark code

> text_file = sc.textFile("poem.txt")

The first line of the code is used to bring the source text file that spark is going to use.

> counts = text_file.flatMap(lambda line: line.split(" "))
>		.map(lambda word: (word, 1))
>   .reduceByKey(lambda a, b: a + b)

The second line is used to map the words and count them, so in the very first line every word of the document is sorted by separating every word by an space “ ” using a flat map to get all the words inside a unique list, then the second line is used to map the words by assigning a key to every word and the initial value of that key and then the third one is to reduce by key assigning to every word the count of the number of times than an specific key (word) appears on the source text file.

> counts.saveAsTextFile("wordscount")

Finally the last line takes the word counts and saves them in a folder named wordscount.

###### Results after execute the PySpark code

It assigned a key to every word on the text file and then, each time the mapping found that key started to add a value, concluding in the sum of how many times that key appeared in the text file, or basically the number of times an specific word appeared on the text file.

![part3-3](/screenshots/part3-3.png?raw=true "part3-3.png")

## Fourth part

###### Anaconda and Jupyter lab installation and configuration evidence
###### Evidence of ipynb scripts running and working okay

![part4-4-1](/screenshots/part4-4-1.png?raw=true "part4-4-1.png")

![part4-4-2](/screenshots/part4-4-2.png?raw=true "part4-4-2.png")

![part4-4-3](/screenshots/part4-4-3.png?raw=true "part4-4-3.png")

![part4-4-4](/screenshots/part4-4-4.png?raw=true "part4-4-4.png")

![part4-4-5](/screenshots/part4-4-5.png?raw=true "part4-4-5.png")

![part4-4-6](/screenshots/part4-4-6.png?raw=true "part4-4-6.png")

![part4-4-7](/screenshots/part4-4-7.png?raw=true "part4-4-7.png")

![part4-4-8](/screenshots/part4-4-8.png?raw=true "part4-4-8.png")

![part4-4-9](/screenshots/part4-4-9.png?raw=true "part4-4-9.png")

![part4-4-10](/screenshots/part4-4-10.png?raw=true "part4-4-10.png")




