---
description: Фильтр по источнику файлов (Async)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Фильтр по источнику файлов (Async)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddeea7398ce332a8b1db444b6b74fe3841f9053
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909702"
---
# <a name="file-source-async-filter"></a>Фильтр по источнику файлов (Async)

Фильтр "асинхронный источник файлов" открывает и считывает локальные файлы различных форматов данных и передает их в фильтр анализатора.

Чтобы загрузить файлы мультимедиа из Интернета по протоколу HTTP, используйте фильтр " [источник файлов (URL-адрес)](file-source--url--filter.md) ". Для чтения файлов ASF используйте фильтр [чтения WM ASF](wm-asf-reader-filter.md) .



| Метка | Значение |
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



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 



