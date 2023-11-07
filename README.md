# Задача регрессии. Предсказание цены алмазов
Проект включает в себя следующее:
* [ноутбук](./notebook/diamonds.ipynb) с анализом датасета, визуализациями, *EDA*, *ML*/*DL* и выводами. [Ссылка](https://nbviewer.org/github/ScReameer/Diamond-price-prediction/blob/main/notebook/diamonds.ipynb) на этот же ноутбук на сайте https://nbviewer.org/ (более удобная навигация, работают внутренние гиперссылки)

* [приложение](./app/), включащее в себя интерфейс для работы с готовой моделью (получение предсказаний в удобном формате). Есть 2 различных способа, как открыть приложение, выбор происходит через *Windows CMD/Linux Bash* после запуска:
    * `app` - десктопная версия приложения. Не работает, если приложение используется в контейнере *Docker*, т.к. *Docker* не предоставляет графический интерфейс от внутренней системы
    * `web` - веб-версия приложения, необходимо будет вставить *URL* из командной строки в адресную строку браузера. Например, `localhost:8502`. Работает как на *Windows*, так и через *Docker*
## Запуск приложения
### Способ 1: *Windows*
1. Скачать репозиторий
2. Распаковать в удобное место
3. Установить *Python* версии не ниже 3.10.8
4. Запустить файл `start.bat` (будет создано виртуальное окружение `venv` внутри папки `app`, в которое установятся все зависимости)
5. Выбрать желаемый способ отображения: `app`  или `web`
### Способ 2: *Docker*
1. Скачать образ  
    `docker pull screameer/diamonds`
2. Запустить контейнер  
    `docker run -it -p=8502:8502 --rm --name=diamonds screameer/diamonds`
3. Выбрать способ отображения `web`
4. Перейти по *URL* из командной строки