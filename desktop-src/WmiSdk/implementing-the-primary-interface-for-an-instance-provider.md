---
title: Реализация основного интерфейса поставщика экземпляров
description: Поставщик экземпляров использует асинхронные методы IWbemServices в качестве основного интерфейса для WMI.
ms.assetid: 80425fa8-2746-4eba-8e7d-4a61e222852a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443b095cfbb134cf031ae8e1403565bc1fa31aea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712461"
---
# <a name="implementing-an-instance-provider-primary-interface"></a>Реализация основного интерфейса поставщика экземпляров

Поставщик экземпляров использует асинхронные методы [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) в качестве основного интерфейса для WMI. Реализуя только те методы, которые удовлетворяют требованиям поставщика экземпляров, можно уменьшить объем ресурсов, которые вы тратите на написание кода. Однако, реализуя методы, зарезервированные для других типов поставщиков, можно сократить число создаваемых поставщиков.

Поскольку они также используются приложениями и поставщиками для запроса служб WMI, [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) содержит множество методов, не отсущественных для поставщика экземпляров. В следующей таблице перечислены методы **IWbemServices** , которые можно реализовать для поставщика экземпляров.



| Метод                                                                   | Функция          |
|--------------------------------------------------------------------------|------------------|
| [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   | Получения        |
| [**путинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               | Изменение     |
| [**делетеинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)         | Удаление         |
| [**креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) | Перечисление      |
| [**ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   | Обработка запросов |



 

Для методов, которые не используются, поставщик может предоставить реализацию заглушки, которая возвращает **поставщик WBEM \_ E \_ \_ не \_ поддерживает**. Сюда входят все методы [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , не перечисленные в приведенной выше таблице.

Один поставщик может работать одновременно в качестве класса, экземпляра и поставщика метода путем правильной регистрации и реализации всех соответствующих методов. Дополнительные сведения см. в разделе [написание поставщика класса](writing-a-class-provider.md) и [написание поставщика метода](writing-a-method-provider.md).

 

 



