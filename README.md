# Домашнее задание к работе 18
## Условие задачи
Создать структуру для хранения указанной в индивидуальном
варианте записи, организовать в программе ввод 5-10 различных
записей, из полученного массива структур найти и напечатать
информацию согласно индивидуальному варианту:
Вариант 23. Запись «Сотрудник»:
Фамилия
Имя
Отчество
Должность
Пол
Дата приема на работу
Вывести все сведения о сотрудниках, стаж которых превышает
10 лет.
## 1. Алгоритм и блок-схема
### Алгоритм
# Алгоритм


### Блок-схема



## 2. Реализация программы
      #define _CRT_SECURE_NO_DEPRECATE 
      #include <stdio.h>
      #include <stdlib.h>
      #include <locale.h>
      
      typedef struct {
          int day;
          int month;
          int year;
      } Date;
      
      typedef struct {
          char surname[50];
          char name[50];
          char patronymic[50];
          char position[50];
          char gender[10];
          Date hire_date;
      } Employee;
      
      int main() {
          setlocale(LC_ALL, "");
      
          Employee emp1, emp2, emp3;
      
          printf("Введите данные сотрудника 1:\n");
          printf("Фамилия: ");
          scanf("%s", emp1.surname);
          printf("Имя: ");
          scanf("%s", emp1.name);
          printf("Отчество: ");
          scanf("%s", emp1.patronymic);
          printf("Должность: ");
          scanf("%s", emp1.position);
          printf("Пол: ");
          scanf("%s", emp1.gender);
          printf("Дата приема (день месяц год): ");
          scanf("%d %d %d", &emp1.hire_date.day, &emp1.hire_date.month, &emp1.hire_date.year);
          printf("\n");
      
          printf("Введите данные сотрудника 2:\n");
          printf("Фамилия: ");
          scanf("%s", emp2.surname);
          printf("Имя: ");
          scanf("%s", emp2.name);
          printf("Отчество: ");
          scanf("%s", emp2.patronymic);
          printf("Должность: ");
          scanf("%s", emp2.position);
          printf("Пол: ");
          scanf("%s", emp2.gender);
          printf("Дата приема (день месяц год): ");
          scanf("%d %d %d", &emp2.hire_date.day, &emp2.hire_date.month, &emp2.hire_date.year);
          printf("\n");
      
          printf("Введите данные сотрудника 3:\n");
          printf("Фамилия: ");
          scanf("%s", emp3.surname);
          printf("Имя: ");
          scanf("%s", emp3.name);
          printf("Отчество: ");
          scanf("%s", emp3.patronymic);
          printf("Должность: ");
          scanf("%s", emp3.position);
          printf("Пол: ");
          scanf("%s", emp3.gender);
          printf("Дата приема (день месяц год): ");
          scanf("%d %d %d", &emp3.hire_date.day, &emp3.hire_date.month, &emp3.hire_date.year);
          printf("\n");
      
          Date current_date = { 15, 12, 2025 };
      
          printf("\nСотрудники со стажем более 10 лет:\n");
      
          int found = 0;
      
          int years1 = current_date.year - emp1.hire_date.year;
          if (current_date.month < emp1.hire_date.month ||
              (current_date.month == emp1.hire_date.month && current_date.day < emp1.hire_date.day)) {
              years1--;
          }
          if (years1 > 10) {
              printf("Сотрудник 1: %s %s %s, стаж: %d лет\n",
                  emp1.surname, emp1.name, emp1.patronymic, years1);
              found = 1;
          }
      
          int years2 = current_date.year - emp2.hire_date.year;
          if (current_date.month < emp2.hire_date.month ||
              (current_date.month == emp2.hire_date.month && current_date.day < emp2.hire_date.day)) {
              years2--;
          }
          if (years2 > 10) {
              printf("Сотрудник 2: %s %s %s, стаж: %d лет\n",
                  emp2.surname, emp2.name, emp2.patronymic, years2);
              found = 1;
          }
      
          int years3 = current_date.year - emp3.hire_date.year;
          if (current_date.month < emp3.hire_date.month ||
              (current_date.month == emp3.hire_date.month && current_date.day < emp3.hire_date.day)) {
              years3--;
          }
          if (years3 > 10) {
              printf("Сотрудник 3: %s %s %s, стаж: %d лет\n",
                  emp3.surname, emp3.name, emp3.patronymic, years3);
              found = 1;
          }
      
          if (!found) {
              printf("Сотрудников со стажем более 10 лет не найдено.\n");
          }
          return 0;
      }
## 3. Результаты работы программы
   Введите данные сотрудника 1:
Фамилия: Saprykin
Имя: Stepan
Отчество: Ur.
Должность: -
Пол: male
Дата приема (день месяц год): 20 10 2007

Введите данные сотрудника 2:
Фамилия: Kartoshov
Имя: Victor
Отчество: Ol.
Должность: director
Пол: male
Дата приема (день месяц год): 12 12 2020

Введите данные сотрудника 3:
Фамилия: Kapustin
Имя: Dima
Отчество: H.
Должность: ingineer
Пол: male
Дата приема (день месяц год): 04 09
1999


Сотрудники со стажем более 10 лет:
Сотрудник 1: Saprykin Stepan Ur., стаж: 18 лет
Сотрудник 3: Kapustin Dima H., стаж: 26 лет
## 4. Информация о разработчике: 
Сапрыкин Степан, бИЦ-251
