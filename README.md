# MY WIFI KARADIO
Слушать радио в Интернет давно стало привычным делом.
Вот и у меня есть несколько любимых радиостанций, которые я включаю на компьютере.
Среди них есть и эфирные и работающие только в Интернет.
Хочу вам рассказать, как сделать удобное устройство для прослушивания Интернет радиостанций без использования компьютера.
Один из самых известных проектов такого устройства - это [Ka-Radio](https://github.com/karawin/Ka-Radio).

Видео сборки:
[![Видео](https://github.com/dbprof/my-wifi-karadio/blob/master/video.png)](https://youtu.be/e8Mtywe9EV4)
Для сборки потребуется:
* 1 х Коробка распределительная Экопласт 85х85х40 мм цвет серый, IP44
https://leroymerlin.ru/product/korobka-raspredelitelnaya-ekoplast-85h85h40-mm-cvet-seryy-12464451/
* 1 х ESP8266 NodeMcu Lua v3
https://aliexpress.ru/item/32779189539.html
* 1 х Модуль записи MP3 VS1053
https://aliexpress.ru/item/32354143509.html
* 1 х разъем micro usb
https://aliexpress.ru/item/4000216515466.html
* 1 х Энкодер
https://aliexpress.ru/item/32917680841.html
* 1 х Arduino NANO
https://aliexpress.ru/item/32989224656.html
* 1 х OLED Display
https://aliexpress.ru/item/32835854912.html
* 3 х Однорядный штыревой разъем PCB
https://aliexpress.ru/item/32597304567.html
* 1 х Макет печатной платы
https://aliexpress.ru/item/32616526051.html

ИНСТРУКЦИЯ (видеоинструкция ниже):
1. Сборка по [схеме](https://github.com/dbprof/my-wifi-karadio/blob/master/schema.png) ниже
2. Скачать архив с GitHub (https://github.com/dbprof/my-wifi-karadio)
3. Запустить ESP8266 DOWNLOAD TOOL V3.8.5 (https://www.espressif.com/en/support/download/other-tools)
4. Выбрать в интерфейсе программы соответствующие файлы из директории "esp8266", как на [картинке](https://github.com/dbprof/my-wifi-karadio/blob/master/DownloadTool.png) и прошить ESP8266
5. При помощи Arduino IDE прошить плату Arduino NANO соответствующими скетчами из директории "arduino"
6. Включить общее питание и подключиться к WiFi точке доступа WifiKaRadio
7. В браузере набрать адрес ESP8266 по умолчанию 192.168.4.1
8. На закладке SETTING ввести имя вашей точки доступа и пароль к ней, а после этого нажать "Validate" и перезагрузить
9. В случае успешного подключения ESP8266 получит адрес от вашей точки доступа, если не подключилась, то можно повторить предидущие шаги
10. Переподключиться по полученному от точки доступа адресу и в закладке EDIT завести необходимые вам адреса интернет радиостанций либо в разделе "Stations Save & Restore" выбрать файл из архива с именем WebStations.txt и нажать "Restore Station to WebRadio"
11. В закладке RADIO раздела "Station control" выбирайте из комбо бокса радиостанцию и нажимайте кнопку проигрывания (бывает, что поток недоступен или не читается, значит есть проблемы с сигналом WiFi или доступом к потоку в Интернет)
12. Устройство также управляется при помощи энкодера: вращение - изменение громкости, нажати и вращение - переключение станций, нажатие - вкл/выкл. (список команд принимаемых esp8266 от arduino в файле [Interface.txt](https://github.com/dbprof/my-wifi-karadio/blob/master/Interface.txt))

Схема подключения:
![Схема подключения](https://github.com/dbprof/my-wifi-karadio/blob/master/schema.png)

Установки для прошивки esp8266:
![Список файлов для прошивки esp8266](https://github.com/dbprof/my-wifi-karadio/blob/master/DownloadTool.png)
