---
{"publish":true,"created":"2025-04-20T16:13:06.000-05:00","modified":"2025-09-12T23:39:09.171-05:00","cssclasses":""}
---


### Definitions

> [!definition]+ Fissionable
> A [nuclide](https://en.wikipedia.org/wiki/Nuclide) which can *theoretically* undergoes nuclear fission as a result of high or low energy neutrons. Examples include $\ce{U^238}$ This encompasses:
> > [!definition]- Fissile
> > A nuclide which *readily* undergoes nuclear fission as a result of low energy neutrons. Examples include $\ce{U^235, Pu^239}$. There are definitions for this which further specify "can be used in a chain reaction" but it is not standard. 
> 
> Fissionable also encompasses:
> > [!definition]- Fertile
> > A nuclide which is *not* fissile itself, but can can capture low energy neutrons to create elements which decay into fissile materials. This makes them suitable for breeder reactors. Examples include $\ce{U^238 and Th^232}$  
> 

### Fuel Cycle
- The **nuclear fuel cycle** describes the progression of nuclear fuel from its creation to its disposal.
	- **Once-Through Cycle**: Used fuel is not reprocessed (USA)
	- **Closed Cycle**: Spent fuel is reprocessed to recover U and Pu for reuse (e.g., France, Russia).
#### 1. Front-End (Fuel Preparation)
- **Mining & Milling:** Uranium ore is extracted and processed into U₃O₈ ("yellowcake").
	1. Convention mining, dig up rocks and grind them up 
	2. Heap leach, dig up rocks then perform chemical extraction
	3. In Situ Recovery, inject water + h2o2/na2co3/co2 and pump it up like EOR 
- **Conversion:** U₃O₈ is converted to UF₆ through chemical processes
	$Reduction: \ce{U3O8 + 2H2 → 3UO2 + 2 H2O}$
	$Hydrofluorination: \ce{UO2 + 4 HF → UF4 + 2 H2O}$
	$Fluorination: \ce{UF4 + F2 → UF6}$
- **Enrichment:** increases the concentration of useful isotope $\ce{U^235}$
	- Concentrations:
		- Natural: 99.3% $\ce{U^238}$, 0.7% $\ce{U^235}$, < 0.01% $\ce{U^234}$
		- Commercial grade (LEU): 3 - 5% $\ce{U^235}$ for LWRs
		- Commercial grade (HALEU): 5 - 20% $\ce{U^235}$ for advanced reactors
		- Weapons grade: 90% $\ce{U^238}$
	- Methods:
		1. Gas diffusion is old and outdated.
		2. Gas centrifuge is standard. Separate based on atomic weight $\Delta$
		3. Laser is cutting edge. Excite Specific isotopes to cause reaction, then separate. 
- **Fabrication:** Enriched UF₆ is turned into UO₂ pellets, packed into fuel rods
	- Conversion to UO2
		- $$\begin{matrix}
		Dry\;Method:\\
		Step\;One:\ce{UF6^{gas} + 2H2O^{gas} → UO2F2^{solid} + 4HF}\\
		Step\;Two:\ce{UO2F2^{solid} + H2^{gas} → UO2^{solid} + 2HF}\end{matrix}$$
		- $$\begin{matrix}
		Wet\;Method:\\
		Step\;One:\ce{?UF6^{gas} + ?H2O^{water} + ?NH3 → ?(NH3)2U2O7^{solid} + ?HF}\\
		Step\;Two:\ce{?(NH3)2U2O7^{solid} →[heat] UO2^{solid}}\end{matrix}$$
	- Pressed into pellets, heated, machined
		- Can add poisons like $\ce{Gd}$ to temporarily slow down reactivity and heat generation
	- Pellets are built into fuel rods [^1]
		- Rods are made mostly (95%) of $\ce{Zr}$ because of its low neutron cross section. 
		- $\ce{Hf}$ is deliberately removed because of high cross section. $\ce{Sn, Nb, Fe, Cr}$ are added in trace to improve corrosive and structural properties.  
		- Filled with pressurized $\ce{He}$ and welded shut, with a little overhead space maintained for gaseous byproducts. 
	- Assemblies vary moderately depending on reactor design. 
		- PWR, BWR, CANDU, AGR, 
#### 2. In-Reactor (Fuel Use)
- **Fission:** Fuel is loaded into a reactor where U-235 undergoes fission, releasing energy.
- **Transmutation:** Some U-238 captures neutrons and turns into Pu-239, which can also fission.
#### 3. Back-End (Used Fuel Management)
- **Storage:** Spent fuel is stored on-site (wet or dry).
- **Reprocessing:** Recover fissile materials (e.g., Pu-239, U-235) for reuse.
- **Disposal:** Placed in final repositories (none in the USA)

### Reactor Types
*These attributes can be mixed and matched, most of them do not exclude each other and hence there is a wide range of possibilities*
- Purpose
	- **Breeder Reactor:** produces more fissile materials than it consumes. More for isotope production than power.
	- **Burner Reactor:** uses more fissile materials than it consumes. Mainly for generating electricity or heat. 
	- **Research Reactors:** used to produce supply of neutrons. Generally these are slow, burners types but in theory could be different[^2]
	- **Propulsion Reactors:** yeah. Naval or Aero. 	
	- ==*Both breeder and burners do some of each process (burning and generating new fuel). It's about the ratios, not all or nothing. They both produce usable electricity.*== 
- Fission speed
	- **Slow** aka **Thermal-neutron reactors**
		- Use a moderator material to decrease the temperature/kinetic energy of the neutrons produced from fission. This increases odds of fission in fissile materials. 
		- Increased fission cross section decreases enrichment required for sustained reaction.  
		- Vastly more common across the world in all cases.
	- **Fast-neutron reactors**
		- Use neutrons directly as they are produced from fission. They have no moderators and use low moderating coolants. Less common and more expensive. 
		- They require higher enrichment grades because of the lower reaction cross section, and degrade hardware faster due to high energy collisions. 
		- However, they produce less transuranic waste because they can fission actinides. 
- Coolant
### Tools
- [NQA-1](https://www.asme.org/certification-accreditation/nuclear-quality-assurance-nqa1-certification) 
	- is an ASME certification for the proper operation of nuclear facilities. This could apply to anyone from power plants, to equipment manufacturers, to fuel handlers, to disposal. 
	- Section 2 is for having a QA program. This includes annual internal audits and manual
	- Section 3 details the manual itself. Must be written in plain English. describes the scope, processes, responsibilities, and authority. 
	- Section 4 application process. 
	- Section 5 audits. Once for initial/renewal, twice over three years, unlimited if triggered for cause or nonconformance. 
	- Section 6, 7, 8 details, changes, suspensions
- [RELAP5-3D](https://en.wikipedia.org/wiki/RELAP5-3D) 
	- is a simulation tool for modeling transient thermal-hydraulic systems.
	- Purpose
		- Analyzing accidents from loss of coolant and operation transient changes. 
	- Capabilities
		- Nonhomogeneous (multiphase with liquid & gas) and nonequilibrium of two or fewer species. 
		- Control systems components like PI, valves, and fluid handlers.
		- Models by approximating flow path as one dimensional, where the radial dispersion is considered negligible. 
	- Method
		- Hydrodynamics require nodalization, where control volume boundaries are manually chosen throughout the flow path. Boundaries should *not* be placed in the middle of substantial density changes or flow transitions. 
			- Each node is connected through junctions which decide which data to pass on and how the connection should be modeled. 
		- Thermodynamics are generally modeled one dimensionally, using finite methods. Analysis connected to the hydrodynamic path can conduct heat transfer calculations normal to the direction of flow (aka how hot do my pipes get)
			- There are 2D simulations for low P core flooding to analyze pressure spikes, but not primary. 
### Decay & Radiation


> [!important] Decay Equation
> $$ N = N_0 e^{-\lambda t}\;\;\;and\;\;\; \lambda = \frac{0.693}{T_{half}} \;\;\;where...$$
> - N is number of Nuclei, t is time
> - $\lambda$ is decay constant
> - $T_{half}$ is half life
- There are many types of radioactive decay
- **Alpha Decay** 
	- Produces an alpha particle, which is an He-4 nucleus. No electrons so it's positive
	- More typical in heavier elements like transuranics
	- Shielded with very little effort
- **Beta Decay**
	- There are two types 
		1. Converting neutron to proton creates electron + antineutrino
		2. Converting proton to neutron creates positron + neutrino 
	- 'easy' to shield with plastic or Al, but that generates brehmsstrahlung, which needs lead
- **Gamma Decay**
	- 
## Sources


[^1]: https://world-nuclear.org/information-library/nuclear-fuel-cycle/conversion-enrichment-and-fabrication/fuel-fabrication#triso-high-temperature-reactor-fuel

[^2]: https://world-nuclear.org/information-library/non-power-nuclear-applications/radioisotopes-research/research-reactors
