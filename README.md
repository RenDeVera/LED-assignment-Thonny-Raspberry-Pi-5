# LED-assignment-Thonny-Raspberry-Pi-5
LED assignment-Thonny
from gpiozero import LED
from time import sleep

red_led = LED (5)
yellow_led = LED (13)
green_led = LED (19)


def stop_light(traffic_status):
    print(traffic_status)

   
    print(traffic_status[f"Red: {red}, Yellow {yellow}, green {green}"])
   
    if red == 1:
        red_led.on()
    else:
        red_led.off()
       
    if yellow == 1:
        yellow_led.on()
    else:
        yellow_led.off()
       
    if green == 1:
        green_led.on()
    else:
        green_led.off()

def main():
    print("Welcome To The STEAM Clown Makey Bot")
#    while(True):
#      print("LED on")
#      red_led.on()
#      yellow_led.on()
#      green_led.on()
#      time.sleep(1)
#      print("LED off")
#      red_led.off()
#      yellow_led.off()
#      green_led.off()
#      time.sleep(1)
    traffic_light = {'red_LED' : 1, 'yellow_LED' : 0, 'green_LED' : 0}
    stop_light(traffic_light)
    sleep(1)
   
    traffic_light = {'red_LED' : 0, 'yellow_LED' : 1, 'green_LED' : 0}
    stop_light(traffic_light)
    sleep(1)
   
    traffic_light = {'red_LED' : 0, 'yellow_LED' : 0, 'green_LED' : 1}
    stop_light(traffic_light)
    sleep(1)

if '_name_' == "_main_":
    main()
