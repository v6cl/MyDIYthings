# Filament cutter for Annex k3 with tradrack

Servo motor DS3225MG 

X-acto no.11 Blade

(https://youtu.be/plr8zOUnL6M)

## config

You need to change to tradrack's wip-inline-filament-cutter branch. 

(https://github.com/Annex-Engineering/TradRack/blob/main/docs/klipper/Installation.md)

```
cd ~
./trad_rack_klippy_module/Klipper_Stuff/klippy_module/install.sh wip-inline-filament-cutter
```

in moonraker.conf

```
[update_manager trad_rack]
type: git_repo
path: ~/trad_rack_klippy_module
origin: https://github.com/Annex-Engineering/TradRack.git
primary_branch: wip-inline-filament-cutter
managed_services: klipper
```
in trad_rack.cfg

```
[trad_rack]
enable_cutter: True
# cutter_fil_sensor_pin: 
cutter_servo_cut_angle: 0
cutter_servo_reset_angle: 145 # init angle
cutter_servo_wait_ms: 1000
cutter_retract_length: 0
cutter_bowden_length: 580 # Distance of Bowden tube from head to cutter.
cutter_retract_speed: 300 # Please write down the value that suits you.
toolhead_sense_speed: 10 # Please write down the value that suits you.
```

> [!CAUTION]
>I recommend that the length of the filament remaining after cutting is 20 to 30 mm. (excluding melted and stretched length)
If it is too short, it will be light and will not fall, and if it is longer than the cutter, it will not be discharged.

![image](https://github.com/v6cl/MyDIYthings/assets/16078263/e37e5de8-b3ff-425e-88ad-d752ddb898a9)
