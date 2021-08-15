---
description: Получение и доставка примеров
ms.assetid: 92954b40-1424-4dee-997c-fc41089b7fa5
title: Получение и доставка примеров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e507cb3e20a8fd08c891cca5143f8bbf8c9d4f9a90bad27dc201dd43c43283e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952153"
---
# <a name="receiving-and-delivering-samples"></a>Получение и доставка примеров

В следующем псевдокоде показано, как реализовать метод **имеминпут:: Receive** :


```C++
HRESULT CMyInputPin::Receive(IMediaSample *pSample)
{
    CAutoLock cObjectLock(&m_csReceive);

    // Perhaps the filter needs to wait on something.
    WaitForSingleObject(m_hSomeEventThatReceiveNeedsToWaitOn, INFINITE);

    // Before using resources, make sure it is safe to proceed. Do not
    // continue if the base-class method returns anything besides S_OK.
    hr = CBaseInputPin::Receive(pSample);
    if (hr != S_OK) 
    {
        return hr;
    }

    /* It is safe to use resources allocated in Active and Pause. */

    // Deliver sample(s), via your output pin(s).
    for (each output pin)
        pOutputPin->Deliver(pSample);

    return hr;
}
```



Метод **Receive** содержит блокировку потоковой передачи, а не блокировку фильтра. Фильтру может потребоваться подождать некоторого события, прежде чем он сможет обработать данные, показанные здесь при вызове **WaitForSingleObject**. Это необходимо сделать не для всех фильтров. Метод [**кбасеинпутпин:: Receive**](cbaseinputpin-receive.md) проверяет некоторые общие условия потоковой передачи. Он возвращает \_ \_ неправильное состояние VFW E, \_ Если фильтр остановлен, S \_ false, если фильтр очищается, и т. д. Любой код возврата, отличный от S \_ OK, указывает, что метод **Receive** должен возвращать значение немедленно и не обрабатывать этот пример.

После обработки образца доставьте его в нисходящий фильтр, вызвав [**кбасеаутпутпин::D еливер**](cbaseoutputpin-deliver.md). Этот вспомогательный метод вызывает **имеминпутпин:: Receive** на нисходящем входном закрепление. Фильтр может доставлять образцы на несколько ПИН-кодов.

 

 



