---
description: Включение поддержки Windows 7 для Intel AVX
ms.assetid: fe19e337-3109-42d6-a704-70662ac7c684
title: Включение поддержки Windows 7 для Intel AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1509bac62634c85aa733b2c1de0c152169ac6cda
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088462"
---
# <a name="enable-windows-7-support-for-intel-avx"></a><span data-ttu-id="791c0-103">Включение поддержки Windows 7 для Intel AVX</span><span class="sxs-lookup"><span data-stu-id="791c0-103">Enable Windows 7 Support for Intel AVX</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="791c0-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="791c0-104">Affected Platforms</span></span>

 <span data-ttu-id="791c0-105">**Клиенты** — Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="791c0-105">**Clients** - Windows 7 SP1</span></span>  
<span data-ttu-id="791c0-106">**Серверы** — Windows Server 2008 R2 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="791c0-106">**Servers** - Windows Server 2008 R2 SP1</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="791c0-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="791c0-107">Feature Impact</span></span>

 <span data-ttu-id="791c0-108">**Серьезность** — низкая</span><span class="sxs-lookup"><span data-stu-id="791c0-108">**Severity** - Low</span></span>  
<span data-ttu-id="791c0-109">**Частота** -низкая</span><span class="sxs-lookup"><span data-stu-id="791c0-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="791c0-110">Описание</span><span class="sxs-lookup"><span data-stu-id="791c0-110">Description</span></span>

<span data-ttu-id="791c0-111">Intel<sup>?</sup></span><span class="sxs-lookup"><span data-stu-id="791c0-111">Intel<sup>?</sup></span></span> <span data-ttu-id="791c0-112">Расширенные векторные расширения (AVX)<sup>?</sup></span><span class="sxs-lookup"><span data-stu-id="791c0-112">Advanced Vector Extensions (AVX)<sup>?</sup></span></span> <span data-ttu-id="791c0-113">— это 256-разрядное расширение вектора с плавающей запятой SIMD для архитектуры Intel.</span><span class="sxs-lookup"><span data-stu-id="791c0-113">is a 256-bit SIMD floating-point vector extension of Intel architecture.</span></span> <span data-ttu-id="791c0-114">Он включает расширения для наборов инструкций и регистров.</span><span class="sxs-lookup"><span data-stu-id="791c0-114">It includes extensions to both instruction and register sets.</span></span>

<span data-ttu-id="791c0-115">Корпорация Майкрософт разработала некоторые улучшения API, такие как функции Ксстате, которые позволяют приложениям получать доступ к информации и состоянию расширенных функций процессора, включая AVX, и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="791c0-115">Microsoft has developed some API enhancements, such as XState functions, that enable applications to access and manipulate extended processor feature information and state, including AVX.</span></span>

## <a name="usage-scenarios"></a><span data-ttu-id="791c0-116">Сценарии использования</span><span class="sxs-lookup"><span data-stu-id="791c0-116">Usage Scenarios</span></span>

<span data-ttu-id="791c0-117">Существует три общих уровня потенциального воздействия.</span><span class="sxs-lookup"><span data-stu-id="791c0-117">There are three general levels of potential impact.</span></span>

<span data-ttu-id="791c0-118">**Уровень 1.** Приложения, которые не используют Intel AVX напрямую, не увидят никакого влияния на их функциональность, даже если они вызывают библиотеки или используют компиляторы, которые косвенно используют или создают расширения Intel AVX.</span><span class="sxs-lookup"><span data-stu-id="791c0-118">**Level 1:** Applications that do not directly use Intel AVX will not see any impact to their functionality even if they call into libraries or use compilers that indirectly use or generate Intel AVX extensions.</span></span> <span data-ttu-id="791c0-119">Это соответствует большинству приложений.</span><span class="sxs-lookup"><span data-stu-id="791c0-119">This represents by far the majority of applications.</span></span>

