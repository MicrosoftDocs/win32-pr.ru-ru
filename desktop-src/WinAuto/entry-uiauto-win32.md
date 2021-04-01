---
title: Автоматизация пользовательского интерфейса
description: Автоматизация пользовательского интерфейса Майкрософт — это платформа специальных возможностей, которая позволяет приложениям Windows предоставлять и использовать программные сведения о пользовательских интерфейсах (UI).
ms.assetid: 700ca38d-ff40-472b-a95a-11fa94c3bc1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8006c79299cc1f736dc43555968443f634d4a51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890892"
---
# <a name="ui-automation"></a><span data-ttu-id="f22c6-103">Автоматизация пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="f22c6-103">UI Automation</span></span>

<span data-ttu-id="f22c6-104">Автоматизация пользовательского интерфейса Майкрософт — это платформа специальных возможностей, которая позволяет приложениям Windows предоставлять и использовать программные сведения о пользовательских интерфейсах (UI).</span><span class="sxs-lookup"><span data-stu-id="f22c6-104">Microsoft UI Automation is an accessibility framework that enables Windows applications to provide and consume programmatic information about user interfaces (UIs).</span></span> <span data-ttu-id="f22c6-105">Он обеспечивает программный доступ к большинству элементов пользовательского интерфейса на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="f22c6-105">It provides programmatic access to most UI elements on the desktop.</span></span> <span data-ttu-id="f22c6-106">Она позволяет продуктам с поддержкой специальных возможностей, таким как средства чтения с экрана, предоставлять сведения о пользовательском интерфейсе конечным пользователям и управлять пользовательским интерфейсом средствами, отличными от стандартных входных данных.</span><span class="sxs-lookup"><span data-stu-id="f22c6-106">It enables assistive technology products, such as screen readers, to provide information about the UI to end users and to manipulate the UI by means other than standard input.</span></span> <span data-ttu-id="f22c6-107">Модель автоматизации пользовательского интерфейса также позволяет скриптам автоматических тестов взаимодействовать с пользовательским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="f22c6-107">UI Automation also allows automated test scripts to interact with the UI.</span></span>

