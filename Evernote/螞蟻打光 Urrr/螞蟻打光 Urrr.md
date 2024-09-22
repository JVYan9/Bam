---
---
Render layer的collection要分層：

* CH
* LIT
* BG

![[Github main/Evernote/螞蟻打光 Urrr/_resources/螞蟻打光_Urrr.resources/image.png]]

### ==Primary Visibility 拖進去collection會設定好==

陰影部分不能全黑，2D會拉不上去

![[Github main/Evernote/螞蟻打光 Urrr/_resources/螞蟻打光_Urrr.resources/image.2.png]]

## ==小檔圖墊在後面==

![[Github main/Evernote/螞蟻打光 Urrr/_resources/螞蟻打光_Urrr.resources/image.11.png]]

要設定兩個都Brute Force，不然會出問題
「算圖出錯，有經驗的都知道是這個問題。」Said by 阿涼姐
![[Github main/Evernote/螞蟻打光 Urrr/_resources/螞蟻打光_Urrr.resources/image.5.png]]

### ==Matte==

![[Github main/Evernote/螞蟻打光 Urrr/_resources/螞蟻打光_Urrr.resources/image.7.png]]

### ==Cryptomatte==

![[Github main/Evernote/螞蟻打光 Urrr/_resources/螞蟻打光_Urrr.resources/image.8.png]]![[Github main/Evernote/螞蟻打光 Urrr/_resources/螞蟻打光_Urrr.resources/image.9.png]]

# ==[Redshift Renderer (maxon.net)](https://help.maxon.net/r3d/maya/en-us/#html/Redshift+Renderer.html?TocPath=_____1)==

# Document⬆️⬆️⬆️

<https://www.youtube.com/watch?v=7ZpGhpik_OA>
![[1677149562570 (1).jpg]]![[1677149645207 (1).jpg]]

![[Github main/Evernote/螞蟻打光 Urrr/_resources/螞蟻打光_Urrr.resources/image.12.png]]

## ==只算玻璃的陰影，不要有建築其他結構的陰影：==  ==（後來發現其實把建築的cast shadow關掉就好了……下面是晏平的作法。）==

建築其他結構：材質 - shadowcatcher，visibility -
![[Github main/Evernote/螞蟻打光 Urrr/_resources/螞蟻打光_Urrr.resources/image.14.png]]

玻璃：visibility - 正常設定
![[Github main/Evernote/螞蟻打光 Urrr/_resources/螞蟻打光_Urrr.resources/image.13.png]]

## ==算圖須注意鏡頭有無校正==

## ==傳到slack要標註並附上校正STmap==

**==Position==**和**==Z depth==**是計算空間
晏平叫我套自發光材質，阿涼姐說沒有道理，沒有算光，材質不影響算圖。
把燈全部關掉，就不會算材質，算P和Z時可以這樣做。

### ==必要設定↓==

![[Github main/Evernote/螞蟻打光 Urrr/_resources/螞蟻打光_Urrr.resources/image.16.png]]

## 兩顆==光球==

灰球 Roughness metalness 都調最不反
反光球球 Roughness = 0, IOR = 0

玻璃的材質Diffuse color都會是黑色，黑色最乾淨。
如果像台灣啤酒的深綠色玻璃罐，會是Refraction color 是深綠色，Diffuse color一樣會是黑色。
