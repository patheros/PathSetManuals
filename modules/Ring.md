
# Ring
![Image of Ring module](../images/Ring.png)

Ring consists for four concentric rings of Notes. Play sequences across the rings. Rotate the rings to make those sequences shift over time.

Like every sequencer in the Rainbows set, Ring is designed to sequence notes. Each step in the sequence can be set to a specific note by clicking the corresponding note. Ring also can also have three more sequencers running on the same module by adding the expander through the contextual menu.

## Panel

![Image of controls](../images/Ring/labels.png)

1. **Clock input** - Advances the sequencer to the next state depending on which ports are connected.
2. **Reset input** - Resets the sequencer to the first state and resets all nodes to their last manually selected mode.
3. **Gate output** - Gate signal to attach to a voice or envelope generator.
4. **CV output** - The CV value here matches the knob of the current state. 
5. **End of Cycle Gate output** - Gate signal that is high on the first step of the sequence after each time the cycle ends.
6. **Ratchet Gate output** - Gate signal that is high whenever the sequencer is ratcheting.
7. **Mute Gate output** - Gate signal that is high whenever the sequencer is muted.
8. **Notes** - The Notes on Ring are divided into four 7 step sequences. Right click for more options.

**Sequences**

The left wing of the panel has controls per sequence. The sequences are labeled Horizontal, Descending Diagonal, Vertical, Ascending Diagonal. Each of these sequences has the following controls:

9. **Length Knob** - Sets the length of the sequence. When above 8, the sequence will ping-pong, repeating each end node.
10. **Length CV** - Modulates Sequence Length Knob.
11. **Length Attenuverter** - Modifiers the CV for the Sequence Length Knob.
12. **Mute Knob** - Makes notes silent. The higher the knob the more often this happens. When the note is silent, the normal `Gate` is low and the `CV output` holds its previous value.
13. **Mute CV** - Modulates Mute Chance Knob.
14. **Mute Attenuverter** - Modifiers the CV for the Mute Chance Knob.
15. **Ratchet Knob** - Makes notes play quickly. The higher the knob the more often this happens. The number of notes played can be configured from Ratchet Speed option the contextual menu.
16. **Ratchet CV** - Modulates Ratchet Chance Knob.
17. **Ratchet Attenuverter** - Modifiers the CV for the Ratchet Knob.

**Jump Points**

The central panel has eight arrows, connecting the ends of all the sequences. Each of those arrows has the following controls:

18. **Jump Knob** - Allows the the play-head to jump from one sequence to the next in a clockwise direction. The play-head can only jump when the sequence has reached its run through the sequence. The value on the knob determines how far it will jump. For example, when set to 1.3 the sequence will have a 30% chance to jump 2 steps, and 70% chance to jump 1.
19. **Jump CV** - Modulates Jump Chance Knob.
20. **Jump Attenuverter** - Modifiers the CV for the Jump Knob.

An astute observer will notice there are 8 jump points but only 4 sequences. Half of the jump points connect to the back-end of a sequence. When a play-head reaches the back-end of a sequence, it plays that sequence in reverse. 

It's also worth noting the jump from the back-end of a sequence will not trigger when the sequence is playing forward, and vis-a-versa. This means at any given time there is only ever one knob that can jump the play-head to a new sequence. This means if any of the jump knobs are at 0, the play-head can get suck on that sequence.

**Rings**

The right wing of the panel has controls per ring. The rings are numbered 1 to 4. With 1 being the inner most ring.

21. **Ring # Cycle Knob** - Causes the notes in a ring to rotate periodically. At a value of 1 or -1, the ring will rotate each time the play-head completes one run through its current sequence. A positive value makes the ring rotate clockwise, and a negative value makes it rotate counter-clockwise.
22. **Ring # Cycle CV** - Modulates Ring # Cycle Chance Knob.
23. **Ring # Cycle Attenuverter** - Modifiers the CV for the Ring # Cycle Knob.
24. **Ring # Cycle Left Trigger** - A rising value on this input will cause the ring to rotate one step to the left, regardless of what value the Cycle Knob is set to.
25. **Ring # Cycle Right Trigger** - A rising value on this input will cause the ring to rotate one step to the right, regardless of what value the Cycle Knob is set to.
26. **Ring # Cycle Gate output** - This gate will be high whenever the ring rotates, regardless of direction or source of the rotation.

## Features

### Notes

Like every sequencer in the Rainbows set, the notes on Ring can be set clicking the light. Left clicking will allow you to select from the currently selected scale. Right clicking will allow for more options. From the right click menu you can:

- **Randomize Notes** - Randomizes ALL notes on the module. Only selects from the current scale.
- **Set Scale & Randomize** - Change the scale and randomizes all notes on the module.
- **Set Scale** - Change the scales. Will NOT change any notes currently on the module.
- **Set Any Note** - Lets you set the note, even if its not in the current scale.

Rainbow set is limited to a 3 octave range, from A3 up to G#5

### Ring Effects

The space between the sequences on Ring have several different effects that can be configured. These settings affect the two adjacent notes. Each row of Ring effects has a chance to apply that can be controlled by the `Odds knobs` on the right of the panel.

The different Ring effects are:

![Image of different effects](../images/Ring/modes.png)

1. **None** - No Effect
2. **Skip** - The note is skipped. The Note still counts against the sequence length, effectively shortening the sequence. Also the sequence can not skip more than 8 notes in a row.
3. **Mute** - The note is silent. The normal `Gate` is low, the `CV output` holds its previous value, and the `Mute Gate` is high.
4. **Ratchet** - Causes several notes to be played in quick succession. The module selects notes from the same column. The number of notes played can be configured from Ratchet Speed option the contextual menu.
5. **Borrow** - Plays the note from the other sequence instead.
6. **Swap** - Swaps the notes from the two adjacent sequences.
7. **Jump** - Moves the play-head over to the other sequence.

### Expander - Four Play-Heads

Like every sequencer in the Rainbows set, Ring has an expander. You can add the expander in the contextual menu. The expander creates four independent play-heads. When the expander is attached you will see the selected note ring is now broken up into for quadrants, one for each of the four play-heads.

The `Clock` and `Reset` inputs on the main module drive all four-heads, but you can also use independently clock and reset inputs on the expander to drive each play-head at a different rates.

On Ring, the four-play heads automatically start on the four different sequences.

### Contextual Menu

- **Randomize Notes** - Randomizes ALL notes on the module. Only selects from the current scale.
- **Set Scale & Randomize** - Change the scale and randomizes all notes on the module.
- **Set Scale** - Change the scales. Will NOT change any notes currently on the module.
- **Ratchet Speed** - Controls how fast the Ratchet mode plays. When set to `Whole Notes` the Ratchet speed is equal to the clock. `Half Notes` plays twice per clock etc.
- **Add Expander** - Adds a 9HP expander to the right of the module. 

### Bypass

When Ring is bypassed the `Gate output` is connected to the `Clock input`.