-   [<span data-ttu-id="f22c6-108">Где применимо</span><span class="sxs-lookup"><span data-stu-id="f22c6-108">Where Applicable</span></span>](#where-applicable)
-   [<span data-ttu-id="f22c6-109">Аудитория разработчика</span><span class="sxs-lookup"><span data-stu-id="f22c6-109">Developer Audience</span></span>](#developer-audience)
-   [<span data-ttu-id="f22c6-110">Требования к времени выполнения</span><span class="sxs-lookup"><span data-stu-id="f22c6-110">Run-Time Requirements</span></span>](#run-time-requirements)
-   [<span data-ttu-id="f22c6-111">Поддержка операционных систем нижнего уровня</span><span class="sxs-lookup"><span data-stu-id="f22c6-111">Support for Down-level Operating Systems</span></span>](#support-for-down-level-operating-systems)

## <a name="where-applicable"></a><span data-ttu-id="f22c6-112">Применение</span><span class="sxs-lookup"><span data-stu-id="f22c6-112">Where Applicable</span></span>

<span data-ttu-id="f22c6-113">Используя автоматизацию пользовательского интерфейса и следующие рекомендации по проектированию, разработчики могут сделать приложения, работающие в среде Windows, более доступными для многих людей с зрением, слухом или нарушениями движения.</span><span class="sxs-lookup"><span data-stu-id="f22c6-113">By using UI Automation and following accessible design practices, developers can make applications running on Windows more accessible to many people with vision, hearing, or motion disabilities.</span></span> <span data-ttu-id="f22c6-114">Кроме того, модель автоматизации пользовательского интерфейса разработана специально для обеспечения надежной функциональности сценариев автоматического тестирования.</span><span class="sxs-lookup"><span data-stu-id="f22c6-114">Also, UI Automation is specifically designed to provide robust functionality for automated testing scenarios.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="f22c6-115">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="f22c6-115">Developer Audience</span></span>

<span data-ttu-id="f22c6-116">Модель автоматизации пользовательского интерфейса разработана для опытных разработчиков C/C++.</span><span class="sxs-lookup"><span data-stu-id="f22c6-116">UI Automation is designed for experienced C/C++ developers.</span></span> <span data-ttu-id="f22c6-117">Как правило, разработчикам нужен умеренный уровень понимания объектов COM и интерфейсов, Юникод и программирования Windows API.</span><span class="sxs-lookup"><span data-stu-id="f22c6-117">In general, developers need a moderate level of understanding about Component Object Model (COM) objects and interfaces, Unicode, and Windows API programming.</span></span>

<span data-ttu-id="f22c6-118">Сведения о модели автоматизации пользовательского интерфейса для управляемого кода см. в разделе [Специальные возможности](/dotnet/framework/ui-automation/) статьи платформа .NET Framework разработчиков MSDN.</span><span class="sxs-lookup"><span data-stu-id="f22c6-118">For information about UI Automation for managed code, please see [Accessibility](/dotnet/framework/ui-automation/) in the .NET Framework Developer's Guide section of MSDN.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="f22c6-119">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="f22c6-119">Run-Time Requirements</span></span>

<span data-ttu-id="f22c6-120">Модель автоматизации пользовательского интерфейса поддерживается в следующих операционных системах: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows 10, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016 и Windows Server 2019.</span><span class="sxs-lookup"><span data-stu-id="f22c6-120">UI Automation is supported on the following operating systems: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows 10, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, and Windows Server 2019.</span></span>

> [!Note]  
> <span data-ttu-id="f22c6-121">Для Windows XP и Windows Server 2003 также требуется Microsoft .NET Framework 3,0.</span><span class="sxs-lookup"><span data-stu-id="f22c6-121">Windows XP and Windows Server 2003 also require Microsoft .NET Framework 3.0.</span></span>

 

## <a name="support-for-down-level-operating-systems"></a><span data-ttu-id="f22c6-122">Поддержка операционных систем нижнего уровня</span><span class="sxs-lookup"><span data-stu-id="f22c6-122">Support for Down-level Operating Systems</span></span>

<span data-ttu-id="f22c6-123">Обновление платформы для Windows Vista — это набор библиотек времени выполнения, позволяющий разработчикам ориентироваться на приложения как в Windows 7, так и в операционных системах нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="f22c6-123">The Platform Update for Windows Vista is a set of run-time libraries that enables developers to target applications to both Windows 7 and down-level operating systems.</span></span> <span data-ttu-id="f22c6-124">Обновление платформы для Windows Server 2008 — это набор библиотек времени выполнения, позволяющий разработчикам ориентироваться на приложения как в Windows Server 2008 R2, так и в предыдущих версиях Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f22c6-124">The Platform Update for Windows Server 2008 is a set of run-time libraries that enables developers to target applications to both Windows Server 2008 R2 and previous versions of Windows Server.</span></span> <span data-ttu-id="f22c6-125">Обновление платформы для Windows Vista и обновление платформы для Windows Server 2008 будут доступны всем клиентам Windows Vista и Windows Server 2008 с помощью Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="f22c6-125">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="f22c6-126">Сторонние приложения, для которых требуется обновление платформы для Windows Vista или обновление платформы для Windows Server 2008, могут иметь Центр обновления Windows определить, установлен ли он. Если это не так, Центр обновления Windows будет скачивать и устанавливать его в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="f22c6-126">Third-party applications that require Platform Update for Windows Vista or Platform Update for Windows Server 2008 can have Windows Update detect whether it is installed; if it is not, Windows Update will download and install it in the background.</span></span>

<span data-ttu-id="f22c6-127">Обновление платформы для Windows Vista и обновление платформы для Windows Server 2008 поддерживают весь набор функций Windows Automation API 3,0 в следующих операционных системах.</span><span class="sxs-lookup"><span data-stu-id="f22c6-127">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 both support the entire Windows Automation API 3.0 feature set on the following operating systems.</span></span>

-   <span data-ttu-id="f22c6-128">Windows XP (на английском языке)</span><span class="sxs-lookup"><span data-stu-id="f22c6-128">Windows XP (English)</span></span> <dl> <span data-ttu-id="f22c6-129">Windows XP Home SP3, x86</span><span class="sxs-lookup"><span data-stu-id="f22c6-129">Windows XP Home SP3 x86</span></span>  
    <span data-ttu-id="f22c6-130">Windows XP Professional SP3, x86</span><span class="sxs-lookup"><span data-stu-id="f22c6-130">Windows XP Professional SP3 x86</span></span>  
    </dl>
-   Windows Server 2003 (English) <dl> <span data-ttu-id="f22c6-131">Windows Server 2003 SP2 (x86 и x64)</span><span class="sxs-lookup"><span data-stu-id="f22c6-131">Windows Server 2003 SP2 (x86 and x64)</span></span>  
    </dl>
-   <span data-ttu-id="f22c6-132">Windows Vista (английский)</span><span class="sxs-lookup"><span data-stu-id="f22c6-132">Windows Vista (English)</span></span> <dl> <span data-ttu-id="f22c6-133">Начальное с пакетом обновления 2 (x86 и x64)</span><span class="sxs-lookup"><span data-stu-id="f22c6-133">Starter SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="f22c6-134">Домашняя расширенная версия 2 (SP2) (x86 и x64)</span><span class="sxs-lookup"><span data-stu-id="f22c6-134">Home Premium SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="f22c6-135">Business SP2 (x86 и x64)</span><span class="sxs-lookup"><span data-stu-id="f22c6-135">Business SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="f22c6-136">Enterprise SP2 (x86 и x64)</span><span class="sxs-lookup"><span data-stu-id="f22c6-136">Enterprise SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="f22c6-137">Ultimate с пакетом обновления 2 (SP2) (x86 и x64)</span><span class="sxs-lookup"><span data-stu-id="f22c6-137">Ultimate SP2 (x86 and x64)</span></span>  
    </dl>
-   <span data-ttu-id="f22c6-138">Windows Server 2008 (английский)</span><span class="sxs-lookup"><span data-stu-id="f22c6-138">Windows Server 2008 (English)</span></span> <dl> <span data-ttu-id="f22c6-139">Windows Server 2008 с пакетом обновления 2 (SP2) (x86 и x64)</span><span class="sxs-lookup"><span data-stu-id="f22c6-139">Windows Server 2008 SP2 (x86 and x64)</span></span>  
    </dl>

<span data-ttu-id="f22c6-140">Дополнительные сведения об обновлениях см. в [статье обновление платформы для Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).</span><span class="sxs-lookup"><span data-stu-id="f22c6-140">For more information about both updates, see [Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f22c6-141">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="f22c6-141">In this section</span></span>

-   [<span data-ttu-id="f22c6-142">Основы модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="f22c6-142">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
-   [<span data-ttu-id="f22c6-143">Рекомендации программиста поставщика модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="f22c6-143">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
-   [<span data-ttu-id="f22c6-144">Руководством программиста клиента автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="f22c6-144">UI Automation Client Programmer's Guide</span></span>](uiauto-clientportal.md)
-   [<span data-ttu-id="f22c6-145">Ссылки</span><span class="sxs-lookup"><span data-stu-id="f22c6-145">Reference</span></span>](entry-uiautocore-ref.md)
-   [<span data-ttu-id="f22c6-146">Примеры</span><span class="sxs-lookup"><span data-stu-id="f22c6-146">Samples</span></span>](samples-entry.md)
-   [<span data-ttu-id="f22c6-147">Приложения</span><span class="sxs-lookup"><span data-stu-id="f22c6-147">Appendixes</span></span>](appendix-entry.md)

 

 