### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# Weather

```python
```

## Step 1
Напиши функцию **carpet_line**, которая принимает один аргумент - длину полосы. Используй цикл **for** для того, чтобы застелить одну полоску ковром. 

Материал уже выдан агенту


## Step 2
Напиши обработчик события чата на сообщение **carpet** принимающий 2 аргумента - длину и ширину ковра. Используя цикл **for** и вызывая функцию **carpet_line** выстели ковер.




```ghost
```python
def carpet_line(lenght):
    for i in range(lenght):
        agent.move(FORWARD, 1)
        agent.place(DOWN)

def carpet(length, width):
    for i in range(width):
        carpet_line(length)
        agent.move(BACK, length)
        agent.move(RIGHT, 1)

player.on_chat("carpet", carpet)
```

