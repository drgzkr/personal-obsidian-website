---
{"dg-publish":true,"permalink":"/website/science/"}
---

Here are some **odd projects** I've worked on through **branches** of my **research**.

## fMRI Basics on Colab
This notebook has basic tools for fMRI analysis with Python
https://colab.research.google.com/drive/1GqsibJftyPEucJNVwbNeupLqJlBG21h3?usp=sharing
---
## [[Science Projects/QPPython\|QPPython]]

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/science-projects/qp-python/#what" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## What?

Python implementation of the core functionality of;

**QPPLab: A generally applicable software package for detecting, analyzing, and visualizing large-scale quasiperiodic spatiotemporal patterns (QPPs) of brain activity**

published here: [https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10557593/](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10557593/)

and maintained here: [https://github.com/GT-EmoryMINDlab/QPPLab](https://github.com/GT-EmoryMINDlab/QPPLab)

Aside from having been written in Matlab, the original package enforces a lot of custom data structures both for inputs and outputs. This one does not. We also made what we believe to be some improvements on the algorithm (e.g. better sliding window implementations requiring less memory).

---

</div></div>


---
## [[Science Projects/GSBS GUI\|GSBS GUI]]

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/science-projects/gsbs-gui/#what" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## What?

A makeshift tkinter GUI for viewing results of the Greedy State Boundary Search algorithm from

[statesegmentation package](https://github.com/lgeerligs/statesegmentation)

Has horrible implementation, but is convenient. I don't know what I'm doing and have no idea how to build a proper GUI. No elegance here.

![](https://private-user-images.githubusercontent.com/60198204/362094519-74192d8d-0f8e-45fd-94a0-848ba51d13e4.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTMxOTkxNjUsIm5iZiI6MTc1MzE5ODg2NSwicGF0aCI6Ii82MDE5ODIwNC8zNjIwOTQ1MTktNzQxOTJkOGQtMGY4ZS00NWZkLTk0YTAtODQ4YmE1MWQxM2U0LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNTA3MjIlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjUwNzIyVDE1NDEwNVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTgxYzAyYmVhOTM2ZmZiYWFjMzIwZDgwOTY5YWM4ODdlM2U3OWI1ODIyYmE2YTFjMDJjMzQ3MzhhYTFiMjIyNjUmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.5ecH9WK1nKqfxvth7o78VDiF8I5EoOOYoYeyOeIA7-Q)

---

</div></div>


---
## [[Science Projects/CNN-based Video Segmentation\|CNN-based Video Segmentation]]


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/science-projects/cnn-based-video-segmentation/#what" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## What?

Naturalistic Video Segmentation using vgg19 Features
This notebook saves the individual frames of given videos, extracts selected vgg19 layer features for each frame for each video and creates feature timeseries, and lastly plots the difference between each frames features on a timeline.
There are certain anomalies, and reasons and solutions are discussed at the end.

More at:
https://colab.research.google.com/drive/16TkQXS8wqkoVg47df1RvOw8B9TmYyjUs?usp=sharing

---

</div></div>


---
## Frequencies, Phases, Harmonics, Discrete States, State Transitions, Criticality, and More...

## Communicative Interpretive Intermediations, A.K.A. Language

