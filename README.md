# Project 3 of Trends and Applications of Computer Vision course of UniTN

In this project we wants to asses various technique to detect a deepfake and to try them on few different deefake generators (FSGAN, DeepFaceLive, GHOST).

## Students

- Giovanni Lorenzini
- Diego Planchenstainer
- Riccardo Sassi
- Riccardo Ziglio

## Challenges

The human suspected to be a deepfake is required to perform some specific actions, such as:
- **Head rotation**: move the head with strong rotation as 90° horizontally or face up towards the celing. This aims at assess whether the model can generate unseen views.
- **Tongue out**: stick a portion of the tongue out. If the segmentation network is capable of detecting the tongue, it will be ignored and thus displayed, otherwise the face swapper will delete it.
- **Hand on face**: hover hand and finger in front of the face, either occluding it partially or completly. The objective is to evaluate the performance of the segmentation network.
- **Standup**: stand up in order to hide the face from the camera. This step wants to assess whether the face detector is capable of re-detecting a face that was hidden/gone out of the scene.
- **Poke cheek**: poke cheek to induce morphological changes in the face. These changes should be sensed by the landmark detector and face allignment networks.
- **Expression**: perform different expression. These changes should be sensed by the landmark detector and face allignment networks.
- **Speaking**: speak to generate lips movement. These changes should be sensed by the landmark detector and face allignment networks.

## Dataset

We used some videos of ourself performing the above actions and videos downloaded from the internet with the celebrity that we want to impersonate.

## Deepfake Generators

We used the following deepfake generators:
- [FSGAN](https://github.com/YuvalNirkin/fsgan):
    - uses a small video for source face;
- [DeepFaceLive](https://github.com/iperov/DeepFaceLive):
    - use pretrained models from DeepFaceLab;
    - in real time;
- [GHOST](https://github.com/ai-forever/ghost):
    - uses a single image for source face.
    
## Results

|               | FSGAN | DeepFaceLive | GHOST |
| :------------ | :---: | :----------: | :---: |
| Head rotation |       |              |       |
| Tongue out    |       |              |       |
| Hand on face  |       |              |       |
| Standup       |       |              |       |
| Poke cheek    |       |              |       |
| Expression    |       |              |       |
| Speaking      |       |              |       |
| **Realism**   |       |              |       |
| **Mean**      |       |              |       |
