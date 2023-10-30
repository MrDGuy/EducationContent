## @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @flyoutOnly 1
### @explicitHints 1
### @diffs true

# House Functions: Python

## Step 1
Code a ``||functions:function||`` and name it **walls**. 

```python
def walls():
    pass
```

## Step 2
Within the **walls** function, code the agent to ``||agent:set block or item||`` and set it to **Acacia Wood Planks** at a count of **64** in slot **1**.

```python
def walls():
    agent.set_item(PLANKS_ACACIA, 64, 1)
```

## Step 3
Within the **walls** function, code a ``||loops:for||`` loop that repeats **3** times an ``||agent:agent move||`` **up by 1** .

```python
def walls():
    agent.set_item(PLANKS_ACACIA, 64, 1)
    for index in range(3):
        agent.move(UP, 1)
```

## Step 4
Code another ``||loops:for||`` loop that repeats **4** times, and drag it inside the first ``||loops:for||`` loop — beneath the first ``||agent:agent move||``. 

```python
def walls():
    agent.set_item(PLANKS_ACACIA, 64, 1)
    for i in range(3):
        agent.move(UP, 1)
        for j in range(4):
            pass
```

## Step 5
Code a third ``||loops:for||`` loop, drag it inside the second ``||loops:repeat||`` loop and place it above the ``||agent: agent turn right||``. Set the third ``||loops:for||`` loop to repeat **4** times. Within the innermost ``||loops:for||`` loop, code the agent to ``||agent:place||`` and set it to **down**. Add an agent ``||agent:move||``, set it to **forward by 1**, and drag it inside the innermost ``||loops:for||`` loop under the ``||agent:place||`` down.

```python
def walls():
    agent.set_item(PLANKS_ACACIA, 64, 1)
    for i in range(3):
        agent.move(UP, 1)
        for j in range(4):
            for k in range(4):
                agent.place(DOWN)
                agent.move(FORWARD, 1)
            
```

## Step 6
With the second loop but outside the third loop (tabbed 3 times), code an ``||agent:agent turn right||``.

```python
def walls():
    agent.set_item(PLANKS_ACACIA, 64, 1)
    for i in range(3):
        agent.move(UP, 1)
        for j in range(4):
            for k in range(4):
                agent.place(DOWN)
                agent.move(FORWARD, 1)
            agent.turn(RIGHT_TURN)
```

## Step 7
Code a new ``||advanced:function||`` and name it **roof**.   

```python
def roof():
    pass
```

## Step 8
Code the agent to ``||agent:set block or item||``, set it to **brick slab**, set the count to **64** and the slot to **1** and drag it into the **roof** ``||functions:function||``. Also, code the agent to ``||agent:move||`` **up by 1**.

```python
def roof():
    agent.set_item(BRICKS_SLAB, 64, 1)
    agent.move(UP, 1)
```

## Step 9
Inside the **roof** ``||functions:function||``, code a ``||loops:for||`` loop and set it to repeat **5** times. 
	
```python
def roof():
    agent.set_item(BRICKS_SLAB, 64, 1)
    agent.move(UP, 1)
    for m in range(5):
        pass
```

## Step 10
Code another ``||loops:for||`` loop and set it to repeat **5** times. Within this loop, add a ``||agent:place down||``, followed by an ``||agent:agent move||`` **forward by 1**. Place this ``||loops:for||`` loop inside the previous loop—above the ``||agent:agent move||`` **back by 5**.

```python
def roof():
    agent.set_item(BRICKS_SLAB, 64 1)
    agent.move(UP, 1)
    for m in range(5):
        for n in range(5):
            agent.place(DOWN)
            agent.move(FORWARD, 1)
        
```

## Step 11
Within the first loop (tabbed twice), code the agent to ``||agent:move||`` **back by 5**, and then code the agent to ``||agent:move||``  **right by 1**.

```python
def roof():
    agent.set_item(BRICKS_SLAB, 64 1)
    agent.move(UP, 1)
    for m in range(5):
        for n in range(5):
            agent.place(DOWN)
            agent.move(FORWARD, 1)
        agent.move(BACK, 5)
        agent.move(RIGHT, 1)
```

## Step 12
Code an ``||player:on chat||`` command and name it **house**.  First drag in an ``||agent:teleport to player||`` code and then have it call both the **walls** and **roof** ``||functions:functions||``.

```python
def on_chat():
    agent.teleport_to_player()
    walls()
    roof()
player.on_chat("house", on_chat)
```


## Step 11
Go into Minecraft and test out the **house** command.

```python
def walls():
    agent.set_item(PLANKS_ACACIA, 64, 1)
    for i in range(3):
        agent.move(UP, 1)
        for j in range(4):
            for k in range(4):
                agent.place(DOWN)
                agent.move(FORWARD, 1)
            agent.turn(RIGHT_TURN)
def roof():
    agent.set_item(BRICKS_SLAB, 64, 1)
    agent.move(UP, 1)
    for m in range(5):
        for n in range(5):
            agent.place(DOWN)
            agent.move(FORWARD, 1)
        agent.move(BACK, 5)
        agent.move(RIGHT, 1)
def on_chat():
    agent.teleport_to_player()
    walls()
    roof()
player.on_chat("house", on_chat)
```
