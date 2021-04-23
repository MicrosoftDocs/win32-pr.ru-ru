---
description: Очистка данных
ms.assetid: 528763a2-c0f2-4981-91dc-dd17987f5bd5
title: Очистка данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ddd052c18928d53511d9e955122d2d66ee59d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805375"
---
# <a name="flushing-data"></a><span data-ttu-id="daaea-103">Очистка данных</span><span class="sxs-lookup"><span data-stu-id="daaea-103">Flushing Data</span></span>

<span data-ttu-id="daaea-104">В следующем псевдокоде показано, как реализовать метод [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) :</span><span class="sxs-lookup"><span data-stu-id="daaea-104">The following pseudocode shows how to implement the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method:</span></span>


```C++
HRESULT CMyInputPin::BeginFlush()
{
    CAutoLock lock_it(m_pLock);
   
    // First, make sure the Receive method will fail from now on.
    HRESULT hr = CBaseInputPin::BeginFlush();
    
    // Force downstream filters to release samples. If our Receive method
    // is blocked in GetBuffer or Deliver, this will unblock it.
    for (each output pin)
    {
        hr = pOutputPin->DeliverBeginFlush();
    }

    // Unblock our Receive method if it is waiting on an event.
    SetEvent(m_hSomeEventThatReceiveNeedsToWaitOn);

    // At this point, the Receive method can't be blocked. Make sure 
    // it finishes, by taking the streaming lock. (Not necessary if this 
    // is the last step.)
    { 
        CAutoLock lock_2(&m_csReceive);

        /* Now it's safe to do anything that would crash or hang 
           if Receive were executing. */
    }
    return hr;
}
```



<span data-ttu-id="daaea-105">Когда начинается запись на диск, метод **бегинфлуш** принимает блокировку фильтра, которая сериализует изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="daaea-105">When flushing starts, the **BeginFlush** method takes the filter lock, which serializes the state change.</span></span> <span data-ttu-id="daaea-106">Блокировка потоковой передачи еще не является защищенной, так как в потоке приложения происходит запись на диск, а поток потоковой передачи может находиться в середине вызова **Receive** .</span><span class="sxs-lookup"><span data-stu-id="daaea-106">It is not yet safe to take the streaming lock, because flushing happens on the application thread, and the streaming thread might be in the middle of a **Receive** call.</span></span> <span data-ttu-id="daaea-107">ПИН-код должен гарантировать, что метод **Receive** не блокируется, и все последующие вызовы **Receive** завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="daaea-107">The pin needs to guarantee that **Receive** is not blocked, and that any subsequent calls to **Receive** will fail.</span></span> <span data-ttu-id="daaea-108">Метод [**кбасеинпутпин:: бегинфлуш**](cbaseinputpin-beginflush.md) задает внутренний флаг, [**кбасеинпутпин:: m \_ бфлушинг**](cbaseinputpin-m-bflushing.md).</span><span class="sxs-lookup"><span data-stu-id="daaea-108">The [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md) method sets an internal flag, [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md).</span></span> <span data-ttu-id="daaea-109">Если флаг имеет **значение true**, метод **Receive** завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="daaea-109">When the flag is **TRUE**, the **Receive** method fails.</span></span>

