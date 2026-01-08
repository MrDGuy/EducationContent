### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 0
### @explicitHints 0
### @diffs false
### @hideDone true

## Your own creation!

Using the ``||agent:agent||``, ``||builder:builder||``, and the ``||blocks:blocks||`` categories, build a creation on your space.

```typescript
    player.onChat("run", function () {
    }
```

```ghost
let number = 0
player.onChat("run", function () {
    agent.teleportToPlayer()
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
    agent.teleport(pos(0, 0, 0), WEST)
    agent.setAssist(PLACE_ON_MOVE, false)
    agent.place(FORWARD)
    agent.destroy(FORWARD)
    agent.till(FORWARD)
    agent.collectAll()
    agent.collect(IRON_SHOVEL)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        for (let index = 0; index < 4; index++) {
            if (0 == 0) {
                blocks.place(GRASS, positions.add(
                pos(0, 0, 0),
                pos(0, 0, 0)
                ))
            } else if (true && blocks.testForBlock(GRASS, randpos(
            pos(0, 0, 0),
            pos(0, 0, 0)
            ))) {
                blocks.fill(
                GRASS,
                world(0, 0, 0),
                pos(0, 0, 0),
                FillOperation.Replace
                )
                blocks.cloneFiltered(
                pos(0, 0, 0),
                pos(0, 0, 0),
                pos(0, 0, 0),
                GRASS,
                CloneMode.Normal
                )
            } else if (positions.equals(
            world(0, 0, 0),
            world(0, 0, 0)
            ) || "" == "") {
                blocks.clone(
                pos(0, 0, 0),
                pos(0, 0, 0),
                pos(0, 0, 0),
                CloneMask.Replace,
                CloneMode.Normal
                )
            } else {
                number += 1
            }
        }
        number = 0 + 0
    }
    agent.setSlot(number)
    agent.setItem(IRON_SHOVEL, 1, 1)
    agent.dropAll(FORWARD)
    agent.drop(FORWARD, 1, 1)
    agent.transfer(1, 1, randint(0, 10))
    builder.move(FORWARD, 1)
    builder.turn(LEFT_TURN)
    builder.mark()
    builder.teleportTo(pos(0, 0, 0))
    builder.place(GRASS)
    builder.tracePath(GRASS)
    builder.shift(1, 1, 1)
    builder.fill(GRASS)
    builder.line(GRASS)
    builder.face(WEST)
    builder.setOrigin()
    builder.teleportToOrigin()
    builder.raiseWall(GRASS, 5)
    builder.copy()
    builder.paste()
    builder.popState()
    builder.pushState()
})


```
