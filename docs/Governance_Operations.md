# Governance and Operations Document

*This is a living document. Changes are expected throughout the life of the project.*

### Table of Contents

1. [Introduction](#introduction)
    - [Project Overview and Objectives](#project-overview-and-objectives)
        - [Noah-MP](#Noah-MP)
        - [Noah-MP Reference Hub](#Noah-MP-Reference-Hub)
    - [Our Team](#our-team)
        - [Organizational Structure](#organizational-structure)
2. [Operations](#operations)
    - [Communications](#communications)
    - [Procedures](#procedures)
3. [Community Practices](#community-practices)
    - [Open Science Commitment](#open-science-commitment)
    - [Land Acknowledgement](#land-acknowledgement)
    - [Diversity Statement](#diversity-statement)
    - [Code of Conduct](#code-of-conduct)
4. [Attribution, Authorship, and Ownership](#attribution-authorship-and-ownership)

## Introduction

The Project Governance guideline outlines operational protocols and regulations designed to elucidate and bolster NOAHMP improvement and its reference hub.

### Project Overview and Objectives

The complex processes of soil moisture dynamics pose significant challenges in understanding climatic, hydrologic, and ecosystem interactions. Many land surface models (LSMs) tend to overestimate surface soil moisture, soil surface evaporation, while underestimating soil surface drying rate. This study focuses on improving the representation of soil moisture dynamics and enhancing the partitioning of evapotranspiration (ET) into transpiration (T) and evaporation (E) to strengthen ecosystem resilience. We leverage SMAP (Soil Moisture Active Passive) observations to improve the Noah-MP LSM over the US continent.

#### Noah-MP

Noah-MP is a widely-used state-of-the-art land surface model used in many research and operational weather/climate models (e.g., HRLDAS, WRF, MPAS, WRF-Hydro/NWM, NOAA/UFS, NASA/LIS, etc.)
The official Noah-MP land surface model unified repository for code downloading and contribution is https://github.com/NCAR/noahmp. Noah-MP is a community open-source model developed with the contributions from the entire scientific community. For development, maintenance, and release of the community Noah-MP GitHub code, please contact: Cenlin He (cenlinhe@ucar.edu) and Fei Chen (feichen@ucar.edu).

#### Noah-MP Reference Hub

Noah-MP model website: https://ral.ucar.edu/solutions/products/noah-multiparameterization-land-surface-model-noah-mp-lsm

### Our Team

Meet the executive team:

- **Guo-Yue Niu**: Niu has been an associated professor at the Department of Hydrology and Atmospheric Sciences (HAS) since 2019 Fall. He has served as the Director of the UA Hydrometeorology Program since 2014. He joined HAS in 2013 Fall as an assistant professor and joined Biosphere 2 as an assistant research professor, The University of Arizona since the fall 2009. He has been working on developing processe-based hydrometeorological and ecohydroligcal models for use in global-scale Earth system models and evaluating the impacts of climate change on ecohydrological processes at catchment scales. He obatined his PhD at the Chinese Academy of Sciences (CAS) in 1996. His major research interests are hydrometeorology, ecohydrology, land surface modeling, distributed hydrological modeling, global and regional climate modeling, and application of remote sensing to modeling. He earned the CCSM (Community Climate System Model) distinguished achievement award by the National Center for Atmospheric Research (NCAR) in 2008 for his work on developing a novel surface water and groundwater model for use in CCSM and "Xuedu Fengzheng" best dissertation award by CAS in 1996. 
- **Ali Behrangi**: I joined the Department of Hydrology and Atmospheric Sciences at the University of Arizona as an associate professor in January 2018.  My doctoral work at the University of California, Irvine was on developing high-resolution precipitation products using satellite images and my postdoctoral work at California Institute of Technology (Caltech) and Jet Propulsion Laboratory (JPL) was on analysis of cloud and precipitation products from multiple sensors. As a NASA JPL scientist (2012-2018)  I was involved in several projects (as principal investigator or co-investigator) on various topics including precipitation retrieval, pathfinder for microwave sounding instrument, tropical cloud and precipitation, water and energy budget studies, GRACE based water storage anomaly, hydrologic modeling, extreme weather and climate studies, mission concept and proposal development, and using diverse data sets across multiple disciplines to quantify precipitation amount and distribution over cold regions(https://behrangi.faculty.arizona.edu/).
- **Mohammad Farmani**: I am Mohammad Farmani, a Ph.D. student in Hydrology and Atmospheric Sciences department at the University of Arizona. I received my BS in Civil Engineering from Iran University of Science and Technology and MS in Water Resources Management from Tarbiat Modares University. My academic journey has been characterized by a strong passion for comprehending the complexity of the natural world, with a specific focus on land-atmosphere interactions, urban flooding, and the application of machine learning and deep learning methods. My current research is centered around advancing our understanding of infiltration processes to enhance the accuracy of streamflow estimation.  

#### Organizational Structure

```
NOAH-MP/SMAP team
├── NOAH-MP team
│   ├── Guo_Yue Niu
│   └── Mohammad Farmani
├── Remote sensing team
    └── SMAP
         ├── Ali Behrangi
         └── Mohammad Farmani

```

## Operations

In order to ensure well distributed work loads across FOSS and the FOSS teaching materials including the FOSS Reference Hub, we have outlined communications and procedure components in order to maximize effectiveness and efficiency.

### Communications

**Internal communications**: communications within the CyVerse/Data Science Institute team is carried out through private Slack channels (CyVerse, CyVerseLearning, Data7) and Zoom meetings.

**External communications**: communications to the dplPy team is carried out through a private Slack channel (openDendro), whilst communication to the guest speakers is done through email (Wade Bishop) and the CyVerse/CyverseLearning Slack Channel (Jason Williams).

**Note keeping & attendees**: communications to FOSS attendees is achieved through the CyVerseLearning Slack channel. This will allow attendees to share thoughts and notes on lectures and materials during and after the workshop. Note keeping during the workshop is carried out through [HackMD](https://hackmd.io/), which links are shared during the workshop sessions. All workshops will be done through Zoom, creating a virtual classroom environment allowing remote attendees to take part to the workshop. Recordings of these workshop sessions will be made available to attendees through a private YouTube playlist. 

### Procedures

All of the code base required for FOSS, the FOSS Reference Hub and the dplPy project is stored in their respective GitHub repositories:

- [FOSS](https://github.com/CyVerse-learning-materials/foss)
- [FOSS Reference Hub](https://github.com/CosiMichele/foss-reference-hub)
- [dplPy](https://github.com/OpenDendro/dplPy) 

All of these repositories can only be modified by the CyVerse/Data Science Institute team (or the dplPy team regarding the dplPy repository) or through a reviewed [pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests). Websites for FOSS ([foss.cyverse.org](https://foss.cyverse.org/)) and OpenDendro ([opendendro.org](https://opendendro.org/)) are created using [MkDocs-Material](https://squidfunk.github.io/mkdocs-material/) and hosted on [GitHub Pages](https://pages.github.com/), built through automated [GitHub Actions](https://github.com/features/actions).

## Community Practices

### Open Science Commitment 

We are committed to Open Science as we operate through transparency, collaboration, and accessibility, guided by the[FAIR (Findable, Accessible, Interoperable, Reusable)](https://www.nature.com/articles/sdata201618) and [CARE (Collective Benefit, Accountability, Responsibility, Equity)](https://www.gida-global.org/care) principles.

Our educational materials and publications are thoughtfully curated to align with Open Science ideals. We seek to empower others to adopt and implement Open Science practices, making research more accessible and reproducible.

### Land Acknowledgement

As part of the University of Arizona, we acknowledge and respect the land and territories on which we are able to perform our duties as educators with the following statement: *We respectfully acknowledge the University of Arizona is on the land and territories of Indigenous peoples. Today, Arizona is home to 22 federally recognized tribes, with Tucson being home to the O’odham and the Yaqui. Committed to diversity and inclusion, the University strives to build sustainable relationships with sovereign Native Nations and Indigenous communities through education offerings, partnerships, and community service.*

### Diversity Statement

We encourage everyone to participate and are committed to building a community for all. 
Although we will fail attimes, we seek to treat everyone as fairly and equally as possible. Whenever a participant has made a mistake, we expect them to take responsibility for it. If someone has been harmed or offended, if you are a witness to an event of this nature, it is your responsibility to both listen carefully and respectfully to the victims, as well as to take action to bring attention to the behaviour, and to make every effort to stop the behaviour. 

It is also our responsibility to do our best to right the wrong. 
Although this list cannot be exhaustive, we explicitly honor diversity in age, gender, gender identity or expression, culture, ethnicity, language, national origin, political beliefs, profession, race, religion, sexual orientation, socioeconomic status, and technical ability. We will not tolerate discrimination based on any of the protected characteristics above, including participants with disabilities.

### Code of Conduct

In conjunction with for using CyVerse cyberinfrastructure, this Code of Conduct applies to all Event participants and their activities while using CyVerse resources and/or attending the Event.

CyVerse is dedicated to providing professional computational research and educational experiences for all of our users, regardless of domain focus, academic status, educational level, gender/gender identity/expression, age, sexual orientation, mental or physical ability, physical appearance, body size, race, ethnicity, religion (or lack thereof), technology choices, dietary preferences, or any other personal characteristic.

When using CyVerse or participating at an Event, we expect you to:

Interact with others and use CyVerse professionally and ethically by complying with our Policies.
Constructively critize ideas and processes, not people.
Follow the Golden Rule (treat others as you want to be treated) when interacting online or in-person with collaborators, trainers, and support staff.
Comply with this Code in spirit as much as the letter, as it is neither exhaustive nor complete in identifying any and all possible unacceptable conduct.
We do not tolerate harassment of other users or staff in any form (including, but not limited to, violent threats or language, derogatory language or jokes, doxing, insults, advocating for or encouraging any of these behaviors). Sexual language and imagery are not appropriate at any time (excludes Protected Health Information in compliance with HIPAA). Any user violating this Code may be expelled from the platform and the workshop at CyVerse's sole discretion without warning.

To report a violation of this Code, directly message a trainer via Slack or email info@cyverse.org with the following information:

Your contact information
Names (real, username, pseudonyms) of any individuals involved, and or witness(es) if any.
Your account of what occurred and if the incident is ongoing. If there is a publicly available record (a tweet, public chat log, etc.), please include a link or attachment.
Any additional information that may be helpful in resolving the issue.

## Attribution, Authorship, and Ownership

FOSS teaching materials and FOSS Reference Hub are made available under the CC BY 4.0 License: https://creativecommons.org/licenses/by/4.0/legalcode.

dplPy and OpenDendro are made available under the GNU General Public Licence v3.0: https://creativecommons.org/licenses/by/4.0/legalcode

We kindly ask to respect the Licences by which this material is developed.
