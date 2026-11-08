<div align="center">
  <img src="assets/hero.svg" width="100%" alt="Inshal Ahmed — full-stack engineer building systems that sense the world">
</div>

I work across the stack. Most of what I build takes a reading from the physical world — satellite imagery, CubeSat telemetry, a camera on a moving car — and turns it into something a person can act on.

## Helios Shield

A 1U CubeSat engineering model that measures UV and magnetic disturbance, logs it on board, and warns a ground operator within seconds of a limit being crossed. Built with the **FalconEye** team for SatForge 2026.

<table>
<tr>
<td width="35%" valign="top">
  <img src="assets/helios-chassis.jpg" width="100%" alt="3D-printed 1U CubeSat chassis">
</td>
<td width="65%" valign="top">
  <img src="assets/helios-dashboard.png" width="100%" alt="Live ground-control dashboard showing gauges, alert levels and the orbit globe">
</td>
</tr>
</table>

- An ESP32 reads a UV module and a 3-axis magnetometer every 2 s, appends each packet to microSD, and posts it over authenticated HTTPS
- A Vercel serverless function stores the latest packet in Upstash Redis; the browser dashboard polls it and raises the alert level within seconds
- Alert thresholds, stale-link detection and out-of-range faults are all computed on the ground, so limits change without re-flashing the firmware
- Verified on the bench: HTTP 200 with matching sequence numbers, live feed in the browser. The UV index stays switched off until it is calibrated against a reference — the firmware reports raw millivolts instead of guessing

<img src="assets/alert-logic.svg" width="100%" alt="Magnetic field change rising through the warning and alert thresholds and clearing again">

