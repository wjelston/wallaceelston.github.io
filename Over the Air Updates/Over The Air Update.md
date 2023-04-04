Over The Air Update

## Table of Contents

1. [Document Synopsis](#document-synopsis)
1. [Glossary](#glossary)
1. [Stakeholder Requirements](#stakeholder-requirements)
1. [Kattegatt PoC](#kattegatt-poc)
1. [Types of Updates](#types-of-updates)
1. [Design Team Consumer Experience and Interaction](#design-team-consumer-experience-and-interaction)
1. [Software Team Delivery Process and Tool Chain](#software-team-delivery-process-and-tool-chain)
1. [Software Team Tech Stack MicroServices Delivery](#software-team-tech-stack-microservices-delivery)
1. [Over the Air Overall Process](#over-the-air-overall-process)
1. [User Interface Software Builds](#user-interface-software-builds)
1. [Main Control Software Builds](#main-control-software-builds)
1. [Auxiliary Boards Software Builds](#auxiliary-boards-software-builds)
1. [Connectivity Board Software Builds](#connectivity-boards-software-builds)
1. [Full System Testing](#full-system-testing)
1. [Cloud Delivery Method](#cloud-delivery-method)
1. [Electrical System Update](#electrical-system-update)
1. [Example json Bundle Script](#example-json-bundle-script)
1. [Dispatching Deployment](#dispatching-deployment)
1. [UML Definition](#uml-definition)


## Document Synopsis

This document includes the <span style="color:red;font-weight:700;font-size:14px">`Software Microservices`</span> release process from the software quality assurance team (SQA), the <span style="color:Red;font-weight:700;font-size:14px"> `Subsystems`</span> <span style="color:Green;font-weight:700;font-size:14px"> for UI Assemblies, Main Control Assemblies, and Auxiliary Control Assemblies</span>  process for HIL testing of each subsystem, <span style="color:red;font-weight:700;font-size:14px">`Full Electrical Systems`</span>  testing, and finally OTA Package delivery to the <span style="color:red;font-weight:700;font-size:14px">`Connectivity Servers`</span> for deployment.  It also has links to the internal system deployment documentation within the system when the OTA bundle is delivered to the <span style="color:red;font-weight:700;font-size:14px;opacity: 1.0;">`product in the field`</span>. 

This document will also show how the `configurations, capabilities and software` are coupled together for `Subsystems` such as User Interface Asemblies, Main Control Assemblies and Auxiliary Control Assemblies, thus allowing Subsystems to be verified and validated.  

In addition to Subsystems verification this document will define the `Systems` verification and validation for coupling all electronics with loads, sensors and switches for systems verification and validation to allow for `Full System Over the Air Updates`.  

At each stage of development, verification and validation this will require subsystem and systems items to be delivered to a Production Release Process, upon completion of verification and validation.

## Glossary
[Glossary](https://sdlcwiki.electrolux.com/pages/viewpage.action?spaceKey=ASTUESWA&title=Glossary+@+ota)

## Stakeholder Requirements

1. As a User I want to be able to remotely push software updates that increase the security, performance and/or capabilities of a single appliance or an ecosystem of appliances.
1. As a User I want to be able to stay secure & ​up-to-date with the latest features, so I can enjoy my product longer with new features throughout the life of the product.
1. As a User I want to be able to add and remove apps from my product to tailor my product to my specific usage patterns and needs, as my life changes.
1. As a User I should be able to choose when and which updates I want to apply to my product, based on my current lifestyle.
1. As a User I should be able to apply full or partial updates at my convenience and manage the applications on my product tailoring to my specific interaction patterns and needs, allowing more flexiblity, easier use and simplifying my daily activities.
1. As a User I should have a recovery mechanism such as Factory Defaults to return my product to a usable condition should an outage occur such as power, internet service provider, or WiFi Network.
1. As a User I expect the full software update process from start (Time of Initiation) to end (Product is ready to use post software update) to take no more than 10 minutes, as these are my expectation from other devices I currently use.


## Kattegatt PoC
<p align="center">
  <img width="1200" src="../images/ucc_electrical_electronics_system_design.jpg">
  </p>

<!-- Notes

-->

## Types of Updates
1. Application 
1. Partial
1. Full 

An `Application` update is the application interface that the consumer will specifically interact with graphically and behaviorally.  This application is the same as the type of application you have on your mobile device when you download an application to interact with.  You can add or delete it; however, does not require you to also download the Operating System with each application download.

A `Partial` update is a software update of the microservices tech stack that requires an update without updating the entire software operating system and is done by doing a differential analysis of the files on the product against the files being updatind and only updating the files in the Operating System that require updates.

A `Full` update is a software update of the entire Operating System by updating a secondary partition for `flip flopping` or erasing, formatting, and writing the new operating system update completely.  This will require more time; however, is needed for those customers who have not connected and updated their appliances regularly and require to just update from the initial update to the new update or for those who need to recover their products from it's original factory software to the latest version.


>**NOTE:**  These software Updates can be either Operating System, Configurations, Capabilties, Applications, Embeded RTOS, or anything related to the Tech Stack, including Low Level Programming Languages to High Level Programming Languages and Configuration Parameters.


## Design Team Consumer Experience and Interaction

### Consumer Interaction Sequence Diagram

![Consumer Interaction Sequence Diagram](../Over%20the%20Air%20Updates/Document%20Formats/out/user_interaction_sequence_diagram/user_interaction_sequence.png)

These are the links to the Design Teams Graphical Assets and Experiences as it pertains to the Over The Air Process on the Appliance Device and on the Mobile Device.


- [OTA Sharepoint Link](https://electrolux.sharepoint.com/:p:/r/sites/GlobalHMIUIStrategy/Shared%20Documents/Design/01%20Presentations/2022%20Sprint%20Reviews/Valhalla%20-%20Sprint%2017-18%20-%20LT%20OTA.pptx?d=w73e109c044eb45a48356c5eddb6070d2&csf=1&web=1&e=ogmhcq&nav=eyJzSWQiOjIxNDc0NzA4ODMsImNJZCI6MjgwNzM2NTczMn0)
- [OTA Figma Link](https://www.figma.com/file/nRlexG1QvxoKLKHnpmi89T/Pattern---OTA-updates?node-id=0-1&t=yd63SKpWlQey2TDx-0)
- [OTA Framer Link - Pending]()

## Software Team Delivery Process and Tool Chain
This is the process as defined by the `SQA (Software Quality Assurance)` Process Owner.  This [presentation](https://electrolux-my.sharepoint.com/:p:/r/personal/francesco_giorgetti_electrolux_com/Documents/File%20di%20chat%20di%20Microsoft%20Teams/PoC_CICD_24Mar23.pptx?d=wfb85134533c94cc5b1b299dd8b17e390&csf=1&web=1&e=SdDVeq) shows the process of micro services from contributors are pushed to the Continuous Development and Continuous Integration Services.  In addtiion it shows how code is checked in and to what service or tool, the build process, the test process, and then release of software services to be tested in Subsystems with Configurations.
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


## Over the Air Overall Process

This should reflect the Overall Process for the Over the Air Update.  Starting from the top left corner of the image below.
<p align="center">
  <img width="1200" src="../Over%20the%20Air%20Updates/Document%20Formats/out/software_config_check_in/software_config_check_in.png">
  </p>

1. Software Engineering Checks In Software.
1. Systems Engineering Checks In Configurations and Capabilties for the product configurations and capabilities that will work with the Software Stack.
1. RTE will build the software and configurations and capabilities together and release to each subsystem for testing.
1. Upon all Subsystems and interfaces of those subsystems being tested and passed their respective test plans those files will be released to a production version for Bill of Material Control.
1. Systems Engineers will build the System Bundle that will include all the subsystem items released (Software, Configurations, Capabilties and Software Bundle Script) and test the programming process for deploying System Updates.  This can be done wirelessly or wired to the system to validate the systems update capabilties.
1. Upon System Validations and test plans passed this software bundle will be released to a production version for Bill of Material Control.
1. From the Producton version within the revision control system this software bundle will then be deployed to the server for release to Beta or all consumers.
1. Once on the server the scheduler will schedule deliver to the consumers, coordinated with consumer acceptance, if required.



<p align="center">
  <img width="1200" src="../images/over_the_air_overall_process.jpg">
  </p>

<!-- Notes

-->


## Software Team Tech Stack MicroServices Delivery
- Software Check in per the process as defined by SQA.
- Continuous Integration and Development servers build the software, identifying build issues and aligning to the scripts for software delivery.
- Software to be built, tested, and promoted based on business needs for development, test, and release of the software packages.

<p align="center">
  <img width="800" src="../images/tech_stack_delivery_teams.jpg">
  </p>

<!-- Notes

-->


## User Interface Software Builds
- This is a specific release for User Interface Assemblies to conduct Hardware in Loop Testing.

<p align="center">
  <img width="800" src="../images/user_interface_sw_builds.jpg">
  </p>

<!-- Notes

-->

## Main Control Software Builds
- This is a specific release for Main Control Assemblies to conduct Hardware in Loop Testing.

<p align="center">
  <img width="800" src="../images/main_control_sw_builds.jpg">
  </p>

<!-- Notes

-->

## Auxiliary Boards Software Builds
- This is a specific release for Auxiliary Control Assemblies to conduct Hardware in Loop Testing.

<p align="center">
  <img width="800" src="../images/auxiliary_boards_sw_builds.jpg">
  </p>

<!-- Notes

-->

## Connectivity Boards Software Builds
- This is a specific release for Connectivity Control Assemblies to conduct Hardware in Loop Testing.

<p align="center">
  <img width="800" src="../images/auxiliary_boards_sw_builds.jpg">
  </p>

<!-- Notes

-->

## Full System Testing
- Full System Verification Testing to validate software, configurations and capabilites are built and aligned to the performance functions of the Full System.  This includes `Loads` (Motors, Heaters, Pumps, etc.), `Sensors` (RTD, NTC, PTC, Hall Effect, Speed, etc.), and `Switches` (Door Lock, Door State, Centrifugal, etc.).
- Full System Testing also includes verifying the Software OTA transfers, updates and deploys properly in a testing environment.

<p align="center">
  <img width="1000" src="../images/ota_bundle_delivery.jpg">
  </p>

<!-- Notes

-->

## Cloud Delivery Method

This is defined by the connectivity cloud team of Principal Architect, Connectivity and Lead System Architect, Connectivity and reflects when the physical assets of software and configuration are delivered to the connectivity team how they deliver to the server for OTA deployment.

<p align="center">
  <img width="500" src="../images/cloud_deployment_mechanism.jpg">
  </p>

<!-- Notes

-->

## Electrical System Update
Below are the links to the Confluence page pertaining to the Over the Air Process. [Over The Air Connectivity @ OTA](https://sdlcwiki.electrolux.com/display/ASTUESWA/Over-The-Air+Connectivity+@+ota) Confluence Page.
<p align="center">
  <img width="1000" src="../images/electrical_system_update_sequence.jpg">
  </p>

<!-- Notes

-->

## Example json Bundle Script
```json
{"PNC": "",
"Serial_Number":"",
"Previous_System_CRChecksum":"",
"New_System_CRChecksum":"",
"Number_Of_Modules_To_Program":"",
"System_Modules":
    {
    "ANC_001":
        {
        "ANC_Node_Number":"",
        "Micro_Supplier":"",
        "Micro_Family":"",
        "Micro_Number":"",
        "Previous_ANC":
            {
            "Previous_ANC_Part_Number":"",
            "Previous_ANC_Version":"",
            "Previous_ANC_Checksum":""
            },
        "New_ANC":
            {
            "New_ANC_Part_Number":"",
            "New_ANC_Version":"",
            "New_URL":"",
            "New_ANC_Checksum":""
            }
        },
    "ANC_002":
        {
        "ANC_Node_Number":"",
        "Micro_Supplier":"",
        "Micro_Family":"",
        "Micro_Number":"",
        "Previous_ANC":
            {
            "Previous_ANC_Part_Number":"",
            "Previous_ANC_Version":"",
            "Previous_ANC_Checksum":""
            },
        "New_ANC":
            {
            "New_ANC_Part_Number":"",
            "New_ANC_Version":"",
            "New_URL":"",
            "New_ANC_Checksum":""
            }
        },
    "ANC_003":
        {
        "ANC_Node_Number":"",
        "Micro_Supplier":"",
        "Micro_Family":"",
        "Micro_Number":"",
        "Previous_ANC":
            {
            "Previous_ANC_Part_Number":"",
            "Previous_ANC_Version":"",
            "Previous_ANC_Checksum":""
            },
        "New_ANC":
            {
            "New_ANC_Part_Number":"",
            "New_ANC_Version":"",
            "New_URL":"",
            "New_ANC_Checksum":""
            }
        }
    }
}


```

## Dispatching Deployment

[Over the Air Connectivity @ OTA](https://sdlcwiki.electrolux.com/pages/viewpage.action?spaceKey=ASTUESWA&title=Over-The-Air+Connectivity+@+ota)


[Reprogramming Mechnanism](https://sdlcwiki.electrolux.com/display/ASTUESWA/Overview+@+ota)

1. [Bootloader](https://sdlcwiki.electrolux.com/display/ASTUESWA/Overview+@+ota) - Used to reset, erase and program the specific software for a specific micro.
1. [Programming Agent]() - Used to Dispatch specific software to the specific node to be reprogrammed.
1. [Scribe](https://sdlcwiki.electrolux.com/display/ASTUESWA/Overview+@+ota) - Ask Lucio is this would be something like your experience using FIT Table for setting partition areas to program specific sectors or pages based on the FIT Table for doing partial updates?
1. [Bridge](https://sdlcwiki.electrolux.com/display/ASTUESWA/Overview+@+ota) - Used to allow the Programming Agent to reach other nodes in the system beyond the direct connection the Programming Agent or Master Programmer may have acess to.
1. [Open Points](https://sdlcwiki.electrolux.com/display/ASTUESWA/Open+points+@+ota)

<!--
Comments:

## UML Definition

### Activity Diagram


![Activity Diagram](../Over%20the%20Air%20Updates/Document%20Formats/out/activity%20diagram/activity%20diagram.png)



How are you packaging the bundle?

What are you using as a mechanism to extract bundle when built with bundle? Script?

How does the system extract the bundle when system receives bundle?

How does each subsystem validate its compatible?

Using DAAS as point to point for nodes on bus one at a time?

Is there an order to the update?

Are you verifying node#?

Micro#?

Programming Agent unpackaged using script. PA. Fetches full package to Wi-Fi node. Fetches each node via URL for specific software to be programmed within script. 


-->

