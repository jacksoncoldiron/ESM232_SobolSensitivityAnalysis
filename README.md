# ESM232_SobolSensitivityAnalysis
Sobol sensitivity analysis for a model of atmospheric conductance

## Analysis Overview
This assignment extends the sensitivity analysis of atmospheric conductance we practiced in class by adapting it to a new environmental setting:

- Higher wind speeds (mean = 300 cm/s, SD = 50 cm/s)

- Shorter vegetation heights (uniformly distributed between 3.5 and 5.5 meters)

- Small uncertainty in model parameters kd and k0 (1% standard deviation of their defaults).

We will perform a Sobol sensitivity analysis to understand how uncertainty in wind speed, vegetation height, and roughness parameters (kd, k0) affects atmospheric conductance estimates in this new context.

#### Files Provided
*Catm.R:* Contains the original atmospheric conductance model function.

*sobol.qmd:* Introduces the Sobol sensitivity analysis method and an example setup using soboljansen from the sensitivity package.

*sobol_atmcon.qmd*: Iterates on the original sensitivity analysis method to include specified changes

## Instructions for Completing the Assignment
#### Model Setup

1. Use the Catm.R model provided.

2. Update inputs according to the new setting:

- Wind speed: Normal distribution (mean = 300 cm/s, SD = 50 cm/s)

- Vegetation height: Uniform distribution between 350 cm and 550 cm (converted from meters).

- Parameters kd and k0: Normally distributed with 1% standard deviation around default values (0.7 and 0.1, respectively).

#### Sobol Sampling

1. Generate parameter samples using the Sobol method.

2. Define the ranges and distributions for v, h, kd, and k0.

3. Run the Model

4. Calculate atmospheric conductance for each set of sampled parameters.

#### Plotting

1. Plot the distribution of conductance estimates showing parameter uncertainty.

2. Identify the 2nd most influential parameter (by total Sobol index) and plot conductance versus windspeed, colored or faceted by that parameter.

#### Estimate Sobol Indices

Compute and report first-order and total-order Sobol indices for each input parameter.

#### Discussion

Comment on differences in conductance sensitivity compared to the class case:

- Higher windspeed vs. lower

- Shorter vegetation vs. taller

## Notes
Assume default values:

kd = 0.7

k0 = 0.1

Default measurement height above canopy = 200 cm.
