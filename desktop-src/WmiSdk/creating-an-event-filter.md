---
description: Фильтр событий — это класс WMI, который описывает, какие события WMI доставляют с физическим потребителем.
ms.assetid: c0ce26a4-5ff2-44b4-8550-c7d8ad0ba0f0
ms.tgt_platform: multiple
title: Создание фильтра событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693e4ef2eee5de14550b8efbf25a9b6720d6a8b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713109"
---
# <a name="creating-an-event-filter"></a><span data-ttu-id="54cd3-103">Создание фильтра событий</span><span class="sxs-lookup"><span data-stu-id="54cd3-103">Creating an Event Filter</span></span>

<span data-ttu-id="54cd3-104">Фильтр событий — это класс WMI, который описывает, какие события WMI доставляют с физическим потребителем.</span><span class="sxs-lookup"><span data-stu-id="54cd3-104">An event filter is a WMI class that describes which events WMI delivers to a physical consumer.</span></span> <span data-ttu-id="54cd3-105">Например, фильтр событий может указать инструментарию WMI предоставить потребителю все события управления питанием или все события перезагрузки системы.</span><span class="sxs-lookup"><span data-stu-id="54cd3-105">For example, an event filter can instruct WMI to deliver to a consumer all power management events, or all system reboot events.</span></span> <span data-ttu-id="54cd3-106">Фильтр событий также описывает условия, при которых Инструментарий WMI доставляет события.</span><span class="sxs-lookup"><span data-stu-id="54cd3-106">An event filter also describes the conditions under which WMI delivers the events.</span></span> <span data-ttu-id="54cd3-107">Фильтр событий может указывать внутреннее или внешнее событие. фильтр может ссылаться на события, происходящие в пространстве имен, то есть за исключением пространства имен фильтра.</span><span class="sxs-lookup"><span data-stu-id="54cd3-107">An event filter can specify an intrinsic or extrinsic event; and the filter can refer to events that originate in the namespace—that is, other than the namespace of the filter.</span></span> <span data-ttu-id="54cd3-108">Постоянный потребитель должен иметь тот же [**креаторсид**](--eventconsumer.md) в экземплярах объекта-получателя, фильтра и привязки.</span><span class="sxs-lookup"><span data-stu-id="54cd3-108">The permanent consumer must have the same [**CreatorSID**](--eventconsumer.md) in the consumer, filter, and binding instances.</span></span> <span data-ttu-id="54cd3-109">Дополнительные сведения см. в статье [безопасное получение событий](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="54cd3-109">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="54cd3-110">В следующей процедуре описывается создание фильтра событий.</span><span class="sxs-lookup"><span data-stu-id="54cd3-110">The following procedure describes how to create an event filter.</span></span>

<span data-ttu-id="54cd3-111">**Создание фильтра событий**</span><span class="sxs-lookup"><span data-stu-id="54cd3-111">**To create an event filter**</span></span>

1.  <span data-ttu-id="54cd3-112">Создайте экземпляр класса System [**\_ \_ EventFilter**](--eventfilter.md) WMI.</span><span class="sxs-lookup"><span data-stu-id="54cd3-112">Create an instance of the WMI [**\_\_EventFilter**](--eventfilter.md) system class.</span></span>
2.  <span data-ttu-id="54cd3-113">Создайте уникальный идентификатор для фильтра с помощью свойства **Name** одним из двух способов:</span><span class="sxs-lookup"><span data-stu-id="54cd3-113">Create a unique identifier for your filter with the **Name** property, in one of two ways:</span></span>

    -   <span data-ttu-id="54cd3-114">Используйте частную схему.</span><span class="sxs-lookup"><span data-stu-id="54cd3-114">Use a private scheme.</span></span>

        <span data-ttu-id="54cd3-115">Произвольное именование фильтров событий работает, пока не конфликтуют с другими схемами именования фильтров.</span><span class="sxs-lookup"><span data-stu-id="54cd3-115">Arbitrarily naming your event filters works as long as you do not conflict with other filter naming schemes.</span></span> <span data-ttu-id="54cd3-116">Следует избегать конфликтов имен, так как добавление экземпляра с совпадающим значением **имени** перезаписывает старый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="54cd3-116">You must avoid naming conflicts because adding an instance with a duplicate **Name** value overwrites the old instance.</span></span>

    -   <span data-ttu-id="54cd3-117">Используйте глобальный уникальный идентификатор (GUID).</span><span class="sxs-lookup"><span data-stu-id="54cd3-117">Use a globally unique identifier (GUID).</span></span>

        <span data-ttu-id="54cd3-118">Если оставить **имя** пустым, WMI заполнит **имя** идентификатором GUID.</span><span class="sxs-lookup"><span data-stu-id="54cd3-118">If you leave **Name** empty, WMI fills **Name** with a GUID.</span></span>

3.  <span data-ttu-id="54cd3-119">Опишите тип события, которое нужно фильтровать с помощью свойства **Query** .</span><span class="sxs-lookup"><span data-stu-id="54cd3-119">Describe the type of event you want filtered with the **Query** property.</span></span>

    <span data-ttu-id="54cd3-120">Свойство **Query** содержит запрос язык запросов WMI (WQL), описывающий тип события, для которого необходимо выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="54cd3-120">The **Query** property contains the WMI Query Language (WQL) query that describes the type of event you want filtered.</span></span> <span data-ttu-id="54cd3-121">Вы можете добиться точной фильтрации, используя различные операторы и расширения WQL.</span><span class="sxs-lookup"><span data-stu-id="54cd3-121">You can achieve precise filtering using a variety of operators and extensions to WQL.</span></span>

    <span data-ttu-id="54cd3-122">Событие журнала NT создается при сбое запроса от постоянного потребителя события.</span><span class="sxs-lookup"><span data-stu-id="54cd3-122">An NT Log event is generated when a query from a permanent event consumer fails.</span></span> <span data-ttu-id="54cd3-123">Источник события — WinMgmt, идентификатор события — 10, а тип события — ошибка.</span><span class="sxs-lookup"><span data-stu-id="54cd3-123">The event's source is WinMgmt, the event ID is 10, and the event type is Error.</span></span>

    <span data-ttu-id="54cd3-124">Инструментарий WMI более эффективен при обработке с преточными запросами, чем с широкими запросами.</span><span class="sxs-lookup"><span data-stu-id="54cd3-124">WMI is more efficient at processing restrictive, specific queries than broad queries.</span></span> <span data-ttu-id="54cd3-125">Создавая конкретный запрос, можно избежать ненужного межпроцессного взаимодействия и сетевого трафика.</span><span class="sxs-lookup"><span data-stu-id="54cd3-125">By creating a specific query, you can avoid unnecessary inter-process communication and network traffic.</span></span> <span data-ttu-id="54cd3-126">В случае событий, создаваемых поставщиком, WMI выполняет фильтрацию в процессе обработки поставщику. Это гарантирует, что только события, соответствующие фильтру, потребуют стоимости межпроцессного обмена данными.</span><span class="sxs-lookup"><span data-stu-id="54cd3-126">In cases of events generated by a provider, WMI performs the filtering in process to the provider; this ensures that only events matching the filter incur the interprocess communication cost.</span></span> <span data-ttu-id="54cd3-127">Дополнительные сведения см. в разделе [запрос WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="54cd3-127">For more information, see [Querying WMI](querying-wmi.md).</span></span>

4.  <span data-ttu-id="54cd3-128">Задайте для свойства **куерилангуаже** тип языка запроса, используемого в свойстве **запрос** .</span><span class="sxs-lookup"><span data-stu-id="54cd3-128">Set the **QueryLanguage** property to the type of query language you use in the **Query** property.</span></span>

    <span data-ttu-id="54cd3-129">Вы почти всегда устанавливаете **куерилангуаже** в "WQL".</span><span class="sxs-lookup"><span data-stu-id="54cd3-129">You will almost always set **QueryLanguage** to "WQL".</span></span>

<span data-ttu-id="54cd3-130">В следующем примере кода описывается фильтр событий, который сигнализирует о событии каждый раз, когда инструментарий WMI создает экземпляр класса [**\_ \_ тимеревент**](--timerevent.md) в корневом \\ пространстве имен CIMV2.</span><span class="sxs-lookup"><span data-stu-id="54cd3-130">The following code example describes an event filter that signals an event each time WMI creates an instance of the [**\_\_TimerEvent**](--timerevent.md) class in the root\\cimv2 namespace.</span></span>

``` syntax
instance of __EventFilter as $FILTER
{
    Name = "MyFilterName";
    Query = "select * from __TimerEvent where TimerID=\"MyTimer\"";
    QueryLanguage = "WQL";
    EventNamespace = "\root\cimv2";

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

<span data-ttu-id="54cd3-131">Свойство **евентнамеспаце** указывает пространство имен, из которого происходят события.</span><span class="sxs-lookup"><span data-stu-id="54cd3-131">The **EventNamespace** property specifies the namespace from which the events originate.</span></span> <span data-ttu-id="54cd3-132">Нет необходимости создавать экземпляры фильтров в пространстве имен, где происходят события.</span><span class="sxs-lookup"><span data-stu-id="54cd3-132">You do not have to create an instance of the filters in the namespace where the events originate.</span></span> <span data-ttu-id="54cd3-133">Если пространство имен не указано, Инструментарий WMI создает фильтр в пространстве имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="54cd3-133">If you do not specify the namespace, then WMI creates the filter in the default namespace.</span></span> <span data-ttu-id="54cd3-134">Внутренние классы событий, такие как [**\_ \_ инстанцеоператионевент**](--instanceoperationevent.md) , доступны в каждом пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="54cd3-134">The intrinsic events classes, such as [**\_\_InstanceOperationEvent**](--instanceoperationevent.md) are available in every namespace.</span></span>

<span data-ttu-id="54cd3-135">Чтобы зарегистрировать логического потребителя для уведомлений о событиях, необходимо привязать фильтры событий к логическому потребителю.</span><span class="sxs-lookup"><span data-stu-id="54cd3-135">To register your logical consumer for event notifications, you must bind the event filters to a logical consumer.</span></span> <span data-ttu-id="54cd3-136">Дополнительные сведения см. в разделе [Привязка фильтра событий к логическому потребителю](binding-an-event-filter-with-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="54cd3-136">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

 

 



