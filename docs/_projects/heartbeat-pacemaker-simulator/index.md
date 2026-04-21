---
title: "Hearbeat and Pacemaker Simulator"
permalink: "/projects/heartbeat-pacemaker-simulator"
project_main: true
sidebar:
  nav: heartbeat_pacemaker_simulator_nav
excerpt: "My ECE 1100 Discovery Project in which I design a heartbeat and pacemaker simulator circuit for modelling purposes."
header:
  teaser: /assets/images/heartbeat-pacemaker-simulator.jpg
# classes: wide
toc: true
toc_sticky: true
---

<style>
  .pagination { display: none !important; }
</style>

<img src="/assets/images/heartbeat-pacemaker-simulator.jpg" style="width: 100%; height: auto;">

The goal of this project was to improve my analog circuit design, signal processing, and oscilloscope skills while also learning about the heart and related medical devices.
- This project entailed creating a circuit model of a heart and a corresponding pacemaker.
- One part of the circuit simulates a heartbeat via a timed signal and an LED that pulses according to the signal. The other part of the circuit simulates a demand pacemaker that detects when the heartbeat becomes irregular or stops and then sends a pulse to correct or replace the heartbeat.
- Users can interact with this model by disconnecting a wire to simulate an irregular or stopped heartbeat.
- Two stretch goals of this project include adding parts to the circuit to model a defibrillator and designing and fabricating a PCB for the circuit, both of which I plan to do in the future.

## Background

For my ECE 1100 class, I was tasked with creating a "Discovery Project", or any ECE-related project that would help me build one or more ECE-related skills.

I instantly knew I wanted to build something related to the medical field, but I wasn't sure what. Also, as I thought about the skills I wanted to develop, I realized that I didn't want to use a microcontroller or any sort of logical chip, as I already had experience with those components. I wanted to work with more "natural" signals, not 0s and 1s, which is what led me to analog circuitry for this project.

As I considered natural signals in the medical field, one stood out: the electrical impulse that causes the heart to pump blood. This brought me to medical devices that electrically interact with the heart: the pacemaker and the defibrillator.

I realized I could model the heart and these devices through an analog circuit. Not only could this allow me to learn about how they work and about analog circuit design, but it could also be a tool for others to learn about the heart and related devices. Furthermore, it could encourage others to consider the amazing intersection between engineering and medicine!

## Skills Practiced
- Analog Circuit Design
- Oscilloscope Usage
- LTSpice Circuit Simulation
