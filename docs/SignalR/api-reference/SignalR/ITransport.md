# ITransport

Defines the basic structure and operations for a transport mechanism in a [HubConnection](../SignalR/HubConnection.md) context. Current implemtations are [WebSocketTransport](../Transports/WebSocketTransport.md) and [LongPollingTransport](../Transports/LongPollingTransport.md). 

## **Fields**:
### **TransferMode**
: Gets the transfer mode used by the transport, which defines whether it's [Binary](../SignalR/TransferModes.md#binary) or [Text](../SignalR/TransferModes.md#text). 
### **TransportType**
: Gets the type of the transport, such as [WebSocket](../SignalR/TransportTypes.md#websocket) or [LongPolling](../SignalR/TransportTypes.md#longpolling). 
### **State**
: Gets the current [TransportStates](../SignalR/TransportStates.md) of the transport, which could be connecting, connected, closing, etc. 
### **ErrorReason**
: Gets a string representation of the reason for any errors that might have occurred during the transport's operations. 
### **OnStateChanged**
: An event that's triggered whenever the state of the transport changes. It provides the previous state and the new state as its parameters. 
## **Methods**:

### **StartConnect**
: Initiates the connection process for the transport. 

### **StartClose**
: Initiates the process to close the transport's connection. 

### **Send**
: Sends data over the transport using the provided [BufferSegment](../Memory/BufferSegment.md). 