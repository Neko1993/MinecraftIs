### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# Check blocks

```python
```

## Step 1
Part2

## Step 2
Напиши функцию **check_ground_stable** в которой, агент пробует сломать блок под собой. Если у него выходит(проверьте командой **agent.detect**), выведите в чат **Unstable**.

## Step 3
При команде в чате **check** двигайтесь вперед и проверяйте блоки на стабильность.

```ghost
```python
def check_ground_stable():
    agent.destroy(DOWN)
    if not agent.detect(AgentDetection.BLOCK, DOWN):
        player.say('Unstable')

def on_chat():
    for i in range(4):
        check_ground_stable()
        agent.move(FORWARD, 1)
player.on_chat("check", on_chat)
```

