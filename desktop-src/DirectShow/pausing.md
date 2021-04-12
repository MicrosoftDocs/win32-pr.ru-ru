---
description: Приостановка
ms.assetid: 945e1b1a-2557-4be2-bfdb-bb11ac7c3fe8
title: Приостановка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07f6f610c3cfac9361e1db40c0fcd37b90645b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140327"
---
# <a name="pausing"></a><span data-ttu-id="aab38-103">Приостановка</span><span class="sxs-lookup"><span data-stu-id="aab38-103">Pausing</span></span>

<span data-ttu-id="aab38-104">Все изменения состояния фильтра должны удерживать блокировку фильтра.</span><span class="sxs-lookup"><span data-stu-id="aab38-104">All filter state changes must hold the filter lock.</span></span> <span data-ttu-id="aab38-105">В методе **Pause** создайте все необходимые для фильтра ресурсы.</span><span class="sxs-lookup"><span data-stu-id="aab38-105">In the **Pause** method, create any resources the filter needs:</span></span>


```C++
HRESULT CMyFilter::Pause()
{
    CAutoLock lock_it(m_pLock);

    /* Create filter resources. */

    return CBaseFilter::Pause();
}
```



<span data-ttu-id="aab38-106">Метод [**кбасефилтер::P Аусе**](cbasefilter-pause.md) устанавливает правильное состояние фильтра (состояние \_ "приостановлено") и вызывает метод [**кбасепин:: Active**](cbasepin-active.md) для каждого подключенного ПИН-кода в фильтре.</span><span class="sxs-lookup"><span data-stu-id="aab38-106">The [**CBaseFilter::Pause**](cbasefilter-pause.md) method sets the correct state on the filter (State\_Paused) and calls the [**CBasePin::Active**](cbasepin-active.md) method on every connected pin in the filter.</span></span> <span data-ttu-id="aab38-107">**Активный** метод информирует ПИН-код о том, что фильтр стал активным.</span><span class="sxs-lookup"><span data-stu-id="aab38-107">The **Active** method informs the pin that the filter has become active.</span></span> <span data-ttu-id="aab38-108">Если ПИН-код создает ресурсы, переопределите **Активный** метод следующим образом:</span><span class="sxs-lookup"><span data-stu-id="aab38-108">If the pin creates resources, override the **Active** method, as follows:</span></span>


```C++
HRESULT CMyInputPin::Active()
{
    // You do not need to hold the filter lock here. It is already held in Pause.

    /* Create pin resources. */

    return CBaseInputPin::Active()
}
```



 

 



