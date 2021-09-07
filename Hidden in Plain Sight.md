### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @flyoutOnly true
### @hideIteration true
### @explicitHints 1

# Hidden in Plain Sight

## Step 1
計劃這次罪犯的主謀隱藏了在人群中。 您需要幫助神奇女俠檢查每個人來弄清楚哪個是偽裝的小偷，然後使用真言套索來獲得最終的畫作碎片。

**可用方塊：**  
``||ww:Move <direction> by <number>||`` - 神奇女俠將往這個【方向】移動指定【數目】的格數。   
``||ww:Turn <direction>||`` - 神奇女俠將往指定的【方向】轉動。   
``||ww:attendee is the thief <direction>||`` - 返回一個布爾值（【true / 是】 | 【false / 否】）關於參加者是不是小偷。   
``||ww:Lasso thief <direction>||`` - 讓神奇女俠對小偷上使用她的真言套索。   
``||loops:repeat <number> times||`` - 以指定的【數目】重複代碼。     
``||loops:while <boolean>||`` - 當布爾值為【true / 是】時重複運行代碼。   
``||logic:if / then||`` - 檢查條件是否為【true / 是】，然後如果它是就這樣做。     
``||logic:not <boolean>||`` - 切換條件的操作。 示例： 【當<true / 是>】 vs. 【當不是<true / 是>】   

```ghost
player.onChat("run", function () {
    ww.moveWW(Direction.Forward, 1)
    ww.turnWW(LEFT_TURN)
    for (let index = 0; index < 4; index++) {
        
    }
    if (ww.locateGoon(Direction.Forward)) {
        ww.apprehendGoon(Direction.Forward)
    }
    while (!(false)) {
        
    }	
})
```
```template
player.onChat("run", function () {
    if (ww.locateGoon(Direction.Forward)) {

    }
})
```
```package
minecraft-ww1984=github:ReWrite-Media/ww1984-ts
```