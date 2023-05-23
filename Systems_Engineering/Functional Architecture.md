Functional Architecture

## Cross Category
	1. Sensors
	2. Loads
	3. Switches
	4. Temperature
	5. Standby
	6. Programming and Reprogramming 
	
		1. Factory
		2. Service
		3. ECM
		4. Connectivity OTA
	7. Connectivity 
	
		1. Provisioning
		2. Claiming
		3. Security and Privacy
		4. OTA 3.0
	8. UI/HMI Configurations (Keys, Indicators, Tuning Performance, Behavior)
	9. Power Loss and Recovery
	10. Initialization and Configuration
	11. Control Board Configurations (Loads, Sensors, Switches)
	12. Appliance States and Modes
	13. Operations
	14. Operands (Start and Cancel)
	15. Input Power requirements (Globally)
	16. Reboot
	17. Restore Factory Default
	18. Error Codes/Alarms
	19. Process = Cycle Performance 
	
		1. Cycles
		2. Phases
		3. Sequences/Cycle Design?
		4. Algorithms
		5. State Machine
		6. Cycle Design
		7. Parameters
	20. Verification and Validation 
	
		1. Performance team requirements (tuning product requirements to drive development speed and tools)
		2. Lab Testing
		3. Factory Testing and Manual Verification
		4. Service Testing and Automatic Verification
	21. Control Settings 
	
		1. General 
		
			1. About 
			
				1. Control Version 
				
					1. HMI Software Version
					2. HMI Configuration Version
					3. NIU Software Version
					4. NIU Configuration Version
					5. Control Board Software Version
					6. Control Board Configuration Version
				2. Control Board
			2. Software Update 
			
				1. Latest Software Version
				2. Update Software Version, if available 
				
					1. Yes
					2. No
		2. Connectivity 
		
			1. Wireless Network 
			
				1. Features 
				
					1. Smart Grid 
					
						1. Opt In
						2. Opt Out
					2. Data Analytics 
					
						1. Opt In
						2. Opt Out
				2. WiFi 
				
					1. On/Off
					2. Status: 
					
						1. Provisioning
						2. Deprovisioning
						3. WiFi Network Connected
						4. WiFi Signal Strength
				3. BLE 
				
					1. On/Off
					2. BLE Network 
					
						i. Pair
						ii. Unpair
			2. Time of Day 
			
				1. 12 Hour/24 Hour
				2. Time of Day Manual
				3. Time of Day Automatic (Connected Appliances Only)
			3. Audio 
			
				1. Volume Level
				2. End of Cycle Tone
				3. Key Press Tone
			4. Display & Brightness 
			
				1. Backlight Brightness
				2. Display Theme
			5. Control Lock 
			
				1. Control Locked
				2. Control Unlocked
			6. Calibration: 
			
				1. Cooking 
				
					1. Temperature Offset
				2. Induction
				3. Ovens
				4. Hoods
				5. Laundry
				6. Washers
				7. Dryers
				8. Dishwashers
				9. Refrigerators
		3. Modes: 
		
			1. Sabbath Mode
			2. Demo Mode
			3. Service Mode 
			
				1. Diagnostics Auto Routine
				2. Results from Auto Routine
				3. Error Failure Codes and Descriptions
				4. System Reboot
			4. Factory Mode/Verification and Validation Mode 
			
				1. Diagnostics Manual
				2. Turn On Loads
				3. Read Sensors/Switches
				4. Restore Factory Reset
## FPP Category Hobs
## FPP Category Hoods
	• Fan Speed 
	
		• Low
		• Medium
		• High
	• Lighting 
	
		•  
## FPP Category Ovens
Functional Requirements:
	• Features with Systems UML diagram (User <--> HMI <--> Access Point <--> Cloud <--> Main Product Controls
	
		• Bake with UML Diagram for how information flows from HMI to Cloud
		• Broil
		• Convection
		• Self Clean
		• Diagnostics Loads, Sensors, Switches
		
			• Loads ON / OFF (Heating Element Bake, Heating Element Broil, Motor Door Lock)
			• Sensors (Read=Get_Status) RTD, NTC, Hall Effect
			• Switches (Read=Get_Status) Door, Door Lock, Limit,
## WET Category Washer
## WET Category Dryer
## WET Category Dishwasher
## FPS Category Refrigeration
## Open Discussion
	
		 
	• Systems Initialization
	• Systems Configuration
	• Systems Modes
	• Systems Selects Cycles
	• Systems Selects Options
	• Systems User Settings
## Control Settings
	1. Control Settings 
	
		1. General 
		
			1. About 
			
				1. Control Version 
				
					1. HMI Software Version
					2. HMI Configuration Version
					3. NIU Software Version
					4. NIU Configuration Version
					5. Control Board Software Version
					6. Control Board Configuration Version
				2. Control Board
			2. Software Update 
			
				1. Latest Software Version
				2. Update Software Version, if available 
				
					1. Yes
					2. No
		2. Connectivity 
		
			1. Wireless Network 
			
				1. Features 
				
					1. Smart Grid 
					
						1. Opt In
						2. Opt Out
					2. Data Analytics 
					
						1. Opt In
						2. Opt Out
				2. WiFi 
				
					1. On/Off
					2. Status: 
					
						1. Provisioning
						2. Deprovisioning
						3. WiFi Network Connected
						4. WiFi Signal Strength
				3. BLE 
				
					1. On/Off
					2. BLE Network 
					
						i. Pair
						ii. Unpair
			2. Time of Day 
			
				1. 12 Hour/24 Hour
				2. Time of Day Manual
				3. Time of Day Automatic (Connected Appliances Only)
			3. Audio 
			
				1. Volume Level
				2. End of Cycle Tone
				3. Key Press Tone
			4. Display & Brightness 
			
				1. Backlight Brightness
				2. Display Theme
			5. Control Lock 
			
				1. Control Locked
				2. Control Unlocked
			6. Calibration: 
			
				1. Cooking 
				
					1. Temperature Offset
				2. Induction
				3. Ovens
				4. Hoods
				5. Laundry
				6. Washers
				7. Dryers
				8. Dishwashers
				9. Refrigerators
		3. Modes: 
		
			1. Sabbath Mode
			2. Demo Mode
			3. Service Mode 
			
				1. Diagnostics Auto Routine
				2. Results from Auto Routine
				3. Error Failure Codes and Descriptions
				4. System Reboot
			4. Factory Mode/Verification and Validation Mode 
			
				1. Diagnostics Manual
				2. Turn On Loads
				3. Read Sensors/Switches
				4. Restore Factory Reset
