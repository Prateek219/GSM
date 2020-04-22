# GSM : Global System for Mobile Communication
This tutorial describes the way to interface GSM modem with a
microcontroller(Atmega16/32).
## COMPUTER INTERFACE
Hyperterminal, a terminal emulation program is used to connect GSM.

The above program can be found on the following link:

http://www.hilgraeve.com/hyperterminal/

GSM modem is controlled using AT commands.

__AT COMMANDS__

These AT commands have the format of “AT<x><n>”, where “<x>”is the
  
command, and “<n>”is/are the argument(s) for that command.
e.g.
ATD 1234567890; //calls a number

Entire AT command set can be accessed from:

http://www.developer.nokia.com/Community/Wiki/AT_Commands
