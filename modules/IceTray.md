# Ice Tray

![Image of IceTray module](../images/IceTray.png)

Ice Tray is a speed shifter and six tape delays, called ice cubes. Each cube can solidify, capturing what ever was last recorded into it for an indefinite amount of time. Left and Right inputs are connected directly to the outputs when bypassed.

### Video

[![Omri Cohen video on Ice Tray](http://img.youtube.com/vi/JJGFmtAUXNA/0.jpg)](http://www.youtube.com/watch?v=JJGFmtAUXNA "Video Manual")

### Ice Cubes

The central section of the module displays the six `Ice Cubes`. The color of the large light indicates the`Solidity` of the ice cube:

* **Bright Blue** - Can be recorded to or played from
* **Dark Blue** - Can only be played from
* **Black** - Can't be accessed, but still remembers its last recording.

You can press the light to change its solidity. The large `Frozen Percent` knob also controls how likely a cube's solidity is to change over time. Crank it all the way up to 100% and the solidity won't change, unless you manually do so. 

The small light on the cube indicates which ice cube is being recorded (red) to and which is being played back (green). An ice cube can't be both at the same time.

Recordings on the cubes will persist when the patch is saved. The recordings can also be cleared through the `Clear Cubes` option in the contextual menu.

### Clocks

Ice Tray doesn't need any clocks to work but you can connect either or both of its clocks to signals to get more control over the rhythm of the output.

When the `Record Clock` is NOT connected, the`Record Length` knob sets the maximum number of seconds each cube is recorded too before switching to a new cube. When `Record Clock` IS connected, the recording cube will switch when the clock is received, or after 10 seconds. Note all times assume 44.1kHz.

Normally the playback cube will finish its recording before switching to a new cube, but you can end this early by sending a trigger to the `Playback Clock`.

The `Playback Clock Resets Position` toggle controls where the playback starts on each cube. When on the playback starts at the start of each cube, but when off the position is not reset, so wherever the last cube ended the next cube starts.

### Speed Shift

The two large dials on the left control the speed at which the input signal is recorded. The pitch of the audio is corrected to maintain the original pitch regardless of playback speed. This can be CPU intensive and can be disabled from the contextual menu.

The `Numerator`  is divided by the `Denominator` to compute the final speed. Both the numerator and denominator can be modulated using the CV inputs and CV scalars. The modulated value is added to that on the large dial. The numerator and denominator are each rounded to the nearest whole number before computing the final speed.

### Patterns and Repeats

The `Repeat` knob controls how many times a single ice cube is repeated before another one is selected. If a CV is connected bellow the know then the knob scales that voltage.

The `Pattern` knob controls the order in which the ice cubes are are played back in. If the knob is turned to the left, the cubes are randomly skipped in increasing large steps leading to a random pattern each time. If the knob is turned to the order of the cubes is shuffled but consistent each time though with the caveat that cubes that are black, or being recorded to are skipped. 

### Feedback

The `Feedback` knob and corresponding CVs at the bottom of Ice Tray feed the output back into the recording cube. Unlike the input signal, the feedback signal is both speed up and pitch shifted by the speed controls. This gives the internal feedback a unique effect that an external source of feedback couldn't replicate.

## Examples
* [IceTray_Example1](../examples/IceTray/IceTray_Example1.vcv) - Mini Tutorial of IceTray with a simple voice and lots of notes.
* [IceTray_Example2](../examples/IceTray/IceTray_Example2.vcv) - Example of a single voice through IceTray with modulation.
* [IceTray_Example3](../examples/IceTray/IceTray_Example3.vcv) - IceTray with another delay and reverb to create more variety in the sound.