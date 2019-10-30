# JS Notes Player

This is a js library that allows you to play notes by giving a letter with or without accidental (eg. Ab, A, A#), octave (-num, 0, num), and bpm or beat duration. Currently the playback uses the crude Web API. In the future, the sounds will be better.

## Playing a note

Use Examples:

BPM 60
```
    var player1 = new NotesPlayer();
    player1.play("A#", 0, 60);
```

BPM 120
```
    var player1 = new NotesPlayer();
    player1.play("A#", 0, 120);
```

1 second on this beat (ignore BPM)
```
    var player1 = new NotesPlayer();
    player1.play("A#", 0, null, 1);
```

Higher octave:
```
    var player1 = new NotesPlayer();
    player1.play("A#", 1, 60);
```

Lower octave:
```
    var player1 = new NotesPlayer();
    player1.play("A#", 1, 60);
```

The key of the engine is in C, so if you want to play B a half note down:
```
    var player1 = new NotesPlayer();
    player1.play("B", -1, 60);
```


### Playing notes simultaneously

C Major Triad Chord
```
    player1.play("C", 0, 60);
    player1.play("E", 0, 60);
    player1.play("G", 0, 60);
```

### Playing notes sequentially

The pause is in milliseconds, allowing you finer control on how the player pauses.

C Major 7 Arpeggio
```
    player1.play("C", 0, 60);
    player1.pause(1000);
    player1.play("E", 0, 60);
    player1.pause(1000);
    player1.play("G", 0, 60);
    player1.pause(1000);
    player1.play("B", 0, 60);
```

## Engine

```
    <script src="js/js-notesplayer.js"></script>
```

## Demo

https://www.wengindustry.com/tools/js-notesplayer

## License

This project is licensed under the MIT License.
