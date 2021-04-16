---
description: 'Поставщик метода должен реализовать IWbemServices в качестве основного интерфейса. Однако для чистого поставщика методов требуется только реализация метода IWbemServices:: Ексекмесодасинк.'
ms.assetid: 39466513-48f3-4bf6-a3ab-e9d2c387480c
ms.tgt_platform: multiple
title: Реализация основного интерфейса для поставщика методов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 196f87a6520d92bf18362be88f8cc40e5133dabe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702663"
---
# <a name="implementing-the-primary-interface-for-a-method-provider"></a>Реализация основного интерфейса для поставщика методов

Поставщик метода должен реализовать [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) в качестве основного интерфейса. Однако для чистого поставщика методов требуется только реализация метода [**IWbemServices:: ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) .

Поскольку другие поставщики используют [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), интерфейс содержит множество методов, не отличных от поставщика чистого метода. Поставщик чистого метода должен предоставить реализацию заглушки, которая возвращает \_ поставщик WBEM E, \_ \_ не \_ поддерживающий все остальные методы **IWbemServices** , кроме [**ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync). Однако многие поставщики методов также служат в качестве поставщиков экземпляров или классов. Методы комбинирования и поставщики экземпляров должны поддерживать больше методов **IWbemServices** .

 

 



