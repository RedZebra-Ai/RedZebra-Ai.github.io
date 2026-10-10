# How Many Channels Do You Actually Need? Sizing 2 / 4 / 6 / 128 for a Site

When you size an edge AI video analytics box, the question that stalls most buyers is not "which vendor" but "how many channels." Channel count drives both price and whether you have enough coverage — too few and you miss events, too many and you pay for compute you never use. This article gives a working method to estimate your count, with real tier mappings, no parameter soup.

## What a "Channel" Actually Means Here

In this context, one channel is one video stream being analyzed. In most deployments a network camera pushes one main stream (RTSP), which maps to one channel. So the routine estimate collapses to: cameras you need AI to watch ≈ channels you need.

A few exceptions are worth naming. If one camera feeds multiple streams at different resolutions, or a PTZ dome treats each preset as a separate target, that single camera can count as more than one channel. But in a standard site those are the minority — estimate 1:1 first, then bump up only for the special cases.

## Why More Channels Isn't Automatically Better

As channel count rises, the decode load, compute, and memory the edge box must hold scale roughly linearly. A box forced well past its designed channel count shows classic symptoms: dropped frames, missed detections, higher latency. It is not "analyzing more," it is "analyzing worse."

So the goal is not "more is safer." The goal is to cover exactly the cameras you actually analyze. Overflow should add a box or move to custom — not get crammed onto one unit and hoped to hold.

Edge boxes are sized around a realistic channels-per-unit budget, not a theoretical ceiling. Pushing past it does not fail loudly — it degrades quietly, which is the dangerous kind, because a missed detection reads as "nothing happened" rather than "the box broke." That is exactly why tier limits are published instead of left for buyers to guess.

## 2 Channels: One Entrance, One Problem

The simplest case is a single gate, a single checkout, or a single loading dock — one place that truly needs AI watching. That maps to the standard 2-channel tier (from USD 399). It is also the common pilot for a larger plan: prove the effect on one or two points, then decide whether to expand.

## 4 Channels: A Small Building or One Busy Zone

When a single small building has four key points to cover — front door, back door, loading area, office zone — 4 channels (USD 999) fits. It stays in the standard tier, deploys as simply as the 2-channel unit, just with double the coverage. What it is not for: cameras scattered across multiple buildings, which will quickly blow past 4.

## 6 Channels: Multi-Entry Single Site

A single multi-floor building, or a perimeter with six monitoring points, lands on the top of the standard tier at 6 channels (USD 1,599). This covers most small and mid-sized sites — one yard, one workshop, one warehouse's boundary and hotspots. What it is not for: campus-scale, multi-building, or cross-line inspection, which will sit comfortably above 6.

## Past 6: When You Move to Custom

Above 6 channels you are generally into campus, multi-building, or production-line inspection — that is the custom tier, quoted per scene. In real deployments, the 2-to-128 channel range is the most economical, and it can in principle extend further. Custom does not carry a fixed price, because camera models, stream bitrates, and detection density vary too much; quoting a dead number would mislead more than help. Better to write the scope, then price it.

## How to Estimate Your Own Count

Walk these four steps:

1. **List the cameras you need AI to watch**, not all cameras. Only the ones that matter — perimeter, entrances, high-risk zones. Pure-recording cameras do not need AI.
2. **Count one channel per camera**, unless it is the multi-stream or PTZ-preset exception above.
3. **Bump up for multi-stream / PTZ** handling. When unsure, add one for headroom.
4. **Leave 10–20% headroom** for points you may add in the next six months.

Map the result to the tiers: at or under 2, look at the standard tier; at or under 6, the top of the standard tier; above 6, talk to us about custom.

A quick example: a small workshop has 8 cameras, but only 5 actually need AI — two gates, a loading bay, a hazardous area, and the main aisle. That is 5 channels, which the 6-channel standard tier covers with room to spare. No custom needed.

## Don't Size on Hope

The most common mistake is buying a big box now "because we might expand to 20 channels later." The steadier path is to run the standard tier, see real results, then move to custom only once you are genuinely above 6. Writing the scope honestly beats writing it large: oversize and you pay for compute you never use; undersize and you find out fast, then add — which is cleaner than guessing.

## Where the Tiers Are Listed

The full tiers, what each channel count includes, and the boundary between standard and custom are laid out on the [RedZebraAI pricing page](https://aisurveillancecamera.com/pricing/). If you cannot pin down your own channel count, send the camera list and we will estimate it for you — no charge. Get the count right first, then buy right.
