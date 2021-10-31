# Human_Action_Recognition
An android app to predict human action (11 categories) trained on CNN network and used tranfer learning technique with vgg16 wieghts the categories are :

1)breakdancing
2)calligraphy
3)celebrating
4)claypotterymaking
5)climbingarope
6)cookingoncampfire
7)eatingicecream
8)golfdriving
9)pushup
10)raisingeyebrows
11)ridingscooter

Feel free to use the training code and if you want the model just DM me 

Here's a demo video 

https://user-images.githubusercontent.com/88105870/139510827-9bffc011-439c-4ac6-8054-1d8e2149e226.mp4

Here is the link of the apk on the drive 
https://drive.google.com/drive/folders/1O8bVE3etUyGzU6uFv1EZQcw69DhdZ5Il?usp=sharing

Report

trials:-

1)	first i try the regular CNN model to train our data set with 20 epochs and get nearly 97% accuracy .

2)	then i try to double the data-set number by using data augmentation but didn't really effect that much on the accuracy(97.8%) ,we conclude that data augmentation actually increase the accuracy a little bit ,but it's also ram consuming , and the most two affective operation in data augmentation is (zooming and cropping ) .

3)	also i used early stopping technique to stop the model when best validation error  is reached.

4)	And also I plot both training and validation loss and training and validation accuracy to visually  help us and to see how the training process goes and also see when the model falls into over fitting , from  the plot we conclude that after epoch 25 the model start to over fit the data and the validation accuracy is getting worse.  
 


5)	and I also tried to change the optimizer and the loss function but I found that Adam optimizer and categorical cross entropy loss function works well for this problem.
 
6)	and I found that the best splitting  percentage of the training data is (80% training 20% validate).

7)	I tried to use transfer learning using vgg16 and build a simple model and tuning it with the vgg16 weights and I reach a 99% accuracy with that.

8)	then I convert the model into tflite model so it can run on android application(using android studio) and then I done with the deployment part as I took one frame every second and predict it then calculate the accuracy of the prediction of the video.

link of the project in google colab:-
https://colab.research.google.com/drive/18hgQJ--e8KKShWldgdKtw7DTk_J9liPj  (the google colab link of the project).


Name /Mostafa Ebrahim mohamed Ebrahiem fathallah


