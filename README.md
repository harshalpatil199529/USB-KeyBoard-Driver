# USB-KeyBoard-Driver

Changing the Functionality of the CAPSLOCK button in the legacy USB Keyboard Driver


In	the	original	driver, the	CAPSLOCK	led	is	turned	on	when	the	CAPSLOCK key	is	pressed the	first	
time	and	is	turned	off	when	it	is	pressed	again, and	is	on	again	when	it	is	pressed	the	next	time,	
and	so	on.	You’ll	change	the	code	to	introduce	two	modes	into	the	driver:	MODE1	and	MODE2.		
When	the	driver	starts	functioning,	it	is	in	MODE1,	in	which CAPSLOCK	will	be	handled	as	usual.	
MODE2	will	be	activated	when	NUMLOCK	is	pressed,	CAPSLOCK	is	not	pressed,	and	CAPSLOCK	
is	not	on.	When	transitioning	to	MODE2,	the	CAPSLOCK	led	will	be	turned	on	automatically.	
MODE2	will	be	active	until	NUMLOCK	is	pressed	again.


However,	when	in	MODE2, CAPSLOCK	led	will	turn off	when	CAPSLOCK	is	pressed	the	first	time	
after	transitioning	to	MODE2	and	will	turn on	when	it	is	pressed	the	next	time,	and	so	on. In	
MODE2, your	driver	should	leave	the	CAPSLOCK	led	status	in	a	way	that	will	be	compatible	with	
MODE1,	e.g,	whether	the	input	layer	thinks	the	CAPSLOCK	is	on	or	not. As	a	result, in	MODE2,	
when	the	CAPSLOCK	led	is	off	(on)	you	will	see	that	the	characters	that	are	typed	on	the	
keyboard	will	be	displayed	in	upper	(lower)	case	mode.
