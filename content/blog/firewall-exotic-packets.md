---
title: "Testing a Firewall with Exotic Packets"
date: 2025-04-20
summary: "What I learned generating adversarial network traffic at Axiado."
tags: ["security", "networking", "internship"]
---

This is a placeholder post — replace this with your actual content.

## The Setup

Write about the firewall testing infrastructure here.

## What Broke

Talk about the interesting failures you found.

## Takeaways

> Blockquotes look like this in your color palette — lilac left border on beige.

You can include code blocks too:

```python
from scapy.all import IP, TCP, send

pkt = IP(dst="10.0.0.1") / TCP(dport=80, flags="S")
send(pkt)
```
