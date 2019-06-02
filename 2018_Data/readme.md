# Preliminary Experiments!
## TL;DR
Experiments that looked at some assay parameters. The tests revealed a problem with light scattering hat may obscure some important data, which is probably because the protein is precipitating because of some interaction with the plastic assay plate.

## Contents
* Aim of the experiments
* Parameters being tested
* Method
* Results and analysis


### Aim of the experiments
These experiments are to make a version of a classical P450 binding tiration in a plate. Classical titrations iteratively add test compounds to a cuvette, mix and then record the changes in the UV-Vis absorbance profile. Changes at 390 and 420 nm are used to calculate the dissosciation constant,*K* ~d~.

At the ime of designing these experiments, I was set on using a factorial-style design, which is [here](2018_Data/20180924-FullFatDesign.csv). I was messing with:
* Vol/µl
* Prot/µM 
* No. Concs (of substrate)
* and a power constant

My end point was going to be the standard deviation of *K* ~d~, which I am trying to minimize. I tried this plate system out in 384 and 1536 well plates

![distributions](https://github.com/jamesengleback/P450_Assay_Development/tree/master/2018_Data)
