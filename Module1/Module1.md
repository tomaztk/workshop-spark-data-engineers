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





<!-- wp:heading -->
<h2 id="windows"><strong>Windows</strong></h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Installing Apache Spark on Windows computer will require preinstalled Java JDK (Java Development Kit). Java 8 or later version, with current version 17. On <a rel="noreferrer noopener" href="https://www.oracle.com/java/technologies/downloads/" target="_blank">Oracle website,</a> download the Java and install it on your system. Easiest way is to download the x64 MSI Installer. Install the file and follow the instructions. Installer will create a folder like "C:\Program Files\Java\jdk-17.0.1".</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":7534,"width":525,"height":310,"sizeSlug":"large","linkDestination":"media"} -->
<div class="wp-block-image"><figure class="aligncenter size-large is-resized"><a href="https://tomaztsql.files.wordpress.com/2021/12/screenshot-2021-12-02-at-19.45.16.png"><img src="https://tomaztsql.files.wordpress.com/2021/12/screenshot-2021-12-02-at-19.45.16.png?w=693" alt="" class="wp-image-7534" width="525" height="310"/></a></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>After the installation is completed, proceed with installation of Apache Spark. Download Spark from the  <a rel="noreferrer noopener" href="https://spark.apache.org/downloads.html" target="_blank">Apache Spark website</a>. Select the Spark release 3.2.0 (Oct 13 2021) with package type: Pre-built for Apache Hadoop 3.3 and later.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":7538,"width":625,"height":199,"sizeSlug":"large","linkDestination":"media"} -->
<div class="wp-block-image"><figure class="aligncenter size-large is-resized"><a href="https://tomaztsql.files.wordpress.com/2021/12/screenshot-2021-12-02-at-20.02.02.png"><img src="https://tomaztsql.files.wordpress.com/2021/12/screenshot-2021-12-02-at-20.02.02.png?w=700" alt="" class="wp-image-7538" width="625" height="199"/></a></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Click on the file <em>"spark-3.2.0-bin-hadoop3.2.tgz"</em> and it will redirect you to download site.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p></p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":7540,"width":530,"height":221,"sizeSlug":"large","linkDestination":"media"} -->
<div class="wp-block-image"><figure class="aligncenter size-large is-resized"><a href="https://tomaztsql.files.wordpress.com/2021/12/screenshot-2021-12-02-at-20.06.13.png"><img src="https://tomaztsql.files.wordpress.com/2021/12/screenshot-2021-12-02-at-20.06.13.png?w=667" alt="" class="wp-image-7540" width="530" height="221"/></a></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Create a folder -  I am creating <em>C:\SparkApp</em> and unzipping all the content of the tgz file into this folder. The final structure of the folder should be: <em>C:\SparkApp\spark-3.2.0-bin-hadoop3.2</em>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p></p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":7542,"width":528,"height":347,"sizeSlug":"large","linkDestination":"media"} -->
<div class="wp-block-image"><figure class="aligncenter size-large is-resized"><a href="https://tomaztsql.files.wordpress.com/2021/12/2021-12-02-20_19_56-window.png"><img src="https://tomaztsql.files.wordpress.com/2021/12/2021-12-02-20_19_56-window.png?w=685" alt="" class="wp-image-7542" width="528" height="347"/></a></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Furthermore, we need to set the environment variables. You will find them in Control Panel -&gt; System -&gt; About -&gt; Advanced System Settings and go to Advanced Tab and click Environment variables. Add three User variables: <code>SPARK_HOME</code>,&nbsp;<code>HADOOP_HOME</code>,&nbsp;<code>JAVA_HOME</code></p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":7546,"sizeSlug":"large","linkDestination":"media"} -->
<div class="wp-block-image"><figure class="aligncenter size-large"><a href="https://tomaztsql.files.wordpress.com/2021/12/2021-12-02-20_36_11-window.png"><img src="https://tomaztsql.files.wordpress.com/2021/12/2021-12-02-20_36_11-window.png?w=636" alt="" class="wp-image-7546"/></a></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>with following values:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><code>SPARK_HOME</code>  <em>C:\SparkApp\spark-3.2.0-bin-hadoop3.2</em>.\bin<br><code>HADOOP_HOME</code>&nbsp;<em>C:\SparkApp\spark-3.2.0-bin-hadoop3.2</em>.\bin<br><code>JAVA_HOME</code> <em>C:\Program Files\Java\jdk-17.0.1\bin</em></p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":7547,"width":532,"height":504,"sizeSlug":"large","linkDestination":"media"} -->
<div class="wp-block-image"><figure class="aligncenter size-large is-resized"><a href="https://tomaztsql.files.wordpress.com/2021/12/2021-12-02-20_39_08-window-1.png"><img src="https://tomaztsql.files.wordpress.com/2021/12/2021-12-02-20_39_08-window-1.png?w=621" alt="" class="wp-image-7547" width="532" height="504"/></a><figcaption>And repeat for all three variables.</figcaption></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>The last part is the download of the Winutil.exe file and paste it to the bin folder of your Spark binary; into: C:\SparkApp\spark-3.2.0-bin-hadoop3.2\bin.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Winutil can be found on <a rel="noreferrer noopener" href="https://github.com/steveloughran/winutils/blob/master/hadoop-3.0.0/bin/winutils.exe" target="_blank">Github</a> and I am downloading for Hadoop-3.0.0.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":7549,"width":410,"height":181,"sizeSlug":"large","linkDestination":"media"} -->
<div class="wp-block-image"><figure class="aligncenter size-large is-resized"><a href="https://tomaztsql.files.wordpress.com/2021/12/2021-12-02-21_35_07-window.png"><img src="https://tomaztsql.files.wordpress.com/2021/12/2021-12-02-21_35_07-window.png?w=544" alt="" class="wp-image-7549" width="410" height="181"/></a></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>After copying the file, open Command line in your windows machinee. Navigate to C:\SparkApp\spark-3.2.0-bin-hadoop3.2\bin and run command <em>spark-shell</em>. This CLI utlity comes with this distribution of Apache spark. You are ready to start using Spark.</p>
<!-- /wp:paragraph -->


