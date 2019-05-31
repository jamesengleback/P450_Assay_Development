# Aim
Previously we saw some light scattering in the plate that may obscure the measurements. The scattering correlated with the volume of 
protein used in the wells (after path length was corrected for) which suggests that thte protein is interacting with the plate
material.

This test is designed to find a plate type that mitigates the scattering effect. I have plate samples from several vendors in [this csv](Inventory.csv)
Down the line, I'll have a tinker with buffer conditions, but surfactants are out because P450 BM3 mutants are known to interact
with these which will give false positives.

# Plan
I'm going to use each of the plate types in my [inventory](Inventory.csv) for this one. My last assay isn't written onto Github
yet but will do soon. 
* Measure the scattering of wild type P450 BM3 heme domain with no substrate 
* Scattering measured by using a derivation of the Rayleigh light scattering equation
* Measurements will be UV-Vis traces taken between 200 and 800 nm

