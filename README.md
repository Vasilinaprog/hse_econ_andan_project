# Анализ данных на python проект


## Наш план
- Собрать данные:
  -Название
  -Производитель
  -Цена
  -Память
  -Камера
  -Экран

  с трёх сайтов в один датасет (ДС1):
  -https://www.technopark.ru/smartfony/
  -https://м.ноу-хау.рф
  -https://www.mvideo.ru/smartfony-i-svyaz-10

- Собрать данные с сайта https://app-time.ru/smartout/1/2024  в датасет (ДС2)

- Заполнить ДС1 с помощью ДС2, добавив доп колонку с годом выпуска


- Делать EDA дальше со всеми этими данными 
- Машинка потом

## Наши проблемы с парсингом(вроде бы вы не должны сильно бить)
Нашей командой было потрачено ~9 человекочасов на парсинг сайта Технопарка https://www.technopark.ru/smartfony/.
"Люди" которые создавали этот сайт и его защиту от ботов заслуживают самых больших антинаград за всю историю этой Вселенной.
Библиотека BeautifulSoup4 оказалась бесссильна(вне зависимости от усилий нашей команды, реквесты не проходили защиту).
Библиотека Selenium тоже.
Поэтому было принято решение использоватьь сайт https://www.mvideo.ru/smartfony-i-svyaz-10 и тактику парсинга в файлы типа .json.
Он тоже оказался крепким орешком: реквест на ~55-65% страниц(как повезёт) возвращает инвалидный формат .json с одинарными кавычками вместо двойных --> декодерJSON ломается.
Поэтому все данные предзагружены с локального устройства.

## EDA идёт норамльно, просим не снижать за малый объём, в связи с потерей душевных и физических сил на этапе парсинга данных :(((((



## Навигация
- .json файлы в основной папке - временные 
- папка data - финальные результаты полученные со всех страниц сайта МВидео 
- config.py - cookies and headers для парсинга 
- main.py - основной файл парсер
- main.ipynb - основной EDA файл (дан как ссылка на лайв файл с коллаба)
