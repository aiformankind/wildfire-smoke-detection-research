# Wildfire Smoke Detection Research

In this project, AI For Mankind want to investigate and promote the use of AI Deep Learning in early wildfire smoke detection. We want to raise awareness about the wildfire crisis and rally more people/AI experts to work on this problem. 

We continue to promote the curation of open datasets to speed up research and development. We collaborate with [HPWREN](http://hpwren.ucsd.edu/) in promoting the collaboration of our volunteers from private tech with public sector in solving this wildfire crisis.

Reach out to us if you would like to [collaborate](ai.for.mankind@gmail.com) with us.

AI For Mankind had created bounding box annotated wildfire smoke images in 2019 and built a wildfire smoke detector using the annotated images. It has shown promising results running against wildfire images captured by HPWREN in 2020. See below.

 1. For 2020-02-05 fire captured by HPWREN camera hp-w-mobo-c, our detector detected the smoke *13 minutes* after fire ignition.

    <br/>
    <a href="https://youtu.be/CcbXdcMEQvs"><img src="images/smoke_detector_in_action_13mins_detected.png" width="500" ></a>
    <br clear="right"/>

 2. For 2020-03-06 fire captured by HPWREN camera mlo-n-mobo-c, our detector detected the smoke *3 minutes* after fire ignition. See video below.

    <br/>
    <a href="https://youtu.be/X_QvjA1-Nb4"><img src="images/smoke_detector_in_action_3mins_detected.png" width="500" ></a>

    <br clear="right"/>

    <br/>
    
 3. For 2019-10-06 fire captured by HPWREN camera pi-s-mobo-c, our detector detected the smoke *3 minutes* after fire ignition. See video below.

    <br/>
    <a href="https://youtu.be/e9T_8coM20M"><img src="images/smoke_detector_in_action_3mins_detected_20191006.png" width="500" ></a>

    <br clear="right"/>

    <br/>
    
 4. For 2019-10-06 fire captured by HPWREN camera lp-s-mobo-c, our detector detected the smoke *10 minutes* after fire ignition. See video below.

    <br/>
    <a href="https://youtu.be/XVvZVnxHv4A"><img src="images/smoke_detector_in_action_10mins_detected_20191006.png" width="500"></a>

    <br clear="right"/>

    <br/>   
 
 5. For 2020-05-21 fire captured by HPWREN camera VEGMGMT ml-w-mobo-c, our detector detected the smoke *16 minutes* after fire ignition.

    <br/>

    <img src="images/20200521_VEGMGMT_ml-w-mobo-c_1590081617_+00960_smoke_detected.png" alt="Wildfire Smoke Detector in Action" width="450"/>
    <br clear="right"/>
    
We ran AI For Mankind's wildfire smoke detector aka "The Super Duper" against past HPWREN images of several fires, here are the promising results obtained.

   - [20191006: Detected smoke ~6 mins after fire ignition (HPWREN ml w mobo c)](https://youtu.be/wt1sQyRjoCI)
   - [20191006: Detected smoke ~7 mins after fire ignition (HPWREN lp n mobo c)](https://youtu.be/dViR_XGQ8Oo)
   - [20191006: Detected smoke ~10 mins after fire ignition (HPWREN lp s mobo c)](https://youtu.be/XVvZVnxHv4A)
   - [20191006: Detected smoke ~3 mins after fire ignition (HPWREN pi s mobo c)](https://youtu.be/e9T_8coM20M)
   - [20191007: Detected smoke ~10 mins after fire ignition (HPWREN sm s mobo c)](https://youtu.be/LqAxrY-Xa4w)
   - [20200206: Detected smoke ~4 mins after fire ignition (HPWREN ml s mobo c)](https://youtu.be/Y3tal1-nk1Y)
   - [20200306: Detected smoke ~3 mins after fire ignition (HPWREN mlo n mobo c)](https://youtu.be/X_QvjA1-Nb4)
   - [20200205: Detected smoke ~13 mins after fire ignition (HPWREN hp w mobo c)](https://youtu.be/CcbXdcMEQvs)
   - [20200615: Detected smoke ~4 mins after fire ignition (HPWREN rm e mobo c)](https://youtu.be/uPSkxGjUqRk)
   
**[See all our wildfire smoke detection results on youtube playlist here.](https://www.youtube.com/playlist?list=PLB-XesK9mcaCCvSbogU9SFBlp1LEAjgT2)** 

As an effort to improve our wildfire smoke detector, we run our model against HPWREN camera images a couple times a day to evaluate our system and collect false positive examples to retrain our model.

We continue to organize a series of Lets Stop Wildfires Hackathons. You can learn more about the hackathons below. 
  
  [2020 Lets Stop Wildfires Hackathon 2.0](https://aiformankind.github.io/lets-stop-wildfires-hackathon-2.0/)
  
  [2019 Lets Stop Wildfires Hackathon](https://aiformankind.github.io/lets-stop-wildfires-hackathon/)
  
## Example Smokes
The following videos show the challenges in detecting wildfire smokes.
1. [Far away smoke](https://youtu.be/D22NCqamu_8)

## What We are Working on

1. Improve model capability to differentiate between cloud/fog and smoke
2. Build end to end feedback loop

## System under Evaluation
We setup the system to run against HPWREN cameras every ~10 minutes for evaluation/testing purpose. Stay tuned for updates. 

## Model Performance
We had developed 3 models: SuperDuper-v1, SuperDuper-v2, and SuperDuper-edge. One of them, SuperDuper-edge is optimized for edge device. The table shows the performance of our models.


| Name            | AveragePrecison 0.5IOU/smoke |
|-----------------|-----------------|
| SuperDuper-v1   | 0.7506           |
| SuperDuper-v2   | 0.8669           |
| SuperDuper-edge | 0.6822           |


## False Positive Rate
We tested our model against different time periods eg. during sunrise, sunset, or foggy condition and shared our false positive rates below. We will continue to curate, test, and share the results and datasets.

| False Positive Study |               |              |                        |                     |                                                                           |
|----------------------|---------------|--------------|------------------------|---------------------|---------------------------------------------------------------------------|
|                      | Model         | Total Images | Num of False Positives | False Positive Rate | Link to Dataset                                                           |
| Sunrise              | SuperDuper-v1 | 181          | 2                      | 0.011       | https://www.dropbox.com/sh/71jdkv7tdtmmif8/AACdd51AH4BNX84bJSrGWrssa?dl=0 |
| Fog                  | SuperDuper-v1 | 181          | 72                     | 0.398        | https://www.dropbox.com/sh/iw40v0yrkkimhha/AAANC4cxJR90cp8cfXF5kYHaa?dl=0 |

On average, false positive rate ~0.0860


## GET STARTED 
We provided the following quick start repo and Colab Notebooks to get you started

#### Object Detection
You can checkout our wildfire smoke detector repo below. It comes with a docker image and annotated [HPWREN](http://hpwren.ucsd.edu/) images to get you started.

1. [Wildfire Smoke Detector Quickstart Repo](https://github.com/aiformankind/wildfire-smoke-detection-camera). Follow the steps to build a simple wildfire smoke detector.

#### Image Classification
You can also checkout the following notebooks for smoke classification provided by us for the last [hackathon](https://aiformankind.org/lets-stop-wildfires-hackathon/). These are built only for classification and not for object detection.

1. [Smoke Classifier using Entire Image](https://github.com/aiformankind/lets-stop-wildfires-hackathon/blob/master/Challenge_1A_WildfireSmokeImageClassifierForDemo.ipynb)

2. [Smoke Classifier using Gridded Image](https://github.com/aiformankind/lets-stop-wildfires-hackathon/blob/master/Challenge_1B_WildfireSmokeImageClassifierForDemo.ipynb)

## Wildfire Resources
1. [FUEGO Wildfire Detection Slides by Kinshuk Govil](https://tinyurl.com/rbrn4oq)
2. [A Review on Forest Fire Detection Techniques](https://journals.sagepub.com/doi/pdf/10.1155/2014/597368)
3. [Wildland Fire Assessment System](http://www.wfas.net/)
4. [The United States Fourth National Climate Assessment Volume II](https://nca2018.globalchange.gov/downloads/NCA4_Report-in-Brief.pdf)
5. [How Wildfire Works](https://science.howstuffworks.com/nature/natural-disasters/wildfire.htm/printable)
6. [Fighting Wildfires](https://mentalfloss.com/article/57094/10-strategies-fighting-wildfires)
7. [Wildland Fire: What is Hazard Fuel Reduction?](https://www.nps.gov/articles/what-is-hazard-fuel-reduction.htm)
8. [Fire Danger Rating](https://www.wfas.net/index.php/fire-danger-rating-fire-potential--danger-32)


## Tensorflow Resources
1. [Tensorflow Quickstart](https://www.tensorflow.org/tutorials/quickstart/beginner)
2. [Tensorflow Tutorials](https://www.tensorflow.org/tutorials)
3. [Install Tensorflow in PyCharm](https://youtu.be/vEXCMOuPB3c)
4. [What is transfer learning? Exploring the popular deep learning approach](https://builtin.com/data-science/transfer-learning) 
5. [Transfer learning in TensorFlow 2 tutorial](https://adventuresinmachinelearning.com/transfer-learning-tensorflow-2/)
6. [Deep learning unbalanced training data](https://towardsdatascience.com/deep-learning-unbalanced-training-data-solve-it-like-this-6c528e9efea6)

## Papers
1. [Do Better ImageNet Models Transfer Better?](https://www.zpascal.net/cvpr2019/Kornblith_Do_Better_ImageNet_Models_Transfer_Better_CVPR_2019_paper.pdf)
2. [SpotTune: Transfer Learning through Adaptive Fine-tuning](http://openaccess.thecvf.com/content_CVPR_2019/papers/Guo_SpotTune_Transfer_Learning_Through_Adaptive_Fine-Tuning_CVPR_2019_paper.pdf)
3. [Taskonomy: Disentangling Task Transfer Learning](http://openaccess.thecvf.com/content_cvpr_2018/papers/Zamir_Taskonomy_Disentangling_Task_CVPR_2018_paper.pdf)


## Donate to Support Us
[Donate](https://donorbox.org/support-the-evaluation-and-deployment-of-wildfire-smoke-detector) to support our efforts. Your donation is tax deductible. 

