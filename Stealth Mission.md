### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @flyoutOnly true
### @hideIteration true
### @explicitHints 1

# Stealth Mission

## Step 1
小偷就在前方，不要觸發警報！您需要幫助神奇女俠避免激光器地通過房間，悄悄地走近並打倒小偷。

**可用方塊：**  
``||ww:Move <direction> by <number>||`` - 神奇女俠將往指定【方向】移動指定【數目】的格數。   
``||ww:Turn <direction>||`` - 神奇女俠將往指定的【方向】轉動。   
``||ww:Takedown criminal <direction>||`` - 往指定的【方向】悄悄地打倒小偷。   
``||loops:repeat <number> times||`` - 以指定的【數目】重複代碼。   

```ghost
player.onChat("run", function () {
    for (let index = 0; index < 4; index++) {
        ww.moveWW(Direction.Forward, 1)
        ww.turnWW(LEFT_TURN)
        ww.takedownGoon(Direction.Forward)
    }
})
```
```template
player.onChat("run", function () {
     ww.moveWW(Direction.Forward, 1)
     ww.turnWW(LEFT_TURN)
 })
```
```package
minecraft-ww1984=github:ReWrite-Media/ww1984-ts
```