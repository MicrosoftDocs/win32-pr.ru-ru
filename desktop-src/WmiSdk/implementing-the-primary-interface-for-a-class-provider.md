---
description: 'Существует два способа реализации поставщика класса: реализуйте интерфейс в качестве поставщика push-уведомлений или в качестве поставщика извлечения.'
ms.assetid: 2c6d3f73-e219-409b-9347-492035c1eb9f
ms.tgt_platform: multiple
title: Реализация основного интерфейса для поставщика класса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f760dba053cadf56d37445c997fc52a99b242a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346725"
---
# <a name="implementing-the-primary-interface-for-a-class-provider"></a><span data-ttu-id="0072a-103">Реализация основного интерфейса для поставщика класса</span><span class="sxs-lookup"><span data-stu-id="0072a-103">Implementing the Primary Interface for a Class Provider</span></span>

<span data-ttu-id="0072a-104">Существует два способа реализации поставщика класса: реализуйте интерфейс в качестве поставщика push-уведомлений или в качестве поставщика извлечения.</span><span class="sxs-lookup"><span data-stu-id="0072a-104">There are two ways to implement a class provider: implement the interface as a push provider, or as a pull provider.</span></span>

<span data-ttu-id="0072a-105">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="0072a-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="0072a-106">Реализация основного интерфейса для поставщика класса push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="0072a-106">Implementing the Primary Interface for a Push Class Provider</span></span>](#implementing-the-primary-interface-for-a-push-class-provider)
-   [<span data-ttu-id="0072a-107">Реализация основного интерфейса для поставщика опрашивающего класса</span><span class="sxs-lookup"><span data-stu-id="0072a-107">Implementing the Primary Interface for a Pull Class Provider</span></span>](#implementing-the-primary-interface-for-a-pull-class-provider)

## <a name="implementing-the-primary-interface-for-a-push-class-provider"></a><span data-ttu-id="0072a-108">Реализация основного интерфейса для поставщика класса push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="0072a-108">Implementing the Primary Interface for a Push Class Provider</span></span>

<span data-ttu-id="0072a-109">В то время как все поставщики реализуют [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) для инициализации и по крайней мере один другой интерфейс в качестве основного интерфейса, поставщик push-уведомлений реализует только **ивбемпровидеринит**.</span><span class="sxs-lookup"><span data-stu-id="0072a-109">Whereas all providers implement [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) for initialization and at least one other interface as their primary interface, a push provider implements only **IWbemProviderInit**.</span></span>

<span data-ttu-id="0072a-110">Убедитесь, что ваша реализация выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="0072a-110">Ensure that your implementation performs the following tasks:</span></span>

-   <span data-ttu-id="0072a-111">Извлекает соответствующие данные класса.</span><span class="sxs-lookup"><span data-stu-id="0072a-111">Retrieves the appropriate class data.</span></span>
-   <span data-ttu-id="0072a-112">Помещает данные в репозиторий WMI.</span><span class="sxs-lookup"><span data-stu-id="0072a-112">Places the data in the WMI repository.</span></span>
-   <span data-ttu-id="0072a-113">Удаляет устаревшие данные.</span><span class="sxs-lookup"><span data-stu-id="0072a-113">Deletes obsolete data.</span></span>

<span data-ttu-id="0072a-114">После завершения процесса инициализации Инструментарий WMI обрабатывает все запросы приложений для классов, принадлежащих поставщику push-уведомлений, без какого-либо дополнительного взаимодействия с поставщиком.</span><span class="sxs-lookup"><span data-stu-id="0072a-114">After completing the initialization process, WMI handles all application requests for classes belonging to the push provider without any further provider interaction.</span></span> <span data-ttu-id="0072a-115">После этого поставщик push-уведомлений эффективно выступает в качестве клиента инструментария WMI, а не поставщика.</span><span class="sxs-lookup"><span data-stu-id="0072a-115">Afterward, the push provider effectively acts as a client of WMI rather than a provider.</span></span> <span data-ttu-id="0072a-116">Дополнительные сведения о реализации [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit)см. [в разделе Инициализация поставщика](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0072a-116">For more information about implementing [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit), see [Initializing a Provider](initializing-a-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="0072a-117">При вызове инструментария WMI для создания, обновления или удаления данных в поставщике push-уведомлений установите параметр *лфлагс* , чтобы он включал флаг **\_ \_ \_ обновления владельца флага WBEM** во всех вызовах методов [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="0072a-117">When calling WMI to create, update, or remove data in a push provider, set the *lFlags* parameter to include the **WBEM\_FLAG\_OWNER\_UPDATE** flag in all calls to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods.</span></span>

 

## <a name="implementing-the-primary-interface-for-a-pull-class-provider"></a><span data-ttu-id="0072a-118">Реализация основного интерфейса для поставщика опрашивающего класса</span><span class="sxs-lookup"><span data-stu-id="0072a-118">Implementing the Primary Interface for a Pull Class Provider</span></span>

<span data-ttu-id="0072a-119">Поставщик опрашивающего класса должен реализовать [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) в качестве основного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0072a-119">A class pull provider should implement [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface.</span></span> <span data-ttu-id="0072a-120">Интерфейс **IWbemServices** поддерживает получение данных, обновление данных, удаление данных, перечисление и обработку запросов.</span><span class="sxs-lookup"><span data-stu-id="0072a-120">The **IWbemServices** interface supports data retrieval, data update, data removal, enumeration, and query processing.</span></span> <span data-ttu-id="0072a-121">Однако, поскольку служба **IWbemServices** также используется приложениями и поставщиками для запроса служб WMI, **IWbemServices** содержит множество методов, не отсущественных для поставщика класса.</span><span class="sxs-lookup"><span data-stu-id="0072a-121">However, because **IWbemServices** is also used by applications and providers to request services of WMI, **IWbemServices** contains many methods that are irrelevant to a class provider.</span></span> <span data-ttu-id="0072a-122">Ваша реализация должна поддерживать извлечение и перечисление классов с помощью методов [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) и [**креатеклассенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) соответственно.</span><span class="sxs-lookup"><span data-stu-id="0072a-122">Your implementation must support class retrieval and enumeration, through the [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) and [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) methods respectively.</span></span> <span data-ttu-id="0072a-123">В следующей таблице перечислены дополнительные асинхронные методы **IWbemServices** , которые можно реализовать для поставщика класса.</span><span class="sxs-lookup"><span data-stu-id="0072a-123">The following table lists the additional asynchronous **IWbemServices** methods that you can implement for a class provider.</span></span>



| <span data-ttu-id="0072a-124">Метод</span><span class="sxs-lookup"><span data-stu-id="0072a-124">Method</span></span>                                                     | <span data-ttu-id="0072a-125">Функция</span><span class="sxs-lookup"><span data-stu-id="0072a-125">Feature</span></span>      |
|------------------------------------------------------------|--------------|
| [<span data-ttu-id="0072a-126">**путинстанцеасинк**</span><span class="sxs-lookup"><span data-stu-id="0072a-126">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) | <span data-ttu-id="0072a-127">Изменение</span><span class="sxs-lookup"><span data-stu-id="0072a-127">Modification</span></span> |
| [<span data-ttu-id="0072a-128">**делетеклассасинк**</span><span class="sxs-lookup"><span data-stu-id="0072a-128">**DeleteClassAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) | <span data-ttu-id="0072a-129">Удаление</span><span class="sxs-lookup"><span data-stu-id="0072a-129">Deletion</span></span>     |



 

> [!Note]  
> <span data-ttu-id="0072a-130">Поскольку обратный вызов приемника может не возвращаться на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="0072a-130">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="0072a-131">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="0072a-131">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="0072a-132">Поставщик класса должен предоставить реализацию заглушки, которая возвращает **\_ поставщик WBEM E, \_ \_ не \_ поддерживающий** все другие методы [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , которые не поддерживают набор функций.</span><span class="sxs-lookup"><span data-stu-id="0072a-132">Your class provider should supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** for all of other [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods that do not support your feature set.</span></span> <span data-ttu-id="0072a-133">В частности, Инструментарий WMI не поддерживает обработку запросов для поставщиков классов.</span><span class="sxs-lookup"><span data-stu-id="0072a-133">Specifically, WMI does not support query processing for class providers.</span></span> <span data-ttu-id="0072a-134">Таким образом, поставщик класса должен возвращать **\_ поставщик WBEM E, \_ \_ не \_ поддерживающий** их реализацию [**IWbemServices:: ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync), присвоить свойству регистрации **куерисуппортлевелс** **значение NULL** или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="0072a-134">As such, a class provider must return **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from their implementation of [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync), set their **QuerySupportLevels** registration property to **NULL**, or both.</span></span>

<span data-ttu-id="0072a-135">Интерфейсы, реализуемые поставщиком классов, очень похожи на интерфейсы для поставщика экземпляров и поставщика методов.</span><span class="sxs-lookup"><span data-stu-id="0072a-135">The interfaces that a class provider implements are very similar to the interfaces for an instance provider and a method provider.</span></span> <span data-ttu-id="0072a-136">Фактически, один поставщик может действовать как все три типа поставщика, реализовав все методы и зарегистрировав их правильно.</span><span class="sxs-lookup"><span data-stu-id="0072a-136">In fact, a single provider can act as all three types of provider by implementing all the methods and registering properly.</span></span>

 

 



