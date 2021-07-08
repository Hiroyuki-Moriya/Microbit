microbit-Trial_CommonVariables.md    

microbit-Trial_CommonVariables_python    

イベント関数の間で値を共有する変数のプログラムの例    

  ボタンAを押すと、数字を１増やして表示する  
  ボタンBを押すと、数字を１減らして表示する  

An example of a variable program that shares values ​​between event functions  
  When button B is pressed, the number is incremented by 1 and displayed.  
  When button B is pressed, the number is decremented by 1 and displayed.  



Tips   
　イベント関数の間で値を共有する変数を使うときは、  
　まず最初に `変数=0` で変数の型を宣言しておく。  
　次に、各々の関数の最初で、 `global 変数1, 変数2` と宣言する。   
