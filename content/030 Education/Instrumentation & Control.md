---
publish: true
created: 1969-12-31T18:00:00.000-06:00
modified: 2025-09-12T23:38:32.000-05:00
cssclasses: ""
---

### "I"
- *Sensor* is a general term for anything that performs measurements 
	- *Transducer* is a sensor that outputs voltage representative of the physical signal. 
	- *Transmitter* is a sensor that outputs current representative of the physical signal.
- Temperature
	- *RTD* relate changes in resistance to material temperature. The realationship is determined by manufacturer in 'steinhart' equation
	- *Thermocouple* (TC) uses the Seebeck effect. Temperature differences in different materials can create a voltage, which is compared to a reference. 
- Strain [How to apply strain gauge](https://www.youtube.com/watch?v=qnS0l8deMZo)
	- *Metallic* materials also increase in resistance under strain. They are typically bonded to the substrate, and although they are fairly hardy and cheap, they are somewhat prone to drift. 
	- *Piezoresistive* materials which increase in resistance while under strain. Namely semiconductors
	- *Piezoelectric* materials which generate an electric field when under strain. Can also work the other way (field induces mechanical strain)
- Pressure
	- Generally can use the same principle as strain gauges, plus a few more:
	- *Optical* measures deflection in fiber optic cable
	- *Capacitive* sensors change their capacitance based on deflection. Similar to metallic.

### "C"
- Pressure relief
	- To size relief valves you have to determine your relief rate based on the system. If you are worried about overpressure, what is the maximum rate pressure could be added?
	- Oversizing is better than under, but creates waste and larger response oscillations 