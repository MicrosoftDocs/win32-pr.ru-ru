---
description: Поставщик экземпляров предоставляет экземпляры одного или нескольких заданных классов.
ms.assetid: d53c3399-cba8-4b5d-8da0-b5a23f94c0ae
ms.tgt_platform: multiple
title: Написание поставщика экземпляров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bddfaa867624bd84cc975d32a8e7b747064d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702464"
---
# <a name="writing-an-instance-provider"></a><span data-ttu-id="02b63-103">Написание поставщика экземпляров</span><span class="sxs-lookup"><span data-stu-id="02b63-103">Writing an Instance Provider</span></span>

<span data-ttu-id="02b63-104">Поставщик экземпляров предоставляет экземпляры одного или нескольких заданных классов.</span><span class="sxs-lookup"><span data-stu-id="02b63-104">An instance provider supplies instances of one or more given classes.</span></span> <span data-ttu-id="02b63-105">Например, поставщик экземпляров может предоставлять сведения о ЦП или оборудовании другого типа.</span><span class="sxs-lookup"><span data-stu-id="02b63-105">For example, an instance provider can supply information regarding a CPU or other type of hardware.</span></span> <span data-ttu-id="02b63-106">Поскольку объекты, управляемые поставщиком экземпляров, обычно меняются на регулярной основе, все поставщики экземпляров считаются поставщиками опрашивающей связи. то есть поставщик, который динамически получает сведения об управляемом объекте всякий раз, когда инструментарий WMI выполняет запрос информации.</span><span class="sxs-lookup"><span data-stu-id="02b63-106">Because the objects managed by an instance provider tend to change on a regular basis, all instance providers are considered pull providers; that is, a provider that dynamically retrieves information regarding a managed object whenever WMI makes a request for the information.</span></span> <span data-ttu-id="02b63-107">Имя берется из идеи, что WMI "извлекает" информацию от поставщика от имени клиентского запроса.</span><span class="sxs-lookup"><span data-stu-id="02b63-107">The name comes from the idea that WMI "pulls" the information from the provider on behalf of a client request.</span></span> <span data-ttu-id="02b63-108">С помощью технологии Pull поставщик экземпляров может поддерживать получение, перечисление, изменение, удаление и обработку запросов конкретного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="02b63-108">Using pull technology, an instance provider can support retrieval, enumeration, modification, deletion, and query processing of a specific instance.</span></span>

<span data-ttu-id="02b63-109">Высокопроизводительные поставщики могут повысить эффективность работы поставщика экземпляров или программно получить доступ к данным, отображаемым в системном мониторе.</span><span class="sxs-lookup"><span data-stu-id="02b63-109">High-performance providers can increase the efficiency of an instance provider or programmatically access the data that appears in System Monitor.</span></span> <span data-ttu-id="02b63-110">Дополнительные сведения см. в разделе [Создание поставщика экземпляров в поставщике High-Performance](making-an-instance-provider-into-a-high-performance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="02b63-110">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md).</span></span>

<span data-ttu-id="02b63-111">В следующей процедуре описывается написание поставщика экземпляров.</span><span class="sxs-lookup"><span data-stu-id="02b63-111">The following procedure describes how to write an instance provider.</span></span>

<span data-ttu-id="02b63-112">**Написание поставщика экземпляров**</span><span class="sxs-lookup"><span data-stu-id="02b63-112">**To write an instance provider**</span></span>

