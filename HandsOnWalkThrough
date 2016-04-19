val originalRDD = sc.parallelize(List("Data1", "Data2", "Data4", "Data5", "Data6", "Bacon", "Hortonworks", "Hadoop", 
"Spark", "Tungesten",
"SQL"), 4)

val flatRDD = originalRDD.flatMap(_.split(" "))

originalRDD.collect().foreach(println)

originalRDD.count()

originalRDD.first()

originalRDD.take(2)

originalRDD.takeSample(true,5,7634184)

val mapped =   originalRDD.mapPartitionsWithIndex{
                       (index, iterator) => {
                           println("Index -> " + index)
                          val myList = iterator.toList
                           myList.map(x => x + " -> " + index).iterator
                        }
                     }
                     
mapped.take(5)

val rddSpark = sc.parallelize(List("SQL","Streaming","GraphX", "MLLib", "Bagel", 
"SparkR","Python","Scala","Java", "Alluxio", "Tungsten", "Zeppelin"))

val rddHadoop = sc.parallelize(List("HDFS", "YARN", "TEZ", "Hive", "HBase", "Pig", "Atlas", 
"Storm", "Accumulo", "Ranger", "Phoenix", "MapReduce", "Slider", "Flume", "Kafka", "Oozie", "Sqoop", "Falcon",
"Knox", "Ambari", "Zookeeper", "Cloudbreak", "SQL", "Java", "Scala", "Python"))

val bigDataRDD = rddHadoop.union(rddSpark)
bigDataRDD.collect()

rddHadoop.intersection(rddSpark).collect()

bigDataRDD.distinct().collect()

bigDataRDD.sample(true,0.25 ).collect()

bigDataRDD.count()

val keyValueRDD = sc.parallelize(Seq(
                    ("Bacon", "Awesome"),
                     ("PorkRoll", "Great"),
                     ("Tofu", "Bogus")))
                     
val groupByRDD = keyValueRDD.groupByKey()
groupByRDD.collect()

val kvRDD = sc.parallelize(Seq((1,"Bacon"), (1, "Hamburger"), (1,"Cheeseburger")))
val reducedByRDD = kvRDD.reduceByKey((a, b) => a.concat(b))
reducedByRDD.take(5)

keyValueRDD.countByKey().foreach(println)

keyValueRDD.saveAsTextFile("here")

keyValueRDD.saveAsObjectFile("here3")

keyValueRDD.saveAsSequenceFile("here2")

%sh ls 

%sh ls here

cat here/part-00003

bigDataRDD.reduce((a, b) => a.concat(b))

val namesRDD = sc.parallelize(List((1, 25), (1, 27), (3, 25), (3, 27)))
val groupByRDD = namesRDD.aggregateByKey(0)((k,v) => v.toInt+k, (v,k) => k+v).collect()

val sortByRDD = namesRDD.sortByKey(true).collect()

val sortByRDD = namesRDD.sortByKey(false).collect()

val otherKeyValueRDD = sc.parallelize(Seq(
                    ("Bacon", "Amazing"),
                     ("Steak", "Fine"),
                     ("Lettuce", "Sad")))
                     
keyValueRDD.join(otherKeyValueRDD).collect()
keyValueRDD.leftOuterJoin(otherKeyValueRDD).collect()
keyValueRDD.rightOuterJoin(otherKeyValueRDD).collect()
keyValueRDD.fullOuterJoin(otherKeyValueRDD).collect()
keyValueRDD.groupWith(otherKeyValueRDD).collect()
keyValueRDD.cartesian(otherKeyValueRDD).collect()
keyValueRDD.pipe("cut -c2-4").collect()

keyValueRDD.coalesce(1).collect()

keyValueRDD.repartition(2).collect()

val sqlContext = new org.apache.spark.sql.SQLContext(sc)

val hereRDD = sc.textFile("here")
hereRDD.count
val df = hereRDD.toDF()
df.registerTempTable("here")
df.printSchema()

%sql

select * from here



// Comment:   For access data logs, unzip before using
