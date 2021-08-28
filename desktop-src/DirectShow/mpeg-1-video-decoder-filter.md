---
description: Фильтр видеодекодера MPEG-1
ms.assetid: 272d2f31-6e57-4ce5-ac86-b4d47f661fea
title: Фильтр видеодекодера MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf865d0e8cf45bcbde20a2d5b6f4035a4a17f970
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468231"
---
# <a name="mpeg-1-video-decoder-filter"></a>Фильтр видеодекодера MPEG-1

Декодирует видео MPEG-1.




| | | Интерфейсы фильтра | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, <strong>испеЦифипропертипажес</strong> | | Типы входных закрепления MEDIATYPE_Video, FORMAT_MPEGVideo<br /> Допустимы следующие подтипы:<br /><ul><li><strong>MEDIASUBTYPE_MPEG1Packet</strong></li><li><strong>MEDIASUBTYPE_MPEG1Payload</strong></li></ul> | | Интерфейсы входных закрепления | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a> | | Типы выходных закрепления Основной тип: <strong>MEDIATYPE_Video</strong>,<br /> Тип формата: <strong>FORMAT_VideoInfo</strong> или <strong>FORMAT_VideoInfo2</strong><br /> Подтипы<br /><ul><li><strong>MEDIASUBTYPE_RGB24</strong></li><li><strong>MEDIASUBTYPE_RGB32</strong></li><li><strong>MEDIASUBTYPE_RGB8</strong></li><li><strong>MEDIASUBTYPE_RGB555</strong></li><li><strong>MEDIASUBTYPE_RGB565</strong></li><li><strong>MEDIASUBTYPE_UYVY</strong></li><li><strong>MEDIASUBTYPE_Y41P</strong></li><li><strong>MEDIASUBTYPE_YUY2</strong></li></ul> | | Интерфейсы выходного ПИН-кода | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | | Фильтровать CLSID | <strong>CLSID_CMpegVideoCodec</strong> | | CLSID страницы свойств | <strong>CLSID_MpegVideoDecodePropertyPage</strong> | | Исполняемый файл | quartz.dll | | <a href="merit.md"></a> Кому | 0x40000001 | | <a href="filter-categories.md">Категория фильтра</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Комментарии

Этот фильтр может декодировать в поверхность DirectDraw. Фильтр использует технологию MMX, если компьютер поддерживает технологию MMX.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 




