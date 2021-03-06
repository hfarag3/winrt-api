---
-api-id: P:Windows.Networking.Sockets.StreamWebSocketControl.ProxyCredential
-api-type: winrt property
---

<!-- Property syntax
public Windows.Security.Credentials.PasswordCredential ProxyCredential { get;  set; }
-->

# Windows.Networking.Sockets.StreamWebSocketControl.ProxyCredential

## -description
The credential to use to authenticate to the proxy server through HTTP header authentication using a [StreamWebSocket](streamwebsocket.md) object.

## -property-value
The credential to use to authenticate to the proxy server through HTTP header authentication.

## -remarks
The [ProxyCredential](streamwebsocketcontrol_proxycredential.md) property must be set before calling the [ConnectAsync](streamwebsocket_connectasync.md) method on the [StreamWebSocket](streamwebsocket.md) object. An attempt to set the [ProxyCredential](streamwebsocketcontrol_proxycredential.md) property after calling the [ConnectAsync](streamwebsocket_connectasync.md) method will result in an error.

## -examples

## -see-also
[How to use advanced WebSocket controls ](http://msdn.microsoft.com/library/0a47f7c3-66f9-4315-886e-bd1afe77bf39), [How to use advanced WebSocket controls ](http://msdn.microsoft.com/library/4ab9621e-90e5-420e-88d0-09f1c7239d7a), [PasswordCredential](../windows.security.credentials/passwordcredential.md), [StreamWebSocket](streamwebsocket.md)