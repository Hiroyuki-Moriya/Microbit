microbit-Trial_LEDcontrol_python.md    

microbit-Trial_LEDcontrol_python    
  LEDを制御するプログラムの例    

  ボタンAが押されたら、LEDを左上から右下に順次点灯する  
  ボタンBが押されたら、その時の位置を退避する  
  シェイクされたら、位置を桁(col)、行(row)の順に表示する  

Example of a program that controls LEDs  
  When button A is pressed, LED light up sequentially from top left to bottom right.  
  When button B is pressed, the current position is saved.  

 After being shaken, display the position in the order of column and row.  


Tips   
　イベント関数の間で値を共有する変数を使うときは、  
　まず最初に `変数=0` で変数の型を宣言しておく。  
　次に、各々の関数の最初で、 `global 変数1, 変数2` と宣言する。   
