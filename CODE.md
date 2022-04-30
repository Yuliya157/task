# Задача 5 из первого блока задач
Написать рекурсивную функцию для расчета степени n вещественного числа a (n — натуральное число).
Рекурсия – это вызов функцией самой себя. 
```python
def power(base, exp):
    if (exp == 1):
        return (base)
    if (exp != 1):
        return (base * power(base, exp - 1))
base = int(input("Введите число: "))
exp = int(input("Введите степень: "))
print("Результат равен:", power(base, exp))
```

# Задача 1 из второго блокам задач
Вывод виде таблицы ФИО и даты рождения всех студентов группы
```python
import pandas as pd
surname_n = []
name_n = []
birt_t = []
ex_n = []
date_n = []
teacher_n = []
all_l = []
n = int(input("Введите количество студентов: "))
while n<0:
    print("Повторите ввод")
    n = int(input("Введите количество студентов еще раз: "))
for i in range(n):
    surname = input("Введите фамилию: ")
    name = input("Введите имя: ")
    year = int(input("Введите год рождения: "))
    month = input("Введите месяц рождения: ")
    ch = int(input("Введите дату рождения: "))
    birt = str(year)+'.'+month+'.'+str(ch)
    birt_t.append(birt)
    surname_n.append(surname)
    name_n.append(name)
    ex = int(input("Введите количество экзаменов: "))
    while ex<3 or ex>5:
        ex = int(input("Введите количество экзаменов от трех до пяти: "))
    for i in range(ex):
        ex1 = input("Введите экзамен: ")
        ex_n.append(ex)
        date = input("Введите дату экзамена: ")
        date_n.append(date)
        teach = input("Введите преподавателя: ")
        teacher_n.append(teach)
all_l.append(surname_n)
all_l.append(name_n)
all_l.append(birt_t)
index = ['Фамилия', 'Имя', 'День рождения']
df = pd.DataFrame(all_l, index) 
print(df)
```
