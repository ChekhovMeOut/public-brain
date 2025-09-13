---
{"publish":true,"created":"2025-03-04T10:49:46.000-06:00","modified":"2025-09-12T23:40:48.003-05:00","cssclasses":""}
---


- After running [[030 Education/MD Simulation]] do trajectory analysis
- Plot potential and kinetic energy over time. Should be pretty Constant
	- remember to throw out the first part
	- Kinetic is slightly positive
	- Total Pe is very negative, total is negative
- Potential energy is sum of:
	- Bond stretch (small)
	- angle bending (small)
	- dihedral alignment (small)
	- improper (small)
	- coulombic (easily largest contribution, very negative)
	- vand der Waals (2nd largest, positive)
- Radial distribution functions (RDF)
	- Density of atoms of a type within a spherical SHELL of radii R and thickness dr 
	- based on same reference atom, but do not have to search for same atom type (eg: Ca reference looking at water density) 
	- varying plot with r: initial spike, valley, then levels out in the middle
	- All things should be equal as you get farther and it appears like the bulk value
	- Example: N termini
		- water density = 3.5 about 3 angstroms
	- Example: C termini
		- water density = 2 at about 3 angstroms
	- Example: tyrosine beta carbon (hydrophobic)
		- water density = 0.5 at 4 angstroms
	- Example: tyrosine N terminus 
		- water density = 3.5 at 3 angstroms 