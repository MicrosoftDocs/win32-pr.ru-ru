---
title: Реализация подключаемого модуля DSP аудиоподсистемы
description: Реализация подключаемого модуля DSP аудиоподсистемы
ms.assetid: 93ff0c45-f418-443d-8fba-c0a62f6e4e80
keywords:
- Подключаемые модули проигрывателя Windows Media, DSP аудиоподсистемы
- подключаемые модули, DSP аудиоподсистемы
- подключаемые модули обработки цифровых сигналов, реализация кода
- Подключаемые модули DSP, реализация кода
- подключаемые модули обработки цифровых сигналов, изменение образца кода
- Подключаемые модули DSP, изменение примера кода
- подключаемые модули обработки цифровых сигналов, реализация аудио
- Подключаемые модули DSP, реализация аудио
- подключаемые модули DSP аудио, реализация кода
- подключаемые модули DSP аудио, изменение образца кода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdde8e7f00fc9ea3ad9bb8b7adb2d0a8bfba6b32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068291"
---
# <a name="implementing-an-audio-dsp-plug-in"></a><span data-ttu-id="ffd1c-113">Реализация подключаемого модуля DSP аудиоподсистемы</span><span class="sxs-lookup"><span data-stu-id="ffd1c-113">Implementing an Audio DSP Plug-in</span></span>

<span data-ttu-id="ffd1c-114">Чтобы создать подключаемый модуль DSP для проигрывателя Windows Media, который обрабатывает аудио, необходимо изменить пример кода в функции с именем **допроцессаутпут**.</span><span class="sxs-lookup"><span data-stu-id="ffd1c-114">To create a Windows Media Player DSP plug-in that processes audio, you'll need to modify the sample code in the function named **DoProcessOutput**.</span></span> <span data-ttu-id="ffd1c-115">**Допроцессаутпут** вызывается каждый раз, когда проигрыватель Windows Media успешно вызывает **Имедиаобжект::P роцессаутпут**.</span><span class="sxs-lookup"><span data-stu-id="ffd1c-115">**DoProcessOutput** is called each time Windows Media Player successfully calls **IMediaObject::ProcessOutput**.</span></span> <span data-ttu-id="ffd1c-116">Это функция, которая выполняет задачи обработки цифровых сигналов, которые создают звуковой результат, который должен создавать подключаемый модуль DSP.</span><span class="sxs-lookup"><span data-stu-id="ffd1c-116">It is the function that performs the digital signal processing tasks that produce the audible result that the DSP plug-in is intended to produce.</span></span>

<span data-ttu-id="ffd1c-117">Обработка звукового потока похожа на обработку события времени.</span><span class="sxs-lookup"><span data-stu-id="ffd1c-117">Processing an audio stream is like handling a timed event.</span></span> <span data-ttu-id="ffd1c-118">**Допроцессаутпут** будет вызываться многократно с определенными интервалами.</span><span class="sxs-lookup"><span data-stu-id="ffd1c-118">**DoProcessOutput** will be called repeatedly and at specific intervals.</span></span> <span data-ttu-id="ffd1c-119">При каждом выполнении кода потребуется обработать определенное число байтов данных.</span><span class="sxs-lookup"><span data-stu-id="ffd1c-119">Each time your code executes, it will need to process a specific number of bytes of data.</span></span> <span data-ttu-id="ffd1c-120">**Допроцессаутпут** содержит следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="ffd1c-120">**DoProcessOutput** contains the following parameters:</span></span>



