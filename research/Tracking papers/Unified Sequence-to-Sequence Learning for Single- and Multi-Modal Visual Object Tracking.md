---
aliases:
  - SeqTrack
tags:
  - paper
  - tracking
---

## Abstract
 - Sequence-to-sequence learning framework for RGB-based and multi-modal object tracking
 - Casts visual tracking as a sequence generation task, forecasting object bounding boxes in an autoregressive manner.
## Intro
 - Existing tracking approaches commonly employ a divide-and-conquer strategy, wherein the tracking problem is decomposed into multiple subtasks, such as 
	 - object scale estimation 
	 - center point localization
 - Deficiencies this paper solves
	 - First, each subtask necessitates a customized head network, leading to a complicated tracking framework.
	 - Second, each head network requires one or more learning loss functions, such as cross-entropy loss [1], [4], ℓ1 loss [1], [4], [6], [7], and generalized IoU loss [4], [6], [7], making the training challenging due to additional hyperparameters. 
















