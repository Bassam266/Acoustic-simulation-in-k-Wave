# Acoustic Simulation in k-Wave

A set of 1D k-Wave simulations exploring the limits of measuring thin-film thickness and acoustic/mechanical properties using the time-of-flight (ToF) and pulse-echo methods.

## Simulation 1 — Time-of-Flight Limitations

The first simulation studies the limitations of measuring thin-film thickness and acoustic/mechanical properties using the ToF. It helps us understand how different acoustic impedances — arising from different polymer layers — influence the time of flight, and how this links to the ultrasound frequency.

**Script:** `Pulse_echo_Simulation_water_glass_film_glass_1.m`

<p align="center">
  <img src="Image_1.png" width="60%" /><br>
  <em>Figure 1 — Time-of-flight simulation for a water–glass–film–glass stack.</em>
</p>

## Simulation 2 — Influence of the Polymer Film on the Reflected Echo

The second simulation focuses on the influence of the thin polymer layer on the reflected echo. The result is compared against a reference (a glass substrate) and tested across different sampling rates.

**Script:** `MultiLayerSimulation_2.m`

<p align="center">
  <img src="Image_2.png" width="60%" /><br>
  <em>Figure 2 — Reflected echo from the polymer film compared with the glass reference.</em>
</p>

## Simulation 3 — Spring-Model Thickness Measurement

The third simulation uses a **spring model** to measure the thin polymer film with the pulse-echo method, implemented as described in the following paper:

> Dwyer-Joyce et al., *The measurement of lubricant film thickness using ultrasound*, Proc. R. Soc. Lond. A **459** (2032), 957–976.
> https://royalsocietypublishing.org/doi/10.1098/rspa.2002.1018

The k-Wave results are comparable to the original results from the paper, as shown below.

<p align="center">
  <img src="Image_3.jpg" width="60%" /><br>
  <em>Figure 3 — k-Wave spring-model results compared with the reference paper.</em>
</p>

Two simulations are performed:

1. **Reference simulation** — collects the echo from the second interface of the glass.
2. **Film simulation** — collects the echo from the glass–film interface; the echo amplitude changes slightly with the thickness of the film.

The strength of this method is that it can measure a thin film using ultrasound waves in the tens-of-MHz range — but it requires the density and the sound velocity of the thin film for the calculation.

**Script:** `Kwave_simulation_with_Spring_model.m`

> **Note:** Always remember to add the k-Wave toolbox to your MATLAB path.
