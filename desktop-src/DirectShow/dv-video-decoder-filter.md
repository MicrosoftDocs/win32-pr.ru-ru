---
description: Фильтр видеодекодера DV
ms.assetid: aa47010e-8510-475d-836a-cb63deeb3a7b
title: Фильтр видеодекодера DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f00d63c92da4c16697d7cc9ff173f4c50e822a10da429a586f8eaa688e9eb96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820686"
---
# <a name="dv-video-decoder-filter"></a>Фильтр видеодекодера DV

Этот фильтр декодирует поток цифрового видео (DV) в несжатое видео.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Интерфейсы фильтра</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>иипдвдек</strong></a>, <strong>IPersistStream</strong>, <strong>испеЦифипропертипажес</strong></td>
</tr>
<tr class="even">
<td>Типы носителей входных закрепления</td>
<td><ul>
<li>MEDIATYPE_Video</li>
<li>MEDIASUBTYPE_dvsd</li>
<li>FORMAT_VideoInfo, FORMAT_DvInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Интерфейсы входных закрепления</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей для выходного ПИН-кода</td>
<td><strong>Основной тип</strong>: MEDIATYPE_Video<strong>подтипы</strong>:<br/>
<ul>
<li>MEDIASUBTYPE_YUY2</li>
<li>MEDIASUBTYPE_UYVY</li>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB32</li>
<li>MEDIASUBTYPE_ARGB32</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB555</li>
<li>MEDIASUBTYPE_RGB8</li>
<li>MEDIASUBTYPE_Y41P</li>
</ul>
<strong>Типы форматов</strong>:<br/> Format_VideoInfo, Format_VideoInfo2<br/></td>
</tr>
<tr class="odd">
<td>Интерфейсы выходного ПИН-кода</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Фильтровать CLSID</td>
<td>CLSID_DVVideoCodec</td>
</tr>
<tr class="odd">
<td>CLSID страницы свойств</td>
<td>CLSID_DVDecPropertiesPage</td>
</tr>
<tr class="even">
<td>Исполняемый объект</td>
<td>qdv.dll</td>
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



 

## <a name="remarks"></a>Remarks

Используйте интерфейс [**иипдвдек**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) , чтобы задать разрешение декодирования: полный, половинный размер, квартал или один восьмой размер.

**Чередование**. более ранние версии декодера всегда разменяют чересстрочную развертку видео. Начиная с DirectX 9,0, декодер DV video может сохранить чересстрочную развертку. Это позволяет разрисовать чередование видео с помощью формирователя микширования видео (VMR) для улучшения качества отрисовки. Чтобы использовать эту функцию, нисходящий фильтр должен поддерживать форматы [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , обозначенные этим форматом значения \_ VideoInfo2 в элементе **Форматтипе** структуры [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) . В выходных данных полного разрешения флаги разчередования (**двинтерлаце**) в структуре **VIDEOINFOHEADER2** устанавливаются в значение `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave` , указывающее на поля с чередованием. В половине разрешения или ниже **двинтерлаце** устанавливается равным нулю, что означает последовательные кадры.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> <dt>

[Цифровое видео в DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