<span data-ttu-id="791c0-120">**Уровень 2:** Расширенные приложения, явно использующие набор инструкций Intel AVX, смогут получать доступ к содержимому регистра AVX и изменять его при возникновении аппаратного исключения.</span><span class="sxs-lookup"><span data-stu-id="791c0-120">**Level 2:** Advanced applications that explicitly use the Intel AVX instruction set will be able to access and change AVX register contents when a hardware exception is raised.</span></span> <span data-ttu-id="791c0-121">Очень небольшое количество приложений попадают в эту категорию, так как оно подразумевает глубокую информацию о потоке инструкций, выполняемую на момент исключения, например приложения с разделами, написанными на языке ассемблера, или те, которые создают машинный код во время выполнения (например, среды выполнения управляемого кода с JIT-компиляцией).</span><span class="sxs-lookup"><span data-stu-id="791c0-121">A very small number of applications would fall into this category, as it implies an intimate knowledge of the instruction stream executing at the time of the exception, such as applications with sections written in assembly language or those that generate machine code at runtime (for example, managed code runtimes with just-in-time compilation).</span></span>

<span data-ttu-id="791c0-122">**Уровень 3.** Приложения отладчика смогут получать доступ к состоянию AVX в отлаживаемом приложении и работать с ним.</span><span class="sxs-lookup"><span data-stu-id="791c0-122">**Level 3:** Debugger applications will be able to access and manipulate the AVX state in the application being debugged.</span></span>

## <a name="how-to-leverage-feature-capabilities"></a><span data-ttu-id="791c0-123">Как использовать возможности функций</span><span class="sxs-lookup"><span data-stu-id="791c0-123">How to Leverage Feature Capabilities</span></span>

<span data-ttu-id="791c0-124">**Уровень 1.** Чтобы приложения не использовали Intel AVX, никаких действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="791c0-124">**Level 1:** No action is necessary for applications to use Intel AVX.</span></span>

<span data-ttu-id="791c0-125">**Уровень 2:** Приложения в этой категории имеют возможность доступа и управления состоянием AVX во время исключения из фильтров исключений.</span><span class="sxs-lookup"><span data-stu-id="791c0-125">**Level 2:** Applications in this category have the option to access and manipulate AVX state at the time of the exception from within their exception filters.</span></span> <span data-ttu-id="791c0-126">После получения контекста базового процессора через Жетексцептионинформатион фильтры должны:</span><span class="sxs-lookup"><span data-stu-id="791c0-126">After obtaining the base processor context via GetExceptionInformation, filters should:</span></span>

 <span data-ttu-id="791c0-127">**1.** проверьте значение флага **context \_ ксстате** .</span><span class="sxs-lookup"><span data-stu-id="791c0-127">**1.** Check the value of the **CONTEXT\_XSTATE** flag.</span></span> <span data-ttu-id="791c0-128">Этот флаг указывает на наличие по крайней мере одной функции Ксстате в контексте.</span><span class="sxs-lookup"><span data-stu-id="791c0-128">This flag indicates the presence of at least one XState feature in the context.</span></span>  
<span data-ttu-id="791c0-129">**2.** если это так, вызовите **жетксстатефеатуресмаск** и проверьте значение флага **\_ AVX ксстате** в возвращенной маске.</span><span class="sxs-lookup"><span data-stu-id="791c0-129">**2.** If this is the case, call **GetXStateFeaturesMask** and test the value of the **XSTATE\_AVX** flag in the returned mask.</span></span> <span data-ttu-id="791c0-130">Это указывает на присутствие состояния AVX в контексте.</span><span class="sxs-lookup"><span data-stu-id="791c0-130">This indicates the presence of AVX state in the context.</span></span>  
<span data-ttu-id="791c0-131">**3.** вызовите **локатексстатефеатуре** , чтобы получить фактическое расположение, где хранится состояние AVX.</span><span class="sxs-lookup"><span data-stu-id="791c0-131">**3.** Call **LocateXStateFeature** to retrieve the actual location where the AVX state is stored.</span></span>  

<span data-ttu-id="791c0-132">**Уровень 3.** Нет необходимости обновлять существующие приложения отладчика, если только они не хотят получить доступ к регистрам Intel AVX:</span><span class="sxs-lookup"><span data-stu-id="791c0-132">**Level 3:** It is not necessary to update existing debugger applications unless they wish access the Intel AVX registers:</span></span>

