---
description: После создания логического потребителя событий и фильтра событий необходимо связать его, который регистрирует логического потребителя для получения уведомлений о событиях, заданных фильтром.
ms.assetid: 2fc3d781-2b93-4e9e-90a1-1b975ab40a01
ms.tgt_platform: multiple
title: Привязка фильтра событий к логическому потребителю
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f44c4b64b98877231b73543d8753c765c3219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912407"
---
# <a name="binding-an-event-filter-with-a-logical-consumer"></a><span data-ttu-id="a410f-103">Привязка фильтра событий к логическому потребителю</span><span class="sxs-lookup"><span data-stu-id="a410f-103">Binding an Event Filter with a Logical Consumer</span></span>

<span data-ttu-id="a410f-104">После создания логического потребителя событий и фильтра событий необходимо связать его, который регистрирует логического потребителя для получения уведомлений о событиях, заданных фильтром.</span><span class="sxs-lookup"><span data-stu-id="a410f-104">After you create the logical event consumer and the event filter you must link them, which registers the logical consumer to receive notification about the events specified by the filter.</span></span>

<span data-ttu-id="a410f-105">Следующая процедура описывает, как привязать фильтр событий к логическому потребителю.</span><span class="sxs-lookup"><span data-stu-id="a410f-105">The following procedure describes how to bind an event filter with a logical consumer.</span></span>

<span data-ttu-id="a410f-106">**Привязка фильтра событий к логическому потребителю**</span><span class="sxs-lookup"><span data-stu-id="a410f-106">**To bind an event filter with a logical consumer**</span></span>

