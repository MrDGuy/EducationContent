### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 0
### @hideDone false

# Cattle

## Step 1
Look at the starter code and try running it. This code allows you to navigate the Agent without counting blocks. Look at the path the Agent needs to take and make sure you finish the coding sequence with correct turns for the Agent. Make sure that the Agent can reach the **gold plate**.  
```blocks
player.onChat("sheep", function () {
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.move(FORWARD, 1)
    }
    agent.turn(LEFT_TURN)
})

``` 

```template
player.onChat("sheep", function () {
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.move(FORWARD, 1)
    }
    agent.turn(LEFT_TURN)
})

``` 

