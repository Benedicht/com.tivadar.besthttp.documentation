---
comments: true
---
# ConnectionOptionsBuilder

Builder class to help creating [ConnectionOptions](../MQTT/ConnectionOptions.md) instances. 

## Examples
!!! Example
	 The following example creates a [ConnectionOptions](../MQTT/ConnectionOptions.md) to connect to localhost on port 1883 using the TCP transport and MQTT protocol version v3.1.1. 
	```cs
	var options = new ConnectionOptionsBuilder()
	        .WithTCP("localhost", 1883)
	        .WithProtocolVersion(SupportedProtocolVersions.MQTT_3_1_1)
	        .Build();
	
	    var client = new MQTTClient(options);
	```
!!! Example
	 This is the same as the previous example, but the builder creates the [MQTTClient](../MQTT/MQTTClient.md) too. 
	```cs
	var client = new ConnectionOptionsBuilder()
	        .WithTCP("localhost", 1883)
	        .WithProtocolVersion(SupportedProtocolVersions.MQTT_3_1_1)
	        .CreateClient();
	```

## **Methods**:

### **WithTCP**
: Add options for a TCP connection. 

### **WithWebSocket**
: Add options for a WebSocket connection. 

### **WithTLS**
: When used MQTTClient going to use TLS to secure the communication. 

### **WithPath**
: Used by the WebSocket transport to connect to the given path. 

### **WithProtocolVersion**
: The protocol version that the plugin has to use to connect with to the server. 

### **CreateClient**
: Creates an MQTTClient object with the already set options. 

### **Build**
: Creates the final ConnectionOptions instance. 