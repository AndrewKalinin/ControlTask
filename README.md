# КОНТРОЛЬНАЯ РАБОТА 
## Задача 
Написать программу, которая из имеющегося массива строк формирует массив из строк, длина которых меньше либо равна 3 символа. Первоначальный массив можно ввести с клавиатуры, либо задать на старте выполнения алгоритма. При решении не рекомендуется пользоваться коллекциями, лучше обойтись исключительно массивами. 
## Примеры
["hello", "2", "world", ":-)"] -> ["2", ":-)"]
["1234", "1567", "-2", "computer science"] -> ["-2" ]
["Russia", "Denmark", "Kazan"] -> []
## Решение задачи
### *Блок-схема*
![Pictures](Diagram.jpg) 

### *Код задачи*
using System;
 
string[] array =
{
    "56",
    "A",
    "try",
    "good",
    "trust",
    "2"
};
 
var result = new string[array.Length];
var realSize = 0;
foreach (var value in array)
{
    if (value.Length <= 3)
    {
        result[realSize] = value;
        realSize++;
    }
}
 
Console.WriteLine(string.Join(Environment.NewLine, result, 0, realSize));

## *Результат решения задачи*
"56",
"A",
"try",
"2"
