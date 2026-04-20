---
title: "Oscilloscope Analysis"
permalink: "/projects/heartbeat-pacemaker-simulator/oscilloscope-analysis"
project_main: false
sidebar:
  nav: "heartbeat_pacemaker_simulator_nav"
classes: wide
---

<style>
  .pagination { display: none !important; }
</style>


<img src="/assets/images/general-img-landscape.png" style="width: 100%; height: auto;"> <!-- image of msox 4034a -->

To precisely analyze the circuit after simulating it over spring break, I used Keysight's MSOX4034A oscilloscope to measure the output signal and to determine characteristics like frequency.

## Heart Rate

The heart rate came out to 1.3683 Hz, or about 82 BPM, similar to the 85 BPM I estimated using the online BPM counter.

<img src="/assets/images/general-img-landscape.png" style="width: 100%; height: auto;"> <!-- scope0 -->

## Pacemaker

After disconnecting the heart output, the pacemaker's heart rate came out to 1.1218 Hz, or about 73 BPM, very close the 72 BPM I estimated using the online BPM counter.

<img src="/assets/images/general-img-landscape.png" style="width: 100%; height: auto;"> <!-- scope1 -->
