---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 40d26ea1-3081-4afd-8b12-bc6521fad390
ms.tgt_platform: multiple
title: E (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd162feb3936712b396db016de036f78aea35a09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703000"
---
# <a name="e-wmi"></a><span data-ttu-id="dfe37-103">E (WMI)</span><span class="sxs-lookup"><span data-stu-id="dfe37-103">E (WMI)</span></span>

<span data-ttu-id="dfe37-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) E [F](gloss-f.md) G [р](gloss-h.md) [.](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="dfe37-104">[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) E [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="dfe37-105"><span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**класс событий**</span><span class="sxs-lookup"><span data-stu-id="dfe37-105"><span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**event class**</span></span>
</dt> <dd>

<span data-ttu-id="dfe37-106">Класс WMI, с помощью которого *потребители событий* могут подписываться на *запросы событий*.</span><span class="sxs-lookup"><span data-stu-id="dfe37-106">A WMI class that *event consumers* can subscribe to by an *event query*.</span></span> <span data-ttu-id="dfe37-107">Класс сообщает о конкретном типе вхождения.</span><span class="sxs-lookup"><span data-stu-id="dfe37-107">The class reports a specific type of occurrence.</span></span> <span data-ttu-id="dfe37-108">Например, класс [**Win32 \_ процессстоптраце**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) сообщает, что конкретный процесс был остановлен.</span><span class="sxs-lookup"><span data-stu-id="dfe37-108">For example, the [**Win32\_ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) class reports that a specific process has stopped.</span></span>

</dd> <dt>

<span data-ttu-id="dfe37-109"><span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**потребитель событий**</span><span class="sxs-lookup"><span data-stu-id="dfe37-109"><span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**event consumer**</span></span>
</dt> <dd>

<span data-ttu-id="dfe37-110">Объект-получатель уведомлений о том, что произошло данное событие.</span><span class="sxs-lookup"><span data-stu-id="dfe37-110">A recipient of notifications that report an occurrence of an event.</span></span> <span data-ttu-id="dfe37-111">Потребитель событий может быть [*временным*](gloss-t.md) или [*постоянным*](gloss-p.md).</span><span class="sxs-lookup"><span data-stu-id="dfe37-111">An event consumer is either [*temporary*](gloss-t.md) or [*permanent*](gloss-p.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfe37-112"><span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**Поставщик потребителей событий**</span><span class="sxs-lookup"><span data-stu-id="dfe37-112"><span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**event consumer provider**</span></span>
</dt> <dd>

<span data-ttu-id="dfe37-113">Поставщик, определяющий, какой постоянный объект-получатель события обрабатывает данное событие.</span><span class="sxs-lookup"><span data-stu-id="dfe37-113">A provider that determines which permanent event consumer handles a given event.</span></span> <span data-ttu-id="dfe37-114">Поставщик объекта-получателя событий регистрируется в инструментарии WMI экземпляром [**\_ \_ евентконсумерпровидеррегистратион**](--eventconsumerproviderregistration.md), который содержит список логических классов [*потребителей*](gloss-l.md) , поддерживаемых поставщиком объектов-получателей событий.</span><span class="sxs-lookup"><span data-stu-id="dfe37-114">An event consumer provider is registered with WMI by an instance of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md), which contains a list of the [*logical consumer*](gloss-l.md) classes that the event consumer provider supports.</span></span> <span data-ttu-id="dfe37-115">Поставщик потребителей событий — это сервер COM, который сопоставляет [*физических потребителей*](gloss-p.md) с *логическими потребителями*.</span><span class="sxs-lookup"><span data-stu-id="dfe37-115">An event consumer provider is a COM server that maps [*physical consumers*](gloss-p.md) to *logical consumers*.</span></span> <span data-ttu-id="dfe37-116">Поставщик потребителей событий поддерживает интерфейс [**ивбемевентконсумерпровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) и является компонентом постоянной пользовательской архитектуры.</span><span class="sxs-lookup"><span data-stu-id="dfe37-116">An event consumer provider supports the [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface and is a component of the permanent consumer architecture.</span></span>

</dd> <dt>

<span data-ttu-id="dfe37-117"><span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**фильтр событий**</span><span class="sxs-lookup"><span data-stu-id="dfe37-117"><span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**event filter**</span></span>
</dt> <dd>

<span data-ttu-id="dfe37-118">Экземпляр системного класса [**\_ \_ EventFilter**](--eventfilter.md) , описывающий тип события и условия доставки уведомления.</span><span class="sxs-lookup"><span data-stu-id="dfe37-118">An instance of the [**\_\_EventFilter**](--eventfilter.md) system class that describes an event type and the conditions for delivering a notification.</span></span> <span data-ttu-id="dfe37-119">Потребитель использует фильтр событий для регистрации, чтобы получить уведомление о конкретном типе события.</span><span class="sxs-lookup"><span data-stu-id="dfe37-119">A consumer uses an event filter to register to receive notification of a specific type of event.</span></span>

</dd> <dt>

<span data-ttu-id="dfe37-120"><span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**поставщик событий**</span><span class="sxs-lookup"><span data-stu-id="dfe37-120"><span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**event provider**</span></span>
</dt> <dd>

<span data-ttu-id="dfe37-121">Поставщик WMI, отслеживающий источник событий и уведомляющий Инструментарий WMI о происходящих событиях.</span><span class="sxs-lookup"><span data-stu-id="dfe37-121">A WMI provider that monitors a source of events and notifies WMI when events occur.</span></span> <span data-ttu-id="dfe37-122">Поставщик событий реализует интерфейсы [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) и [**ивбемевентпровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) , а иногда [**ивбемевентпровидеркуерисинк**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).</span><span class="sxs-lookup"><span data-stu-id="dfe37-122">An event provider implements the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) interfaces, and sometimes [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).</span></span>

</dd> <dt>

<span data-ttu-id="dfe37-123"><span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**запрос события**</span><span class="sxs-lookup"><span data-stu-id="dfe37-123"><span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**event query**</span></span>
</dt> <dd>

<span data-ttu-id="dfe37-124">Инструкция [*язык запросов WMI*](gloss-w.md) , используемая потребителями событий для регистрации для получения уведомлений о конкретных событиях.</span><span class="sxs-lookup"><span data-stu-id="dfe37-124">A [*WMI Query Language*](gloss-w.md) statement that event consumers use to register to receive notification of specific events.</span></span> <span data-ttu-id="dfe37-125">Поставщик событий использует запрос событий для регистрации на генерирование уведомлений о событиях определенного типа.</span><span class="sxs-lookup"><span data-stu-id="dfe37-125">An event provider uses an event query to register to generate notifications of specific events.</span></span>

</dd> <dt>

<span data-ttu-id="dfe37-126"><span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**Схема расширения**</span><span class="sxs-lookup"><span data-stu-id="dfe37-126"><span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**extension schema**</span></span>
</dt> <dd>

<span data-ttu-id="dfe37-127">Третий уровень [*схемы CIM*](gloss-c.md), включающий в себя расширения для конкретной платформы схемы CIM, такие как Windows, UNIX и Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="dfe37-127">The third layer of the [*CIM schema*](gloss-c.md), which includes platform-specific extensions of the CIM schema such as Windows, UNIX, and Exchange Server.</span></span> <span data-ttu-id="dfe37-128">См. также [*Общие*](gloss-c.md) модели и модель ядра.</span><span class="sxs-lookup"><span data-stu-id="dfe37-128">Also see [*common model*](gloss-c.md) and core model.</span></span>

</dd> <dt>

<span data-ttu-id="dfe37-129"><span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**внешние события**</span><span class="sxs-lookup"><span data-stu-id="dfe37-129"><span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**extrinsic event**</span></span>
</dt> <dd>

<span data-ttu-id="dfe37-130">Уведомление о событии от поставщика.</span><span class="sxs-lookup"><span data-stu-id="dfe37-130">An event notification from a provider.</span></span> <span data-ttu-id="dfe37-131">Большинство поставщиков создают экземпляр класса событий, определенного в MOF-файлах поставщика.</span><span class="sxs-lookup"><span data-stu-id="dfe37-131">Most providers create an instance of an event class defined in the provider MOF files.</span></span> <span data-ttu-id="dfe37-132">Внешнее событие наследует от [**\_ \_ екстринсицевент**](--extrinsicevent.md).</span><span class="sxs-lookup"><span data-stu-id="dfe37-132">An extrinsic event inherits from [**\_\_ExtrinsicEvent**](--extrinsicevent.md).</span></span> <span data-ttu-id="dfe37-133">Например, [Поставщик журнала событий](/previous-versions/windows/desktop/eventlogprov/event-log-provider) определяет класс событий [**Win32 \_ нтложевент**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span><span class="sxs-lookup"><span data-stu-id="dfe37-133">For example, the [Event Log Provider](/previous-versions/windows/desktop/eventlogprov/event-log-provider) defines the event class [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span> <span data-ttu-id="dfe37-134">См. также [*Внутреннее событие*](gloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="dfe37-134">Also see [*intrinsic event*](gloss-i.md).</span></span>

</dd> </dl>

 

 
