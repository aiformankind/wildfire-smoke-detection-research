# Wildfire Smoke Detection Research

In this project, AI For Mankind want to investigate and promote the use of AI Deep Learning in early wildfire smoke detection. We want to raise awareness about the wildfire crisis and rally more people/AI experts to work on this problem. 

We continue to promote the curation of open datasets to speed up research and development. We collaborate with [HPWREN](http://hpwren.ucsd.edu/) in promoting the collaboration of our volunteers from private tech with public sector in solving this wildfire crisis.

  AI For Mankind had annotated 744 wildfire smoke HPWREN images in 2019 and built a wildfire smoke detector using the annotated images. It has shown promising results running against wildfire images captured by HPWREN in 2020. See below.

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
We setup the system to run against HPWREN cameras every 30 minutes for evaluation/testing purpose. Each site handles ~ 60 cameras so that we can finish evaluating all the cameras within 30 mins. In the next few weeks, we will reduce the delay to ~15 mins. 

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

## Donate to Support Us
[Donate](https://donorbox.org/support-the-evaluation-and-deployment-of-wildfire-smoke-detector) to support our efforts. Your donation is tax deductible. 

