The general workflow for building an adult PBPK model has been described by Kuepfer et al. ([Kuepfer 2016](#5-references)). Relevant information on the anthropometry (height, weight) was gathered from the respective clinical study, if reported. Information on physiological parameters (e.g. blood flows, organ volumes, hematocrit) in adults was gathered from the literature and has been incorporated in PK-Sim® as described previously ([Willmann 2007](#5-references)). The  applied activity and variability of plasma proteins and active processes that are integrated into PK-Sim® are described in the publicly available 'PK-Sim® Ontogeny Database Version 7.3' ([PK-Sim Ontogeny Database Version 7.3](#5-references)).

A stepwise approach was used to fit the model to data.

1. Define distribution model, cellular permeability, renal and metabolic clearance on data after single i.v. administration. For this purpose, literature values from [Mexiletine, Drugs.com](#5-references) were derived for renal CL and CYP2D6 combined with CYP1A2 metabolic clearance, or total hepatic CL, fitted against the data.

2. Define intestinal permeability and fraction absorbed by fitting the model against data after p.o. single dose administration ([Pringle 1986](#5-references)). Investigate multiple oral doses predictions in CYP2D6 extensive and poor metabolizers ([Labbé 2000](#5-references)).

The predefined “Standard European Male for DDI” individual (age = 30 y, weight = 73 kg, height = 176 cm, BMI = 23.57 kg/m2) with added CYP2D6 expression obtained from PK-Sim RT PCR database was used if not stated otherwise. For simulations of Japanese subjects ([Kusumoto 1998](#5-references)), a typical Japanese individual (age = 30 y, weight = 61.87 kg, height = 168.99 cm, BMI = 21.67 kg/m2) was created in PK-Sim from predefined database “Japanese (2015)” by adding CYP1A2 and CYP2D6 expression from PK-Sim RT PCR database.

For simulations of CYP2D6 PM, the CYP2D6 pathway has been switched off.

Population simulation of single 83 mg p.o. administration was conducted to visually compare the predicted concentration-time profiles to the observed concentrations reported in the literature, in terms of mean and variability. A population of 1000 male individuals was generated based on “Standard European Male for DDI”. Age range was limited to 20-40 years.

Details about input data (physicochemical, *in vitro* and clinical) can be found in [Section 2.2](#22-data).

Details about the structural model and its parameters can be found in [Section 2.3](#23-model-parameters-and-assumptions).
