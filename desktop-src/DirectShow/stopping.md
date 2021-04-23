---
description: Остановка
ms.assetid: e2796b69-05e5-4ced-b238-257952d81211
title: Остановка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a93bde3b504400eed59190bf1651828f2f4509a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912116"
---
# <a name="stopping"></a><span data-ttu-id="ff901-103">Остановка</span><span class="sxs-lookup"><span data-stu-id="ff901-103">Stopping</span></span>

<span data-ttu-id="ff901-104">Метод " **останавливаться** " должен разблокировать метод **Receive** и отменить фиксацию распределителя фильтра.</span><span class="sxs-lookup"><span data-stu-id="ff901-104">The **Stop** method must unblock the **Receive** method and decommit the filter's allocators.</span></span> <span data-ttu-id="ff901-105">При отсчете распределителя происходит принудительное возвращение всех ожидающих **вызовов метода** noreturn, что разблокирует вышестоящее фильтры, ожидающие выборки.</span><span class="sxs-lookup"><span data-stu-id="ff901-105">Decommitting an allocator forces any pending **GetBuffer** calls to return, which unblocks upstream filters that are waiting for samples.</span></span> <span data-ttu-id="ff901-106">Метод « **Завершение** » удерживает блокировку фильтра, а затем вызывает метод [**Кбасефилтер:: останавливаться**](cbasefilter-stop.md) , который вызывает [**кбасепин:: Inactive**](cbasepin-inactive.md) для всех ПИН-кодов фильтра:</span><span class="sxs-lookup"><span data-stu-id="ff901-106">The **Stop** method holds the filter lock and then calls the [**CBaseFilter::Stop**](cbasefilter-stop.md) method, which calls [**CBasePin::Inactive**](cbasepin-inactive.md) on all of the filter's pins:</span></span>


```C++
HRESULT CMyFilter::Stop()
{
    CAutoLock lock_it(m_pLock);
    // Inactivate all the pins, to protect the filter resources.
    hr = CBaseFilter::Stop();

    /* Safe to destroy filter resources used by the streaming thread. */

    return hr;
}
```



<span data-ttu-id="ff901-107">Переопределите **Неактивный** метод входного контакта следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ff901-107">Override the input pin's **Inactive** method as follows:</span></span>


```C++
HRESULT CMyInputPin::Inactive()
{
    // You do not need to hold the filter lock here. 
    // It is already locked in Stop.

    // Unblock Receive.
    SetEvent(m_hSomeEventThatReceiveNeedsToWaitOn);

    // Make sure Receive will fail. 
    // This also decommits the allocator.
    HRESULT hr = CBaseInputPin::Inactive();

    // Make sure Receive has completed, and is not using resources.
    {
        CAutoLock c(&m_csReceive);

        /* It is now safe to destroy filter resources used by the
           streaming thread. */
    }
    return hr;
}
```



 

 



