---
description: Удаление всех фильтров в графе
ms.assetid: a11af581-c331-4607-be8b-5f65961bd422
title: Удаление всех фильтров в графе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d414ef7e532eaf5df9143a6b601a57e4a8bd45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805878"
---
# <a name="remove-all-the-filters-in-the-graph"></a>Удаление всех фильтров в графе

Самый простой способ удалить все фильтры в графе фильтра — это просто освободить диспетчер графов фильтров и создать новый. Обязательно выпустите все указатели, которые ваше приложение будет использовать с любыми интерфейсами в диспетчере графов фильтров, а также указатели на объекты в графе, включая фильтры, ПИН-коды, контрольные часы и т. д.

Кроме того, можно удалить фильтры по одному с помощью метода [**ифилтерграф:: ремовефилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) :


```C++
// Stop the graph.
pControl->Stop();

// Enumerate the filters in the graph.
IEnumFilters *pEnum = NULL;
HRESULT hr = pGraph->EnumFilters(&pEnum);
if (SUCCEEDED(hr))
{
    IBaseFilter *pFilter = NULL;
    while (S_OK == pEnum->Next(1, &pFilter, NULL))
     {
         // Remove the filter.
         pGraph->RemoveFilter(pFilter);
         // Reset the enumerator.
         pEnum->Reset();
         pFilter->Release();
    }
    pEnum->Release();
}
```



В этом примере используется метод [**ифилтерграф:: енумфилтерс**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) для перечисления фильтров в графе. Удаление фильтра приводит к тому, что объект перечислителя становится несинхронизированным с графом. Чтобы сбросить перечислитель, используйте метод [**иенумфилтерс:: Reset**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) . В противном случае любой последующий вызов метода [**иенумфилтерс:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) завершится ошибкой.

 

 



