---
title: О Имедиаобжект
description: О Имедиаобжект
ms.assetid: c483f74a-efd8-4a9f-a719-686099755e63
keywords:
- Подключаемые модули проигрывателя Windows Media, интерфейсы
- подключаемые модули, интерфейсы
- подключаемые модули обработки цифровых сигналов, интерфейсы
- Подключаемые модули DSP, интерфейсы
- интерфейсы, подключаемые модули DSP
- Подключаемые модули проигрывателя Windows Media, интерфейс Имедиаобжект
- подключаемые модули, интерфейс Имедиаобжект
- подключаемые модули обработки цифровых сигналов, интерфейс Имедиаобжект
- Подключаемые модули DSP, интерфейс Имедиаобжект
- Интерфейс Имедиаобжект
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbbecd749242b67bc5c8f36b3c7a2c0a5fbe461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773583"
---
# <a name="about-imediaobject"></a><span data-ttu-id="37536-113">О Имедиаобжект</span><span class="sxs-lookup"><span data-stu-id="37536-113">About IMediaObject</span></span>

<span data-ttu-id="37536-114">Интерфейс **имедиаобжект** является необходимым интерфейсом для дмос.</span><span class="sxs-lookup"><span data-stu-id="37536-114">The **IMediaObject** interface is the required interface for DMOs.</span></span> <span data-ttu-id="37536-115">**Имедиаобжект** содержит методы, используемые подключаемым модулем DSP Windows Media Player для получения данных из проигрывателя Windows Media, обработки данных и возврата обработанных данных в проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="37536-115">**IMediaObject** contains the methods that a Windows Media Player DSP plug-in uses to get data from Windows Media Player, to process the data, and to return the processed data to Windows Media Player.</span></span> <span data-ttu-id="37536-116">Полную документацию по интерфейсу **имедиаобжект** см. в разделе «DirectShow» Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="37536-116">For complete documentation of the **IMediaObject** interface, see the DirectShow section of the Windows SDK.</span></span>

<span data-ttu-id="37536-117">Методы **имедиаобжект** можно классифицировать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="37536-117">The methods of **IMediaObject** can be categorized as follows:</span></span>

## <a name="methods-that-handle-format-negotiation"></a><span data-ttu-id="37536-118">Методы, обрабатывающие согласование формата</span><span class="sxs-lookup"><span data-stu-id="37536-118">Methods that Handle Format Negotiation</span></span>

<span data-ttu-id="37536-119">Это методы, которые вызываются проигрывателем Windows Media для получения сведений о форматах данных, поддерживаемых подключаемым модулем.</span><span class="sxs-lookup"><span data-stu-id="37536-119">These are the methods that Windows Media Player calls to get information about the data formats supported by the plug-in.</span></span> <span data-ttu-id="37536-120">Эти способы включают перечисленные ниже.</span><span class="sxs-lookup"><span data-stu-id="37536-120">These methods include:</span></span>

-   <span data-ttu-id="37536-121">**жетинпутмакслатенци**</span><span class="sxs-lookup"><span data-stu-id="37536-121">**GetInputMaxLatency**</span></span>
-   <span data-ttu-id="37536-122">**жетинпутсизеинфо**</span><span class="sxs-lookup"><span data-stu-id="37536-122">**GetInputSizeInfo**</span></span>
-   <span data-ttu-id="37536-123">**жетинпутстреаминфо**</span><span class="sxs-lookup"><span data-stu-id="37536-123">**GetInputStreamInfo**</span></span>
-   <span data-ttu-id="37536-124">**жетинпуттипе**</span><span class="sxs-lookup"><span data-stu-id="37536-124">**GetInputType**</span></span>
-   <span data-ttu-id="37536-125">**жетаутпутсизеинфо**</span><span class="sxs-lookup"><span data-stu-id="37536-125">**GetOutputSizeInfo**</span></span>
-   <span data-ttu-id="37536-126">**жетаутпутстреаминфо**</span><span class="sxs-lookup"><span data-stu-id="37536-126">**GetOutputStreamInfo**</span></span>
-   <span data-ttu-id="37536-127">**жетаутпуттипе**</span><span class="sxs-lookup"><span data-stu-id="37536-127">**GetOutputType**</span></span>
-   <span data-ttu-id="37536-128">**жетстреамкаунт**</span><span class="sxs-lookup"><span data-stu-id="37536-128">**GetStreamCount**</span></span>
-   <span data-ttu-id="37536-129">**сетинпутмакслатенци**</span><span class="sxs-lookup"><span data-stu-id="37536-129">**SetInputMaxLatency**</span></span>
-   <span data-ttu-id="37536-130">**сетинпуттипе**</span><span class="sxs-lookup"><span data-stu-id="37536-130">**SetInputType**</span></span>
-   <span data-ttu-id="37536-131">**сетаутпуттипе**</span><span class="sxs-lookup"><span data-stu-id="37536-131">**SetOutputType**</span></span>

