Speakers are a block which allow computers to play music in world. They can be wrapped as peripherals (with name `speaker`) and used as upgrades for pocket computers and turtles.

The speaker has a limit to the number of notes and sounds which can be played in a single tick. At most one sound (played using `playSound`) can be played each tick. However, one can play up to 8 notes (using `playNote`) each tick, allowing you to create complex note-block melodies using the speaker.

## Configuration
 - `maxNotesPerTick = 8`: The maximum number of notes which can be played in a single tick.

## Methods
### `speaker.playNote(instrument: string[, volume:number[, pitch:number]]): boolean`
Play a note with the given volume and pitch. 

The instrument name corresponds to those provided by [Note Blocks](https://minecraft.gamepedia.com/Note_Block#Instruments). It may be one of the following strings: `bass`, `basedrum`, `bell`, `chime`, `flute`, `guitar`, `hat`, `snare` or`xylophone`.

Volume may be any number between 0 and 3 inclusive. 1 is the default, with 3 being the volume of a normal note block. Like note blocks, a higher volume does not imply a louder sound, merely that it can be heard further away.

The pitch may be a number between 0 and 24 inclusive, defaulting to 1. This represents the number of times one has [right-clicked a noteblock](https://minecraft.gamepedia.com/Note_Block#Notes). 0 representing F♯ and 24 representing F♯ 2 octaves higher.

This will return `true` if the note could be played or `false` if too many notes have been played in a single tick.

### `speaker.playSound(name: string[, volume:number[, pitch:number]]): boolean`
Play a sound with the given volume and pitch.

The sound name corresponds to a resource name in [Minecraft's `sound.json` file](https://minecraft.gamepedia.com/Sounds.json#Java_Edition_values). For instance `minecraft:entity.player.levelup` is the sound one hears when leveling up.

Like `.playNote`, the volume may be any value between 0 and 3 defaulting to 1.

The pitch argument is slightly different. Instead this may be any value between 0 and 2, with a larger value representing a higher pitch. One may convert from `.playNote` to `.playSound` pitches with the following equation: `2 ^ ((pitch - 12) / 12)`.

This will return `true` if the sound could be played or `false` if too many sounds were played in a single tick.