microbit-Pet-Hamster.md    

# microbit-Pet-Hamster_block  

## ペットハムスター  

  揺さぶられたとき  
    悲しい表情のアイコンを表示します。  
    悲しい効果音を鳴らします。  
    居眠りします。

  ロゴを短くタップしたとき  
    うれしい表情のアイコンを表示します。  
    くすくす笑う効果音を鳴らします。  
    居眠りします。


## Pet Hamster  

  When shaken
    Shows a sad expression icon.
    Sounds a sad sound effect.
    Take a nap.

  When you tap the logo briefly
    Displays an icon with a happy expression.
    Makes a giggle sound effect.
    Take a nap.

## Source code
```
"""
    Title  : Pet-Hamster
    Version: 01
    Author : Hiroyuki.Moriya
    Use    : https://makecode.microbit.org/#editor
"""
def on_gesture_shake():
    basic.show_icon(IconNames.SAD)
    soundExpression.sad.play_until_done()
    basic.show_icon(IconNames.ASLEEP)
input.on_gesture(Gesture.SHAKE, on_gesture_shake)

def on_logo_pressed():
    basic.show_icon(IconNames.HAPPY)
    soundExpression.giggle.play_until_done()
    basic.show_icon(IconNames.ASLEEP)
input.on_logo_event(TouchButtonEvent.PRESSED, on_logo_pressed)

basic.show_icon(IconNames.ASLEEP)
```
