### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Iron ores in tunels

```python
```

## Step 1
Part5
На команду в чате, Адент должен двигаться пока не достигнет конца шахты. Если перед ним **IRON_ORE**, то разрушаем блок и забираем руду с собой.
Необходимо повторить для каждой из шахт. Агента можно перемещать с помощью свистка.

```ghost
```python
def on_chat():
    while not agent.detect(AgentDetection.BLOCK, FORWARD):
        agent.move(FORWARD, 1)
    if agent.inspect(AgentInspection.BLOCK, FORWARD) == IRON_ORE:
        agent.destroy(FORWARD)
        agent.collect_all()
player.on_chat("run", on_chat)

```

