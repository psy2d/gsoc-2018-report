## Google Summer of Code 2018 - Final Report

# Emotion Recognition Component for Learnbot

Learnbot is an educational robot used to develop computational thinking in kids of age 10 and above. As a participant of Google Summer of Code, I worked on building an emotion recognition component based on facial expressions for learnbot. During the summer I reached most of the proposed goals, and created a fairly accurate and stable emotion recognition component.

## Application Period

I was extremely interested in this particular project as computer vision and robotics have always fascinated me. I contacted the mentors and discussed my ideas regarding the project. My interaction was mainly with [Pillar Bachiller](https://github.com/pilarbachiller), who guided me throughout the entire journey. She cleared all my doubts and gave me feedback on my ideas during this period.

The 3 important things that I did during the application period, that led to my selection were:
1. Good communication with the mentor, which helped me understand the objectives and scope of the project.
2. I created a small version of the original project. This version was able to recognize 3 basic emotions: Happy, Sad, Neutral.
3. I wrote a detailed project proposal, keeping in mind the suggestions provided by my mentor.

## Community Bonding Period

My excitement knew no bounds when the results were out and my proposal had been accepted for GSoC. The first thing I did was sending an email to my mentor and thanking her for the opportunity.

We discussed the action plan, mode of communication and frequency of our communication, right at the start of the community bonding period. We also decided a way to keep track of my work during GSoC: by writing blog posts.

During this period, I made myself familiar with the code base and learnt how to create a basic RoboComp component. I created an initial version of the component which recognizes 3 emotion, by integrating the code of my prototype into the newly created RoboComp component.

## Coding Period

Initially, I had planned to test out 2 models:
1. CNN - DSIFT model
2. Cross-channel CNN for analysing mutimodal data.

Later on, I changed the plan and decided to focus on facial expression data only, instead of multimodal data. So, I implemented 3 different types of models:
1. CNN
2. CNN-DSIFT
3. CNN + facial landmarks detection

The CNN model turned out to be the best, with least computational costs among the three.

I trained these models on multiple different facial expression data sets and compared the results. The data sets which I experimented with were: [FER2013](https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge/data), [CK+](http://www.pitt.edu/~emotion/ck-spread.htm), [JAFFE](http://www.kasrl.org/jaffe.html), [KDEF](http://www.emotionlab.se/kdef/) and [AffectNet](http://mohammadmahoor.com/affectnet/). The model trained using AffectNet was included in the final component.

Aligning faces using facial landmarks and adaptive histogram equalization was added to the component, in order to make recognition more stable and robust.

**Features of the final emotion recognition component:**

1. Ability to recognize 5 emotion types: happiness, sadness, anger, surprise, neutral.
2. Vertical face alignment using facial landmarks.
3. Adaptive histogram equalization to handle uneven illumination conditions.
4. Deep learning based face detector and a haar-cascade based face detector.
5. Ability to recognize emotions for multiple faces in a single frame.

## Future Work

1. Extending the project to recognize more number of emotions.
2. Using the detected emotions to provide feedback in form of dialogue or by showing an emotion on learnbot's display.
3. Analysing multimodal data for emotion recognition.

## Posts

For a more detailed view on my work during GSoC, you can have a look at my blog posts:
1. [Hello, World!](https://robocomp.github.io/web/gsoc/2018/sayali_deshpande/post1)
2. [Happy? Sad? Neutral?](https://robocomp.github.io/web/gsoc/2018/sayali_deshpande/post2)
3. [The CNN-DSIFT Model](https://robocomp.github.io/web/gsoc/2018/sayali_deshpande/post3)
4. [Experimenting with Facial Landmarks](https://robocomp.github.io/web/gsoc/2018/sayali_deshpande/post4)
5. [~~Problems~~ Solved](https://robocomp.github.io/web/gsoc/2018/sayali_deshpande/post5)

## Source Code

Commits: [link](https://github.com/robocomp/robocomp-robolab/commits/master?author=psy2d)

Final Emotion Recogntion Component: [link](https://github.com/robocomp/robocomp-robolab/tree/master/components/emotionrecognition2)

Emotion Recognition Client Component: [link](https://github.com/robocomp/robocomp-robolab/tree/master/components/emotionrecognitionclient)

RoboComp-RoboLab: [link](https://github.com/robocomp/robocomp-robolab)


Finally, I would like to thank Google and RoboComp for giving me this wonderful opportunity. I am grateful to my mentor for helping me out at every hurdle and providing me valuable inputs at every step.

## References

1. [https://arxiv.org/pdf/1608.02833.pdf](https://arxiv.org/pdf/1608.02833.pdf)
2. [https://arxiv.org/pdf/1708.03985.pdf](https://arxiv.org/pdf/1708.03985.pdf)

