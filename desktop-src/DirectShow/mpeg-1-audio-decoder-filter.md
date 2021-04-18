---
description: Фильтр звукового декодера MPEG-1
ms.assetid: 2f695ac6-7d4b-41a8-b4c5-83fb9d20ab9d
title: Фильтр звукового декодера MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f2c68243544a8c6a77cbd8101c85d68f393c3d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682293"
---
# <a name="mpeg-1-audio-decoder-filter"></a>Фильтр звукового декодера MPEG-1

Декодирует слой MPEG-1 и звук уровня II в PCM.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Интерфейсы фильтра</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, <strong>испеЦифипропертипажес</strong></td>
</tr>
<tr class="even">
<td>Типы носителей входных закрепления</td>
<td>MEDIATYPE_Audio, FORMAT_WaveFormatEx<br/> Допустимы следующие подтипы:<br/>
<ul>
<li>MEDIASUBTYPE_MPEG1Packet</li>
<li>MEDIASUBTYPE_MPEG1Payload</li>
<li>MEDIASUBTYPE_MPEG1AudioPayload</li>
<li>GUID_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>Интерфейсы входных закрепления</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей для выходного ПИН-кода</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_PCM</td>
</tr>
<tr class="odd">
<td>Интерфейсы выходного ПИН-кода</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Фильтровать CLSID</td>
<td>CLSID_CMpegAudioCodec</td>
</tr>
<tr class="odd">
<td>CLSID страницы свойств</td>
<td>CLSID_MpegAudioDecoderPropertyPage</td>
</tr>
<tr class="even">
<td>Исполняемый объект</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Заслуживают</a></td>
<td>0x03680001</td>
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

 

 




