"# lab1-traffic-light-chien-yu-hsu" 
# Embedded_OS_Lab1_NE6091116
## Overview

Use multitask to implement LED and button. LED have two state,when the button is pressed,the LED will switch to another state.

## LED_Task
定義兩個整數，分別是接收參數和模式的切換。mode=0&1分別代表兩種狀態的LED。當我們壓下button，便會進入到其中一種狀態。

<img width="350" alt="lab1 led_task" src="https://user-images.githubusercontent.com/80887185/123582159-eb605480-d80f-11eb-874c-64dcbb11fac3.PNG">

**1. mode = 0**

當綠燈亮或紅燈發亮時，都會不斷地確認mode有無改變。

<img width="472" alt="lab1 mode0" src="https://user-images.githubusercontent.com/80887185/123582615-b3a5dc80-d810-11eb-9eb2-b97e516a86a4.PNG">

**2. mode = 1**

設定紅燈為每1000ms就會熄滅一次，達到紅燈閃爍的效果。一樣在每行步驟執行時都會判斷mode有無改變。

<img width="459" alt="lab1 mode1" src="https://user-images.githubusercontent.com/80887185/123583642-8ce8a580-d812-11eb-9486-3a73791c5b52.PNG">

## Button_Task

用prevState和curState來記錄先前和現在的狀態。並且判別現在的狀態和先前的狀態是否相同，若狀態不相同就把現在的狀態assign給先前的狀態。

<img width="418" alt="lab1 buttontask" src="https://user-images.githubusercontent.com/80887185/123592069-58c7b180-d81f-11eb-9d3f-a07464f00ee9.PNG">
