### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# ladders

```python
```

## Step 1
Помоги Маркусу починить лестницу. Запасные части уже в инвентаре Агента.


```ghost
```python
def plantSeed(direction):
    agent.till(direction)
    agent.place(direction)

agent.move(LEFT, 3)
plantSeed(DOWN)
agent.move(RIGHT, 3)
agent.move(FORWARD, 1)
plantSeed(DOWN)
agent.move(RIGHT, 4)
agent.move(FORWARD, 1)
plantSeed(DOWN)
```

