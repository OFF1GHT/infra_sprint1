# Руководство по установке и запуску проекта "Kittygram"
Этот проект позволяет пользователям добавлять информацию о своих питомцах - котиках, включая их кличку, год рождения, цвет и достижения. Проект использует Gunicorn и Nginx для обеспечения стабильности и высокой производительности.

## Требования
Прежде чем начать установку проекта, убедитесь, что на вашем сервере установлены следующие компоненты:

- Python 3.x
- Gunicorn
- Nginx
- Git

## Установка
1. Клонируйте репозиторий проекта из GitHub:
```
git clone https://github.com/your-username/kitty-focus.git
```
2. Перейдите в директорию проекта:
```
cd kitty-focus
```
3. Создайте и активируйте виртуальное окружение:
```
python3 -m venv venv
```
```
source venv/bin/activate
```
4. Установите зависимости проекта:
```
pip install -r requirements.txt
```

## Запуск
1.  Установите Gunicorn:
```
pip install gunicorn==20.1.0
```
1. Запустите Gunicorn:
```
gunicorn -b 0.0.0.0:8000 app:app
```
2. Настройте Nginx. Создайте конфигурационный файл в директории /etc/systemd/system/gunicorn_названиепроекта.service

3. Перезапустите Nginx:
```
sudo service nginx restart
```
Теперь ваш проект "Kittygram" доступен по адресу https://infrasprint1.hopto.org.

## Использование
1. Откройте веб-браузер и перейдите по адресу https://infrasprint1.hopto.org.
2. Нажмите на кнопку "Добавить кота" и заполните информацию о своем питомце.
3. Просматривайте и редактируйте информацию о котиках на главной странице.
