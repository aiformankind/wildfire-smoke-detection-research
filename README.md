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
 
 4. For 2020-05-21 fire captured by HPWREN camera VEGMGMT ml-w-mobo-c, our detector detected the smoke *16 minutes* after fire ignition.

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
   
As an effort to improve our wildfire smoke detector, we run our model against HPWREN camera images a couple times a day to evaluate our system and collect false positive examples to retrain our model.

We continue to organize a series of Lets Stop Wildfires Hackathons. You can learn more about the hackathons below. 
  
  [2020 Lets Stop Wildfires Hackathon 2.0](https://aiformankind.github.io/lets-stop-wildfires-hackathon-2.0/)
  
  [2019 Lets Stop Wildfires Hackathon](https://aiformankind.github.io/lets-stop-wildfires-hackathon/)

## What We are Working on

1. Improve model capability to differentiate between cloud/fog and smoke
2. Build end to end feedback loop

## System under Evaluation
We setup the system to run against HPWREN cameras every 15 minutes for evaluation/testing purpose. Each site handles ~ 60 cameras so that we can finish evaluating all the cameras within 15 mins. 

[Site 1](http://wildfire-smoke-detector.westus2.cloudapp.azure.com:5000)
[Site 2](http://wildfire-smoke-detector-2.westus2.cloudapp.azure.com:5000)
[Site 3](http://wildfire-smoke-detector-3.westus2.cloudapp.azure.com:5000)
[Site 4](http://wildfire-smoke-detector-4.westus2.cloudapp.azure.com:5000)

## Donate to Support Us
[Donate](https://donorbox.org/support-the-evaluation-and-deployment-of-wildfire-smoke-detector) to support our efforts. Your donation is tax deductible. 

