---
title: RTCPeerConnectionIceEvent
slug: Web/API/RTCPeerConnectionIceEvent
page-type: web-api-interface
browser-compat: api.RTCPeerConnectionIceEvent
---

{{APIRef("WebRTC")}}

The **`RTCPeerConnectionIceEvent`** interface represents events that occur in relation to {{Glossary("ICE")}} candidates with the target, usually an {{domxref("RTCPeerConnection")}}.

Only one event is of this type: {{domxref("RTCPeerConnection.icecandidate_event", "icecandidate")}}.

{{InheritanceDiagram}}

## Instance properties

_A `RTCPeerConnectionIceEvent` being an {{domxref("Event")}}, this event also implements these properties_.

- {{domxref("RTCPeerConnectionIceEvent.candidate")}} {{ReadOnlyInline}}
  - : Contains the {{domxref("RTCIceCandidate")}} containing the candidate associated with the event, or `null` if this event indicates that there are no further candidates to come.

## Constructors

- {{domxref("RTCPeerConnectionIceEvent.RTCPeerConnectionIceEvent()", "RTCPeerConnectionIceEvent()")}}
  - : Returns a new `RTCPeerConnectionIceEvent`. It takes two parameters, the first being a string representing the type of the event; the second a dictionary containing the {{domxref("RTCIceCandidate")}} it refers to.

## Instance methods

_A `RTCPeerConnectionIceEvent` being an {{domxref("Event")}}, this event also implements these properties. There is no specific {{domxref("RTCDataChannelEvent")}} method._

## Examples

```js
pc.onicecandidate = (ev) => {
  console.log(
    `The ICE candidate ('${ev.candidate.candidate}') added to connection.`,
  );
};
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [WebRTC](/en-US/docs/Web/API/WebRTC_API)
- Its usual target: {{domxref("RTCPeerConnection")}}.
