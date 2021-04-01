---
title: Функция PlaySound
description: Функция PlaySound
ms.assetid: ce405a13-c4ab-4c9a-bcfe-8d4427b3d2d8
keywords:
- мультимедиа Audio, функция PlaySound
- Audio, функция PlaySound
- волна Audio, функция PlaySound
- PlaySound, функция
- Функция Сндплайсаунд
- PlaySound, функция по сравнению с функцией Сндплайсаунд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5723b1937c974e6c622c1f2010e8d2129e787cdd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104260522"
---
# <a name="the-playsound-function"></a><span data-ttu-id="6041e-109">Функция PlaySound</span><span class="sxs-lookup"><span data-stu-id="6041e-109">The PlaySound Function</span></span>

<span data-ttu-id="6041e-110">Функцию [**PlaySound**](/previous-versions//dd743680(v=vs.85)) можно использовать для воспроизведения звука звукозаписи, если звук умещается в доступную память.</span><span class="sxs-lookup"><span data-stu-id="6041e-110">You can use the [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function to play waveform audio if the sound fits into available memory.</span></span> <span data-ttu-id="6041e-111">(Функция [**сндплайсаунд**](/previous-versions//dd798676(v=vs.85)) предлагает подмножество возможностей PlaySound.</span><span class="sxs-lookup"><span data-stu-id="6041e-111">(The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function offers a subset of the capabilities of PlaySound.</span></span> <span data-ttu-id="6041e-112">Чтобы максимально увеличить переносимость приложения на основе Win32, используйте **PlaySound**, а не **сндплайсаунд**.)</span><span class="sxs-lookup"><span data-stu-id="6041e-112">To maximize the portability of your Win32-based application, use **PlaySound**, not **sndPlaySound**.)</span></span>

<span data-ttu-id="6041e-113">Функция **PlaySound** позволяет указать звук одним из трех способов:</span><span class="sxs-lookup"><span data-stu-id="6041e-113">The **PlaySound** function allows you to specify a sound in one of three ways:</span></span>

-   <span data-ttu-id="6041e-114">В качестве системного предупреждения используйте псевдоним, хранящийся в файле WIN.INI или в реестре.</span><span class="sxs-lookup"><span data-stu-id="6041e-114">As a system alert, using the alias stored in the WIN.INI file or the registry</span></span>
-   <span data-ttu-id="6041e-115">Как имя файла</span><span class="sxs-lookup"><span data-stu-id="6041e-115">As a filename</span></span>
-   <span data-ttu-id="6041e-116">Как идентификатор ресурса</span><span class="sxs-lookup"><span data-stu-id="6041e-116">As a resource identifier</span></span>

<span data-ttu-id="6041e-117">Функция [**PlaySound**](/previous-versions//dd743680(v=vs.85)) позволяет воспроизводить звук в непрерывном цикле, заканчивая только при повторном вызове **PlaySound** , указывая **значение NULL** или идентификатор звука другого звука для параметра *псзсаунд* .</span><span class="sxs-lookup"><span data-stu-id="6041e-117">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function allows you to play a sound in a continuous loop, ending only when you call **PlaySound** again, specifying either **NULL** or the sound identifier of another sound for the *pszSound* parameter.</span></span>

<span data-ttu-id="6041e-118">Функцию **PlaySound** можно использовать для синхронного или асинхронного воспроизведения звука, а также для управления поведением функции другими способами, когда она должна предоставлять общий доступ к системным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="6041e-118">You can use **PlaySound** to play the sound synchronously or asynchronously, and to control the behavior of the function in other ways when it must share system resources.</span></span>

<span data-ttu-id="6041e-119">Дополнительные сведения об использовании функции PlaySound см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="6041e-119">For more information about using PlaySound, see the following topics:</span></span>

-   [<span data-ttu-id="6041e-120">Использование функции PlaySound для воспроизведения Waveform-Audio файлов</span><span class="sxs-lookup"><span data-stu-id="6041e-120">Using PlaySound to Play Waveform-Audio Files</span></span>](using-playsound-to-play-waveform-audio-files.md)
-   [<span data-ttu-id="6041e-121">Использование функции PlaySound для цикла звуков</span><span class="sxs-lookup"><span data-stu-id="6041e-121">Using PlaySound to Loop Sounds</span></span>](using-playsound-to-loop-sounds.md)
-   [<span data-ttu-id="6041e-122">Использование функции PlaySound для воспроизведения системных звуков</span><span class="sxs-lookup"><span data-stu-id="6041e-122">Using PlaySound to Play System Sounds</span></span>](using-playsound-to-play-system-sounds.md)

<span data-ttu-id="6041e-123">Дополнительные примеры использования **PlaySound** в приложениях на основе Win32 см. в разделе [Воспроизведение звуковых ресурсов](playing-wave-resources.md).</span><span class="sxs-lookup"><span data-stu-id="6041e-123">For more examples of how to use **PlaySound** in your Win32-based applications, see [Playing WAVE Resources](playing-wave-resources.md).</span></span>

 

 