<span data-ttu-id="37536-132">Некоторые из этих методов, например **жетинпуттипе** и **сетинпуттипе**, используют структуру **\_ \_ типа мультимедиа DMO** для описания формата данных, используемых потоком.</span><span class="sxs-lookup"><span data-stu-id="37536-132">Several of these methods, such as **GetInputType** and **SetInputType**, use the **DMO\_MEDIA\_TYPE** structure to describe the format of the data used by a stream.</span></span> <span data-ttu-id="37536-133">Когда проигрыватель Windows Media вызывает эти методы, он предоставляет указатель на структуру **\_ \_ типа мультимедиа DMO** .</span><span class="sxs-lookup"><span data-stu-id="37536-133">When Windows Media Player calls these methods, it provides a pointer to a **DMO\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="37536-134">Если метод, например **сетинпуттипе** , указывает сведения о типе мультимедиа, подключаемый модуль должен скопировать структуру **\_ \_ типа мультимедиа DMO** в переменную-член и проверить его члены данных, чтобы определить тип данных, которые проигрыватель Windows Media будет предоставлять во входном буфере.</span><span class="sxs-lookup"><span data-stu-id="37536-134">If a method such as **SetInputType** specifies the media type information, the plug-in should copy the **DMO\_MEDIA\_TYPE** structure to a member variable and inspect its data members to determine the type of data that Windows Media Player will provide in the input buffer.</span></span> <span data-ttu-id="37536-135">Если метод, например **жетинпуттипе** , получает сведения о типе мультимедиа, подключаемый модуль должен скопировать адрес переменной-члена, содержащей структуру **\_ \_ типа мультимедиа DMO** , в указатель, предоставленный проигрывателем Windows Media в списке параметров.</span><span class="sxs-lookup"><span data-stu-id="37536-135">If a method such as **GetInputType** retrieves the media type information, the plug-in should copy the address of the member variable containing the **DMO\_MEDIA\_TYPE** structure to the pointer provided by Windows Media Player in the parameter list.</span></span>

<span data-ttu-id="37536-136">Проигрыватель Windows Media в основном использует два члена структуры **\_ \_ типа мультимедиа DMO** :</span><span class="sxs-lookup"><span data-stu-id="37536-136">Windows Media Player mainly uses two members of the **DMO\_MEDIA\_TYPE** structure:</span></span>

-   <span data-ttu-id="37536-137">**мажортипе**: глобальный уникальный идентификатор (GUID), указывающий общую категорию носителя, например аудио или видео.</span><span class="sxs-lookup"><span data-stu-id="37536-137">**majortype**: A globally unique identifier (GUID) that specifies the overall category of the media, such as audio or video.</span></span>
-   <span data-ttu-id="37536-138">**подтип**— идентификатор GUID, указывающий более подробное описание носителя, например звук PCM.</span><span class="sxs-lookup"><span data-stu-id="37536-138">**subtype**: A GUID that specifies a more detailed description of the media, such as PCM audio.</span></span>

<span data-ttu-id="37536-139">Эти идентификаторы GUID можно найти в заголовке с именем UUIDs. h, который входит в состав Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="37536-139">These GUIDs can be found in the header named uuids.h, which is included with the Windows SDK.</span></span>

<span data-ttu-id="37536-140">Такие методы, как **жетинпутсизеинфо** , предоставляют сведения для проигрывателя Windows Media о том, сколько памяти требуется для выделения буферов обработки.</span><span class="sxs-lookup"><span data-stu-id="37536-140">Methods such as **GetInputSizeInfo** provide information to Windows Media Player about how much memory is required to allocate the processing buffers.</span></span> <span data-ttu-id="37536-141">Такие методы, как **жетстреамкаунт** и **жетаутпутстреаминфо** , предоставляют сведения проигрывателю Windows Media о количестве и символе потоков, поддерживаемых подключаемым модулем DSP.</span><span class="sxs-lookup"><span data-stu-id="37536-141">Methods such as **GetStreamCount** and **GetOutputStreamInfo** provide information to Windows Media Player about the number and character of the streams supported by the DSP plug-in.</span></span>

