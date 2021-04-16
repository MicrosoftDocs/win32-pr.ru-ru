---
description: Фильтр декодера Line 21
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: Фильтр декодера Line 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839a6ff8e77f4815b74f5de65b8f0e2a565cdc2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672957"
---
# <a name="line-21-decoder-filter"></a>Фильтр декодера Line 21

Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

В этой строке 21 фильтр декодера декодировать строку 21 данные и выводит текст заголовка на точечные рисунки.

Входной ПИН-код подключается к любому поставщику данных Line 21 (обычно это видеодекодер DVD или фильтр [декодера CC](cc-decoder-filter.md) ). Декодер CC предоставляет линии 21 данных из ВБИ аналогового телевизионного сигнала. Закрепление вывода подключается к дополнительному ПИН-коду [микшера наложения](overlay-mixer-filter.md) или к другому модулю подготовки видео, например VMR.

Этот фильтр принимает данные строки 21 в стандартном формате пары байтов или для DVD-диска в качестве пакета для всей группы изображений (GOP). Для каждого GOP в видеопотоке DVD может существовать пользовательский пакет данных, содержащий сведения о заголовке конкретного GOP и строку 21 данных. Формат пар байтов определяется в стандарте EIA/CEA-608-B. Дополнительные сведения см. в этом стандарте.

Доступны две версии этого фильтра:



| Фильтр            | CLSID                 |
|-------------------|-----------------------|
| Декодер Line 21   | \_LINE21DECODER CLSID  |
| Line 21 декодер 2 | \_LINE21DECODER2 CLSID |



 

Фильтр версии 1 используется на платформах Microsoft® Windows® 95/98/Me и Windows 2000. Фильтр версии 2 доступен в Microsoft Windows XP и более поздних версиях и используется каждый раз, когда в графе находится модуль подготовки видео.

Сведения в следующей таблице относятся к обеим версиям фильтра:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Интерфейсы фильтра</td>
<td><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>ибасефилтер</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей входных закрепления</td>
<td>Основной тип: MEDIATYPE_AUXLine21DataSubtype:<br/>
<ul>
<li>MEDIASUBTYPE_Line21_BytePair (стандартная строка 21)</li>
<li>MEDIASUBTYPE_Line21_GOPPacket (DVD-строка 21)</li>
</ul>
Тип формата: FORMAT_VideoInfo или GUID_NULL<br/></td>
</tr>
<tr class="odd">
<td>Интерфейсы входных закрепления</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей для выходного ПИН-кода</td>
<td>Основной тип: MEDIATYPE_VideoSubtype:<br/>
<ul>
<li>MEDIASUBTYPE_RGB8</li>
<li>MEDIASUBTYPE_RGB555</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB32</li>
</ul>
Тип формата: FORMAT_VideoInfo<br/></td>
</tr>
<tr class="odd">
<td>Интерфейсы выходного ПИН-кода</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Фильтровать CLSID</td>
<td>См. предыдущую таблицу</td>
</tr>
<tr class="odd">
<td>CLSID страницы свойств</td>
<td>Нет</td>
</tr>
<tr class="even">
<td>Исполняемый объект</td>
<td>qdvd.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Заслуживают</a></td>
<td>Line 21 декодер: MERIT_NORMALLine 21 декодер 2: MERIT_NORMAL + 2<br/></td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Категория фильтра</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> <dt>

[Субтитры и телетекст](closed-captions-and-teletext.md)
</dt> <dt>

[Конфигурация графа фильтра DVD](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




