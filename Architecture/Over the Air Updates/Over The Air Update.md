Over The Air Update

## Table of Contents

1. [Document Overview](#document-overview)
1. [Glossary](#glossary)
1. [Stakeholder Requirements](#stakeholder-requirements)
1. [Kattegatt PoC](#kattegatt-poc)
1. [Kattegatt PoC Communications Interfaces](#kattegatt-poc-communications-interfaces)
1. [Types of Updates](#types-of-updates)
1. [Design Team Consumer Experience and Interaction](#design-team-consumer-experience-and-interaction)
1. [Software Team Delivery Process and Tool Chain](#software-team-delivery-process-and-tool-chain)
1. [Software Team Tech Stack MicroServices Delivery](#software-team-tech-stack-microservices-delivery)
1. [Over the Air Overall Process](#over-the-air-overall-process)
1. [User Interface Controls Software Builds](#user-interface-controls-software-builds)
1. [Main Controls Software Builds](#main-controls-software-builds)
1. [Auxiliary Controls Software Builds](#auxiliary-controls-software-builds)
1. [Connectivity Controls Software Builds](#connectivity-controls-software-builds)
1. [Full System Testing](#full-system-testing)
1. [Cloud Delivery Method](#cloud-delivery-method)
1. [Electrical System Update](#electrical-system-update)
1. [Example Bundle Script](#example-bundle-script)
1. [Dispatching Deployment](#dispatching-deployment)
1. [Questions-Comments](#questions-comments)


## Document Overview <a name="document-overview"></a>

This document includes the <span style="color:red;font-weight:700;font-size:14px">`Software Microservices`</span> release process from the software quality assurance team (SQA), the <span style="color:Red;font-weight:700;font-size:14px"> `Subsystems`</span> <span style="color:Green;font-weight:700;font-size:14px"> for UI Assemblies, Main Control Assemblies, and Auxiliary Control Assemblies</span>  process for HIL testing of each subsystem, <span style="color:red;font-weight:700;font-size:14px">`Full Electrical Systems`</span>  testing, and finally OTA Package delivery to the <span style="color:red;font-weight:700;font-size:14px">`Connectivity Servers`</span> for deployment.  It also has links to the internal system deployment documentation within the system when the OTA bundle is delivered to the <span style="color:red;font-weight:700;font-size:14px;opacity: 1.0;">`product in the field`</span>. 

This document will also show how the `configurations, capabilities and software` are coupled together for `Subsystems` such as User Interface Asemblies, Main Control Assemblies and Auxiliary Control Assemblies, thus allowing Subsystems to be verified and validated.  

In addition to Subsystems verification this document will define the `Systems` verification and validation for coupling all electronics with loads, sensors and switches for systems verification and validation to allow for `Full System Over the Air Updates`.  

At each stage of development, verification and validation this will require subsystem and systems items to be delivered to a Production Release Process, upon completion of verification and validation.

## Glossary <a name="glossary"></a>

<a href="https://sdlcwiki.electrolux.com/pages/viewpage.action?spaceKey=ASTUESWA&title=Glossary+@+ota" target="_blank">Glossary link</a>

## Stakeholder Requirements <a name="stakeholder-requirements"></a>

1. As a User I want to be able to remotely push software updates that increase the security, performance and/or capabilities of a single appliance or an ecosystem of appliances.
1. As a User I want to be able to stay secure & ​up-to-date with the latest features, so I can enjoy my product longer with new features throughout the life of the product.
1. As a User I want to be able to add and remove apps from my product to tailor my product to my specific usage patterns and needs, as my life changes.
1. As a User I should be able to choose when and which updates I want to apply to my product, based on my current lifestyle.
1. As a User I should be able to apply full or partial updates at my convenience and manage the applications on my product tailoring to my specific interaction patterns and needs, allowing more flexiblity, easier use and simplifying my daily activities.
1. As a User I should have a recovery mechanism such as Factory Defaults to return my product to a usable condition should an outage occur such as power, internet service provider, or WiFi Network.
1. As a User I expect the full software update process from start (Time of Initiation) to end (Product is ready to use post software update) to take no more than 10 minutes, as these are my expectation from other devices I currently use.


## Kattegatt PoC <a name="kattegatt-poc"></a>
<p align="center">
  <img width="1200" src="../images/ucc_electrical_electronics_system_design.jpg">
  </p>

<!-- Notes

-->

## Kattegatt PoC Communications Interfaces <a name="kattegatt-poc-communications-interfaces"></a>
<p align="center">
  <img width="1200" src="./document_formats/kattegatt_poc_comm_protocol_1.jpg">
  </p>

<!-- Notes

-->

## Folder Structure <a name="foler-structure"></a>
<p align="left">
  <img width="300" src="./document_formats/Folder_Structure.jpg">
  </p>

<!-- Notes

-->


## Types of Updates <a name="types-of-updates"></a>
1. Application 
1. Partial
1. Full 

An `Application` update is the application interface that the consumer will specifically interact with graphically and behaviorally.  This application is the same as the type of application you have on your mobile device when you download an application to interact with.  You can add or delete it; however, does not require you to also download the Operating System with each application download.

A `Partial` update is a software update of the microservices tech stack that requires an update without updating the entire software operating system and is done by doing a differential analysis of the files on the product against the files being updatind and only updating the files in the Operating System that require updates.

A `Full` update is a software update of the entire Operating System by updating a secondary partition for `flip flopping` or erasing, formatting, and writing the new operating system update completely.  This will require more time; however, is needed for those customers who have not connected and updated their appliances regularly and require to just update from the initial update to the new update or for those who need to recover their products from it's original factory software to the latest version.


>**NOTE:**  These software Updates can be either Operating System, Configurations, Capabilties, Applications, Embeded RTOS, or anything related to the Tech Stack, including Low Level Programming Languages to High Level Programming Languages and Configuration Parameters.


## Design Team Consumer Experience and Interaction <a name="design-team-consumer-experience-and-interaction"></a>

### Consumer Interaction Sequence Diagram <a name="consumer-interaction-sequence-diagram"></a>

![Consumer Interaction Sequence Diagram](./document_formats/user_interaction_sequence.png)

These are the links to the Design Teams Graphical Assets and Experiences as it pertains to the Over The Air Process on the Appliance Device and on the Mobile Device.


- [OTA Sharepoint Link](https://electrolux.sharepoint.com/:p:/r/sites/GlobalHMIUIStrategy/Shared%20Documents/Design/01%20Presentations/2022%20Sprint%20Reviews/Valhalla%20-%20Sprint%2017-18%20-%20LT%20OTA.pptx?d=w73e109c044eb45a48356c5eddb6070d2&csf=1&web=1&e=ogmhcq&nav=eyJzSWQiOjIxNDc0NzA4ODMsImNJZCI6MjgwNzM2NTczMn0)
- [OTA Figma Link](https://www.figma.com/file/nRlexG1QvxoKLKHnpmi89T/Pattern---OTA-updates?node-id=0-1&t=yd63SKpWlQey2TDx-0)
- [OTA Framer Link - Pending]()

## Software Team Delivery Process and Tool Chain <a name="software-team-delivery-process-and-tool-chain"></a>
This is the process as defined by the `SQA (Software Quality Assurance)` Process Owner.  This [presentation](https://electrolux-my.sharepoint.com/:p:/r/personal/francesco_giorgetti_electrolux_com/Documents/File%20di%20chat%20di%20Microsoft%20Teams/PoC_CICD_24Mar23.pptx?d=wfb85134533c94cc5b1b299dd8b17e390&csf=1&web=1&e=SdDVeq) shows the process of micro services from contributors are pushed to the Continuous Development and Continuous Integration Servers.

In addtiion it shows how code is checked in and to what service or tool, the build process, the test process, and then release of software services to be tested in Subsystems with Configurations.
<!-- Notes

-->
<p align="center">
  <img width="1200" src="../images/ci_cd_process/slide1.jpeg">
  </p>

<p align="center">
  <img width="1200" src="../images/ci_cd_process/slide2.jpeg">
  </p>

  <p align="center">
  <img width="1200" src="../images/ci_cd_process/slide3.jpeg">
  </p>

  <p align="center">
  <img width="1200" src="../images/ci_cd_process/slide4.jpeg">
  </p>


<p align="center">
  <img width="1200" src="../images/ci_cd_process/slide5.jpeg">
  </p>

<p align="center">
  <img width="1200" src="../images/ci_cd_process/slide6.jpeg">
  </p>


## Over the Air Overall Process <a name="over-the-air-overall-process"></a>

This should reflect the Overall Process for the Over the Air Update.  Starting from the top left corner of the image below.
<p align="center">
  <img width="1200" src="./document_formats/software_config_check_in.png">
  </p>

1. Software Engineering Checks In Software libraries and functional changes with instrumented code to test the libary software modules.
1. Systems Engineering Checks In Configurations and Capabilties for the product configurations and capabilities that will work with the Software Stack.
1. SQA (Software Quality Assurance) will perform testing of the software modules ensuring the software complies to the company standards, the functional libaries operate as intended, and provide feedback on any issues pertaining to these software modules.
1. RTE will build the software and configurations and capabilities together and release to each subsystem for testing.
1. Subsystem testing of all modules will be completed to ensure the User Interface, Main Control, Auxiliary Boards and Connectivity Subsystems pass there Hardware In Loop Testing for an approved Subystem Test Plan.
1. Upon all Subsystems and interfaces of those subsystems being tested and passed their respective test plans those files will be released to a production version for Bill of Material Control.
1. Systems Engineers will build the System Bundle that will include all the subsystem items released (Software, Configurations, Capabilties and Software Bundle Script) and test the programming process for deploying System Updates.  This can be done wirelessly or wired to the system to validate the systems update capabilties.
1. Upon System Validations and test plans passed this software bundle will be released to a production version for Bill of Material Control.
1. From the Producton version within the revision control system this software bundle will then be deployed to the server for release to Beta or all consumers.
1. Once on the server the scheduler will schedule deliver to the consumers, coordinated with consumer acceptance, if required.



<p align="center">
  <img width="1450" src="../images/over_the_air_overall_process.jpg">
  </p>

<!-- Notes

-->


## Software Team Tech Stack MicroServices Delivery <a name="software-team-tech-stack-microservices-delivery"></a>
- Software Check in per the process as defined by SQA.
- Continuous Integration and Development servers build the software, identifying build issues and aligning to the scripts for software delivery.
- Software to be built, tested, and promoted based on business needs for development, test, and release of the software packages.
- Release of these modules and libraries will be under revision control in Software Repositories, such as Bitbucket or Github, and Build Repositories, such as Jenkins.

<p align="center">
  <img width="800" src="../images/tech_stack_delivery_teams.jpg">
  </p>

<!-- Notes

-->


## User Interface Controls Software Builds <a name="user-interface-controls-software-builds"></a>
- This is a specific release for User Interface Assemblies to conduct Hardware in Loop Testing.
- This is our current release process to production which will include a bootloader for each of the micros in the subsystem.

<p align="center">
  <img width="800" src="../images/user_interface_sw_builds.jpg">
  </p>

<!-- Notes

-->

## Main Controls Software Builds <a name="main-controls-software-builds"></a>
- This is a specific release for Main Control Assemblies to conduct Hardware in Loop Testing.
- This is our current release process to production which will include a bootloader for each of the micros in the subsystem.


<p align="center">
  <img width="800" src="../images/main_control_sw_builds.jpg">
  </p>

<!-- Notes

-->

## Auxiliary Controls Software Builds <a name="auxiliary-controls-software-builds"></a>
- This is a specific release for Auxiliary Control Assemblies to conduct Hardware in Loop Testing.
- This is our current release process to production which will include a bootloader for each of the micros in the subsystem.


<p align="center">
  <img width="800" src="../images/auxiliary_boards_sw_builds.jpg">
  </p>

<!-- Notes

-->

## Connectivity Controls Software Builds
<a name="connectivity-controls-software-builds"></a>
- This is a specific release for Connectivity Control Assemblies to conduct Hardware in Loop Testing.
- This is our current typical release process to production which will include a bootloader for each of the micros in the subsystem.


<p align="center">
  <img width="800" src="../images/connectivity_sw_builds.jpg">
  </p>

<!-- Notes

-->

## Full System Testing <a name="full-system-testing"></a>
- Full System Verification Testing to validate software, configurations and capabilites are built and aligned to the performance functions of the Full System.  This includes `Loads` (Motors, Heaters, Pumps, etc.), `Sensors` (RTD, NTC, PTC, Hall Effect, Speed, etc.), and `Switches` (Door Lock, Door State, Centrifugal, etc.).
- Full System Testing also includes verifying the Software OTA transfers, updates and deploys properly in a testing environment.


<p align="center">
  <img width="1000" src="../images/full_system_with_OTA.jpg">
  </p>

<!-- Notes

-->

[Release to TeamCenter Process Video](https://electrolux-my.sharepoint.com/:v:/r/personal/wallace_elston_electrolux_com/Documents/Video/OTA%20Process%20and%20Releasing%20to%20TeamCenter.mov?csf=1&web=1&e=H53b16)

Example of this file is below at [Example OSD json Bundle](./document_formats/osd_file/package.json)

## Releases <a name="releases"></a>

Previously we only released software and configurattions to our suppliers to build our controls and program software, and our factories to update controls in our factories.  **Now it is important that those instances of software and configurations are deployed to our consumers who have already purchased appliances and have those appliances in their home.**

## Cloud Delivery Method <a name="cloud-delivery-method"></a>

This is defined by the connectivity cloud team of Principal Architect, Connectivity and Lead System Architect, Connectivity and reflects when the physical assets of software and configuration are delivered to the connectivity team how they deliver to the server for OTA deployment.

<p align="center">
  <img width="500" src="../images/cloud_deployment_mechanism.jpg">
  </p>

<!-- Notes

-->

## Electrical System Update <a name="electrical-system-update"></a>
Below are the links to the Confluence page pertaining to the Over the Air Process. [Over The Air Connectivity @ OTA](https://sdlcwiki.electrolux.com/display/ASTUESWA/Over-The-Air+Connectivity+@+ota) Confluence Page.
<p align="center">
  <img width="1000" src="../images/electrical_system_update_sequence.jpg">
  </p>

<!-- Notes

-->

## UML Diagram

### Electrical System and Cloud Interface
![Electrical System UML](./document_formats/user_interaction_sequence.png)



## Example Bundle Script <a name="example-bundle-script"></a>

[OSD.json Example](./document_formats/osd_file/package.json)

## Dispatching Deployment <a name="dispatching-deployment"></a>

[Over the Air Connectivity @ OTA](https://sdlcwiki.electrolux.com/pages/viewpage.action?spaceKey=ASTUESWA&title=Over-The-Air+Connectivity+@+ota)


[Reprogramming Mechnanism](https://sdlcwiki.electrolux.com/display/ASTUESWA/Overview+@+ota)

1. [Bootloader](https://sdlcwiki.electrolux.com/display/ASTUESWA/Overview+@+ota) - Used to reset, erase and program the specific software for a specific micro.
1. [Programming Agent]() - Used to Dispatch specific software to the specific node to be reprogrammed.
1. [Scribe](https://sdlcwiki.electrolux.com/display/ASTUESWA/Overview+@+ota) - Ask Lucio is this would be something like your experience using FIT Table for setting partition areas to program specific sectors or pages based on the FIT Table for doing partial updates?
1. [Bridge](https://sdlcwiki.electrolux.com/display/ASTUESWA/Overview+@+ota) - Used to allow the Programming Agent to reach other nodes in the system beyond the direct connection the Programming Agent or Master Programmer may have acess to.
1. [Open Points](https://sdlcwiki.electrolux.com/display/ASTUESWA/Open+points+@+ota)






## Questions-Comments <a name="questions-comments"></a>

1. Scribe and FIT Table the same for partitioning software blocks:
      1. Bootloader Application
      1. RTOS
      1. Horizon
      1. Application
      1. Configuration
      1. Capability

1. How are you packaging the bundle?

1. What are you using as a mechanism to extract bundle when built with bundle? Script?

1. How does the system extract the bundle when system receives bundle?

1. How does each subsystem validate its compatible?

1. Using DAAS as point to point for nodes on bus one at a time?

1. Is there an order to the update?

What Characteristics of the Update are you verifying:

1. Are you verifying node#?
1. Micro Supplier? Micro Family? Micro Number?  All of the above.

1. Programming Agent unpackaged using script. PA. Fetches full package to Wi-Fi node. Fetches each node via URL for specific software to be programmed within script. 




