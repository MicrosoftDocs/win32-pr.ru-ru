---
description: Фильтр по источнику файлов (Async)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Фильтр по источнику файлов (Async)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403564b751e53f160ab140ac89bfda4fd9576f00
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494988"
---
# <a name="file-source-async-filter"></a>Фильтр по источнику файлов (Async)

Фильтр "асинхронный источник файлов" открывает и считывает локальные файлы различных форматов данных и передает их в фильтр анализатора.

Чтобы загрузить файлы мультимедиа из Интернета по протоколу HTTP, используйте фильтр " [источник файлов (URL-адрес)](file-source--url--filter.md) ". Для чтения файлов ASF используйте фильтр [чтения WM ASF](wm-asf-reader-filter.md) .



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра                        | [**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **ифилесаурцефилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)                                                   |
| Типы носителей входных закрепления                    | Неприменимо                                                                                                                       |
| Интерфейсы входных закрепления                     | Неприменимо                                                                                                                       |
| Типы носителей для выходного ПИН-кода                   | **MEDIATYPE \_ Stream**. Подтип зависит от формата мультимедиа. (**Медиасубтипе \_ null** , если фильтр не распознает формат.) |
| Интерфейсы выходного ПИН-кода                    | [**Иамасинкреадертиместампскалинг**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| Фильтровать CLSID                             | **\_АСИНКРЕАДЕР CLSID**                                                                                                               |
| CLSID страницы свойств                      | Нет страницы свойств                                                                                                                     |
| Исполняемый объект                               | quartz.dll                                                                                                                           |
| [Заслуживают](merit.md)                       | **\_маловероятно**                                                                                                                  |
| [Категория фильтра](filter-categories.md) | **\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID**                                                                                                    |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 



