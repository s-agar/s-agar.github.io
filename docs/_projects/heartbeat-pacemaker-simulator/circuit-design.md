---
title: "Circuit Design"
permalink: "/projects/heartbeat-pacemaker-simulator/circuit-design"
project_main: false
sidebar:
  nav: "heartbeat_pacemaker_simulator_nav"
classes: wide
---

<style>
  .pagination { display: none !important; }
</style>

When researching different approaches to essentially create two timers, one for the heart and one for the pacemaker, the astable (or free-running) multivibrator caught my eye. I could have used, say, a quartz crystal oscillator, but I felt like this wasn't "natural," in the sense that how such a component worked wasn't immediately intuitive to me, and probably wouldn't be to others. But an astable multivibrator can be explained in a relatively simple manner: there are two "buckets" of charge, or capacitors, and only one can be filled at a time. Each bucket takes the same amount of time to fill every time, so when a bucket is filled, it can be emptied into a pipe at a regular interval. Furthermore, every component, in an astable multivibrator circuit, and especially the capacitors, can easily be seen on a circuit board.

## Astable Multivibrator

But what exactly is an astable multivibrator? According to [this source](https://www.electronics-tutorials.ws/waveforms/astable.html), it is a free-running, oscillating circuit that continuously switches between two states, thereby producing two square wave output waveforms. In other words, it's a circuit that creates two pulses at a regular interval.

<blockquote>
    <details>
        <summary>
        An aside
        </summary>
        The astable multivibrator was especially fascinating to me because I had just learned about latches, or cross-coupled transistors, in my digital design class. According to the linked source above, cross-coupled transistors are the core of each of the different types of multivibrators, like monostable, bistable, and astable. In fact, latches are a type of bistable multivibrator, since they have two stable (or resting) states: high or low. The "astable" in "astable multivibrator," therefore, means that the circuit does not have a stable or resting state. This makes sense when considering the fact that the circuit is relentlessly switching between high and low at its two outputs.
    </details>
</blockquote>

<figure>
    <img src="/assets/images/astable-diagram.gif" style="width: 100%; height: auto;">
    <figcaption>An astable multivibrator circuit diagram. <a href="https://www.electronics-tutorials.ws/waveforms/astable.html">Source</a></figcaption>
</figure>

And how does it work? Looking at the circuit above: say TR1 is off and TR2 is on. Then Plate A of C1 is essentially connected straight to Vcc (6V) as there is no voltage drop through R1 (no current is flowing through the resistor since TR1 is not conducting any). Plate B of C1 has about 0.6V because standard NPN transistors usually require a base-emitted voltage of 0.6 to 0.7V. This creates a potential difference of 5.4V across C1. Since TR2 is on, C2 starts to charge up, and as soon as it reaches this 0.6V threshold, it turns TR1 on, causing Plate A of C1 to fall to 0V (with ideal components). This happens because TR1 acts like a closed switch that connects Plate A of C1 straight to ground. The drop in voltage from 6V to 0V on Plate A of C1 causes an equal and instantaneous drop in voltage on Plate B, pulling it down to -5.4V. This reverse voltage turns TR2 off. Since TR1 is now on and TR2 is now off, C1 begins to charge up from -5.4V towards the 6V supply. As C1 reaches 0.6V, though, it turns TR2 back on and TR1 off. Now, the circuit is back to the state described originally, and the whole process repeats again, and again, and again.
