microbit-Countdown.md    

# microbit-Countdown_block  

## カウントダウン  


## Countdown  



## Source code
```
"""
    Title  : Countdown
    Version: 01
    Author : Hiroyuki.Moriya
    Use    : https://makecode.microbit.org/#editor
"""
for index in range(3):
    music.play_tone(262, music.beat(BeatFraction.QUARTER))
    basic.show_number(3 - index)
music.play_tone(392, music.beat(BeatFraction.WHOLE))
basic.show_string("Go!")
```
