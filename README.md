# SparkTransformations
Meetup

Tim Spann

ex-Pivotal Senior Field Engineer
DZONE MVB and Zone Leader
ex-Startup Senior Engineer / Team Lead

http://www.slideshare.net/bunkertor 
http://sparkdeveloper.com/ 
http://www.twitter.com/PaasDev


Setup

Java JDK 8, Scala 2.10, SBT 0.13, Maven 3., Spark 1.6.0
http://www.oracle.com/technetwork/java/javase/downloads/index.html 
http://www.scala-lang.org/download/2.10.6.html
http://www.scala-lang.org/download/install.html
http://www.scala-sbt.org/download.html 
http://apache.claz.org/maven/maven-3/3.3.9/binaries/apache-maven-3.3.9-bin.zip
http://spark.apache.org/downloads.html 
http://d3kbcqa49mib13.cloudfront.net/spark-1.6.0-bin-hadoop2.6.tgz
http://www.apache.org/dyn/closer.cgi/incubator/zeppelin/0.5.6-incubating/zeppelin-0.5.6-incubating-bin-all.tgz
For Mac (brew install sbt)




Running Zeppelin

https://zeppelin.incubator.apache.org/docs/0.5.6-incubating/install/install.html
https://github.com/hortonworks-gallery/zeppelin-notebooks

Download the Apache Zeppelin binary (Mac and Linux)
zeppelin-0.5.6-incubating-bin-all
Unzip
Run
cd zeppelin-0.5.6-incubating-bin-all 
./bin/zeppelin-daemon.sh start
http://localhost:8080/

export SPARK_MASTER_IP=127.0.0.1
export SPARK_LOCAL_IP=127.0.0.1
export SCALA_HOME={YOURDIR}/scala-2.10.6
export PATH=$PATH:$SCALA_HOME/bin

For Windows, use SET instead of EXPORT and ; and not :.



