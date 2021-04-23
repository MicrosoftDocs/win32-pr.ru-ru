---
description: Поставщик потребителей событий — это компонент постоянной архитектуры потребителей, который определяет, какой постоянный потребитель событий обрабатывает данное событие.
ms.assetid: c5a0d0ec-99af-4815-9ad2-e59db70e04ce
ms.tgt_platform: multiple
title: Создание поставщика объектов событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c7aeeb9b44b37d887df49cf5049d5a9e59ad72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702463"
---
# <a name="writing-an-event-consumer-provider"></a><span data-ttu-id="c0ee1-103">Создание поставщика объектов событий</span><span class="sxs-lookup"><span data-stu-id="c0ee1-103">Writing an Event Consumer Provider</span></span>

<span data-ttu-id="c0ee1-104">Поставщик потребителей событий — это компонент постоянной архитектуры потребителей, который определяет, какой постоянный потребитель событий обрабатывает данное событие.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-104">An event consumer provider is a component of the permanent consumer architecture that determines which permanent event consumer handles a given event.</span></span> <span data-ttu-id="c0ee1-105">Необходимо создать поставщик потребителей событий вместе с постоянными потребителями событий, чтобы правильно маршрутизировать события из WMI.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-105">You should create an event consumer provider along with your permanent event consumers to route events properly from WMI.</span></span>

<span data-ttu-id="c0ee1-106">Поставщик объектов-получателей событий связывает поставщик событий со списком классов потребителей.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-106">An event consumer provider links an event provider with a list of consumer classes.</span></span> <span data-ttu-id="c0ee1-107">Экземпляры этих классов потребителей затем получают события от этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-107">Instances of these consumer classes then receive events from that provider.</span></span> <span data-ttu-id="c0ee1-108">Инструментарий WMI определяет, в какой поставщик потребителей передаются события, на основе экземпляра [**\_ \_ евентконсумерпровидеррегистратион**](--eventconsumerproviderregistration.md) , который связывает экземпляр [**\_ \_ Win32Provider**](--win32provider.md) поставщика с логическим классом-получателем.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-108">WMI identifies which consumer provider the events are delivered to, based on the [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) instance, which associates the consumer provider [**\_\_Win32Provider**](--win32provider.md) instance with a logical consumer class.</span></span> <span data-ttu-id="c0ee1-109">Пользователи создают экземпляры класса-получателя в рамках постоянной подписки.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-109">Users create instances of the consumer class as part of a permanent subscription.</span></span> <span data-ttu-id="c0ee1-110">Если поставщик событий не выполняется при возникновении события, Инструментарий WMI запускает поставщик, когда ему требуется доставка событий.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-110">If the event provider is not running when an event occurs, then WMI starts the provider when it needs to deliver events.</span></span>

<span data-ttu-id="c0ee1-111">В следующей процедуре описывается реализация поставщика потребителей событий.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-111">The following procedure describes how to implement an event consumer provider.</span></span>

<span data-ttu-id="c0ee1-112">**Реализация поставщика потребителей событий**</span><span class="sxs-lookup"><span data-stu-id="c0ee1-112">**To implement an event consumer provider**</span></span>

1.  <span data-ttu-id="c0ee1-113">Разработка классов потребителей в MOF-файл (MOF) и их регистрация в WMI.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-113">Design consumer classes in Managed Object Format (MOF) and register them with WMI.</span></span> <span data-ttu-id="c0ee1-114">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="c0ee1-114">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

    <span data-ttu-id="c0ee1-115">Поставщики классов регистрируются в WMI путем создания экземпляра [**\_ \_ Win32Provider**](--win32provider.md) и класса [**\_ \_ евентконсумерпровидеррегистратион**](--eventconsumerproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="c0ee1-115">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and an [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) class.</span></span> <span data-ttu-id="c0ee1-116">Дополнительные сведения см. в разделе [Регистрация поставщика потребителей событий](registering-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c0ee1-116">For more information, see [Registering an Event Consumer Provider](registering-an-event-consumer-provider.md).</span></span>

2.  <span data-ttu-id="c0ee1-117">Реализуйте интерфейс [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) для поставщика.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-117">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="c0ee1-118">Инструментарий WMI использует [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) для загрузки и инициализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-118">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="c0ee1-119">Дополнительные сведения см. [в разделе Инициализация поставщика](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c0ee1-119">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="c0ee1-120">Поставщики потребителей событий настоятельно рекомендуется использовать модель многопоточности "both".</span><span class="sxs-lookup"><span data-stu-id="c0ee1-120">Event consumer providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="c0ee1-121">Реализуйте интерфейс [**ивбемевентконсумерпровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) для поставщика.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-121">Implement the [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface for your provider.</span></span>

    <span data-ttu-id="c0ee1-122">Интерфейс [**ивбемевентконсумерпровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) является основным интерфейсом для поставщика потребителей событий.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-122">The [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface is the primary interface for an event consumer provider.</span></span>

4.  <span data-ttu-id="c0ee1-123">Предоставьте одного или нескольких физических потребителей для получения сообщений о событиях из WMI.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-123">Supply one or more physical consumers to receive the event messages from WMI.</span></span>

    <span data-ttu-id="c0ee1-124">Физический потребитель — это COM-объект, представляющий постоянный потребитель событий.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-124">A physical consumer is a COM object that represents a permanent event consumer.</span></span> <span data-ttu-id="c0ee1-125">Все физические потребители должны реализовывать интерфейс [**ивбемунбаундобжектсинк**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) .</span><span class="sxs-lookup"><span data-stu-id="c0ee1-125">All physical consumers must implement the [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) interface.</span></span> <span data-ttu-id="c0ee1-126">Дополнительные сведения см. [в разделе Реализация физического потребителя](implementing-a-physical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="c0ee1-126">For more information, see [Implementing a Physical Consumer](implementing-a-physical-consumer.md).</span></span>

 

 



