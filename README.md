# Домашнее задание к работе 6
## Условие задачи
32. Даны произвольные числа А, В, С. Если нельзя построить
треугольник с такими длинами сторон, то вывести «не треугольник», иначе
напечатать «равносторонний треугольник» или «равнобедренный» или какой
либо иной.

## 1. Алгоритм и блок-схема
### Алгоритм
1. **Начало**
2. ввод значений
3.Проверка
4. **Конец**
   
### Блок-схема
<img width="1282" height="922" alt="image" src="https://github.com/user-attachments/assets/b9d2b602-cac7-43f6-835b-5104811cf6d5" />


## 2. Реализация программы
#include <locale.h>
#include <stdio.h>
#define _CRT_SECURE_NO_WARNINGS
#include <stdlib.h>
#include <math.h>


int main()
{
    setlocale(LC_CTYPE, "RUS");
    int x, y, z;
    printf("ВВЕДИТЕ Х\n");
    scanf_s("%d", &x);
    printf("ВВЕДИТЕ Y\n");
    scanf_s("%d", &y);
    printf("ВВЕДИТЕ Z\n");
    scanf_s("%d", &z);
    if (x <= 0 || y <= 0 || z <= 0) {
        printf("не треугольник\n");
    }
    else if ((x + y <= z) || (x + z <= y) || (y + z <= x)) {
        printf("не треугольник\n");
    }
    else {
        if (x == y && y == z) {
            printf("равносторонний треугольник\n");
        }
        else if (x == y || x == z || y == z) {
            printf("равнобедренный треугольник\n");
        }
        else {
            printf("разносторонний треугольник\n");
        }

    }
}

## 3. Результаты работы программы
ВВЕДИТЕ Х
3
ВВЕДИТЕ Y
4
ВВЕДИТЕ Z
5
разносторонний треугольник

<img width="827" height="298" alt="image" src="https://github.com/user-attachments/assets/28911145-3504-4b5e-b0a4-6a91fbab1721" />
