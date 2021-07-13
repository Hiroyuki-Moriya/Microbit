microbit-Trial_LEDcontrol_python.md    

microbit-Trial_LEDcontrol_python    
  LEDを制御するプログラムの例    

  ボタンAが押されたら、LEDを左上から右下に順次点灯する  
  ボタンBが押されたら、その時の位置を退避すると同時に半分の明るさでLEDをつける  
  シェイクされたら、位置を桁(col)、行(row)の順に表示する   

Example of a program that controls LEDs  
  When button A is pressed, LED light up sequentially from top left to bottom right.  
  When button B is pressed, the position at that time is retracted and at the same time the LED is turned on at half the brightness.  
 After being shaken, display the position in the order of column and row.  


Tips   
　イベント関数の間で値を共有する変数を使うときは、  
　まず最初に `変数=0` で変数の型を宣言しておく。  
　次に、各々の関数の最初で、 `global 変数1, 変数2` と宣言する。   


### Source code
```
"""
    Title  : Trial_LEDcontrol_python
    Version: 02
    Author : Hiroyuki.Moriya
    Use    : https://makecode.microbit.org/#editor
"""

"""
ボタンAが押されたら、LEDを左上から右下に順次点灯する
ボタンBが押されたら、その時の位置を退避すると同時に半分の明るさでLEDをつける
シェイクされたら、位置を桁(col)、行(row)の順に表示する
Tips
　イベント関数の間で値を共有する変数を使うときは、
　まず最初に `変数=0` で変数の型を宣言しておく。
　次に、各々の関数の最初で、 `global 変数1, 変数2` と宣言する。

"""

sv_row = 0
sv_col = 0
ex_row = 0
ex_col = 0
led.plot(0, 0)
basic.pause(500)
led.plot(2, 2)
basic.pause(500)
led.plot(4, 4)
basic.pause(500)
led.unplot(4, 4)
basic.pause(500)
led.unplot(2, 2)
basic.pause(500)
led.unplot(0, 0)

def on_button_pressed_a():
    global ex_row, ex_col, sv_col, sv_row
    ex_row = 0
    while ex_row < 5:
        ex_col = 0
        while ex_col < 5:
            led.plot(ex_col, ex_row)
            basic.pause(500)
            led.unplot(ex_col, ex_row)
            led.plot_brightness(sv_col, sv_row, 128)
            ex_col += 1
        ex_row += 1
input.on_button_pressed(Button.A, on_button_pressed_a)

def on_gesture_shake():
    basic.clear_screen()
    basic.show_arrow(ArrowNames.EAST)
    basic.show_number(sv_col)
    basic.show_arrow(ArrowNames.EAST)
    basic.show_number(sv_row)
input.on_gesture(Gesture.SHAKE, on_gesture_shake)

def on_button_pressed_b():
    global sv_col, sv_row
    sv_col = ex_col
    sv_row = ex_row
input.on_button_pressed(Button.B, on_button_pressed_b)
```
