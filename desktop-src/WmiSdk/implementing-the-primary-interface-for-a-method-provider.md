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
# <a name="implementing-the-primary-interface-for-a-method-provider"></a><span data-ttu-id="6ec6c-104">Реализация основного интерфейса для поставщика методов</span><span class="sxs-lookup"><span data-stu-id="6ec6c-104">Implementing the Primary Interface for a Method Provider</span></span>

<span data-ttu-id="6ec6c-105">Поставщик метода должен реализовать [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) в качестве основного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6ec6c-105">A method provider should implement [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface.</span></span> <span data-ttu-id="6ec6c-106">Однако для чистого поставщика методов требуется только реализация метода [**IWbemServices:: ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) .</span><span class="sxs-lookup"><span data-stu-id="6ec6c-106">However, a pure method provider requires only that you implement the [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) method.</span></span>

<span data-ttu-id="6ec6c-107">Поскольку другие поставщики используют [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), интерфейс содержит множество методов, не отличных от поставщика чистого метода.</span><span class="sxs-lookup"><span data-stu-id="6ec6c-107">Because other providers use [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), the interface contains many methods that are irrelevant to a pure method provider.</span></span> <span data-ttu-id="6ec6c-108">Поставщик чистого метода должен предоставить реализацию заглушки, которая возвращает \_ поставщик WBEM E, \_ \_ не \_ поддерживающий все остальные методы **IWbemServices** , кроме [**ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span><span class="sxs-lookup"><span data-stu-id="6ec6c-108">Your pure method provider should supply a stub implementation that returns WBEM\_E\_PROVIDER\_NOT\_CAPABLE for all of other **IWbemServices** methods besides [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span></span> <span data-ttu-id="6ec6c-109">Однако многие поставщики методов также служат в качестве поставщиков экземпляров или классов.</span><span class="sxs-lookup"><span data-stu-id="6ec6c-109">However, many method providers also serve as instance or class providers.</span></span> <span data-ttu-id="6ec6c-110">Методы комбинирования и поставщики экземпляров должны поддерживать больше методов **IWbemServices** .</span><span class="sxs-lookup"><span data-stu-id="6ec6c-110">Combination method and instance providers must support more of the **IWbemServices** methods.</span></span>

 

 



