﻿play_game.html - запускной файл
versions.txt - список версий с последними изменениями, выводится по клику на номер версии в левом нижнем углу в интерфейсе

Директории:
	css - стили
	games - игры
	images - изображения для нужд интерпретатора
	js - скрипты javascript
	log - файлы с логами
	php - скрипты php
	promo - баннеры
	
Содержимое директории css:
	styles.css - единственный файл со стилями

Содержимое директории games:
	Каждая игра лежит в своей директории, название директории должно быть на английском.
	Файлы:
		icon.png и icon-high.png - иконки игры; первая - в строке заголовка браузера, вторая не используется.
		thumbnail.png и thumbnail-high.png - превьюшки; первая - выводится на кнопке игры, вторая - на фоне главного экрана игры.
		img.ini - файл с информацией о разрешении игры
		info.txt - файл с названием игры
	Директории:
		background - директория с изображениями фонов
		foreground - директория со спрайтами
		script - директория со скриптами (.SCR)
		sound - директория с музыкой и звуками.
	
	Замечание 1: регистр имён файлов и директорий играет роль.
	Замечание 2: поддержка того или иного формата аудиофайлов зависит исключительно от браузера.

Содержимое директории images:
	vnds.png - иконка интерпретатора, пока не выбрана игра. После выбора игры заменяется на иконку игры.

Содержимое директории js:
	functions.js - служебные функции, не относящиеся непосредственно к движку.
	vnds.class.js - функции непосредственно движка VNDS и близкие к ним по важности.
	jquery-3.2.1.min.js - библиотека jquery, с которой точно всё работает.
	ie_html5_support.js - "заглушка" для HTML5 для IE9. Не уверен, что нужна, но пусть будет.

Содержимое директории log:
	vnds_errors.log - лог ошибок движка (формат CSV, разделитель - табуляция)
	game_XXX_errors.log - лог ошибок скриптов игры XXX (формат CSV, разделитель - табуляция)
	promo_show.log - лог показов баннеров (формат CSV, разделитель - табуляция)
	promo_click.log - лог кликов на баннеры (формат CSV, разделитель - табуляция)

Содержимое директории php:
	get_games_list.php - скрипт, возвращающий информацию об установленных играх
	get_script_data.php - скрипт, возвращающий содержимое текущего скрипта VNDS
	get_promo.php - скрипт, возвращающий информацию о баннере, который необходимо показать (см. promo_show.log)
	redirect_promo.php - скрипт, сохраняющий информацию о клике на баннер (см.promo_click.log)
	save_log.php - скрипт, сохраняющий информацию об ошибках интерпретатора и скриптов VNDS (см. vnds_errors.log и game_XXX_errors.log)

Содержимое директории promo:
	promo.csv - файл с информацией о баннерах (468x60), например: "Энтузиасты;http://enthusiasts-ts.ru/;ent.jpg"
	Графические файлы, указанные в файле promo.csv, например "ent.jpg"
