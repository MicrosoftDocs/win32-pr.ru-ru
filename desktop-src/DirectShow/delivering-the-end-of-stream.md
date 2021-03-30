---
description: Доставка конца потока
ms.assetid: 23afdb2e-93b0-4a74-94bd-e38eb82a5995
title: Доставка конца потока
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bd80d186bd62e6360fa1600f4ba970281315aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894210"
---
# <a name="delivering-the-end-of-stream"></a><span data-ttu-id="7b132-103">Доставка конца потока</span><span class="sxs-lookup"><span data-stu-id="7b132-103">Delivering the End of Stream</span></span>

<span data-ttu-id="7b132-104">Когда входной ПИН-код получает уведомление об окончании потока, он распространяет вызов в нисходящем направлении.</span><span class="sxs-lookup"><span data-stu-id="7b132-104">When the input pin receives an end-of-stream notification, it propagates the call downstream.</span></span> <span data-ttu-id="7b132-105">Все нисходящие фильтры, получающие данные из этого ПИН-кода, также должны получать уведомление об окончании потока.</span><span class="sxs-lookup"><span data-stu-id="7b132-105">Any downstream filters that receive data from this input pin should also get the end-of-stream notification.</span></span> <span data-ttu-id="7b132-106">Опять же, переведите блокировку потоковой передачи, а не блокировку фильтра.</span><span class="sxs-lookup"><span data-stu-id="7b132-106">Again, take the streaming lock and not the filter lock.</span></span> <span data-ttu-id="7b132-107">Если фильтр содержит незавершенные данные, которые еще не были доставлены, то перед отправкой уведомления об окончании потока фильтр должен доставлять его.</span><span class="sxs-lookup"><span data-stu-id="7b132-107">If the filter has pending data that was not yet delivered, the filter should deliver it now, before it sends the end-of-stream notification.</span></span> <span data-ttu-id="7b132-108">Он не должен передавать данные после конца потока.</span><span class="sxs-lookup"><span data-stu-id="7b132-108">It should not send any data after the end of the stream.</span></span>


```C++
HRESULT CMyInputPin::EndOfStream()
{
    CAutoLock lock_it(&m_csReceive);

    /* If the pin has not delivered all of the data in the stream 
       (based on what it received previously), do so now.  */

    // Propagate EndOfStream call downstream, via your output pin(s).
    for (each output pin)
    {    
        hr = pOutputPin->DeliverEndOfStream();
    }
    return S_OK;
}
```



<span data-ttu-id="7b132-109">Метод [**кбасеаутпутпин::D еливерендофстреам**](cbaseoutputpin-deliverendofstream.md) вызывает [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) на нисходящем входном закрепление.</span><span class="sxs-lookup"><span data-stu-id="7b132-109">The [**CBaseOutputPin::DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) method calls [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the downstream input pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b132-110">См. также</span><span class="sxs-lookup"><span data-stu-id="7b132-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b132-111">Потоки и критические разделы</span><span class="sxs-lookup"><span data-stu-id="7b132-111">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 



