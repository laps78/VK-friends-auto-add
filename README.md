# VK recomended friends auto clicker

## Содержание

[Описание программного обеспечения](#описание-программного-обеспечения)

[Возможности алгоритма](#возможности-алгоритма)

[Как это работает?](#как-это-работает?)

[Инcтрукция по установке расширения Chrome](#инcтрукция-по-установке-расширения-chrome)

[Использование расширения chrome или userScript](#использование-расширения-chrome-или-userScript)

[Откуда можно скачать и установить userScripts](#откуда-можно-скачать-и-установить-userscripts)

## Описание программного обеспечения

**Автокликер для добавления друзей Вконтакте**
by L.A.P.S. Lab

Данный продукт поставляется бесплатно и представляет собой mvp версию расширенного ПО для работы с социальными сетями от лаборатории [L.A.P.S. Lab](https://prolaps.ru)

ПО распространяется свободно в нескольких версиях:

- Google Chrome Extension - расширение для браузера google chrome
- userScript - пользовательский скрипт для браузерных расширений типа [GreaseMonkey](https://ru.wikipedia.org/wiki/Greasemonkey), [TemperMonkey](https://ru.wikipedia.org/wiki/Tampermonkey), e.t.c.
- Исходного кода на языке программирования javascript, содержащегося [тут](https://github.com/laps78/VK-friends-auto-add/blob/main/vk-friends-clicker.js), в данном репозитории.

В данном репозитории содержится его свободно распространяемый открытый [исходный код](https://github.com/laps78/VK-friends-auto-add/blob/main/vk-friends-clicker.js).

![screenshot](./assets/clicker-actions.png)

## Возможности алгоритма

1.Имитация человеческого поведения

- прокликивает ссылки в случайной последовательности
- случайный интервал между кликами (задаются параметрами, по-умолчанию - от 10 до 15 секунд между кликами)
- ограничено количество кликов (задается параметрами - по умолчанию 30)
- логи действий в консоли браузера и localStorage (ожидается)

§ 2.Доступно несколько режимов работы

- из консоли браузера
- Firefox GreeseMonkey UserScript
- Chrome расширение(ожидается)

## Как это работает?

Скрипт запускается в консоли, в расширении браузера или как выделенное расширение браузера и предлагает скликать найденное количество специфических ссылок на странице. В выдаче страницы по умолчанию 30 рекоммендаций.

После запуска скрипт:

- составляет массив ссылок из всех найденных по классу
- перемешивает ссылки в массиве
- составляет список отложенных задач типа _element.click()_
- выполняет задачи
- отчитывается о выполнении

Скрипт предполагает запуск при каждой перезагрузке страницы.

![screenshot-report](./assets/report-new.png)

## Инcтрукция по установке расширения Chrome

1. Скачиваем .ZIP архив с расширением [из репозитория](./extensions/Chrome.zip) или [из магазина (ожидается)](https://prolaps.ru/shop)
2. Если необходимо, перенесите в удобное для вас место и распакуйте ахрхив с расширением
3. Откройте браузер chrome и наберите в адресной строке chrome://extensions
   ![наберите в адресной строке chrome://extensions](./assets/new-howto/goto-extensions.png)
4. Включите режим разработчика
5. Нажмите "Загрузить распакованное расширение" и выберите папку, в которую распаковали .ZIP архив
   ![Нажмите "Загрузить распакованное расширение"](./assets/new-howto/upload-extension.png)
6. Активируйте расширение
   ![Активируйте расширение](./assets/new-howto/activate-extension.png)
7. Отключите режим разработчика

## Использование расширения chrome или userScript

1. В браузере chrome авторизуйтесь в вашем аккаунте ВК
2. Перейдите на страницу Друзья -> Найти друзей
3. Обновите страницу
4. После обновления прокрутите страницу немного вниз, чтобы отобразилось больше рекомендаций
5. Автокликер предложит добавить рекомендации - нажмите "ок"
6. Дождитесь окончания работы кликера и вывода диалогового окна с отчетом. Либо жмите [F12]->[консоль] - информация о работе расширения логируется в консоли браузера
7. Повторите пп. 3-6 при необходимости

## Откуда можно скачать и установить userScripts

- [База пользовательских скриптов Greasy Fork](https://greasyfork.org/ru/scripts/470474-vk-recomended-friends-auto-clicker)
