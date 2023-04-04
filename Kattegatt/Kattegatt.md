# Kattegatt

## Table of Contents

1. [Product Categories and Product Platform](#product-categories-and-product-platform)
     1. [Cooking](#cooking)
     1. [Laundry](#laundry)
     1. [Refrigeration](#refrigeration)
1. [Global Strategy](#global-strategy)
1. [One Pager of Initiatives](#one-pager-initiatives)
1. [Kattegatt Slice/PoC](#kattegatt-slicepoc)
     1. [Product Description Kattegatt](#product-description)
     1. [Systems Design Kattegatt](#system-design)
     1. [Flexible Architecture](#flexible-architecture)
     1. [Use Case Cluster Electrical and Electronics System Design for PoC](#use-case-cluster-electrical-and-electronics-system-design-for-poc)
     1. [Tech Stack Delivery Product Teams](#tech-stack-delivery-product-teams)
     1. [Tech Stack Delivery Software Teams](#tech-stack-delivery-software-teams)
     1. [Continuous Integration and Development](#continuous-integrationcontinuous-development-video)
     1. [Outcomes Of Kattegatt](#outcomes-of-kattegatt)
1. [Valhalla](#valhalla)
     1. [Consumer Experience](#consumer-experience)
     1. [Mechanical Architecture](#mechanical-architecture)
     1. [Electrical Architecture](#electrical-architecture)
     1. [Electronics Architecture](#electronics-architecture)


## Design Principles
<p align="center">
  <img width="1200" src="design principles/slide2.jpeg">
  </p>

## Product Categories and Product Platform
Product Categories:
<p align="center">
  <img width="1200" src="../images/consumer_experience/slide8_design_complexity.jpeg">
  </p>

<p align="center">
  <img width="1200" src="../images/product_portfolio.jpg">
  </p>

<!-- Notes

-->

### Cooking
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

### Laundry
|Category|Platform|Sub-Category|
|---|---|---|
|Laundry|Washer|Front Load|
|Laundry|Washer|Top Load|
|Laundry|Dryer|Single|
|Laundry|Combo|Single|

### Refrigeration
|Category|Platform|Sub-Category|
|---|---|---|
|Refrigeration|Side By Side|Side By Side|
|Refrigeration|Side By Side|FDBM|
|Refrigeration|Side By Side|Multi Door|
|Refrigeration|Top Mount|Bottom Mount|
|Refrigeration|Freezers|Ice Chest|




## Global Strategy
Strategy to support all regions across all product categories.
<p align="center">
  <img width="1200" src="../images/global_organization.png">
  </p>

<!-- Notes

-->

1. Europe
1. North America/Canada
1. South America
1. Asia



## One Pager Initiatives
<p align="center">
  <img width="1200" src="../images/initiative_one_pager.jpg">
  </p>

<!-- Notes

-->

## Kattegatt Slice/PoC
### Product Description
[**BIO_ECWS3012AS-OL**](https://www.electrolux.com/en/p/kitchen/wall-ovens/single-wall-ovens/ECWS3012AS)
Single Built In Oven Product Platform
<p align="center">
  <img width="1200" src="../images/BIO_ECWS3012AS-OL.png">
  </p>

Control Panel for Built In Oven
<p align="center">
  <img width="1200" src="../images/ECWS3012AS-CRL.png">
  </p>

### System Design
<p align="center">
  <img width="1200" src="../images/UCC_Electrical_Electronics_System_Design.jpg">
  </p>

<!-- Notes

-->

### Flexible Architecture
<p align="center">
  <img width="1200" src="../images/flexible_platform.jpg">
  </p>

<!-- Notes

-->
|EPU|SOM|Description|Version|Display|RTOS/OS|
|----|----|----|----|----|----|
|EPU_001|IMx8 Mini|Valhalla UI Architecture 001|1.0|7.8" Display|Linux OS/Horizon RTOS|
|EPU_002|IMx8 Mini|Valhalla UI Architecture 002|1.0|4.3" Display|Linux OS/Horizon RTOS|
|EPU_003|IMx8 Mini|Valhalla UI Architecture 003|1.0|2.8" Display|Linux OS/Horizon RTOS|
|EPU_004|M4|Valhalla UI Architecture 004|1.0|LED Module/7 Segment Display|Horizon RTOS|
|EPU_005|M4|Valhalla UI Architecture 005|1.0|LED 7 Segment/Point Display|Horizon RTOS|

### Use Case Cluster Electrical and Electronics System Design for PoC
<p align="center">
  <img width="1200" src="../images/UCC/UCC_and_Target_Architecture_1.jpg">
  </p>
<p align="center">
  <img width="1200" src="../images/UCC/UCC_and_Target_Architecture_2.jpg">
  </p>
<p align="center">
  <img width="1200" src="../images/UCC/UCC_and_Target_Architecture_3.jpg">
  </p>
<p align="center">
  <img width="1200" src="../images/UCC/UCC_and_Target_Architecture_4.jpg">
  </p>
<p align="center">
  <img width="1200" src="../images/UCC/UCC_and_Target_Architecture_5.jpg">
  </p>
<p align="center">
  <img width="1200" src="../images/UCC/UCC_and_Target_Architecture_6.jpg">
  </p>
<p align="center">
  <img width="1200" src="../images/UCC/UCC_and_Target_Architecture_7.jpg">
  </p>
<p align="center">
  <img width="1200" src="../images/UCC/UCC_and_Target_Architecture_8.jpg">
  </p>
<p align="center">
  <img width="1200" src="../images/UCC/UCC_and_Target_Architecture_9.jpg">
  </p>
<p align="center">
  <img width="1200" src="../images/UCC/UCC_and_Target_Architecture_10.jpg">
  </p>
<p align="center">
  <img width="1200" src="../images/UCC/UCC_and_Target_Architecture_11.jpg">
  </p>
<p align="center">
  <img width="1200" src="../images/UCC/UCC_and_Target_Architecture_12.jpg">
  </p>
<p align="center">
  <img width="1200" src="../images/UCC/UCC_and_Target_Architecture_13.jpg">
  </p>
<p align="center">
  <img width="1200" src="../images/UCC/UCC_and_Target_Architecture_14.jpg">
  </p>
<p align="center">
  <img width="1200" src="../images/UCC/UCC_and_Target_Architecture_15.jpg">
  </p>

<!-- Notes


-->

### Tech Stack Delivery Product Teams
<p align="center">
  <img width="1200" src="../images/Build_and_Partitioning_TEAM_Aligned_Tech_Stack.jpg">
  </p>

<!-- Notes

-->

### Tech Stack Delivery Software Teams
<p align="center">
  <img width="1200" src="../images/Tech_Stack_Delivery_Teams.jpg">
  </p>

<!-- Notes

-->

### Continuous Integration/Continuous Development Video
[![Continuous Integration/Continuous Development](../images/CI_CD_Meeting.png)](https://electrolux-my.sharepoint.com/personal/francesco_giorgetti_electrolux_com/_layouts/15/stream.aspx?id=%2Fpersonal%2Ffrancesco%5Fgiorgetti%5Felectrolux%5Fcom%2FDocuments%2FFile%20di%20chat%20di%20Microsoft%20Teams%2FCI%5FCD%20meeting%2D20230324%5F113819%2DRegistrazione%20della%20riunione%20%281%29%2Emp4&referrer=Teams%2ETEAMS%2DELECTRON&referrerScenario=p2p%5Fns%2Dbim&ga=1)


## Outcomes of Kattegatt

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


## **Valhalla**

**Goals:**
1. Common Consumer Experience
1. Common Mechanical Architecture
1. Common Electrical Architecture with UDA
1. Common Electronics Architecture using UEHWA and UESWA

#### Roadmap Vision
<p align="center">
  <img width="1200" src="../images/consumer_experience/Slide40_Initial_Vision.jpeg">
  </p>

### Consumer Experience
#### Current Ux Debt Project by Project
<p align="center">
  <img width="1200" src="../images/consumer_experience/Slide7_Ux_Debt.jpeg">
  </p>

#### Interaction Layers
<p align="center">
  <img width="1200" src="../images/consumer_experience/Slide10_Component_Layers.jpeg">
  </p>

#### Reusable Widgets
<p align="center">
  <img width="1200" src="../images/consumer_experience/Slide18_Reusable_Widgets.jpeg">
  </p>


#### Modalities and Good/Better/Best

<p align="center">
  <img width="1200" src="../images/consumer_experience/Slide25_Good_Better_Best.jpeg">
  </p>


#### Cross Product Solutions

<p align="center">
  <img width="1200" src="../images/consumer_experience/Slide14_Cross_Product.jpeg">
  </p>



### Mechanical Architecture
#### Process for Mechanical Constraints
<p align="center">
  <img width="1200" src="../images/mechanical/cooking/Slide2_Process.jpeg">
  </p>




#### Cooking

**Clustering**
<p align="center">
  <img width="1200" src="../images/mechanical/cooking/Slide3_Clustering.jpeg">
  </p>

**Envelopes**
<p align="center">
  <img width="1200" src="../images/mechanical/cooking/Slide5_Envelopes.jpeg">
  </p>

**Assemblies**
<p align="center">
  <img width="1200" src="../images/mechanical/cooking/Slide7_assembly.jpeg">
  </p>

#### Laundry Dish
**Clustering**
<p align="center">
  <img width="1200" src="../images/mechanical/laundry_dish/Slide1_Clustering.jpeg">
  </p>

**Compound Shapes**
<p align="center">
  <img width="1200" src="../images/mechanical/laundry_dish/Slide2_Shapes.jpeg">
  </p>

**Envelopes**
<p align="center">
  <img width="1200" src="../images/mechanical/laundry_dish/Slide4_envelopes.jpeg">
  </p>


#### Refrigeration

**Current**
<p align="center">
  <img width="1200" src="../images/mechanical/refrigeration/Slide3_Current.jpeg">
  </p>


**Clustering**
<p align="center">
  <img width="1200" src="../images/mechanical/refrigeration/Slide7_Clustering.jpeg">
  </p>


**Envelopes**
<p align="center">
  <img width="1200" src="../images/mechanical/refrigeration/Slide9_envelopes.jpeg">
  </p>

#### All Categories

**Outcomes - All Categories**
<p align="center">
  <img width="1200" src="../images/consumer_experience/Slide17_Mechanical_Landscape.jpeg">
  </p>

### Electrical Architecture

Horizon Systems Architecture:

#### Appliance States and Modes

Appliance modes

1. Off Mode
1. User Mode (Default Mode)
1. Demo Mode
1. Sabbath Mode
1. Programming Mode
1. Diagnostics Mode
 
Appliance States

1. Disconnected State
1. Initialization State
1. Standby State 
1. Delay Start State
1. Active State
1. Error State

Subsystems:

1. UI/HMI 
1. Main Control Board
1. Auxiliary Control Boards
1. Sensors
1. Loads
1. Switches
1. Harnesses/Connections

Features:

1. Temperature
1. Standby
1. Programming and Reprogramming
1. Factory
1. Service
1. ECM
1. Connectivity OTA
1. Connectivity
1. Provisioning
1. Claiming
1. Security and Privacy
1. Over The Air Update
1. Power Loss and Recovery
1. Initialization and Configuration

Operations:
1. Operands (Start and Cancel)

Control Settings
1. General
     1. About
          1. Product Version
               1. Model Number
               1. Serial Number
          1. Control Versions
               1. HMI Software Version
               1. HMI Configuration Version
               1. NIU Software Version
               1. NIU Configuration Version
               1. Control Board Software Version
               1. Control Board Configuration Version
     1. Software Update
          1. Latest Software Version
          1. Update Software Version, if available
              1. Yes
              1. No
1. Connectivity
    1. Wireless Network
    1. Features
    1. Smart Grid
         1. Opt In
         1. Opt Out
    1. Data Analytics
         1. Opt In
         1. Opt Out
    1. WiFi
         1. On/Off
         1. Status:
             1. Provisioning
             1. Deprovisioning
         1. WiFi Network Connected
         1. WiFi Signal Strength
    1. BLE
         1. On/Off
         1. BLE Network
              1. Pair
              1. Unpair
1. Personalization
     1. Time of Day
          1. 12 Hour/24 Hour
          1. Time of Day Manual
          1. Time of Day Automatic (Connected Appliances Only)
     1. Audio
          1. Volume Level
          1. End of Cycle Tone
          1. Key Press Tone
     1. Display & Brightness
          1. Backlight Brightness
          1. Display Theme
     1. Control Lock
          1. Control Locked
          1. Control Unlocked
     1. Calibration:
          1. Cooking
                1. Hobs
                1. Ovens
                     1. Temperature Offset
                1. Hoods
          1. Laundry
          1. Washers
          1. Dryers
          1. Dishwashers
          1. Refrigerators
     1. Modes:
          1. Sabbath Mode
          1. Demo Mode
1. Service Mode
     1. Diagnostics Auto Routine
     1. Results from Auto Routine
     1. Error Failure Codes and Descriptions
     1. System Reboot
     1. Factory Mode/Verification and Validation Mode
     1. Diagnostics Manual
     1. Turn On Loads
     1. Read Sensors/Switches
     1. Restore Factory Reset

Unified Data Architecture
<p align="center">
  <img width="1200" src="../images/UDA/Slide3.jpeg">
  </p>


### Electronics Architecture

#### UEA - Unified Electronics Hardware Architecture
<p align="center">
  <img width="1200" src="../images/UEA/Slide8_UEA_HW.jpeg">
  </p>



#### UESWA - Unified Electronics Software Architecture
<p align="center">
  <img width="1200" src="../images/UEA/Slide17_UEA_SW.jpeg">
  </p>
