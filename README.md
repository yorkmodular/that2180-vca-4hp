## York Modular THAT2180 VCA

I've done more than my fair share of lo-fi VCAs in the past, so here's one with a bit more in the way of 'fi'.

Unlike some others, this module is built around the THAT2180 Blackmer cell IC - I find it easier to use, and less prone to self-destruction, than the V2164.

This is a 100% through-hole build - there are a couple of different versions of the THAT2180 (A and B) but unless you're looking for insanely low levels of THD the C variant gives the best bang for the buck.

There's a single signal input and a control voltage input with associated attenuator. Prototype versions of this module had one attenuated and one unattenuated CV channel, but to keep costs down I went for a single attenuated CV channel - if this bothers you, you can always route your CVs through a mixer beforehand. Anyway, irrespective of this, it's possible to get some _very_ cool sounding distortion out of it with the levels turned up.

The included parts pretty much reflect a datasheet build, but if you know what you're doing then there's scope for a bit of tweaking here and there (in particular, the CV input stage)

### Construction notes

- The THAT2180 is an SIL (single inline) IC - these are pretty uncommon but really no different from the DIL ICs you may be used to. The footprint on the PCB will have a dot at one end corresponding to pin 1; the notch in the IC should be at this end.
- If you've bought the partial kit then you'll need to source a THAT2180 or equivalent. There are three different variants of the IC available, offering varying degrees of THD. For most practical purposes, the C variant is fine, and relatively inexpensive - if you feel the need to use the A or B variant then go ahead; they're all interchangeable but the A and B variants are pretty expensive.
- The op-amp in the circuit is acting as both an amplifier and a buffer. I supply a TL072/082 by default and these will do the job admirably. If you want to use a 'proper' audio op-amp then make sure it is pin-compatible with the TL0x2 series. Most dual audio op-amps (eg. NE5532) are, but double-check first.
- **IMPORTANT**: Fit the trimmer pot _before_ you solder the level pots and jacks in place. Trust me on this ;-)

### Basic setup

Unless you strike it _extremely_ lucky then chances are you're going to have to do a bit of tweaking once you've completed the build. In a nutshell, you'll probably want no output from the VCA when the control voltage is 0V.

Fortunately, there's a simple way to achieve this:

- Plug an audio source (VCO, whatever) into the signal input. I suggest a constant frequency square or sawtooth wave, since these are easily audible even at low volumes.
- Turn the CV attenuator fully counter-clockwise.
- Plug the output into either an oscilloscope (preferred) or a suitable speaker.
- **If you're using an oscilloscope**, adjust the trimmer pot on the module until the output is 0V (or whatever value you prefer). 
- If you're working by ear:
-- **If there's an audible output with zero CV**, adjust the trimmer until you can no longer hear anything.
-- **If there isn't an audible output**, adjust the trimmer until you can hear something and _then_ readjust until the signal is no longer audible.

There are undoubtedly fancier ways of achieving the same result, but this Works For Me. 

Be aware that you _will_ get signal distortion if you use particularly hot CVs - the attenuator pot supplied has a linear taper, but there's nothing to stop you substituting an audio taper (or any other taper you like)
