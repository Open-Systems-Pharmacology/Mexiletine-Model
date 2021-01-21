### 2.3.1 Absorption

Gastrointestinal permeability was fitted to concentration data after single dose oral administration.

The default dissolution Weibull profile (`Dissolution time (50% dissolved)` = 60min, `Dissolution shape` = 0.92) was used for description of formulation.

### 2.3.2 Distribution

Physico-chemical parameters were set to the reported values (see [Section 2.2.1](#2.2.1-In-vitro-and-physico-chemical-data)). It was assumed that the major binding partner in plasma is albumin.

Because mexiletine is a strong base, permeation across the barriers between interstitial space and intracellular space (cellular permeability) had to be adjusted manually, as only uncharged molecules can pass through membranes, which is not accounted for by the permeability calculated by PK-Sim. The parameters `Specific organ permeability` and `Lipophilicity` defining the distribution in tissues were fitted to i.v. data.

After testing the available organ-plasma partition coefficient and cell permeability calculation methods available in PK-Sim, observed clinical data were best described by choosing the partition coefficient calculation by `Rodgers and Rowland` and cellular permeability calculation by `PK-Sim Standard`.

### 2.3.3 Metabolism and Elimination

Following metabolization and elimination processes are implemented:

- Linear CYP1A2, with specific clearance set to 28.6% of estimated total Liver Plasma Clearance (according to [Labbé 2000](#5-References))
- Linear CYP2D6, with specific clearance set to 37.1% of estimated total Liver Plasma Clearance (according to [Labbé 2000](#5-References))
- Liver plasma clearance,  with specific clearance set to 34.3% of estimated total Liver Plasma Clearance (according to [Labbé 2000](#5-References))
- Kidney plasma clearance with plasma clearance value set to reported value (see [Section 2.2.1](#2.2.1-In-vitro-and-physico-chemical-data))

The model has been developed with kidney and liver plasma clearances only, without separating between the different enzymes. The parameter `Specific clearance` of the total hepatic clearance was estimated by fitting the model to observed data (see [Section 2.2.2](#2.2.2-Clinical-data)). The parameters `Specific clearance` of the linear CYP1A2 and CYP2D6 metabolization processes have been calculated from from the total hepatic clearance by multiplying the identified total hepatic clearance by the reported percentage contribution of the respective enzyme and dividing by the `Reference concentration` of the respective enzyme as given by the PK-Sim database (1.8 µmol/l for CYP1A2 and 0.4 µmol/l for CYP2D6). This is necessary as the `Specific clearance` is multiplied by the concentration of the enzymes in the respective organ, with reference concentration of the dummy enzyme used in the total hepatic clearance being 1 µmol/l per default. With the applied parameter values, CYP1A2 in the liver is responsible for 25% of total mexiletine metabolization, while CYP2D6 in the liver is responsible for 33% of total metabolization. Additional metabolization by CYP2D6 takes place in intestinal mucosa, though to a minor extent.

### 2.3.4 Automated Parameter Identification

Following parameter values were estimated for the model:

- `Specific clearance` (Total hepatic clearance)
- `Specific organ permeability`
- `Lipophilicity`
- `Plasma clearance` of total Liver Plasma Clearance (divided between three processes in final model)
- `Intestinal permeability (transcellular)`
