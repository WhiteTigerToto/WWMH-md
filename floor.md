### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

<!-- ### @flyoutOnly true -->
### @hideIteration true
### @explicitHints 1

# Dance Floor

## Step 1
牆上的顏色似乎與地板上的顏色相同。 您需要幫助神奇女俠以牆上看到的次序在地板彩色塊上移動。 這樣應該解鎖牆面的秘密門。

**可用方塊：**  
``||ww:Move <direction> by <number>||`` - 神奇女俠將往指定【方向】移動指定【數目】的格數。  
``||ww:Turn <direction>||`` - 神奇女俠將往指定的【方向】轉動。  
``||loops:repeat <number> times||`` - 以指定的【數目】重複代碼。

```ghost
player.onChat("run", function () {
    ww.moveWW(Direction.Forward, 1)
    ww.turnWW(LEFT_TURN)
    for (let index = 0; index < 4; index++) {
        
    }
})
```
```template
player.onChat("run", function () {
    ww.moveWW(Direction.Forward, 1)
    ww.turnWW(RIGHT_TURN)
})
```
```package
minecraft-ww1984=github:ReWrite-Media/ww1984-ts
```
