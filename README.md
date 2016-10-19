# clmk

*caps lock midi keys*

Max abstraction facilitating MIDI input with a QWERTY keyboard, mimicking the old Logic Caps-Lock mode, or the similar one in Ableton Live.

## mappings

* Caps Lock to enable
* Keys fall on the top two rows of QWERTY.
* Z/X = ± 8ve
* C/V = ± dynamics
* 1/2 = ± pitch bend
* 3–8 = mod wheel stepper
* shift, tab = sustain

## outlets

1. pitch/velocity pairs for use with **noteout**
2. full messages for use with **midiout**
3. **midievent** (i.e. for use with vst~) etc.

## inlets/args

MIDI channel and ramp times (ms) for mod-wheel and pitch-bend can be set using the bpatcher interface, or alternatively can be quickly set when instantiating an abstraction:

args**: <*midi channel*> <*mod-wheel ramp time*> <*pitch bend ramp (ms)*>

args are optional and default to 1, 80, 45.

The same params can be set via inlets (in the same order).

## bpatcher

The default **clmk** bpatcher is optimized for the default 15px grid on a retina screen. **clmk.6** is optimized for Max 6, and **clmk.big** for non retina systems (and, by inclusion, Max 5).
