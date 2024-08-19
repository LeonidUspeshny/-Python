# Университет Синергия Домашние задания по предмету Программирование на языке Python
Домашние задания 
# Урок №3. Ввод-вывод и базовые переменные  
 Задание №1  
   
 Давай представим, что мы пишем бэкенд для сайта ветеринарной клиники.
 Нам нужно написать программу, которая будет запрашивать у пользователя
 вид питомца, его возраст и кличку, а потом выведет все эти данные в одно
 предложение. Например:
 Это желторотый питон по кличке "Каа". Возраст: 34 года  
 РЕШЕНИЕ:  
 a = input("Вид питомца: ")  
 b = input("Возраст питомца: ")  
 c = input("Кличка питомца: ")  
 print("Это" , a, "по кличке ",c,"." "Восраст: ",b ,"года" )
   
 Задание №2 
   
А теперь мы с тобой напишем форму ввода ответа на тест по биологии для
студентов. Он должен запрашивать по порядку этапы развития человека
(проверим твое умение гуглить, что тоже очень важно для программиста. ) и в
конце вывести все стадии, разделенные знаком =>, что будет означать
постепенный переход от одного к другому. В следующих уроках мы дополним
эту форму до полноценного теста, который будет проверять правильность
ответов, а пока - начнем с малого. Напоминаем, что разделить эти данные
тебе поможет команда sep внутри команды print, например, чтобы разделить
переменные знаком + нужно ввести:
print(a1, a2, a3, sep='+')
Подсказка: последняя стадия развития - Homo sapiens sapiens.      
РЕШЕНИЕ:  
print("Учеными доказано, что существует 5 этапов развития человека")  
a = input("Введите первый этап развития: ")  
b = input("Введите второй этап развития: ")  
c = input("Введите третий этап развития: ")  
d = input("Введите четвертый этап развития: ")  
e = input("Введите пятый этап развития: ")  
print(a, b, c, d, e, sep='=>') 
  
# Урок №4. float, int и арифметические операции  
Задание №1  
Пользователь вводит стороны прямоугольника, выведите его площадь и
периметр. На вход программе могут подаваться как целые числа, так и
вещественные   
РЕШЕНИЕ:   
a = float(input("Введите длину стороны A: "))  
b = float(input("Введите длину стороны B: "))  
area = a * b  
perimeter = 2 * (a + b)  
print("Площадь прямоугольника:", area)  
print("Периметр прямоугольника:", perimeter) 

Задание №2  
Дано пятизначное целое число. Напишите алгоритм, который возведёт
количество десятков в степень количества единиц. Затем умножит это число
на количество сотен. И делит получившееся число на разность количества
десятков тысяч и количества тысяч
Например, есть число 46275
Необходимо возвести 7 (десятки) в степень 5 (единицы), умножить
получившееся число на 2 (сотни), и разделить на разность между 4 (десятки
тысяч) и 6 (тысячи) то есть (4-6)
В результате необходимо получить вещественное число. В нашем примере это
будет: -16807.0  
РЕШЕНИЕ:  
a = 46275  
a1 = 46275 % 10 # получаем остаток от деления (5)  
a2 = 46275 % 100 # получаем десяток от деления (75)  
a2 = a2 // 10 # делим десяток без остатка (7)  
c = a2 ** a1 # возводим 7 в степень 5  
d = a // 10000 # выделяем десятки тысяч (4)  
f = a // 1000 # получаем 46  
f = f % 10 # выделяем тысячи (6)  
a3 = a % 1000  
a3 = a3 // 100 # выделяем сотни  
b = c * a3 # умножаем предыдущий результат на кол-во сотен (2)  
b1 = b / (d - f)  
print("Дано число 46275")  
print("Единицы: ", a1)  
print("Десятки: ", a2)  
print("Десятки в степени едениц: ",c )  
print("Умножаем предыдущий результат на кол-во сотен: ",b)  
print("Делим результат на разность между 4 и 6 ", b1) 

# Урок №5. Логические и условные операторы  
Задание №1  
Пользователь вводит целое число. Выведите его строку-описание вида
"отрицательное четное число", "нулевое число", "положительное нечетное число",
например, численным описанием числа 190 является строка "положительное
четное число". Если число не является четным - выведите сообщение "число не
является четным"  
Решение:  
a = int(input("Введите целое число: "))  
if a > 0 and a % 2 == 0:  
    print("Положительное четное число")  
elif a < 0 and a % 2 == 0:  
    print("Отрицательное четное число")    
elif a > 0 and not a % 2 == 0:  
    print("Положительное нечетное число")   
elif a < 0 and not a % 2 == 0:  
    print("Отрицательное нечетное число")   
else:  
    print("нулевое число ")  
    
