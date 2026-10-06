# Ambient Sounds

Recordings for the [ambient player](https://github.com/splenguin/ambientPlayer).
The Pi keeps a copy at `~/ambientSounds`. Pressing **Update from GitHub** on the
control page pulls this repo too, then restarts the sound.

## Folders

| Folder  | What goes in it | Where it plays |
|---------|-----------------|----------------|
| `owls/` | Owl calls: hoots, trills, whinnies | Only the elevated (tree) speakers, when Birds is on |

### Naming owls

The letters at the start of a file name say which owl it is: `owlA_01.wav`,
`owlA_02.wav`... are owl `owlA`, and `owlB_01.wav`... are owl `owlB`. Keep each
owl to one bird or species, so it sounds like the same animal every time it
calls. On the Pi, `AMBIENT_SPEAKERS` can give each elevated speaker its own
owl (see the ambientPlayer README); a speaker set to `birds` plays any of them.

The player picks a random file each time and varies its speed, tone and
distance slightly, so 5 to 20 different takes are plenty. More variety beats
longer files.

## Preparing a recording

- **Format:** FLAC or WAV, 48 kHz. Mono is best; for stereo files only the
  left channel is used.
- **Length:** trim each file to a single call or a short phrase, 1 to 10
  seconds, with a little silence at the ends. Files longer than about 12
  seconds still work, but the player only plays a random excerpt of them.
- **Level:** normalize each file so its loudest peak is around -3 dB. The
  player sets the actual loudness.
- **Clean:** cut out other loud birds, voices, traffic and handling noise.
  Faint background is fine.

Audacity does all of this: trim, then Effect > Normalize, then File > Export
as FLAC.

## Licensing

This repo is public, so only add recordings you're allowed to redistribute:
your own, public domain, CC0, or CC BY (with credit). Add a line to
`CREDITS.md` for every file that isn't your own.

Good sources:
- [freesound.org](https://freesound.org): filter by license and pick
  "Creative Commons 0".
- US government recordings are public domain, for example from the National
  Park Service and US Fish & Wildlife Service.

Avoid xeno-canto and the Macaulay Library for this repo. Most of their
recordings are non-commercial or all-rights-reserved.
