# Flipper Zero Wav Files
A collection of wav format songs for Flipper Zero.

You can do it by yourself.
I convert my mp3 files based on Uberguido's Guide:
```
ffmpeg -i .\input.mp3 -c:a pcm_u8 -fflags +bitexact -flags:a +bitexact -ac 2 -ar 48k output.wav
```

\
If you're on linux and want to convert all your songs in a folder, you can do this:
```
for i in *.mp3; do ffmpeg -i "$i" -c:a pcm_u8 -fflags +bitexact -flags:a +bitexact -ac 2 -ar 48k "${i%.}.wav"; done
```

\
I will not add anymore songs after this, so pull requests are welcome. Thanks you.
