# Digital Pursuit Rotor Test

A modern, highly configurable, browser-based implementation of the classic Pursuit Rotor apparatus used in cognitive psychology, neuroscience, and motor control research.

## 1. Background & History
The Pursuit Rotor Test is a classic "tracking game" designed to measure visual-motor tracking skills and hand-eye coordination. 
* **The Traditional Apparatus:** Historically, the test utilized a mechanical device resembling a vinyl record player. A metal turntable spun a small metal target (usually at a high speed, such as 60 RPM), and participants used a hinged metal wand (stylus) to maintain contact with the target as it rotated.
* **The Digital Evolution:** Because tracking an object with a computer mouse, trackpad, or touchscreen requires different biomechanical feedback than a physical wand, digital adaptations are typically scaled down in speed. The clinical standard for digital baseline testing is approximately 8 RPM. This application faithfully recreates the digital clinical standard while allowing researchers to scale difficulty linearly.

## 2. What the Test Measures
This software continuously evaluates user performance to quantify specific neurological and cognitive functions:
* **Procedural Learning (Muscle Memory):** The brain's ability to automate a physical skill. Because the target moves in a predictable, continuous circle, healthy neural pathways will adapt, showing a distinct "learning curve" (higher scores in later trials compared to initial trials).
* **Motor Control & Precision:** The efficiency of communication between the visual cortex and fine motor muscle groups to execute smooth, micro-adjustments.
* **Sustained Attention & Fatigue:** Tracking a repetitive moving target requires intense executive focus. Degradation in scores over long durations highlights cognitive fatigue or lapses in concentration.

## 3. Clinical & Research Applications
Researchers and medical professionals utilize Pursuit Rotor tracking for several diagnostic and experimental purposes:
* **Neurodegenerative Disease Screening:** Conditions like Parkinson’s or Huntington’s impair the basal ganglia, making smooth muscle movements difficult. Patients typically struggle to stay on target and show flattened learning curves.
* **Traumatic Brain Injury (TBI):** Used to assess hand-eye coordination deficits following concussions or severe head trauma.
* **Pharmacological & Fatigue Studies:** Applied to measure the extent to which alcohol, specific medications, or sleep deprivation impairs physical reflexes and coordination.

## 4. Software Features & Parameters
This application is built for maximum flexibility in a laboratory or classroom setting. It features a responsive, touch-friendly HTML5 Canvas that scales perfectly across desktop monitors, tablets, and smartphones. 

Researchers can manipulate the following independent variables in real-time:
* **Trials per Session (1–20):** Define the exact number of tracking rounds before the session concludes and data is finalized.
* **RPM / Speed (1–60):** Adjust the rotational velocity of the target. 8 RPM is the baseline standard; higher RPMs exponentially increase difficulty.
* **Target Size (10–50px):** Manipulate the spatial margin of error. A smaller radius demands higher visual-motor precision.
* **Trial Duration (5–60s):** Standard trials last 15–20 seconds. Shorter durations test immediate acquisition, while longer durations induce cognitive fatigue.
* **Rest Interval (0–60s):** Controls the inter-trial interval (ITI) for experimental design. 

## 5. Experimental Design: Massed vs. Spaced Practice
The software natively supports standard practice distribution experiments:
* **Massed Practice:** Set the *Rest Interval* to `0`. The test will pause after each trial, requiring the user to manually click "Start Next Trial," allowing for immediate repetition with minimal rest.
* **Spaced Practice:** Set the *Rest Interval* above `0` (e.g., 10 seconds). The software will introduce a strict, automated countdown timer between trials, enforcing neurological rest before the next round begins.

## 6. Scoring & Data Export
The application operates on a 60-frames-per-second (`requestAnimationFrame`) loop to ensure high-fidelity timekeeping. 

* **Time on Target (ToT):** Calculated by accumulating the exact delta-time (in milliseconds) the user's cursor or finger remains within the target radius. The software strictly caps time calculation to the exact duration of the trial to prevent frame-trailing inaccuracies.
* **Accuracy:** Represented as the percentage of the total trial duration successfully tracked.
* **CSV Export:** Upon completion of a trial or session, researchers can export a `.csv` file containing the learning curve data. The spreadsheet logs: *Trial Number, RPM, Target Radius, Trial Duration, Score (s), and Accuracy (%)*.

## 7. Setup & Usage
No installation, backend server, or dependencies are required. 

## 8. Author & Copyright
**Created by:** Sarah Qureshi  
This tool complements other cognitive psychology resources, such as the Digital Memory Drum Simulator, to provide accessible, high-quality interactive lab experiences.

 # License

**Copyright (c) 2026 Sarah Qureshi. All rights reserved.**

This software is free to use for personal, educational and non-commercial purposes, including use in classrooms and linking to it from other sites.

You may not copy, redistribute, modify, sell or create derivative works of the source code without prior written permission from the copyright holder.

**Contact:** [sarahqureshipsych@gmail.com](mailto:sarahqureshipsych@gmail.com)
© 2026 Sarah Qureshi. All rights reserved.  
This software and associated documentation files are protected by copyright law. You may not reproduce, distribute, modify, display, or create derivative works of this software, in whole or in part, without explicit prior written permission from the copyright holder.