1.  <span data-ttu-id="a410f-107">Создайте экземпляр класса System [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md) в репозитории WMI.</span><span class="sxs-lookup"><span data-stu-id="a410f-107">Create an instance of the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) system class in the WMI repository.</span></span>

    <span data-ttu-id="a410f-108">Класс [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md) является классом ассоциации, который связывает экземпляр фильтра событий и экземпляр логического потребителя с помощью свойств ссылки на **Фильтр** и **потребитель** .</span><span class="sxs-lookup"><span data-stu-id="a410f-108">The [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) class is an association class that links the event filter instance and the logical consumer instance together through the **Filter** and **Consumer** reference properties.</span></span> <span data-ttu-id="a410f-109">Дополнительные сведения см. в разделе [объявление класса ассоциации](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="a410f-109">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

2.  <span data-ttu-id="a410f-110">Задайте свойство **Filter** для экземпляра фильтра.</span><span class="sxs-lookup"><span data-stu-id="a410f-110">Set the **Filter** property to the instance of your filter.</span></span>
3.  <span data-ttu-id="a410f-111">Задайте для свойства **потребителя** экземпляр логического потребителя.</span><span class="sxs-lookup"><span data-stu-id="a410f-111">Set the **Consumer** property to the instance of your logical consumer.</span></span>
4.  <span data-ttu-id="a410f-112">Задайте свойство **деливерсинчронаусли** , чтобы определить нужный тип доставки.</span><span class="sxs-lookup"><span data-stu-id="a410f-112">Set the **DeliverSynchronously** property to determine the type of delivery you want.</span></span>

    <span data-ttu-id="a410f-113">Свойство **деливерсинчронаусли** определяет, когда инструментарий WMI доставляет уведомления о событиях синхронно или асинхронно.</span><span class="sxs-lookup"><span data-stu-id="a410f-113">The **DeliverSynchronously** property determines when WMI delivers event notifications synchronously or asynchronously.</span></span> <span data-ttu-id="a410f-114">Установка этого свойства в **значение true** запрашивает синхронную доставку.</span><span class="sxs-lookup"><span data-stu-id="a410f-114">Setting this property to **TRUE** requests a synchronous delivery.</span></span> <span data-ttu-id="a410f-115">Синхронная доставка используется только в том случае, когда постоянный потребитель может обрабатывать события приблизительно в 100 МКС.</span><span class="sxs-lookup"><span data-stu-id="a410f-115">Use synchronous delivery only when the permanent consumer can process events within approximately 100 microseconds.</span></span>

    > [!Note]  
    > <span data-ttu-id="a410f-116">Поскольку обратный вызов приемника может не возвращаться на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="a410f-116">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="a410f-117">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="a410f-117">For more information, see [Calling a Method](calling-a-method.md).</span></span>

     

5.  <span data-ttu-id="a410f-118">При отмене регистрации потребителя логических событий убедитесь, что вы удалили экземпляр [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="a410f-118">When unregistering your logical event consumer, ensure you delete the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance.</span></span>

    <span data-ttu-id="a410f-119">Каждый экземпляр [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md) представляет регистрацию для конкретного уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="a410f-119">Each [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance represents a registration for a specific event notification.</span></span> <span data-ttu-id="a410f-120">При удалении привязки WMI отключает регистрацию.</span><span class="sxs-lookup"><span data-stu-id="a410f-120">When you delete a binding, WMI deactivates the registration.</span></span> <span data-ttu-id="a410f-121">Возможно, потребуется удалить экземпляры логического потребителя и фильтра событий, чтобы отключить регистрацию в зависимости от реализации.</span><span class="sxs-lookup"><span data-stu-id="a410f-121">You might have to delete the logical consumer and event filter instances to deactivate registration, depending on the implementation.</span></span>

<span data-ttu-id="a410f-122">В следующем примере кода показан экземпляр [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md) , связывающий экземпляр класса [**активескриптевентконсумер**](activescripteventconsumer.md) с конкретным фильтром событий (экземпляр потребителя событий был создан в разделе [Создание логического потребителя](creating-a-logical-consumer.md) , а фильтр событий был создан в разделе [Создание фильтра событий](creating-an-event-filter.md) ).</span><span class="sxs-lookup"><span data-stu-id="a410f-122">The following code example shows you a [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance that associates an instance of an [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class with a specific event filter (the instance of the event consumer was created in the [Creating a Logical Consumer](creating-a-logical-consumer.md) topic, and the event filter was created in the [Creating an Event Filter](creating-an-event-filter.md) topic).</span></span>

``` syntax
instance of __FilterToConsumerBinding
{
    Filter = $FILTER;
    Consumer = $CONSUMER;
    DeliverSynchronously=FALSE;

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

<span data-ttu-id="a410f-123">Два потребителя, [**активескриптевентконсумер**](activescripteventconsumer.md) и [**коммандлинивентконсумер**](commandlineeventconsumer.md), не будут работать, если их создатель не является членом локальной группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="a410f-123">Two consumers, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) and [**CommandLineEventConsumer**](commandlineeventconsumer.md), will not work unless their creator is a member of the local Administrators group.</span></span>

<span data-ttu-id="a410f-124">**:** Когда администратор создает подписку, ее идентификатор безопасности не используется для свойства **креаторсид** , но вместо него используется идентификатор безопасности локальной группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="a410f-124">**:** When an administrator creates a subscription, his SID is not used for the **CreatorSID** property, but the SID of the local Administrators group is used instead.</span></span> <span data-ttu-id="a410f-125">Таким образом, экземпляры могут создаваться разными администраторами, и подписка по-прежнему будет работать.</span><span class="sxs-lookup"><span data-stu-id="a410f-125">Therefore, instances can be created by different administrators and the subscription will still work.</span></span> <span data-ttu-id="a410f-126">Дополнительные сведения см. в статье [безопасное получение событий](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="a410f-126">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="a410f-127">Если фильтр привязан к логическому потребителю, событие записывается с помощью [трассировки событий](/windows/desktop/ETW/event-tracing-portal) для Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="a410f-127">When a filter is bound to a logical consumer the event is recorded by [Event Tracing](/windows/desktop/ETW/event-tracing-portal) for Windows (ETW).</span></span> <span data-ttu-id="a410f-128">Дополнительные сведения см. в разделе [Трассировка действия WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="a410f-128">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a410f-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a410f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a410f-130">Получение событий в любое время</span><span class="sxs-lookup"><span data-stu-id="a410f-130">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

 
