[![Pipeline Status](https://gitlab.crja72.ru/django_2023/projects/team5/badges/main/pipeline.svg)]

# VaccinePlan

---

## English Version 🇬🇧

### A platform for vaccination planning — helping you avoid unnecessary calls and registration queues.

### On this website, you can:

* Register a personal account  
* View clinics and available vaccines  
* Attach yourself to a specific clinic  
* View and create your personal vaccination calendar  
* Apply for clinic administration rights  

---

# Project Launch Instructions

## Basic Setup

### Clone the repository using git:

```
git clone https://gitlab.crja72.ru/django_2023/projects/team5.git
```

### Create and activate a virtual environment:

```
python3 -m venv venv 
```

```
source venv/bin/activate 
```

---

### Project Dependencies

To install dependencies for **production mode**:

```
pip3 install -r requirements/prod.txt
```

For **development mode** (includes production dependencies):

```
pip3 install -r requirements/dev.txt
```

For **testing**:

```
pip3 install -r requirements/test.txt
```

---

### Environment Variables

Create a `.env` file in the root directory of the project.  
Fill it in using the example file `.example_env`, also located in the root directory.

The variable **DJANGO_DEBUG** should be set to `False` in production mode and `True` in development mode.  
This setting affects how data is displayed on the pages.

> All the following commands are executed from the directory `team5/vaccineplan`.

---

### Secret Key

To generate a secret key for the project, execute the following commands in the terminal:

```
python3 manage.py shell
```

```
from django.core.management.utils import get_random_secret_key
```

```
get_random_secret_key()
```

---

## The following commands are executed from the project directory `vaccineplan`

### Apply migrations to create database tables:

```
python3 manage.py migrate
```

### View the current ER diagram of the database structure at:

[ERD](https://dbdiagram.io/d/VaccinePlan-65733c7756d8064ca0a99943)

### Load fixtures into the database:

```
python3 manage.py loaddata fixtures/cities.json
```

```
python3 manage.py loaddata fixtures/illnesses.json
```

```
python3 manage.py loaddata fixtures/vaccines.json
```

### Create a user for logging into the admin panel:

```
python3 manage.py createsuperuser
```

After executing the command, fill in all required fields in the console (username, email, password, etc.)

### Run the project using the following command and open the link shown in the terminal:

```
python3 manage.py runserver
```

---

## Русская версия 🇷🇺

### Платформа для планирования вакцинации. Это избавит вас от лишних звонков и очередей в регистратуру.

### На сайте вы можете:

* Зарегистрировать личный аккаунт  
* Просмотреть поликлиники и имеющиеся вакцины в ней  
* Прикрепиться к определённой поликлинике  
* Просмотреть и составить личный календарь вакцинации  
* Подать заявление на администрирование клиники  

---

# Инструкция по запуску проекта

## Основные настройки

### Склонируйте репозиторий с помощью git команды:

```
git clone https://gitlab.crja72.ru/django_2023/projects/team5.git
```

### Создайте виртуальное окружение и активируйте его:

```
python3 -m venv venv 
```

```
source venv/bin/activate 
```

---

### Зависимости проекта

Установить зависимости для **прод режима**:

```
pip3 install -r requirements/prod.txt
```

Для **дев режима** (включает в себя установку продовых зависимостей):

```
pip3 install -r requirements/dev.txt
```

Для **тестов**:

```
pip3 install -r requirements/test.txt
```

---

### Переменные виртуального окружения

Создайте в корневой директории проекта файл `.env`.  
Заполните файл переменными окружения по примеру файла `.example_env`, расположенного также в корневой директории проекта.

Значение переменной **DJANGO_DEBUG** в прод режиме — `False`, в дев режиме — `True`.  
От этого значения зависит отображение данных на страницах.

> Все дальнейшие команды выполняются из директории `team5/vaccineplan`.

---

### Секретный ключ

Получить данные секретного ключа для проекта можно с помощью выполнения следующих команд в терминале:

```
python3 manage.py shell
```

```
from django.core.management.utils import get_random_secret_key
```

```
get_random_secret_key()
```

---

## Последующие команды выполняются из директории проекта `vaccineplan`

### Выполните миграции для создания таблиц в БД:

```
python3 manage.py migrate
```

### Актуальная ER-диаграмма со структурой БД по ссылке:

[ERD](https://dbdiagram.io/d/VaccinePlan-65733c7756d8064ca0a99943)

### Загрузите фикстуры в БД:

```
python3 manage.py loaddata fixtures/cities.json
```

```
python3 manage.py loaddata fixtures/illnesses.json
```

```
python3 manage.py loaddata fixtures/vaccines.json
```

### Создайте пользователя для входа в admin-панель:

```
python3 manage.py createsuperuser
```

После выполнения команды заполните все нужные поля в консоли (юзернейм, почта, пароль и т.д.)

### Запустите проект с помощью следующей команды и перейдите по ссылке в терминале:

```
python3 manage.py runserver
```