<span data-ttu-id="37536-142">**Жетинпутмакслатенци** и **сетинпутмакслатенци** реализуются дмос в особых случаях.</span><span class="sxs-lookup"><span data-stu-id="37536-142">**GetInputMaxLatency** and **SetInputMaxLatency** are implemented by DMOs in special cases.</span></span> <span data-ttu-id="37536-143">Подключаемые модули DSP проигрывателя Windows Media должны возвращать E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="37536-143">Windows Media Player DSP plug-ins should return E\_NOTIMPL.</span></span>

## <a name="methods-that-specify-or-retrieve-state-information"></a><span data-ttu-id="37536-144">Методы, указывающие или получающие сведения о состоянии</span><span class="sxs-lookup"><span data-stu-id="37536-144">Methods that Specify or Retrieve State Information</span></span>

<span data-ttu-id="37536-145">Это методы, которые вызываются проигрывателем Windows Media для получения или задания значений, связанных с текущим состоянием подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="37536-145">These are the methods that Windows Media Player calls to get or set values related to the current state of the plug-in.</span></span> <span data-ttu-id="37536-146">Эти способы включают перечисленные ниже.</span><span class="sxs-lookup"><span data-stu-id="37536-146">These methods include:</span></span>

-   <span data-ttu-id="37536-147">**жетинпуткурренттипе**</span><span class="sxs-lookup"><span data-stu-id="37536-147">**GetInputCurrentType**</span></span>
-   <span data-ttu-id="37536-148">**жетинпутстатус**</span><span class="sxs-lookup"><span data-stu-id="37536-148">**GetInputStatus**</span></span>
-   <span data-ttu-id="37536-149">**жетаутпуткурренттипе**</span><span class="sxs-lookup"><span data-stu-id="37536-149">**GetOutputCurrentType**</span></span>

<span data-ttu-id="37536-150">**Жетинпуткурренттипе** и **жетаутпуткурренттипе** используют структуру **\_ \_ типа мультимедиа DMO** для возврата сведений в проигрыватель Windows Media о типах носителей, ранее заданных для входных и выходных потоков.</span><span class="sxs-lookup"><span data-stu-id="37536-150">**GetInputCurrentType** and **GetOutputCurrentType** use the **DMO\_MEDIA\_TYPE** structure to return information to Windows Media Player about the media types previously set for the input and output streams.</span></span> <span data-ttu-id="37536-151">**Жетинпутстатус** Возвращает флаг, который указывает проигрывателю Windows Media, может ли подключаемый модуль DSP принимать входные данные.</span><span class="sxs-lookup"><span data-stu-id="37536-151">**GetInputStatus** returns a flag that tells Windows Media Player whether the DSP plug-in can accept input data.</span></span>

## <a name="methods-that-handle-buffering-and-processing-data"></a><span data-ttu-id="37536-152">Методы, обрабатывающие буферизацию и обработку данных</span><span class="sxs-lookup"><span data-stu-id="37536-152">Methods that Handle Buffering and Processing Data</span></span>

<span data-ttu-id="37536-153">Это методы, которые вызываются проигрывателем Windows Media для инициации различных процессов, выполняемых подключаемым модулем для обработки цифровых сигналов.</span><span class="sxs-lookup"><span data-stu-id="37536-153">These are the methods that Windows Media Player calls to initiate the various processes that the plug-in performs to do the digital signal processing.</span></span> <span data-ttu-id="37536-154">Эти способы включают перечисленные ниже.</span><span class="sxs-lookup"><span data-stu-id="37536-154">These methods include:</span></span>

-   <span data-ttu-id="37536-155">**аллокатестреамингресаурцес**</span><span class="sxs-lookup"><span data-stu-id="37536-155">**AllocateStreamingResources**</span></span>
-   <span data-ttu-id="37536-156">**Разрыв**</span><span class="sxs-lookup"><span data-stu-id="37536-156">**Discontinuity**</span></span>
-   <span data-ttu-id="37536-157">**Очистка**</span><span class="sxs-lookup"><span data-stu-id="37536-157">**Flush**</span></span>
-   <span data-ttu-id="37536-158">**фристреамингресаурцес**</span><span class="sxs-lookup"><span data-stu-id="37536-158">**FreeStreamingResources**</span></span>
-   <span data-ttu-id="37536-159">**Блокировка**</span><span class="sxs-lookup"><span data-stu-id="37536-159">**Lock**</span></span>
-   <span data-ttu-id="37536-160">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="37536-160">**ProcessInput**</span></span>
-   <span data-ttu-id="37536-161">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="37536-161">**ProcessOutput**</span></span>

