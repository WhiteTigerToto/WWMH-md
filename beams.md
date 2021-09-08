### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

<!-- ### @flyoutOnly true -->
### @hideIteration true 
### @explicitHints 1

# Beams of Color

## Step 1
牆壁上顯示了一組顏色次序。您需要幫助神奇女俠將彩色玻璃以牆壁上的次序放在光束的頂部，請告訴她往哪裡移動和放置哪種顏色。

**可用方塊：**   
``||ww:Move <direction> by <number>||`` - 神奇女俠將往指定【方向】移動指定【數目】的格數。  
``||ww:Turn <direction>||`` - 神奇女俠將往指定的【方向】轉動。  
``||ww:Place <color> Stained Glass <direction>||`` - 往指定【方向】放置一塊【顏色】玻璃。  
``||loops:repeat <number> times||`` - 以指定的【數目】重複代碼。  

```ghost
player.onChat("run", function () {
    for (let index = 0; index < 4; index++) {
        ww.moveWW(Direction.Forward, 1)
        ww.turnWW(LEFT_TURN)
        ww.placeBlock(BeamsGlass.YellowStainedGlass, Direction.Forward)
    }
})
```
```template
player.onChat("run", function () {
    ww.moveWW(Direction.Forward, 3)
    ww.placeBlock(BeamsGlass.LimeStainedGlass, Direction.Right)
})
```
```package
minecraft-ww1984=github:ReWrite-Media/ww1984-ts
```
