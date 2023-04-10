# __Exercise Recognition & Rep Counting__

1. Background, what is it and its application?

> Context

While motion-based sensor is the most popular approach, it's an expensive method and limited to tracking a particular body part which the sensor is attached to.

Vision-based approaches, on the other hand, offer more flexibility. 

There are several vision-based methods, often each method is specifically designed for an exclusive problem (e.g. workout rep counting). 

> Applications
- activity monitoring
- sports and fitness tracking
- AR gaming
- insights and correlation to biological data (heartrate, pulse, breath, etc)

> Contents to be discussed

*4* foundational frameworks for human pose estimation:

        - OpenPose
        - AlphaPose
        - MediaPipe
        - Yolo v7 & v8

*5* popular methods:

        - RepNet: Class Agnostic rep counting in the Wild
        - Rule-based exercise rep counting using Pose Estimation
        - Exercise rep counting using ideas from Signal Processing
        - GymCam
        - Rep counting using a DL-based Optical Flow Approach

2. Technical Review and Existing Methods

A. Frameworks (brief) review:

> OpenPose


Github: https://github.com/CMU-Perceptual-Computing-Lab/openpose

Documentation: https://cmu-perceptual-computing-lab.github.io/openpose/web/html/doc/md_doc_00_index.html



> AlphaPose

Github: https://github.com/MVIG-SJTU/AlphaPose

Documentation (trên Github luôn): https://github.com/MVIG-SJTU/AlphaPose/tree/master/docs

Paper: https://arxiv.org/pdf/1612.00137.pdf



> MediaPipe

Github: https://github.com/google/mediapipe

Documentation: https://developers.google.com/mediapipe/solutions/guide



> Yolo 

Github YOLO v7: https://github.com/WongKinYiu/yolov7
Github Yolo v8: https://github.com/ultralytics/ultralytics

Documentation: https://docs.ultralytics.com

Paper: https://arxiv.org/pdf/2207.02696.pdf


B. Frameworks comparision

- Chưa tìm hiểu đủ kĩ để liệt kể ra pros and cons
- YOLO, MediaPipe và OpenPose có vẻ có documentation rõ ràng nhất
- 

C. Existing solutions

> RepNet 

[6]

Summary:
- Estimate the period of time an action is repeated
- Count rep and time of each rep, NOT detect type of exercise
- Work for UNSEEN VIDEOS 
- TSM (explained below in architechture highlights section)
- Resource intensive
- Restricted input: limited number of frames of input video (bcuz the size of the TSM = number of input frames)

Input & Output:
- Input: Video
- Output: per-frame period length and per-frame periodicity score

Dataset:

- 
Architechture highlight:


Temporal Similarity Matrix (TSM)






> Rule-based

> Signal Processing

> GymCam

> DL-based Optical Approach







3. Dataset

4. Hardware requirement

5. Reference

[1] Recognizing exercises and rep counting in real time, 2020. https://arxiv.org/pdf/2005.03194.pdf

[2] A review of different approaches to vision-based rep counting, 2023. https://towardsdatascience.com/vision-based-rep-counting-in-the-wild-cb9a4d1bdb7e

[3] Recognition and Rep Counting for Complex Exercises  with Deep Learning, 2019. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6387025/pdf/sensors-19-00714.pdf

[4] AI Fitness coach at home using Image Recognition, 2022. https://assets.researchsquare.com/files/rs-2047283/v1_covered.pdf?c=1664462832

[5] YOLO v8 review and experiment, 2023. https://medium.com/mlearning-ai/yolo-v8-the-real-state-of-the-art-eda6c86a1b90

[6] Class Agnostic Video Rep Counting In The Wild, 2020. https://arxiv.org/pdf/2006.15418.pdf

