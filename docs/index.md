#  🟢 Objectives of the project

    *  Implementing the new parametrization of Noah-MP and assessing its accuracy in representing soil moisture
    *  Increase the accuracy of transpiration and evapotranspiration estimation
    *  Increase the accuracy of streamflow estimation in arid regions during the dry periods    

## What is the problem?
Many land surface models tend to overestimate soil moisture across CONUS. Soil moisture serves as a memory mechanism for the soil and directly influences both rainfall and streamflow


![Average soil moisture](https://github.com/mfarmani95/FOSS_Weekly/assets/83543441/33f93ea3-dadc-4830-8553-eb34a6656c0f)


## So what is wrong with it? 🤔


When the soil retains more moisture than is realistically present, it can lead to the generation of artificially elevated streamflow and baseflow. This is because soil water content is intrinsically linked to the two primary mechanisms of streamflow generation: ❗ Infiltration excess and Saturation excess❗

Imagine a scenario where an arid region's surface soil moisture is overestimated. If this surface soil approaches or reaches saturation due to such overestimation, its capacity to absorb subsequent rainfall diminishes. This condition can amplify infiltration excess, resulting in increased surface runoff. Essentially, this means models might portray streamflow values that diverge from true conditions.🔴


![image](https://github.com/mfarmani95/FOSS_Weekly/assets/83543441/888c7d8f-073b-459c-8f72-152df8ffa309)


<img width="1460" alt="Screenshot 2023-11-05 at 8 23 01 PM" src="https://github.com/mfarmani95/FOSS_Weekly/assets/83543441/d68799e9-5624-417e-8d30-12f7c62c5f44">



