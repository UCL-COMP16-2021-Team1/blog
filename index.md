# 3D Tennis Analysis with CV/AI

## Development

### Week 14
Date: 21/03/2022

Since the last update, we've finished refining our shot recognition model and have now also completed our front-end design, utilising Bootstrap to create a simple and clean UI. We are also working on outputting .BVH files from the players' data so that it can be used for things like attaching models etc. 

Furthermore, we have created our scripts and slides for the upcoming final presentation where we will present our project to our client and assessors. We will soon film and record our presentation video to be ready for the 23rd deadline.

As part of our final deliverables, we have also begun working on creating an executable for our program so that it would be much easier for non-technical users to use our program.

### Week 12
Date: 07/03/2022

Over the last 2 weeks, we began creating the backend API using Flask as well as the front-end with Vue.js to connect the analysis pipeline to the front-end web application. Furthermore, since the last blog update we've narrowed the scope in the type of shots we recognise as we realised having so many different shots made recognising the various shots more difficult and in most scenarios, those shot types wouldn't be sought for by general players. From recognising 12 shot types we now have narrowed it to 4. Due to this, we've worked on further refining the model to work more generically for both front-end and back-facing cameras, compared to just being a tennis trainer application as we said in the last blog update. It would now be a general tennis analytics application that can be used for various purposes.

Furthermore, when creating our backend API, we made sure to keep it flexible and extendable so that other developers would easily be able to make use of the system we've created and the more in-depth analysis it has to offer. This would especially apply to our project partners as they would want to use it in a more professional scenario.

Additionally, we've begun creating our report website and filling it in with the information we can at the moment, such as the Home and Requirement page.

### Week 10
Date: 21/02/2022

Last week, we attempted to configure our current pipeline to be able to work with real live tennis matches. One issue we ran into at the beginning of this, was to do with not being able to properly extract the 2 players in the video feed due to limitations of mediapipe and how there is a certain distance limit for mediapipe to work properly. Another issue was to do with having many other people in the frame. 
We attempted to solve this by first running box-tracking on the video to track the players and then crop into those boxes to perform the skeletal pose extraction. However, there were more issues that arose with the shot recognition not being able to perform properly due to things such as bad camera angles since the player sometimes has their back towards the camera and their arms aren???t properly extracted.

Moreover, we successfully got the 3D reconstruction working as well as getting the webapp to work with this, Three.js. We aim to also get this to work with .gltf files in order to obtain 3D reconstructions of the video feeds that we analyse.

While working on getting the pipeline analysis working and the 3D reconstruction, we started analysing the information we had acquired from our pseudo interviews, to use in creating our personas and use case diagrams. From the information and preferences we gathered, we created wireframes to represent how the UI would be used. 

In the following week, we took some time to discuss the doability of being able to analyse tennis matches and came to realise that given the resources we had, it would be difficult to accomplish this. From there we collectively decided to change the scope of our project slighlty and aim to create a Tennis trainer app that instead utilises the front camera to record a players shots and movement. The plan would be to keep almost of the analytics and features the same with the shot recognition and 3D reconstruction but instead of it working on a tennis match, it would be just one player infront of the camera taking practice shots which will be analysed. This would better suit the data set which we used to train our model on as well.

We are now currently aiming to redesign our wireframes to suit the idea of a Tennis training app as well as get a basic prototype of our program running with a simple front-end to display how the program would function.

### Week 8
Date: 07/02/2022

We've continued working on each of our individual experiments and have started merginig our work together in order to check the compatibility between different sections. Notably, we've created a pipeline between the poses extracted by [MediaPipe](https://google.github.io/mediapipe/) and shot recognition as well as fixed a few calibration errors, which has resulted in 90.6% accuracy with the implemented Convolutional Neural Network model.

Furthermore, in order to make sure our product is in fact targeted towards the user, we conducted interviews with a group of pseudo-users consisting of one fan, one tennis player and one coach, which provided us with more details as well as more goals to complete our final project.

We've also begun working on reconstructing shots with 3D skeletons using the [Three.js](https://threejs.org) JavaScript library and are currently figuring out how to include court boundaries and ball coordinates. We're presently aiming at completing the second ST-GCN model as well as analyzing the pseudo-user data in order to better configure our final product.

### Week 5
Date: 17/01/2022

Over the last 2 weeks of the project we???ve all individually worked on our specified experiments in which we did research for. Some results we obtained was obtaining a 85-90% accuracy on one of our models based on Convolutional Neural Networks and successfully extracting the 3D skeleton poses from a basic video feed of a single tennis player.

Subsequently we prepared and scripted for the elevator pitch where we presented our project and its selling points as well as the current progress we???ve had, presenting the pitch to our tutors as well as our clients on the 21st of January.

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