| <span data-ttu-id="ffd1c-121">Параметр</span><span class="sxs-lookup"><span data-stu-id="ffd1c-121">Parameter</span></span>          | <span data-ttu-id="ffd1c-122">Описание</span><span class="sxs-lookup"><span data-stu-id="ffd1c-122">Description</span></span>                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd1c-123">*пбаутпутдата*</span><span class="sxs-lookup"><span data-stu-id="ffd1c-123">*pbOutputData*</span></span>     | <span data-ttu-id="ffd1c-124">Это указатель **байта** на буфер, где ваша реализация **допроцессаутпут** должна скопировать обработанные данные.</span><span class="sxs-lookup"><span data-stu-id="ffd1c-124">This is a **BYTE** pointer to the buffer where your implementation of **DoProcessOutput** must copy its processed data.</span></span> |
| <span data-ttu-id="ffd1c-125">*пбинпутдата*</span><span class="sxs-lookup"><span data-stu-id="ffd1c-125">*pbInputData*</span></span>      | <span data-ttu-id="ffd1c-126">Это постоянный указатель **байта** на буфер, содержащий обрабатываемые данные.</span><span class="sxs-lookup"><span data-stu-id="ffd1c-126">This is a constant **BYTE** pointer to the buffer that contains the data to be processed.</span></span>                               |
| <span data-ttu-id="ffd1c-127">*кббитестопроцесс*</span><span class="sxs-lookup"><span data-stu-id="ffd1c-127">*cbBytesToProcess*</span></span> | <span data-ttu-id="ffd1c-128">Это значение **типа DWORD** , содержащее количество байтов во входном буфере для обработки.</span><span class="sxs-lookup"><span data-stu-id="ffd1c-128">This is a **DWORD** value that contains a count of the number of bytes in the input buffer to be processed.</span></span>             |



 

<span data-ttu-id="ffd1c-129">В следующих разделах содержатся сведения о том, как изменить код, созданный мастером подключаемых модулей проигрывателя Windows Media, чтобы создать собственный подключаемый модуль DSP для аудио.</span><span class="sxs-lookup"><span data-stu-id="ffd1c-129">The following sections provide details about how to modify the code generated by the Windows Media Player Plug-in Wizard to create your own audio DSP plug-in:</span></span>

-   [<span data-ttu-id="ffd1c-130">Реализация Допроцессаутпут</span><span class="sxs-lookup"><span data-stu-id="ffd1c-130">Implementing DoProcessOutput</span></span>](implementing-doprocessoutput.md)
-   [<span data-ttu-id="ffd1c-131">Добавление свойств в образец подключаемого модуля DSP для аудио</span><span class="sxs-lookup"><span data-stu-id="ffd1c-131">Adding Properties to the Sample Audio DSP Plug-in</span></span>](adding-properties-to-the-sample-audio-dsp-plug-in.md)
-   [<span data-ttu-id="ffd1c-132">Реализация страницы свойств для подключаемого модуля DSP</span><span class="sxs-lookup"><span data-stu-id="ffd1c-132">Implementing the Property Page for a DSP Plug-in</span></span>](implementing-the-property-page-for-a-dsp-plug-in.md)
-   [<span data-ttu-id="ffd1c-133">Изменение примера свойства подключаемого модуля DSP аудиоподсистемы</span><span class="sxs-lookup"><span data-stu-id="ffd1c-133">Changing the Sample Audio DSP Plug-in Property</span></span>](changing-the-sample-audio-dsp-plug-in-property.md)
-   [<span data-ttu-id="ffd1c-134">О прекращении поддержки</span><span class="sxs-lookup"><span data-stu-id="ffd1c-134">About Discontinuity</span></span>](about-discontinuity.md)
-   [<span data-ttu-id="ffd1c-135">О выделении ресурсов потоковой передачи</span><span class="sxs-lookup"><span data-stu-id="ffd1c-135">About Allocating Streaming Resources</span></span>](about-allocating-streaming-resources.md)

## <a name="related-topics"></a><span data-ttu-id="ffd1c-136">См. также</span><span class="sxs-lookup"><span data-stu-id="ffd1c-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffd1c-137">**О подключаемых модулях DSP**</span><span class="sxs-lookup"><span data-stu-id="ffd1c-137">**About DSP Plug-ins**</span></span>](about-dsp-plug-ins.md)
</dt> </dl>

 

 