Задание №2  
Дано слово из маленьких латинских букв. Сколько там согласных и гласных
букв? Гласными называют буквы «a», «e», «i», «o», «u».
Для решения задачи создайте переменную и в неё положите слово с
помощью input()
А также определите количество каждой из этих гласных букв Если какой-то из
перечисленных букв нет - Выведите False  
Решение:   
word = input("Введите любое слово на латинском языке маленькими буквами: ")  
list = ['a','o','i','u','e']  
glas = 0  
sogl = 0  
for i in range(len(word)):  
    if word[i] in list:  
        glas += 1          
    else:  
        sogl += 1      
print("Количество гласных букв: ", glas)  
print("Количество согласных: ", sogl)  

Задание №3  
Два инвестора - Майкл и Иван хотят вложиться в стартап. Фаундеры сказали,
что минимальная сумма инвестиций - X долларов, больше инвестировать
можно сколько угодно. У Майкла A долларов, у Ивана B долларов. Если оба
могут вложиться - выведите 2, если только Майкл - Mike, если только Иван -
Ivan, если не могут по отдельности, но вместе им хватает - 1, если никто - 0.  
Решение:  
maikl = int(input("Сколько долларов у Майкла ? "))  
ivan = int(input("Сколько долларов у Ивана ? "))  
x = 1000 # минимальная сумма для инвестиция  
if x <= maikl and x > ivan:  
    print("Вложиться может только Майкл")  
if x <= ivan and x > maikl:  
    print("Вложиться может только Иван")  
if x > maikl and x > ivan and x <= (maikl + ivan):  
    print("Можете вложиться только вместе")  
if x <= maikl and x <= ivan:  
    print("С деньгами у вас все впорядке, вкладывайтесь )")  
print("Удачи в этой пирамиде ))") 

# Урок No6. Циклы while и for  
Задание №1  
Сначала вводится число N, затем вводится ровно N целых чисел. Подсчитайте,
сколько из них равны нулю, и выведите это количество  
Решение:  
a  = int(input("Введите чило "))  
count = 0  
for i in range(a):  
    num = int(input("Введите  чиcло "))  
    if num == 0:  
        count += 1  
print("Количество раз ты ввел ноль: ",count)  

Задание No2  
Вводится натуральное число X. Подсчитайте количество натуральных делителей числаX 
(включая 1 и само число). x≤2e9 (2миллиарда) 
Решение:  
x = int(input("Введите число X: "))  
if x == 1:  
    d = 1  
else:  
    d = 2  
    for i in range(2, int((x/2) + 1)):  
        if x % i == 0:  
            d += 1  
print(d)  

Задание №3  
Вводятся целые числа A и B. Гарантируется, что A ≤ B. Выведите все четные
числа на заданном отрезке через пробел 
Решение:  
a = int( input("Enter a: ") )  
b = int( input("Enter b: ") ) + 1  
[ print(num, end = " ") for num in range(a,b) if a < b and num % 2 == 0]  

# Урок No7. Строки  

Задание №1  
На вход подается 1 строка без пробелов. По данной строке определите,
является ли она палиндромом (то есть, можно ли прочесть ее наоборот, как,
например, слово "шалаш"). Необходимо вывести ”yes”, если строка является
палиндромом, и “no” в противном случае.  
Решение: 
str = input()  
if str == str[::-1]:  
   print('yes')  
else:  
   print("no")  

Задание №2  
Дана строка, длина которой не превосходит 1000. Вам требуется
преобразовать все идущие подряд пробелы в один. Выведите измененную
строку.  
Решение:  
text = input()  
print(' '.join(text.split()))  

# Урок No8. Списки

Задание № 1
Впервой строке вводится число N.Далее в N строк вводится N чисел (1≤N≤
10000),по одному числу на строке.Все числа помодулю не превышают 10e5
Переверните массив чисел. Выведите N чисел - перевернутый массив  
Решение:  
n = int(input("Ведите колличество чисел: "))  
list = []  
for i in range(n):  
    a = int(input("Введите значение болше 1, и меньше 10000: " ))  
    if a>=1 and a<=10000:  
        list.append(a)         
    else:  
        print('Введите другое значение')   
print(list)  
print(list[::-1])  

Задание № 2  

Впервую строчку вводится число N (1≤N≤100000). Вследующую строку через пробел вводятся N чисел (1≤Ai≤10e9). 
Вам требуется написать метод, который получает на вход массив и изменяет его таким образом, чтобы на первом 
месте стоял последний элемент, на втором - первый, на третьем - второй и т.д. Выведите N чисел - измененный массив  
Решение:  
n = int(input("Ведите колличество чисел >=1 и <=1000000 "))  
list = []  
for i in range(n):  
    a = int(input("Введите значение болше 1, и меньше 10000: " ))  
    if a >=1 and a <=100000:          
        list.append(a)  
    else:  
        print("Введите верное число")   
