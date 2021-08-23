---
description: Получение событий
ms.assetid: 18c5892d-7e33-497c-ab7d-d17fea5df17e
title: Получение событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1132b2b0140c86c2be1e7916e8d1de28e231b2eca50596714aaa82346aaf83eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072728"
---
# <a name="retrieving-events"></a>Получение событий

фильтр Graph Manager предоставляет три интерфейса, поддерживающих уведомления о событиях.

-   [**Имедиаевентсинк**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) содержит метод для фильтров для публикации событий.
-   [**Имедиаевент**](/windows/desktop/api/Control/nn-control-imediaevent) содержит методы для получения событий приложениями.
-   [**Имедиаевентекс**](/windows/desktop/api/Control/nn-control-imediaeventex) наследует от и расширяет интерфейс [**имедиаевент**](/windows/desktop/api/Control/nn-control-imediaevent) .

фильтры посылают уведомления о событиях путем вызова метода [**имедиаевентсинк:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) в фильтре Graph Manager. Уведомление о событии состоит из кода события, определяющего тип события, и двух параметров, которые предоставляют дополнительные сведения. В зависимости от кода события параметры могут содержать указатели, коды возврата, время ссылки или другие сведения. Полный список кодов событий и параметров см. в разделе [коды уведомлений о событиях](event-notification-codes.md).

чтобы получить событие из очереди, приложение вызывает метод [**имедиаевент:: четный**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) в фильтре Graph Manager. Этот метод блокируется до тех пор, пока не будет возвращено событие, которое будет возвращаться или пока не истечет указанное время. Если имеется событие в очереди, метод возвращает код события и два параметра события. После вызова **метода** Event приложение всегда должно вызывать метод [**Имедиаевент:: фриевентпарамс**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) , чтобы освободить все ресурсы, связанные с параметрами события. Например, параметр может быть значением **BSTR** , выделенным графом фильтра.

В следующем примере кода показана структура извлечения событий из очереди.


```C++
long evCode;
LONG_PTR param1, param2;
HRESULT hr;
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch(evCode) 
    { 
        // Call application-defined functions for each 
        // type of event that you want to handle.
    } 
    hr = pEvent->FreeEventParams(evCode, param1, param2);
}
```



чтобы переопределить обработку события по умолчанию для фильтра Graph Manager, вызовите метод [**имедиаевент:: канцелдефаулсандлинг**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) с кодом события в качестве параметра. Можно восстановить обработку по умолчанию, вызвав метод [**имедиаевент:: ресторедефаулсандлинг**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) . Если граф фильтра не выполняет обработку по умолчанию для указанного кода события, вызов этих методов не оказывает никакого влияния.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



