# xml-parser
[![Stars](https://img.shields.io/github/stars/khorevaa/xml-parser.svg?label=Github%20%E2%98%85&a)](https://github.com/khorevaa/xml-parser/stargazers)
[![Release](https://img.shields.io/github/tag/khorevaa/xml-parser.svg?label=Last%20release&a)](https://github.com/khorevaa/xml-parser/releases)
[![Открытый чат проекта https://gitter.im/EvilBeaver/oscript-library](https://badges.gitter.im/khorevaa/xml-parser.png)](https://gitter.im/EvilBeaver/oscript-library)

[![Build Status](https://travis-ci.org/khorevaa/xml-parser.svg?branch=master)](https://travis-ci.org/khorevaa/xml-parser)
[![Coverage Status](https://coveralls.io/repos/github/khorevaa/xml-parser/badge.svg?branch=master)](https://coveralls.io/github/khorevaa/xml-parser?branch=master)

# Библиотека для cериализации данных в xml

Библиотека предназначена для записи и чтения данных XML для

# Установка

Для установки необходимо:
* Скачать файл *.ospx из раздела [releases](https://github.com/khorevaa/xml-parser/releases)
* Воспользоваться командой:

```
opm install -f <ПутьКФайлу>
```
или

```
opm install xml-parser
```

# Пример работы:

* Чтение данных из файла
```bsl

    //<ФайлПФР>
    //    <ИмяФайла>
    //        <НазваниеФормата>fb2</НазваниеФормата>
    //        <НазваниеПрограммы />
    //    </ИмяФайла>
    //</ФайлПФР>

    ПутьКФайлу = "ТутНуженПутьКФайлу";

	ПроцессорXML = Новый СериализацияДанныхXML();
	
	РезультатЧтения = ПроцессорXML.ПрочитатьИзФайла(ПутьКФайлу);

    Сообщить(РезультатЧтения"ФайлПФР"]["ИмяФайла"]["НазваниеФормата"]);

```

* Запись данных в файл
```bsl

    ПутьКФайлу = "ТутНуженПутьКФайлу";

	ПроцессорXML = Новый СериализацияДанныхXML();
	ДанныеЗаписиXML = Новый Структура("name", "Наименование");

	ПроцессорXML.ЗаписатьВФайл(ПутьКФайлу);
   
    // Содержимое файла 
    //<name>Наименование</name>

```

## Публичный интерфейс

[Документация публичного интерфейса](docs/README.md) (в разработке)

## Доработка

Доработка проводится по git-flow. Жду ваших PR.

## Лицензия

Смотри файл [`LICENSE`](LICENSE).