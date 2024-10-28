# Real-time-video-AI-application

## Tasks
- classification
- localization
- object detection
- segmentation

## AI inference 
can ahppen on edge, on premise or on cloud.

Edge-based, ML solution:
- fast response time, lower bandwidth cost,
- mitigate network related problems
- improve data privacy and security

On Cloud/prem:
For more complex and computation heavy, but has the problem of latency
Sending raw visdeos, bandwidth cost, if has low connectivity

## IVA Application workflow
Video stream -> decoded -> preprocessed -> AI inference (detection, classification, ..) -> 
- encode for storage
- displayed
- stream and batch processing (analytics)

## Challenges
Quality, speed, efficiency and cost competitive

Deployment flexibility
Run on small edge devices or public clouds.
Transfer learning fine tuning and optimization

## Deepstream SDK
Gstreamer:
### Elements
Elements are core building blocks
pass data from a source to sink element
from one plugin to the next
- src element passes element to stream
- filter element processes stream

### Bin
A bin is a container for a collection of plugins.
Manages elements contained in it

### Pipeline
Top level bin managing synchronization of the contained elements

### Deepstram:
Allows hardware accelerated plugins, allow processing on gpu and cpu, parallelization and sync

## Streaming Data
### Buffers
Data flows from one lemenet to one or more source pads with buffers.
### Events
Sending of info between plugins.
### Bus 
Bus object responsible for delivering to the application.
### Messages
post info on message bus
### Queries
Allow appllications to request info from pipeline

Sync receives data. access data within the pipeline, deliver messages, 
plug in can for example do inference.

## Metadata Structure
As data passes through buffers, metadata is progressively attached.
Objects and bounding box coordinates, add a probe to access metadata (callback function)
probe callback is very important.
Accuracy, Intersection over union, mean average precision (object detection)
how many stream can our stream handle reliably?
add plugins to identify rate limiting processes. how much an app uses the GPU.
Modular and sclable application.


