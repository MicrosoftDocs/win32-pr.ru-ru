---
title: Реализация основного интерфейса поставщика экземпляров
description: Поставщик экземпляров использует асинхронные методы IWbemServices в качестве основного интерфейса для WMI.
ms.assetid: 80425fa8-2746-4eba-8e7d-4a61e222852a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb8157a7b4e9637314eb8bb09cdb34e2d3d1d9c87202e6ad0ea4b08fddd3326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118108558"
---
# <a name="implementing-an-instance-provider-primary-interface"></a>Реализация основного интерфейса поставщика экземпляров

Поставщик экземпляров использует асинхронные методы [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) в качестве основного интерфейса для WMI. Реализуя только те методы, которые удовлетворяют требованиям поставщика экземпляров, можно уменьшить объем ресурсов, которые вы тратите на написание кода. Однако, реализуя методы, зарезервированные для других типов поставщиков, можно сократить число создаваемых поставщиков.

Поскольку они также используются приложениями и поставщиками для запроса служб WMI, [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) содержит множество методов, не отсущественных для поставщика экземпляров. В следующей таблице перечислены методы **IWbemServices** , которые можно реализовать для поставщика экземпляров.



| Метод                                                                   | Компонент          |
|--------------------------------------------------------------------------|------------------|
| [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   | Получения        |
| [**путинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               | Изменение     |
| [**делетеинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)         | Удаление         |
| [**креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) | Перечисление      |
| [**ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   | Обработка запросов |



 

Для методов, которые не используются, поставщик может предоставить реализацию заглушки, которая возвращает **поставщик WBEM \_ E \_ \_ не \_ поддерживает**. Сюда входят все методы [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , не перечисленные в приведенной выше таблице.

Один поставщик может работать одновременно в качестве класса, экземпляра и поставщика метода путем правильной регистрации и реализации всех соответствующих методов. Дополнительные сведения см. в разделе [написание поставщика класса](writing-a-class-provider.md) и [написание поставщика метода](writing-a-method-provider.md).

 

 



