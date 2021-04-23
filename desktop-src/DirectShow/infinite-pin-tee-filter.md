---
description: Фильтр неограниченного ПИН-кода Tee
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Фильтр неограниченного ПИН-кода Tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3433a0c2f5fe55fa59c42ed6e02d34f6e2cf0e6d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909232"
---
# <a name="infinite-pin-tee-filter"></a>Фильтр неограниченного ПИН-кода Tee

Этот фильтр доставляет образцы, доставляемые на входные контакты, в переменное число заголовков выходных данных. При создании экземпляра фильтра он имеет один выходной ПИН-код. Каждый раз при подключении выходного контакта фильтр создает другой выходной ПИН-код. Все выходные сигналы имеют тот же тип носителя, что и входной ПИН-код.

Версия этого фильтра также предоставляется в виде примера пакета SDK. См. [Пример фильтра инфти](inftee-filter-sample.md).



| Метка | Значение |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра                        | [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Типы носителей входных закрепления                    | Любой тип мультимедиа                                                                                                                                     |
| Интерфейсы входных закрепления                     | [**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Типы носителей для выходного ПИН-кода                   | Любой тип мультимедиа. Тип выходных данных всегда соответствует типу входных данных для всех закрепления вывода.                                                                 |
| Интерфейсы выходного ПИН-кода                    | [**Имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Фильтровать CLSID                             | \_ИНФТИ CLSID                                                                                                                                      |
| CLSID страницы свойств                      | Нет страницы свойств                                                                                                                                   |
| Исполняемый объект                               | qcap.dll                                                                                                                                           |
| [Заслуживают](merit.md)                       | \_ \_ не \_ использовать                                                                                                                                |
| [Категория фильтра](filter-categories.md) | \_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID                                                                                                                      |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 



