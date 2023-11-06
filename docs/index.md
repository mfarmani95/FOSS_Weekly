#  🟢 Objectives of the project

    *  Implementing the new parametrization of Noah-MP and assessing its accuracy in representing soil moisture
    *  Increase the accuracy of streamflow estimation in arid regions during the dry periods
    *  Increase the accuracy of transpiration and evapotranspiration estimation

## What is the problem?
Many land surface models tend to overestimate soil moisture across CONUS. Soil moisture serves as a memory mechanism for the soil and directly influences both rainfall and streamflow


![Average soil moisture](https://github.com/mfarmani95/FOSS_Weekly/assets/83543441/33f93ea3-dadc-4830-8553-eb34a6656c0f)

## So what is wrong with it? 🤔
Having more moisture in the soil than the reality would lead to generation of unrealistically higher streamflow and baseflow. Since the soil water water content is directly related to the to main way of streamflow generations, ❗Infiltration excess and saturation excess❗
Now, consider this situation, in which higher soil moisture is estimated for surface soil moisture in an arid region 🔴
If the surface soil is already saturated or near saturation (high soil moisture content due to overestimation), it has a reduced capacity to absorb additional rainfall. This can lead to increased infiltration excess and, subsequently, more surface runoff.
In other words, models generate some streamflow that doesn't exist in reality.

![image](https://github.com/mfarmani95/FOSS_Weekly/assets/83543441/888c7d8f-073b-459c-8f72-152df8ffa309)





