---
{"dg-publish":true,"permalink":"/stupid-projects/football-state-segmentation/"}
---


## What?

I wanted to see if I could take raw football tracking data (just the x/y coordinates of players and the ball) and carve it up into meaningful “states” of play. Not tactics per se, just recurring spatial configurations that show up again and again, hidden in the flow.

The notebook loads one half of a match, does some light cleaning, centers everything around the team’s center of mass (so positions are comparable across time), and then uses GSBS (a state segmentation method from neuroimaging) to chop the game into temporally coherent chunks.

You get:
- a cleaned and down sampled 2D array of movement features
- a correlation-based template of the “average” state
- time segments that align with sharp shifts in overall spatial pattern
- visualizations of transitions between states: some matrices, timelines, chord plots

I didn't have the time (but more importantly the motivation) to pursue this further, and the notebook is a bit of a mess; but it looks like a promising approach. 

Of course, if one wants to go about doing something similar, training recurrent deep learning models or transformers on this data would surely perform better.

![Pasted image 20250728221453.png|400](/img/user/Pasted%20image%2020250728221453.png)
![Untitled 5.png|400](/img/user/Untitled%205.png)

---  
## Some resulting figures

![Untitled 6.png](/img/user/Untitled%206.png)

![Untitled 7.png|250](/img/user/Untitled%207.png) | ![Untitled 8.png|250](/img/user/Untitled%208.png)

notebook is here:
<div class="rich-link-card-container"><a class="rich-link-card" href="https://colab.research.google.com/drive/1jlKluk1uOt9MESNtB_2sMJRGnb3DfatH?usp=sharing" target="_blank">
	<div class="rich-link-image-container">
		<div class="rich-link-image" style="background-image: url('https://colab.research.google.com/img/colab_favicon_256px.png')">
	</div>
	</div>
	<div class="rich-link-card-text">
		<h1 class="rich-link-card-title">Google Colab</h1>
		<p class="rich-link-card-description">
		
		</p>
		<p class="rich-link-href">
		https://colab.research.google.com/drive/1jlKluk1uOt9MESNtB_2sMJRGnb3DfatH?usp=sharing
		</p>
	</div>
</a></div>



