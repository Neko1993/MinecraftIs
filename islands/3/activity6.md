### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# Iron

```python
```

## Step 1
Засади грядку с пшеницей. Над каждым участком проверяй, есть ли на нем **WHEAD** старая пшеница, если есть выведи в чат **WHEAD** и уничтож ее, если под тобой воздух, то просто выведи в чат **AIR**.

```ghost
```python
def plant(length):
    for i in range(length):
        agent.move(FORWARD, 1)
        block = agent.inspect(AgentInspection.BLOCK, DOWN)
        if block == WHEAT:
            agent.destroy(DOWN)
            agent.place(DOWN)
            player.say('WHEAT')
        elif block == AIR:
            agent.place(DOWN)
            player.say('AIR')
   

def done(length, width):
    for i in range(width):
        plant(length)
        agent.move(BACK, length)
        agent.move(LEFT, 1)

player.on_chat("plant", done)
```