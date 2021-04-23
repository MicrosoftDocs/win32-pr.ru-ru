---
title: Допроцессаутпут в примере подключаемого модуля DSP видео
description: Допроцессаутпут в примере подключаемого модуля DSP видео
ms.assetid: 67536e35-a049-49c8-bd89-fad1fab37e6c
keywords:
- Подключаемые модули проигрывателя Windows Media, DSP видео
- подключаемые модули, DSP видео
- подключаемые модули обработки цифровых сигналов, Допроцессаутпут
- Подключаемые модули DSP, Допроцессаутпут
- подключаемые модули DSP видео, Допроцессаутпут
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3bc844890930209a1c6007213d3c466f0cd15b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691154"
---
# <a name="doprocessoutput-in-the-sample-video-dsp-plug-in"></a><span data-ttu-id="a3165-108">Допроцессаутпут в примере подключаемого модуля DSP видео</span><span class="sxs-lookup"><span data-stu-id="a3165-108">DoProcessOutput in the Sample Video DSP Plug-in</span></span>

<span data-ttu-id="a3165-109">Так как подключаемый модуль DSP видео обычно поддерживает несколько форматов видео, удобно разделить код реализации обработки на отдельную функцию для каждого формата.</span><span class="sxs-lookup"><span data-stu-id="a3165-109">Because a video DSP plug-in typically supports several video formats, it is convenient to separate the processing implementation code into a separate function for each format.</span></span> <span data-ttu-id="a3165-110">Это означает, что реализация **допроцессаутпут** для подключаемых модулей DSP видео относительно проста.</span><span class="sxs-lookup"><span data-stu-id="a3165-110">This means that the implementation of **DoProcessOutput** for video DSP plug-ins is relatively simple.</span></span>

<span data-ttu-id="a3165-111">Реализация в примере подключаемого модуля сначала проверяет, включил ли пользователь подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="a3165-111">The implementation in the sample plug-in first tests whether the user has enabled the plug-in.</span></span> <span data-ttu-id="a3165-112">Если подключаемый модуль отключен, код копирует данные, содержащиеся во входном буфере, в выходной буфер, не изменяя его, как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="a3165-112">If the plug-in is disabled, the code copies the data provided in the input buffer to the output buffer without changing it, as the following code demonstrates:</span></span>


```C++
// Test whether the plug-in has been disabled by the user.
if (!m_bEnabled)
{
    // Just copy the data without changing it. You should
    // also do any necessary format conversion here.
    memcpy(pbOutputData, pbInputData, m_dwBufferSize);
    *cbBytesProcessed = m_dwBufferSize;

    return S_OK;
}

```



<span data-ttu-id="a3165-113">Если подключаемый модуль включен, код просто выполняет ряд **проверок элемента подтип входного типа носителя** , чтобы определить текущий формат видео.</span><span class="sxs-lookup"><span data-stu-id="a3165-113">If the plug-in is enabled, the code simply performs a series of checks on the input media type **subtype** member to determine the current video format.</span></span> <span data-ttu-id="a3165-114">При обнаружении совпадения код вызывает соответствующую функцию обработки.</span><span class="sxs-lookup"><span data-stu-id="a3165-114">When a match is found, the code calls the appropriate processing function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3165-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a3165-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3165-116">**Реализация подключаемого модуля DSP видео**</span><span class="sxs-lookup"><span data-stu-id="a3165-116">**Implementing a Video DSP Plug-in**</span></span>](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