![C++](https://img.shields.io/badge/C++-0E1728?style=flat-square&logo=cplusplus&logoColor=4FC3F7)
![ESP32](https://img.shields.io/badge/ESP32-0E1728?style=flat-square&logo=espressif&logoColor=FF4D7E)
![JavaScript](https://img.shields.io/badge/JavaScript-0E1728?style=flat-square&logo=javascript&logoColor=F7DF1E)
![Vercel](https://img.shields.io/badge/Vercel-0E1728?style=flat-square&logo=vercel&logoColor=FFFFFF)
![Upstash Redis](https://img.shields.io/badge/Upstash%20Redis-0E1728?style=flat-square&logo=redis&logoColor=FF4438)

**[Repository](https://github.com/inshal8717/HeliosShield_by_FalconEye)** · **[Live dashboard](https://helioshield-iota.vercel.app)**

## Other work

<table>
<tr>
<td width="50%" valign="top">

### [GreenBytes (Duroob)](https://github.com/inshal8717/GreenBytes)

Community tourism marketplace connecting visitors with farmers, guides and local businesses in the Al Qua'a region of the UAE. Built for the Tatweer Hackathon 2026.

- Role-based marketplace across tourist, farmer, guide and local business, with a bilingual EN/AR interface
- Google Maps with farmer-drawn safe-zone polygons, and a booking flow that detects time-slot conflicts
- An evening planner powered by Gemini that generates desert itineraries

![JavaScript](https://img.shields.io/badge/JavaScript-0E1728?style=flat-square&logo=javascript&logoColor=F7DF1E)
![Node.js](https://img.shields.io/badge/Node.js-0E1728?style=flat-square&logo=nodedotjs&logoColor=5FD35F)
![Firebase](https://img.shields.io/badge/Firebase-0E1728?style=flat-square&logo=firebase&logoColor=FFCA28)
![Gemini](https://img.shields.io/badge/Gemini-0E1728?style=flat-square&logo=googlegemini&logoColor=8E7CFF)

**[Live](https://duroobtourism.vercel.app)** · **[Demo video](https://youtu.be/kawjYLrZvtg)**

</td>
<td width="50%" valign="top">

### [EmergencyConnectUAE](https://github.com/inshal8717/EmergencyConnectUAE)

Emergency-services coordination platform that puts dispatchers, responders, hospitals and admins on one incident picture.

- Geospatial incident mapping on PostgreSQL with PostGIS spatial indexing
- Real-time incident management, responder assignment and routing, hospital resource tracking
- MFA and role-based access control across five user roles, via Supabase

![Java](https://img.shields.io/badge/Java-0E1728?style=flat-square&logo=openjdk&logoColor=ED8B00)
![TypeScript](https://img.shields.io/badge/TypeScript-0E1728?style=flat-square&logo=typescript&logoColor=4FA3F7)
![PostGIS](https://img.shields.io/badge/PostGIS-0E1728?style=flat-square&logo=postgresql&logoColor=6D8CFF)
![Supabase](https://img.shields.io/badge/Supabase-0E1728?style=flat-square&logo=supabase&logoColor=3FCF8E)

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [Satellite Change Detection](https://github.com/inshal8717/self-supervised-satellite-change-detection-train)

PyTorch pipeline that learns Sentinel-2 image representations from unlabelled imagery using temporal contrastive pretraining, so no human labels are needed for training.

- Dense feature-distance change maps, with unsupervised Otsu thresholding and morphological cleanup
- Real before/after pairs pulled from Microsoft Planetary Computer and co-registered to a UTM grid
- Streamlit dashboard with change heatmaps, binary masks, IoU/F1/AUROC metrics and tiled inference for large scenes

![Python](https://img.shields.io/badge/Python-0E1728?style=flat-square&logo=python&logoColor=4DA3E0)
![PyTorch](https://img.shields.io/badge/PyTorch-0E1728?style=flat-square&logo=pytorch&logoColor=EE4C2C)
![Streamlit](https://img.shields.io/badge/Streamlit-0E1728?style=flat-square&logo=streamlit&logoColor=FF4B4B)

</td>
<td width="50%" valign="top">

### [Autonomous Car Simulation](https://github.com/inshal8717/AutonomousCarSimulation)

CPU-only lane-following and traffic-light control for ROS 2 Jazzy and Gazebo Harmonic — no GPU and no neural nets required.

- Classical OpenCV and NumPy perception driving a PID steering controller
- Supervisor state machine with failsafe watchdogs, an offline evaluator and quantified performance metrics
- 43 tests covering the complete pipeline

![Python](https://img.shields.io/badge/Python-0E1728?style=flat-square&logo=python&logoColor=4DA3E0)
![ROS 2](https://img.shields.io/badge/ROS%202-0E1728?style=flat-square&logo=ros&logoColor=6EA8FE)
![OpenCV](https://img.shields.io/badge/OpenCV-0E1728?style=flat-square&logo=opencv&logoColor=7C6BFF)

</td>
</tr>
</table>

## Stack

Languages
&nbsp;
![Python](https://img.shields.io/badge/Python-0E1728?style=flat-square&logo=python&logoColor=4DA3E0)
![TypeScript](https://img.shields.io/badge/TypeScript-0E1728?style=flat-square&logo=typescript&logoColor=4FA3F7)
![JavaScript](https://img.shields.io/badge/JavaScript-0E1728?style=flat-square&logo=javascript&logoColor=F7DF1E)
![Java](https://img.shields.io/badge/Java-0E1728?style=flat-square&logo=openjdk&logoColor=ED8B00)
![C++](https://img.shields.io/badge/C++-0E1728?style=flat-square&logo=cplusplus&logoColor=4FC3F7)

Machine learning and vision
&nbsp;
![PyTorch](https://img.shields.io/badge/PyTorch-0E1728?style=flat-square&logo=pytorch&logoColor=EE4C2C)
![OpenCV](https://img.shields.io/badge/OpenCV-0E1728?style=flat-square&logo=opencv&logoColor=7C6BFF)
![NumPy](https://img.shields.io/badge/NumPy-0E1728?style=flat-square&logo=numpy&logoColor=4DABF7)
![Streamlit](https://img.shields.io/badge/Streamlit-0E1728?style=flat-square&logo=streamlit&logoColor=FF4B4B)

Platforms and data
&nbsp;
![Node.js](https://img.shields.io/badge/Node.js-0E1728?style=flat-square&logo=nodedotjs&logoColor=5FD35F)
![Firebase](https://img.shields.io/badge/Firebase-0E1728?style=flat-square&logo=firebase&logoColor=FFCA28)
![Supabase](https://img.shields.io/badge/Supabase-0E1728?style=flat-square&logo=supabase&logoColor=3FCF8E)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-0E1728?style=flat-square&logo=postgresql&logoColor=6D8CFF)
![Vercel](https://img.shields.io/badge/Vercel-0E1728?style=flat-square&logo=vercel&logoColor=FFFFFF)
![Redis](https://img.shields.io/badge/Redis-0E1728?style=flat-square&logo=redis&logoColor=FF4438)

Robotics and embedded
&nbsp;
![ROS 2](https://img.shields.io/badge/ROS%202-0E1728?style=flat-square&logo=ros&logoColor=6EA8FE)
![Gazebo](https://img.shields.io/badge/Gazebo-0E1728?style=flat-square&logo=gazebo&logoColor=FF7A3D)
![ESP32](https://img.shields.io/badge/ESP32-0E1728?style=flat-square&logo=espressif&logoColor=FF4D7E)
![Arduino](https://img.shields.io/badge/Arduino-0E1728?style=flat-square&logo=arduino&logoColor=2BD4E8)

<img src="https://raw.githubusercontent.com/inshal8717/inshal8717/output/snake.svg" width="100%" alt="A snake moving across the contribution graph">

## Reach me

[![GitHub](https://img.shields.io/badge/GitHub-inshal8717-0E1728?style=flat-square&logo=github&logoColor=E6ECF5)](https://github.com/inshal8717)

<!-- Add email / LinkedIn here when ready -->
