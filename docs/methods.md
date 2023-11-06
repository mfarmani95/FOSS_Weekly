### Table of Contents

1. [Introduction](#introduction)
    - [Soil Moisture Memory](#Soil_Moisture_Memory)
        - [Long-term and short-term memory](#Long-term_and_short-term_memory)


## Introduction
### Soil Moisture Memory
Soil Moisture Memory (SMM) denotes the period from when a perturbation begins to when it ends in the time domain. For instance, in a wet scenario, soil moisture (SM) diminishes due to atmospheric flux exchanges or drainage to deeper soil layers. This water loss process comprises several stages: immediate drainage and runoff when SM is saturated; evaporation at the maximum rate when SM is below saturation but still relatively high; evaporation at a water-limited rate when SM is lower; and cessation of water loss when SM reaches a critically low point. This entire process can be represented as a "Loss Function" which varies based on whether SM is in an energy-controlled state or a water-limited state. Traditional SMM methods using coarse temporal data often blur these stages, hindering model development. However, a newer hybrid method utilizing higher-resolution satellite data discerns between these stages, offering more precise references for model calibration, especially in diagnosing biases in Land-Atmosphere coupling.

<img width="505" alt="image" src="https://github.com/mfarmani95/FOSS_Weekly/assets/83543441/766fd023-15a3-4c1e-b935-c323d103fdfd">

![image](https://github.com/mfarmani95/FOSS_Weekly/assets/83543441/ba43c666-7abe-4ca0-a077-6c13c71a1292)


#### Long-term and short-term memory
The hybrid model, as outlined by McColl et al. (2019), estimates soil moisture memory in both water-limited (long timescales) and energy-limited (short timescales) regimes. For the water-limited phase, like Stage-II ET, a deterministic equation describes the multi-day processes that satellites can measure. In contrast, the energy-limited stage involves faster processes like drainage, runoff, and Stage-I ET, requiring a stochastic model. This model incorporates variables like precipitation occurrence, volumetric soil moisture, and averages over time. Equations within the model provide explicit expressions for both memory types. For the water-limited memory, drydown events, signifying consistent soil moisture reduction, are identified without precipitation data. The assumption is that consistent soil moisture decrease indicates no precipitation. The model then fits the identified drydown events to obtain parameters. Certain criteria, like limiting soil moisture to specific values and filtering events with minimal observation samples, ensure accurate model fitting, aligning with guidelines from McColl, Alemohammad et al. (2017).

<img width="437" alt="Screenshot 2023-11-05 at 8 53 55 PM" src="https://github.com/mfarmani95/FOSS_Weekly/assets/83543441/6f6ad123-81df-443f-bbb4-dd3a53b364e1">

<img width="296" alt="Screenshot 2023-11-05 at 8 53 21 PM" src="https://github.com/mfarmani95/FOSS_Weekly/assets/83543441/fbcf1fc8-00b9-4134-a31c-d67cea0ac524">
