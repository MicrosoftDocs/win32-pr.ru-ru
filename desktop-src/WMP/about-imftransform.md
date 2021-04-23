---
title: О Имфтрансформ
description: О Имфтрансформ
ms.assetid: 889f2d82-148a-4a7e-b78c-37ec86b37e0b
keywords:
- Подключаемые модули проигрывателя Windows Media, интерфейсы
- подключаемые модули, интерфейсы
- подключаемые модули обработки цифровых сигналов, интерфейсы
- Подключаемые модули DSP, интерфейсы
- интерфейсы, подключаемые модули DSP
- Подключаемые модули проигрывателя Windows Media, интерфейс Имфтрансформ
- подключаемые модули, интерфейс Имфтрансформ
- подключаемые модули обработки цифровых сигналов, интерфейс Имфтрансформ
- Подключаемые модули DSP, интерфейс Имфтрансформ
- Интерфейс Имфтрансформ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb58ab84070a8cb9390e4525b9b642f15a29f14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691144"
---
# <a name="about-imftransform"></a><span data-ttu-id="235d3-113">О Имфтрансформ</span><span class="sxs-lookup"><span data-stu-id="235d3-113">About IMFTransform</span></span>

<span data-ttu-id="235d3-114">Интерфейс **имфтрансформ** — это один из интерфейсов, который должен быть реализован подключаемым модулем DSP с двойным режимом.</span><span class="sxs-lookup"><span data-stu-id="235d3-114">The **IMFTransform** interface is one of the interfaces that must be implemented by a dual-mode DSP plug-in.</span></span> <span data-ttu-id="235d3-115">Проигрыватель Windows Media вызывает методы интерфейса **имфтрансформ** , чтобы предоставить данные подключаемому модулю и получить обработанные данные обратно из подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="235d3-115">Windows Media Player calls the methods of the **IMFTransform** interface to provide data to the plug-in and to retrieve processed data back from the plug-in.</span></span> <span data-ttu-id="235d3-116">Полную документацию по интерфейсу **имфтрансформ** см. в разделе Media Foundation Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="235d3-116">For complete documentation of the **IMFTransform** interface, see the Media Foundation section of the Windows SDK.</span></span>

<span data-ttu-id="235d3-117">Методы **имфтрансформ** можно классифицировать следующим образом.</span><span class="sxs-lookup"><span data-stu-id="235d3-117">The methods of **IMFTransform** can be categorized as follows.</span></span>

## <a name="methods-that-handle-format-negotiation"></a><span data-ttu-id="235d3-118">Методы, обрабатывающие согласование формата</span><span class="sxs-lookup"><span data-stu-id="235d3-118">Methods That Handle Format Negotiation</span></span>

<span data-ttu-id="235d3-119">Проигрыватель Windows Media вызывает следующие методы для получения сведений о форматах данных, поддерживаемых подключаемым модулем.</span><span class="sxs-lookup"><span data-stu-id="235d3-119">Windows Media Player calls the following methods to get information about the data formats supported by the plug-in.</span></span>

-   <span data-ttu-id="235d3-120">**жетстреамкаунт**</span><span class="sxs-lookup"><span data-stu-id="235d3-120">**GetStreamCount**</span></span>
-   <span data-ttu-id="235d3-121">**жетстреамлимитс**</span><span class="sxs-lookup"><span data-stu-id="235d3-121">**GetStreamLimits**</span></span>
-   <span data-ttu-id="235d3-122">**жетинпутстреаминфо**</span><span class="sxs-lookup"><span data-stu-id="235d3-122">**GetInputStreamInfo**</span></span>
-   <span data-ttu-id="235d3-123">**жетаутпутстреаминфо**</span><span class="sxs-lookup"><span data-stu-id="235d3-123">**GetOutputStreamInfo**</span></span>
-   <span data-ttu-id="235d3-124">**жетинпутаваилаблетипе**</span><span class="sxs-lookup"><span data-stu-id="235d3-124">**GetInputAvailableType**</span></span>
-   <span data-ttu-id="235d3-125">**жетаутпутаваилаблетипе**</span><span class="sxs-lookup"><span data-stu-id="235d3-125">**GetOutputAvailableType**</span></span>
-   <span data-ttu-id="235d3-126">**сетинпуттипе**</span><span class="sxs-lookup"><span data-stu-id="235d3-126">**SetInputType**</span></span>
-   <span data-ttu-id="235d3-127">**сетаутпуттипе**</span><span class="sxs-lookup"><span data-stu-id="235d3-127">**SetOutputType**</span></span>
-   <span data-ttu-id="235d3-128">**GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="235d3-128">**GetAttributes**</span></span>
-   <span data-ttu-id="235d3-129">**жетинпутстреаматтрибутес**</span><span class="sxs-lookup"><span data-stu-id="235d3-129">**GetInputStreamAttributes**</span></span>
-   <span data-ttu-id="235d3-130">**жетаутпутстреаматтрибутес**</span><span class="sxs-lookup"><span data-stu-id="235d3-130">**GetOutputStreamAttributes**</span></span>
-   <span data-ttu-id="235d3-131">**жетстреамидс**</span><span class="sxs-lookup"><span data-stu-id="235d3-131">**GetStreamIDs**</span></span>

