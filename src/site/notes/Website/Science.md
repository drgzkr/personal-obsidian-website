---
{"dg-publish":true,"permalink":"/website/science/"}
---

Here are some **odd projects** I've worked on through **branches** of my **research**.
Perhaps I'll also share the kitchen side of the papers I'm working on in the future...

---
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




---
## Frequencies, Phases, Harmonics, Discrete States, State Transitions, Criticality, and More...



---
## Communicative Interpretive Intermediations (A.K.A. Language) and Brain to Brain Interfaces

This is a small paper I wrote for a MSc course, and I like it. I don't have the energy to revise and build on it to make an actual publishable work out of it, but I would like interested minds to read it and engage with it. Have a look if you are curious:

<div class="rich-link-card-container"><a class="rich-link-card" href="https://docs.google.com/document/d/1Q5Y49cY1s4veYPyvTIDfG_rNk0JlPrUf/edit?usp=sharing&ouid=112645292736462517674&rtpof=true&sd=true" target="_blank">
	<div class="rich-link-image-container">
		<div class="rich-link-image" style="background-image: url('https://ssl.gstatic.com/docs/documents/images/kix-favicon-2023q4.ico')">
	</div>
	</div>
	<div class="rich-link-card-text">
		<h1 class="rich-link-card-title">DoraGözükara_i6110205_Timing Neural Processing With EEG and MEG_2019_FPN.docx</h1>
		<p class="rich-link-card-description">
		EEG Based Non-Invasive Brain to Brain Interfaces: State of the art human computer interfaces with a clumsy last step Dora Gözükara i6110205 Faculty of Psychology and Neuroscience Timing of Neural Processing with EEG and MEG Fren Smulders Spring 2019 Maastricht Abstract Brain to br...
		</p>
		<p class="rich-link-href">
		https://docs.google.com/document/d/1Q5Y49cY1s4veYPyvTIDfG_rNk0JlPrUf/edit?usp=sharing&ouid=112645292736462517674&rtpof=true&sd=true
		</p>
	</div>
</a></div>

---

## You know what?

I also have very close and academic interests in:
- **ANN interpretability**
	- I think my neuroscience background gives me the right tools and frameworks to understand ANN models and their internal 'cognition', computationally. Naturally, I'm interested in feature space trajectories and general representational computations of cognition, both in AI models and in biological brains. I'm interested in various kinds of models, from CNNs to AEs to LLMs.
	- Naturally, I'm also interested if/when/how we might need to consider ANNs and their 'experiences'... (please don't get scared, I know what I'm talking about)
- **Hierarchical Cognition and Computation**
- **Big Science**
	- I have a multitude of intense feelings towards the future of science in light of ANNs: 
		- *terror*,
		- *marvel*,
		- *FOMO*,
		- *humility*,
		- *hope*,
		- *despair*...
	- I want to be involved in LLM driven science, either understanding, mapping, generating; or even executing and reviewing.
	- HMU if you know someone... this can't be done on an individuals budget 😢 (i tried making a cute and fun 'artsy' scientific paper generator back in 2021. now we have people doing this:)
- **Education, but like, genuinely**
	- LLMs gave me the excuse to try my rebellious educational ideas. For a course I was coordinating and TAing, I structured the assessments so that students would grade their own assignments based on the effort they thought they gave to them. They were not expected to submit right answers. LLMs could do that for them. Instead, they were expected to try their own answers, and if they didn't understand how they would go about doing that, to clearly write what information they though they were missing or did not understand. The workgroup sessions were then when we discussed answers or confusions, without any assessment/grading stress. 
	- [[Website/About Me#Teaching\|Problem based learning (PBL)]] is very effortful for both the educator and the students (well that's mostly the point anyway), and LLMs can help bring its principles to self-study and autodidaction. We could build amazing tools for learners of all ages/levels.