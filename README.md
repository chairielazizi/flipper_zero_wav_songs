# Flipper Zero Wav Files
A collection of wav format songs for Flipper Zero.
Please put the wav files in the root of your SD card in th wav_player folder.

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
I think I will not add any more songs after this, so pull requests are welcome. Thank you.

\
Tips: If your wav files is not detected or does not appear in the wav_player fap, remove any single quote or double quote ( ' and ")
