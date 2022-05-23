# Blender
![Image of Blender module](../images/Blender.png)

Blender is a “Distortion Looper”. It was created to allow you to capture all of the bizarre transient effects into a rhythmic loop. Blender simply needs divided clock and your good to roll. Sample its internal sounds sources or feed other sounds into it.

## Quick Start

![Image of quick start patch](../images/Blender/quick_start_1.png)

[Download Quick Start](../examples/Blender/Blender_QuickStart.vcvs?raw=true)

Turn the `Input Vol` knob up and down to make a beat. Then play around with the four big knobs to distort that beat as Blender continuously records itself on a loop.

## Panel

![Image of controls](../images/Blender/labels.png)

1. **L/R Audio Input** - Input audio source. Contextual menu controls which internal noise source is used when no input is connected.
2. **Input Source** - Select between two internal sound sources and the Audio Input ports.
3. **Input Volume** - Controls how loud the input audio is in the mix. This knob is ignored for the first sample after the module is reset. 
4. **Input Mute** - When red, the input audio is muted. The mute is ignored for the first sample after the module is reset.
5. **L/R Audio Output** - Output audio source. 
6. **Mix Volume** - Spring Loaded! Controls how loud the output audio is mixed back into the next sample. This knob reset to 1 after each sample is recorded because the reduced audio is baked into the sample at that point.
7. **Reset Button** - Clears the internal sample and triggers a one second recording if a cable is patched to `Audio Input`
8. **Reset Trigger** - Triggers reset button when the signal is high.
9. **Clock Input** - Syncs the internal loop length to the clock length. Max loop length is 10 seconds at 48kHZ.
10. **Recording** - Toggle if Blender is recording to its internal buffer.
11. **Ring Knob** - Spring Loaded! Applies a resonating delay to the sample. Turning the knob clockwise has a linear effect. Turning the knob counter-clockwise has an exponential effect.
12. **Ring CV** - Modulates Ring Knob.
13. **Ring Attenuverter** - Modifies CV for Ring Knob.
14. **Pitch Knob** - Spring Loaded! Shifts the pitch of the sample up or down.
15. **Pitch CV** - Modulates Pitch Knob.
16. **Pitch Attenuverter** - Modifies CV for Pitch Knob.
17. **Scratch Knob** - Spring Loaded! Applies a turntable style effect to the sample.
18. **Scratch CV** - Modulates Scratch Knob.
19. **Scratch Attenuverter** - Modifies CV for Scratch Knob.
20. **Filter Knob** - Spring Loaded! Filters the sample. Turning the knob clockwise applies a high pass filter. Turning the knob counter-clockwise applies a low pass filter.
21. **Filter CV** - Modulates Filter Knob.
22. **Filter Attenuverter** - Modifies CV for Filter Knob.

**Expander**

*Added through contextual menu*

23. **Playback Trigger Input** - When this input goes high Blender will reset it's playback.
24. **Playback Mode** - When set to One-shot Blender will only play once for each Playback Trigger received. Additional blender will no longer re-trigger when Playback Trigger is received.
25. **Playback Start Position** - Controls where in the recorded loop Blender restarts it's playback at.
26. **Playback Start Position CV** - Modulates the Playback Start Position Knob.
27. **Playback Start Position Attenuverter** - Modifies the CV for Playback Start Position Knob.

### Spring Loaded Distortion Knobs

The four main distortion knobs are spring loaded. Meaning they return to their default position after you release them. This allows you to turn them for an effect and then release them when you want that effect to fade back.

The Mix Volume is also spring loaded too.

### Expander

The Blender expander allows for an alternative way to use Blender. Before adding the expander play around with Blender in record mode to get an interesting sample loaded the up. Then turn off record mode and add the expander. Connect the Trigger/Reset input to your clock and listen to Blender play a repeated hit. Try changing the Position parameter to get different segments of the internal sample to play. Switch the Mode to one-shot to make it play less often.

### Bypass

When Blender is bypassed the `Audio Input` is routed to the `Audio Output`.