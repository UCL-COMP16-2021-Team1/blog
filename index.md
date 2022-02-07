# 3D Tennis Analysis with CV/AI

## Development

### Week 8
Date: 07/02/2022

We've continued working on each of our individual experiments and have started merginig our work together in order to check the compatibility between different sections. Notably, we've created a pipeline between the poses extracted by [MediaPipe](https://google.github.io/mediapipe/) and shot recognition as well as fixed a few calibration errors, which has resulted in 90.6% accuracy with the implemented Convolutional Neural Network model.

Furthermore, in order to make sure our product is in fact targeted towards the user, we conducted interviews with a group of pseudo-users consisting of one fan, one tennis player and one coach, which provided us with more details as well as more goals to complete our final project.

We've also begun working on reconstructing shots with 3D skeletons using the [Three.js](https://threejs.org) JavaScript library and are currently figuring out how to include court boundaries and ball coordinates. We're presently aiming at completing the second ST-GCN model as well as analyzing the pseudo-user data in order to better configure our final product.

### Week 5
Date: 17/01/2022

Over the last 2 weeks of the project we’ve all individually worked on our specified experiments in which we did research for. Some results we obtained was obtaining a 85-90% accuracy on one of our models based on Convolutional Neural Networks and successfully extracting the 3D skeleton poses from a basic video feed of a single tennis player.

Subsequently we prepared and scripted for the elevator pitch where we presented our project and its selling points as well as the current progress we’ve had, presenting the pitch to our tutors as well as our clients on the 21st of January.

From here, we plan to start creating the pipeline between the extracted 3D skeleton avatars from Media Pipe and the CNN model, as well as starting to work on the 3D reconstruction where we visualise the 3D data we have. We also plan to complete a second model based on Spatial Temporal Graph Convolutional Networks and conduct a pseudo user interview to gain more information on what users would prefer in a UI so we can begin creating that in the following weeks.

### Week 3
Date: 13/12/2021

Based on our research and requirements analysis, we have refined our requirements to make them more coherent and now focus on 3D tennis shot analysis. This will involve extracting 3D skeletal animations of tennis shots from video and training a model to classify them. Our client and Professor Dean have happily agreed to these changes.

We have researched into extracting 3D poses from video using [MediaPipe](https://google.github.io/mediapipe/) and classifying 3D tennis shot animations using methods such as [CNN models](https://arxiv.org/abs/1704.07595) and [graph convolutional network models](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7662764/). We have found an [open-access dataset](http://thetis.image.ece.ntua.gr/) of 3D tennis shot animations (of both amateurs and experts) that we can use to train the models.

We will now be starting our experiments to try out these methods.

### Week 1
Date: 29/11/2021

On Monday, we provided a list of suggested requirements to our client and Professor Dean:
1. Play in an interactive 3D environment against an AI simulating professional players extracted from tennis match videos.
2. Train a model on tennis game videos and offer live suggestions based on the feed. This acts as a tennis trainer by helping young learners observe techniques and see variations.
3. Determine which sections of a video of a tennis match can be considered a highlight and put them into a highlight reel.
4. Contextually score specific aspects of a tennis match, e.g. positioning, shots, ball trajectory etc. Use for training and entertainment/reference. 

 We agreed upon two main areas of requirements, video classifiers for tennis matches and 3D avatar extraction of the tennis players and proceeded with research of the specifics of each domain. Each team member was allocated one part of the research:
 - Morgane would look into general high-level software architecture and project management;
 - Prithvi would be researching the video classifiers;
 - Jin would investigate the extraction of 3D avatars from video feed.
