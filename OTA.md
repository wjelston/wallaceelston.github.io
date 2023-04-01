Over The Air Update

## Table of Contents

1. [Document Synopsis](#document-synopsis)
1. [Terms and Definitions](#terms-and-definitions)
1. [Stakeholder Requirements](#stakeholder-requirements)
1. [Kattegatt PoC](#kattegatt-poc)
1. [Software Team Delivery Process and Tool Chain](#software-team-delivery-process-and-tool-chain)
1. [Software Team Tech Stack MicroServices Delivery](#software-team-tech-stack-microservices-delivery)
1. [Over the Air Overall Process](#over-the-air-overall-process)
1. [User Interface Software Builds](#user-interface-software-builds)
1. [Main Control Software Builds](#main-control-software-builds)
1. [Auxiliary Boards Software Builds](#auxiliary-boards-software-builds)
1. [Connectivity Board Software Builds](#connectivity-boards-software-builds)
1. [Bundle Script](#bundle-script)
1. [json Bundle Script](#json-bundle-script)




## Document Synopsis


## Terms and Definitions
UBD - Unified Bundle Descriptor
URL - Universal Resource Locator
ANC is a Part Number for a specific component in TeamCenter
PNC is the Overall Model Number for a specific BOM to be built and distributed to our consumer

## Stakeholder Requirements

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

## Software Team Delivery Process and Tool Chain

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
<p align="center">
  <img width="800" src="./images/user_interface_sw_builds.jpg">
  </p>

<!-- Notes

-->

## Main Control Software Builds
<p align="center">
  <img width="800" src="./images/main_control_sw_builds.jpg">
  </p>

<!-- Notes

-->

## Auxiliary Boards Software Builds
<p align="center">
  <img width="800" src="./images/auxiliary_boards_sw_builds.jpg">
  </p>

<!-- Notes

-->

## Connectivity Boards Software Builds
<p align="center">
  <img width="800" src="./images/auxiliary_boards_sw_builds.jpg">
  </p>

<!-- Notes

-->

## Bundle Script
<p align="center">
  <img width="1000" src="./images/ota_bundle_delivery.jpg">
  </p>

<!-- Notes

-->

## Cloud Delivery Method
<p align="center">
  <img width="500" src="./images/cloud_deployment_mechanism.jpg">
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