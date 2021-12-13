# Table of Contents
* Abstract
* [Introduction](#1-introduction)
* [Related Work](#2-related-work)
* [Technical Approach](#3-technical-approach)
* [Evaluation and Results](#4-evaluation-and-results)
* [Discussion and Conclusions](#5-discussion-and-conclusions)
* [References](#6-references)

# Abstract

This project attempts to use software defined radios to create a detector of Wifi and Bluetooth signals. I have used this project as the first part to a larger project which will use the detection of these signals within a network of SDRs to be able to locate the radio source that is emitting the Wifi or Bluetooth signal.

# 1. Introduction

## Motivation & Objective: 
    In this project, I will be using a network of time synchronized Software Defined Radios to create a spatial radar-like system to collect information about an environment including radio sources as well as object detection that may be out of the visible range. The motivation comes from being able to use a system like this to monitor the capacity of a room or use it for security. For example, this could also be used in search and rescue to triangulate a radio source in a remote location with greater accuracy than GPS as the area where the system would be deployed is smaller, thus can detect the source with greater SNR. This technology can also be used to monitor heartbeat and breathing for a room with multiple people which can be useful in a hospital setting.

## State of the Art & Its Limitations
Modern SDRs are used by amateur radio hobbyists and are very common. In a software defined radio (SDR), the motivation is that all the signal processing such as the demodulation is done in software rather than by dedicated hardware. This means that the only RF hardware needed is basically an A/D or D/A converter, an amplifier, and an antenna. This allows for greater flexibility of uses for the radio with a single unit. SDRs are heavily used in military and cellphone operations, where devices need to adapt to multiple different communication standards and protocols. SDRs are being used currently for spatial radar in areas in the military, security, and other scientific research fields. The flexibility of the approach allows for multiple antennas and receivers to be placed to allow for detection on a very wide spectrum.

## Novelty & Rationale: What is new in your approach and why do you think it will be successful?
I believe my approach is slightly different because it will eventually be used for object detection that would be outside of radio sources. I want to advance this project into a Masters capstone project, so while the class project might not cover this scope, I hope that eventually I am able to heartbeats and breathing in a room with multiple people. 

## Potential Impact
This project, if successful, could be very useful in a security or medical field. If I can detect heartbeats and breathing in a room, it could be used to monitor multiple patients in a hospital with a single setup of distributed SDRs instead of potentially invasive individual monitors on patients. 

## Challenges

There were significant challenges with this part of the project, the first being to get GNU radio set up and running. Talking to some students in Professor Srivastava's lab, getting the GNU radio framework set up and working to transmit and receive signals is a challenge in itself to acheive in the time frame of the class. The original goal of this first part was to be able to locate signals in 2d. However, the challenges and background information I needed to ramp up with GNURadio and telecommunication systems was signficant. I was able to create a detector for wifi and bluetooth. The future setup for wireless detection of heartbeats and breathing will require a different set of skills with finding datasets and a model that will help us detect heartbeat and breathing from the radios transmitting and receiving signals. 

## Requirements for Success

Because this project uses SDRs where all the signal processing is done in software, a signficant amount of knowledge of signal processing and communication systems will be needed. Getting GNU radio setup will be another challenge that is more on the software side. Once I move on to triangulation of an unknown radio source, I will require various forms of existing data to train a model to facilitate AMC (automatic modulation classification) so that I can detect an unkown source. For detecting heartbeats and breathing, I will require other datasets to detect changes in the Wifi channel estimate. In terms of resources, I currently am using 2 SDRs and 2 antennas in the 2.4-5 Ghz range to help me detect Wifi and Bluetooth signals. This frequency range allows me to detect the full wifi and bluetooth band.

## Metrics of Success

For the scope of this class, the metric for success is to be able to detect presense of a Wifi or Bluetooth signal using a single SDR. For the larger scope of the capstone project, my goal will be to triangulate the location of an unknown radio source in the 2.4 Ghz band.

# 2. Related Work

## 9.a. Papers

List the key papers that you have identified relating to your project idea, and describe how they related to your project. Provide references (with full citation in the References section below).

Wireless breathing detection: http://eprints.gla.ac.uk/225797/
    This paper discusses how the researchers were able to use a SDR and the channel state information to detect the movements caused by breathing on a single human subject

SDR Radar: https://corescholar.libraries.wright.edu/etd_all/91/
    This paper discusses what different parameters to create an effective SDR based radar using GNU radio

UAV Triangulation of CellPhone for Search and Rescue: https://digital.wpi.edu/concern/student_works/gb19f842x
    This paper discusses how a Unmanned Aerial Vehicle (UAV) with an SDR could be used to detect a cell phone signal by finding its direction and using the orientation of the UAV itself.


## 9.b. Datasets

I will be searching for datasets in the latter half of the project for my capstone.

## 9.c. Software

I will be using the GNU Radio open source framework for my SDRs. This framework contains different blocks for common communication protocols such as bluetooth and wifi. This will make the implementation of detecting a cellular source much simpler as I will not need to do all the signal processing from scratch. This will allow me to make full use of the SDRs flexibility for detecting radio sources.

# 3. Technical Approach

## Wifi Specification

A majority of the


# 4. Evaluation and Results

# 5. Discussion and Conclusions

# 6. References
