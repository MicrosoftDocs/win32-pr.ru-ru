---
description: Фильтр синтаксического анализатора QuickTime Movie
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: Фильтр синтаксического анализатора QuickTime Movie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a046e143487a1455aeeb125910bbf4452b4f947
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341952"
---
# <a name="quicktime-movie-parser-filter"></a>Фильтр синтаксического анализатора QuickTime Movie

Этот компонент был удален из Windows Vista и более поздних операционных систем. Он доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.

Фильтр синтаксического анализатора QuickTime Movie разделяет данные® Apple® QuickTime в аудио и видео потоки. Он поддерживает QuickTime 2,0 и более ранних версий. Входной ПИН-код подключается к фильтру источника, такому как фильтр [источника асинхронного файла](file-source--async--filter.md) или фильтр [источника файла URL-адреса](file-source--url--filter.md) . Средство синтаксического анализа использует фильтр [AVI распаковки](avi-decompressor-filter.md) или [Qt](qt-decompressor-filter.md) для распаковки файлов QuickTime. Фильтр создает один выходной ПИН-код для потока видео и один выходной ПИН-код для аудиопотока.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Интерфейсы фильтра</td>
<td><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>Иаммедиаконтент</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>ибасефилтер</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей входных закрепления</td>
<td>MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie;</td>
</tr>
<tr class="odd">
<td>Интерфейсы входных закрепления</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей для выходного ПИН-кода</td>
<td><ul>
<li>MEDIATYPE_Video, MEDIASUBTYPE_NULL FORMAT_VideoInfo</li>
<li>MEDIATYPE_Audio, MEDIASUBTYPE_NULL FORMAT_WaveFormatEx</li>
</ul></td>
</tr>
<tr class="odd">
<td>Интерфейсы выходного ПИН-кода</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Фильтровать CLSID</td>
<td>CLSID_QuickTimeParser</td>
</tr>
<tr class="odd">
<td>CLSID страницы свойств</td>
<td>Нет страницы свойств.</td>
</tr>
<tr class="even">
<td>Исполняемый объект</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Заслуживают</a></td>
<td>MERIT_NORMAL</td>
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
</dt> </dl>

 

 



