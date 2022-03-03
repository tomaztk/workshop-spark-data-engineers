# Module 1: Getting to know Apache Spark, Installation and setting up the environment


# What is Apache

Check PPT!

# Apache Applications

Check PPT!

# General installation (quick)

Download anaconda
Start Jupyter notebook
!pip install pyspark


# Installation on Windows
## Step 1: Install Java
Apache Spark appears to primarily run on Java so we need to install that.

Download your favourite flavour of OpenJDK 11. 
Once installed, check the version:

`java --version`

## Step 2: Install Python
Download your favourite way to install Python 3.9. I like Anaconda which you can download [here](https://www.anaconda.com/products/individual#windows).
For the most part next, next, next through the installer.
Tick the box to add it to your PATH environment variable.
Register it as your default Python.

Check that it's installed by opening a command prompt and running:

`python --version`


## Step 3: Install Hadoop
Apache Spark uses Apache Hadoop for it's distributed file services.

Download your favourite way to install Hadoop 3.2+. 
I like this popular precompiled GitHub repository, download the entire repository [here](https://github.com/cdarlint/winutils)
Extract it to your desktop then copy the files from the version folder you want to C:\Hadoop\bin\
Add a new environment variable called HADOOP_HOME and point it to C:\Hadoop then add that environment variable to your PATH environment with the subfolder \bin appended.

Check that it's installed by opening a command prompt and running:

`winutils`


## Step 4: Install Spark
Finally, we've got the prerequisites now we can start to actually install Apache Spark!


Download the latest version for the version of Hadoop you selected above [here](https://spark.apache.org/downloads.html).

Extract the downloaded archive to C:\Spark meaning that the actual files will be in a folder such as: C:\Spark\spark-3.1.1-bin-hadoop3.2

Add a new environment variable called SPARK_HOME and point it to the spark binary folder above then add that to your PATH environment variable.
Check that it's installed by opening a command prompt as admin and running:

`spark-shell`


Once it starts up you can open your web browser and navigate to http://localhost:4040/ where you'll see a status page and you can start trying to run scripts in Scala or Python.

You can start now with funky commands:

```Scala
val textFile = spark.read.textFile("C:\\Spark\\spark-3.1.1-bin-hadoop3.2\\README.md")
textFile.count()
textFile.first()
```

# Installation on Mac

Install Brew
Go to Brew Website https://brew.sh/

Copy the url from Home page on mac os terminal to install Home brew

Run below command to update home brew

`brew upgrade && brew update`

Java Installation
Check Java Version
`Java -version`

Run below command to install Java8
`brew cask install java8`

For Latest Java use
`brew cask install java`

Check Java Version

Install xcode-select
`xcode-select --install`

Install Scala
`brew install scala`

Use `scala -version` to get the scala version

Install Apache Spark
`brew install apache-spark`

To start spark shell execute below command
`Spark-shell`

Run below command to check the execution which will return the string “Hello World”
`val s = "hello world"`

Run `pyspark` to start pyspark shell

Add Spark path to bash profile
Run below command and then add the path to the profile
```
nano ~/.profile
export SPARK_HOME=/usr/local/Cellar/apache-spark/2.4.4/libexec
export PYTHONPATH=/usr/local/Cellar/apache-spark/2.4.4/libexec/python/:$PYTHONP$
source ~/.bash_profile
```

`cd /usr/local/Cellar/apache-spark/2.4.4/libexec/sbin`

And execute below command to start all services
`sbin/start-all.sh`

Check the locations: 

Spark Master UI : http://localhost:8080/

Spark Application UI : http://localhost:4040/



# Docker (!)

Download docker desktop (for Mac or for Windows)!

Convenience Docker Container Images
Spark Docker Container images are available from DockerHub, called [Apache\Spark-py](https://hub.docker.com/r/apache/spark-py/tags), these images contain non-ASF software and may be subject to different license terms.


# Azure services

## Virtual Machines

## HDInsight

## Azure Synapse

## Databricks



# Azure Databricks *

SImple, clean and easy!


# Environment and languages

There are many languages available for Spark API support

## Spark Language (Scala)

## PySpark

## RSpark / Sparkly

## Databricks Pandas (vs. Python Pandas)