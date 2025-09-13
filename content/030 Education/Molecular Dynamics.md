---
{"publish":true,"created":"2025-03-04T10:49:46.000-06:00","modified":"2025-09-12T23:39:05.077-05:00","cssclasses":""}
---


- MD does not always apply
	- Classical dynamics applies when a certain equation is met, basically the bond frequency has to be low enough. ADD ME LATER
- Based primarily on Newtons 2nd law F =ma. Integrating from acceleration (a) to velocity (v) to position (r) is used to solve for atom location as a function of time
	- QM is too expensive to calculate with usually
	- Expand a, v, and r in taylor series to compare time T to T+delta
	- Verlet Algorithm
		- Obtain by subtracting the two series
		- Requires k and k-1, step to calculate k+1
	- Half-step AKA Leapfrog
		- Problems with verlet if timescale is too small
		- Velocity is calculated halfway between position and vice versa
		- Smaller errors, but never have both v and r at the same time making analysis complicated