## <a name="methods-that-specify-or-retrieve-state-information"></a><span data-ttu-id="235d3-132">Методы, указывающие или получающие сведения о состоянии</span><span class="sxs-lookup"><span data-stu-id="235d3-132">Methods That Specify or Retrieve State Information</span></span>

<span data-ttu-id="235d3-133">Проигрыватель Windows Media вызывает следующие методы для получения или задания значений, связанных с текущим состоянием подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="235d3-133">Windows Media Player calls the following methods to get or set values related to the current state of the plug-in.</span></span>

-   <span data-ttu-id="235d3-134">**сетинпуттипе**</span><span class="sxs-lookup"><span data-stu-id="235d3-134">**SetInputType**</span></span>
-   <span data-ttu-id="235d3-135">**сетаутпуттипе**</span><span class="sxs-lookup"><span data-stu-id="235d3-135">**SetOutputType**</span></span>
-   <span data-ttu-id="235d3-136">**жетинпуткурренттипе**</span><span class="sxs-lookup"><span data-stu-id="235d3-136">**GetInputCurrentType**</span></span>
-   <span data-ttu-id="235d3-137">**жетаутпуткурренттипе**</span><span class="sxs-lookup"><span data-stu-id="235d3-137">**GetOutputCurrentType**</span></span>
-   <span data-ttu-id="235d3-138">**жетинпутстатус**</span><span class="sxs-lookup"><span data-stu-id="235d3-138">**GetInputStatus**</span></span>
-   <span data-ttu-id="235d3-139">**аддинпутстреамс**</span><span class="sxs-lookup"><span data-stu-id="235d3-139">**AddInputStreams**</span></span>
-   <span data-ttu-id="235d3-140">**делетеинпутстреамс**</span><span class="sxs-lookup"><span data-stu-id="235d3-140">**DeleteInputStreams**</span></span>
-   <span data-ttu-id="235d3-141">**жетаутпутстатус**</span><span class="sxs-lookup"><span data-stu-id="235d3-141">**GetOutputStatus**</span></span>
-   <span data-ttu-id="235d3-142">**сетаутпутбаундс**</span><span class="sxs-lookup"><span data-stu-id="235d3-142">**SetOutputBounds**</span></span>

> [!Note]  
> <span data-ttu-id="235d3-143">**Сетинпуттипе** и **сетаутпуттипе** используются как для согласования формата, так и для указания и получения сведений о состоянии.</span><span class="sxs-lookup"><span data-stu-id="235d3-143">**SetInputType** and **SetOutputType** are used both for format negotiation and for specifying and retrieving state information.</span></span>

 

## <a name="methods-that-handle-buffering-and-processing-data"></a><span data-ttu-id="235d3-144">Методы, обрабатывающие буферизацию и обработку данных</span><span class="sxs-lookup"><span data-stu-id="235d3-144">Methods That Handle Buffering and Processing Data</span></span>

<span data-ttu-id="235d3-145">Проигрыватель Windows Media вызывает следующие методы для запуска различных процессов, которые выполняет подключаемый модуль для обработки цифровых сигналов.</span><span class="sxs-lookup"><span data-stu-id="235d3-145">Windows Media Player calls the following methods to initiate the various processes that the plug-in performs to do the digital signal processing.</span></span>

-   <span data-ttu-id="235d3-146">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="235d3-146">**ProcessInput**</span></span>
-   <span data-ttu-id="235d3-147">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="235d3-147">**ProcessOutput**</span></span>
-   <span data-ttu-id="235d3-148">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="235d3-148">**ProcessMessage**</span></span>
-   <span data-ttu-id="235d3-149">**процессевент**</span><span class="sxs-lookup"><span data-stu-id="235d3-149">**ProcessEvent**</span></span>

## <a name="related-topics"></a><span data-ttu-id="235d3-150">См. также</span><span class="sxs-lookup"><span data-stu-id="235d3-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="235d3-151">**Требуемые интерфейсы**</span><span class="sxs-lookup"><span data-stu-id="235d3-151">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 




