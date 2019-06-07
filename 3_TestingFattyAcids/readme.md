### Aim
etc

```python
>>> import pandas as pd
>>> data = pd.read_csv('20190607_SubstrateWeighing.csv')
>>> print(data)
                 Compound      Mw   Actual Weight (mg)  
0             Lauric acid  222.30                  3.9  
1  Sodium Dodecyl Sulfate  288.40                  7.1  
2           Plamitic Acid  256.42                 19.6  
3        N-Palmitoglycine  313.48                  0.7  
4       4-PhenylImidazole  144.18                 12.6  
5        Arachadonic Acid  304.48                  5.2  
>>> data['mols'] =data[' Actual Weight (mg)']/(data[' Mw']*1000)
>>> data['VolDMSO (mM)']= (data['mols']/0.01)*1000 # convert from L to mL
>>> data
                 Compound      Mw   Actual Weight (mg)      mols  VolDMSO (mM)
0             Lauric acid  222.30                  3.9  0.000018      1.754386
1  Sodium Dodecyl Sulfate  288.40                  7.1  0.000025      2.461859
2           Plamitic Acid  256.42                 19.6  0.000076      7.643710
3        N-Palmitoglycine  313.48                  0.7  0.000002      0.223300
4       4-PhenylImidazole  144.18                 12.6  0.000087      8.739076
5        Arachadonic Acid  304.48                  5.2  0.000017      1.707830
```
