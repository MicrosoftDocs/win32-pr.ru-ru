---
description: .
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: Динамическое распределение памяти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1e868a89714a7f6f1d77f9416515897876c150
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693643"
---
# <a name="dynamic-memory"></a><span data-ttu-id="a64f2-103">Динамическое распределение памяти</span><span class="sxs-lookup"><span data-stu-id="a64f2-103">Dynamic Memory</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="a64f2-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="a64f2-104">Affected Platforms</span></span>

<span data-ttu-id="a64f2-105">**Клиенты (работающие как виртуальные машины)** — Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="a64f2-105">**Clients (running as virtual machines)** - Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="a64f2-106">**Серверы** — Windows Server 2008 R2 Hyper-V SP1</span><span class="sxs-lookup"><span data-stu-id="a64f2-106">**Servers** - Windows Server 2008 R2 Hyper-V SP1</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="a64f2-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="a64f2-107">Feature Impact</span></span>

 <span data-ttu-id="a64f2-108">**Серьезность** — низкая</span><span class="sxs-lookup"><span data-stu-id="a64f2-108">**Severity** - Low</span></span>  
<span data-ttu-id="a64f2-109">**Частота** — высокая</span><span class="sxs-lookup"><span data-stu-id="a64f2-109">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="a64f2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a64f2-110">Description</span></span>

<span data-ttu-id="a64f2-111">На высоком уровне динамическая память Hyper-V является усовершенствованием управления памятью для роли Hyper-V, входящей в состав Windows Server 2008 R2 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a64f2-111">At a high level, Hyper-V Dynamic Memory is a memory management enhancement for the Hyper-V role included in Windows Server 2008 R2 SP1.</span></span> <span data-ttu-id="a64f2-112">Он предназначен для использования в рабочей среде и позволяет клиентам достичь более высоких показателей плотности консолидации и виртуальной машины, одновременно оптимизируя использование памяти на физическом компьютере.</span><span class="sxs-lookup"><span data-stu-id="a64f2-112">It is designed for production use and enables customers to achieve higher consolidation/virtual machine (VM) density ratios while optimizing the memory utilization in the physical machine.</span></span> <span data-ttu-id="a64f2-113">Выделение статического выделения памяти сокращается, и при необходимости выделяется дополнительная память.</span><span class="sxs-lookup"><span data-stu-id="a64f2-113">The static memory allocation is reduced and additional memory is allocated on an as needed basis.</span></span> <span data-ttu-id="a64f2-114">Динамическая память влияет на разработчиков программного обеспечения, желающих обеспечить правильную работу программного обеспечения в среде виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a64f2-114">Dynamic Memory impacts software developers who want to ensure that their software works correctly in a virtual machine environment.</span></span>

## <a name="usage-scenario"></a><span data-ttu-id="a64f2-115">Сценарии использования</span><span class="sxs-lookup"><span data-stu-id="a64f2-115">Usage Scenario</span></span>

<span data-ttu-id="a64f2-116">Существует два сценария использования ключей, в которых динамическая память приходится играть в приложения на стороне главного приложения и на гостевых приложениях.</span><span class="sxs-lookup"><span data-stu-id="a64f2-116">There are two key usage scenarios where Dynamic Memory comes into play, host-side applications and guest-side applications.</span></span>

<span data-ttu-id="a64f2-117">**Приложения на стороне сервера (средства управления)**</span><span class="sxs-lookup"><span data-stu-id="a64f2-117">**Host-side applications (management tools)**</span></span>

<span data-ttu-id="a64f2-118">Старые средства, управляющие новым сервером Windows Server 2008 R2 с пакетом обновления 1 (SP1), не смогут получить доступ к новым параметрам динамическая память.</span><span class="sxs-lookup"><span data-stu-id="a64f2-118">Old tools managing a new Windows Server 2008 R2 SP1 server will not be able to access the new Dynamic Memory settings.</span></span> <span data-ttu-id="a64f2-119">Были разработаны новые API WMI и счетчики производительности для управления новыми параметрами динамическая память для виртуальных машин Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="a64f2-119">New WMI APIs and performance counters have been developed to manage the new Dynamic Memory settings for Hyper-V virtual machines.</span></span> <span data-ttu-id="a64f2-120">Разработчики программного обеспечения, работающие с инструментами управления, должны воспользоваться преимуществами этих API и счетчиков для использования с Windows Server 2008 R2 с пакетом обновления 1 (SP1) с установленной ролью Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="a64f2-120">Software developers working on management tools should take advantage of these APIs and counters for use with Windows Server 2008 R2 SP1 with the Hyper-V role installed.</span></span> <span data-ttu-id="a64f2-121">Сведения об этих новых API-интерфейсах можно найти [в документации по поставщику WMI для Hyper-V на сайте MSDN](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider).</span><span class="sxs-lookup"><span data-stu-id="a64f2-121">Details about these new APIs will be available via [Hyper-V WMI Provider documentation on MSDN](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider).</span></span>

