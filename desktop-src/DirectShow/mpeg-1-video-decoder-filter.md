---
description: Фильтр видеодекодера MPEG-1
ms.assetid: 272d2f31-6e57-4ce5-ac86-b4d47f661fea
title: Фильтр видеодекодера MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec7f48e441226dee33ef949219e8008e15c9d711
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682196"
---
# <a name="mpeg-1-video-decoder-filter"></a>Фильтр видеодекодера MPEG-1

Декодирует видео MPEG-1.



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
<td>MEDIATYPE_Video, FORMAT_MPEGVideo<br/> Допустимы следующие подтипы:<br/>
<ul>
<li><strong>MEDIASUBTYPE_MPEG1Packet</strong></li>
<li><strong>MEDIASUBTYPE_MPEG1Payload</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td>Интерфейсы входных закрепления</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"> <strong>имеминпутпин</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей для выходного ПИН-кода</td>
<td>Основной тип: <strong>MEDIATYPE_Video</strong>,<br/> Тип формата: <strong>FORMAT_VideoInfo</strong> или <strong>FORMAT_VideoInfo2</strong><br/> Подтипы<br/>
<ul>
<li><strong>MEDIASUBTYPE_RGB24</strong></li>
<li><strong>MEDIASUBTYPE_RGB32</strong></li>
<li><strong>MEDIASUBTYPE_RGB8</strong></li>
<li><strong>MEDIASUBTYPE_RGB555</strong></li>
<li><strong>MEDIASUBTYPE_RGB565</strong></li>
<li><strong>MEDIASUBTYPE_UYVY</strong></li>
<li><strong>MEDIASUBTYPE_Y41P</strong></li>
<li><strong>MEDIASUBTYPE_YUY2</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td>Интерфейсы выходного ПИН-кода</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Фильтровать CLSID</td>
<td><strong>CLSID_CMpegVideoCodec</strong></td>
</tr>
<tr class="odd">
<td>CLSID страницы свойств</td>
<td><strong>CLSID_MpegVideoDecodePropertyPage</strong></td>
</tr>
<tr class="even">
<td>Исполняемый объект</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Заслуживают</a></td>
<td>0x40000001</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Категория фильтра</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Комментарии

Этот фильтр может декодировать в поверхность DirectDraw. Фильтр использует технологию MMX, если компьютер поддерживает технологию MMX.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 




