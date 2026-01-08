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
player.onChat("reset", function () {
    // 1) Bring Agent back to the player
    agent.teleportToPlayer()

    // 2) Get player block position
    const p = player.position()
    const x = p.getValue(Axis.X)
    const y = p.getValue(Axis.Y)
    const z = p.getValue(Axis.Z)

    // 3) Restore the ground column beneath the player to Tunneler's Dream layers
    //    y-1: grass
    blocks.place(GRASS, pos(x, y - 1, z))

    //    y-2 .. y-6: 5 layers of dirt
    blocks.fill(
        DIRT,
        pos(x, y - 2, z),
        pos(x, y - 6, z),
        FillOperation.Replace
    )

    //    y-7: stone (start of the deep stone layer)
    blocks.place(STONE, pos(x, y - 7, z))

    // 4) Clear blocks above the player (air above "ground level" at their spot)
    blocks.fill(
        AIR,
        pos(x, y, z),
        pos(x, y + 25, z),
        FillOperation.Replace
    )
})
player.onChat("xyzabcdef", function (num1, num2) {
    player.teleport(pos(0, 0, 0))
    player.position()
    player.say(":)")
    blocks.place(GRASS, pos(0, 0, 0))
    blocks.fill(GRASS, pos(0, 0, 0), pos(0, 0, 0), FillOperation.Replace)
    mobs.spawn(CHICKEN, pos(0, 0, 0))
    mobs.monster(ZOMBIE)
    agent.teleportToPlayer()
    agent.move(FORWARD, 1)
    agent.getPosition()
    agent.place(FORWARD)
    agent.interact(FORWARD)
    agent.destroy(FORWARD)
    agent.till(FORWARD)
    agent.collectAll()
    agent.collect(IRON_SHOVEL)
    agent.inspectBlock(FORWARD)
    agent.detect(AgentDetection.Block, FORWARD)
    agent.setSlot(1)
    agent.setItem(GRASS, 1, 1)
    agent.getItemCount(1)
    agent.getItemDetail(1)
    posCamera(0, 0, 0)
    pos(0, 0, 0)
    posLocal(0, 0, 0)
    world(0, 0, 0)
    positions.add(pos(0, 0, 0), pos(0, 0, 0))
    positions.equals(world(0, 0, 0), world(0, 0, 0))
    randpos(pos(0, 0, 0), pos(0, 0, 0))
    myPosition.getValue(Axis.X)
    myPosition.toWorld()
    agent.turn(TurnDirection.Left)
    loops.pause(100)

    for (let i = 0; i < 5; i++) {
        
    }

    while (true) {
        
    }
    if (true) {
        
    }

    if (true) {
        
    } else {
        
    }

    true && true

    true || false
    randint(0, 10)
})
```
