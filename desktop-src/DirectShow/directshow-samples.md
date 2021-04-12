---
description: Примеры DirectShow
ms.assetid: 4166d5ca-5e02-49f6-bcb1-d448f8175a0c
title: Примеры DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f58c10615aaaa4305a30934e32ef9b11efb18c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538060"
---
# <a name="directshow-samples"></a>Примеры DirectShow

Примеры DirectShow включены в [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx). Они находятся в \[ корневых примерах пакета SDK для пути, с помощью \] \\ \\ мультимедиа \\ DirectShow.

В следующей таблице перечислены все примеры DirectShow, предоставленные в Windows SDK. Инструкции по созданию образцов см. в документации, предоставленной в Windows SDK.

Если для образца имеется дополнительная документация, первый столбец этой таблицы ссылается на нее.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Образец</th>
<th>Область</th>
<th>Описание</th>
<th>Дополнительные зависимости</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="directshow-base-classes.md">Базовые классы DirectShow</a></td>
<td>Библиотека базовых классов</td>
<td>Классы C++ и служебные функции, предназначенные для реализации фильтров DirectShow.</td>

</tr>
<tr class="even">
<td><a href="amcap-sample.md">Пример Амкап</a></td>
<td>Сбор</td>
<td>Приложение для записи видео.</td>
<td>стрмбасе. lib</td>
</tr>
<tr class="odd">
<td><a href="dvapp-sample.md">Пример Двапп</a></td>
<td>Сбор</td>
<td>Приложение для записи цифрового видео (DV).</td>

</tr>
<tr class="even">
<td><a href="playcap-sample.md">Пример Плайкап</a></td>
<td>Сбор</td>
<td>Простое приложение для записи.</td>

</tr>
<tr class="odd">
<td><a href="dmo-demo-sample.md">Демонстрационный пример DMO</a></td>
<td>DMO</td>
<td>Потоковая передача звуковых данных из WAV-файла с помощью звукового эффекты DMO.</td>
<td>Пакет SDK для DirectX</td>
</tr>
<tr class="even">
<td>Пример DVD-диска</td>
<td>DVD-диск</td>
<td>Демонстрируется простое воспроизведение и Навигация DVD, а также расширенные функции, такие как управление родительским уровнем, закладки, Караоке и синхронизация команд.</td>

</tr>
<tr class="odd">
<td><a href="inftee-filter-sample.md">Образец фильтра Инфти</a></td>
<td>Фильтры, Прочие</td>
<td>Пример реализации фильтра <a href="infinite-pin-tee-filter.md">бесконечного ПИН-кода tee</a> .</td>
<td>стрмбасе. lib</td>
</tr>
<tr class="even">
<td><a href="metronome-filter-sample.md">Образец фильтра метрономе</a></td>
<td>Фильтры, Прочие</td>
<td>Показывает, как реализовать ссылочное время.</td>
<td>стрмбасе. lib</td>
</tr>
<tr class="odd">
<td><a href="psi-parser-filter-sample.md">Образец фильтра средства синтаксического анализа PSI</a></td>
<td>Фильтры, Прочие</td>
<td>Получает таблицы сведений о программе (PSI) из транспортного потока MPEG-2 и извлекает сведения о программе.</td>
<td>стрмбасе. lib</td>
</tr>
<tr class="even">
<td><a href="dump-filter-sample.md">Образец фильтра дампа</a></td>
<td>Фильтры, модуль подготовки отчетов</td>
<td>Записывает образцы носителей, получаемые в текстовый файл.</td>
<td>стрмбасе. lib</td>
</tr>
<tr class="odd">
<td>Фильтр Сампвид</td>
<td>Фильтры, модуль подготовки отчетов</td>
<td>Фильтр модуля подготовки отчетов видео.</td>
<td>стрмбасе. lib</td>
</tr>
<tr class="even">
<td><a href="scope-filter-sample.md">Образец фильтра области</a></td>
<td>Фильтры, модуль подготовки отчетов</td>
<td>Отображает звуковые данные как формы Wave.</td>
<td>стрмбасе. lib</td>
</tr>
<tr class="odd">
<td><a href="async-filter-sample.md">Пример асинхронного фильтра</a></td>
<td>Фильтры, источник</td>
<td>Фильтр чтения файлов, поддерживающий последовательное скачивание.</td>
<td>стрмбасе. lib</td>
</tr>
<tr class="even">
<td><a href="ball-filter-sample.md">Образец фильтра шарика</a></td>
<td>Фильтры, источник</td>
<td>Фильтр источников видео, создающий изображение вращающегося шарика.</td>
<td>стрмбасе. lib</td>
</tr>
<tr class="odd">
<td><a href="push-source-filters-sample.md">Пример фильтров источника push-уведомлений</a></td>
<td>Фильтры, источник</td>
<td>Фильтры источников, предоставляющие следующие данные в виде видеопотока: одно растровое изображение, набор точечных рисунков, копия текущего изображения рабочего стола.</td>
<td>стрмбасе. lib</td>
</tr>
<tr class="even">
<td><a href="synth-filter-sample.md">Образец фильтра синтезатора</a></td>
<td>Фильтры, источник</td>
<td>Фильтр источников, который создает звуковые волны. В этом примере демонстрируется построение динамического графа.</td>
<td>стрмбасе. lib</td>
</tr>
<tr class="odd">
<td><a href="ezrgb24-filter-sample.md">Образец фильтра EZRGB24</a></td>
<td>Фильтры, преобразование</td>
<td>Фильтр обработки изображений.</td>
<td>стрмбасе. lib</td>
</tr>
<tr class="even">
<td><a href="gargle-filter-sample.md">Образец фильтра гаргле</a></td>
<td>Фильтры, преобразование</td>
<td>Фильтр звуковых эффектов.</td>
<td>стрмбасе. lib</td>
</tr>
<tr class="odd">
<td><a href="wavdest-filter-sample.md">Образец фильтра Вавдест</a></td>
<td>Фильтры, преобразование</td>
<td>Записывает звуковой поток в WAV-файл.</td>
<td>стрмбасе. lib</td>
</tr>
<tr class="even">
<td><a href="dmoenum-sample.md">Пример Дмоенум</a></td>
<td>Разное</td>
<td>Показывает, как перечислить <a href="directx-media-objects.md">объекты мультимедиа DirectX</a> (дмос).</td>

