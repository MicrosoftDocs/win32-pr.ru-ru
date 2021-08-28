---
title: Интерфейсы IMAPI
description: В следующих таблицах приведены и кратко описаны интерфейсы, используемые разработчиками C/C++ и связанным объектом скрипта. Добавьте в таблицу имя объекта с параметром \ 0034; IMAPI2. \ 0034; для полного определения имени объекта при создании объекта в скрипте.
ms.assetid: dba81a45-34a8-4b49-9ccb-d61a7e7ee1f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c093acd587f975859d68fda23f6c1f169d969a78
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466185"
---
# <a name="imapi-interfaces"></a>Интерфейсы IMAPI

В следующих таблицах приведены и кратко описаны интерфейсы, используемые разработчиками C/C++ и связанным объектом скрипта. Добавьте перед именем объекта в таблице "IMAPI2". для полного определения имени объекта при создании объекта в скрипте.

В следующей таблице перечислены интерфейсы, связанные с устройствами, подсистемой записи и форматами записи и стирания форматирования.




| | | Интерфейс | Объект | | Высокоуровневая подсистема записи.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></li></ul> | MsftWriteEngine2 | | Основной модуль записи образов.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></li></ul> | MsftDiscFormat2Data | | Ластик для дисков.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></li></ul> | MsftDiscFormat2Erase | | Необработанный модуль записи изображений.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></li></ul> | MsftDiscFormat2RawCD | | Средство записи образов в один раз.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></li></ul> | MsftDiscFormat2TrackAtOnce | | Перечисление дисковых устройств в списке оборудования системы.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></li></ul> | MsftDiscMaster2 | | Делегат уведомления для объекта MsftDiscMaster2.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></li></ul> | DDiscMaster2Events | | Отдельное устройство записи.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></li></ul> | MsftDiscRecorder2 | | Атрибуты записи устройства, включая тип носителя, скорость записи и тип углового элемента управления скоростью.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>ивритеспиддескриптор</strong></a></li></ul> | Мсфтвритеспиддескриптор | 




 

В следующей таблице перечислены интерфейсы файловой системы.




| | | Интерфейс | Объект | | Поток загрузочного образа и свойства для интеграции загрузочного образа в образ диска.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>ибутоптионс</strong></a></li></ul> | Бутоптионс | | Образ и свойства файловой системы. Этот объект включает все записи и ссылки на образ загрузки и образ результата.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>дфилесистемимажеевентс</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>дфилесистемимажеимпортевентс</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>ифилесистемимаже</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></li></ul> | Кфилесистемимаже | | Контейнер потока данных, предоставленный объектом файловой системы.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>ифилесистемимажересулт</strong></a></li></ul> | Филесистемимажересулт | | Элемент каталога в образе файловой системы.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>ифсидиректоритем</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></li></ul> | Фсидиректоритем | | Файловый элемент в образе файловой системы.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>ифсифилеитем</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></li></ul> | Фсифилеитем | | Интерфейс, содержащий свойства, общие для файлов и элементов каталога.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>ифсиитем</strong></a></li></ul> | Фсиитем | | Создание необработанного образа компакт-диска.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>иравкдимажекреатор</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>иравкдимажетраккинфо</strong></a></li></ul> | Мсфтравкдимажекреатор | | Объект модуля поддержки объекта Stream для сцепления нескольких потоков.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>истреамконкатенате</strong></a></li></ul> | Мсфтстреамконкатенате | | Поток с чередованием для добавления к образу диска.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>истреаминтерлеаве</strong></a></li></ul> | Мсфтстреаминтерлеаве | | Созданный в псевдо-Random поток.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>истреампсеудорандомбасед</strong></a></li></ul> | MsftStreamPrgn001 | | Объект скрипта <strong>мсфтстреамзеро</strong> не реализован в качестве интерфейса. | <a href="msftstreamzero.md"><strong>мсфтстреамзеро</strong></a> | 




 

В следующей таблице перечислены вспомогательные интерфейсы.




| | | Интерфейс | Объект | | Коллекция диапазонов секторов в образе файловой системы.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>иблоккранже</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>иблоккранжелист</strong></a></li></ul> | Нет соответствующего объекта | | Поддержка записи при проверке.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>ибурнверификатион</strong></a></li></ul> | Нет соответствующего объекта | | Перечислитель Фсиитемс для приложений C/C++.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>иенумфсиитемс</strong></a></li></ul> | Енумфсиитемс | | Перечислитель Прогресситемс для приложений C/C++.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>иенумпрогресситемс</strong></a></li></ul> | Енумпрогресситемс | | <ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>ифсинамедстреамс</strong></a></li></ul> | FsiFileItem2 | |. Поддержка проверки образов ISO.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>иисоимажеманажер</strong></a></li></ul> | Нет соответствующего объекта | | Поддержка нескольких сеансов.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>имултисессион</strong></a></li></ul> | Нет соответствующего объекта | | Последовательная поддержка нескольких сеансов.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>имултисессионсекуентиал</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></li></ul> | Мсфтмултисессионсекуентиал | | Имя файла и связанные блоки в результирующем изображении.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>ипрогресситем</strong></a></li></ul> | Прогресситем | | Вывод образа результатов, разбитый по имени файла и связанным блокам.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>ипрогресситемс</strong></a></li></ul> | Прогресситемс | 




 

 

 




