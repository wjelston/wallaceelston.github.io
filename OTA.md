Over The Air Update

## Table of Contents

1. [Document Synopsis](#document-synopsis)
1. [Glossary](#glossary)
1. [Stakeholder Requirements](#stakeholder-requirements)
1. [Kattegatt PoC](#kattegatt-poc)
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
1. [json Bundle Script](#json-bundle-script)
1. [Dispatching Deployment](#dispatching-deployment)


<!--
Notes:
- Design and Consumer Experience Requirements from Figma, Supernova, Flutter, React, SHAPE for Over the Air Update
- Write up Synopsis
- Share with Saili
- Share with OTA Review this week.
-->


## Document Synopsis

This document includes the microservices release process from the software team, the subsystems process for HIL testing of each subsystem, systems testing for full system testing, and finally OTA Package delivery to the Connectivity Servers for deployment.  It also has links to the internal system deployment documentation within the system when the OTA bundle is delivered to the product in the field.


This document will be the definition for the Process from **`Software`** check in of `micro services`, to the builds for development, test, release for verification and validation.  

This document will also show how the `configurations, capabilities and software` are coupled together for `Subsystems` such as User Interface Asemblies, Main Control Assemblies and Auxiliary Control Assemblies, thus allowing Subsystems to be verified and validated.  

In addition to Subsystems verification this document will define the `Systems` verification and validation for coupling all electronics with loads, sensors and switches for systems verification and validation to allow for `Full System Over the Air Updates`.  

At each stage of development, verification and validation this will require subsystem and systems items to be delivered to a Production Release Process, upon completion of verification and validation.



## Glossary
[Glossary](https://sdlcwiki.electrolux.com/pages/viewpage.action?spaceKey=ASTUESWA&title=Glossary+@+ota)

## Stakeholder Requirements

1. Remotely pushed software packages that increase the security, performance or capabilities of a single appliance or an ecosystem of appliances
1. I want my appliances to stay secure & ​
up-to-date with the latest features, so I can enjoy my product longer
1. As a User I want to be able to update my product to the latest software and configurations updates.
1. As a User I want to be able to enable future capabilities my product may initiatilly not support, by software and configuration updates.
1. As a User I want to be able to add and remove apps from my product to tailor my product to my specific usage and needs.
1. As a User I should be able to choose when and which updates i want to apply to my product.  
1. As a User I should be able to apply full or partial updates.
1. As a User I should have a recovery mechanism such as Factory Defaults to return my product to a usable condition should an outage occur such as power, internet service provider, or WiFi Network.
1. As a User I expect the full software update process from start to end to take no more than 10 minutes, as these are my expectation from other devices I currently use.


## Kattegatt PoC
<p align="center">
  <img width="1200" src="./images/ucc_electrical_electronics_system_design.jpg">
  </p>

<!-- Notes

-->

## Design Team Consumer Experience and Interaction

These are the links to the Design Teams Graphical Assets and Experiences as it pertains to the Over The Air Process on the Appliance Device and on the Mobile Device.

[Sharepoint Link](https://electrolux.sharepoint.com/:p:/r/sites/GlobalHMIUIStrategy/Shared%20Documents/Design/01%20Presentations/2022%20Sprint%20Reviews/Valhalla%20-%20Sprint%2017-18%20-%20LT%20OTA.pptx?d=w73e109c044eb45a48356c5eddb6070d2&csf=1&web=1&e=ogmhcq&nav=eyJzSWQiOjIxNDc0NzA4ODMsImNJZCI6MjgwNzM2NTczMn0)
[Figma Link](https://www.figma.com/file/wZxnB2zvGxjbsCnSkdYx00/Design---OTA-updates?node-id=0-1&t=GSjXDAo0vJzmwF9I-0)
[Framer Link - Pending]()

## Software Team Delivery Process and Tool Chain
This is the process as defined by the `SQA (Software Quality Assurance)` Process Owner.  This presentation shows the process of micro services from contributors are pushed to the Continuous Development and Continuous Integration Services.  In addtiion it shows how code is checked in and to what service or tool, the build process, the test process, and then release of software services to be tested in Subsystems with Configurations.
<!-- Notes

-->
<p align="center">
  <img width="1200" src="./images/ci_cd_process/slide1.jpeg">
  </p>

<p align="center">
  <img width="1200" src="./images/ci_cd_process/slide2.jpeg">
  </p>

  <p align="center">
  <img width="1200" src="./images/ci_cd_process/slide3.jpeg">
  </p>

  <p align="center">
  <img width="1200" src="./images/ci_cd_process/slide4.jpeg">
  </p>


<p align="center">
  <img width="1200" src="./images/ci_cd_process/slide5.jpeg">
  </p>

<p align="center">
  <img width="1200" src="./images/ci_cd_process/slide6.jpeg">
  </p>




## Over the Air Overall Process
This should reflect the Overall Process for the Over the Air Update.
<p align="center">
  <img width="1200" src="./images/over_the_air_overall_process.jpg">
  </p>

<!-- Notes

-->


## Software Team Tech Stack MicroServices Delivery
<p align="center">
  <img width="800" src="./images/tech_stack_delivery_teams.jpg">
  </p>

<!-- Notes

-->


## User Interface Software Builds
- Hardware in Loop Testing
<p align="center">
  <img width="800" src="./images/user_interface_sw_builds.jpg">
  </p>

<!-- Notes

-->

## Main Control Software Builds
- Hardware in Loop Testing
<p align="center">
  <img width="800" src="./images/main_control_sw_builds.jpg">
  </p>

<!-- Notes

-->

## Auxiliary Boards Software Builds
- Hardware in Loop Testing
<p align="center">
  <img width="800" src="./images/auxiliary_boards_sw_builds.jpg">
  </p>

<!-- Notes

-->

## Connectivity Boards Software Builds
- Hardware in Loop Testing
<p align="center">
  <img width="800" src="./images/auxiliary_boards_sw_builds.jpg">
  </p>

<!-- Notes

-->

## Full System Testing
- Full System Verification Testing
<p align="center">
  <img width="1000" src="./images/ota_bundle_delivery.jpg">
  </p>

<!-- Notes

-->

## Cloud Delivery Method

This is defined by the connectivity cloud team of Principal Architect, Connectivity and Lead System Architect, Connectivity and reflects when the physical assets of software and configuration are delivered to the connectivity team how they deliver to the server for OTA deployment.

<p align="center">
  <img width="500" src="./images/cloud_deployment_mechanism.jpg">
  </p>

<!-- Notes

-->

## Electrical System Update

<p align="center">
  <img width="1000" src="./images/electrical_system_update_sequence.jpg">
  </p>

<!-- Notes

-->

## json Bundle Script
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
