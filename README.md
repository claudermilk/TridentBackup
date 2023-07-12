# Blue Trident

This is a backup of my self-sourced Trident 250 config files.

I have cribbed a number of ideas from others to learn the possibiliteis of the Klipper & Jinja2 config language. I primarily took ideas from [Alex Zellner](https://github.com/zellneralex/klipper_config)'s config, and [Andrew Ellis](https://github.com/AndrewEllis93/v2.247_backup_klipper_config). A few bits and pieces of inspiration also came from various other shared configs and the [Voron Design documentation](https://docs.vorondesign.com/).

Note that many of the details are specific to my machine and if you choose to copy macros be sure to read through them and understand what they are doing--and what needs to be changed to suit your own printer and environment.

My current mods on the printer are:
- Waveshare 4.3" touchscreen with KlipperScreen
- randell XY endstop PCB
- chamber thermistor
- purge bucket and nozzle brush
- WS2812B LED strip case lights
- Logan BC PTFE tube guide
- RefillPlease filament sensor
- PanzerObserver webcam mount with OV5648
- Tap
- hernsl magnetic bottom plate clips
- Nevermore Micro
- ramalama2 pin front idlers
- Rainbow Barf Stealthburner logo LED
- hartk 2-piece Stealthburner toolhead PCB
- LDO breakout PCB
- MirageC79 WobbleX
- Modified Stealthburner main body to accomodate a UM2 lock for the PTFE tube

Obsolete Mods
- _hartk SexBolt Z endstop_
- _hartk Z endstop PCB_
- _Klicky Probe_

I have taken advantage of the include functionality and broken up my config into more task-focused files.
- /input_shaper. Output from input shaper runs.
- /KAMP. The excellent Klipper Adaptive Mesh and Purge library. Used without modification.
- /script. My shell scripts used in other macros.
- bed_mesh.cfg. Basic bed mesh definition.
- belt_tension.cfg. Belt tensioning testing.
- fans.cfg. Define the fans on the printer and all macros specific to running them.
- input_shaper.cfg. Setting up input shaper and the test macro.
- KlipperScreen.conf. My modified KlipperScreen menu defintion.
- leds.cfg. Defining the printer LEDs and all effects & macros to run them.
- macros_backup.cfg. My macros to push the config here to GitHub.
- macros_debug.cfg. A couple of informational macros swiped from Alex Zellner's repository.
- macros_filament.cfg. All macros related to filaments. Ideas taken from Alex Zellner and heavily modified for my use. Maintains a "database" of filaments and sets a variable to the printer "knows" what is loaded.
- macros_nozzle_scrub.cfg. Routines for using the purge bucket & nozzle brush mod.
- macros_plate.cfg. Same ideas as macros_filament. I am only using it to automate adding extra squish for textured plates.
- macros_probe.cfg. Used to quickly switch between Tap and Klicky.
- macros.cfg. This contains the primary macros for printing: print_start, print_end and and directly supporting macros.
- mainsail.cfg. As with moonraker, the default with a few adjustments.
- moonraker-obico-update.cfg. Auto update definition for moonraker.
- moonraker-obico.cfg. Definition for Obico.
- moonraker.conf. Pretty much the default file with adjustments for my environment.
- printer.cfg. This retains the physical printer component definitions.
- runout.cfg. Macros for using the RefillPlease mod.
- test_probe_accuracy.cfg. Copied set of macros for testing Tap. Mainly used aftr intiial installation of Tap.
- test_speed.cfg. Macros from Andrew Ellis for testing the maximum speed the printer can achieve.
- timelapse.cfg. A set of macros for generating timelapses. See macro for source.
- variable_setup.cfg. Create a centralized definition for a variable dictionary of preinter settings. Excellent concept taken from Alex Zellner and modified to my needs.
- webcam.txt. Standard file, no mods made.
- macros_refresh_obico.cfg. Update the Obico libraries. Not in use currently.
- macros_webcam.cfg. Used to stop/start the webcam. Not really needed any more, but left in just in case.
