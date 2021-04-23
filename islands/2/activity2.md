### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Variables

```python
```

## Step 1
Создайте функцию **sum** принимающую один аргумент **n**. Функция должна считать сумму первых n чисел(от 0 до n). Используйте цикл **for** и переменную **s** для решения. Функция должны возвращать(**return s**) полученную сумму. 
Вызовите функцию и выведете ответ в чат (**player.say(str(sum(10)))**) со следующими параметрами: 5, 10, 30.


```ghost
```python
def sum(n):
    s = 0
    for i in range(n+1):
        s += i
    return s
player.say(str(sum(10)))
```