<span data-ttu-id="a64f2-122">**Приложения на стороне гостя**</span><span class="sxs-lookup"><span data-stu-id="a64f2-122">**Guest-side applications**</span></span>

<span data-ttu-id="a64f2-123">Разработчики пишут программное обеспечение для использования внутри виртуальной машины, настроенной на использование динамическая память необходимо помнить, что память системы виртуальной машины больше не является постоянной.</span><span class="sxs-lookup"><span data-stu-id="a64f2-123">Developers writing software for use inside a virtual machine configured to use Dynamic Memory need to keep in mind that VM system memory is no longer constant.</span></span> <span data-ttu-id="a64f2-124">Следовательно, приложение должно освободить память, если она больше не нужна для того, чтобы другие приложения могут воспользоваться этим ресурсом.</span><span class="sxs-lookup"><span data-stu-id="a64f2-124">Consequently, their application should free memory when it is no longer needed to allow other applications to take advantage of the resource.</span></span>

<span data-ttu-id="a64f2-125">Выделение памяти и освобождение ресурсов по-прежнему работают как обычные для пользовательских приложений.</span><span class="sxs-lookup"><span data-stu-id="a64f2-125">Memory allocations and de-allocations continue to work as normal for user applications.</span></span> <span data-ttu-id="a64f2-126">Динамическая память полностью прозрачна для большинства приложений конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="a64f2-126">Dynamic Memory is completely transparent to most end user applications.</span></span> <span data-ttu-id="a64f2-127">Однако если разрабатываемое программное обеспечение использует счетчики производительности памяти на виртуальной машине, необходимо выполнить тщательное тестирование в среде с включенной динамическая память, чтобы гарантировать, что программное обеспечение вносит изменения в учетную запись выделения памяти гостевой операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a64f2-127">However if the software being developed makes use of memory performance counters in the virtual machine then careful testing should be performed in a Dynamic Memory enabled environment to ensure that the software takes the changes that are made to the Guest operating system memory allocation into account.</span></span> <span data-ttu-id="a64f2-128">Доступная память больше не является "статической" с точки зрения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a64f2-128">Available memory is no longer "static" from the virtual machine?s perspective.</span></span>

## <a name="solutions"></a><span data-ttu-id="a64f2-129">Решения</span><span class="sxs-lookup"><span data-stu-id="a64f2-129">Solutions</span></span>

<span data-ttu-id="a64f2-130">Чтобы воспользоваться преимуществами динамическая память, на виртуальных машинах должны быть установлены обновленные службы Integration Services (SP1).</span><span class="sxs-lookup"><span data-stu-id="a64f2-130">Virtual machines must have updated integration services (SP1) installed in order to take advantage of Dynamic Memory.</span></span> <span data-ttu-id="a64f2-131">Убедитесь, что все компьютеры, используемые для управления виртуальными машинами Hyper-V, используют последние версии Windows Server 2008 R2 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a64f2-131">Ensure that all machines used in the management of Hyper-V virtual machines are using the latest Windows Server 2008 R2 SP1 bits.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="a64f2-132">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="a64f2-132">Links to Other Resources</span></span>

-   [<span data-ttu-id="a64f2-133">Блог о динамическая память в блоге по Hyper-V</span><span class="sxs-lookup"><span data-stu-id="a64f2-133">Dynamic Memory Coming To Hyper-V blog</span></span>](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [<span data-ttu-id="a64f2-134">Использование поставщика WMI Hyper-V</span><span class="sxs-lookup"><span data-stu-id="a64f2-134">Using the Hyper-V WMI Provider</span></span>](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a><span data-ttu-id="a64f2-135">Отказ от ответственности</span><span class="sxs-lookup"><span data-stu-id="a64f2-135">Disclaimer</span></span>

<span data-ttu-id="a64f2-136">Информация, содержащаяся в этом документе, относится к предварительной версии программного продукта, которая может быть значительно изменена перед первым коммерческим выпуском.</span><span class="sxs-lookup"><span data-stu-id="a64f2-136">The information contained in this document relates to prerelease software product that may be substantially modified before its first commercial release.</span></span> <span data-ttu-id="a64f2-137">Таким образом, информация может не точнее описывать или отражать программный продукт при первой коммерческой выпуске.</span><span class="sxs-lookup"><span data-stu-id="a64f2-137">Accordingly, the information may not accurately describe or reflect the software product when first commercially released.</span></span> <span data-ttu-id="a64f2-138">Этот документ является исключительно информационным.</span><span class="sxs-lookup"><span data-stu-id="a64f2-138">This document is for informational purposes only.</span></span> <span data-ttu-id="a64f2-139">MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.</span><span class="sxs-lookup"><span data-stu-id="a64f2-139">MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.</span></span>

 

 
