# Glass Smith
![Image of GlassSmith module](../images/GlassSmith.png)

Glass Smith is a premium companion to the free sequencer [Glass Shard](https://library.vcvrack.com/PathSet-GlassShard/GlassShard). Glass Smith gives you the ability to craft one new configuration of Glass Shard every day. You will want to read the [Glass Shard manual](https://github.com/patheros/PathSetManuals/blob/main/modules/GlassShard.md) to better understand Glass Smith.

## Usage

![Image of controls](../images/GlassSmith/labels.png)

Glass Smith lets you create a new Glass Share configuration with some limited control. You can force your new configuration to contain two specific modifiers. Or you can force your module to NOT have two specific modifiers modifiers. Or you can do one of each.

1. **Request Type** - Toggles if that modifier is forced to be included or excluded in the configuration you are about to create. 
2. **Request Modifier** - Controls which modifier is included or excluded.
3. **Craft Button** - Press and hold to craft a new configuration of Glass Shard.

Once you have the request type and modifiers picked, press and hold the craft button to use one of your daily charges to craft a configuration unique to you. An instance of Glass Shard will be created with the new configuration. The configuration will also be added to your Config Collection. Note that if you share a patch with other people, they will also get a copy of this configuration added to their Config Collection.

## Daily Limits

Glass Smith has a global number of charges. These are shown as teal gems on the craft button. Glass Smith will gain one charge every day and can hold up to nine charges. Each charge can be used to craft one new configuration of Glass Shard.

## Modifiers

Here is a full list of all the modifiers for Glass Shard.

| Image    | Name     | Effect   |
| -------- | -------- | -------- |
| ![Branching Random](../images/GlassShard/modifiers/Effect_branch_random.svg) | Branching Random | After this node finishes playing the next branch is selected at random from left, output, or right. |
| ![Branching Weighted](../images/GlassShard/modifiers/Effect_branch_weight.svg) | Branching Weighted | The branches are weighted with the left branch being three times as likely as the right and the output branch being twice as likely as the right. |
| ![Branching Memory](../images/GlassShard/modifiers/Effect_branch_sticky.svg) | Branching Memory | Remembers the last branching direction that was taken: left, output, or right. Has a high chance of repeating that last branch direction. |
| ![Double Play](../images/GlassShard/modifiers/Effect_repeat_node_forward.svg) | Double Play | This node will play twice before continuing to the next node. |
| ![Ping Pong](../images/GlassShard/modifiers/Effect_repeat_node_backward.svg) | Ping Pong | This node will place twice before continuing to the next node. On the second play. The sliders will play in reverse. |
| ![All da Gates](../images/GlassShard/modifiers/Effect_runs.svg) | All da Gates | Every beat on this node will play a gate, repeating the CV values if needed. |
| ![Maybe Mute](../images/GlassShard/modifiers/Effect_mute_chance.svg) | Maybe Mute | Each slider has a 30% chance of being skipped. This chance is rerolled each time the slider is played. The chance of skipping multiple sliders in a row is decreased. |
| ![Drop Sliders](../images/GlassShard/modifiers/Effect_mute_deal.svg) | Drop Sliders | Each slider has a 30% chance of being skipped. This chance is set each time Glass Shard is reset, creating more consistent patterns. |
| ![Round Robin](../images/GlassShard/modifiers/Effect_cycle_knobs.svg) | Round Robin | Each time this node is triggered it only lasts for one beat. The CV played cycles through each of the steps, each time this node is played. |
| ![Three's Company](../images/GlassShard/modifiers/Effect_three_knobs.svg) | Three's Company | This node only has three beats, instead of four. |
| ![Echo](../images/GlassShard/modifiers/Effect_echo.svg) | Echo | A copy of this node is played on the second polyphony channel, delayed by one node. |
| ![Waterfall](../images/GlassShard/modifiers/Effect_waterfall.svg) | Waterfall | When this node is played all four nodes on this row are played as chord. |
| ![Duet](../images/GlassShard/modifiers/Effect_split.svg) | Duet | Every other node is played on the second polyphony channel. |
| ![Mix it Up](../images/GlassShard/modifiers/Effect_change_each_play.svg) | Mix it Up | Every time a slider is played it's CV value is randomized. |
| ![Perfect Double](../images/GlassShard/modifiers/Effect_perfect_double.svg) | Perfect Double | Always have 2nd Poly Channel. When this modifier is active that channel plays off set by a perfect 5th or ocative, up or down. |
| ![Imprfect Double](../images/GlassShard/modifiers/Effect_imperfect_dobule.svg) | Imperfect Double | Always have a copy of the note played on the second polyphony channel. When this modifier is active that channel can play offset up or down by up to two semitones. Turn on the quantizer to help tame this extra bit of spice.|