1.  <span data-ttu-id="02b63-113">[Регистрация поставщика в WMI](registering-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="02b63-113">[Register your provider with WMI](registering-an-instance-provider.md).</span></span>

    <span data-ttu-id="02b63-114">Поставщики экземпляров регистрируются в WMI путем создания экземпляра [**\_ \_ Win32Provider**](--win32provider.md) и класса [**\_ \_ инстанцепровидеррегистратион**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="02b63-114">Instance providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and an [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class.</span></span>

2.  <span data-ttu-id="02b63-115">[Инициализируйте поставщик](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="02b63-115">[Initialize your provider](initializing-a-provider.md).</span></span>

    <span data-ttu-id="02b63-116">Инструментарий WMI использует [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) для загрузки и инициализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="02b63-116">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="02b63-117">Это задача, общая для всех поставщиков.</span><span class="sxs-lookup"><span data-stu-id="02b63-117">This is a task common to all providers.</span></span>

    > [!Note]  
    > <span data-ttu-id="02b63-118">Поставщики экземпляров настоятельно рекомендуется использовать модель многопоточности "both".</span><span class="sxs-lookup"><span data-stu-id="02b63-118">Instance providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="02b63-119">[Реализуйте интерфейс IWbemServices для вашего поставщика](implementing-the-primary-interface-for-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="02b63-119">[Implement the IWbemServices interface for your provider](implementing-the-primary-interface-for-an-instance-provider.md).</span></span>

    <span data-ttu-id="02b63-120">Интерфейс [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) является основным интерфейсом для поставщика экземпляров.</span><span class="sxs-lookup"><span data-stu-id="02b63-120">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for an instance provider.</span></span>

4.  <span data-ttu-id="02b63-121">Добавьте дополнительный код, необходимый для поставщика.</span><span class="sxs-lookup"><span data-stu-id="02b63-121">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="02b63-122">При проектировании поставщика вам, скорее всего, придется вызывать интерфейсы WMI.</span><span class="sxs-lookup"><span data-stu-id="02b63-122">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="02b63-123">Дополнительные сведения см. [в разделе Выполнение вызовов к WMI](making-calls-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="02b63-123">For more information, see [Making Calls to WMI](making-calls-to-wmi.md).</span></span>

    <span data-ttu-id="02b63-124">При получении сведений для клиента может потребоваться доступ к уровням безопасности для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="02b63-124">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="02b63-125">Дополнительные сведения см. в разделе [олицетворение клиента](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="02b63-125">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="02b63-126">При необходимости [реализуйте высокопроизводительный интерфейс](improving-the-efficiency-of-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="02b63-126">If necessary, [implement the high-performance interface](improving-the-efficiency-of-an-instance-provider.md).</span></span>

    <span data-ttu-id="02b63-127">Высокопроизводительный интерфейс увеличивает скорость, с которой поставщик может реагировать на запросы из WMI.</span><span class="sxs-lookup"><span data-stu-id="02b63-127">The high-performance interface increases the speed at which the provider can react to requests from WMI.</span></span>

6.  <span data-ttu-id="02b63-128">При необходимости [Реализуйте поддержку частичных обновлений экземпляров](supporting-partial-instance-operations.md).</span><span class="sxs-lookup"><span data-stu-id="02b63-128">If necessary, [implement support for partial-instance updates](supporting-partial-instance-operations.md).</span></span>

    <span data-ttu-id="02b63-129">Как предполагает имя, обновление частичного экземпляра — это метод, который используется для обновления только части экземпляра.</span><span class="sxs-lookup"><span data-stu-id="02b63-129">As the name implies, a partial-instance update is a technique use to update only part of an instance.</span></span> <span data-ttu-id="02b63-130">Дополнительные сведения о вызове частичного экземпляра из клиента см. в разделе [обновление части экземпляра](updating-part-of-an-instance.md) и [получение части экземпляра WMI](retrieving-part-of-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="02b63-130">For more information about calling a partial instance from a client, see [Updating Part of an Instance](updating-part-of-an-instance.md) and [Retrieving Part of a WMI Instance](retrieving-part-of-an-instance.md).</span></span>

7.  <span data-ttu-id="02b63-131">Замените имеющийся поставщик новым кодом.</span><span class="sxs-lookup"><span data-stu-id="02b63-131">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="02b63-132">Вам не нужно выполнять этот шаг, если у вас нет уже существующего поставщика для копирования.</span><span class="sxs-lookup"><span data-stu-id="02b63-132">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="02b63-133">Дополнительные сведения см. [в разделе Обновление поставщика](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="02b63-133">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



