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
    return result;
}
string res = Method4(10, "a ");
Console.WriteLine(res);
```
# Цикл в цикле
* Пример
```csharp
for (int i = 2; i <=10; i++)
{
    for (int j = 2; j <= 10; j++)
    {
         Console.WriteLine($"{i} x {j} = {i * j}");
    }
    Console.Writeline();
}
```

* _Пример Цикла в цикле и применение метода_
```csharp
//Лекция. Задача 1: Дан текст. В тексте нужно все пробелы заменить черточками,
// маленькие буквы "к" заменить большими "К",
// а большие "С" заменить маленькими "с".

Console.Clear();
string text =
    "- Я думаю, - сказал князь, улыбаясь, - что, "
    + "ежели бы вас послали вместо нашего милого Винценгероде,"
    + "вы бы взяли приступом согласие прусского короля. "
    + "Вы так красноречивы. Вы дадите мне чаю?";

// string s = "qwerty"
//             112345
// simbol[3] // r

string Replace(string text, char oldValue, char newValue)
{
    string result = String.Empty;

    int length = text.Length;
    for (int i = 0; i < length; i++)
    {
        if (text[i] == oldValue)
            result = result + $"{newValue}";
        else
            result = result + $"{text[i]}";
    }
    return result;
}

string newText = Replace(text, ' ', '|');
Console.WriteLine(newText);
Console.WriteLine();

newText = Replace(newText, 'к', 'К');
Console.WriteLine(newText);
Console.WriteLine();

newText = Replace(newText, 'с', 'С');
Console.WriteLine(newText);
```
* _Пример№2 Цикла в цикле и применение метода_
```csharp
Console.Clear();
int[] arr = { 1, 5, 4, 3, 2, 6, 7, 1, 1 };

void PrintArray(int[] array)
{
    int count = array.Length;

    for (int i = 0; i < count; i++)
    {
        Console.Write($"{array[i]} ");
    }
    Console.WriteLine();
}

void SelectionSort(int[] array)
{
    for (int i = 0; i < array.Length - 1; i++)
    {
        int minPosition = i;
        for (int j = i + 1; j < array.Length; j++)
        {
            if (array[j] < array[minPosition])
                minPosition = j;
        }
        int temporary = array[i];
        array[i] = array[minPosition];
        array[minPosition] = temporary;
    }
}
PrintArray(arr);
SelectionSort(arr);
PrintArray(arr);
```
# Двумерные массивы
```csharp
Console.Clear();

string [,] table = new string[2, 5];
//String.Empty
//table[0, 0] table[0, 1] table[0, 2] table[0, 3] table[0, 4]
//table[1, 0] table[1, 1] table[1, 2] table[1, 3] table[1, 4]


table[1, 2] ="word";
for(int rows = 0; rows < 2; rows++)
{
    for(int columns = 0; columns < 5; columns++)
    {
        Console.WriteLine($"-{table[rows, columns]}-");
    }
}



void PrintArray(int[,] matr)/*создает массив*/
{ //GetLength(0) - считает количество строк
    for (int rows = 0; rows < matr.GetLength(0); rows++)
    {
        //GetLength(1) - считает количество столбцов
        for (int columns = 0; columns < matr.GetLength(1); columns++)
        {
            Console.Write($"{matr[rows, columns]} ");
        }
        Console.WriteLine();
    }
}

void FillArray(int[,] matr)/* заполняет двумерный массив*/
{
    for (int rows = 0; rows < matr.GetLength(0); rows++)
    {
        for (int columns = 0; columns < matr.GetLength(1); columns++)
        {
            matr[rows, columns] = new Random().Next(1, 10);
        }
    }
}

int[,] matrix = new int[3, 4];
Console.WriteLine();
FillArray(matrix);
PrintArray(matrix);
```

# Рекурсия
* Функция которая вызывает сама себя
```csharp
Console.Clear();

double Factorial(int n)
{
    if (n == 1)
        return 1;
    else
        return n * Factorial(n - 1);
}
for (int i = 1; i < 40; i++)
{
    Console.WriteLine($"{i}! = {Factorial(i)}");
}

f(1) = 1
f(2) = 1
f(n) = f(n-1) + f(n-2)

int Fibonacci(int n)
{
    if (n == 1 || n == 2)
        return 1;
    else
        return Fibonacci(n - 1) + Fibonacci(n - 2);
}
for (int i = 1; i < 45; i++)
{
    Console.WriteLine($"f({i}) = {Fibonacci(i)}");
}
Console.WriteLine();
```
