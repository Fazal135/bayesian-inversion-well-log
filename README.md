# Bayesian Inversion of Well Logs

This project estimates porosity and lithology volumes (sandstone, shale, limestone) from well log data using Bayesian inversion. I used a real well from Kansas and followed the method from a 2017 CGS/SEG research paper.

##  What This Project Is About

I worked with well log data from a shaly-sand reservoir and applied Bayesian inversion to estimate subsurface properties. The main idea is to combine well log measurements with prior knowledge (from core samples) to get better, uncertainty-aware estimates of porosity and rock composition.

## Tools & Libraries Used

- Python
- NumPy
- SciPy
- Matplotlib
- lasio (for reading `.las` well log files)

##  What I Did (Step-by-Step)

1. Loaded the `.las` well log data using `lasio`
2. Focused on logs like gamma ray, bulk density, acoustic travel time, and neutron porosity (3600–3650 ft)
3. Checked if the formation was a shaly-sand (it was)
4. Defined a petrophysical model (porosity, sandstone, shale, limestone)
5. Used the Bayesian inversion formula to estimate model parameters
6. Plotted results — both estimates and their uncertainties
7. Showed how Bayesian inversion reduces uncertainty using prior info + data


## Summary

The Bayesian inversion not only provided realistic estimates of porosity and rock volumes but also significantly reduced uncertainty — by **72.7% in porosity**, **30.1% in sandstone volume**, **14.7% in shale**, and **13.8% in limestone** — making the results much more reliable for interpretation.