<span data-ttu-id="791c0-133">**1.** чтобы определить, включена ли AVX, отладчик должен использовать:</span><span class="sxs-lookup"><span data-stu-id="791c0-133">**1.** To determine if AVX is enabled, the debugger should use:</span></span>

-   <span data-ttu-id="791c0-134">Жетенабледксстатефеатурес для получения маски включенных функций Ксстате на процессорах x86 или x64, чтобы определить, какие функции существуют и включены в системе перед использованием функции процессора Ксстате или попытки управления контекстами Ксстате.</span><span class="sxs-lookup"><span data-stu-id="791c0-134">GetEnabledXStateFeatures to get a mask of enabled XState features on x86 or x64 processors to determine what features are present and enabled on the system before using an XState processor feature or attempting to manipulate XState contexts</span></span>

  
<span data-ttu-id="791c0-135">**2.** если AVX существует и вы хотите получить и манипулировать состоянием AVX из отлаживаемого приложения (например, GetThreadContext и SetThreadContext), отладчик должен использовать:</span><span class="sxs-lookup"><span data-stu-id="791c0-135">**2.** If AVX is present and you wish to retrieve and manipulate the AVX state from the application being debugged (for example, GetThreadContext and SetThreadContext), the debugger should use:</span></span>

-   <span data-ttu-id="791c0-136">Функция Инитиализеконтекст для инициализации структуры контекста в буфере с требуемым размером и выравниванием</span><span class="sxs-lookup"><span data-stu-id="791c0-136">InitializeContext Function to Initialize a context structure inside a buffer with the necessary size and alignment</span></span>
-   <span data-ttu-id="791c0-137">Функция Копиконтекст для копирования структуры исходного контекста (включая любые Ксстате) на инициализированную структуру контекста назначения</span><span class="sxs-lookup"><span data-stu-id="791c0-137">CopyContext Function to copy a source context structure (including any XState) onto an initialized destination context structure</span></span>

  
<span data-ttu-id="791c0-138">**3.** чтобы проверить, установить и определить состояние AVX в контексте процессора, отладчик должен использовать:</span><span class="sxs-lookup"><span data-stu-id="791c0-138">**3.** To test, set and locate the AVX state within a processor context, the debugger should use:</span></span>

-   <span data-ttu-id="791c0-139">Локатексстатефеатуре получить указатель на состояние процессора для отдельной функции Ксстате в структуре контекста</span><span class="sxs-lookup"><span data-stu-id="791c0-139">LocateXStateFeature to retrieve a pointer to the processor state for an individual XState feature within a context structure</span></span>
-   <span data-ttu-id="791c0-140">Жетксстатефеатуресмаск вернуть маску функций Ксстате, установленных в структуре контекста</span><span class="sxs-lookup"><span data-stu-id="791c0-140">GetXStateFeaturesMask to return the mask of XState features set within a context structure</span></span>
-   <span data-ttu-id="791c0-141">Сетксстатефеатуресмаск для установки маски функций Ксстате, установленных в структуре контекста</span><span class="sxs-lookup"><span data-stu-id="791c0-141">SetXStateFeaturesMask to set the mask of XState features set within a context structure</span></span>

  


## <a name="links-to-other-resources"></a><span data-ttu-id="791c0-142">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="791c0-142">Links to Other Resources</span></span>

-   <span data-ttu-id="791c0-143">Дополнительные сведения о функциях Ксстате в Windows SDK см. в разделе [Отладка функций](../debug/debugging-functions.md).</span><span class="sxs-lookup"><span data-stu-id="791c0-143">For information about the XState functions in the Windows SDK, see [Debugging Functions](../debug/debugging-functions.md).</span></span>
-   <span data-ttu-id="791c0-144">Общие сведения о инструкциях и возможностях Intel AVX см. [в разделе Intel AVX: новые границы повышения производительности и эффективности энергопотребления](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).</span><span class="sxs-lookup"><span data-stu-id="791c0-144">For an overview of the instructions and capabilities of the Intel AVX, see [Intel AVX: New Frontiers in Performance Improvements and Energy Efficiency](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).</span></span>

 

 