<span data-ttu-id="37536-162">Проигрыватель Windows Media вызывает **аллокатестреамингресаурцес** и **фристреамингресаурцес** для предоставления подключаемого модуля DSP с возможностью настройки или освобождения дополнительных буферов, которые могут потребоваться подключаемому модулю для внутренней обработки.</span><span class="sxs-lookup"><span data-stu-id="37536-162">Windows Media Player calls **AllocateStreamingResources** and **FreeStreamingResources** to provide the DSP plug-in with an opportunity to set up or release any additional buffers the plug-in may require for internal processing.</span></span>

<span data-ttu-id="37536-163">Подключаемым модулям DSP в проигрывателе Windows Media не требуется использовать метод **прекращения поддержки** DMO.</span><span class="sxs-lookup"><span data-stu-id="37536-163">Windows Media Player DSP plug-ins do not need to use the DMO **Discontinuity** method.</span></span>

<span data-ttu-id="37536-164">Проигрыватель Windows Media вызывает **Сброс** , чтобы направить подключаемый модуль DSP на диск всех внутренних буферизованных данных.</span><span class="sxs-lookup"><span data-stu-id="37536-164">Windows Media Player calls **Flush** to direct the DSP plug-in to flush all internally buffered data.</span></span> <span data-ttu-id="37536-165">Подключаемый модуль должен освободить все ссылки на интерфейсы **имедиабуффер** , очистить все значения, указывающие метку времени или длину выборки для буфера мультимедиа, и повторно инициализировать все внутренние состояния, зависящие от содержимого примера носителя.</span><span class="sxs-lookup"><span data-stu-id="37536-165">The plug-in should release any references to **IMediaBuffer** interfaces, clear any values that specify the time stamp or sample length for the media buffer, and reinitialize any internal states that depend upon the contents of the media sample.</span></span>

<span data-ttu-id="37536-166">Проигрыватель Windows Media вызывает метод ProcessInput для передачи указателя на интерфейс **имедиабуффер** подключаемому модулю DSP.</span><span class="sxs-lookup"><span data-stu-id="37536-166">Windows Media Player calls ProcessInput to pass a pointer to an **IMediaBuffer** interface to the DSP plug-in.</span></span> <span data-ttu-id="37536-167">Этот интерфейс предоставляет доступ к входному буферу, выделенному проигрывателем Windows Media для предоставления данных подключаемому модулю.</span><span class="sxs-lookup"><span data-stu-id="37536-167">This interface provides access to the input buffer allocated by Windows Media Player to supply data to the plug-in.</span></span> <span data-ttu-id="37536-168">Проигрыватель Windows Media в дальнейшем вызывает **ProcessOutput** для передачи указателя на интерфейс **имедиабуффер** , который предоставляет доступ к выходному буферу, выделенному проигрывателем Windows Media для получения обработанных данных из подключаемого модуля DSP.</span><span class="sxs-lookup"><span data-stu-id="37536-168">Windows Media Player subsequently calls **ProcessOutput** to pass a pointer to an **IMediaBuffer** interface that provides access to the output buffer allocated by Windows Media Player to receive the processed data from the DSP plug-in.</span></span>

<span data-ttu-id="37536-169">Интерфейс **имедиаобжект** включает метод с именем **Lock**.</span><span class="sxs-lookup"><span data-stu-id="37536-169">The **IMediaObject** interface includes a method named **Lock**.</span></span> <span data-ttu-id="37536-170">Этот метод предназначен для получения или освобождения блокировки DMO для сохранения сериализации объектов DMO при выполнении нескольких операций.</span><span class="sxs-lookup"><span data-stu-id="37536-170">This method is designed to acquire or release a lock on the DMO to keep the DMO serialized when performing multiple operations.</span></span> <span data-ttu-id="37536-171">Версия **имедиаобжект:: Lock** в коде мастера переопределяет реализацию **блокировки** в библиотеке ATL.</span><span class="sxs-lookup"><span data-stu-id="37536-171">The version of **IMediaObject::Lock** in the wizard code overrides the ATL implementation of **Lock**.</span></span> <span data-ttu-id="37536-172">Так как проигрыватель Windows Media сериализует вызовы, выполненные в интерфейсе DMO подключаемого модуля DSP, реализация **блокировки** просто возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="37536-172">Because Windows Media Player serializes calls made to the DMO interface of a DSP plug-in, the implementation of **Lock** simply returns S\_OK.</span></span> <span data-ttu-id="37536-173">Дополнительные сведения о создании многопоточных DMO см. в разделе «DirectShow» Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="37536-173">For details about how to create a multithreaded DMO, refer to the DirectShow section of the Windows SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37536-174">См. также</span><span class="sxs-lookup"><span data-stu-id="37536-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37536-175">**Требуемые интерфейсы**</span><span class="sxs-lookup"><span data-stu-id="37536-175">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 




