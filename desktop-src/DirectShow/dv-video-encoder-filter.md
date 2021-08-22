---
description: Фильтр кодировщика видео DV
ms.assetid: ac57bd11-de16-4a58-9f4b-da270a57ad08
title: Фильтр кодировщика видео DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff676fd5120ad76d2c9e6507f31ded9b8b67541c3d807befc948e7268397fd28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016072"
---
# <a name="dv-video-encoder-filter"></a>Фильтр кодировщика видео DV

Этот фильтр кодирует несжатый видео-поток в цифровое видео (DV). Он предоставляет пользовательский интерфейс [**идвенк**](/windows/desktop/api/Strmif/nn-strmif-idvenc)для настройки разрешения и формата кодирования.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Интерфейсы фильтра</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>Иамвидеокомпрессион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>идвенк</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <strong>IPersistStream</strong>, <strong>испеЦифипропертипажес</strong></td>
</tr>
<tr class="even">
<td>Типы носителей входных закрепления</td>
<td><ul>
<li>Основной тип: MEDIATYPE_VideoThe следующие подтипы являются допустимыми:<br/>
<ul>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB555</li>
</ul></li>
<li>Тип формата: FORMAT_VideoInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Интерфейсы входных закрепления</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей для выходного ПИН-кода</td>
<td><ul>
<li>Основной тип: MEDIATYPE_Video</li>
<li>Подтип: MEDIASUBTYPE_dvsd</li>
<li>Тип формата: FORMAT_VideoInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Интерфейсы выходного ПИН-кода</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Фильтровать CLSID</td>
<td>CLSID_DVVideoEnc</td>
</tr>
<tr class="odd">
<td>CLSID страницы свойств</td>
<td>CLSID_DVEncPropertiesPage</td>
</tr>
<tr class="even">
<td>Исполняемый объект</td>
<td>qdv.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Заслуживают</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Категория фильтра</a></td>
<td>CLSID_VideoCompressorCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Remarks

Для 16-разрядного видео (МЕДИАСУБТИПЕ \_ RGB555 или медиасубтипе \_ RGB565) входное значение должно быть 720 x 480 ПИКСЕЛЕЙ для NTSC или 720 x 576 ПИКСЕЛЕЙ для PAL. Для 24-разрядного видео ограничения на размер входных данных отсутствуют.

Выходные данные всегда 720 x 480 для NTSC или 720 x 576 для PAL; 24-разрядное видео масштабируется в соответствии с этими размерами.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> <dt>

[Цифровое видео в DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




