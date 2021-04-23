---
title: Сведения о примере подключаемого модуля DSP аудиоподсистемы
description: Сведения о примере подключаемого модуля DSP аудиоподсистемы
ms.assetid: e60b055b-77e6-470e-91f6-9882827cf238
keywords:
- Подключаемые модули проигрывателя Windows Media, примеры
- подключаемые модули, примеры
- подключаемые модули обработки цифровых сигналов, примеры
- Подключаемые модули DSP, примеры
- Подключаемые модули проигрывателя Windows Media, DSP аудиоподсистемы
- подключаемые модули, DSP аудиоподсистемы
- подключаемые модули обработки цифровых сигналов, образцы аудио
- Подключаемые модули DSP, аудио-примеры
- Примеры, подключаемые модули DSP
- подключаемые модули DSP аудио, примеры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edc3a5860c0c52837bfece16d2e709bf16d836d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330112"
---
# <a name="about-the-sample-audio-dsp-plug-in"></a><span data-ttu-id="33792-113">Сведения о примере подключаемого модуля DSP аудиоподсистемы</span><span class="sxs-lookup"><span data-stu-id="33792-113">About the Sample Audio DSP Plug-in</span></span>

<span data-ttu-id="33792-114">Пример подключаемого модуля DSP аудиоподсистемы предоставляет простую реализацию обработки, которая масштабирует амплитуду звука по фактору, предоставленному пользователем на странице свойств.</span><span class="sxs-lookup"><span data-stu-id="33792-114">The sample audio DSP plug-in provides a simple processing implementation that scales the amplitude of the audio by a factor provided by the user in the property page.</span></span> <span data-ttu-id="33792-115">Подключаемый модуль принимает значения от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="33792-115">The plug-in accepts values between zero and 1.</span></span> <span data-ttu-id="33792-116">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="33792-116">The default value is 1.</span></span> <span data-ttu-id="33792-117">Значение 1 не влияет на звук; другие коэффициенты масштабирования — это множители для звуковых образцов.</span><span class="sxs-lookup"><span data-stu-id="33792-117">A value of 1 has no effect upon the sound; other scale factors are multipliers for the audio samples.</span></span> <span data-ttu-id="33792-118">Например, значение 0,5 приведет к снижению объема тома в 6 шкала.</span><span class="sxs-lookup"><span data-stu-id="33792-118">For instance, a value of .5 would result in a 6 decibel decrease in volume.</span></span> <span data-ttu-id="33792-119">Нулевое значение приводит к отсутствию тишины.</span><span class="sxs-lookup"><span data-stu-id="33792-119">A value of zero results in silence.</span></span>

<span data-ttu-id="33792-120">Пример подключаемого модуля DSP для аудиоподсистемы работает с аудио-или моно PCM.</span><span class="sxs-lookup"><span data-stu-id="33792-120">The sample audio DSP plug-in works with stereo or mono PCM audio.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33792-121">См. также</span><span class="sxs-lookup"><span data-stu-id="33792-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33792-122">**Создание подключаемого модуля DSP**</span><span class="sxs-lookup"><span data-stu-id="33792-122">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




