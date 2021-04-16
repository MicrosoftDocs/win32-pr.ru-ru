---
description: Фильтр синтаксического анализатора волн
ms.assetid: 53a9538d-7a79-40bb-9468-d710eb238925
title: Фильтр синтаксического анализатора волн
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb30465a25ab3a6eef190b5fbecd4a4878c2744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664695"
---
# <a name="wave-parser-filter"></a>Фильтр синтаксического анализатора волн

Фильтр средства синтаксического анализа WAVE анализирует звуковые данные в формате WAV, Au или AIF. Вышестоящий фильтр должен быть фильтром [источника асинхронного файла](file-source--async--filter.md) , фильтром [источников URL-адресов](file-source--url--filter.md) или совместимым сторонним фильтром исходного кода, который содержит звуковые данные WAV. Поток вывода — это звуковые данные, которые можно напрямую подключаться к фильтру рендеринга аудио или к промежуточному фильтру преобразования.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Интерфейсы фильтра</td>
<td><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>Иаммедиаконтент</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>иперсистмедиапропертибаг</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей входных закрепления</td>
<td>Основной тип: MEDIATYPE_StreamThe следующие подтипы являются допустимыми:<br/>
<ul>
<li>MEDIASUBTYPE_AIFF</li>
<li>MEDIASUBTYPE_AU</li>
<li>MEDIASUBTYPE_WAVE</li>
</ul></td>
</tr>
<tr class="odd">
<td>Интерфейсы входных закрепления</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей для выходного ПИН-кода</td>
<td>Основной тип: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM или другой тип сжатия. (См. раздел <a href="audio-subtypes.md"><strong>звуковые подтипы</strong></a>.)<br/> Тип формата: FORMAT_WaveFormatEx<br/></td>
</tr>
<tr class="odd">
<td>Интерфейсы выходного ПИН-кода</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>имедиасикинг</strong></a></td>
</tr>
<tr class="even">
<td>Фильтровать CLSID</td>
<td>{D51BD5A1-7548-11cf-A520-0080C77EF58A}</td>
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
<td>MERIT_UNLIKELY</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Категория фильтра</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Комментарии

Этот фильтр поддерживает следующие типы файлов:

-   ВОЛНА (. wav)
-   AIFF и AIFF-C (. AIF)
-   AU (Au)

Однако он имеет следующие ограничения в аудио формате:

-   Звук должен быть 8-или 16-разрядным линейным PCM.
-   Для файлов AIFF-C звук должен быть распакован, в порядке байтов с обратным порядком (тип сжатия "NONE").

## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 




