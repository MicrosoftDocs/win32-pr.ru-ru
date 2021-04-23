---
description: Фильтр декомпрессора МЖПЕГ
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Фильтр декомпрессора МЖПЕГ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23a3e3c09d218a83f5243bf6702d3b5fc3ae1c16
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910022"
---
# <a name="mjpeg-decompressor-filter"></a>Фильтр декомпрессора МЖПЕГ

Этот фильтр декодирует видеопоток из изображения перемещения JPEG в несжатое видео. Некоторые цифровые видеокамеры создают поток видео в формате JPEG.



| Метка | Значение |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра                        | [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Типы носителей входных закрепления                    | МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ мжпг                                                                                                               |
| Интерфейсы входных закрепления                     | [**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Типы носителей для выходного ПИН-кода                   | \_устройство MEDIATYPE, медиасубтипе \_ null                                                                                                               |
| Интерфейсы выходного ПИН-кода                    | [**Имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Фильтровать CLSID                             | \_МЖПЕГДЕК CLSID                                                                                                                                    |
| CLSID страницы свойств                      | Нет страницы свойств                                                                                                                                   |
| Исполняемый объект                               | quartz.dll                                                                                                                                         |
| [Заслуживают](merit.md)                       | неуспешный \_ режим                                                                                                                                      |
| [Категория фильтра](filter-categories.md) | \_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID                                                                                                                      |



 

## <a name="remarks"></a>Комментарии

Этот фильтр совместим с видео о перемещении JPEG, в котором используется код FOURCC "МЖПГ". Он не может декодировать другие виды перемещения JPEG. Для этого необходимо использовать фильтр декодера стороннего производителя.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 



