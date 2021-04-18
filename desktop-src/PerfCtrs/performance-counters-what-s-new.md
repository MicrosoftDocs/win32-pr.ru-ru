---
description: В этом разделе описаны новые функции, добавленные в счетчики производительности для каждого выпуска.
ms.assetid: 14bdae6c-9dcd-401e-8c43-5391e00cf7e3
title: Новые возможности (счетчики производительности)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0c1189a185351eabae438a01c6f111952f164e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663171"
---
# <a name="whats-new-with-performance-counters"></a><span data-ttu-id="e536e-103">Новые возможности счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="e536e-103">What's New with Performance Counters</span></span>

<span data-ttu-id="e536e-104">В этом разделе описаны новые функции, добавленные в счетчики производительности для каждого выпуска.</span><span class="sxs-lookup"><span data-stu-id="e536e-104">This section describes the new features that were added to Performance Counters for each release.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="e536e-105">Windows 7 и Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e536e-105">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="e536e-106">Средство [КТРПП](ctrpp.md) было изменено для улучшения и упрощения создания кода.</span><span class="sxs-lookup"><span data-stu-id="e536e-106">The [CTRPP](ctrpp.md) tool was changed to improve and simplify code generation.</span></span> <span data-ttu-id="e536e-107">Теперь средство создает только заголовок и файл ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e536e-107">The tool now generates only a header and resource file.</span></span> <span data-ttu-id="e536e-108">Если требуется старое поведение при создании кода (не рекомендуется), можно использовать новый `-legacy` аргумент.</span><span class="sxs-lookup"><span data-stu-id="e536e-108">If you want to old code generation behavior (not recommended), you can use the new `-legacy` argument.</span></span>

- <span data-ttu-id="e536e-109">Теперь необходимо указать новые `-o` `-rc` аргументы и, задающих имя и расположение заголовка и файла ресурсов соответственно.</span><span class="sxs-lookup"><span data-stu-id="e536e-109">You must now specify the new `-o` and `-rc` arguments that specify the name and location of the header and resource file, respectively.</span></span>
- <span data-ttu-id="e536e-110">Можно использовать необязательный `-prefix` аргумент New для указания строки, добавляемой в начало глобальных переменных и функций, определенных в создаваемом файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="e536e-110">You can use the optional new `-prefix` argument to specify a string to add to the beginning of global variables and functions defined in the generated header file.</span></span>
- <span data-ttu-id="e536e-111">Если необходимо обновить манифест счетчиков, использование нового создания кода исключает необходимость слияния предыдущей реализации обратного вызова с новым созданным кодом, так как обратные вызовы больше не включаются в созданный код.</span><span class="sxs-lookup"><span data-stu-id="e536e-111">If you have to update your counters manifest, using the new code generation eliminates the need to merge your previous callback implementation with the new generated code since the callbacks are no longer included in the generated code.</span></span>

<span data-ttu-id="e536e-112">`symbol`Для следующих элементов манифеста доступен новый атрибут:</span><span class="sxs-lookup"><span data-stu-id="e536e-112">A new `symbol` attribute is available for the following manifest elements:</span></span>

