# Radiant_
This is a thermal radiation model for combustion systems using the Monte-Carlo ray tracing method. This solver couples to OpenFOAM, uses GPUs for acceleration, and includes line-by-line non-gray modeling including the contributions of many common chemical species used in combustion. Please visit [Prof. Xinyu Zhao's homepage](https://ctfzhao.com/codes/) for details on how to access the code.


## Capabilities
This solver is built on top of the fireFoam, reactingFoam, and buoyantReactingFoam solvers in OpenFOAM, and for OpenFoam versions 5, 7, 9 and 10. This enables simulations from wildfires to rocket and jet engines.

The code operates by evaluating a timestep using the OpenFoam solver with volumetric energetic contributions evaluated from Radiant. Additionally, wall emission and absorption are accounted for with the gray body approximation. 

Currently, the solver provides 0.01 1/cm wavenumber resolution in the infrared and visible spectral ranges. Emission profiles include contributions from CO2, H2O, CO, CH4, C2H2, C2H4, C2H6, and soot evaluated from the HITEMP and HITRAN spectroscopic databases.
