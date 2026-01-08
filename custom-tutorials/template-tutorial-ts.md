### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @flyoutOnly 1
### @explicitHints 0
### @diffs true

# Template Tutorial

```typescript
player.onChat("run", function () {
	
})
```


```ghost
function build_walls(side: any) {
    agent.teleportToPlayer()
    agent.move(UP, 1)
    agent.move(LEFT, 3)
    agent.setItem(STONE_BRICKS, 64, 1)
    for (let index1 = 0; index1 < 4; index1++) {
        for (let index2 = 0; index2 < side; index2++) {
            agent.place(DOWN)
            agent.move(FORWARD, 1)
        }
        agent.turn(TurnDirection.Left)
    }
}

player.onChat("walls", function on_on_chat(side2: any) {
    build_walls(side2)
})
```
