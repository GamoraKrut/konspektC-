# konspektC#

Console.ReadLine() - Команда ввода

Console.WriteLine() - Команда вывода

Console.Write() - Выводит в одну строку

int.Parse() - Возвращает преобразованное число

Convert.ToInt32() - Преобразует в число

Convet.ToString() - Преобразует в строку

+ в скобках используется вместо запятой

Double - дробные числа

bool - true/false

string - строка

% - нахождение остатка от деления

new Random().Next(min, max) - дает случайное число от min до max-1

string.ToLower() - делает все буквы строчными

№Синтаксис:

* условие;

* {

* набор действий
 
* }

Console.Clear() - очищает консоль терминала

# Функции в програмировании:

ВoзвращаемыйТипДанных ИмяМетода([ТипДанных1 ИмяАргумента1,...])

{

Тело Метода

return ЗначениеСоответствующееВозвращаемомуТипуДанных;

}

* Пример:

```сsharp
double f(double x)
{
double result = x * x + 1;
return result
}
```

* Пример массива:

```csharp
int[] array = {1, 2, 3, 4, 5, 6,};
```
array - метод для массива


```csharp
string name = "Artur";
int age = 24;
double height = 1.7;
Console.WriteLine($"Name: {name} Age: {age} Height: {heiht}");
```
На выводе будет:

*Name: Artur Age: 24 Height: 1.7*

