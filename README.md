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

Задание №2  
Дано слово из маленьких латинских букв. Сколько там согласных и гласных
букв? Гласными называют буквы «a», «e», «i», «o», «u».
Для решения задачи создайте переменную и в неё положите слово с
помощью input()
А также определите количество каждой из этих гласных букв Если какой-то из
перечисленных букв нет - Выведите False  
Решение:  

Задание №3  
Два инвестора - Майкл и Иван хотят вложиться в стартап. Фаундеры сказали,
что минимальная сумма инвестиций - X долларов, больше инвестировать
можно сколько угодно. У Майкла A долларов, у Ивана B долларов. Если оба
могут вложиться - выведите 2, если только Майкл - Mike, если только Иван -
Ivan, если не могут по отдельности, но вместе им хватает - 1, если никто - 0.  





 

