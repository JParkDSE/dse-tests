# pth

Performance Test Harness (pth) provides tools for sending lines (producers) and monitoring data stores (monitors). 


## Installation

### Software Prerequsites

You must have java, maven, and git installed. 

#### Linux 
<pre>
sudo yum -y install epel-release
sudo yum -y install git
sudo yum -y install java-1.8.0-openjdk
sudo yum -y install maven
</pre>

#### Windows 
- Install [Java](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) 
  -- Java SE Development Kit Windows x64.  
  -- Accept Defaults for installs.
  -- Open Windows Advanced System Settings; Environemnt Variables
  -- Create a new System Variable; Variable name: JAVA_HOME, Variable value: C:\Program Files\Java\jdk1.8.0_121.  
  -- NOTE: The last number should match the version of Java you installed. You can use Explorer and navigate to the folder. then cut and paste the value.
- Install [Git](https://git-scm.com/download/win) Download 64-bit Git for Windows Setup. Defaults for all installation dialogs. 
  -- You can use defaults during install
- Install [Maven](https://maven.apache.org/download.cgi)
  -- Download the Binary zip archive and unzip (I usually put it in C:\) 
  -- Open Windows Advanced System Settings; Environemnt Variables
  -- Edit the Path variable and append Maven to the path. Append a semicolon followed by path to Maven bin folder (e.g. ;C:\apache-maven-3.5.0\bin).  Cut and paste is helpful.

### Build pth

<pre>
git clone https://github.com/rtrujill007/dse-tests
cd dse-tests/dse-pth
mvn install 
</pre>

After Build; the target folder will contain:
- lib folder: all of the jar dependencies
- pth.jar: small executable jar without dependencies.
- pth-full.jar: big executable jar with dependencies.

### Senders (send)
These tools send lines from a file.
- [Kafka](./docs/Kafka.md) : Send lines to Kafka topic.

### Monintor (mon)
These tools montior counts and report changes.
- [SolrIndexMon](./docs/SolrIndexMon.md) : Monitor count and rate for Solr Index.
- [CassandraMon](./docs/CassandraMon.md) : Monitor count and rate for Cassandra Table.
- [KafkaTopicMon](./docs/KafkaTopicMon.md) : Monitor count and rate for Kafka Topic.


### Data

Small sample `planes.csv` data is included.  This file has 100,000 lines.


## License

http://www.apache.org/licenses/LICENSE-2.0 




