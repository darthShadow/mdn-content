---
title: "RTCInboundRtpStreamStats: perDscpPacketsReceived property"
short-title: perDscpPacketsReceived
slug: Web/API/RTCInboundRtpStreamStats/perDscpPacketsReceived
page-type: web-api-instance-property
browser-compat: api.RTCStatsReport.type_inbound-rtp.perDscpPacketsReceived
---

{{APIRef("WebRTC")}}

The **`perDscpPacketsReceived`**
property of the {{domxref("RTCInboundRtpStreamStats")}} dictionary is a record
comprised of key/value pairs in which each key is a string representation of a
Differentiated Services Code Point and the value is the number of packets received for
that DCSP.

> [!NOTE]
> Not all operating systems make data available on a per-DSCP
> basis, so this property shouldn't be relied upon on those systems.

## Value

A record comprised of string/value pairs. Each key is the string representation of a
single Differentiated Services Code Point (DSCP)'s ID number.

> [!NOTE]
> Due to network bleaching and remapping, the numbers seen on
> this record are not necessarily going to match the values as they were when the data
> was sent.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{RFC(2474)}}: The Differentiated Service field in IPv4 and IPv6 headers
