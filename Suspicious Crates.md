### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @flyoutOnly true
### @hideIteration true 
### @explicitHints 1

# Suspicious Crates

## Step 1
失蹤的畫作碎片被隱藏了在箱子中。您需要幫助神奇女俠搜索每個箱子來找到失蹤的畫作碎片，如果她發現失蹤畫作碎片，請讓她打破箱子來獲得它。

**可用方塊：**  
``||ww:Move <direction> by <number>||`` - 神奇女俠將往指定【方向】移動指定【數目】的格數。  
``||ww:Turn <direction>||`` - 神奇女俠將往指定的【方向】轉動。   
``||ww:painting inside crate <direction>||`` - 返回一個布爾值（【true / 是】 | 【false / 否】）關於是否有於指定【方向】尋找隱藏畫作。    
``||ww:Break crate <direction>||`` - 指示神奇女俠嘗試及收回隱藏的畫作。  
``||loops:repeat <number> times||`` - 以指定的【數目】重複代碼。    
``||loops:while <boolean>||`` - 當布爾值為【true / 是】時重複運行代碼。  
``||logic:if / then||`` - 檢查條件是否為【true / 是】，然後如果它是就這樣做。  
``||logic:not <boolean>||`` - 切換條件的操作。 示例： 【當<true / 是>】 vs. 【當不是<true / 是>】  

```ghost
player.onChat("run", function () {
    ww.moveWW(Direction.Forward, 1)
    ww.turnWW(LEFT_TURN)
    if (ww.locatePainting(Direction.Forward)) {
        ww.retrievePainting(Direction.Forward)
    }
    for (let index = 0; index < 4; index++) {
        
    }
    while (!(false)) {
        
    }	
})
```
```template
player.onChat("run", function () {
    if (ww.locatePainting(Direction.Forward)) {

    }
})
```
```package
minecraft-ww1984=github:ReWrite-Media/ww1984-ts
```