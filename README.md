# RSNA Spotlight 2021

### From Theory to Practice: Live Demonstration 

This is a guide for the session "From Theory to Practice: Live Demonstration" in the *RSNA Spotlight Course 2021 AI Implementation: Building Expertise and Influence*.

### Objective:

By the end of this activity, you will be able to:

* Understand the overall process to train a deep learning model
* Learn basic concepts on how to assess model generalizability and performance

### Instructions:

#### Step 1: Download the [file for Experiment 1 here](https://github.com/kitamura-felipe/RSNASpotlight2021/blob/main/experiments/experiment1.tm?raw=true) and save it somewhere you can find it later.

#### Step 2: Right click on the [teachable machine link here](https://teachablemachine.withgoogle.com/train/image) and choose "Open in a new tab" (or hold CTRL key + left mouse click)

You should see this website:

![Screenshot](https://github.com/kitamura-felipe/RSNASpotlight2021/blob/main/images/image04.png)

#### Step 3: Click on the left upper corner to open the menu and then click on "Open project from file" as below:

![Screenshot](https://github.com/kitamura-felipe/RSNASpotlight2021/blob/main/images/image05.png)

#### Step 4: Upload the file from Experiment 1 (Step 1) and wait for it to load.

You should see multiple head CT images loaded onto the platform organized by presence or absence of hemorrhage:

![Screenshot](https://github.com/kitamura-felipe/RSNASpotlight2021/blob/main/images/image06.png)

#### Step 5: Click on train and wait for it to finish. It may take a while for the training to start.

After training, experiment 1 should look like this:

![Screenshot](https://github.com/kitamura-felipe/RSNASpotlight2021/blob/main/images/experiment1.png)

Notice that the accuracy is not as good as one may expect from a machine learning model. This is due to the limited number of cases in this experiment (30 normal + 30 hemorrhage)


#### Step 6: Repeat steps 3 to 5, but now load the [file for Experiment 2 here](https://github.com/kitamura-felipe/RSNASpotlight2021/blob/main/experiments/experiment2.tm?raw=true)

After training, experiment 2 should look like this:

![Screenshot](https://github.com/kitamura-felipe/RSNASpotlight2021/blob/main/images/experiment2.png)

Notice that the accuracy seems to have improved significantly. However, a closer look at the confusion matrix shows that most of the positive cases have been misclassified as negative. This is due to the heavy class imbalance thas was simulated in this experiment (1000 normal + 30 hemorrhage).

#### Step 7: Repeat steps 3 to 5, but now load the [file for Experiment 3 here](https://github.com/kitamura-felipe/RSNASpotlight2021/blob/main/experiments/experiment3b.tm?raw=true)

After training, experiment 3 should look like this:

![Screenshot](https://github.com/kitamura-felipe/RSNASpotlight2021/blob/main/images/experiment3b.png)

Notice that the accuracy is lower than in the last experiment. However, a closer look at the confusion matrix shows that it is indeed correctly classifying most of the positive cases, although still nor perfect. In this experiment our dataset was balanced (1000 normal + 1000 hemorrhage).


#### Step 8: Repeat steps 3 to 5, but now load the [file for Experiment 4 here](https://github.com/kitamura-felipe/RSNASpotlight2021/blob/main/experiments/experiment4.tm?raw=true)

After training, experiment 4 should look like this:

![Screenshot](https://github.com/kitamura-felipe/RSNASpotlight2021/blob/main/images/experiment4.png)

In this experiment we are training a multiclass model, which means the algorithm will predict only 1 of 5 classes (normal, intraventricular, subdural, intraparenchymal, subdural). Because of the limited number of images in each class (79) to keep it balanced, the accuracy is not impressive.

#### Step 9: Repeat steps 3 to 5, but now load the [file for Experiment 5 here](https://github.com/kitamura-felipe/RSNASpotlight2021/blob/main/experiments/experiment5.tm?raw=true)

After training, experiment 5 should look like this:

![Screenshot](https://github.com/kitamura-felipe/RSNASpotlight2021/blob/main/images/experiment5.png)

In this experiment we are also training a multiclass model, which means the algorithm will predict only 1 of 5 classes (normal, intraventricular, subdural, intraparenchymal, subdural). But now we have not limited the number of images per class, which leads to a huge class imbalance. Althoug accuracy has risen, the confusion matrix shows the high accuracy is biased because of the overwhelming number of normal cases. The model is predicting almost everything as normal.