# Installation on Mac


<!-- wp:paragraph -->
<p>With installing Apache Spark on MacOS, most of the installation can be done using CLI.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Presumably, you already have installed BREW. You can always update the brew to latest version:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>brew upgrade &amp;&amp; brew update </code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>After this is finished, run the java installation </p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">brew install java8
brew install java
brew install openjdk</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>Installing xcode is the next step:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>xcode-select --install</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p> After this is finished, install scala:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>brew install scala</code></pre>
<!-- /wp:code -->

<!-- wp:image {"id":7555,"sizeSlug":"large","linkDestination":"media"} -->
<figure class="wp-block-image size-large"><a href="https://tomaztsql.files.wordpress.com/2021/12/screenshot-2021-12-02-at-22.04.28.png"><img src="https://tomaztsql.files.wordpress.com/2021/12/screenshot-2021-12-02-at-22.04.28.png?w=1024" alt="" class="wp-image-7555"/></a></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p> And the final step is to install Spark by typing the following command in CLI:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>brew install apache-spark</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>And run:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>brew link apache-spark</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Finally, to execute the Spark shell, command is the same in Windows as it is in MacOS. Run the following command to start spark shell:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>Spark-shell</code></pre>
<!-- /wp:code -->

<!-- wp:image {"align":"center","id":7563,"width":769,"height":463,"sizeSlug":"large","linkDestination":"media"} -->
<div class="wp-block-image"><figure class="aligncenter size-large is-resized"><a href="https://tomaztsql.files.wordpress.com/2021/12/screenshot-2021-12-02-at-22.31.50.png"><img src="https://tomaztsql.files.wordpress.com/2021/12/screenshot-2021-12-02-at-22.31.50.png?w=1024" alt="" class="wp-image-7563" width="769" height="463"/></a></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Spark is up and running on OpenJDK VM with Java 11.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Compete set of code, documents, notebooks, and all of the materials will be available at the Github repository:&nbsp;<a rel="noreferrer noopener" href="https://github.com/tomaztk/Spark-for-data-engineers" target="_blank">https://github.com/tomaztk/Spark-for-data-engineers</a></p>
<!-- /wp:paragraph -->


# Installing on mac Alternatively


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
export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk-17.0.2.jdk/Contents/Home

#export SPARK_HOME=/usr/local/Cellar/apache-spark/3.2.1/libexec
export SPARK_HOME=/opt/homebrew/Cellar/apache-spark/3.2.1/libexec

#export PATH=/usr/local/Cellar/apache-spark/3.2.1/bin:$PATH
export PATH=/opt/homebrew/Cellar/apache-spark/3.2.1:$PATH
export PYSPARK_PYTHON=/Users/tomazkastrun/opt/anaconda3/bin/python
```

Source the profile by:

`soruce .zshrc`

`source ~/.bash_profile`


`cd /usr/local/Cellar/apache-spark/2.4.4/libexec/sbin`

And execute below command to start all services

` bash sbin/start-all.sh`

Check the locations: 

Spark Master UI : http://localhost:8080/
Or Alternatively: http://192.168.0.242:8080/

Spark Application UI : http://localhost:4040/
and Alternatevly: http://192.168.0.242:4040/


Start Jupyter notebook and type:

```
import pyspark
from pyspark import SparkContext
sc = SparkContext()
n = sc.parallelize([4,10,9,7])
n.take(3)
```

# Docker (!)

Download docker desktop (for Mac or for Windows)!

Convenience Docker Container Images
Spark Docker Container images are available from DockerHub, called [Apache\Spark-py](https://hub.docker.com/r/apache/spark-py/tags), these images contain non-ASF software and may be subject to different license terms.


# Azure services

## Virtual Machines

Create a Virtual Machine and install the above processes on your own! (repeat installation for Windows or for Linux/MACos)

## HDInsight

## Azure Synapse



## Azure Databricks *

SImple, clean and easy!
1) Get free Azure subscription
2) Connect to Databricks
Note: Azure Free Trail subscription has a limit of 4 cores, and you cannot use Azure Databricks using a Free Trial Subscription because to create spark cluster which requires more than 4 cores.

Workaround:

You could try below steps as a workaround:

1) Create a free subscription

2) Go to your profile and change your subscription to pay-as-you-go

3) Remove the spending limit (steps here) to allow quota request.

4) Request quota increase.

5) When you create your Azure Databricks workspace, you can select the Trial (Premium - 14-Days Free DBUs) pricing tier to give the workspace access to free Premium Azure Databricks DBUs for 14 days.


# Environment and languages

There are many languages available for Spark API support

## Spark Language (Scala)

## PySpark

## RSpark / Sparkly

## Databricks Pandas (vs. Python Pandas)

