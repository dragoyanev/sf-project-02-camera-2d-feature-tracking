# SFND 2D Feature Tracking

<img src="images/keypoints.png" width="820" height="248" />

# Rubric

## MP.0 Mid-Term Report  
this file is providing all information

## MP.1 Data Buffer Optimization 
 I have used deque structure as more effective - commit 80e80eebc75d

## MP.2 Keypoint Detection 
 commit 69368d9b30

## MP.3 Keypoint Removal 
 commit c2c7de9615

## MP.4 Keypoint Descriptors 
 commit 45e1b333f3f

## MP.5 Descriptor Matching 
 commit dab48e55afc6

## MP.6 Descriptor Distance Ratio 
 commit 1c56996b212


## MP.7 Performance Evaluation 1

Provided data in spreadsheet table in ~workspace/mid\_term\_project.ods 


# #MP.8 Performance Evaluation 2

Provided data in spreadsheet table in ~workspace/mid\_term\_project.ods 


## MP.9 Performance Evaluation 3

Provided data in spreadsheet table in ~workspace/mid\_term\_project.ods 

Based on the numbers I have evaluated with these image sequences I suggest usage of the 
Detector type `SHI-TOMASI` because it returns most unique keypoints.
The time ratio used per point detection is low. 

The Detector type `FAST` have faster initial detection time but after filtering 
the unique keypoints count is decreased drastically and the time increased so the method is loosing effectivenes.

The time for keypoints detection is having bigger impact than the matching methods.

The count points in the matching methods are dependent on the detector results 
so here the speed is more important factor than the count.

This is my TOP3 taking in account key point count, speed ratio and the above explanations:

1. `SHI-THOMASI` / `BRIEF`
2. `SHI-THOMASI` / `ORB`
3. `SHI-THOMASI` / `BRISK`

