![[Pasted image 20240413205424.png]]
![[Pasted image 20240413205454.png]]
SPECIFICALLY THE TIME.SLEEP(2) FUNCTION
![[Pasted image 20240413210724.png]]
found in the moisture (class) found below
![[Pasted image 20240413210804.png]]        try:

            GPIO.add_event_detect(self._gpio_pin, GPIO.RISING, callback=self._event_handler, bouncetime=1)

        except RuntimeError as e:

            if self._gpio_pin == 8:

                raise RuntimeError("Poop dick")

            else:

                raise e
![[Pasted image 20240413220309.png]]
