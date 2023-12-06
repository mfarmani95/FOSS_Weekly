### Table of Contents

1. [Introduction](#introduction)
    - [Soil Moisture Memory](#Soil_Moisture_Memory)
        - [Long-term and short-term memory](#Long-term_and_short-term_memory)


## Introduction
### Soil Moisture Memory
Soil moisture memory (SMM) refers to the time for a perturbation to dissipate or the time between a perturbation starts and ceases in the time domain. To illustrate, when a precipitation occurs and the near-surface soil moisture increases, start of the perturbation, the increased moisture will diminish gradually due to evaporation to atmospheric, flux exchange, or draining to the deeper soil. So the loss of water is consist of several stages respectively: 1) right after precipitation occurrence and saturating the surface soil moisture, the soil is not capable of keep water (having water higher than field capacity, θ_fc) and so the surface runoff and drainage happens; 2) having intermediate soil moisture, belove the θ_fc and above the critical point, θ_c, in this situation the moisture in the soil is higher the potential evaporation, hence the evaporation happens in the maximum rate, called Stage-I ET; 3) as the evaporation continues and the moisture available in the soil goes below the critical point, the water available in the soil is lower than potential evaporation, the evaporation happens in water-limited rate which is determined by SM, named as Stage-II ET; 4) finally, the loss of water will be stopped as the SM goes below the soil wilting point θ_w. As explained the whole process of losing water by soil, Loss Function, can be considered as function as SM, which can be divided into two major categories, energy-limited and water-limited, Figure 1.
The energy-limited processes, which encompass drainage and stage-I ET, occur on timescales ranging from hours to a few days. Conversely, water-limited processes unfold over longer durations, including weekly, monthly, and seasonal timescales. Conventional methodologies for quantifying soil moisture memory, predicated on the principles of the Markov process and often constrained by coarse temporal resolution data, typically conflate these two distinct hydrometeorological phenomena—energy and water limitations. The innovative hybrid model formulated by McColl et al. (2019), however, proficiently differentiates the memory associated with each regime by incorporating three-day soil moisture data from the SMAP satellite. This nuanced Soil Moisture Memory (SSM) approach provides a robust benchmark, thereby substantially improving the capacity of Land Surface Models (LSMs) to calibrate their parameterizations of soil moisture dynamics under diverse environmental conditions.
<img width="535" alt="image" src="https://github.com/mfarmani95/FOSS_Weekly/assets/83543441/fa3a1f3f-aed7-47f6-86fc-8f86c3192d13">
Figure 1 Schematic diagrams of (a) surface water loss process and (b) soil moisture memory at different soil moisture regimes [adapted from (McColl et al. 2017b)]. Note that the x-axis in panel (a) refers to SM (m3m−3), and y-axis refers to surface water lose rate, L(𝜃) (mm/s) ; Emax is the maximum evaporation rate (mm/s ). In panel (b), x-axis refers to time (e.g., days) and y-axis refers to SM content (m3m−3). 𝜃𝑤 , 𝜃c, and 𝜃fc refers to the wilting point, critical point, and field capacity, respectively.

We expound upon the concept of soil moisture memory as it pertains to two distinct regimes: the water-limited regime (τ_L), where 'L' denotes the protracted temporal scale that is characteristic of water-limited processes, and the energy-limited regime (τ_S), with 'S' indicating the abbreviated temporal scale inherent to energy-limited processes. This delineation is grounded in the framework proposed by McColl et al. (2019). Their hybrid model integrates a deterministic equation to faithfully represent the water-limited process, which benefits from the extended temporal span that satellite datasets can monitor and reflect. In contrast, the energy-limited process, constrained by a narrower temporal window, poses significant observational challenges for current satellite technologies to accurately characterize. To address this gap, McColl et al. (2019) introduced a stochastic equation tailored to encapsulate the dynamics of this transient process, thereby providing a robust methodology to elucidate the intricacies of this energy-limited regime that were previously unresolved.  The hybrid model is as follow:


