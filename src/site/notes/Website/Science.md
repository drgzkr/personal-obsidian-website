---
{"dg-publish":true,"permalink":"/website/science/"}
---

Here are some **side projects/tools** I've worked on through **branches** of my **research**.
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
## Communicative Interpretive Intermediations (A.K.A. Language) and Brain to Brain Interfaces

This is a small paper I wrote for a MSc course, and I like it. I don't have the energy to revise and build on it to make an actual publishable work out of it, but I would like interested minds to read it and engage with it. Have a look if you are curious:
[Here](https://docs.google.com/document/d/1Q5Y49cY1s4veYPyvTIDfG_rNk0JlPrUf/edit?usp=sharing&ouid=112645292736462517674&rtpof=true&sd=true)

---

# Unattempted Projects

## [[Science Projects/Wittgenstein and Representational Similarity\|Wittgenstein and Representational Similarity]]

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/science-projects/wittgenstein-and-representational-similarity/#what" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## What?

A concept I’ve been chewing on: drawing a formal bridge between Wittgenstein’s late philosophy of language. specifically his notion of family resemblances. and how we now study neural representations in cognitive neuroscience using tools like Representational Similarity Analysis (RSA).

Put simply: I think there’s a useful and underappreciated **isomorphism** between **the way meaning emerges in language (according to Wittgenstein)** and the way meaning or content is **encoded in distributed neural population codes.**

It’s still a rough idea, but I’d like to polish it into a short perspective or opinion paper. The goal is to sketch a common conceptual language for discussing high-level semantics (philosophy of language) and low-level neurocomputational implementation (brain activity patterns), with RSA as the bridge.

---


</div></div>



## [[Science Projects/Fourier Theory of Perception\|Fourier Theory of Perception]]


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/science-projects/fourier-theory-of-perception/#what" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## What?
This is a very old idea (see [here](https://pubmed.ncbi.nlm.nih.gov/11430239/)). I myself started suspecting something like this might be a very clean framework to understand perception (and perhaps other cognitive phenomena) more closely than contemporary neuroscience gives credit to, when I was going through a course on MRI and learning about how MRI images are reconstructed via the k-space. I also thought perception working through the frequency space both in audition via the cochlea, and vision via spatial frequency selective cells made the idea much more compelling.

I didn't touch it for a long time, and then heard it from [Katja](https://seelikat.github.io/)!

I then played with the idea more operationally and made [this](https://colab.research.google.com/drive/1WkukBkBrAt8xgoCK2eSwvA-KtOtfIrKl?usp=sharing) exploratory notebook out of it.

**BEWARE:** The notebook is an early prototype, and thus lacks validation. The data it uses is *very* limited and the whole idea and pipeline needs serious rethinking. I suspect there might be some issues with the parameter space, regularization, and model architectures. Definitely needs a cleaner start. 

Nevertheless, here are some pretty figures to look at:


![Untitled 9.png](/img/user/Untitled%209.png)

![Untitled 10.png|250](/img/user/Untitled%2010.png)

---



</div></div>



--- 
## You know what else?

I also have very close and academic interests in:
- **ANN interpretability**
	- I think my neuroscience background gives me the right tools and frameworks to understand ANN models and their internal 'cognition', computationally. Naturally, I'm interested in feature space trajectories and general representational computations of cognition, both in AI models and in biological brains. I'm interested in various kinds of models, from CNNs to AEs to LLMs.
	- Most recent examples I'm working around are:
		- https://www.sciencedirect.com/science/article/pii/S0896627322000058
		- Hierarchical cognition and computation
		- The analogy between positional encoding vectors in transformers and grid cells in brains
	- Naturally, I'm also interested if/when/how we might need to reconsider ANNs and their 'experiences'... (please don't get scared, I know what I'm talking about)

- **Big Science**
	- I have a multitude of intense feelings towards the future of science in light of ANNs: 
		- *terror*
		- *marvel*
		- *FOMO*
		- *humility*
		- *hope*
		- *despair*...
	- I want to be involved in LLM driven big science, either understanding, mapping, synthesizing; or even generating, executing, and reviewing.
	- HMU if you know someone... this can't be done on an individuals budget 😢 (i tried making a cute and fun 'artsy' scientific paper generator back in 2022. Now we have people doing this publicly: https://arxiv.org/pdf/2408.06292. **God knows what is happening in well funded private labs...**)

- **Education, but like, genuinely**
	- LLMs gave me the excuse to try my rebellious educational ideas. For a course I was coordinating and TAing, I structured the assessments so that students would grade their own assignments based on the effort they thought they gave to them. They were not expected to submit right answers. LLMs could do that for them. Instead, they were expected to try their own answers, and if they didn't understand how they would go about doing that, to clearly write what information they though they were missing or did not understand. The workgroup sessions were then when we discussed answers or confusions, without any assessment/grading stress. 
	- [[Website/About Me#Teaching\|Problem based learning (PBL)]] is very effortful for both the educator and the students (well that's mostly the point anyway), and LLMs can help bring its principles to self-study and autodidaction. We could build amazing tools for learners of all ages/levels.