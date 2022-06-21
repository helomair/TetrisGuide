# 方塊教學相關

[TOC]

---

## 0. 簡介

作者： Helomair

寫這些是想把多年來的經驗記錄下來，並且拿來教社群中的新人，如果對你有幫助，那麼也請你把這教學分享給身邊喜歡玩方塊的朋友

<span style="font-size: 30px; color: red">請勿將教學的內容拿去營利 </span>

歡迎加入台灣俄羅斯方塊社群Discord (https://discord.gg/MEgjDcbt2n)！

## 1. [類型與機制概覽](https://medium.com/@very860112/%E4%BF%84%E7%BE%85%E6%96%AF%E6%96%B9%E5%A1%8A-%E5%BE%9E%E5%85%A5%E9%96%80%E5%88%B0%E9%80%80%E5%9D%91-%E5%85%A5%E9%96%80%E7%AF%87-1-a6f4c92cf407)
俄羅斯方塊分為兩種，2001年以前的```Classic Tetris```，和之後的```Guideline Tetris```。

Classic 在此不多贅述，相關資訊可以看[啾啾鞋的介紹](https://www.youtube.com/watch?v=Dh9VaezvVnU)，目前算是The Tetris Company主要在推廣的項目 (因為有官方世界大賽)

Guideline 則是 The Tetris Company 從2001年開始制定的一系列標準，規定未來方塊遊戲須根據此標準製作

所以基本上，從2001年開始有官方授權的Tetris遊戲都叫Guideline Tetris (或是有照標準做的非授權也算)

台灣比較早期接觸到的Guideline Tetris應該是TGM3，當時對戰類並沒有那麼盛行，直到2010年Tetris Battle橫空出世。

而標準中制訂的相關機制，比較主要的有：

* **版面大小：**
> 10 * 40，上層20列為隱藏區塊讓玩家以為只有10 * 20。 假如硬體效能允許的話，可顯示部分第21列。

* **方塊顏色**
![](https://i.imgur.com/aoVLZjK.png)


* **7 bag random**
> 每次7個方塊一組，順序隨機，7個走完後再進行下一組

* **預設按鍵**
> 定義所有操作的預設鍵位，包含鍵盤、手把、手機按鍵等

* **Hold**
> 玩家可以存放一個方塊在hold欄中

![](https://i.imgur.com/2s9Xv7b.png)


* **Super Rotation System (SRS)**
> 其中制定了踢牆機制

* **Next piece queue**
> 顯示接下來的方塊

![](https://i.imgur.com/FEhJoNY.png)


* **計分表 (B2B & Combo)**
> 有興趣可以看看
> [完整計分表](https://tetris.wiki/Scoring#Recent_guideline_compatible_games)
> [Combo 定義](https://tetris.wiki/Combo)

* **垃圾行機制**
> 有興趣也可以先看看，後面會介紹垃圾行機制在對局中的影響
> https://tetris.wiki/Garbage

* **T轉**
> 有興趣也可以先看看，後面會介紹完整的T轉機制
> https://tetris.wiki/T-Spin

* **方塊影子**
> 原文是寫Ghost piece，就是方塊正下方有個影子可以讓玩家知道方塊下去會在甚麼地方

![](https://i.imgur.com/jqlfPc4.png)

* **etc....**

以上列的幾個是比較主要的，其他像是Level、Timing、Music我就不詳細寫了，有興趣可以查看[Tetris Wiki](https://tetris.wiki/Tetris_Guideline)

## 2. 平台

> 此處放置一些社群常用的平台以供參考，如果有需要新增的話可以留言或是聯絡我

| 名稱                      | 網址 | 簡介 |
| --------                 | -------- | -------- |
| Tetris Battle            | [網址](https://zh.wikipedia.org/wiki/Tetris_Battle)     | 已停運，台灣人的回憶，許多老玩家入坑的遊戲  |
| Tetrio                   | [網址](http://tetr.io/)     | 由[osk](https://osk.sh/)開發，在線人數相當高，對戰UI寫得很好很適合拿來辦比賽。改動Combo表讓4w的威脅度直線下降。有相當華麗的特效，顯卡撐得住的話可以特效全開試試。    |
| Jstris                   | [網址](https://jstris.jezevec10.com/)     | 由[jezevec10](https://github.com/jezevec10)開發，在Tetrio出來以前大部分玩家都聚集在這裡。定期舉辦Js Cup。擁有相當強大的回放功能和許多模式可以拿來練習。  |
| Tetris Online Poland     | [網址](http://tetrisonline.pl/)     | 由Wojtek開發，TOJ改寫而來。一般簡稱TOP，Combo傷害非常高，早期TB跟TF還在營運時就有一部份玩家轉移過來，因為只有一條命所以對局時會考慮更多。當時相較於TB也不會那麼卡。      |
| Puyo Puyo Tetris         | [網址](https://store.steampowered.com/app/546050/Puyo_PuyoTetris/)     | Sega開發，有PS4 NS PC等版本，於2020年推出2代，**很適合新手入坑**。由於消行有延遲，要避免沒效率的消除，此平台的高手效率都很高。作為訓練效率算是挺有幫助的。     |
| Tetris Effect: Connected | [網址](https://www.tetriseffect.game/connected/)     | 原版推出時是沒有對戰的，主打音樂跟華麗特效，後續出了Connected才有對戰功能，有zone的對局模式還挺有趣的。**有史以來第一個願意修改Combo Table的官方遊戲**     |


## 3. 踢牆機制
<span style="font-size: 30px; color: red"> **懶人包：** </span>
正文基本上都在講解機制，如果只是想學怎麼轉的話可以看看[保羅方塊旋轉教學](https://www.youtube.com/watch?v=UdYri9Kx6Zs)
或是直接看正文最後一部分**常用踢牆技巧**
>補充： 最懶的方法就是，把方塊卡到該位置後，順轉逆轉各按四下，進不去就拿180轉試試，~~不行就算了~~

<span style="font-size: 30px;"> **正文：** </span>

> 本文圖片皆來自 https://tetris.wiki/Super_Rotation_System

Super Rotation System (以下簡稱SRS) 中定義了方塊初始方向與位置、方塊基本旋轉、踢牆判定
本文重點講解踢牆，其他的部分看情況補上。
本文會根據**方塊重心**、**踢牆判定**、**踢牆後移動方式**、**常用踢牆技巧**等部分講解

### **方塊重心**

先看看下面這張圖，每一行最左邊為方塊起始狀態，後面為每次按下順轉後的情況
根據定義，方塊的旋轉都是繞著重心在旋轉，單方向按下四次後會回到初始狀態
所以方塊一般來說
<span style="font-size: 18px;">**不會因為旋轉而改變重心的水平位置**</span>
<span style="font-size: 18px;">**不會因為旋轉而改變重心的水平位置**</span>
<span style="font-size: 18px;">**不會因為旋轉而改變重心的水平位置**</span>
**而唯一的例外就是踢牆**
![](https://i.imgur.com/yih7md7.png)
> 圖片來源：https://harddrop.com/wiki/File:SRS-pieces.png

### **踢牆判定**

SRS 定義了四種代號來代表方塊旋轉的方向：
* 0 = 起始狀態
* R = 從起始狀態按一次順時鐘旋轉 (右)
* L = 從起始狀態按一次逆時鐘旋轉 (左)
* 2 = 從起始狀態按兩次順轉 (或是逆轉)，總之就是轉180度

踢牆發生於 **方塊基本旋轉受阻** (撞到牆面或地面，或是跟現有堆疊卡到)
> 以下為 J 方塊逆轉後，會發現有一部份跟目前場面卡到，便會觸發踢牆機制，判定方塊最終位置

> 之所以會這樣轉是因為 J 方塊的重心在長條部分的中間，仔細看下圖就會發現那格不會因為單純旋轉而改變位置

![](https://i.imgur.com/Qs6HkCC.png)

下一部份講解踢牆移動機制

### **踢牆後移動機制**

踢牆機制觸發後會有5次位置判定，Test1 ~ Test5，過程中有地方判斷成功就中斷判定並將方塊放置
假如過Test 5後都沒有地方可放，便判定此次旋轉失敗，回覆上一動。

J, L, S, T, Z 使用同一個判定表 ，I 方塊自己獨立一個判定表，O沒有踢牆機制
表格中的座標為重心座標，(0,0)就是當前位置，(+1,0)就是重心往右一格，以此類推
![](https://i.imgur.com/eymKhOH.png)

看得很混亂對吧，以下給個範例，請根據第一張表的最下面0->L那行來看

![](https://i.imgur.com/TiCne1q.png)

1. 起始位置，按一下逆轉
2. Test 1，重心於(0,0)位置不可放 (因為和目前場面卡到)
3. Test 2，根據表格將重心移到(+1,0)做判定，依舊不可放
4. Test 3，根據表格將重心移到(+1,+1)做判定，依舊不可放
5. Test 4，根據表格將重心移到(0,-2)做判定，依舊不可放
6. Test 5，根據表格將重心移到(+1,-2)做判定，可放，此次旋轉成功。

### **常用踢牆技巧**
> 建議可以看看 https://harddrop.com/wiki/SRS 下面的Wall Kick Illustration，詳細且有圖片說明
> 這裡目前僅列出作者在實戰中常用的，180度轉看情況更新
#### S 方塊 (<span style="color: green">綠 </span>)
1. 左右無高牆，先 R 一次卡到定點，再 R 一次可進
![](https://i.imgur.com/Ax5c0NN.png)
2. 左右有高牆，進洞前先 **L** ，到底後再 **L** 一次可進
![](https://i.imgur.com/rzgZckE.png)

#### Z 方塊 (<span style="color: red">紅 </span>)
> 跟S完全相反
1. 左右無高牆，先 L 一次卡到定點，再 L 一次可進
2. 左右有高牆，進洞前先 **R** ，到底後再 **R** 一次可進

#### J 方塊 (<span style="color: blue">藍 </span>) L 方塊 (<span style="color: orange">橘 </span>)
1. 這種形狀可以塞進去，J順轉L逆轉

![](https://i.imgur.com/gVeGDpB.png)

在此位置順轉
![](https://i.imgur.com/GSq2vzN.png)

![](https://i.imgur.com/jOHFVen.png)

在此位置逆轉
![](https://i.imgur.com/uc6goUg.png)

#### I 方塊 (<span style="color: #00FFFF">淡藍 </span>)
> I 方塊太多，強烈建議去HD官網看完整一點
1. 以下順轉可進
![](https://i.imgur.com/e2wVAE1.png)
![](https://i.imgur.com/AaPLtHb.png)
![](https://i.imgur.com/lAFeEVF.png)


2. 以下逆轉可進
![](https://i.imgur.com/RcRkUqB.png)
![](https://i.imgur.com/FzlD3Hh.png)
![](https://i.imgur.com/mzz8cbq.png)

#### T 方塊 (<span style="color: purple">紫 </span>)
> 留到T轉機制再講


## 4. T轉機制
> 本文圖片皆來自 https://harddrop.com/wiki/T-Spin

<span style="font-size: 30px; color: red"> **懶人包：** </span>
只想知道怎麼轉的話可以直接看後面的 **常見T轉類型**

<span style="font-size: 30px"> **正文：** </span>

### 觸發條件
根據Harddrop Wiki，觸發條件有三：
1. 必須是 T 方塊
2. **最後一次**動作必須是旋轉 
> 左右移、下降、因重力下降都不可以，必須旋轉後到定點，旋轉後踢牆後到定點也行
3. 符合 3-corner 原則

### 3-corner 原則
3-corner 指的是 T 方塊的四個角中有三塊角落是有方塊的，以下給個範例
![](https://i.imgur.com/KUcIZxF.png)
可以看到，最右邊那張圖的三個黑色的方格，他們各占了T方塊所框出來的九宮格的角落，佔了三個以上就符合3-corner 原則

下面給個不符合的範例
![](https://i.imgur.com/0v6yqXg.png)
很明顯只有兩格，不符合3-corner 原則

### T-spin mini 機制
mini是一種比較奇特的T-spin，傷害較低但是因為還是T-spin，所以能維持back-to-back效果 (後面會講解b2b機制)
一般來說，Mini的觸發條件為**踢牆後**的T-spin，且只消 0 ~ 1 行 (所以TST雖有踢牆，但如果消2行以上就不算mini，只消1行的話要看遊戲怎麼定義)
但根據遊戲，有些Mini會被認為是正常的T-spin，下面給個範例
**Case A.**
![](https://i.imgur.com/kTyBBjM.png)

**Case B.**
![](https://i.imgur.com/LgU4XcU.png)

**Case C.**
![](https://i.imgur.com/TufrRuM.png)


| 遊戲      | Mini     | Not Mini |
| -------- | -------- | -------- |
| Tetris DS (Singleplayer)       | A B     | C     |
| Tetris Online (Japan)          | B       | A C     |
| Tetris Friends                 | C       | A B     |
| Jstris                         | C       | A B     |


### 常見T轉類型
> T轉種類繁多，這裡只列出最基本的，歡迎上HD Wiki看更多 https://harddrop.com/wiki/Category:T-Spin_Methods

#### TSS (T-spin Single)
> 這個只是做個範例，右邊補上三格就可以是TSD

![](https://i.imgur.com/RxlF93m.png)


#### TSD (T-spin Double)
![](https://i.imgur.com/UsWDYx9.png)

#### TST (T-spin Triple)
> 這裡根據踢牆機制，T方塊立直，面朝右，進洞後兩次逆轉可以下去

![](https://i.imgur.com/0lphg4F.png)

#### STSD
> 可消兩個TSD

![](https://i.imgur.com/tRNYpul.png)

![](https://i.imgur.com/MbJZ84p.png)

![](https://i.imgur.com/8mm3p0U.png)

#### T-spin mini Single
> 貼地貼牆後順轉，注意牆必須三格高

![](https://i.imgur.com/ouNQSD8.png)
![](https://i.imgur.com/8PpRrkt.png)
<br>

> 這也是一種mini，進洞後逆轉

![](https://i.imgur.com/3gHuyx1.png)
![](https://i.imgur.com/Jtb6ZoX.png)


#### T-spin mini Double
可以先看看這張動圖 https://harddrop.com/w/images/7/77/T-Mini_Double.gif
分為Neo跟Fin
Neo:
![](https://i.imgur.com/UCyog0x.png)
Fin:
![](https://i.imgur.com/baHcARN.png)

#### King Crimson
> Triple消完後就有一個STSD可用

![](https://i.imgur.com/ZXkxnoR.png)

#### Imperial Cross
> 兩個TSD

![](https://i.imgur.com/QjfrfGL.png)

![](https://i.imgur.com/LEeamLQ.png)

![](https://i.imgur.com/0p1I4O4.png)


## 5. 計分、傷害、為何要T轉？
<span style="font-size: 30px; color: red"> **懶人包：** </span>
~~當然就是帥啊~~

簡單來講，在有B2B的情況下，一個T-spin double 消 2 行送給對方 5 行，一個Tetris 消 4 行但也送給對方 5 行，所以T-spin的效益比較高。
實際上當然不只這樣，但最簡單的講法我覺得這樣就夠了，剩下的我放到正文講。


<span style="font-size: 30px"> **正文：** </span>
這部分會簡述一般的傷害機制，及各平台的傷害差異

### Back to Back (B2B)
#### 定義
B2B 機制根據定義，是特殊消行後，下次消行也為特殊消行時，下次消行會帶有B2B效果
> 特殊消行：一般來說就是 T轉 跟 Tetris。有的平台可能會定義SZ轉也算，但那些是例外不在此討論。

而B2B效果就是**傷害多送 1 行**，很直觀吧？
如果不太懂後面會有例子

### T轉
我們先撇除 mini 的情況，一般的傷害表的定義，**T轉的傷害是消行的2倍**

所以 

| 類型               | 消行   | 攻擊 |
| -------- | -------- | -------- |
| T-spin Single     | 1     | 2     |
| T-spin Double     | 2     | 4     |
| T-spin Triple     | 3     | 6     |
| Tetris            | 4     | 4     |

再加上前面的 B2B 效果
| 類型               | 消行   | 攻擊 |
| -------- | -------- | -------- |
| B2B T-spin Single     | 1     | 3     |
| B2B T-spin Double     | 2     | 5     |
| B2B T-spin Triple     | 3     | 7     |
| B2B Tetris            | 4     | 5     |

大概是這樣，但前面一直有提到的，**平台間可能會有差異**，所以我這裡提的是常見的定義

那麼 mini 呢？
mini 就是**傷害減半，減半後再加上B2B傷害(如果有的話)**
| 類型               | 消行   | 攻擊 |
| -------- | -------- | -------- |
| T-spin Single Mini     | 1     | 1     |
| B2B T-spin Single Mini     | 1     | 2     |

(但 Puyo Puyo Tetris 的 Mini 是不送行，有B2B送一行)

**下面放個平台傷害簡表來給讀者一個參考**
![](https://i.imgur.com/H8lBne4.png)


### Combo

在講解Combo 前先講一個觀念，那就是**單消其實很耗資源**
因為除了Tetris以外，其他單消的傷害都是消的行數 -1
所以

| 類型               | 消行   | 攻擊 |
| -------- | -------- | -------- |
| Single             | 1     | 0     |
| Double             | 2     | 1     |
| Triple             | 3     | 2     |
| Tetris            | 4     | 4     |

知道了這件事後我們下面來講Combo。

Combo 我們有時也稱之為 ren，反正就是連消
有經歷過 Tetris Battle 時期的玩家應該都有練過 留 2 3 4 的打法，這些打法就是用combo去輸出
但為何留4 (以下簡稱4W) 傷害會這麼高？
請先看看以下這張表
![](https://i.imgur.com/akWiXC1.png)

可以看到，後續消行的傷害加成非常噁心，這也是 4W 會強大的一個原因，一個單消媲美一個T-spin，還不會破壞地形，簡單粗暴

關於 Combo 跟 4W 的話題先到這，後面我特別留了一個章節來講解為何社群討厭4W，敬請期待。



### 為何要T轉？
第 4 章有講解了T轉的判定，前兩部分也講解了傷害機制，但為何我們需要練T轉？ ~~當然就是因為帥啊~~

直觀來講就是 **效率**

下面用 ``` 效率 = 傷害 / 消的行數 ``` 的公式來看各種情況，**皆消除8行**，此公式代表每消一行會送給對手多少傷害。
**注意：假如都有B2B的話，T-spin跟Tetris的順序對換的話傷害是不會變的，你可以算算看**
**注意2：使用 Puyo Puyo Tetris 的傷害表**

| 情況      | 總傷害    | 效率 |
| -------- | -------- | -------- |
| T-spin Double + B2B T-spin Double + B2B Tetris     | 4 + 5 + 5 = 14     | 14/8 = 1.75    |
| T-spin Double + B2B T-spin Double * 3     |  4 + 5 * 3 = 19     | 19/8 =  2.375    |
| T-spin Triple + B2B T-spin Triple + B2B T-spin Double     |  6 + 7 + 5 = 18     | 18/8 = 2.25    |
| Tetris + B2B Tetris     |  4 + 5 = 9     | 9/8 = 1.125    |
| 8 Combo (全單消)     |  16     | 16/8 = 2    |
| 無Combo，單消8行     |  0     | 0/8 = 0    |
| 無Combo，消 Double * 4     |  4     | 4/8 = 0.5    |

大概看得出來了吧，單消多沒效率

那我們是不是從頭到尾就無腦疊 T-spin Tetris跟維持B2B就可以贏了呢？ ~~是~~

**是，但不完全是**

這遊戲是雙方互相攻擊的，無腦B2B的話很容易被炸回來，這部分留到後面對局部分會有講解

## 5.1 特例：Tetr.io
這部分算是補充，不會寫太多，所以沒有懶人包。

在TB關閉的現在，Tetrio算是比較多人入坑的一個選項了，但由於Tetrio做了一些改動，所以以前的打法在這裡是不能用的

先講結論： **T-spin、Tetris、B2B的效益遠大於單純打Combo**，更直觀的來說就是3W 4W被大幅削弱。

首先我們來看一下傷害表

![](https://i.imgur.com/VEfR6Jx.png)

1. Single 到了 10 combo 以上還是只有送 2 行，打 4W 打了 15 Combo也總共只會送 24 行，效益低且風險高。

2. Quad (Tetris)等高輸出手段在高 Combo 的情況下消行會有傷害加成，所以打了幾個Combo後接個Tetris會非常痛。

3. 連續的 B2B 也會有額外的傷害加成，圖表右邊有B2B Level，不同Level有不同的傷害表。

## 6. 對局

<span style="font-size: 30px; color: green">**前言：**</span>
對局有非常多東西可以講，但因為這篇文章是寫給新人看的，所以只會講解非常基礎的東西而已

未來可能會開個進階篇的文章來講更多對局的觀念

進階篇連結：\<Undefined\>

<span style="font-size: 30px; color: red"> **懶人包：** </span>
因為垃圾行機制，大攻擊容易被打回來，所以傷害高不一定會贏

手速快的不一定會贏，放的方塊多不代表他的傷害會跟著高

隨時關注對手情況有助於打贏對方

<span style="font-size: 30px; color: black"> **正文：** </span>

對局要講些啥我想了很久，因為東西太多了，而且每個玩家的對局觀念也會有所不同，要寫出一些能給新人看的其實很難。

所以這部分會講一些對局該注意的機制跟基礎觀念，不會太深，有個印象就好。

### 垃圾行機制

間單來講就是：**同一波攻擊，垃圾行的洞會在同一個位置**

下面是最直觀的例子，對面打了一個Perfect Clear 送了12行，那麼這12行的垃圾洞理論上會在同一個地方

![](https://i.imgur.com/6CRSVtP.png)

雖然還是有平台差異，但目前比較熱門的平台中除了Puyo Puyo Tetris以外，垃圾行機制是差不多的

**目前也只有Puyo Puyo Tetris的垃圾行是系統協助打散的 (30% 分散)**

### 乾淨的垃圾行

上一章在講傷害時有講過，是否無腦B2B就一定會贏了？ **不一定**

B2B的大傷害送給對方的垃圾行是非常乾淨的，其實是送資源給對手打回來，會被頂到天上去

有些玩家的打法就是利用對手送的垃圾行來打反擊的，你打越多過去，回來的就更多

所以無腦 B2B 不一定會贏

### 凌亂的垃圾行

打大攻擊會被對手得到乾淨的垃圾行進而被打回來，那有沒有辦法控制？ 

**有，但偏難**

會有乾淨的垃圾行是因為一次消行後送的攻擊太大，那只要打散就好了，兩次T-spin之前多一點小的下消，或是T-spin後接下消，這樣對手就會有一部分乾淨的垃圾行 + 亂的垃圾行。

下面給個噁心一點的例子

![](https://i.imgur.com/FxoSx4b.png)

對面如果都是打 Combo ，然後你全吃下來的話就有可能長這個樣子

### 垃圾行機制對局勢的影響

亂的垃圾行會比較難挖，實際影響就是不好打輸出，也不好做防禦，拖慢整體節奏。
但要讓對手吃下亂的垃圾行偏難，因為大多時候下消的Combo會被對手抵銷，傷害不夠。

乾淨的垃圾行好挖，會被對方一波完全打回來。
但前提是對手吃了你一大波攻擊後還有辦法活下來，如果你的輸出比對方高且持續輸出的話，那對手有可能沒機會把資源打回來。

如果是剛接觸這遊戲不久的人的話，其實不用太在意這些東西，在往上練了之後會自然感受到這個機制的影響，現在有個印象就好。

另外 **4W 強大的一個原因也是因為垃圾行機制**，原因可以先自己想一想，這留到後面一起講。

### Timing

Timing 就是時機的掌握，資源送出去的時機不同會影響局勢。

一個最簡單的情況就是：
> Q： 雙方都有一個Tetris可以打，我方在低處，對方在高處，那麼這個Tetris該怎麼打？
> 
> A： 吃下對方的Tetris後再把Tetris打過去
> 因為我方吃下這波輸出沒事，但對方沒資源防守且在高處，這個吃下去可能會死，整體來說是我方占優

上面這個例子算是一個簡單的Timing例子，實際上並沒有這麼簡單，只是給讀者一個感覺

我個人對Timing的理解就是：
> 理解當前局勢，進而判斷手上的資源如何利用，打時間差攻擊或是進行防守
> 在避免自己難受的同時，嘗試讓對方難受

### 手速的影響

首先要講個觀念

<span style="font-size: 18px;">**手速快不一定會贏**</span>
<span style="font-size: 18px;">**手速快不一定會贏**</span>
<span style="font-size: 18px;">**手速快不一定會贏**</span>

很重要所以講三次

很多人會認為手速快的就有絕對優勢，其實並沒有

手速快代表的是資源量較多，但資源量多不代表效率會高，硬拉高手速的代價就是堆疊不好、效率也不好。

所以有時會看到那種速度型的雜魚，就是硬拉手速以為這樣就會贏，然而這樣會縮限自身效率，其實並沒有甚麼卵用。

簡單來講就是沒有想清楚就擺了

但速度慢也不代表效率就高，還是要看堆疊意識，堆疊好基本上效率就不會低

### 堆疊的重要性
<span style="font-size: 18px;">**堆疊是一切的基礎**</span>

堆疊就只是把場面疊平而已，很簡單吧？

堆疊意識夠好，在面對各種場況時就能做到更好的對應，大多時候場面平整的可操作空間就非常大

下面給幾個例子感受一下：
1. 左邊較優，避免場面凹凸不平
![](https://i.imgur.com/QeHhQJ1.png)
2. 右邊較優，讓左邊的洞有辦法放S 和 Z
![](https://i.imgur.com/Tx1Kh1U.png)
3. 根據Next方塊來考慮不同情況的最佳解
![](https://i.imgur.com/EXVkvW5.png)

至於堆疊怎麼練習，後面的相關練習法會講，基本上是根據當前版面和未來的方塊來考慮如何擺放

### 7 Bag

7個不同的方塊為一包，包中方塊的順序打亂，但每包互相不干涉

7 Bag 機制保證了雙方的資源相同，每個方塊的出現率也相同

也因此沒有甚麼 **對方運氣好抽到哪個方塊較多的情況**，因為你們雙方的資源是一模一樣的

## 7. 開局介紹
<span style="font-size: 30px; color: red"> **懶人包：** </span>
開局可以不用會很多，但是你要能知道對方的開局後續會有甚麼接續，知道越多就越能做出應對
**給新人的最大建議：不要只會開局**

<span style="font-size: 30px; color: black"> **正文：** </span>
開局 (Opening) 是指**從遊戲最一開始的那一包方塊，根據公式所做出的堆疊**。

下面我引用 **Noogy** 在 HD社群發表的 [A Guide on Openings](https://harddrop.com/forums/index.php?showtopic=2519) 中關於開局的介紹：

> An opener would be your initial approach to the initial bag(s) of pieces you get. 
Openers can vary in length, from quick t-spin double approaches to long combo starts. 
Many people who do not use openers will most likely use a tetris opener by default (stacking for a single tetris or a b2b tetris)

開局可長可短，可短到只有一個TSD，也有長到10+ ren以上的combo開局

本章將分為 開局的重要性、開局在對局中的影響、常見開局介紹
### 開局的重要性

<span style="font-size: 16px; color: red">**快速成形 且 效益保證** </span>

由於遊戲開局時的場面是完全乾淨的，所以你能完全知道第一包怎麼打，跟著公式走就好，不用想太多就自然會快。

前面有說過打得快，效率會下降，**但開局不一樣**。

開局的快是因為跟著公式走，並且公式保證了後面的接續和效率，所以快的同時也保證了效率，輸出會很誇張。

### 開局在對局中的影響

這裡講幾個觀念，看看有個印象就好：
1. 熟練的開局不用多，但要知道常見開局的後續接續
2. 開局可以擾亂對手節奏
3. C4W可以練，但這是拿來BM人用的我覺得還是不要常用

基本上我開局只會用 TKI、PC、DT炮、C-spin，算是比較熟悉且不會打錯的開局，但我會去注意對手的開局並思考應對。

比如說 
1. MKO 傷害接近TKI，但容易接PC
2. DT炮 傷害等於一個PC，且後續可接4W或是PC
3. Stick Spin 的火力在第三 四包中，且後續可能會有PC
4. TKI 傷害穩定，且後續可能會有PC或是接LST
5. PC 傷害高但垃圾行乾淨，等於對方送資源給我打，所以要趕快把垃圾行開出來

之類的

但開局的差異性可以很大，對手如果打個幾場就換開局的話，我也要跟著換應對，節奏會被擾亂到。

上面是簡單講一下影響，新手不用想太多有個印象就好，玩得開心最重要

### 常見開局介紹

簡單講一些，有興趣請看 [HD教學](https://harddrop.com/wiki/Opener#TKI_3_.28Fonzie_variation.29)

1. [TKI](https://harddrop.com/wiki/TKI_3_Opening)
     簡單、易懂
     隨時維持地形平坦，隨時準備DS，好用
     後續可接 [LST](https://four.lol/stacking/lst)，高手速且熟練的 LST 輸出非常驚人
     https://youtu.be/pJVyB3G3dZg
2. [DT cannon](https://harddrop.com/wiki/Double_Triple_Cannon_Setups#Empty_Field_Setups)
    可以拿來秀給剛接觸遊戲的朋友的簡單開場
    沒那麼實用且失誤會讓自己很危險，但奈何看起來很帥，有興趣還是學一下
    建議只學standard DT
3. [MKO](https://four.lol/openers/mko)
     好處在於可以讓版面維持平坦的狀態，但會需要很好的T轉概念來達到它的最大效益。
     高PC率
4. [Stick Spin](https://harddrop.com/wiki/Stickspin)
    馬來西亞玩家 Stickmancomic 發明，在Tetr.io很強 ~~(毒瘤)~~
    使用了3包做成2個 B2B T-spin double 以及B2B T-spin triple 的超高傷害開場 ，並且後面還有各種不同的pc接續
    
5. [C-spin](https://harddrop.com/wiki/C-Spin)
    在日本被叫做TKI，稍微有點不同
    T-spin Triple + Double的組合
    後面有些PC的接續，算還不錯用
6. [4W](https://harddrop.com/wiki/Opener#Combo_Openers)
    練了可以增加堆疊意識，但不要太依賴這種東西
    目前社群算是挺討厭C4W開局，理由會放在後面講
7. [Gamushiro Stacking](https://harddrop.com/wiki/Gamushiro_Stacking)
    Jstris Ultra 前世界紀錄使用的開場
    Triple Double Attack
    99%機率在TD後接PC

## 8. 中局觀念
<span style="font-size: 30px; color: green">**前言：**</span>
中盤觀念跟對局一樣有非常多東西可以講，但因為這篇文章是寫給新人看的，所以只會講解基礎的東西而已

未來可能會開個進階篇的文章來講更多中盤的觀念

進階篇連結：\<Undefined\>

<span style="font-size: 30px; color: red"> **懶人包：** </span>

場面平整就是一切，這項基礎做好了才能有更多空間去考慮接下來的事情

<span style="font-size: 30px; color: black"> **正文：** </span>

這裡講講中盤，會根據以下幾個大方向去講一些觀念
* 進入中盤
* 場面維持
* 垃圾行處理
* 有啥做啥

也推薦 [現代俄羅斯方塊世界排名第8的教學](https://youtu.be/uO7AjYgZVLc) 這支影片，8 分鐘的影片基本上把中盤該做的事都講過一遍了

### 進入中盤

並沒有一個硬性規定說中局是什麼時候開始，一般來講就是開局公式打完後就算進入中盤
因為從這裡開始，雙方比拚的就是基礎實力與觀念了，不再是照著公式走
~~有可能一方已經進中盤了，另外一方還在打開局~~
整場對局有 85% 都在中盤


個人認為對戰方塊最好玩且最精華的就是中盤，在這個時候，你每分每秒的決策都在轉變
> 自己當下的場況、next 的方塊、對手場況、對手習慣、雙方資源差、timing 時機
> 任何因素都會影響對局走向

### 場面維持

**簡單來講：維持場面平整，疊乾淨疊平**

平整的場面才有更多機會去做輸出，也能夠有更多的選擇，所有進攻防守的基礎都建立在平整的場面上

那麼，什麼叫平整？ **高度相近 (差距 2 以內)**

**平整的情況**
> 在這種場況下，方便搭 t-spin，且不需要花資源去把某一邊高度補上，隨時有個 Tetris 可以消
> 而在往上疊的過程中，就是一直不斷地去維持兩邊的高度一致

![](https://i.imgur.com/RPg6Yd0.png)

**不平整的情況**
> 在這種場況下，左邊需要 I，右邊也需要 I，兩個 I 最多相差距離 13 個方塊
> 在這個時候吃到傷害就只能往下消，傷害不會多高
> 且浪費一堆方塊，疊到這個高度可是要花很多方塊的

![](https://i.imgur.com/lNr7Aha.png)



### 垃圾行處理

> By 世界最強 czsmall
> 
> 如果意識到版面有很亂的垃圾，可以先停止當下動作並想辦法先把他們全部挖掉，留下乾淨的垃圾（如果有的話），再繼續做自己的向上堆疊

> 垃圾行是干擾也是機會，好好利用可以增加輸出。維持低高度場面，有助於後續更多的 B2B 堆疊

> 在場面於高點時，你理應考慮如何往下消而不是繼續在高處貪 T spin，會死的
> ![](https://i.imgur.com/DQ9jPws.png)





<br><br><span style="font-size: 18px;">**挖掘(dig) 基本觀念**</span>
1. 最大原則，保持場面平整
2. 其次，盡量不要擋到垃圾行

大多數時候，在做挖掘時，方塊擺放盡可能的不要去阻擋到接下來幾行的垃圾行洞 (我個人是 4 行)

但這些都是建立在擺放時場面是平整的大前提之下

有時會為了保持場面平整，蓋住垃圾行是允許的，這樣會能有更多選擇跟路線

有另外一種可能，就是**你已經想好一連串的ds路線，這裡蓋住沒關係，因為後續 ds combo 可以把它清掉**
    
基本就這樣，剩下就是經驗

[範例： Jstris cheese mode 100 L](https://jstris.jezevec10.com/replay/55249228)


<br><br><span style="font-size: 18px;">**關於 DownStack (ds) 和 挖掘 (dig)**</span>

> By Diao
> "try to not cover the garbage hole" is a misleading advice
> downstack≠100% dig  pls everyone stop getting it wrong

會跟挖掘分開來主要是因為上面 Diao 的這兩句話

我一直以來都沒有把這兩個準確分開來看過，在這裡稍微講一下自己對 ds 的想法

ds 顧名思義就是下消，但這要是有效率(傷害)的一連串消行，這對我來說才叫做 ds ~~簡單來講就是 combo~~ ~~4wide~~

所以有時高等玩家的 downstack 不會只用垃圾行，甚至會自己疊加資源，做成更大傷害的 ds combo

<br> 那挖掘呢？

純挖掘的場合，我覺得更像是**為了解場**

場面混亂，垃圾行非常雜，找不到一個合適的 ds 路徑，被迫只能放棄輸出，把當下目標改成解場，目標是達到安全且平整的場面，再接著進行輸出

在這個過程中，有可能會做出 ds combo 或是做成 t spin 做點輸出順便解場，端看你的堆疊


<br><br><span style="font-size: 18px;">**下面講講，在維持效率且要解場的前提下，有哪些其他方式可以去嘗試**</span>

1. Tetris (B2B retaining technique)
    > 補齊高度，並在消掉後開洞
    
    ![](https://i.imgur.com/MnxlQQ7.png)
    > photo from https://www.youtube.com/watch?v=uO7AjYgZVLc 2:46
    > 已授權 by Circulation

2. 預留
    > T 作為預留的 t spin 蓋子，當這個 Tetris 消完之後，左邊就有一個 t spin 可以接著用

    ![](https://i.imgur.com/JGV7yCP.png)
    
想到會再補充


### 有啥做啥
> 有 T 再做 T槽，有 I 再疊 I槽

上面那句話算是概括了這部分要講的全部東西

1. 如果都沒有 T，還去做 T槽，甚至是拿 T 去做堆疊後再做 T槽。
    那接下來可能要等 1 包的方塊量才會來下一個 T，這個 T槽才會被使用到。
    最差的情況就是被逼著拆炮，甚至是搞壞場面導致死亡
    
2. I 同理，如果疊 I槽疊太爽，所有 I 都拿去做堆疊，當緊急需要的時候卻沒有 I 可以用，甚至無法拆炮直接死亡

*其實有時不一定是上面描述的情況，也不一定要照著這個規則走，但對於剛接觸的新手來說，我認為先帶著這個觀念去練習是不錯的，未來變強之後自然會照著自身的堆疊經驗去走，而不是死守著這個規則*

<br>

> 有時手上 + next 都沒有 T，也還是能做 T槽，大多都是場面平整時
> S 往右擺當成蓋子，雖然沒有 T 可用，但隨時有個 I 可以用

![](https://i.imgur.com/9CnmJeG.png)





## 9. 相關練習方法
## 10. 攻擊手法介紹 (T spin | ren)
## 11. 反擊手法介紹 (ds)
## 12. Timing介紹
## 13. 4W為何惹人厭
## 14. 高等玩家介紹
