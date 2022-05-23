# Astro Vibe

![Image of IceTray module](https://github.com/patheros/PathSetModules/blob/main/images/AstroVibe.png)

Astro Vibe is three planetary obiters that can operate as VCOs or LFOs. Each orbiter has a wide range of controllable settings as well as internal planetary signature that affects the waveform. There are over three septillion planetary signatures and once you leave one your unlikely to ever find it again. Does nothing when bypassed.

### Planet

Each orbiter generates a unique planetary signature when the module is created and when either the `New Planet Button or Trigger` is activated. The planetary signature affects the output waveform giving it a unique signature. For the Notes waveform mode each signature creates a unique sequence of between 2 and 22 different notes to play. In the crunchy waveform mode it affects the overall timbre of the sound. There are over three septillion signatures and no way to return to one once you leave. Signatures do persist when the patch is saved.

### Clock and Freq

Each orbiter has a `Clock` input which advances the notes in the Notes waveform mode. It does nothing in the Tones waveform mode. The clocks on the 2nd and 3rd orbiter are normalized to the previous orbiter, meaning you only have to connect a clock to the 1st orbiter to get all 3 going.

Each orbiter also has a `Frequency Knob` and `1V/Oct Input`. These two control the overall tone of the sound in the Audible mode and the overall speed of the LFO in the LFO mode. The 1V/Oct input is also normalized between the orbiters.

Note all internal routing can be disabled from the contextual menu.

### Engine and Waveform

The central switches control the `Engine` and `Waveform` of each Orbiter. Each switch is togglable to change the mode and also controllable with the corresponding input. If the input is high (above 5 volts) the toggle is inverted. If its low (bellow 0 volts) the toggle acts as normal. If the input is between 0 and 5 volts, the toggle flips back and forth and is proportionally one way or the other depending on what the input voltage is.

When the `Engine` mode is `Atomic` the sound more pure and smaller. When the mode is `Black Hole` the sound is buzzier and louder.

When the `Waveform` mode is on `Notes`the sound is melodic and plays a sequence with the clock. When on `Tones` the sound is always on and can be more crunchy. 

### Warping

The `Space Input`, `Spin Input` and `Warp Knob`all adjust the timbre of the sound as well as the panning between the left and right channels. The overall effect is more pronounced on the Tones waveform.

The Space and Spin Inputs are double normalized. If the previous orbiter is set to LFO mode, then the left and right channels are routed to the Space and Spin respectively. If not, then the previous orbiters space and spin inputs are carried forward. This internal routing can be disabled from the contextual menu.

### LFO vs Audio

Each orbiter has an `Speed` toggle that switches between an `Audible` mode and a `LFO` mode. In the Audible mode the output is also added to the master output at the top of the Module. In the LFO mode the output is normalized into the next orbiter's Space and Spin.

### Gain

Each orbiter has a `Gain` knob under its output. This gain is applied in both `Audible` and `LFO` mode. When the gain is turned to the left past the half way point the voltages are inverted.

## Examples
* [AstroVibe_Example1](../examples/AstroVibe/AstroVibe_Example1.vcv) - Shows all 4 possible combinations of Engine and Waveform when used in audio output. Also demonstrates the variety the planetary signature provides the oscillator. 
* [AstroVibe_Example2](../examples/AstroVibe/AstroVibe_Example2.vcv) - Polyphonic example also using one of the obiters as an LFO and the internal routing.
* [AstroVibe_Example3](../examples/AstroVibe/AstroVibe_Example3.vcv) - More complete atmospheric patch showing off two AstroVibes.

Note examples use [other plugins](#other-plugins).