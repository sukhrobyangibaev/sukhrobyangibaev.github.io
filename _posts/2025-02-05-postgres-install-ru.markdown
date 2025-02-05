---
layout: post
title: "Базы данных | Практическое занятие 1"
description: Введение в PostgreSQL
date: 2025-02-05 08:30:00 +0500
categories: [class_materials,databases_en]
---

# Введение в PostgreSQL

# Скачивание и установка PostgreSQL

Чтобы установить PostgreSQL локально на свой компьютер, посетите [установщик от EDB](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads) и скачайте последнюю версию, совместимую с вашей операционной системой.

![](/assets/images/2025-02-05-postgres-install/Screenshot%202025-02-05%20095648%201.png)

## Запуск установки

Когда загрузка будет завершена, дважды щелкните загруженный файл и начните установку:

![](/assets/images/2025-02-05-postgres-install/Screenshot%202025-02-05%20095922.png)

![](https://www.w3schools.com/postgresql/screenshot_postgresql_install2.png)

## Укажите директорию

Вы можете указать расположение PostgreSQL, я выберу вариант по умолчанию:

![](/assets/images/2025-02-05-postgres-install/Screenshot%202025-02-05%20100145.png)

## Выбор компонентов

Чтобы использовать PostgreSQL, вам потребуется установить сервер PostgreSQL. В этом руководстве мы также будем использовать компонент pgAdmin 4 и инструменты командной строки:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_install4.png)

## Директория хранения

Вы также можете выбрать, где хранить данные базы данных, я выберу вариант по умолчанию:

![](/assets/images/2025-02-05-postgres-install/Screenshot%202025-02-05%20100308.png)

## Выбор пароля

Вам нужно будет выбрать пароль для доступа к базе данных. Поскольку это локальная база данных без входящих подключений, я выберу пароль 12345678:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_install6.png)

## Выбор порта

Вы можете установить порт, который должен прослушивать сервер, я выберу вариант по умолчанию:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_install7.png)

## Выбор локали

Выберите географическое расположение сервера базы данных:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_install8.png)

## Финальная проверка

Если все выглядит нормально, нажмите «Далее», чтобы продолжить:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_install9.png)

## Запуск установки:

Нажмите «Далее», чтобы начать установку:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_install10.png)

## Установка

Это может занять некоторое время, пожалуйста, подождите.

![](https://www.w3schools.com/postgresql/screenshot_postgresql_install11.png)

## Завершено!

Теперь вы установили PostgreSQL на свой компьютер, и в следующей главе вы начнете его использовать!

![](https://www.w3schools.com/postgresql/screenshot_postgresql_install12.png)

---
# Подключение к базе данных

## SQL Shell (psql)

SQL Shell (psql) — это программа на основе терминала, в которой вы можете писать и выполнять синтаксис SQL в терминале командной строки.

### Откройте SQL Shell (psql)

Вы найдете инструмент SQL Shell (psql) в меню «Пуск» в разделе PostgreSQL:

![](/assets/images/2025-02-05-postgres-install/Screenshot%202025-02-05%20100931%201.png)

Как только программа откроется, вы должны увидеть окно, подобное приведенному ниже.

Введите имя сервера.

Предлагаемый вариант — localhost, что верно, нажмите Enter, чтобы принять:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_shell1.png)

## База данных

Предлагаемая база данных — postgres, что верно, нажмите Enter, чтобы принять:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_shell2.png)

## Порт

Предлагаемый порт — 5432, что верно, по крайней мере, в моем случае, нажмите Enter, чтобы принять:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_shell3.png)

## Имя пользователя

Предлагаемое имя пользователя — postgres, что верно, нажмите Enter, чтобы принять:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_shell4.png)

## Пароль

Введите пароль, который вы выбрали при установке базы данных PostgreSQL, мой пароль 12345678:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_shell5.png)

## Результат

Результат может выглядеть как ошибка, но если он показывает `psql (17.2)` или любую другую версию, и в конце вы видите команду `postgres=#` (и, возможно, предупреждение между ними), то вы успешно подключились к базе данных!

![](/assets/images/2025-02-05-postgres-install/Pasted%20image%2020250205133203.png)

## Выполнение операторов SQL

После подключения к базе данных вы можете начать выполнять операторы SQL.

Наша база данных пуста, поэтому мы пока не можем запрашивать какие-либо таблицы, но мы можем проверить версию с помощью этого оператора SQL:

```sql
SELECT version();
```

Чтобы вставить операторы SQL в команду SQL Shell, просто напишите их после команды `postgres=#` вот так:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_shell7.png)

Нажмите Enter, и результат должен выглядеть так:

![](/assets/images/2025-02-05-postgres-install/Pasted%20image%2020250205133248.png)

## Помните о точке с запятой

> Всегда завершайте операторы SQL точкой с запятой `;`

---

# pgAdmin4

## Запуск pgAdmin4

Вы найдете приложение pgAdmin4 в меню «Пуск» в разделе PostgreSQL:

![](/assets/images/2025-02-05-postgres-install/Pasted%20image%2020250205133521.png)

## pgAdmin4

Начните с открытия параметра «Серверы» в меню слева:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_pgadmin4_2.png)

## Подключение к серверу

Теперь вам нужно ввести пароль, который вы создали при установке PostgreSQL, мой пароль 12345678:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_pgadmin4_3.png)

## Поиск базы данных

Нажмите на параметр «База данных» в меню слева:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_pgadmin4_4.png)

## Открытие инструмента запросов

Вы должны найти базу данных с именем `postgres`, щелкните ее правой кнопкой мыши и выберите «Инструмент запросов»:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_pgadmin4_5.png)

## Инструмент запросов

В инструменте запросов мы можем начать выполнять операторы SQL.

![](https://www.w3schools.com/postgresql/screenshot_postgresql_pgadmin4_6.png)

## Написание операторов SQL

Наша база данных пуста, поэтому мы пока не можем запрашивать какие-либо таблицы, но мы можем проверить версию с помощью этого оператора SQL:

```sql
SELECT version();
```

Чтобы вставить операторы SQL в инструмент запросов, просто напишите в поле ввода вот так:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_pgadmin4_7.png)

## Выполнение операторов SQL

Чтобы выполнить оператор SQL, нажмите кнопку «Воспроизвести» над полем ввода:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_pgadmin4_8.png)

## Результат

Оператор SQL выполнен, и вы можете увидеть результат в области «Вывод данных»:

![](https://www.w3schools.com/postgresql/screenshot_postgresql_pgadmin4_9.png)

Теперь мы изучили два способа подключения к базе данных и выполнения операторов SQL на ней:

- SQL Shell (psql)
- pgAdmin 4