a = list.pop(-1)     
list.insert(0, a)  
print(list)  

Задание No3  
На берегу реки стояли n рыбаков, все они хотели перебраться на другой берег. Одна лодка может выдержать неболее m килограмм, 
при этом в лодку помещается неболее 2 человек. Определите, какое минимальное число лодок нужно, чтобы перевезти на другой 
берег всех рыбаков Впервую строку вводится число m (1≤m≤10e6) -максимальная масса, которую может выдержать одналодка. 
Во вторую строку вводится число n (1≤n≤100) -количество рыбаков. Вследующие N строк вводится по одному числу Ai (1≤Ai≤m)
-вес каждого путешественника. Программа должна вывести одно число - минимальное количество лодок, необходимое для 
переправки всех рыбаков на противоположный берег.  
Решение:  
m = int(input("Максимальная масса, которую может выдержать баркас: "))  
n = int(input("Колличество рыбаков стоящих на берегу реки: "))  
mass = []  
for i in range(n) :  
    i = int(input("Введите массу рыбака: "))  
    if m > i:  
        mass.append(i)  
    else:    
        print("Извини братан, лодка с тобой потонет")  
mass.sort()   
left = 0   
right = len(mass) - 1    
boat = 0    
while left <= right:  
    if mass[left] + mass[right] <= m:  
        left +=1       
    right -= 1  
    boat += 1   
print(f'Колличетво лодок которые понадобятся: {boat}')  

# Урок №9. Множества

Задание №1  
В первую строку вводится число N – количество чисел (1 ≤ N ≤ 100000). Во
вторую строку вводится через пробел N чисел, каждое не превышает 2*10e9
по модулю. Требуется выяснить, сколько среди этих чисел различных.
Выведите число, равное количеству различных чисел среди данных.  
Решение:  
N = int(input("Введите колличество чисел: "))  
numbers = list(map(int, input(f'Введите через пробел {N} чисел: ').split()))  
number_list = set(numbers)  
print(len(number_list))  

Задание №2  
Вводятся два списка чисел, которые могут содержать до 100000 чисел
каждый. Все числа каждого списка находятся на отдельной строке. Выведите,
сколько чисел содержится одновременно как в первом списке, так и во
втором.  
Решение:  
list1 = set(map(int, input('Введите через пробел числа (список 1): ').split()))  
list2 = set(map(int, input('Введите через пробел числа (список 2): ').split()))  
intersection = list1.intersection(list2)  
print(len(intersection))  
print(list1)  
print(list2)  

Задание №3  
Во входную строку вводится последовательность чисел через пробел. Для
каждого числа выведите слово ”YES” (в отдельной строке), если это число
ранее встречалось в последовательности или ”NO”, если не встречалось.  
Решение:  
list = input('Введите через пробел числа : ')  
numbers = map(int, list.split())  
seen = set()  
for number in numbers:  
    if number in seen:  
        print("YES")  
    else:  
        print("NO")  
        seen.add(number)  
        
# Урок №10. Словари

Задание №1  
Ранее вы выполняли задание связанное с ветеринарной клиникой. В той
задаче вам предстояло вывести информацию о питомце на экран. Сейчас вам
необходимо создать словарь pets = {}  
Решение:  
pets = dict()  
pet_name = input("Имя питомца: ")  
pet_view = input(f"Введите вид питомца {pet_name}: ")  
pet_age = int(input(f"Введите возраст питомца {pet_name}: "))  
pet_user = input(f"Введите владельца питомца {pet_name}: ")  
if pet_age % 10 == 1 and pet_age % 100 != 11:  
    suffix = "год"  
elif pet_age % 10 in [2, 3, 4] and not (pet_age % 100 in [12, 13, 14]):  
    suffix = "года"  
else:  
    suffix = "лет"  
pet_info = {  
    "Вид питомца ": pet_view,  
    "Возраст питомца ": f"{pet_age} {suffix}",  
    "Владелец питомца ": pet_user  
}  
pets[pet_name] = pet_info  
print(pets)  

Задание №2  
С помощью цикла создайте словарь, в котором ключи будут, например от
числа 10, до -5 (включительно). А значениями этих ключей будут сами эти
числа возведённые в степени равных этим числам  
Решение:  
result_dict = {}  
for key in range(10, -6, -1):  
    result_dict[key] = key ** key   
print(result_dict)  

# Доп задание:  
Создаем пустой словарь  
my_dict = {}  
Запрашиваем у пользователя 5 слов и их значения  
for i in range(5):  
    key = input(f"Введите слово {i + 1}: ")  
    value = input(f"Введите значение для слова '{key}': ")  
    my_dict[key] = value  
Выводим созданный словарь  
print("Созданный словарь:")  
print(my_dict) 

