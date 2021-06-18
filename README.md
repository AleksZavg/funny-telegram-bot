# Funny-telegram-bot
Телеграм бот разработанный на базе Aiogram. Официальная ссылка - [@alekszavg_funny_bot](http://t.me/alekszavg_funny_bot).

Распространяется по лизенции MIT. Все поддерживаемые функции бота были взяты с других репозиториев (более подробный список можно найти в разделе [Техническая информация](#Техническая-информация))
## Содержание
- [Назначение](#Назначение)
- [Установка](#Установка)
- [Техническая информация](#Техническая-информация)
- [От автора](#От-автора)


## Назначение
Этот бот был написан для развлечения. Не стоит воспринимать его как серьёзный проект!

## Установка
В данный момент этот бот запущен на Heroku в бесплатном тарифном плане

Чтобы установить этого бота на сервис Heroku, нужно:
+ Создать приложение на этом сервисе
+ В настройках приложения добавить buildpack, и добавить нужные переменные в окружение 
> ![Пункт 2](https://github.com/AleksZavg/funny-telegram-bot/blob/main/for_github_readme/heroku_setting.png) 
+ В репозитерии уже есть нужные Procfile и Aptfile для нормальной работы бота (Procfile - для того, чтобы бота можно было запустить, а Aptfile - устанавливает нужные библиотеки для работы opencv-python)
+ Далее нужно "закинуть" исходники на сервера Heroku. Для этого привязываем, ваш клонированый к себе в профиль, репозиторий в этим ботом. После, в вкладке *Deploy* начинаем процесс "Деплоя", для этого внизу нужно нажать на кнопку *Deploy Branch*
+ Если на этом этапе у вас возникли ошибки, то могу посоветовать почитать официальную документацию Heroku c переводчиком, а также, гуглите ошибки!
+ На последнем этапе нам нужно запустить бота, для этого нужно нажать на "Ручку" и "передёрнуть" ползунок в противоположную сторону
> ![Пункт 6](https://github.com/AleksZavg/funny-telegram-bot/blob/main/for_github_readme/heroku_setting_2.png)
+ Для того, что прочитать лог нужно нажать на кнопку *More* (скриншот выше) и нажать на *View Logs*. Это не будет лишним при отладке!
+ **Если вы запустите этого бота на Heroku, то тогда не будут работать**:
     + Функция Ping запроса. (Чтобы включить эту функцию нужно: зайти в файл *ping_func.py* и убрать комментарии, а также убрать эту строку *await message.answer("❗️ Из-за технических ограничений сервиса Heroku функция Ping не работает!")*)

## Техническая информация
+ Этот бот написан на Aiogram
+ При написании бота была использована виртуальная среда (venv), а также переменные из среды (.env)
+ Для локального использования нужно создать .env , в нём должны быть *api_key* (str), *admin* (int), *who_need_notif* (list) 
+ Структура проекта взята из шаблона [Latand-а](https://github.com/Latand/aiogram-bot-template)
+ Чтобы добавить новый функционал нужно дополнять файлы *__init__.py*
+ В этой структуре бота имеет значение порядок импорта!
+ Что было использовано в боте:
    + Нейросеть по определению пола, которую я слегка адаптировал - [ССЫЛКА](https://github.com/extremecodetv/walrus)
    + Библиотека *pythonping*

## От автора
Если у вас есть какие-то пожелания или претензии, то пишите мне в телеграм [@alekszavg](https://t.me/alekszavg) или на GitHub!
Это мой первый и, пока что, самый крупный проект, поэтому если где-то напортачил, я сильно извеняюсь! Можете написать мне об ошибке, и я постараюсь её исправить.

**Всем удачи и до свидания!**
