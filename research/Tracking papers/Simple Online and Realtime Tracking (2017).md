---
tags:
  - paper
  - tracking
  - realtime
  - kalman
  - SORT
  - Hungarian
aliases:
  - SORT
---
[SORT](https://arxiv.black/pdf/1602.00763)

Variants of interest:
 - [[DeepSort]]
 - [[HybridSort]]

## Abstract
 - Pragmatic approach to multiple object tracking where the main focus is to associate objects efficiently for online and realtime applications.
 - tracking-by-detection
 - Kalman Filter
 - Hungarian Algorithm
 - Up to 260 Hz
## Intro
 - This work is primarily targeted towards online tracking where only detections from the previous and the current frame are presented to the tracker.
 - Aim is to associate detections across frames in a video sequence
 - excludes occlusion
### Main Contributions
 - We leverage the power of CNN based detection in the context of MOT.
 - A pragmatic tracking approach based on the Kalman filter and the Hungarian algorithm is presented and evaluated on a recent MOT benchmark.
 - Code will be open sourced to help establish a baseline method for research experimentation and uptake in collision avoidance applications.
 - Traditional approaches
## Literature review
 - [Multiple Hypothesis Tracking](https://ieeexplore.ieee.org/document/1102177)
 - [Joint Probabilistic Data Association](https://openaccess.thecvf.com/content_iccv_2015/html/Rezatofighi_Joint_Probabilistic_Data_ICCV_2015_paper.html)
 ### Hungarian Algorithm
	 1. tracklets are formed by associating detections across adjacent frames
	 where both geometry and appearance cues are combined to form the affinity
	 matrix
	 2. tracklets are associated to each other to bridge broken trajectories
	 caused by occlusion, again using both geometry and appearance cues

## Methodology
### Detection
 - capture features, propose regions and classify
 - Old detector -> FrRCNN(VGG16)
### Estimation Model
 - Object representation and motion model
	 - used to propagate the object to the next frame
 - $X = [u,v,s,r, \dot{u}, \dot{v}, \dot{s}]^{\text{T}}$
 - u and v are horizontal and vertical positions of the center pixel of the target
 - s and r are scale and aspect ratio
 - this is followed by horizontal, vertical and scale change over time ($\dot{r}$ is considered constant)
 - detections update this model, otherwise this model predicts
### Data Association

 
 
 
 