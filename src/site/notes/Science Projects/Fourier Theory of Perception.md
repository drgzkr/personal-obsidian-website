---
{"dg-publish":true,"permalink":"/science-projects/fourier-theory-of-perception/"}
---


## What?
This is a very old idea (see [here](https://pubmed.ncbi.nlm.nih.gov/11430239/)). I myself started suspecting something like this might be a very clean framework to understand perception (and perhaps other cognitive phenomena) more closely than contemporary neuroscience gives credit to, when I was going through a course on MRI and learning about how MRI images are reconstructed via the k-space. I also thought perception working through the frequency space both in audition via the cochlea, and vision via spatial frequency selective cells made the idea much more compelling.

I didn't touch it for a long time, and then heard it from [Katja](https://seelikat.github.io/)!

I then played with the idea more operationally and made [this](https://colab.research.google.com/drive/1WkukBkBrAt8xgoCK2eSwvA-KtOtfIrKl?usp=sharing) exploratory notebook out of it.

**BEWARE:** The notebook is very hastily made and was not iterated on further for corrections and checks. The data it uses is *very* limited and the whole idea and pipeline needs serious rethinking. I suspect there might be some issues with the parameter space, regularization, and model architectures. Definitely needs a cleaner start. 

Nevertheless, here are some pretty figures to look at:


![Untitled 9.png](/img/user/Untitled%209.png)

![Untitled 10.png|250](/img/user/Untitled%2010.png)

---


## How?

The notebook tries to poke at whether a Fourier-based representation of visual input can predict fMRI BOLD responses in visual and scene-related cortical areas.
### Core Idea

Take movie frames --> compute their 2D FFTs --> massage and mask the frequency domain in different ways --> run linear (and ridge) regressions --> see how well those features can predict voxel-level time series from human brain recordings.

### What Actually Happens

- Movie frames are preprocessed and converted to grayscale and resized.
- I play with masking different regions of the Fourier domain (low-pass, elliptical high-pass, concentric rings, etc.), reconstruct the images, and visualize what’s being preserved or lost.
- For each masked frequency region (especially these ring-shaped bands), I extract time series across frames.
- These time series are used as regressors against mean BOLD signals from regions like VIS_L, VIS_R, PPA_L, PPA_R, RSC_L, and RSC_R.
- I also compare regression performance using:
    - Raw image pixels
    - VGG-19 features (conv layer and fully connected)
    - Full FFT real components
- Then I histogram correlation coefficients across voxels to get a feel for what’s happening.

### Takeaways (Tentative and Probably Sketchy)

- FFT-based features can do _something_—some brain areas (especially visual ones) show moderate voxel-level correlation.
- Compared to pixel-based and VGG features, Fourier features are surprisingly not completely trash.
- Ring-based frequency bands seem to pull out structure in the signal, but it's unclear what they really mean in terms of representation.

## And?

I'd like to work on this more, but you know, there are annoying hiccups like financial security etc. I am forced to prioritize.

Contact me if you'd like to talk about it though!