</tr>
<tr class="odd">
<td><a href="mapper-sample.md">Пример сопоставителя</a></td>
<td>Разное</td>
<td>Показывает, как использовать средство <a href="filter-mapper.md">сопоставления фильтров</a> для поиска фильтров в реестре.</td>

</tr>
<tr class="even">
<td>Пример Сисенум</td>
<td>Разное</td>
<td>Демонстрирует использование <a href="system-device-enumerator.md">перечислителя системных устройств</a> для перечисления устройств и фильтров.</td>

</tr>
<tr class="odd">
<td><a href="cutscene-sample.md">Пример Кутсцене</a></td>
<td>Воспроизведение</td>
<td>Воспроизводит видеофайл в полноэкранном режиме.</td>

</tr>
<tr class="even">
<td>Пример Ддравкскл</td>
<td>Воспроизведение</td>
<td>Воспроизводит видео в полноэкранном режиме с эксклюзивным экраном с помощью интерфейса <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>иддравексклмодевидео</strong></a> в фильтре <a href="overlay-mixer-filter.md">микшера оверлея</a> .</td>

</tr>
<tr class="odd">
<td>Пример Дшовплайер</td>
<td>Воспроизведение</td>
<td>Приложение для воспроизведения видео.</td>

</tr>
<tr class="even">
<td>Пример Еврплайер</td>
<td>Воспроизведение</td>
<td>Демонстрирует использование фильтра Евр DirectShow.
<blockquote>
[!Note]<br />
Требуется Windows Vista или более поздняя версия.
</blockquote>
<br/> <br/> Этот образец доступен в Windows SDK для Windows Server 2008 или более поздней версии.<br/></td>
<td>стрмбасе. lib</td>
</tr>
<tr class="odd">
<td>Пример Texture3D9</td>
<td>Воспроизведение</td>
<td>Рисует видео на текстурной поверхности Microsoft DirectX 9,0.</td>
<td>стрмбасе. lib, пакет SDK DirectX</td>
</tr>
<tr class="even">
<td><a href="ticker-sample.md">Пример использования Tick</a></td>
<td>VMR-9</td>
<td>Использует VMR-9 для смешения видео и текста.</td>

</tr>
<tr class="odd">
<td>Пример VMR9Allocator</td>
<td>VMR-9</td>
<td>Реализует пользовательский распределитель-представление для VMR-9.</td>
<td>стрмбасе. lib</td>
</tr>
<tr class="even">
<td>Пример VMR9Compositor</td>
<td>VMR-9</td>
<td>Реализует пользовательское микшер для VMR-9.</td>

</tr>
<tr class="odd">
<td><a href="vmrplayer-sample.md">Пример Вмрплайер</a></td>
<td>VMR-9</td>
<td>Использует VMR-9 для смешения одного или двух работающих видео и статического изображения.</td>

</tr>
<tr class="even">
<td>Пример водяного знака</td>
<td>VMR-9</td>
<td>Смешивает статическое изображение на видео во время воспроизведения с помощью VMR-9.</td>

</tr>
<tr class="odd">
<td><a href="windowless-sample.md">Пример без окон</a></td>
<td>VMR-9</td>
<td>Демонстрирует режим без окон в VMR-9.</td>

</tr>
</tbody>
</table>



 

## <a name="additional-dependencies"></a>Дополнительные зависимости

Некоторые примеры связаны с библиотекой базовых классов DirectShow. Для построения этих образцов необходимо сначала построить библиотеку базовых классов. Дополнительные сведения см. в разделе [базовые классы DirectShow](directshow-base-classes.md). Для всех примеров фильтров требуется Библиотека базовых классов.

Для некоторых примеров также требуется пакет SDK DirectX в дополнение к Windows SDK. Чтобы создать эти образцы, необходимо установить пакет SDK для DirectX и задать \_ переменную среды% дкссдк dir%, равную пути установки пакета SDK DirectX.

Во многих примерах DirectShow используется набор общих заголовков и исходных файлов, расположенных в \[ корневых примерах пакета SDK директрори \] \\ \\ мультимедиа \\ DirectShow \\ Common. При копировании образца папки в другой каталог следует также скопировать общую папку.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Настройка среды сборки](setting-up-the-build-environment.md)
</dt> </dl>

 

 




