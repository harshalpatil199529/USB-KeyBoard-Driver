
Basic Working - I have modified the USB keyboard driver in such a way that when we press the NUMLOCK key the led turns ON and when we press it again the led turns OFF.

Complete Working -

1) MODE1 

- CAPSLOCK is not enabled   => CAPSLOCK LED is initially OFF, letter = Lowercase

- CAPSLOCK is enabled       => CAPSLOCK LED will turn ON,  letter = Uppercase
	
2) MODE2 

for enabling mode 2 we need to press NUMLOCK making sure that CAPSLOCK is OFF

- initially in MODE2: CAPSLOCK is not enabled => CAPSLOCK LED is initially ON, NUMLOCK LED is also ON, letter = Lowercase

- CAPSLOCK is enabled => CAPSLOCK LED turns OFF, NUMLOCK LED is also ON, letter = Uppercase

3) Going from MODE2 to MODE1 

- While CAPSLOCK is not enabled => NUMLOCK is enabled, both NUMLOCK and CAPSLOCK LEDs will turn off, letter = Lowercase

- When CAPSLOCK is enabled     => NUMLOCK is enabled, CAPSLOCK LED will turn ON, NUMLOCK LED will turn OFF, letter = Uppercase
           

