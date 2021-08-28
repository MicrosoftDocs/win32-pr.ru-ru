---
description: 'Поставщик метода должен реализовать IWbemServices в качестве основного интерфейса. Однако для чистого поставщика методов требуется только реализация метода IWbemServices:: Ексекмесодасинк.'
ms.assetid: 39466513-48f3-4bf6-a3ab-e9d2c387480c
ms.tgt_platform: multiple
title: Реализация основного интерфейса для поставщика методов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709fcc698155ad0a9e786636045654b08d1cd2b7dfabd946b2d3ee9e8192485
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244234"
---
# <a name="implementing-the-primary-interface-for-a-method-provider"></a>Реализация основного интерфейса для поставщика методов

Поставщик метода должен реализовать [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) в качестве основного интерфейса. Однако для чистого поставщика методов требуется только реализация метода [**IWbemServices:: ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) .

Поскольку другие поставщики используют [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), интерфейс содержит множество методов, не отличных от поставщика чистого метода. Поставщик чистого метода должен предоставить реализацию заглушки, которая возвращает \_ поставщик WBEM E, \_ \_ не \_ поддерживающий все остальные методы **IWbemServices** , кроме [**ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync). Однако многие поставщики методов также служат в качестве поставщиков экземпляров или классов. Методы комбинирования и поставщики экземпляров должны поддерживать больше методов **IWbemServices** .

 

 



