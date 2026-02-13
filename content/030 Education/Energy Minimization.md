---
publish: true
created: 1969-12-31T18:00:00.000-06:00
modified: 2025-09-12T23:38:13.000-05:00
cssclasses: ""
---

key operation for [[030 Education/MD Simulation]] and studying [[Protein Interactions]]


- EMin is finding lowest energy form on a graph, like a regular math problem
- Central dogma: lowest energy structure is the 'correct' one
	- This is where first derivative = 0
		- If 2nd derivative > 0, it's a minimum
		- if 2nd derivative < 0, it's a maximum
		- If 2nd derivative = 0, it's a saddle point
	- So in this problem
		- y is potential energy usually from force field equaitons
		- Xi is coordinate, sometime cartesian but not usually
- We have to look for global minimum not local minima
	- **Newton's method:** most CPU intensive but accurate
		- Approximate y locally using a Taylor series truncated to a parabola
		- Newton-Raphson: generalization of newton to multiple dimensions
	- **Steepest descent: **cheap on CPU works better when far away
		- Draw bunch of lines and use 3 points to make parabolas
		- calculate one with lowest point, go there. Repeat
		- Good at getting in the area quickly on dramatic cliffs but struggles with shallow plains it will wander aimlessly 
	- **Conjugate gradients:** good general more expensive than steepest
		- Use M steps where M is the number of variables
		- Search in one, draw orthogonal vector for each one and proceed
	- Strategy
		- It's advisable to start with a cheap one like steepest descent then refine search with a more expensive and accurate method
