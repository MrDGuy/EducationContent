### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @flyoutOnly 0
### @explicitHints 0
### @diffs true

# Template Tutorial

## Code Your Project
Move and build with an ``||agent:agent||`` or ``||blocks:block||`` code.
```typescript
player.onChat("run", function () {
	
})
```


```customts
player.onChat("reset", function() {
    let playerGround = positions.groundPosition(player.position())
    let x = playerGround.getValue(Axis.X);
    let y = 173;
    let z = playerGround.getValue(Axis.Z);
    blocks.fill(AIR, world(x - 32, y, z - 32), world(x + 32, y + 5, z + 32), FillOperation.Replace);
    blocks.fill(AIR, world(x - 32, y+6, z - 32), world(x+32, y+11, z+32), FillOperation.Replace);
    blocks.fill(AIR, world(x - 32, y + 12, z - 32), world(x + 32, y + 17, z + 32), FillOperation.Replace);
    blocks.fill(AIR, world(x - 32, y + 18, z - 32), world(x + 32, y + 23, z + 32), FillOperation.Replace);
    blocks.fill(GRASS, world(x - 32, y-1, z - 32), world(x + 32, y-1, z + 32), FillOperation.Replace);
    blocks.fill(DIRT, world(x - 32, y-2, z - 32), world(x + 32, y-5, z + 32), FillOperation.Replace);
    blocks.fill(STONE, world(x - 32, y - 6, z - 32), world(x + 32, y - 10, z + 32), FillOperation.Replace);
    blocks.fill(STONE, world(x - 32, y - 11, z - 32), world(x + 32, y - 15, z + 32), FillOperation.Replace);
})
```
```ghost
player.onChat("xyzabcdef", function (num1, num2) {
	let playerGround = positions.groundPosition(player.position())
    player.teleport(pos(0, 0, 0))
	let myPosition = player.position()
	let newPosition = positions.add(
    	pos(0, 0, 0),
    	pos(0, 0, 0)
    )
    myPosition.getValue(Axis.X);
    player.say(agent.getOrientation())
    blocks.place(GRASS, pos(0, 0, 0))
	let blockType = blocks.blockByName("IRON_SHOVEL");
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
	agent.teleport(pos(0, 0, 0), WEST)
    count = agent.getItemCount(1)
    agent.setAssist(PLACE_ON_MOVE, false)
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
    player.say(agent.getItemDetail(1))
    for (let index = 0; index < 5; index++) {
    	
    }
    while (true) {
    	break;
    }
    agent.turn(LEFT_TURN)
	agent.turnLeft()
	agent.turnRight()
	let x = randint(1,100);
	let y = randint(1,100);
	if(!x==5||y!==5&&x>50)
	{

	}
    loops.pause(100)
    if (agent.detect(AgentDetection.Block, FORWARD)) {
    	
    }
    if (agent.detect(AgentDetection.Block, FORWARD) && (!(agent.detect(AgentDetection.Block, FORWARD)) || agent.detect(AgentDetection.Block, FORWARD))) {
    	
    } else {
    	
    }
})
```
