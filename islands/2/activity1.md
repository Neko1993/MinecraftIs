### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Iron ores in tunels

```python
```

## Step 1
Создайте функцию **sum** принимающую 2 аргумента **a** и **b** и выводящую в чат сообщение вида **a + b = c**, где a и b - числа переданные как аргументы, а c - их сумма. Вызывайте эту функцию как обработчик сообщения **sum**

Для выполнения задания Вам понадобятся следующие команды:

- **str** - преобразование из числа в строку

- **+** - слияние двух строк


```ghost
```python
def sum(a, b):
    c = a+b
    player.say(str(a)+'+'+str(b)+'='+str(a+b))

player.on_chat('sum', sum)
```