<span data-ttu-id="daaea-110">Получив вызов **бегинфлуш** , ПИН-код гарантирует, что все нисходящие фильтры выпускают свои примеры и возвращают из вызовов **Receive** .</span><span class="sxs-lookup"><span data-stu-id="daaea-110">By delivering the **BeginFlush** call downstream, the pin guarantees that all downstream filters release their samples and return from **Receive** calls.</span></span> <span data-ttu-id="daaea-111">Это, в свою очередь, гарантирует, что входной ПИН-код не блокируется **в ожидании при** **получении**.</span><span class="sxs-lookup"><span data-stu-id="daaea-111">This in turn guarantees that the input pin is not blocked waiting for **GetBuffer** or **Receive**.</span></span> <span data-ttu-id="daaea-112">Если метод **Receive** вашего ПИН-кода ожидает события (например, для получения ресурсов), метод **бегинфлуш** должен принудительно ожидать завершения, установив событие.</span><span class="sxs-lookup"><span data-stu-id="daaea-112">If your pin's **Receive** method ever waits on an event (for example, to get resources), the **BeginFlush** method should force the wait to terminate by setting the event.</span></span> <span data-ttu-id="daaea-113">На этом этапе гарантированно возвращается метод **Receive** , а флаг **m \_ бфлушинг** предотвращает выполнение новых вызовов **Receive** .</span><span class="sxs-lookup"><span data-stu-id="daaea-113">At this point, the **Receive** method is guaranteed to return, and the **m\_bFlushing** flag prevents new **Receive** calls from doing any work.</span></span>

<span data-ttu-id="daaea-114">Для некоторых фильтров это все, что нужно сделать **бегинфлуш** .</span><span class="sxs-lookup"><span data-stu-id="daaea-114">For some filters, that is all **BeginFlush** needs to do.</span></span> <span data-ttu-id="daaea-115">Метод **ендфлуш** сообщит фильтру, что он может снова начать получать образцы.</span><span class="sxs-lookup"><span data-stu-id="daaea-115">The **EndFlush** method will signal to the filter that it can start receiving samples again.</span></span> <span data-ttu-id="daaea-116">Другим фильтрам может потребоваться использовать переменные или ресурсы в **бегинфлуш** , которые также используются в **Receive**.</span><span class="sxs-lookup"><span data-stu-id="daaea-116">Other filters may need to use variables or resources in **BeginFlush** that are also used in **Receive**.</span></span> <span data-ttu-id="daaea-117">В этом случае фильтр должен сначала сохранить потоковую блокировку.</span><span class="sxs-lookup"><span data-stu-id="daaea-117">In that case, the filter should hold the streaming lock first.</span></span> <span data-ttu-id="daaea-118">Не забудьте сделать это до выполнения какого-либо из описанных выше действий, так как это может привести к взаимоблокировке.</span><span class="sxs-lookup"><span data-stu-id="daaea-118">Be sure not to do this before any of the previous steps, because you might cause a deadlock.</span></span>

<span data-ttu-id="daaea-119">Метод **ендфлуш** удерживает блокировку фильтра и распространяет вызов по нисходящей:</span><span class="sxs-lookup"><span data-stu-id="daaea-119">The **EndFlush** method holds the filter lock and propagates the call downstream:</span></span>


```C++
HRESULT CMyInputPin::EndFlush()
{
    CAutoLock lock_it(m_pLock);
    for (each output pin)
        hr = pOutputPin->DeliverEndFlush();
    return CBaseInputPin::EndFlush();
}
```



<span data-ttu-id="daaea-120">Метод [**кбасеинпутпин:: ендфлуш**](cbaseinputpin-endflush.md) сбрасывает флаг **m \_ бфлушинг** в **значение false**, что позволяет методу **Receive** снова начать получать образцы.</span><span class="sxs-lookup"><span data-stu-id="daaea-120">The [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) method resets the **m\_bFlushing** flag to **FALSE**, which allows the **Receive** method to start receiving samples again.</span></span> <span data-ttu-id="daaea-121">Это должен быть последний шаг в **ендфлуш**, так как ПИН-код не должен получать выборки до тех пор, пока не будет выполнен сброс и не будут уведомлены все нисходящие фильтры.</span><span class="sxs-lookup"><span data-stu-id="daaea-121">This should be the last step in **EndFlush**, because the pin must not receive any samples until flushing is complete and all downstream filters are notified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="daaea-122">См. также</span><span class="sxs-lookup"><span data-stu-id="daaea-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daaea-123">Потоки и критические разделы</span><span class="sxs-lookup"><span data-stu-id="daaea-123">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 



