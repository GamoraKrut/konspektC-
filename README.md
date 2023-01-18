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

void - метод который ничего не возвращает

```csharp
//Ex 1:
void Method1()
{
    Console.WriteLine(@"Author ...");
}
Method1();
//Ex 2:
void Method2(string msg, int count)
{
    int i=0;
    while (i < count)
       {
       Console.WriteLine(msg);
       i++;
       }
}
Method2("Text", 4);
//Ex 3:
void Method2(string msg, int count)
{
    int i=0;
    while (i < count)
       {
       Console.WriteLine(msg);
       i++;
       }
}
//Method2(msg: "Text", count: 4);
Method2(count: 4, msg: "New text");

int Method3()
{
    return DateTime.Now.Year;
}

int year = Method3();
Console.WriteLine(year);

string Method4(int count, string text)
{
    int i = 0;
string result = String.Empty; //тоже самое что string result = "";

    While(i < count)
    {
        result = result + text;
        i++;
    }
    return result
}
string res = Method4(10, "abc");
Console.WriteLine(res);
```

# Цикл for
* Пример
```csharp
string Method4(int count, string text)
{
    string result = String.Empty; //тоже самое что string result = "";
    for(int i = 0; i < count; i++)
    {
        result = result + text;
    }
    return result
}
string res = Method4(10, "a ");
Console.WriteLine(res);
```
