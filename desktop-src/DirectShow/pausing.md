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
# <a name="pausing"></a>Приостановка

Все изменения состояния фильтра должны удерживать блокировку фильтра. В методе **Pause** создайте все необходимые для фильтра ресурсы.


```C++
HRESULT CMyFilter::Pause()
{
    CAutoLock lock_it(m_pLock);

    /* Create filter resources. */

    return CBaseFilter::Pause();
}
```



Метод [**кбасефилтер::P Аусе**](cbasefilter-pause.md) устанавливает правильное состояние фильтра (состояние \_ "приостановлено") и вызывает метод [**кбасепин:: Active**](cbasepin-active.md) для каждого подключенного ПИН-кода в фильтре. **Активный** метод информирует ПИН-код о том, что фильтр стал активным. Если ПИН-код создает ресурсы, переопределите **Активный** метод следующим образом:


```C++
HRESULT CMyInputPin::Active()
{
    // You do not need to hold the filter lock here. It is already held in Pause.

    /* Create pin resources. */

    return CBaseInputPin::Active()
}
```



 

 



