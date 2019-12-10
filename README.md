Shruthi-1 - MOD
=======================
## Preamble

This fork contains minor modifications to the original shruthi (1.03) Master Branch. The customizations are compatible with the original version, lies in the branch 'original'. All changes in the source are uniformly marked with beginning and ending comment.

## Modifications

1. [SEQ Handling - External BPM](https://github.com/rio-rattenrudel/shruthi-1/commit/aec0904e4ff012a145512ef84a24a13eba4a4901)

* Sequences operated by external BPM should behave like driven by internal BPM. That is, sequences are controlled by NOTE On/Off, but the external tempo is used. 
* Furthermore, the 12 ticks delay was removed, which otherwise can not be programmed exactly.

2. [Fixed: SEQ Rhythm Page Editor](https://github.com/rio-rattenrudel/shruthi-1/commit/3635574db7a03e429eca79e33e80ad97ac0cc1b7)

* Now the page will be displayed correctly (with shifted offset)
* It is now possible to move with P1, equivalent to the Step Sequencer

3. [Fixed: SEQ Tracker & Rhythm Editor II](https://github.com/rio-rattenrudel/shruthi-1/commit/1bef7258c06444ed6cccb32a8d90e109d683f4c8)

* Now the tracker is displayed correctly (with shifted offset)
* The Encoder increment is fixed for Rhythm Page Editor
* Refactoring

4. [Feature: Pattern Rotation Storage](https://github.com/rio-rattenrudel/shruthi-1/commit/a569b070aa8c4e85f0655adccbe4af36389b1298)

* Now the patch contains the "pattern rotation" that is shared with "groove template" storage (Upper Nibble).
* A pattern rotation reset is added for "non-running" patch changes
* _Note: affects data storage_

## Original Notes
```
Shruthi-1, a digital/analog hybrid MIDI monosynth.

This project is a redesign of the original Shruti-1, with a spec'ed up CPU,
and a focus on easy upgrades/modification of the analog section.
The ATMega644p allows new features in the firmware -- a larger selection of
oscillator algorithms, a bigger selection of wavetables, and a tiny sequencer.

Original developer: Emilie Gillet (emilie.o.gillet@gmail.com)

The firmware is released under a GPL3.0 license. It includes a
reimplementation of the formant synthesis algorithm used in Peter Knight's
Cantarino speech synthesizer.

The PCB layouts and schematics (in /hardware/shruthi/design/pcb)
are released under a Creative Commons cc-by-sa 3.0 license - except for some
discontinued filter boards which were released under a cc-by-nc-sa 3.0 license.

Documentation, analyses, simulations and 3D models are released under a
Creative Commons cc-by-sa 3.0 license.
```
