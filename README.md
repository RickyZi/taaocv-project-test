# Project 3 of Trends and Applications of Computer Vision course of UniTN

In this project we wants to asses various technique to detect a deepfake and to try them on few different deefake generators (FSGAN, DeepFaceLive, GHOST).

## Students

- Giovanni Lorenzini
- Diego Planchenstainer
- Riccardo Sassi
- Riccardo Ziglio

## Challenges

The human suspected to be a deepfake is required to perform some specific actions, such as:
- **Head rotation**: move the head with strong rotation as 90° horizontally or face up towards the ceiling. This aims at assess whether the model can generate unseen views.
- **Tongue out**: stick a portion of the tongue out. If the segmentation network is capable of detecting the tongue, it will be ignored and thus displayed, otherwise the face swapper will delete it.
- **Hand on face**: hover hand and finger in front of the face, either occluding it partially or completly. The objective is to evaluate the performance of the segmentation network.
- **Close up**: move the face close to the camera. This step wants to assess whether the face detector is capable of detecting only part of face and the resolution of the face.
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

|                         |  FSGAN  |  GHOST  | DeepFaceLive |
| :---------------------- | :-----: | :-----: | :----------: |
| Head rotation           |   0.5   |   2.8   |   **4.8**    |
| Tongue out              | **4.2** |    2    |     0.5      |
| Hand on face            |   1.8   |   2.5   |   **5.3**    |
| Close up                |    5    |    4    |   **7.8**    |
| Standup                 |    0    | **7.8** |      5       |
| Poke cheek              |    0    | **5.3** |      5       |
| Expression              |    7    |   7.3   |   **8.5**    |
| Speaking                |   6.5   |    6    |    **9**     |
| **Average**             | **3.1** | **4.7** |   **5.7**    |
| **Realism**             | **4.8** | **7.5** |    **9**     |
| **Lighting conditions** |  **2**  |  **6**  |    **9**     |
