---
description: Фильтр сжатия МЖПЕГ
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: Фильтр сжатия МЖПЕГ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02928df4d09b50c0ac152aed99ed87dc6362fb70
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910012"
---
# <a name="mjpeg-compressor-filter"></a>Фильтр сжатия МЖПЕГ

Этот фильтр сжимает несжатый видеопоток, используя сжатие JPEG.



| Метка | Значение |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра                        | [**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**                                                                                                                                                                                             |
| Типы носителей входных закрепления                    | \_устройство MEDIATYPE, медиасубтипе \_ null                                                                                                                                                                                                               |
| Интерфейсы входных закрепления                     | [**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Типы носителей для выходного ПИН-кода                   | МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ мжпг                                                                                                                                                                                                               |
| Интерфейсы выходного ПИН-кода                    | [**Иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Фильтровать CLSID                             | \_МЖПЖЕНК CLSID                                                                                                                                                                                                                                     |
| CLSID страницы свойств                      | Нет страницы свойств                                                                                                                                                                                                                                   |
| Исполняемый объект                               | quartz.dll                                                                                                                                                                                                                                         |
| [Заслуживают](merit.md)                       | \_ \_ не \_ использовать                                                                                                                                                                                                                                |
| [Категория фильтра](filter-categories.md) | \_ВИДЕОКОМПРЕССОРКАТЕГОРИ CLSID                                                                                                                                                                                                                     |



 

## <a name="remarks"></a>Комментарии

Этот фильтр кодирует с помощью подтипа носителя МЕДИАСУБТИПЕ \_ мжпг, соответствующего коду FourCC "мжпг".

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 



