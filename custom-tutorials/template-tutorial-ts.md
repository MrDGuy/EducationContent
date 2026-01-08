### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @flyoutOnly 0
### @explicitHints 0
### @diffs true

# Template Tutorial

## Code Your Project
Code an ``||agent:agent||`` and move and build with the agent. 
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
    player.say(agent.getOrientation())
    blocks.place(GRASS, pos(0, 0, 0))
    blocks.fill(
    GRASS,
    posLocal(0, 0, 0),
    world(0, 0, 0),
    FillOperation.Replace
    )
    blocks.fill(
    GRASS,
    agent.getPosition(),
    pos(0, 0, 0),
    FillOperation.Replace
    )
    mobs.spawn(mobs.monster(ZOMBIE), positions.add(
    randpos(
    pos(0, 0, 0),
    pos(0, 0, 0)
    ),
    pos(0, 0, 0)
    ))
    agent.teleportToPlayer()
    agent.move(FORWARD, 1)
    agent.place(FORWARD)
    agent.interact(FORWARD)
    agent.destroy(FORWARD)
    agent.till(FORWARD)
    agent.collectAll()
    agent.collect(IRON_SHOVEL)
    player.say(agent.inspectBlock(FORWARD))
    agent.setSlot(1)
    agent.setItem(GRASS, 1, 1)
    player.say(agent.getItemCount(1))
    player.say(agent.getItemDetail(1))
    for (let index = 0; index < 5; index++) {
    	
    }
    while (true) {
    	break;
    }
    agent.turn(LEFT_TURN)
    loops.pause(100)
    if (agent.detect(AgentDetection.Block, FORWARD)) {
    	
    }
    if (agent.detect(AgentDetection.Block, FORWARD) && (!(agent.detect(AgentDetection.Block, FORWARD)) || agent.detect(AgentDetection.Block, FORWARD))) {
    	
    } else {
    	
    }
})
```
