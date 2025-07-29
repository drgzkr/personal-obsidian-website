---
{"dg-publish":true,"permalink":"/stupid-projects/brain-lamp/"}
---

## What?

By using smt like [this](https://community.mrtrix.org/t/connectome-node-mesh-visualisation-problem/1571/13) connectome visualization tool of MRtrix, build a 3d model of the brain with areas connected with realistic WM simplifications.

Smt like this, but transparent and simpler:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc2B4ZZOj_6_qtkcGmtkvRNYqhdzKc7IF1l8KfEe8XqCgI3TyrIHsSD9OfEBahI8f2Y1MrS1tW-vXNG2nm3gNTlREcz1UDkpsvBMsIkTYhvQyUijZ9wgeJrJxYGgCFxYJGFG7kPpraLLwu5hDcAQNVFT-hl?key=vpIcQv8PgR9wCy0vi8o6Og)

  

- Run LED filaments along the tubes and in the hollow ROIs 
- Get resting state data and construct 1 functional connectivity sweep loop to play on the brain.
- Assign different colors for different functional networks, combine colors where necessary by blending them into each other.
- Activate LEDs based on the created loop.
- Dance.

## Project

The project has 2 main branches: physical build, and the software.
### The Physical Brain

#### 3D Print the model

- Access a 3d printer
	- find someone who has 1
		- PROs
		- someone with experience
		- no material investment needed
		- CONs
		- good opportunity to get a 3d printer
	- buy a 3d printer
		- PROs
		- fun
		- can use in future projects
		- CONs
		- slightly costly
		- I dont have much space
- Prepare the 3d model
	- find real open access diffusion data
	- hope you can export MRTrix visualisation tool models as 3d models
- decide on how the lamp will look like aesthetically
	- how many connections
	- how many ROIs
	- how big do the tubes need to be
#### Build the LED circuit

- Use either an Arduino or Raspberry Pi
	- Pi could be better for future software additions like live input
- Find appropriate addressable led tubes
- learn the controller software and hardware    
- placing the LEDs in the tubes and ROIs in such a complex shape will not be easy, or easily reproducible find a clever solution 
- paths of relatively straight/linear hollow tubes and ROIs to just push the LED through them?
- place them as the print goes by?
- have some connection gaps throughout?
- openable sections?

### The Software

- find an open suitable dataset
- run a functional connectivity analysis and extract the timeseries for all needed functional networks
- determine the length of the loop
- Decide on which functional networks to use based on the physical brain design

- Alternatively, additionally, eventually, or inescapably, add other visualizations, like:
	- camera input and visual stream lighting
	- auditory input and auditory stream activity
	- both together
	- glow a certain color for notifications
	- change speed
	- etc