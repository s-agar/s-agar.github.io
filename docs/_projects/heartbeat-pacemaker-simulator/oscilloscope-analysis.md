---
title: "Oscilloscope Analysis"
permalink: "/projects/heartbeat-pacemaker-simulator/oscilloscope-analysis"
project_main: false
sidebar:
  nav: "heartbeat_pacemaker_simulator_nav"
# classes: wide
toc: true
toc_sticky: true
---

<style>
  .pagination { display: none !important; }
</style>

<figure>
    <img src="/assets/images/Keysight-MSOX4024A-b0.png.png" style="width: 100%; height: auto;">
    <figcaption>The MSOX 4034A oscilloscope. <a href="https://www.datatec.eu/MSOX4034A">Source</a></figcaption>
</figure>

To precisely analyze the circuit after simulating it over spring break, I used Keysight's MSOX4034A oscilloscope to measure the output signal and to determine characteristics like frequency.

## Heart Rate

The heart rate came out to 1.3683 Hz, or about 82 BPM, similar to the 85 BPM I estimated using the online BPM counter.

<img src="/assets/images/scope_0.png" style="width: 100%; height: auto;">

## Pacemaker

After disconnecting the heart output, the pacemaker's heart rate came out to 1.1218 Hz, or about 73 BPM, very close the 72 BPM I estimated using the online BPM counter.

<img src="/assets/images/scope_1.png" style="width: 100%; height: auto;">
