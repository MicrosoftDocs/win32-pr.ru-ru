---
description: Инструментарий WMI поддерживает различные модели потоков в зависимости от того, как размещается поставщик, и от типа функций поставщика, таких как класс или свойство.
ms.assetid: cce3faf5-7bfe-46fe-9205-57398ab9dae9
ms.tgt_platform: multiple
title: Выбор правильной регистрации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b66ec0266b5482dcff13a7de05a5bd1414312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712118"
---
# <a name="choosing-correct-registration"></a><span data-ttu-id="aaf21-103">Выбор правильной регистрации</span><span class="sxs-lookup"><span data-stu-id="aaf21-103">Choosing Correct Registration</span></span>

<span data-ttu-id="aaf21-104">Инструментарий WMI поддерживает различные модели потоков в зависимости от того, как размещается поставщик, и от типа функций поставщика, таких как [класс](writing-a-class-provider.md) или [свойство](writing-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="aaf21-104">WMI supports different threading models depending on how the provider is hosted and the type of provider functionality, such as [Class](writing-a-class-provider.md) or [Property](writing-a-property-provider.md).</span></span> <span data-ttu-id="aaf21-105">Например, у [*несвязанных поставщиков*](gloss-d.md) не поддерживаются все типы функций поставщика.</span><span class="sxs-lookup"><span data-stu-id="aaf21-105">For example, [*decoupled providers*](gloss-d.md) do not support all the types of provider functionality.</span></span> <span data-ttu-id="aaf21-106">Дополнительные сведения о различных моделях размещения и их настройке см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="aaf21-106">For more information about different hosting models and how to configure them, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="in-process-providers"></a><span data-ttu-id="aaf21-107">Поставщики In-Process</span><span class="sxs-lookup"><span data-stu-id="aaf21-107">In-Process Providers</span></span>

<span data-ttu-id="aaf21-108">Внутрипроцессный поставщик выполняется в общем хост-процессе Wmiprvse.exe.</span><span class="sxs-lookup"><span data-stu-id="aaf21-108">In-process providers run in a shared host process, Wmiprvse.exe.</span></span> <span data-ttu-id="aaf21-109">Большинство типов внутрипроцессного поставщика используют модель многопотокового подразделения (MTA).</span><span class="sxs-lookup"><span data-stu-id="aaf21-109">Most in-process provider types use the multithreaded apartment (MTA) model.</span></span>

<span data-ttu-id="aaf21-110">Модель MTA поддерживается для следующих типов функций поставщика:</span><span class="sxs-lookup"><span data-stu-id="aaf21-110">The MTA model is supported for the following types of provider functionality:</span></span>

-   [<span data-ttu-id="aaf21-111">Поставщик класса</span><span class="sxs-lookup"><span data-stu-id="aaf21-111">Class Provider</span></span>](writing-a-class-provider.md)
-   [<span data-ttu-id="aaf21-112">Поставщик экземпляров</span><span class="sxs-lookup"><span data-stu-id="aaf21-112">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="aaf21-113">Поставщик метода</span><span class="sxs-lookup"><span data-stu-id="aaf21-113">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="aaf21-114">Поставщик свойств</span><span class="sxs-lookup"><span data-stu-id="aaf21-114">Property Provider</span></span>](writing-a-property-provider.md)
-   [<span data-ttu-id="aaf21-115">Поставщик событий</span><span class="sxs-lookup"><span data-stu-id="aaf21-115">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="aaf21-116">Поставщик потребителей событий</span><span class="sxs-lookup"><span data-stu-id="aaf21-116">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

<span data-ttu-id="aaf21-117">Модель с одним потоком подразделений (STA) поддерживается для некоторых типов функций поставщика:</span><span class="sxs-lookup"><span data-stu-id="aaf21-117">The single-threaded apartment (STA) model is supported for some types of provider functionality:</span></span>

-   [<span data-ttu-id="aaf21-118">Поставщик экземпляров</span><span class="sxs-lookup"><span data-stu-id="aaf21-118">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="aaf21-119">Поставщик метода</span><span class="sxs-lookup"><span data-stu-id="aaf21-119">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="aaf21-120">Поставщик событий</span><span class="sxs-lookup"><span data-stu-id="aaf21-120">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="aaf21-121">Поставщик потребителей событий</span><span class="sxs-lookup"><span data-stu-id="aaf21-121">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

## <a name="out-of-process-providers"></a><span data-ttu-id="aaf21-122">Поставщики вне процесса</span><span class="sxs-lookup"><span data-stu-id="aaf21-122">Out-of-Process Providers</span></span>

<span data-ttu-id="aaf21-123">Поставщики, размещенные на разных узлах общих служб, поддерживают следующие функции поставщика:</span><span class="sxs-lookup"><span data-stu-id="aaf21-123">Providers that are hosted in a different shared service host support the following provider functionality:</span></span>

-   [<span data-ttu-id="aaf21-124">Поставщик класса</span><span class="sxs-lookup"><span data-stu-id="aaf21-124">Class Provider</span></span>](writing-a-class-provider.md)
-   [<span data-ttu-id="aaf21-125">Поставщик экземпляров</span><span class="sxs-lookup"><span data-stu-id="aaf21-125">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="aaf21-126">Поставщик метода</span><span class="sxs-lookup"><span data-stu-id="aaf21-126">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="aaf21-127">Поставщик свойств</span><span class="sxs-lookup"><span data-stu-id="aaf21-127">Property Provider</span></span>](writing-a-property-provider.md)
-   [<span data-ttu-id="aaf21-128">Поставщик событий</span><span class="sxs-lookup"><span data-stu-id="aaf21-128">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="aaf21-129">Поставщик потребителей событий</span><span class="sxs-lookup"><span data-stu-id="aaf21-129">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

<span data-ttu-id="aaf21-130">Дополнительные сведения об узлах общих служб см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="aaf21-130">For more information about shared service hosts, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="decoupled-providers"></a><span data-ttu-id="aaf21-131">Несвязанные поставщики</span><span class="sxs-lookup"><span data-stu-id="aaf21-131">Decoupled Providers</span></span>

<span data-ttu-id="aaf21-132">Отделенные поставщики размещаются в приложении.</span><span class="sxs-lookup"><span data-stu-id="aaf21-132">Decoupled providers are hosted in an application.</span></span> <span data-ttu-id="aaf21-133">Дополнительные сведения см. [в разделе Включение поставщика в приложение](incorporating-a-provider-in-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="aaf21-133">For more information, see [Incorporating a Provider in an Application](incorporating-a-provider-in-an-application.md).</span></span> <span data-ttu-id="aaf21-134">Поставщики, созданные с помощью WMI в платформа .NET Framework, отделены от.</span><span class="sxs-lookup"><span data-stu-id="aaf21-134">Providers created using WMI in the .NET Framework are decoupled.</span></span> <span data-ttu-id="aaf21-135">Несвязанные Поставщики поддерживают следующие функции поставщика:</span><span class="sxs-lookup"><span data-stu-id="aaf21-135">Decoupled providers support the following provider functionality:</span></span>

-   [<span data-ttu-id="aaf21-136">Поставщик экземпляров</span><span class="sxs-lookup"><span data-stu-id="aaf21-136">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="aaf21-137">Поставщик метода</span><span class="sxs-lookup"><span data-stu-id="aaf21-137">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="aaf21-138">Поставщик событий</span><span class="sxs-lookup"><span data-stu-id="aaf21-138">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="aaf21-139">Поставщик потребителей событий</span><span class="sxs-lookup"><span data-stu-id="aaf21-139">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

## <a name="related-topics"></a><span data-ttu-id="aaf21-140">См. также</span><span class="sxs-lookup"><span data-stu-id="aaf21-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaf21-141">Разработка поставщика WMI</span><span class="sxs-lookup"><span data-stu-id="aaf21-141">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="aaf21-142">Размещение и безопасность поставщика</span><span class="sxs-lookup"><span data-stu-id="aaf21-142">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
</dt> </dl>

 

 



