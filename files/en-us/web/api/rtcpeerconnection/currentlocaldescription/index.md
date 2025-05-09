---
title: "RTCPeerConnection: currentLocalDescription property"
short-title: currentLocalDescription
slug: Web/API/RTCPeerConnection/currentLocalDescription
page-type: web-api-instance-property
browser-compat: api.RTCPeerConnection.currentLocalDescription
---

{{APIRef("WebRTC")}}

The **`currentLocalDescription`** read-only property of the {{domxref("RTCPeerConnection")}} interface returns an {{domxref("RTCSessionDescription")}} object describing the local end of the connection as it was most recently successfully negotiated since the last time the {{domxref("RTCPeerConnection")}} finished negotiating and connecting to a remote peer.
Also included is a list of any ICE candidates that may already have been generated by the ICE agent since the offer or answer represented by the description was first instantiated.

To change the `currentLocalDescription`, call {{domxref("RTCPeerConnection.setLocalDescription()")}}, which triggers a series of events which leads to this value being set.
For details on what exactly happens and why the change isn't necessarily instantaneous, see [Pending and current descriptions](/en-US/docs/Web/API/WebRTC_API/Connectivity#pending_and_current_descriptions) in the WebRTC Connectivity page.

> [!NOTE]
> Unlike {{domxref("RTCPeerConnection.localDescription")}}, this value represents the actual current state of the local end of the connection;
> `localDescription` may specify a description which the connection is currently in the process of switching over to.

## Value

The current description of the local end of the connection, if one has been set.
If none has been successfully set, this value is `null`.

## Examples

This example looks at the `currentLocalDescription` and displays an alert containing the {{domxref("RTCSessionDescription")}} object's `type` and
`sdp` fields.

```js
const pc = new RTCPeerConnection();
// …
const sd = pc.currentLocalDescription;
if (sd) {
  alert(`Local session: type='${sd.type}'; sdp description='${sd.sdp}'`);
} else {
  alert("No local session yet.");
}
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

> [!NOTE]
> The addition of `currentLocalDescription` and {{domxref("RTCPeerConnection.pendingLocalDescription", "pendingLocalDescription")}} to the WebRTC spec is relatively recent.
> In browsers which don't support them, just use {{domxref("RTCPeerConnection.localDescription", "localDescription")}}.

## See also

- {{domxref("RTCPeerConnection.setLocalDescription()")}}, {{domxref("RTCPeerConnection.pendingLocalDescription")}}, {{domxref("RTCPeerConnection.localDescription")}}
- {{domxref("RTCPeerConnection.setRemoteDescription()")}}, {{domxref("RTCPeerConnection.remoteDescription")}}, {{domxref("RTCPeerConnection.pendingRemoteDescription")}}, {{domxref("RTCPeerConnection.currentRemoteDescription")}}
- [WebRTC](/en-US/docs/Web/API/WebRTC_API)
