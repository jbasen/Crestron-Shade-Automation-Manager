# Crestron-Shade-Automation-Manager
Simpl# Pro program to automate operation of shades within a building
This is a Simpl# Pro program that was written during the original private beta of Simpl# Pro on Crestron Labs.  The program is designed to automate the opening and closing of window shades in a building to optimize energy management and/or the protection of valuable furnishings from the sun.  

Execution of the program is driven by an xml data file.  The file shade_data.xml should be loaded to the \RM\Main\  folder on the processor.  An example shade_data.xml file is included.  The file contains:

1) Definitions of the shade hardware and gateway hardware(connections to the hardware will be created by the Shade Automation Manager Program)

2) Definitions of Rooms

3) Definition of the Shades within each Room

The program communicates with a main A/V control program through an EISC.  Within the xml file are elements that define which joins on the EISC are used to communicate information, such as, the temperature within the room measured by a Crestron thermostat that is controlled through the AV program.  The program will use thermostat data to decide whether to open or close a shade to assist heating the room if it is cold or to protect the room from the sun if the room is warm.

In the xml file there are attributes for each shade that describe its angle from north, the size of an overhanging eave, and more.  This data is used by the program as it calculates the angle and elevation of the sun and determines if the sun is shining into the window or not.  

The option field in the shade object can have several different entries
"energy_save_optimal" - open/close shade to take advantage of the sun to help heat a room but close for insulation whenever possible
"energy_save_aesthetics" - open/close shade to take advantage of the sun for heating a room but open for view whenever possible
"art_save_optimal" - close whenever sun on window, otherwise open whether it is cloudy or not
"art_save_aesthetics" - close whenever sun on window, otherwise close if it is sunny and open if cloudy

Additional features of the Shade Manual

1) You can manually control each shade from AV program through joins defined in the XML file

2) A digital join is used to define if there is a party taking place, or not (Party_Mode).  If a party is taking place automated shade movements are suspended so they don't disturb the event.  Specific rooms can be set in the XML file to ignore the party flag.  This would be typical for bedrooms that aren't an area where guests would be located.

3) Shades can be organized into groups so, for example, all shades within a room can be programmed to move together.  Groups are defined in the XML file

4) Opening and closing of shades at specific times of the day (including sunrise and sunset) can be defined in the XML file for each shade.  For example, a shade can be programmed to open at 8am, close at 10am, and then start operating automatically based on the option field setting at noon.
