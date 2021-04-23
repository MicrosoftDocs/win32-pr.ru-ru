---
description: Фильтр источника файлов (URL-адрес)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Фильтр источника файлов (URL-адрес)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ddfa7282adbf5117bd2c52465c6eb30efbd69e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909242"
---
# <a name="file-source-url-filter"></a>Фильтр источника файлов (URL-адрес)

Фильтр источников файлов URL-адресов — это универсальный асинхронный фильтр источника, который работает с любым исходным файлом, который может идентифицироваться по универсальному указателю ресурсов (URL), а основной тип носителя — Stream. Сюда входят файлы AVI, MOV, MPEG и WAV. Для этого требуется, чтобы подчиненный фильтр был синтаксическим анализатором, таким как [Разделитель потока MPEG-1](mpeg-1-stream-splitter-filter.md), [Разделитель AVI](avi-splitter-filter.md)или [средство синтаксического анализа фильмов QuickTime](quicktime-movie-parser-filter.md).



| Метка | Значение |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра                        | [**Иамопенпрогресс**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ифилесаурцефилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)       |
| Типы носителей входных закрепления                    | Неприменимо                                                                                                                       |
| Интерфейсы входных закрепления                     | Неприменимо                                                                                                                       |
| Типы носителей для выходного ПИН-кода                   | \_Поток MEDIATYPE. Подтип зависит от формата мультимедиа. (МЕДИАСУБТИПЕ \_ Значение NULL, если фильтр не распознает формат.)         |
| Интерфейсы выходного ПИН-кода                    | [**Иамасинкреадертиместампскалинг**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| Фильтровать CLSID                             | \_УРЛРЕАДЕР CLSID                                                                                                                     |
| CLSID страницы свойств                      | Нет страницы свойств                                                                                                                     |
| Исполняемый объект                               | quartz.dll                                                                                                                           |
| [Заслуживают](merit.md)                       | \_маловероятно                                                                                                                      |
| [Категория фильтра](filter-categories.md) | \_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID                                                                                                        |



 

## <a name="remarks"></a>Комментарии

Этот фильтр использует URLMon и поддерживает кодовые страницы.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 



