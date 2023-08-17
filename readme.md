## GALAXY PROPERTIES PROJECT

Final Project - PHYS 3600ID Fall 2022

### GUIDELINES

The data are simulated (but realistic) spectra of galaxies at redshift = 1 (corresponding to an epoch of about 5 billion years in the past - those are far!), and our goal is to learn how to predict different physical properties of the galaxies.

Our learning set is made of 1,000 galaxies (note: I might get more if needed!). For each galaxy, our information consists of 850 measurements of the brightness (measured in a funny unit called microJansky) at 850 wavelengths, between 1,995 Angstrom and 100,000 Angstrom, which in layman terms correspond to ultraviolet (UV) to infrared (IR). These are available in the file:

> spectra.csv

Summarizing, we have 850 features for each object. The wavelengths corresponding to each feature (which are not needed for building the Machine Learning model), but are needed to plot spectra are also available in a separate file:

> wavelengths.csv

Our goal will be to learn how to predict some properties of the galaxies from their spectra, in particular:

**Age:** how long ago did the galaxy form its first stars?

**Tau:** (a bit difficult to explain, so let's use this simple version) A parameter, also expressed in the units of time, which describes how fast/slow the process of star formation proceeds.

**Stellar Mass:** the total amount of mass in stars (because we know there is also gas and dark matter, right)? Usually expressed in units of the mass of the Sun so we don't have to deal with very large numbers.

**Dust (A\_v):** Amount of cosmic dust in a galaxy, measured as the diminishing of optical light (since dust absorbs optical waves).

These four quantities are available for each galaxy in the learning set in the file:

> GalaxyProperties.csv

Our targets are the four properties described above. For age and tau, the units are Gyr (Giga years, aka billions of years). For dust, the units are magnitudes of obscuration (roughly, an amount of 0.1 corresponds to a reduction in brightness of 25%). For mass, the units are log 10 of stellar mass in Solar units, so a number = 8 means that the galaxy's mass is 108 MSun.

\* We will build/optimize four different regression models to predict the four targets.

---

#### What we will perform

1. Visualize data (at least a few spectra) to get a sense of how they look.

2. Choose which algorithm we will use for this problem.

3. Explore data and pre-process, if needed.

4. Build a reference model and use cross-validation to estimate how well it performs.

5. Diagnose, optimize and repeat!

6. Conclude the "best model" and discuss its results

7. Repeat 1-6 as needed for each of the four targets, draw appropriate comparisons.

---

#### Notes

- Two of these properties will be easier to predict (there is a good correlation between truth and predictions), and two will be harder, and will require more fiddling around.

- There is a lot of noise.


