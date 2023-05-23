Unified Data Architecture

__This document is an example, and not specific to the implementation of the UDA Initiative.__



As a basis for Communications and using the OSI Model alignment of the Internal Communications bus for accountability are below:

[Wikipedia - 7 Layers OSI Model](https://en.wikipedia.org/wiki/OSI_model)

1.  Application layer (Unified Data Architecture - API)
1.  Presentation layer (Unified Data Architecture - OpCode/Data)
1.  Session layer (Unified Data Architecture - Node List/SAP)
1.  Transport layer (MACS-EVO)
1.  Network layer (MACS-EVO)
1.  Data link layer (MACS-EVO)
1.  Physical layer (Single Wire UART EDM)

**Layers 4 - 7 are coverred** in the [MACS-EVO Protocol Specification-SP000012530](./documents/SP000012530A-MS-GLOBAL-MACS%20Evo.docx) pulled directly from TeamCenter; however, this is only reference and most recent revision should be reviewed from TeamCenter.


Layers 1 - 3 are covered in this document as part of the Unified Data Architecture Initiative.

API.OpCode.SAP.<span style="color:red;font-weight:500;font-size:15px">__.DATA_1.DATA_2...Data_N.__</span>CRC1.CRC2



# Application Layer
## Definition API: 
[API - Wikipedia](https://en.wikipedia.org/wiki/API)

## Cross Category API <a name="cross-category-api"></a>
- API_001 (Supplier_Information)

|API|OpCode|SAP|Data1|Data2|Data3|Data4|Data5|Data6|Data7|Data8|Data9|Data10|Data11|Data12|Data13|Data14|Data15|Data16|Data17|Data18|Data19|Data20|
|---|----|-----|-----|----|-----|-----|----|-----|-----|----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
|001|[Opcode](#opcode)|[SAP](#sap)|[Supplier_Name](#supplier_name)|[Supplier_Location](#supplier_location)|[Build_Date](#build_date)|[Build_Date](#build_date)|[Build_Date](#build_date)|[Build_Date](#build_date)|[Build_Date](#build_date)|[Build_Date](#build_date)|[Build_Date](#build_date)|[Build_Date](#build_date)|[Test_Date](#test_date)|[Test_Date](#test_date)|[Test_Date](#test_date)|[Test_Date](#test_date)|[Test_Date](#test_date)|[Test_Date](#test_date)|[Test_Date](#test_date)|[Test_Date](#test_date)|[Test_Result](#test_result)


- API_002 (Manufacturing_Information)

|API|OpCode|SAP|Data1|Data2|Data3|Data4|Data5|Data6|Data7|Data8|Data9|Data10|Data11|Data12|Data13|Data14|Data15|
|---|----|-----|-----|----|-----|-----|----|-----|-----|----|-----|-----|-----|-----|-----|-----|-----|
|002|[Opcode](#opcode)|[SAP](#sap)|[PNC_Number](#pnc)|[ANC_Number](#anc)|


- API_003 (Sensor_Status)

|API|OpCode|SAP|Data1|Data2|Data3|Data4|Data5|Data6|Data7|Data8|Data9|Data10|Data11|Data12|Data13|Data14|Data15|
|---|----|-----|-----|----|-----|-----|----|-----|-----|----|-----|-----|-----|-----|-----|-----|-----|
|003|[Opcode](#opcode)|[SAP](#sap)|[RTD_Temperature_1](#rtd_temperature)|[RTD_Temperature_2](#rtd_temperature)|[NTC_Temperature_1](#ntc_temperature)|[NTC_Temperature_2](#ntc_temperature)|[PTC_Temperature_1](#ptc_temperature)|[PTC_Temperature_2](#ptc_temperature)|

- API_004 (Switch_Status)

|API|OpCode|SAP|Data1|Data2|Data3|Data4|Data5|Data6|Data7|Data8|Data9|Data10|Data11|Data12|Data13|Data14|Data15|
|---|----|-----|-----|----|-----|-----|----|-----|-----|----|-----|-----|-----|-----|-----|-----|-----|
|004|[Opcode](#opcode)|[SAP](#sap)|[Door_State_1](#door_state)|[Door_State_2](#door_state)|[Door_State_3](#door_state)|[Door_State_4](#door_state)|[Door_Lock_State_1](#door_lock_state)|[Door_Lock_State_2](#door_lock_state)|[Door_Lock_State_3](#door_lock_state)|[Door_Lock_State_4](#door_lock_state)|

- API_005 (Load_Status)

|API|OpCode|SAP|Data1|Data2|Data3|Data4|Data5|Data6|Data7|Data8|Data9|Data10|Data11|Data12|Data13|Data14|Data15|
|---|----|-----|-----|----|-----|-----|----|-----|-----|----|-----|-----|-----|-----|-----|-----|-----|
|005|[Opcode](#opcode)|[SAP](#sap)|[Low Power Loads Bitfield-Upper Byte](#low_power_loads_bitfield_upper_byte)|[Low Power Loads Bitfield-Lower Byte](#low_power_loads_bitfield_lower_byte)|[High Power Loads Bitfield-Upper Byte](#high_power_loads_bitfield_upper_byte)|[High Power Loads Bitfield-Lower Byte](#high_power_loads_bitfield_lower_byte)|[Double Line Break Bitfield](#double_link_break)|[]()|[]()|

- API_010 (Cycle_Information)

|API|OpCode|SAP|Data1|Data2|Data3|Data4|Data5|Data6|Data7|Data8|Data9|Data10|Data11|Data12|Data13|Data14|Data15|
|---|----|-----|-----|----|-----|-----|----|-----|-----|----|-----|-----|-----|-----|-----|-----|-----|
|010|[Opcode](#opcode)|[SAP](#sap)|[State](#state)|[Mode](#mode)|[Cycle_Index]()|[]()|

# Session Layer
## Node List:
[Communications - Node Addressing](https://electrolux.jamacloud.com/perspective.req#/containers/142810?projectId=175)


## SAP: <a name="sap"></a>

## SAP Actions:
|Hex Value| Description|
|---|---|
|0x01|Send and Forget|
|0x02|Message Received Response|
|0x03|Application Respone|


Synchronous communication is invoked by request and response operation and process output is returned immediately after the operation. In general terms, you can say that a synchronous scenario is when a sender process sends a request to the receiver and waits for a response. If an error occurs at the receiver side, the sender application is responsible for sending the message again.

- **Application Error** − There is an error at the receiver end while processing a message and the sender is not aware about this error and keeps waiting for the reply.
- **Network level Error** − In this error, there is an error in communication network between the sender and the receiver. Sender is not aware about this and the message is stuck in between and the sender waits till the operation timeout.
- **Error in Response Message** − In this scenario, an error occurs and the response message gets stuck in between and sender keeps on waiting

In Asynchronous Communication, you add an intermediate system or a middleware between two systems. When a Sender Application sends a request, it does not wait for the Receiver Application to send the response. If there is a failure due to some reason, the middleware is responsible for resending the message. If required, the receiving system can send a response back to Sender as a separate asynchronous call.

# Presentation Layer
## OpCode:  <a name="opcode"></a>
Type: unsigned char

|Hex Value| Description|
|---|---|
|0x01|Publish or Post Message|
|0x02|Write or Put Message|
|0x03|Read or Get Message|
|0x04|Remove or Delete Message|


## Data:
### Cross Category Data:
#### [State](https://electrolux.jamacloud.com/perspective.req#/containers/28711?projectId=175) <a name="state"></a>
Type: unsigned char

|Hex Value| Description|
|---|---|
|0x01|Disconnnected State|
|0x02|Initialization State|
|0x03|Standby State|
|0x04|Delay Start State|
|0x05|Active State|
|0x06|Selection State|
|0x07|Running State|
|0x08|Paused State|
|0x09|Completed State|
|0x0A|Error State|

#### [Mode](https://electrolux.jamacloud.com/perspective.req#/containers/28711?projectId=175) <a name="mode"></a>
Type: unsigned char

|Hex Value| Description|
|---|---|
|0x01|Off Mode|
|0x02|User Mode (Default Mode)|
|0x03|Demo Mode|
|0x04|Sabbath Mode|
|0x05|Programming Mode|
|0x06|Diagnostics Mode|

#### Sensors: <a name="sensors"></a>

- ##### RTD Temperature <a name="rtd_temperature"></a>
    - [Temperature Analysis](https://sdlcwiki.electrolux.com/display/GTCSI/Temperature+Data+Analysis)
    - [Temperature Range](https://sdlcwiki.electrolux.com/display/GTCSI/Temperature+Data+Analysis)
    - [Temperature Units](https://electrolux.jamacloud.com/perspective.req#/items/26277)
    - [Temperature Resolution](https://sdlcwiki.electrolux.com/display/GTCSI/Temperature+Data+Analysis)
    - [Temperature Accuracy]()

- ##### NTC Temperature <a name="ntc_temperature"></a>

- ##### PTC Temperature <a name="ptc_temperature"></a>

- ##### Humidity​: <a name="relative_humidity"></a>
    - [Humidity Analysis](https://sdlcwiki.electrolux.com/display/GTCSI/Humidity+Data+Analysis)
    - [Humidity Range](https://sdlcwiki.electrolux.com/display/GTCSI/Humidity+Data+Analysis)
    - [Humidity Units](https://sdlcwiki.electrolux.com/display/GTCSI/Humidity+Data+Analysis)
    - [Humidity Resolution](https://sdlcwiki.electrolux.com/display/GTCSI/Humidity+Data+Analysis)
    - [Humidity Accuracy](https://sdlcwiki.electrolux.com/display/GTCSI/Humidity+Data+Analysis)

#### Switches: <a name="switches"></a>
- ##### Door State​: <a name="door_state"></a>
    - [Door State Analysis](https://sdlcwiki.electrolux.com/display/GTCSI/Data+List)
    - [Door State Range](https://sdlcwiki.electrolux.com/display/GTCSI/Data+List)
    - [Door State Units](https://sdlcwiki.electrolux.com/display/GTCSI/Data+List)
    - [Door State Resolution](https://sdlcwiki.electrolux.com/display/GTCSI/Data+List)
    - [Door State Accuracy](https://sdlcwiki.electrolux.com/display/GTCSI/Data+List)

- ##### Door Lock State​: <a name="door_lock_state"></a>
    - [Door Lock State Analysis](https://sdlcwiki.electrolux.com/display/GTCSI/Data+List)
    - [Door Lock State Range](https://sdlcwiki.electrolux.com/display/GTCSI/Data+List)
    - [Door Lock State Units](https://sdlcwiki.electrolux.com/display/GTCSI/Data+List)
    - [Door Lock State Resolution](https://sdlcwiki.electrolux.com/display/GTCSI/Data+List)
    - [Door Lock State Accuracy](https://sdlcwiki.electrolux.com/display/GTCSI/Data+List)

#### PNC <a name="pnc"></a>
Type: unsigned char
15 bytes

- Product Number Code --> link to TeamCenter Released Version of Product Number Code Specification
- 15 Characters

#### ANC  <a name="anc"></a>
Type: unsigned char
15 bytes

- Article Number Code  --> link to TeamCenter Released Version of  Article Number Code Specification
- 15 Characters

#### Supplier_Name <a name="supplier_name"></a>
Type: unsigned char

|Hex Value|Description|
|---|---|
|0x01|Jabil|
|0x02|Flextronics|
|0x03|H&T|

#### Supplier_Location <a name="supplier_location"></a>
Type: unsigned char

|Hex Value|Description|
|---|---|
|0x01|Mexico|
|0x02|Hungary|
|0x03|China|

#### Build_Date  <a name="build_date"></a>
Type: unsigned long
Length of Data: 8 bytes
Format:  Julian Date

#### Test_Date <a name="test_date"></a>
Type: unsigned long
Length of Data: 8 bytes
Format:  Julian Date

#### Test_Result <a name="test_result"></a>
Type: unsigned char

|Hex Value|Description|
|---|---|
|0x00|No Testing Completed|
|0x01|Testing Passed|
|0x02|Testing Failed|

#### Loads Status <a name="load_status"></a>
##### Low Power Loads Bitfield- Upper Byte <a name="low_power_loads_bitfield_upper_byte"></a>
Type: unsigned char

|Hex Value|K8|K7|K6|K5|K4|K3|K2|K1|Description|
|---|---|---|---|---|---|---|---|---|---|
|0x00|0|0|0|0|0|0|0|0|No Loads are On|
|0x01|0|0|0|0|0|0|0|1|K1 On|
|0x02|0|0|0|0|0|0|1|0|K2 On|
|0x03|0|0|0|0|0|0|1|1|K1 and K2 On|
|0x04|0|0|0|0|0|1|0|0|K3 On|
|0x05|0|0|0|0|0|1|0|1|K1 and K3 On|
|0x06|0|0|0|0|0|1|1|0|K2 and K3 On|
|0x07|0|0|0|0|0|1|1|1|K1, K2 and K3 On|
|0x08|0|0|0|0|1|0|0|0|K4 On|
|0x09|0|0|0|0|1|0|0|1|K1 and K4 On|
|0x0A|0|0|0|0|1|0|1|0|K1 and K2 On|
|0x0B|0|0|0|0|1|0|1|1|K1, K2 and K4 On|
|0x0C|0|0|0|0|1|1|0|0|K1 and K3 On|
|0x0D|0|0|0|0|1|1|0|1|K1, K3, and K4 On|
|0x0E|0|0|0|0|1|1|1|0|K2, K3 and K4 On||
|0x0F|0|0|0|0|1|1|1|1|K1, K2, K3 and K4 On|
|0x10|0|0|0|1|0|0|0|0|K5 On|
|0x11|0|0|0|1|0|0|0|1|K5 and K1 On|
|0x12|0|0|0|1|0|0|1|0|K5 and K2 On|
|0x13|0|0|0|1|0|0|1|1|K5, K1, and K2 On|
|0x14|0|0|0|1|0|1|0|0|K5 and K3 On|
|0x15|0|0|0|1|0|1|0|1|K5, K1, and K3 On|
|0x16|0|0|0|1|0|1|1|0|K5, K3, and K2 On|
|0x17|0|0|0|1|0|1|1|1|K5, K3, K2, and K1 On|
|0x18|0|0|0|1|1|0|0|0|K5 and K4 On|
|0x19|0|0|0|1|1|0|0|1|K5, K4 and K1 On|
|0x1A|0|0|0|1|1|0|1|0|K5, K4, and K2 On|
|0x1B|0|0|0|1|1|0|1|1|K5, K4, K2, and K1 On|
|0x1C|0|0|0|1|1|1|0|0|K5, K4 and K3 On|
|0x1D|0|0|0|1|1|1|0|1|K5, K4, K3, and K1 On|
|0x1E|0|0|0|1|1|1|1|0|K5, K4, K3, and K2 On|
|0x1F|0|0|0|1|1|1|1|1|K5, K4, K3, K2 and K1 On|

##### Low Power Loads Bitfield - Lower Byte <a name="low_power_loads_bitfield_lower_byte"></a>
For Expansion if needed.

##### High Power Loads Bitfield-Upper Byte <a name="high_power_loads_bitfield_upper_byte"></a>


##### High Power Loads Bitfield-Lower Byte <a name="high_power_loads_bitfield_lower_byte"></a>


##### Double Line Break Bitfield <a name="double_link_break"></a>




### Category Data Architecture - Ovens

### Category Data Architecture - Hobs

### Category Data Architecture - Hoods

### Category Data Architecture - Microwaves

### Category Data Architecture - Washer

###  Category Data Architecture - Dryer

### Category Data Architecture - Dishwasher

### Category Data Architecture - Refrigeration


