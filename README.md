DCMonitor
=====

A simple, lightweight Data Center monitor, currently includes Zookeeper, Kafka, [Druid](http://druid.io/)(in progress). Motivated by [KafkaOffsetMonitor](https://github.com/quantifind/KafkaOffsetMonitor), but faster and more stable.

It is written in java, and use [InfluxDB v0.9](https://github.com/influxdb/influxdb) as historical metrics storage.

###Zookeeper monitor


![](img/zk.png)

###Kafka monitor


![](img/kafka_sum.png)
![](img/kafka_offset.png)

##Installation

Node: java(1.6 or later version) is needed for compilation and runing.

* Set up your Zookeeper, Kafka, Druid(If you have) for monitoring.
* Set up [InfluxDB](https://github.com/influxdb/influxdb) v0.9.
	
	If v0.9 haven't been finally released by now, you may have to compile it yourself. Check its [doc](https://github.com/influxdb/influxdb/blob/master/CONTRIBUTING.md) to see how to compile InfluxDB.

* Compile & deploy DCMonitor

	* compile
	
	```
	git clone git@github.com:shunfei/DCMonitor.git
	cd DCMonitor
	./build.sh
	```
Then a `target` folder will be generated.
	
	* deploy
	
	You only need to deploy `target`, `run.sh`, `config` to target machine. Modify those files in `config` and run `run.sh`. If every thing is fine, visit `http://hostname:8075` to enjoy!
	
	