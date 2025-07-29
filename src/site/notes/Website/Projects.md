---
{"dg-publish":true,"permalink":"/website/projects/"}
---

 
Here are some **silly** projects I make whenever I'm **bored** or **procrastinating**.
They are **meant for a laugh**, so don't take them **seriously**...

## [[Stupid Projects/Sinbeddings\|Sinbeddings]]

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/stupid-projects/sinbeddings/#what" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## What?

See the sin trajectory of any sequence of events.
Given a text with multiple sentences, an LLM codes each sentence based on how much of which 7 sin is present. 
The dashboard then visualizes the sin journey of the text with an animated radar plot and state space trajectory made up of 2 principal components of the whole sinbedding timeline.
The dimensions are also interpreted based on which sin is loaded in them to characterize a unique sin-space for the text.

Play with it by giving it biographies, or known literary texts, or your own stories.

![Pasted image 20250722151723.png|500](/img/user/Pasted%20image%2020250722151723.png)
![Pasted image 20250722155707.png|500](/img/user/Pasted%20image%2020250722155707.png)

---



</div></div>


## [[Stupid Projects/WikiBrainrot\|WikiBrainrot]]

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/stupid-projects/wiki-brainrot/#what" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## What?
This little pipeline pulls a random Wikipedia article and creates a text to speech dictation of it using coqui-tts.
It then loads a long video, chops it to the length of the audio file, adds the text of the speech (at correct timestamps) to the video, and saves the corresponding video file.

TLDR: Free TikTok Brainrot Generator

|![Pasted image 20250722154817.png|150](/img/user/Pasted%20image%2020250722154817.png)|![Pasted image 20250722154911.png|150](/img/user/Pasted%20image%2020250722154911.png)|![Pasted image 20250722155031.png|150](/img/user/Pasted%20image%2020250722155031.png)

--- 

</div></div>


## [[Stupid Projects/GumuslukCircir\|GumuslukCircir]]

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/stupid-projects/gumusluk-circir/#what" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## What?
This notebook was born out of boredom and curiosity during my short vacation in Gumusluk, Bodrum.
Several cicadas were around the house of my friend who hosted a group of us for a week, who were quite chatty (both us and the cicadas).
Here is one which joined us during one of our card playing sessions:

![Untitled.jpeg|200](/img/user/Untitled.jpeg)|![Untitled 4.png|320](/img/user/Untitled%204.png)

One morning, I was reading on the balcony, and was accompanied by a few of these loud high-chitin friends. I decided to ignore their privacy and recorded them without their consent.
Here are some simple analysis done on that recording that takes a closer look at the cicada song at a very basic level.

---

</div></div>


## [[Stupid Projects/Football State Segmentation\|Football State Segmentation]]

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/stupid-projects/football-state-segmentation/#what" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## What?

I wanted to see if I could take raw football tracking data (just the x/y coordinates of players and the ball) and carve it up into meaningful “states” of play. Not tactics per se, just recurring spatial configurations that show up again and again, hidden in the flow.

The notebook loads one half of a match, does some light cleaning, centers everything around the team’s center of mass (so we are looking at team configurations independent of overall location), and then uses GSBS (a state segmentation method from neuroimaging) to chop the game into temporally coherent chunks.

The notebook has:
- a cleaned and down sampled 2D array of movement features (player x-y coordinates)
- time segments that align with sharp shifts in overall spatial pattern
- visualizations of transitions between states: some matrices, timelines, chord plots

I didn't have the time (but more importantly the motivation) to pursue this further, and the notebook is a bit of a mess; but it looks like a promising approach. Some hierarchical clustering is also possible on the states.

Of course, if one wants to go about doing something similar, training recurrent deep learning models or transformers on this data would surely perform better.

![Pasted image 20250728221453.png|400](/img/user/Pasted%20image%2020250728221453.png)
![Untitled 5.png|400](/img/user/Untitled%205.png)

---  

</div></div>


# Idea Drafts

These are unattempted and poorly though-through darfts. 
Please don't steal them 🙏 
Thank you 😇

## [[Stupid Projects/BrainLamp\|BrainLamp]]


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/stupid-projects/brain-lamp/#what" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



## What?

By using smt like [this](https://community.mrtrix.org/t/connectome-node-mesh-visualisation-problem/1571/13) connectome visualization tool of MRtrix, build a 3d model of the brain with areas connected with realistic WM simplifications.

Smt like this, but transparent and simpler:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc2B4ZZOj_6_qtkcGmtkvRNYqhdzKc7IF1l8KfEe8XqCgI3TyrIHsSD9OfEBahI8f2Y1MrS1tW-vXNG2nm3gNTlREcz1UDkpsvBMsIkTYhvQyUijZ9wgeJrJxYGgCFxYJGFG7kPpraLLwu5hDcAQNVFT-hl?key=vpIcQv8PgR9wCy0vi8o6Og)

  

- Run LED filaments along the tubes and in the hollow ROIs 
- Get resting state data and construct 1 functional connectivity sweep loop to play on the brain.
- Assign different colors for different functional networks, combine colors where necessary by blending them into each other.
- Activate LEDs based on the created loop.
- Dance.


</div></div>
