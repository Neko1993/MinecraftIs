### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# Check blocks

```python
```

## Step 1
Напиши функцию - обработчик сообщения **bridge**. Используй цикл **for** для постройки моста шириной в один блок.

Материалы уже выданы агенту


```ghost
```python
def bridge(n):
    for i in range(n):
        agent.move(FORWARD, 1)
        agent.place(DOWN)

player.on_chat("bridge", bridge)
```

