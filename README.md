# PWM2TMR-creating-timers-from-PWM-modules
Creating timers from PWM modules

Turning unused PWM modules into timers. Demo's on LM3S811 but the code should run on TM4C with minor modifications.

The following creates a smooth blinking LED:

	//use two PWM-based timers to create dimming up / down effect on led
	pwm1tmr_init(PWM_PS2x, 1001); pwm1tmr_act(led_flp);
	pwm2tmr_init(PWM_PS2x, 1000); pwm2tmr_act(led_flp);
