# T2_INTERPOLATION
INTERPOLATION OF T2 RELAXATION TIME IN THE ECHO MODULATION CURVE FIT ALGORITHM  SIMULATION DATABASE FOR A MULTI-SE PROTOCOL

## INTERPOLATION OF T2 RELAXATION TIME IN THE ECHO MODULATION CURVE FIT ALGORITHM


![alt text](https://github.com/laureneb26/T2_INTERPOLATION/blob/main/T2INVIVO.png)

## SIMULATION DATABASE FOR A MULTI-SE PROTOCOL

_Assumptions : In this work, we will assume a perfectly homogeneous magnetic field B1, as well as T
relaxation time fixed to a specific value._

**INTRODUCTION/ENVIRONMENT :**
Nowadays, T2-relax-based contrast is widely used for non-invasive diagnosis. Unfortunately, this only
allows visually qualitative mapping. We would rather be intereseted into getting the actual values of the
T2 relaxation times in order to get T2-mapping.
Although quantitative T2-mapping through single-echo SE has demonstrated merit for various
applications, it stills remains challenging in the case of the guenine to get T2 relaxation time values.

In the case of a single-echo SE, the signal decays exponentially (so called FID=free indcution decay) and so
will be used as values of reference for our research.
Despite its benefit of reducing the diffusion effect, Multi-echo SE bring into play side effects/parameters
that will distort the decay form of the signal. Among them, the strong signal contamination that splits the
signal into three coherence pathways (leading to indirect echoes, and consequently deviation from the
correct T2 values).
Therefore, we won’t be able to consider the exponential decaying form of the signal and we will have to
perform simulations under the EMC fit algorithm to get the corresponding T2 relaxation time values. Note
that multi-echo SE consequently elongates the T2 curve (because of the echoes due to refocusing pulses
at FA (=flip angles) chosen in a range around an optimal value of 180 degree).
It has been desmontrated that the EMC fit algorithm get optimal matching T2 results (high accuracy and
precision) for our purpose (see reference 3).
However, simulations are very impractical in the sense of computational time efficiency.

**PURPOSE :**
Investigate an interpolating model for T2 relaxation times as a function of echo train length (ETL) only.
We will assume that the rotating magnetic field B1 is homogoneous and that T1 relaxation time is fixed.
Our goal is to define an interpolation in T2 vaues that will be less time consuming than the appropriate
simulations.

**METHODS:**
We will explore the EMC curves in order to define an interpolation pattern for the T2 values, thus saving
consequent computational time in simulations.
We expect a non-linear scale interpolation (or partially linear) since the decay behaves similar to an
exponential form :a difference ∆𝑡 bewteen small time values will lead to significant change in the echo
amplitude compared to the same difference applied to higher times (due to log scale).
We thus need to investigate for an appropriate and non-uninform interpolation.

- Analysis of the data base (5D dimensions will be restriced to T2 values only) on a brain
    sample
- Interpolation model tests in Matlab
- Calculation of relative error between the interpolated values and the ones from the
    database.
    1.Number of interpolated lines should be maximized
    2. The relative error between the interpolation to the actual simulated datas should not
    overcome the actual measurement error (ideally, order of magnitude less, not same range).

**RESOURCES :**

- Graphical User Interface (GUI)
- Matlab software
- Rapid and Accurate T2 Mapping from Multi-Spin-Echo Data Using Bloc-simulation-Based Reconstruction
paper (Noam Ben-Eliezer, Daniel K.Sodickson, Kai Tobias Block).


