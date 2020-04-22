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

## GSM ATMEGA INTERFACE
 __CONNECTIONS__
GSM is connected to Atmega via MAX 232.




## SMS: Using AT Commands
- Two message modes: PDU and Text
- AT+CMGF=1 //Text Mode

OK
AT+CMGS=“9559753551"
> Hello World<Ctrl>+<Z>
+CMGS: 44
OK


### SAMPLE CODE FOR SENDING AN SMS
```
void sendmessage(char msg[], char num[]);
{
int i=0,j=0;
puts("AT+CMGF=");
putchar(49); // sends the ASCII value of '1'
puts("AT+CMGS=");
putchar('\"');
while(num[i]!='\0')
{
j=(int)num[i];
putchar(j); //sends the ASCII values of the numbers
i++;
}
puts("Hello World");
putchar('26'); //sends the ASCII value of <Ctrl>+<Z>
}
```
