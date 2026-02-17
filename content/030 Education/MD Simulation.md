---
publish: true
created: 1969-12-31T18:00:00.000-06:00
modified: 2025-09-12T23:38:58.000-05:00
cssclasses: ""
---

Practical notes derived from the theorem of [[030 Education/Molecular Dynamics]]

- Force fields in YASARA
	- AMBER: 5 essential parts, good for explicit solvents no in vacuo
	- YAMBER-AMBER: AMBER adapted for yasara good for long protein simulations
	- YASARA/YASARA2: Best for homology modelling. uses dihedral potentials
	- YAMBER3:
		- What were using with a 7.86 anstrom cutoff for vdW forces only
		- long range electrostatic uses coulombs law via Wwalds algorithm
		- made for long simulations.
		- vdW interactions are a little stronger to eliminate holes in structure building
- Prepare structure for simulation
	- Add hydrogens, solvate it, eliminate gps, eliminate steric clashes 
	- Check amide sidechain orientation (Asn/Gln) because hydrogen is ambiguous
	- Check atom assignments of histidine assignments because Carbon vs Nitrogen is difficult
	- Final minimization
- Dunk it in a box bound, usually water box
- Some programs have to specify which cysteines are bridged
- Initial state
	- position r is from experimental (crystallographers or QM)
	- velocities are random values in boltzman distribution modulated by temperature
- Simulation
	- initial state r and v
	- sum of forces are vector F on each atom via force field
	- calculate accelerations from newtons 2nd law
	- use a small time interval dt
	- calculate dv = integral(a x dt)
	- new velocity vector v' = v + dv
	- new positions r' = r + v' dt
	- take new r' and v' and return to step 2
- Periodic boundary conditions
	- every time an atom exits from boundary conditions of the cell, an identical one of same type enters from opposite side with same velocity
- Equilibration
	- Have to wait for the system to equilibrate at the given temperature because initial V are random
	- this means you can't use the first part of the simulation
	- for protein you dump the first nanosecond
	- for peptide this doesn't take as long, 100-300 picoseconds
	- you know when Heavy Atom root mean standard deviation (HA_rmsd) plotted over time should equilibrate 
	- Energy should be pretty constant over time
	- 