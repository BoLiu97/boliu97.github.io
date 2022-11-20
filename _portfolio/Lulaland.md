---
title: "Lullaland"
excerpt: "Virtual Reality , Fabrication, Circuit Design, Healthcare"
header: 
    image: Lula_front.png
    teaser: Lula_front.png
collection: portfolio

---

**Global Innovation Exchange, University of Washington**

People: Bo Liu(first author), Steve Wang, Yuqing Zhang, John Raiti

**Updates**: This research is preparing to submit to CHI as Late-Breaking Work

## My Work: 
Hardware: Circuit Design, Prototype Iteration

Software: VR Development Full Stack

## Lullaland
People associate the hospital with things they deem stressful and scary. **When they are in healthcare settings, patients have emotional reactions like anxiety, aggression, and anger mainly because they lack control of their environment.** These emotional responses can increase not only pain sensitivity but also delay important medical treatment, lower efficiency, and also undermine patients’ willingness to continue their healthcare treatment.

People associate the hospital with things they deem stressful and scary. When they are in healthcare settings, patients have emotional reactions like anxiety, aggression, and anger mainly because they lack control of their environment. These emotional responses can increase not only pain sensitivity but also delay important medical treatment, lower efficiency, and also undermine patients’ willingness to continue their healthcare treatment.

<video width="80%" height=auto controls>
  <source type="video/mp4" src="https://boliu97.github.io/files/Video/Lullaland_demo.mp4">
</video>

## Interview & Suvery

### We interviewed 12 participants, including 6 adults and 6 parents, each for 30 minutes.
We asked them to walk us through the whole experience they had at clinic, and asked their mood changes.

### We also conducted a survey to further prove our insights. We sent out questionnaires online and got 40 results.
**90%** of participants would feel nervous when they go to hospitals.
The hospital environment, unknown therapies and the smell of the hospital are the top three factors that cause anxiety.

**70%** of participants reported that they have tried meditation to help get relaxed. 85% of participants said they will need to draw their attention from the anxiety.

**85%** of participants said they will need to draw their attention from the anxiety.

## Hardware

Hardware Design           |      Circuit Design
:-------------------------:|:-------------------------:
![](http://boliu97.github.io/images/Lula_HardSch.webp)  |  ![](http://boliu97.github.io/images/Lula_3D.webp)

*   Control the on/off of 2 fans to provide with different aroma intensity
*   Contain four isolated sections for different fragrance oil pods
*   Use a motor servo to choose different fragrances
*   Wireless and wearable with a battery integrated

## Prototype
<img src='/images/Lula_prototype.png'>

## Software
In Unity, we used Restclient to transform request and response data to Google Firebase. As users navigated the scene, we sent the distance data and the current scene code to the cloud. Then, in the aroma diffuser, the ESP32 extracts the distance data to control the fans and adjust the odor's intensity. Moreover, the scene code was used to control the spin angle of a motor to adjust the smell it diffuses. Therefore, the smell blends with the scene the user sees in Oculus.
<img src='/images/Lula_front.png'>

## Conclusion 

In summary, our research points to the feasibility of multisensory interactive VR content when applying VR distraction in medical healthcare. Our work contributes to a novel de-stress game of VR + aroma that can be used to reduce anxiety in high-stress situations such as hospital waiting rooms. With the fast-growing technology and the increasing need for a better medical care experience, there will be more possibilities and demands for the discovery of distraction-based VR therapy.

