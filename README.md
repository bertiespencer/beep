# Beep
A little package that brings sound to any Go application. Suitable for playback and audio-processing.
Forked from [faiface/beep](https://github.com/faiface/beep) for some tiny additions.

## Features

Beep is built on top of its [Streamer](https://godoc.org/github.com/faiface/beep#Streamer) interface, which is like [io.Reader](https://golang.org/pkg/io/#Reader), but for audio. It was one of the best design decisions I've ever made and it enabled all the rest of the features to naturally come together with not much code.

- **Decode and play WAV, MP3, OGG, and FLAC.**
- **Encode and save WAV.**
- **Very simple API.** Limiting the support to stereo (two channel) audio made it possible to simplify the architecture and the API.
- **Rich library of compositors and effects.** Loop, pause/resume, change volume, mix, sequence, change playback speed, and more.
- **Easily create new effects.** With the `Streamer` interface, creating new effects is very easy.
- **Generate completely own artificial sounds.** Again, the `Streamer` interface enables easy sound generation.
- **Very small codebase.** The core is just ~1K LOC.

## Dependencies

For playback, Beep uses [Oto](https://github.com/hajimehoshi/oto) under the hood. Check its requirements to see what you need to install for building your application.

Running an already built application should work with no extra dependencies.

## Licence

[MIT](https://github.com/faiface/beep/blob/master/LICENSE)
