### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Apples for Marvin

```python
```

## Step 1
Собери яблоки для Марвина.
Для этого напиши код, выполняющийся на сообщение в чате **Apple**. Поднимайся вверх, пока не обнаружишь препятствие сверху. После этого сорви яблоко командой agent.destroy(). Собери 5 яблок таким образом.


```ghost
```python
def on_chat():
    while not agent.detect(AgentDetection.BLOCK, UP):
        agent.move(UP, 1)
    agent.destroy(UP)
player.on_chat("apple", on_chat)
```

