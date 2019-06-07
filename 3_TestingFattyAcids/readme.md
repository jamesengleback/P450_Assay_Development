### Aim
etc

```python
>>> import pandas as pd
>>> data = pd.read_csv('20190607_SubstrateWeighing.csv')
>>> data['mols'] =data[' Actual Weight (mg)']/(data[' Mw']*1000)
>>> data['VolDMSO (mM)']= (data['mols']/0.01)*1000 # convert from L to mL
>>> data['Vol DMSO to add to make 50 mM'] = (data['mols']/0.05)*1000
>>> data
                 Compound      Mw   Actual Weight (mg)      mols  VolDMSO (mL)  Vol DMSO to add to make 50 mM (mL)
0             Lauric acid  222.30                  3.9  0.000018      1.754386                       0.350877
1  Sodium Dodecyl Sulfate  288.40                  7.1  0.000025      2.461859                       0.492372
2           Plamitic Acid  256.42                 19.6  0.000076      7.643710                       1.528742
3        N-Palmitoglycine  313.48                  0.7  0.000002      0.223300                       0.044660
4       4-PhenylImidazole  144.18                 12.6  0.000087      8.739076                       1.747815
5        Arachadonic Acid  304.48                  5.2  0.000017      1.707830                       0.341566
```

Some working for protein cooncentration calcs
```python
>>> nwells = 8*16 #5 compounds, run out of NPG. 1 row of pure protein, 1 row of prot+DMSO 2.5%, 1 row of prot+DMSO 5%
>>> total_assayVol = nwells*1.5*50 #uL, 1.5x safey margin
>>> target_proein_vol = total_assayVol/2
>>> prot_conc = 983.4087522105264

>>> target_proein_vol
4800.0
>>> target_proein_vol*20 # target protein conc is 20 uM
96000.0
>>> 96000.0/prot_conc
97.61963149525488
>>> 

```

Sure messed up there. I'll make the 50 mM aliquots then diute to 10 mM
