# Useful JS MIDI Effects

A collection of JS MIDI Effects for Reaper.
These have been tested on Reaper v7.36 as of this writing.

## Installation

You can install these by doing a git clone in your reaper effects directory (e.g., `/Users/<username>/Library/Application Support/REAPER/Effects/midi/` on Mac, for example).  
After this, trigger a rescan of the effects by opening the effects selector window, right clicking on the left pane and choosing "Scan for new plugins"

If the `LICENSE` and `README.md` file bother you in the effects list just delete those files since they obviously do not work as effects.

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