# Урок №11. Функции  
Задание №1  
● Создайте функцию, которая принимает в качестве параметра -
натуральное целое число.
● Данная функция находит факториал полученного числа
Например, факториал числа 3 это число 6.
● Теперь создайте список факториалов чисел от получившегося ранее
факториала 6, до 1.
В итоге, на вход программа получает например число 3, возвращает число 6
(факториал числа 3) и вам нужно сделать список из факториалов числа 6 в
убывающем порядке. Находим факториал числа 6 - это 720, затем от числа 5 -
это 120 и так далее вплоть до 1
То есть, результирующий список будет выглядеть в нашем примере так:
[720, 120, 24, 6, 2, 1]  
Решение:  
def factorial(n):  
    if n == 0 or n == 1:  
        return 1  
    else:  
        return n * factorial(n - 1)  

def factorials_list(n):  
    fact_n = factorial(n)  
    print(f"Факториал числа {n} равен: {fact_n}")  
    factorials = []  
    for i in range(fact_n, 0, -1):  
        factorials.append(factorial(i))  
    return factorials  

number = int(input('Введите число: '))  
result = factorials_list(number)  
print("Список факториалов от", factorial(number), "до 1:", result)  

Задание №2  
В Урок №10. Задание №1 вы создавали словарь с информацией о питомце.
Теперь нам нужна "настоящая" база данных для ветеринарной клиники.
Подробный требуемый функционал будет ниже. Пока что справка:
● Создайте функцию create
● Создайте функцию read
● Создайте функцию update
● Создайте функцию delete
● Используйте словарь pets, который будет предоставлен ниже, либо
создайте свой аналогичный  
Решение: 
import collections  
pets = dict()  

def pets_list(id):  
    print("Список питомцев")  
    print("---------------")  
    for pet in pets:  
        print(f'Имя: {pets[id]['имя']}, Вид: {pets[id]["вид"]}, Возраст: {suffix(pets[id]["возраст"])}')  
    
def create():  
    print('Введите информацию о питомце')  
    name = input('Введите имя питомца: ')  
    species = input('Введите вид питомца: ')  
    age = int(input('Введите возраст питомца: '))  
    owner_name = input('Введите владельца питомца: ')  
    if pets:  
        last_id = collections.deque(pets.keys(), maxlen=1)[0]  
        new_id = last_id + 1  
    else:  
        new_id = 1  
    pets[new_id] = {'имя': name, 'вид': species, 'возраст': age, 'владелец': owner_name}  

def suffix(age):  
    if 11 <= age % 100 <= 14:  
        return f"{age} лет"  
    elif age % 10 == 1:  
        return f"{age} год"  
    elif age % 10 in [2, 3, 4]:  
        return f"{age} года"  
    else:  
        return f"{age} лет"  

def delete(pet_id):  
    if pet_id in pets:  
        del pets[pet_id]  
        print(f"Питомец с идентификатором {pet_id} удален.")  
    else:  
        print("Питомец с таким идентификатором не найден.")  

def update(pet_id, name=None, species=None, age=None):  
    pet = pets.get(pet_id) 
    if pet:  
        if name:  
            pet['name'] = name  
        if species:  
            pet['species'] = species  
        if age is not None:  
            pet['age'] = age  
        print(f"Информация о питомце с ID {pet_id} обновлена.")  
    else:  
        print(f"Питомец с ID {pet_id} не найден.")  

def pets_id(pet_id):  
    if pet_id in pets:  
        print(pets[pet_id])  
    else:  
        print(False)  

while True:  
    command = input("Введите команду (или 'stop' для выхода) : ")  
    if command.lower() == 'stop':  
        print("Команда 'stop' получена. Завершение программы.")  
        break  

    if command == 'create':  
        create()  
    elif command == 'read':  
        a = int(input("Введите ID питомца: "))  
        print(pets_list(a))  
    if command == 'delete':  
        b = int(input("Введите ID питомца: "))  
        delete(b)  
    if command == 'update':  
        c = int(input("Введите ID питомца: "))  
        name = input('Введите имя питомца: ')  
        species = input('Введите вид питомца: ')  
        age = int(input('Введите возраст питомца: '))  
        update(c, name, species, age)  

# Урок №13. Двумерные списки  

Задание №1  
С помощью цикла создайте матрицу вида 10x10  
И нужно придумать, как их сложить, чтобы получить matrix_3:  
import random  
matrix_1 = [[random.randint(-50, 200) for _ in range(10)] for _ in range(10)]  
matrix_2 = [[random.randint(-50, 200) for _ in range(10)] for _ in range(10)]  
print('matrix_1')  
for row1 in matrix_1:  
    print(*row1)  
print('matrix_2')    
for row2 in matrix_2:  
    print(*row2)  


























 

