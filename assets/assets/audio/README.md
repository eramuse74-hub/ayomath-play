# Audio assets

## Background music & sound effects — synthesized at runtime

Since v1.1.8 the app **synthesizes its own music and SFX at runtime** — no
audio files to ship or license:

- `lib/music_synth.dart` — original chiptune loops (calm + Mode Cepat),
- `lib/sfx_synth.dart` — correct-answer chime, gentle wrong-answer tone,
  level-up fanfare, star pop.

Both are played by `AudioController` (`lib/audio.dart`) via `BytesSource`, so
this folder stays empty and everything works offline out of the box.

### Optional: your own music override

If you ever prefer a recorded track, drop a looping `bg_music.mp3` here and
switch `AudioController._startMusic` to an `AssetSource`. Keep it original /
royalty-free (CC0 / public domain / CC-BY with credit) and run
`flutter pub get` to refresh the asset bundle.
