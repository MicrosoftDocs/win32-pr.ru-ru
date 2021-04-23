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
# <a name="implementing-an-instance-provider-primary-interface"></a><span data-ttu-id="5e7c7-103">Реализация основного интерфейса поставщика экземпляров</span><span class="sxs-lookup"><span data-stu-id="5e7c7-103">Implementing an instance provider primary interface</span></span>

<span data-ttu-id="5e7c7-104">Поставщик экземпляров использует асинхронные методы [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) в качестве основного интерфейса для WMI.</span><span class="sxs-lookup"><span data-stu-id="5e7c7-104">An instance provider uses the asynchronous methods of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface to WMI.</span></span> <span data-ttu-id="5e7c7-105">Реализуя только те методы, которые удовлетворяют требованиям поставщика экземпляров, можно уменьшить объем ресурсов, которые вы тратите на написание кода.</span><span class="sxs-lookup"><span data-stu-id="5e7c7-105">By implementing only the methods that fulfill the needs of your instance provider, you can reduce the amount of resources you spend coding.</span></span> <span data-ttu-id="5e7c7-106">Однако, реализуя методы, зарезервированные для других типов поставщиков, можно сократить число создаваемых поставщиков.</span><span class="sxs-lookup"><span data-stu-id="5e7c7-106">However, by implementing methods reserved for other types of providers, you can reduce the number of providers you write.</span></span>

<span data-ttu-id="5e7c7-107">Поскольку они также используются приложениями и поставщиками для запроса служб WMI, [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) содержит множество методов, не отсущественных для поставщика экземпляров.</span><span class="sxs-lookup"><span data-stu-id="5e7c7-107">Because it is also used by applications and providers to request services of WMI, [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) contains many methods that are irrelevant to an instance provider.</span></span> <span data-ttu-id="5e7c7-108">В следующей таблице перечислены методы **IWbemServices** , которые можно реализовать для поставщика экземпляров.</span><span class="sxs-lookup"><span data-stu-id="5e7c7-108">The following table lists the **IWbemServices** methods that you can implement for an instance provider.</span></span>



| <span data-ttu-id="5e7c7-109">Метод</span><span class="sxs-lookup"><span data-stu-id="5e7c7-109">Method</span></span>                                                                   | <span data-ttu-id="5e7c7-110">Функция</span><span class="sxs-lookup"><span data-stu-id="5e7c7-110">Feature</span></span>          |
|--------------------------------------------------------------------------|------------------|
| [<span data-ttu-id="5e7c7-111">**жетобжектасинк**</span><span class="sxs-lookup"><span data-stu-id="5e7c7-111">**GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   | <span data-ttu-id="5e7c7-112">Получения</span><span class="sxs-lookup"><span data-stu-id="5e7c7-112">Retrieval</span></span>        |
| [<span data-ttu-id="5e7c7-113">**путинстанцеасинк**</span><span class="sxs-lookup"><span data-stu-id="5e7c7-113">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               | <span data-ttu-id="5e7c7-114">Изменение</span><span class="sxs-lookup"><span data-stu-id="5e7c7-114">Modification</span></span>     |
| [<span data-ttu-id="5e7c7-115">**делетеинстанцеасинк**</span><span class="sxs-lookup"><span data-stu-id="5e7c7-115">**DeleteInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)         | <span data-ttu-id="5e7c7-116">Удаление</span><span class="sxs-lookup"><span data-stu-id="5e7c7-116">Deletion</span></span>         |
| [<span data-ttu-id="5e7c7-117">**креатеинстанцеенумасинк**</span><span class="sxs-lookup"><span data-stu-id="5e7c7-117">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) | <span data-ttu-id="5e7c7-118">Перечисление</span><span class="sxs-lookup"><span data-stu-id="5e7c7-118">Enumeration</span></span>      |
| [<span data-ttu-id="5e7c7-119">**ексеккуерясинк**</span><span class="sxs-lookup"><span data-stu-id="5e7c7-119">**ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   | <span data-ttu-id="5e7c7-120">Обработка запросов</span><span class="sxs-lookup"><span data-stu-id="5e7c7-120">Query processing</span></span> |



 

<span data-ttu-id="5e7c7-121">Для методов, которые не используются, поставщик может предоставить реализацию заглушки, которая возвращает **поставщик WBEM \_ E \_ \_ не \_ поддерживает**.</span><span class="sxs-lookup"><span data-stu-id="5e7c7-121">For methods that you do not use, your provider can supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE**.</span></span> <span data-ttu-id="5e7c7-122">Сюда входят все методы [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , не перечисленные в приведенной выше таблице.</span><span class="sxs-lookup"><span data-stu-id="5e7c7-122">This includes all [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods not listed in the above table.</span></span>

<span data-ttu-id="5e7c7-123">Один поставщик может работать одновременно в качестве класса, экземпляра и поставщика метода путем правильной регистрации и реализации всех соответствующих методов.</span><span class="sxs-lookup"><span data-stu-id="5e7c7-123">A single provider can act simultaneously as a class, instance, and method provider by proper registration and implementation of all relevant methods.</span></span> <span data-ttu-id="5e7c7-124">Дополнительные сведения см. в разделе [написание поставщика класса](writing-a-class-provider.md) и [написание поставщика метода](writing-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5e7c7-124">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing a Method Provider](writing-a-method-provider.md).</span></span>

 

 



