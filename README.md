I'm releasing this shade automation demo program as it can provide people with ideas on how they can optimize energy usage in a home.  I've written this code in preparation for receiving some new shade controllers that I will beta testing and then installing in my home.  

The main portion of the program consists of two modules

1.	Sun on Window v3
2.	Shade Automation Control v5

Sun on Window v3 - This module tracks the angle and elevation of the sun throughout the day based on the latitude and longitude of the home.   It also reads an XML formatted data file that describes the windows in a home that have motorized shades including their angle to north and any obstructions that would block the sun from shining through the window into the room.  The module then mathematically determines if the sun is currently shining into each window and outputs this information using a series of digital signals. 

Shade Automation Control v5 - This module uses the output of the Sun on Window module as well as user preferences for how the shade on a specific window should be automated to open and close the shade during the day.  The module gives the user the choice of automating the operation of the shade for:

•	Daylight Harvesting - The shade is opened during the day when the sun is not directly shining into the window to provide indirect light into the room to offset the need for electrical lights
•	Solar Heating - The shade is opened during the day when the sun is shining through the window to leverage the sun to help heat the room and reduce the need for running the heating system.  A temperature limit can be programmed and if the temperature in the room rises above the limit the shade will closed until the temperature drops below a specified number of degrees below the temperature limit.
•	Regulated Solar Heating - In this mode the shade acts as a first stage to the furnace.  When the thermostat calls for heat the shade will be opened to heat the room.  If the room hasn't come up to temperature by a programmable timeout the furnace will then be activated.  Once the thermostat senses that the temperature has risen above the set point the thermostat will stop calling for heat and the programming will close the shade and cease calling for heat from the furnace, if it was turned on.

The operation of the above modules is fully demonstrated in the Shade Automation Control Demo Program.  The program controls 7 shades with varying options for how the shades are automated.  The details of how the program is making decisions can be tracked in SimplDebugger.  

The above modules each have detailed help files to provide full details on their use.

It should be noted that the Sun on Window v3 module currently supports the automation of 20 motorized shades in a home.  A module that supports more than 20 shades can be provided by special request.  

The Sun on Window v3 module and Shade Automation Control v5 module are released as shareware.  That is, they are free for Crestron programmers use on their own automation systems or for a dealer to use on their in house demo system.  However, if you use one, or both, modules on customer systems where you, or the dealer/CSP you work for, will profit from it then I ask for a single payment of $100.  

What you get is 

1.	My thanks
2.	Permission to use the modules on as many client projects as you want
3.	A copy of the Simpl# source code for the Sun on Window Module
4.	Good Karma

You can contact me at jay.m.basen@gmail.com to arrange for payment.

Thanks
Jay Basen
