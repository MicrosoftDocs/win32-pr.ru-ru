---
description: Получение и доставка примеров
ms.assetid: 92954b40-1424-4dee-997c-fc41089b7fa5
title: Получение и доставка примеров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364743e0dfc201d419a61fa4c88bde686976d6b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894506"
---
# <a name="receiving-and-delivering-samples"></a><span data-ttu-id="3cfaa-103">Получение и доставка примеров</span><span class="sxs-lookup"><span data-stu-id="3cfaa-103">Receiving and Delivering Samples</span></span>

<span data-ttu-id="3cfaa-104">В следующем псевдокоде показано, как реализовать метод **имеминпут:: Receive** :</span><span class="sxs-lookup"><span data-stu-id="3cfaa-104">The following pseudocode shows how to implement the **IMemInput::Receive** method:</span></span>


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



<span data-ttu-id="3cfaa-105">Метод **Receive** содержит блокировку потоковой передачи, а не блокировку фильтра.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-105">The **Receive** method holds the streaming lock, not the filter lock.</span></span> <span data-ttu-id="3cfaa-106">Фильтру может потребоваться подождать некоторого события, прежде чем он сможет обработать данные, показанные здесь при вызове **WaitForSingleObject**.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-106">The filter might need to wait on some event before it can process the data, shown here by the call to **WaitForSingleObject**.</span></span> <span data-ttu-id="3cfaa-107">Это необходимо сделать не для всех фильтров.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-107">Not every filter will need to do this.</span></span> <span data-ttu-id="3cfaa-108">Метод [**кбасеинпутпин:: Receive**](cbaseinputpin-receive.md) проверяет некоторые общие условия потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-108">The [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method verifies some general streaming conditions.</span></span> <span data-ttu-id="3cfaa-109">Он возвращает \_ \_ неправильное состояние VFW E, \_ Если фильтр остановлен, S \_ false, если фильтр очищается, и т. д.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-109">It returns VFW\_E\_WRONG\_STATE if the filter is stopped, S\_FALSE if the filter is flushing, and so forth.</span></span> <span data-ttu-id="3cfaa-110">Любой код возврата, отличный от S \_ OK, указывает, что метод **Receive** должен возвращать значение немедленно и не обрабатывать этот пример.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-110">Any return code other than S\_OK indicates that the **Receive** method should return immediately and not process the sample.</span></span>

<span data-ttu-id="3cfaa-111">После обработки образца доставьте его в нисходящий фильтр, вызвав [**кбасеаутпутпин::D еливер**](cbaseoutputpin-deliver.md).</span><span class="sxs-lookup"><span data-stu-id="3cfaa-111">After the sample is processed, deliver it to the downstream filter by calling [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md).</span></span> <span data-ttu-id="3cfaa-112">Этот вспомогательный метод вызывает **имеминпутпин:: Receive** на нисходящем входном закрепление.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-112">This helper method calls **IMemInputPin::Receive** on the downstream input pin.</span></span> <span data-ttu-id="3cfaa-113">Фильтр может доставлять образцы на несколько ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-113">A filter might deliver samples to several pins.</span></span>

 

 



