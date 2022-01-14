# 3D Tennis Analysis with CV/AI

## Development
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
