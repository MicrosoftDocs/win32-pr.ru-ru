---
title: Использование подключаемого модуля "Echo Sample DSP"
description: Использование подключаемого модуля "Echo Sample DSP"
ms.assetid: 62e393a4-0787-40e2-8693-678971a25fbf
keywords:
- Подключаемые модули проигрывателя Windows Media, проверка эхо-образцов
- подключаемые модули, проверка эхо-образцов
- подключаемые модули обработки цифровых сигналов, Проверка образца эха
- Подключаемые модули DSP, Тестирование образца эха
- Пример подключаемого модуля Echo DSP, тестирование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47746f9e09db7b6cd0b93ec4eac74afaaba278b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700701"
---
# <a name="using-the-echo-sample-dsp-plug-in"></a><span data-ttu-id="6df88-108">Использование подключаемого модуля "Echo Sample DSP"</span><span class="sxs-lookup"><span data-stu-id="6df88-108">Using the Echo Sample DSP Plug-in</span></span>

<span data-ttu-id="6df88-109">Когда вы создаете бесплатную сборку подключаемого модуля Windows Media Player Echo DSP, вы можете использовать его в проигрывателе Windows Media, чтобы услышать этот результат.</span><span class="sxs-lookup"><span data-stu-id="6df88-109">When you create an error-free build of your Windows Media Player echo DSP plug-in, you can use it in Windows Media Player to hear the effect.</span></span> <span data-ttu-id="6df88-110">При запуске проигрывателя Windows Media подключаемый модуль должен быть включен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6df88-110">When you start Windows Media Player, the plug-in should be enabled by default.</span></span> <span data-ttu-id="6df88-111">Если вы воспроизводите аудио-или видеофайлы с аудио, вы должны слышать один и тот же звук, который воспроизводится на том же томе, что и исходный звук.</span><span class="sxs-lookup"><span data-stu-id="6df88-111">If you play audio or video with audio, you should hear a one-second echo in the sound that plays at the same volume as the original sound.</span></span>

<span data-ttu-id="6df88-112">Можно поэкспериментировать с различными уровнями времени задержки и эффектов, изменив значения на странице свойств подключаемый модуль Echo.</span><span class="sxs-lookup"><span data-stu-id="6df88-112">You can experiment with different delay times and effects levels by changing the values in the echo plug-in property page.</span></span> <span data-ttu-id="6df88-113">Попробуйте применить различные типы исходных материалов, например музыку или речь.</span><span class="sxs-lookup"><span data-stu-id="6df88-113">Try the effect on different types of source material, such as music or speech.</span></span> <span data-ttu-id="6df88-114">Время задержки 200 мс с уровнем влияния 30 приведет к жестко пробелому, что звучит так, как эффект, используемый на ранних рок и в записи отката.</span><span class="sxs-lookup"><span data-stu-id="6df88-114">A delay time of 200 ms with an effects level of 30 will result in a tightly spaced echo that sounds like the effect used on early rock and roll recordings.</span></span> <span data-ttu-id="6df88-115">Уровни эффектов, превышающие 50, приводят к тому, что исходный сигнал будет ниже по сравнению с эхо-выводом, который называется действием предварительного эха.</span><span class="sxs-lookup"><span data-stu-id="6df88-115">Effects levels greater than 50 will result in the original signal being lower in volume than the echo, which is called a pre-echo effect.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6df88-116">См. также</span><span class="sxs-lookup"><span data-stu-id="6df88-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6df88-117">**Пример эха**</span><span class="sxs-lookup"><span data-stu-id="6df88-117">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




