# mqttKafkaBridge

Bridge which consumes MQTT messages and republishes them on Kafka on the same topic.

## Usage

    $ java -jar mqttKafkaBridge.jar [options...]

Where `options` are:

    --help (-h)  : Show help
    --id VAL     : MQTT Client ID
    --topics VAL : MQTT topic filters (comma-separated)
    --uri VAL    : MQTT Server URI
    --zk VAL     : Zookeeper connect string

## Logging
`mqttKafkaBridge` uses [log4j](http://logging.apache.org/log4j/2.x/) for logging, as do the [Paho](http://www.eclipse.org/paho/) and [Kafka](http://kafka.apache.org/) libraries it uses. There is a default `log4j.properties` file packaged with the jar which simply prints all messages of level `INFO` or greater to the console. If you want to customize logging, simply create your own `log4j.properties` file, and start up `mqttKafkaBridge` as follows:

    $ java -Dlog4j.configuration=file:///path/to/log4j.properties -jar mqttKafkaBridge [options...]