- [<span data-ttu-id="e536e-113">поставщики</span><span class="sxs-lookup"><span data-stu-id="e536e-113">provider</span></span>](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
- [<span data-ttu-id="e536e-114">counterSet</span><span class="sxs-lookup"><span data-stu-id="e536e-114">counterSet</span></span>](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)
- [<span data-ttu-id="e536e-115">подписан</span><span class="sxs-lookup"><span data-stu-id="e536e-115">counter</span></span>](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)

<span data-ttu-id="e536e-116">`symbol`Атрибут является обязательным для [provider](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) и [CounterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)и является необязательным для [счетчика](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element).</span><span class="sxs-lookup"><span data-stu-id="e536e-116">The `symbol` attribute is required for [provider](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) and [counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element), and is optional for [counter](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element).</span></span> <span data-ttu-id="e536e-117">Атрибут позволяет указать символическое имя, которое можно использовать для ссылки на каждый элемент при вызове функций поставщика (например, можно использовать символьное имя набора счетчиков при вызове [перфкреатеинстанце](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)).</span><span class="sxs-lookup"><span data-stu-id="e536e-117">The attribute lets you provide a symbolic name that you can use to reference each element when calling the provider functions (for example, you can use the counter set symbolic name when calling [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)).</span></span>

## <a name="windows-vista"></a><span data-ttu-id="e536e-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e536e-118">Windows Vista</span></span>

<span data-ttu-id="e536e-119">Архитектура счетчиков производительности для предоставления данных счетчиков была полностью изменена в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="e536e-119">The Performance Counters architecture for providing counter data was completely changed for this release.</span></span>

<span data-ttu-id="e536e-120">Ранее вы использовали INI-файл для определения данных счетчика и реализовали библиотеку DLL производительности, которая выполнялась в процессе потребителя для предоставления данных по запросу потребителя.</span><span class="sxs-lookup"><span data-stu-id="e536e-120">Previously, you used an INI file to define your counter data and you implemented a performance DLL which ran in the consumer's process to provide the data when a consumer requested it.</span></span> <span data-ttu-id="e536e-121">Эта архитектура устарела и не рекомендуется для нового кода из-за серьезных проблем с производительностью и надежностью.</span><span class="sxs-lookup"><span data-stu-id="e536e-121">This architecture is deprecated and is not recommended for new code due to significant performance and reliability issues.</span></span>

<span data-ttu-id="e536e-122">Новая архитектура использует манифест для определения данных счетчика и выполняет код в процессе поставщика для предоставления данных, когда потребитель запрашивает их.</span><span class="sxs-lookup"><span data-stu-id="e536e-122">The new architecture uses a manifest to define the counter data and runs code in the provider's process to provide the data when a consumer requests it.</span></span> <span data-ttu-id="e536e-123">Дополнительные сведения см. в разделе [предоставление данных счетчика с помощью версии 2,0](providing-counter-data-using-version-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="e536e-123">For additional details, see [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>

<span data-ttu-id="e536e-124">Для этого выпуска были добавлены следующие функции:</span><span class="sxs-lookup"><span data-stu-id="e536e-124">The following functions were added for this release:</span></span>

- [<span data-ttu-id="e536e-125">контролкаллбакк</span><span class="sxs-lookup"><span data-stu-id="e536e-125">ControlCallback</span></span>](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [<span data-ttu-id="e536e-126">перфкреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="e536e-126">PerfCreateInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [<span data-ttu-id="e536e-127">перфделетеинстанце</span><span class="sxs-lookup"><span data-stu-id="e536e-127">PerfDeleteInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [<span data-ttu-id="e536e-128">перфкуеринстанце</span><span class="sxs-lookup"><span data-stu-id="e536e-128">PerfQueryInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [<span data-ttu-id="e536e-129">перфсеткаунтерсетинфо</span><span class="sxs-lookup"><span data-stu-id="e536e-129">PerfSetCounterSetInfo</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [<span data-ttu-id="e536e-130">перфсетулонгкаунтервалуе</span><span class="sxs-lookup"><span data-stu-id="e536e-130">PerfSetULongCounterValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [<span data-ttu-id="e536e-131">перфсетулонглонгкаунтервалуе</span><span class="sxs-lookup"><span data-stu-id="e536e-131">PerfSetULongLongCounterValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [<span data-ttu-id="e536e-132">перфсеткаунтеррефвалуе</span><span class="sxs-lookup"><span data-stu-id="e536e-132">PerfSetCounterRefValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [<span data-ttu-id="e536e-133">перфстартпровидер</span><span class="sxs-lookup"><span data-stu-id="e536e-133">PerfStartProvider</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [<span data-ttu-id="e536e-134">перфстоппровидер</span><span class="sxs-lookup"><span data-stu-id="e536e-134">PerfStopProvider</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

<span data-ttu-id="e536e-135">Для этого выпуска были добавлены следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="e536e-135">The following structures were added for this release:</span></span>

- [<span data-ttu-id="e536e-136">\_удостоверение счетчика производительности \_</span><span class="sxs-lookup"><span data-stu-id="e536e-136">PERF\_COUNTER\_IDENTITY</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [<span data-ttu-id="e536e-137">\_сведения о счетчике производительности \_</span><span class="sxs-lookup"><span data-stu-id="e536e-137">PERF\_COUNTER\_INFO</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [<span data-ttu-id="e536e-138">\_сведения о наборе счетчиков производительности \_</span><span class="sxs-lookup"><span data-stu-id="e536e-138">PERF\_COUNTERSET\_INFO</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [<span data-ttu-id="e536e-139">\_экземпляр COUNTERSET производительности \_</span><span class="sxs-lookup"><span data-stu-id="e536e-139">PERF\_COUNTERSET\_INSTANCE</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)

<span data-ttu-id="e536e-140">Список XML-элементов, используемых в манифесте для определения счетчиков, см. в разделе [схема счетчиков производительности](performance-counters-schema.md).</span><span class="sxs-lookup"><span data-stu-id="e536e-140">For a list of the XML elements that you use in your manifest to define your counters, see [Performance Counters Schema](performance-counters-schema.md).</span></span>

<span data-ttu-id="e536e-141">Сведения о средстве предварительного процессора КТРПП, который анализирует манифест и создает код, используемый в качестве отправной точки для поставщика, см. в разделе [КТРПП](ctrpp.md).</span><span class="sxs-lookup"><span data-stu-id="e536e-141">For information on the CTRPP pre-processor tool that parses your manifest and generates the code that you use as the starting point for your provider, see [CTRPP](ctrpp.md).</span></span>
