# Kattegatt

## Table of Contents

1. [Design Principles](#design-principles)
1. [Product Categories and Product Platform](#product-categories-and-product-platform)
    1. [Cooking](#cooking)
    1. [Laundry](#laundry)
    1. [Refrigeration](#refrigeration)
1. [Global Strategy](#global-strategy)
1. [One Pager of Initiatives](#one-pager-initiatives)
1. [Kattegatt Slice/PoC](#kattegatt-slice-poc)
    1. [Product Description Kattegatt](#product-description)
    1. [Systems Design Kattegatt](#system-design)
    1. [Use Case Clusters](#use-case-clusters)
    1. [Tech Stack Delivery Product Teams](#tech-stack-delivery-product-teams)
    1. [Tech Stack Delivery Software Teams](#tech-stack-delivery-software-teams)
    1. [Continuous Integration and Development](#continuous-integrationcontinuous-development-video)
    1. [Outcomes Of Kattegatt](#outcomes-of-kattegatt)
1. [Valhalla](#valhalla)
    1. [Roadmap Vision](#roadmap-vision)
    1. [Consumer Experience](#consumer-experience)
        1. [Current Ux Debt Project by Project](#current-ux-debt-project-by-project)
        1. [Iteration Layers](#interaction-layers)
        1. [Reusable Graphics](#reusable-graphics)
        1. [Modalities](#modalities-and-goodbetterbest)
        1. [Cross Product Solutions](#cross-product-solutions)
  1. [Mechanical Architecture](#mechanical-architecture)
      1. [Process for Mechanical Constraints](#process-for-mechanical-constraints)
      1. [Cooking](#cooking-1)
      1. [Laundry/Dish](#laundry-dish)
      1. [Refrigeration](#refrigeration)
      1. [All Categories](#all-categories)
  1. [Electrical Systems Architecture](#electrical-systems-architecture)
      1. [Horizon Systems Architecture](#horizon-systems-architecture)
      1. [UDA](#unified-data-architecture)
  1. [Horizon Subsystems Architecture](#horizon-subsystems-architecture)
  1. [Electronics Module Architecture](#electronics-module-architecture)
      1. [Flexible Architecture](#flexible-architecture)
      1. [EPU Modules](#epu-modules)
      1. [UEA](#uea---unified-electronics-hardware-architecture)
      1. [UESWA](#ueswa---unified-electronics-software-architecture)
      1. [Configurations](#configurations)
      1. [Tools](#tools)
  1. [Organizational Strategy](#organizational-material)
      1. [Organization Process](#organization-process)
      1. [Strategy](#strategy)
      1. [Architecture](#architecture)
      1. [Execution](#execution)
      1. [Practical Application Methodology](#practical-application-methodology)


## Design Principles <a name="design-principles"></a>
<p align="center">
  <img width="1200" src="design_principles/slide2.jpeg">
  </p>

## Product Categories and Product Platform <a name="product-categories-and-product-platform"></a>

Product Categories:
<p align="center">
  <img width="1200" src="./images/consumer_experience/slide8_design_complexity_1.jpeg">
  </p>

<p align="center">
  <img width="1200" src="./images/product_portfolio_1.jpg">
  </p>

<!-- Notes

-->

### Cooking <a name="cooking"></a>
|Category|Platform|Sub-Category|
|---|---|---|
|Cooking|Built In Ovens|Single|
|Cooking|Built In Ovens|Double|
|Cooking|Built In Ovens|Combo|
|Cooking|Built In Ovens|Dedicated Microwave|
|Cooking|Free Standing Oven|Single with Induction|
|Cooking|Free Standing Oven|Single with Radiant|
|Cooking|Free Standing Oven|Single with Gas|
|Cooking|Hobs/Cooktop|Induction|
|Cooking|Hobs/Cooktop|Radiant|
|Cooking|Hobs/Cooktop|Gas|
|Cooking|Hoods|Single|

### Laundry <a name="laundry"></a>
|Category|Platform|Sub-Category|
|---|---|---|
|Laundry|Washer|Front Load|
|Laundry|Washer|Top Load|
|Laundry|Dryer|Single|
|Laundry|Combo|Single|

### Refrigeration <a name="refrigeration"></a>
|Category|Platform|Sub-Category|
|---|---|---|
|Refrigeration|Side By Side|Side By Side|
|Refrigeration|Side By Side|FDBM|
|Refrigeration|Side By Side|Multi Door|
|Refrigeration|Top Mount|Bottom Mount|
|Refrigeration|Freezers|Ice Chest|




## Global Strategy <a name="global-strategy"></a>

Strategy to support all regions across all product categories.
<p align="center">
  <img width="1200" src="./images/global_organization.png">
  </p>

<!-- Notes

-->

1. Europe
1. North America/Canada
1. South America
1. Asia



## One Pager Initiatives <a name="one-pager-initiatives"></a>

<p align="center">
  <img width="1200" src="./images/initiative_one_pager_1.jpg">
  </p>

<!-- Notes

-->

## Kattegatt Slice/PoC <a name="kattegatt-slice-poc"></a>

### Product Description <a name="product-description"></a>

[**BIO_ECWS3012AS-OL**](https://www.electrolux.com/en/p/kitchen/wall-ovens/single-wall-ovens/ECWS3012AS)
Single Built In Oven Product Platform
<p align="center">
  <img width="1200" src="./images/BIO_ECWS3012AS-OL.png">
  </p>

Control Panel for Built In Oven
<p align="center">
  <img width="1200" src="./images/ECWS3012AS-CRL.png">
  </p>

### System Design <a name="system-design"></a>
<p align="center">
  <img width="1200" src="./images/ucc_electrical_electronics_system_design.jpg">
  </p>

<!-- Notes

-->

### Use Case Clusters <a name="use-case-clusters"></a>

<p align="center">
  <img width="1200" src="./images/UCC/UCC_and_Target_Architecture_1.jpg">
  </p>
<p align="center">
  <img width="1200" src="./images/UCC/UCC_and_Target_Architecture_2.jpg">
  </p>
<p align="center">
  <img width="1200" src="./images/UCC/UCC_and_Target_Architecture_3.jpg">
  </p>
<p align="center">
  <img width="1200" src="./images/UCC/UCC_and_Target_Architecture_4.jpg">
  </p>
<p align="center">
  <img width="1200" src="./images/UCC/UCC_and_Target_Architecture_5.jpg">
  </p>
<p align="center">
  <img width="1200" src="./images/UCC/UCC_and_Target_Architecture_6.jpg">
  </p>
<p align="center">
  <img width="1200" src="./images/UCC/UCC_and_Target_Architecture_7.jpg">
  </p>
<p align="center">
  <img width="1200" src="./images/UCC/UCC_and_Target_Architecture_8.jpg">
  </p>
<p align="center">
  <img width="1200" src="./images/UCC/UCC_and_Target_Architecture_9.jpg">
  </p>
<p align="center">
  <img width="1200" src="./images/UCC/UCC_and_Target_Architecture_10.jpg">
  </p>
<p align="center">
  <img width="1200" src="./images/UCC/UCC_and_Target_Architecture_11.jpg">
  </p>
<p align="center">
  <img width="1200" src="./images/UCC/UCC_and_Target_Architecture_12.jpg">
  </p>
<p align="center">
  <img width="1200" src="./images/UCC/UCC_and_Target_Architecture_13.jpg">
  </p>
<p align="center">
  <img width="1200" src="./images/UCC/UCC_and_Target_Architecture_14.jpg">
  </p>
<p align="center">
  <img width="1200" src="./images/UCC/UCC_and_Target_Architecture_15.jpg">
  </p>

<!-- Notes


-->

### Tech Stack Delivery Product Teams <a name="tech-stack-delivery-product-teams"></a>

<p align="center">
  <img width="1200" src="./images/Build_and_Partitioning_TEAM_Aligned_Tech_Stack.jpg">
  </p>

<!-- Notes

-->

### Tech Stack Delivery Software Teams <a name="tech-stack-delivery-software-teams"></a>

<p align="center">
  <img width="1200" src="./images/tech_stack_delivery_teams.jpg">
  </p>

<!-- Notes

-->

### Continuous Integration/Continuous Development Video

<a name="continuous-integrationcontinuous-development-video"></a>

[![Continuous Integration/Continuous Development](./images/CI_CD_Meeting.png)](https://electrolux-my.sharepoint.com/personal/francesco_giorgetti_electrolux_com/_layouts/15/stream.aspx?id=%2Fpersonal%2Ffrancesco%5Fgiorgetti%5Felectrolux%5Fcom%2FDocuments%2FFile%20di%20chat%20di%20Microsoft%20Teams%2FCI%5FCD%20meeting%2D20230324%5F113819%2DRegistrazione%20della%20riunione%20%281%29%2Emp4&referrer=Teams%2ETEAMS%2DELECTRON&referrerScenario=p2p%5Fns%2Dbim&ga=1)


## Outcomes of Kattegatt <a name="outcomes-of-kattegatt"></a>

Initiatives:
1.	Valhalla UI Initiative to continue using the PoC (i.e. EPU = MPU/MCU)
1.	UDA Initiative to Continue
1.	UEA/UESWA Initiatives are part of the tech stack and should continue.
1.	Start a initiative with the Main Control Boards to integrate the inverter/motor control.

What we need from BCG is a plan for the following:   
1.	Way of Working – Agile across the teams.
1.	Budget to fund initiatives
1.	UCC aligned to these Initiatives
1.	Teams with Product Owners, Scrum Masters, contributing to the initiatives.
1.	Product Suites aligned with the business proposal for profitability OR Strategic Market Objectives
Right Now I see they are validating strategies and initiatives we already have in place, and I want to ensure the outcomes of the work BCG is sustainable for the inititiaves…




### Electronics Module Architecture <a name="electronics-module-architecture"></a>

#### UEA - Unified Electronics Hardware Architecture
<a name="uea"></a>

<p align="center">
  <img width="1200" src="../horizon/UEA/Slide8_UEA_HW.jpeg">
  </p>


#### UESWA - Unified Electronics Software Architecture
<a name="ueswa"></a>

<p align="center">
  <img width="1200" src="../horizon//UEA/Slide17_UEA_SW.jpeg">
  </p>

#### UEA Configurations - Unified Electronics Architecture
<a name="configurations"></a>

#### UEA Tools - Unified Electronics Architecture
<a name="tools"></a>

## Organizational Material <a name="organizational-material"></a>

### Organization Process <a name="organization-process"></a>

Slice Approach:

<p align="center">
  <img width="1200" src="./documents/process_and_organization.jpg">
  </p>

### Strategy:  <a name="strategy"></a>

- Aligned Roadmaps from the Use Case Clusters outlining strategic use cases globally that the architecture teams consumer and create solutions around.
- These roadmaps are built from industry technologies like automotive, wearables, consumer electronics (smartphones), competitive benchmarking like Bosch, Miele, Wolf, Whirlpool, LG, Samsung, and Business Goals and Ventures like sustainability, partnerships with Amazon, Matter, Google, Power Management, etc.
- Strategy focuses on 5 - 7 years goal

### Architecture:  <a name="architecture"></a>

- Create a Mechanical Architecture Team within each product Platform in the CxA Categories with the goal to focon on the following architectures:
  - Console
  - Cavity
  - Chassis
  - Aesthetics
  - Door, Handle and Badging
- Centralize all design strategies through a central User Design, Connectivity, Electrical and Electronics Systems, Mechanical Systems Organization that can deliver to all the stakeholders globally. Based around these product platforms and leveraging synergies between product platforms....(For instance Ovens, Dishwasher, Washer and Dryer are all about the same shape, size and mechanical design).
- Architecture focuses on 3 - 5 year goals.

### Execution: <a name="execution"></a>
 
- Align the R&D CxA's to just integrating these centralized solutions onto their platform with the goal of NO NEW technologies, just a integration, test, release to manufacturing, logistics and release to the consumer philosophy.  Typical time to integrate, test, release to manufacturing, logistics and finally release to consumer should be less than 6 - 8 moths.
- This group also focuses on improving the individual product performance such as Washing performance, cooking performance, cooling performance, etc.
- Execution focuses on 1 - less than 2 year goals.

Getting the organization correct, and enabling a few people rather than all projects deciding on Architecture will speed up, and reduce cost because you are centralizing design elements and reducing the indecision, redundancy, tooling costs and maintenance costs of redundancy.  There are more the same than different in our appliances across the company.

### Practical Application Methodology <a name="practical-application-methodology"></a>

Step 1:  

- Align Executive Leadership.....Ola, Ian Banes, Marco B, Patrick Le Corre, Elena Breda.

Step 2: 

- From a Mechanical Architecture Perspective for console, chassis, do what cooking just did:

- From an Electronics and Electrical System Perspective Move everyone to EES and assign accountability for ownership of the Tech Stack and Decision Making Accountability, and accelerate a stable tech stack with ownership model.  Put all Project's on hold to build a stable architecture for which to build all projects on.

  Systems:
  - Systems Solutions Architect Cross Category, this includes Connectivity, Manufacturing, Service, Quality inputs.
  - Systems Solutions Architect Connectivity
  - Systems Solutions Architect Category FPP, Accountable for Category specific solutions
  - Systems Solutions Architect Category FPS, Accountable for Category specific solutions
  - Systems Solutions Architect Category WET, Accountable for Category specific solutions

  Subsystem:
  - Subsystems Solutions Architect HMI/UI
  - Subsystems Solutions Architect Main Controls
  - Subsystems Solutions Architect Loads
  - Subsystems Solutions Architect Sensors
  - Subsystems Solutions Architect Switches
  - Subsystems Solutions Architect Harnesses/Wiring
  - Subsystems Solutions Architect Connectivity

  Software:
    - Software Solutions Architect Cross Category
    - Software Solutions Architect Category FPP, Accountable for Category specific solutions
    - Software Solutions Architect Category FPS, Accountable for Category specific solutions
    - Software Solutions Architect Category WET, Accountable for Category specific solutions

  Hardware:
    - Hardware Solutions Architect Cross Category
    - Hardware Solutions Architect Category FPP, Accountable for Category specific solutions
    - Hardware Solutions Architect Category FPS, Accountable for Category specific solutions
    - Hardware Solutions Architect Category WET, Accountable for Category specific solutions

  Configuration/Tools
    - Configurations Solutions Architect Cross Category
    - Configurations Solutions Architect FPP, Accountable for Category specific solutions
    - Configurations Solutions Architect FPS, Accountable for Category specific solutions
    - Configurations Solutions Architect WET, Accountable for Category specific solutions

Step 3: 
- Engage with a single Project to build the full tech stack including the Application from the work done in the previous year within the R&D CxA's with the Execution Teams on a single project.  Map process, refine process, update process for how projects are delivered from Architecture Phase to Execution Phase and resolve any issues in Architecture Process or Tech Stack. Single Pilot Organizational Alignment.

Step 4: 
- Engage with a project per category to ensure the Tech Stack and Systems Architecture are robust to all product categories, one project per category. Partial Organizational alignment around the Projects per category impacted.

Step 5:
- Mass Deployment including all tools, processes, Full Organizational Alignment between Architecture and Execution Teams.