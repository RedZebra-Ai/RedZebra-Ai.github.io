title: Connecting RTSP Cameras to an Edge AI Box

layout: default

# Connecting RTSP Cameras to an Edge AI Box: Protocols, Codecs, and the Pitfalls Nobody Warns You About

## 1. Why This Guide Exists
Most businesses and campuses already run IP cameras and want AI without replacing their lenses. An edge AI box sits behind the cameras and reuses the existing optics. This guide is a pre-deployment checklist written for system integrators — not a product page.

## 2. What RTSP Is — and Why Your Cameras Speak It
RTSP (Real-Time Streaming Protocol) is the de facto standard for camera output. This section explains how RTSP relates to ONVIF (ONVIF handles discovery and configuration; RTSP handles pulling the stream) and the main-stream vs sub-stream choice that analytics should consume.

## 3. The Codec Decision: H.264 vs H.265 at the Edge
The core differences in compression ratio and compute cost, and what they mean for an edge box in terms of bandwidth, storage, and device load. The conclusion is stated up front; the deep comparison is deferred to article A2 so the two do not overlap.

## 4. Bandwidth and Storage: The Math Before You Deploy
Per-channel bitrate estimates for 1080p / 4MP / 4K, a quick calculation of local edge storage pressure, and a small table integrators can use to estimate bandwidth by camera count.

## 5. Pitfalls Nobody Warns You About
ONVIF profile mismatch (Profile S vs T confusion), sub-stream being ignored by analytics while main-stream is too heavy, NAT/firewall blocking RTSP (UDP-to-TCP negotiation), multi-vendor codec negotiation failures, missing NTP time sync causing event timing errors, and audio streams interfering with video pull.

## 6. Pre-Deployment Field Checklist
An item-by-item checklist covering protocol, bitrate, resolution, ONVIF profile, network, power, and storage headroom — the "Field Checklist" promised in the title, ready for integrators to tick off on site.

## 7. Where RedZebraAI Fits — and What to Read Next
A natural paragraph noting that RedZebraAI edge boxes support RTSP ingestion, 198+ algorithms, and 2–128 channels, linking once to the algorithms list (naked URL or brand name anchor, no keyword stuffing), then guiding readers to the algorithm catalog without a hard sell.
