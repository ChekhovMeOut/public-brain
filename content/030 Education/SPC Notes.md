---
{"publish":true,"created":"2025-03-25T11:18:37.000-05:00","modified":"2025-09-12T23:40:35.653-05:00","cssclasses":""}
---

### References
- https://www.qimacros.com/pdf/histogram-cheat-sheet.pdf
- https://sixsigmastudyguide.com/process-capability-pp-ppk-cp-cpk/
- https://www.qimacros.com/lean-six-sigma-articles/stability-analysis-vs-capability-analysis/
- https://pressbooks.palni.org/spcleanmanufacturing/chapter/chapter-10a/


- **Process stability** is when the process is is consistent, and any noise in the output is due to standard variation. If it is unstable, that means there is some special cause variation
	- This is assessed using control charts. Which one you use depends on data. These are for numerical values:
		- X-chart is plotting the mean of each subgroup, over subgroup count. UCL and LCL are 3 sigma of all subgroup averages. This is the alternative to I-MR charts.
		- I-MR chart is plotting individual data points over time. The UCL and LCL are the moving range at each point. This is the alternative to x-charts.
		- R chart is plotting the subgroup range over subgroup count. This is usually presented with X-bar, not on its own. It shows sample dispersion, and is best when sample size is low (n < 10). 
		- S chart is plotting the subgroup deviation over subgroup count. This is usually presented with X-bar, not on its own. It shows sample dispersion, and is best when sample size is high (n > 10). 
	- These control charts are for attribute data:
		- P-chart
		- U-chart
		- C-chart

- **Process capability**: can the process can meet the product requirements outputs? 
	- Process capability indexes are when you are looking at a subset of the data, like a subgroup or comparing improvements. Uses a sigma estimation. 
		- **Assumes & requires that process is stable**
		- $C_p$ (Capability Index) - how spread is data between the LSL and USL?
		- $C_pk$ (Capability Centering Index) - how centered is data between the LSL and USL?
	- Process performance indexes are when you are looking at a the entire set of data, like handing off a batch of wafers to the customer. Uses normal SD.
		- **Process does not need to be stable**
		- $P_p$ (Performance Index) - how spread is data between the LSL and USL?
		- $P_pk$ (Performance Centering Index) - how centered is data between the LSL and USL?
	- Interpreting $P_p,\;P_pk,\;C_p,\;C_pk$
		- $0 ≤ incapable < 1.0$
		- $1.0 ≤ barely\;capable < 1.33$
		- $1.33 ≤ moderately\;capable < 2.0$
		- $2.0 ≤ highly\;capable$