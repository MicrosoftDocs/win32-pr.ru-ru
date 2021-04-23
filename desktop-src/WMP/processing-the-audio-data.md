---
title: Обработка звуковых данных
description: Обработка звуковых данных
ms.assetid: ba41e3f4-d991-4da6-9091-7a7e42622e76
keywords:
- Подключаемые модули проигрывателя Windows Media, метод Echo Sample Допроцессаутпут
- подключаемые модули, метод Echo Sample Допроцессаутпут
- подключаемые модули обработки цифровых сигналов, метод Echo Sample Допроцессаутпут
- Подключаемые модули DSP, метод Echo Sample Допроцессаутпут
- Пример подключаемого модуля Echo DSP, метод Допроцессаутпут
- Пример подключаемого модуля Echo DSP, звуковые данные
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc14acb99aed20825ff970025363c6a795a0c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700629"
---
# <a name="processing-the-audio-data"></a><span data-ttu-id="821de-109">Обработка звуковых данных</span><span class="sxs-lookup"><span data-stu-id="821de-109">Processing the Audio Data</span></span>

<span data-ttu-id="821de-110">Реализация **допроцессаутпут** по умолчанию начинается с получения указателя на допустимую структуру **вавеформатекс** , точно так же, как было сделано в **аллокатестреамингресаурцес**.</span><span class="sxs-lookup"><span data-stu-id="821de-110">The default implementation of **DoProcessOutput** begins by retrieving a pointer to a valid **WAVEFORMATEX** structure, exactly like was done in **AllocateStreamingResources**.</span></span> <span data-ttu-id="821de-111">Затем он использует информацию в этой структуре для вычисления количества выборок во входном буфере, ожидающих обработки.</span><span class="sxs-lookup"><span data-stu-id="821de-111">It then uses the information in that structure to calculate the number of samples in the input buffer waiting to be processed.</span></span> <span data-ttu-id="821de-112">Следующий код из реализации по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="821de-112">The following code is from the default implementation:</span></span>


```C++
// Get a pointer to the valid WAVEFORMATEX structure
// for the current media type.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;

// Calculate the number of samples to process.
DWORD dwSamplesToProcess = (*cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;

```



<span data-ttu-id="821de-113">Затем код проверяет элемент **вбитсперсампле** , чтобы определить битовую глубину звука.</span><span class="sxs-lookup"><span data-stu-id="821de-113">Then, the code inspects the **wBitsPerSample** member to determine the bit depth of the audio.</span></span> <span data-ttu-id="821de-114">Это значение используется в операторе switch, чтобы обеспечить отдельную обработку для 8-разрядных и 16-разрядных аудио.</span><span class="sxs-lookup"><span data-stu-id="821de-114">This value is used in a switch statement to provide separate processing for 8-bit and 16-bit audio.</span></span>

## <a name="differences-between-8-bit-and-16-bit-audio"></a><span data-ttu-id="821de-115">Различия между 8-разрядным и 16-разрядным звуком</span><span class="sxs-lookup"><span data-stu-id="821de-115">Differences Between 8-bit and 16-bit Audio</span></span>

<span data-ttu-id="821de-116">Между 8-и 16-разрядным звуком связаны важные различия.</span><span class="sxs-lookup"><span data-stu-id="821de-116">There are important differences between 8-bit and 16-bit audio.</span></span> <span data-ttu-id="821de-117">Таким образом, подпрограммы обработки для создания эффекта эха отличаются.</span><span class="sxs-lookup"><span data-stu-id="821de-117">Therefore, the processing routines to create the echo effect are different.</span></span> <span data-ttu-id="821de-118">Два формата различаются следующими способами.</span><span class="sxs-lookup"><span data-stu-id="821de-118">The two formats differ in the following ways:</span></span>

-   <span data-ttu-id="821de-119">Каждый формат имеет другой размер выборки: 8-разрядные образцы каждый из них занимают один байт памяти, а 16-разрядные — в каждом из двух байтов.</span><span class="sxs-lookup"><span data-stu-id="821de-119">Each format has a different sample size: 8-bit samples each occupy one byte of memory, while 16-bit samples each occupy two bytes.</span></span>
-   <span data-ttu-id="821de-120">Каждый формат представляет амплитуду звука по-разному.</span><span class="sxs-lookup"><span data-stu-id="821de-120">Each format represents the audio amplitude differently.</span></span> <span data-ttu-id="821de-121">8-разрядный звук представлен целым числом без знака в диапазоне от 0 до 255; значение 128 представляет тишину.</span><span class="sxs-lookup"><span data-stu-id="821de-121">8-bit audio is represented by an unsigned integer with a range from 0 to 255; a value of 128 represents silence.</span></span> <span data-ttu-id="821de-122">16-разрядный звук представлен целым числом со знаком в диапазоне от-32768 до 32767; нулевое значение обозначает тишину.</span><span class="sxs-lookup"><span data-stu-id="821de-122">16-bit audio is represented by a signed integer with a range from -32768 to 32767; a value of zero represents silence.</span></span>

<span data-ttu-id="821de-123">Несмотря на то что процесс создания эхо-эффекта является принципиально идентичным для каждого формата, сведения должны слегка отличаться.</span><span class="sxs-lookup"><span data-stu-id="821de-123">While the process of creating the echo effect is fundamentally identical for each format, the details must differ slightly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="821de-124">См. также</span><span class="sxs-lookup"><span data-stu-id="821de-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="821de-125">**Реализация Цечо::D Опроцессаутпут**</span><span class="sxs-lookup"><span data-stu-id="821de-125">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




