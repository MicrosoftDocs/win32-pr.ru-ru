---
description: Фильтр кодировщика видео DV
ms.assetid: ac57bd11-de16-4a58-9f4b-da270a57ad08
title: Фильтр кодировщика видео DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e14928c937313d056549a348bd255f251354c0ab
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482640"
---
# <a name="dv-video-encoder-filter"></a>Фильтр кодировщика видео DV

Этот фильтр кодирует несжатый видео-поток в цифровое видео (DV). Он предоставляет пользовательский интерфейс [**идвенк**](/windows/desktop/api/Strmif/nn-strmif-idvenc)для настройки разрешения и формата кодирования.




| | | Интерфейсы фильтра | <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>Иамвидеокомпрессион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>идвенк</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <strong>IPersistStream</strong>, <strong>испеЦифипропертипажес</strong> | | Типы входных закрепления <ul><li>Основной тип: MEDIATYPE_VideoThe следующие подтипы являются допустимыми:<br /><ul><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB555</li></ul></li><li>Тип формата: FORMAT_VideoInfo</li></ul> | | Интерфейсы входных закрепления | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | | Типы выходных закрепления <ul><li>Основной тип: MEDIATYPE_Video</li><li>Подтип: MEDIASUBTYPE_dvsd</li><li>Тип формата: FORMAT_VideoInfo</li></ul> | | Интерфейсы выходного ПИН-кода | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | | Фильтровать CLSID | CLSID_DVVideoEnc | | CLSID страницы свойств | CLSID_DVEncPropertiesPage | | Исполняемый файл | qdv.dll | | <a href="merit.md"></a> Кому | MERIT_DO_NOT_USE | | <a href="filter-categories.md">Категория фильтра</a> | CLSID_VideoCompressorCategory | 




 

## <a name="remarks"></a>Комментарии

Для 16-разрядного видео (МЕДИАСУБТИПЕ \_ RGB555 или медиасубтипе \_ RGB565) входное значение должно быть 720 x 480 ПИКСЕЛЕЙ для NTSC или 720 x 576 ПИКСЕЛЕЙ для PAL. Для 24-разрядного видео ограничения на размер входных данных отсутствуют.

Выходные данные всегда 720 x 480 для NTSC или 720 x 576 для PAL; 24-разрядное видео масштабируется в соответствии с этими размерами.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> <dt>

[Цифровое видео в DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




