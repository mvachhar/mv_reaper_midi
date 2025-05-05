# Useful JS MIDI Effects

A collection of JS MIDI Effects for Reaper.
These have been tested on Reaper v7.36 as of this writing.

## Installation

The easiest way to use these plugins is to use Reapack.

### Install Reapack

Please follow the installation instructions here to install ReaPack: https://reapack.com/user-guide#installation

### Configure this Repository in ReaPack

Add the following repository to your reapack: https://raw.githubusercontent.com/mvachhar/mv_reaper_midi/master/index.xml

Do this by going to the menu and choosing `Extensions > ReaPack > Import Repository`.

### Find and install the plugins you want

You can now navigate to `Extensions > ReaPack > Browse packages` and choose any effects that are included here.
A list of effects and plugins is below.

## Effects

### MIDI Experssion Pedal Curve + Toe Switch Emulation (`exp_modulator.jsfx`)

Plugin that modifes the MIDI CC message to change the rate at which a midi expression pedal changes a control.
You can control the input CC number that the plugin will use.
If you need to change the output CC, you can use the builtin MIDI plugins to remap the messages/channels/etc.
You can set input threshold where the expression pedal generates a non-zero CC message, and the point at which the output is saturated (i.e., maximum value)
The curve shape can be made more or less aggressive, with linear as the neutral setting.

There is also toe switch emulation so that expression pedals without a toe switch can act like they have one.
If toe switch emulation is enabled, pressing the pedal all the way to generate a CC value of 127 will trigger toggle the toe switch.
It is helpful to set the the saturation to 75-80% so that you can max out the output without accidentally triggering the toeswitch emulation.
You can set the output CC message for the toe switch emulation independently of the input CC number.
