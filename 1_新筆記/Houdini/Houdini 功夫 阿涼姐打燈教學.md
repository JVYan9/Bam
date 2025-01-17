## 一、基本介面操作
### 1. 切換鏡頭
![[Pasted image 20250114165745.png]]
### 2. 切換介面
![[Pasted image 20250114165755.png]]
1. shop 是放材質的地方
2. obj 物件 包含特效 燈光
3. out 是拆層的地方

主要打燈拆層都是在這三層運用

## 二、阿涼姐的Node
**：打開我給妳們的檔案 最簡單的方法是  把以下我截圖的東西  剪下貼上到 要製作的胡迪尼檔案上**

| ![[Pasted image 20250106135439.png]] | ![[Pasted image 20250106135443.png]] | ![[Pasted image 20250106135446.png]] |
| ------------------------------------ | ------------------------------------ | ------------------------------------ |

## 三、拆層節點 Node
在out的介面 按下tab 就可以看到工具列表：
![[Pasted image 20250109141431.png]]

### 各項基本設定：
此處的設定，在阿涼姐的Node裡都已設定好，不需要特別調整。以下說明大致看過、理解就好。

| 設定 算圖格數 鏡頭 算圖尺寸：![[Pasted image 20250109141505.png]] | 設定 算圖出去的路徑：![[Pasted image 20250109141522.png]] | 設定品質：![[Pasted image 20250109141538.png]] | 設定動態模糊：![[Pasted image 20250109141555.png]] | 設定GI **記得兩個都要用 Brute force**：![[Pasted image 20250109141720.png]] |
| ---------------------------------------------------- | ----------------------------------------------- | ----------------------------------------- | ------------------------------------------- | ----------------------------------------------------------------- |

### 🌟拆層重點🌟：

| ![[Pasted image 20250113160325.png]] | ⬅️ 簡單來說，就是把要算的物件加進去空格裡面。 |
| ------------------------------------ | ------------------------ |

#### 加入物件的方法：
##### 方法1：
按下 *（圖1）* 紅色圈選的按鈕，在 *（圖2）* 選取需要加入的物件，黃色範圍是已選取的物件。

| 圖1 ⬇️                                | 圖2 ⬇️                                |
| ------------------------------------ | ------------------------------------ |
| ![[Pasted image 20250113160840.png]] | ![[Pasted image 20250113160847.png]] |
##### 方法2：
直接打物件Node的名字。
##### 方法3：
把物件Node直接拖進去空格裡面。

#### 其他設定：
1. 打一個`*`代表「加入全部」。*（圖1）*
2. 打一個`^`可以忽略該物件。*（圖1）*
3. 可以利用物件的名稱 `*Render*` 會把所有 名稱有Render的都加進來。*（圖2）*

| 圖1 ⬇️                                | 圖2 ⬇️                                |
| ------------------------------------ | ------------------------------------ |
| ![[Pasted image 20250113161442.png]] | ![[Pasted image 20250113161852.png]] |

#### 🌟各欄位特性說明🌟：

| ![[Pasted image 20250114192829.png]] |
| ------------------------------------ |
1. <span style="color:rgb(255, 0, 0)">Candidate</span> 欄位：obj node 右邊點藍色的 就會算出來 *（上圖右上角所示）*
2. <span style="color:rgb(0, 176, 240)">Force</span> 欄位：可以從右邊加入 加入之後藍燈沒亮也算得出來  
3. <span style="color:rgb(255, 221, 0)">Phantom</span> 欄位：加入之後算不出來 就像maya裡 關掉visible的效果
4. <span style="color:rgb(208, 134, 228)">粉紫色的框框</span>  是搭配要一起用的

##### 範例（一） 設定Matte：
**Forced Matte** 和 **Matte Parms From** 這兩個欄位常常拿來設定算影子。
![[Liang-01.png]]

##### 範例（二） 算影子：
這個例子是 算名稱有_RBD_物件 在 Render_Wall Render_Matte_Building上的影子
![[Pasted image 20250115182449.png]]