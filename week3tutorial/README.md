current as at 13 august 2025

https://docs.google.com/document/d/1n7N--D_V7k-Vl2K5-Uea01G0diisov3JBa1yBlSiimE/edit?tab=t.0 


Step 1: Understand and Define the Problem (Analyse)

The objective is to design and simulate a combinational logic circuit for the above seat belt sensor problem. We need to consider the alarm, the sensors in the seat, the sensors in the seat belt and the sensors in the ignition. We need to activate the alarm if the car is started and the passesnegers are not wearing seat belts (this only applies to the front seats, and they must be occupied for the alarm to sound. (there's no pointactivating an alarm if no seats are occupied)). It is assumed that the system works only as intended and nothing will ever malfunction. For the logic circuit and data table, we also assume that there has be a driver in the car. It does not make sense for there to be a passenger without a driver, regardless of the seatbelt.

Step 2: Organise and Describe the Data


SYMBOL
MEANING
TYPE
ACTIVE LOGIC
DRIV
Driver is in the seat
Input
HIGH 1 (1 = present)
PASS
Passenger is in the seat
input
HIGH 1 (1 = present)
IGN
Ignition switch is ON
Input
HIGH (1 = on)
BELTD
Drivers seatbelt is unfastended
Input
LOW (0 = unfastened)
BELTP
Passengers seatbelt unfastened
Input
LOW (0 = unfastened)
ALARM
Alarm signal (active LOW = sounds when 0)
Output
LOW = ON


Step 3: Plan the Solution (Design the Algorithm)

Repeat for both passenger and driver seats and belts

Very first: check that the car switch ignition (IGN) is on (if the car is running Input is 1)

Check that someone is in the driver seat,
If someone is in the driver seat (DRIV), the input is equal to 1 (HIGH 1)
	If the driver is in the seat, check that he is wearing a seatbelt (BELTD), if they are        wearing a seatbelt, Input is 1, if they are not wearing it, input is zero.
     If IGN equals 1 and DRIV equals 1 and BELTD is 0, then activate car alarm (output 0)






Then

Check that someone is in the passenger seat,
If someone is in the passenger seat (DRIV), the input is equal to 1 (HIGH 1)
	If the passenger is in the seat, check that he is wearing a seatbelt (BELTP), if they are        wearing a seatbelt, Input is 1, if they are not wearing it, input is zero.
     If IGN equals 1 and PASS equals 1 and BELTP is 0, then activate car alarm (output 0)


If seatbelt BELTP and BELTD equals 1, then turn of the car alarm.




If IGN = HIGH

   DRIV = 1 and BELTD = 0


   PASS = 1 and BELTP = 0
Then alarm = LOW (activates)




Truth table


2^n

N = inputs

TRUTH TABLE

INPUT
INPUT
INPUT
INPUT
INPUT
OUTPUT
IGN
DRIV
BELTD
PASS
BELTP
ALARM
