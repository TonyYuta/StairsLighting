# StairsLighting
:Author: yutaka
:Email: anades@yandex.ru
:Date: 08/05/2018
:Revision: version# 149
:License: Public Domain

= Project: Stairs Light

== Step 1: Installation
1. Install RGB Strips on both sides of a stairs
2. Install IR Sensors on a left side of a stairs
3. Assemble Arduino-based Stairs Lights device
4. Connect all sensors, RGB Strips, and power adapters to Stairs Lights device

== Step 2: Assemble the circuit
Assemble the circuit following the diagram layout.png attached to the sketch

== Step 3: Load the code
Upload the code contained in this sketch on to your board

=== Folder structure
....
 sketch123                => Arduino sketch folder
  ├── sketch123.ino       => main Arduino file
  ├── schematics.png      => (optional) an image of the required schematics
  ├── layout.png          => (optional) an image of the layout
  └── ReadMe.adoc         => this file
....

=== License
This project is released under a {License} License.

=== Contributing
To contribute to this project please contact Tony Kagaya tonykagaya<@gmail.com>

=== BOM
Add the bill of the materials you need for this project.

|===
| ID | Part name           | Part number  | Quantity
| R1 | Arduino Uno         |              | 1       
| L1 | Pixel RGB LED Strip |              | 10        
| A1 | Shield Expand IO    |              | 1 
| ID | Part name           | Part number  | 2
| R1 | 650 Resistor        |              | 20       
| L1 | Wires Strip 4 gauge |              | 50        
| A2 | Arduino Box         |              | 1 
| A3 | Obstacle IR Sensor  |              | 14 
| A3 | Socket/screw 8(pair)|              | 3 
| A3 | RTC                 |              | 1 
|===

Features' Hystory:

v.149
08/05/2018
• add new up / down functions
• removed old up / down functions
• changed function scanning sensors: 3 times for each to prevent wrong triggering

v.148
08/04/2018
• change chase_up functions
• set up exact leds qty: Left 129, Right 185

v.147
07/29/2018
• speed up reaction
• change chase_up functions

v.146
07/15/2018
• updating way to retreave sensors' state to speed up reaction
• use an array for sensor states

v.144
07/12/2018
• start using IR sensors
• first and last sensors triggers light

v.143
07/01/2018
• hardware issues vere fixed: for left and right strips signal (d) and GNG were switched
Now:
on left & right strips Green wire is GND, Black wire is signal (d)
• #define L_STRIP_PORT 19
 #define R_STRIP_PORT 20
• int IR_SENSORS[15] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15};
• L strip: 129
• R strip: 185 (140 - one color, rest - other)
• Apply chase_tiny_1, chase_tiny_1, and chase_tiny_3
• temporary use incorrect R_LEDS = 220 to mask issue with R strip at the very top

v.140
11/26/2018
• left strip chanded from 8 to 12 port
• right strip chanded from 9 to 13 port

since port 1 worcs incorrectly all sensors were shifted up:
• IR_SENSOR_01 port changed from 0 to 2 
• IR_SENSOR_01 port changed from 1 to 3 
• IR_SENSOR_01 port changed from 2 to 4 
• IR_SENSOR_01 port changed from 3 to 5 
• IR_SENSOR_01 port changed from 4 to 6 

v.136
11/26/2017
• modes Chase & Chase_tiny were removed

*/
