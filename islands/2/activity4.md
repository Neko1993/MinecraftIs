### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Forest

```python
```

## Step 1
Помоги фермеру посадить семена. Они уже в инвентаре агента, так что можешь начинать писать код. Места посадки обозначены факелами. Постарайся решить задачу одним запуском кода.

Для обработки земли используй agent.till, а для посадки agent.place


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

