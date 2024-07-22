Для развертывания и запуска проекта Django CRM по ссылке здесь, вам потребуется выполнить следующие шаги:
### 1. Установка системных требований:
Установите необходимые пакеты, запустив следующие команды:
```
     sudo apt install postgresql xvfb libfontconfig wkhtmltopdf git libpq-dev python3-dev python3-pip gem ruby ruby-dev build-essential libssl-dev libffi-dev python3-venv redis-server redis-tools virtualenv -y
     sudo gem install sass
     sudo apt-get install postfix
```
### 2. Установка зависимостей проекта:
Создайте и активируйте виртуальное окружение:
```
     virtualenv venv
     source venv/bin/activate
```
- Установите зависимости проекта, выполнив:
```
     pip install -r requirements.txt
```
### 3. Настройка переменных окружения:
- Следуйте инструкциям в файле env.md для переменных окружения и сохраните их в файле .env в текущей папке проекта.
- Добавьте 127.0.0.1 test.localhost в файл hosts /etc/hosts.
### 4. Запуск проекта:
- Выполните миграции базы данных:
```
     python manage.py migrate
```
- Запустите сервер:
```
     python manage.py runserver
```
- Откройте <http://localhost:8000> в браузере и создайте новую учетную запись с именем компании "test".
### 5. Редактирование контента:
Для редактирования контента в блоге выполните:
```
     python manage.py create_blog_user 'username'
```
### 6. Полезные инструменты и пакеты:
- `pipdeptree` - для просмотра дерева зависимостей pip.
- `black` - для форматирования кода в соответствии со стандартами кодирования Python.
- `pip-check -H` - для просмотра обновляемых пакетов.
Эти шаги помогут вам успешно развернуть и запустить проект Django CRM.
