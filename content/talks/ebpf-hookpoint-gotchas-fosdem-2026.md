---
title: "eBPF Hookpoint Gotchas: Why Your Program Fires (or Fails) in Unexpected Ways"
date: 2026-02-01
event: "FOSDEM 2026"
location: "Brussels, Belgium"
summary: "Deep dive into eBPF hookpoints - kprobes/fentry, tracepoints, and uprobes - exposing internal kernel mechanics that cause surprising edge cases."
tags:
  - eBPF
  - linux
  - kernel
slides_url: "https://speakerdeck.com/doniacld/ebpf-hookpoint-gotchas-why-your-program-fires-or-fails-in-unexpected-ways"
video_url: "https://mirror.as35701.net/video.fosdem.org/2026/h1308/8GVBN7-ebpf-hooks-gotchas.mp4"
event_url: "https://fosdem.org/2026/schedule/event/8GVBN7-ebpf-hooks-gotchas/"
cover_image: "/images/talks/fosdem-2026-ebpf-gotchas.png"
featured: true
---

Co-presented with Chris Tarazi at FOSDEM 2026 in the eBPF Developer Room.

## Abstract

eBPF programs often behave differently than developers expect, not because of incorrect logic, but because of subtle behaviours of the hookpoints themselves. 

In this talk, we focus on a small set of high-impact, commonly misunderstood attachment types:
- **kprobes/fentry**
- **tracepoints** 
- **uprobes**

We expose the internal kernel mechanics that cause surprising edge cases, explain why they occur, and show how to work around them.

## Resources

- [FOSDEM Event Page](https://fosdem.org/2026/schedule/event/8GVBN7-ebpf-hooks-gotchas/)
- [PDF Slides](https://fosdem.org/2026/schedule/event/8GVBN7-ebpf-hooks-gotchas/)
- [Video Recording](https://mirror.as35701.net/video.fosdem.org/2026/h1308/8GVBN7-ebpf-hooks-gotchas.mp4)