(dθ(t))/dt= {█(-(θ(t)-θ_w  )/τ_L ,                P=0@-(θ(t)-θ ̅  )/τ_S + ε(t),      P>0  )┤![image](https://github.com/mfarmani95/FOSS_Weekly/assets/83543441/5f5d09de-08c8-4591-aacf-6aa48c728482)


where, θ is the volumetric soil moisture, P indicates the occurrence of precipitation, θ_w is a minimum soil moisture, θ ̅ is the time average SM, and ε(t) is an independent and identically distributed random variable with a mean of zero, τ_L and τ_S are SSM for the water-limited and energy-limited regimes, respectively. McColl et al. (2019) solved the equations and showed that the memories can be expressed as:

θ(t)= ∆θ exp(- t/τ_L )+ θ_w            P=0	(2)
τ_S  = -(∆t/2)/log((∆z [(〖∆θ〗_+ ) ̅ ])/α)                    P>0	(3)

where, ∆θ is equal to the SM changes during the drydown event, ∆t is the temporal resolution of the SM data, α refers precipitation intensity, and (〖∆θ〗_+ ) ̅  = θ(t) - θ(t-∆t) refers to a positive increment in soil moisture. 

In the analysis of water-limited memory, we employed Equation 2, fitting it to the soil moisture time series over a specified drydown interval, thereby extracting τ_L as a parameter intrinsic to the fit. In contrast, short-term memory was ascertained directly from the application of Equation 3. For the computation of long-term memory, which operated under the presumption of no precipitation, soil moisture data was considered as the primary input. However, to accurately assess the memory from the energy-limited stage, it was necessary to combine both rainfall and soil moisture data to completely understand the complex interactions that controlled this phase.

It should be mentioned that as it is specified by He et al.(2023), the terms "water-limited" and "energy-limited" are used with some flexibility, as their definitions are not absolute. It is conceivable, for instance, that Stage-I ET might take place during periods of soil drying even in the absence of rainfall. There is also the potential for Stage-I ET to occur between consecutive rainfalls without the soil reaching to the critical point θ_c, which could happen in extreme humid climate regions. Furthermore, the absence of precipitation data in this method to detect soil drydown periods introduces the possibility of misidentification. Rainfall that occurs within the 2-3 day gaps between satellite soil moisture observations could be overlooked, leading to a scenario where subsequent readings indicate a decrease in soil moisture, despite the actual occurrence of rainfall shortly after the preceding measurement.
![image](https://github.com/mfarmani95/FOSS_Weekly/assets/83543441/8da64fa0-2d21-48ce-93a1-26dfd453667a)




#### Long-term and short-term memory
The hybrid model, as outlined by McColl et al. (2019), estimates soil moisture memory in both water-limited (long timescales) and energy-limited (short timescales) regimes. For the water-limited phase, like Stage-II ET, a deterministic equation describes the multi-day processes that satellites can measure. In contrast, the energy-limited stage involves faster processes like drainage, runoff, and Stage-I ET, requiring a stochastic model. This model incorporates variables like precipitation occurrence, volumetric soil moisture, and averages over time. Equations within the model provide explicit expressions for both memory types. For the water-limited memory, drydown events, signifying consistent soil moisture reduction, are identified without precipitation data. The assumption is that consistent soil moisture decrease indicates no precipitation. The model then fits the identified drydown events to obtain parameters. Certain criteria, like limiting soil moisture to specific values and filtering events with minimal observation samples, ensure accurate model fitting, aligning with guidelines from McColl, Alemohammad et al. (2017).

<img width="437" alt="Screenshot 2023-11-05 at 8 53 55 PM" src="https://github.com/mfarmani95/FOSS_Weekly/assets/83543441/6f6ad123-81df-443f-bbb4-dd3a53b364e1">

<img width="296" alt="Screenshot 2023-11-05 at 8 53 21 PM" src="https://github.com/mfarmani95/FOSS_Weekly/assets/83543441/fbcf1fc8-00b9-4134-a31c-d67cea0ac524">

## references
Mccoll, Kaighin A., Qing He, Hui Lu, and Dara Entekhabi. 2019. “Short-Term and Long-Term Surface Soil Moisture Memory Time Scales Are Spatially Anticorrelated at Global Scales.” Journal of Hydrometeorology 20(6):1165–82. doi: 10.1175/JHM-D-18-0141.1.

McColl, Kaighin A., Wei Wang, Bin Peng, Ruzbeh Akbar, Daniel J. Short Gianotti, Hui Lu, Ming Pan, and Dara Entekhabi. 2017b. “Global Characterization of Surface Soil Moisture Drydowns.” Geophysical Research Letters 44(8):3682–90. doi: 10.1002/2017GL072819.
![image](https://github.com/mfarmani95/FOSS_Weekly/assets/83543441/77fca300-442a-4e34-af25-813d6c86dfd5)
