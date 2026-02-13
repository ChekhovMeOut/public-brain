---
publish: true
created: 1969-12-31T18:00:00.000-06:00
modified: 2025-09-12T23:38:09.000-05:00
cssclasses: ""
---


### Basic electrostatics
- involve stationary or slowly moving charges, sizes vary
- Interactions between charges are guided by:
	- coulomb's law, gauss's law, electrostatic potential, electric field
	- Default is vacuum, extra terms (dielectric const) are needed for materials. TLDR dielectric dampens the effect of the forces
- This physics matters because it describes the majority of AA interactions in solution
- Assumptions made for protein chem:
	- Charged AA are assumed to always be charged no WRT location
	- neglect explicit solvent molecules, do vacuum with dielectric approximations
	- Short time scale
### Introduction to Poisson-Boltzman
- Poisson-boltzman is commonly written as 
$$ \nabla^2\phi = - \frac{\rho}{\in_0} $$
- You have to define the problem in 3D space as the nabla is a gradient
	- There is a boundary between the bulk solve and the protein surface where the dielectric constant transitions and must be made with a smooth function
	- Ions are distrubted in energy with a boltzman distribution, which determines their relative location and frequency within the boundary layer
### PB equation and solutions
- Solving
	- Can only be solved analytically for very simple systems
	- Otherwise need numerical methods like finite difference
		- Discretize space into a grid, solve using laplace operator
		- At the edges of the grid use boundary condition potential = 0. Allows you to solve for adjacent cells, then fill in the gid
### Protein applications
- Hydration energies
	- in a vacuum and water
- Binding energies between proteins, antibodies, small molecules, etc.
	- Largely contributed by electrostatic factors (in addition to steric)
$$ \Delta G_{binding} = \Delta G_{complex}-(\Delta G_{receptor} - \Delta G_{ligand}) $$ $$ "there is no god but god" $$
- Molecular dynamics 
	- Forces between discrete objects can be incorporated into traditional MD force fields
	- Better for calculating strongly charged objects like salt bridges
- Brownian Dynamics
	- Simulation of solution diffusion, matters in quiescent contexts
- pKa and Titration
	- pH is a critical factor in stability
	- residues charges are often determined by subtle interactions between protonated/deprotonated residues
### Calculating Protonation states
### Conclusions
