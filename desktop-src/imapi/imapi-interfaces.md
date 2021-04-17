---
title: Интерфейсы IMAPI
description: В следующих таблицах приведены и кратко описаны интерфейсы, используемые разработчиками C/C++ и связанным объектом скрипта. Добавьте в таблицу имя объекта с параметром \ 0034; IMAPI2. \ 0034; для полного определения имени объекта при создании объекта в скрипте.
ms.assetid: dba81a45-34a8-4b49-9ccb-d61a7e7ee1f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac989a9871b761a1f1700ec599cc51affd30b2e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "105681578"
---
# <a name="imapi-interfaces"></a>Интерфейсы IMAPI

В следующих таблицах приведены и кратко описаны интерфейсы, используемые разработчиками C/C++ и связанным объектом скрипта. Добавьте перед именем объекта в таблице "IMAPI2". для полного определения имени объекта при создании объекта в скрипте.

В следующей таблице перечислены интерфейсы, связанные с устройствами, подсистемой записи и форматами записи и стирания форматирования.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Интерфейс</td>
<td>Объект</td>
</tr>
<tr class="even">
<td>Высокоуровневая подсистема записи.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></li>
</ul></td>
<td>MsftWriteEngine2</td>
</tr>
<tr class="odd">
<td>Основной модуль записи образов.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></li>
</ul></td>
<td>MsftDiscFormat2Data</td>
</tr>
<tr class="even">
<td>Ластик для дисков.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></li>
</ul></td>
<td>MsftDiscFormat2Erase</td>
</tr>
<tr class="odd">
<td>Необработанный модуль записи изображений.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></li>
</ul></td>
<td>MsftDiscFormat2RawCD</td>
</tr>
<tr class="even">
<td>Средство записи образов в один раз.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></li>
</ul></td>
<td>MsftDiscFormat2TrackAtOnce</td>
</tr>
<tr class="odd">
<td>Перечисление дисковых устройств в списке оборудования системы.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></li>
</ul></td>
<td>MsftDiscMaster2</td>
</tr>
<tr class="even">
<td>Делегат уведомления для объекта MsftDiscMaster2.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></li>
</ul></td>
<td>DDiscMaster2Events</td>
</tr>
<tr class="odd">
<td>Отдельное устройство записи.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></li>
</ul></td>
<td>MsftDiscRecorder2</td>
</tr>
<tr class="even">
<td>Атрибуты записи устройства, включая тип носителя, скорость записи и тип углового элемента управления скоростью.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>ивритеспиддескриптор</strong></a></li>
</ul></td>
<td>мсфтвритеспиддескриптор</td>
</tr>
</tbody>
</table>



 

В следующей таблице перечислены интерфейсы файловой системы.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Интерфейс</td>
<td>Объект</td>
</tr>
<tr class="even">
<td>Поток загрузочного образа и свойства для интеграции загрузочного образа в образ диска.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>ибутоптионс</strong></a></li>
</ul></td>
<td>бутоптионс</td>
</tr>
<tr class="odd">
<td>Образ и свойства файловой системы. Этот объект включает все записи и ссылки на образ загрузки и образ результата.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>дфилесистемимажеевентс</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>дфилесистемимажеимпортевентс</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>ифилесистемимаже</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></li>
</ul></td>
<td>кфилесистемимаже</td>
</tr>
<tr class="even">
<td>Контейнер потока данных, предоставленный объектом файловой системы.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>ифилесистемимажересулт</strong></a></li>
</ul></td>
<td>филесистемимажересулт</td>
</tr>
<tr class="odd">
<td>Элемент каталога в образе файловой системы.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>ифсидиректоритем</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></li>
</ul></td>
<td>фсидиректоритем</td>
</tr>
<tr class="even">
<td>Файловый элемент в образе файловой системы.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>ифсифилеитем</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></li>
</ul></td>
<td>фсифилеитем</td>
</tr>
<tr class="odd">
<td>Интерфейс, содержащий свойства, общие для файлов и элементов каталога.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>ифсиитем</strong></a></li>
</ul></td>
<td>фсиитем</td>
</tr>
<tr class="even">
<td>Создание необработанного образа компакт-диска.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>иравкдимажекреатор</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>иравкдимажетраккинфо</strong></a></li>
</ul></td>
<td>мсфтравкдимажекреатор</td>
</tr>
<tr class="odd">
<td>Объект модуля поддержки объекта Stream для сцепления нескольких потоков.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>истреамконкатенате</strong></a></li>
</ul></td>
<td>мсфтстреамконкатенате</td>
</tr>
<tr class="even">
<td>Поток с чередованием для добавления к образу диска.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>истреаминтерлеаве</strong></a></li>
</ul></td>
<td>мсфтстреаминтерлеаве</td>
</tr>
<tr class="odd">
<td>Созданный в псевдо-Random поток.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>истреампсеудорандомбасед</strong></a></li>
</ul></td>
<td>MsftStreamPrgn001</td>
</tr>
<tr class="even">
<td>Объект скрипта <strong>мсфтстреамзеро</strong> не реализован в качестве интерфейса.</td>
<td><a href="msftstreamzero.md"><strong>мсфтстреамзеро</strong></a></td>
</tr>
</tbody>
</table>



 

В следующей таблице перечислены вспомогательные интерфейсы.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Интерфейс</td>
<td>Объект</td>
</tr>
<tr class="even">
<td>Коллекция диапазонов секторов в образе файловой системы.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>иблоккранже</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>иблоккранжелист</strong></a></li>
</ul></td>
<td>Нет соответствующего объекта</td>
</tr>
<tr class="odd">
<td>Поддержка записи при проверке.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>ибурнверификатион</strong></a></li>
</ul></td>
<td>Нет соответствующего объекта</td>
</tr>
<tr class="even">
<td>Перечислитель Фсиитемс для приложений C/C++.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>иенумфсиитемс</strong></a></li>
</ul></td>
<td>енумфсиитемс</td>
</tr>
<tr class="odd">
<td>Перечислитель Прогресситемс для приложений C/C++.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>иенумпрогресситемс</strong></a></li>
</ul></td>
<td>енумпрогресситемс</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>ифсинамедстреамс</strong></a></li>
</ul></td>
<td>FsiFileItem2</td>
</tr>
<tr class="odd">
<td>Поддержка проверки ISO-образа.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>иисоимажеманажер</strong></a></li>
</ul></td>
<td>Нет соответствующего объекта</td>
</tr>
<tr class="even">
<td>Поддержка нескольких сеансов.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>имултисессион</strong></a></li>
</ul></td>
<td>Нет соответствующего объекта</td>
</tr>
<tr class="odd">
<td>Последовательная поддержка нескольких сеансов.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>имултисессионсекуентиал</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></li>
</ul></td>
<td>мсфтмултисессионсекуентиал</td>
</tr>
<tr class="even">
<td>Имя файла и связанные блоки в результирующем изображении.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>ипрогресситем</strong></a></li>
</ul></td>
<td>прогресситем</td>
</tr>
<tr class="odd">
<td>Вывод образа результатов, разбитый по имени файла и связанным блокам.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>ипрогресситемс</strong></a></li>
</ul></td>
<td>прогресситемс</td>
</tr>
</tbody>
</table>



 

 

 




