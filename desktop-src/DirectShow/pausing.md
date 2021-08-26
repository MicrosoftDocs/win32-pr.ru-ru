---
description: Приостановка
ms.assetid: 945e1b1a-2557-4be2-bfdb-bb11ac7c3fe8
title: Приостановка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f113bdaa41709055202886112d678c2a1fbb172d99e880ceaafc997817412a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997284"
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



 

 



