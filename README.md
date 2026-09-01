# hey dragon model Arduino

# this repo contains one hands on project for recognising the wake word hey dragon #
1. the outline of this project is to detect the wake word in our case it is hey dragon and react to it
2. requirements
   - Arduino UNO Q
   - Edge impulse account to train the model
   - Arduino app lab and VS code
3. create a account in edge impulse website free account
4. this impulse will be used to
   - collect an label audio data samples, extract features from video samples
   - split data and create edge impulses
   - train and evaluate model
   - build a simple app lab project
5. after that that created model can be run on Arduino UNO for real time interference
6. data collection
   - can be split into 2 types
   - wake word collection: for this project you need to collect 3 mins of voice with the help of impulse.
     go to data acquisition and start collecting data of 3 mins of voice 1 min each recording. remember to name it as hey_dragon(label) and set set as training
   - noise collection: for noise you can record anything than wake word tapping screaming casual wooshes, thuds etc, background noise.
     remember to name it as hey_dragon(noise) and set set as training
7. after collecting you will have 6 mins of recording with 3 mins hey dragon and 3 mins noise
8. now split the data as train and test in the impulse website itself
9. start splitting sample with help of 3 dots next to recording set the timeline as 1000ms and split and generate split for all 6 recordings and then you will have lot of data to start training
10. go to impulse design -> create impulse set processing block as MFCC audio and learning block as classification check output feature has 2 labels hey_dragon and noise. save impulse
11. new tabs will come below create impulse as MFCC and classifier 1st click on MFCC and go down and click on save parameters, go to classifier and click save and train.
12. after training completes you can see related graphs like ROC curve, confusion matrix and accuracy etc.
13. after training go for testing and test your model if it is above 90% also then the model will work mine came out as 98%
14. go below the tabs and select deployment and select Arduino UNO Q export the model.
15. to deploy you need to have both Arduino app lab + and vs code
16. in app lab + you will select a already present model and edit the wake word as hey_dragon and run then test the wake word in the board the heart animation wil play.

this project was a part of course I got free from QUALCOMM 
link: https://academy.qualcomm.com/course-catalog/AI-Upskilling-Certificate-Development-from-Model-to-App
this is a free course in this we have 3 projects in those this is one of the project

author
@tunder00
