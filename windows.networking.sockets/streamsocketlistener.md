---
-api-type: winrt class
---
 Create the [StreamSocketListener](streamsocketlistener.md).
 Use the [Control](streamsocketlistener_control.md) property to retrieve a [StreamSocketListenerControl](streamsocketlistenercontrol.md) object and set the socket quality of service required.
 Assign the [ConnectionReceived](streamsocketlistener_connectionreceived.md) event to an event handler.
 Call the [BindServiceNameAsync](streamsocketlistener_bindservicenameasync.md) or [BindEndpointAsync](streamsocketlistener_bindendpointasync.md) method to bind to a local TCP port number or service name. For Bluetooth RFCOMM, the local service name parameter is the Bluetooth Service ID.
 When a connection is received, use the [StreamSocketListenerConnectionReceivedEventArgs](streamsocketlistenerconnectionreceivedeventargs.md) object to retrieve the [Socket](streamsocketlistenerconnectionreceivedeventargs_socket.md) property with the [StreamSocket](streamsocket.md) object created.
 Use the [StreamSocket](streamsocket.md) object to send and receive data.
 Call the [Close](streamsocketlistener_close.md) method to stop listening for and accepting incoming network connections and release all unmanaged resources associated with the [StreamSocketListener](streamsocketlistener.md) object. Any [StreamSocket](streamsocket.md) objects created when a connection is received are unaffected and can continue to be used as needed.