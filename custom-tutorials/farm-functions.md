### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false
### @flyoutOnly 1
### @explicitHints 1
### @diffs true

# Farm: Python

## Step 1
Write a function called **plant_row** which takes two parameters: **distance** and **vegetable**
```python
def plant_row(distance, vegetable):
    agent.set_item(vegetable, 64, 1)
    for index2 in range(distance):
        agent.till(FORWARD)
        agent.move(FORWARD, 1)
        agent.place(DOWN)
    agent.move(BACK, distance)
    agent.move(RIGHT, 2)
```

## Step 2
Beneath the plant_row function, code an ``||player: on chat||`` command and name it **farm**. Code the agent ``||agent:to teleport to player||``. 

```python
def on_chat(num_rows):
    agent.teleport_to_player()
player.on_chat("farm", on_chat)
```

## Step 3
Beneath the plant_row function, code an ``||player: on chat||`` command and name it **farm**. Call the **plant_row** function with a distance and a crop. 

```python
def on_chat(num_rows):
    agent.teleport_to_player()
    for index in range(num_rows):
        plant_row(8, CARROTS)
player.on_chat("farm", on_chat)
```

## Step 4
Beneath the plant_row function, code an ``||player: on chat||`` command and name it **farm**. Call the **plant_row** function two more times with a distance and a crop. 

```python
def on_chat(num_rows):
    agent.teleport_to_player()
    for index in range(num_rows):
        plant_row(8, CARROTS)
    for index in range(num_rows):
        plant_row(8, PUMPKIN_SEEDS)
    for index in range(num_rows):
        plant_row(8, BEETROOT_SEEDS)
player.on_chat("farm", on_chat)
```

## Step 5
Complete code:

```python
def plant_row(distance, vegetable):
    agent.set_item(vegetable, 64, 1)
    for index2 in range(distance):
        agent.till(FORWARD)
        agent.move(FORWARD, 1)
        agent.place(DOWN)
    agent.move(BACK, distance)
    agent.move(RIGHT, 2)

def on_chat(num_rows):
    agent.teleport_to_player()
    for index in range(num_rows):
        plant_row(8, CARROTS)
    for index in range(num_rows):
        plant_row(8, PUMPKIN_SEEDS)
    for index in range(num_rows):
        plant_row(8, BEETROOT_SEEDS)
player.on_chat("farm", on_chat)
```
