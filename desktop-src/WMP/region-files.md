---
title: Файлы регионов
description: Файлы регионов
ms.assetid: 20952eb9-4cd1-4d7d-b5cc-f1741977745f
keywords:
- Обложки Windows Media Player для мобильных устройств, графические файлы
- обложки, файлы Art
- файлы для обложек, изображений
- графические файлы для обложек, файлов регионов
- Обложки мобильных приложений проигрывателя Windows Media, файлы регионов
- обложки, файлы регионов
- Файлы регионов в обложках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d258afeab029df7218d3616b8aecdb62c72806
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332112"
---
# <a name="region-files"></a><span data-ttu-id="4047c-110">Файлы регионов</span><span class="sxs-lookup"><span data-stu-id="4047c-110">Region Files</span></span>

<span data-ttu-id="4047c-111">Файлы регионов требуются, если используется любой тип кнопки нажатия (2PushHit, Пушхит или Тогглехит).</span><span class="sxs-lookup"><span data-stu-id="4047c-111">Region files are required if you use any type of hit button (2PushHit, PushHit, or ToggleHit).</span></span>

<span data-ttu-id="4047c-112">Файлы регионов используются для определения областей, которые будут реагировать на касание, которое также называется нажатием, на определенной кнопке.</span><span class="sxs-lookup"><span data-stu-id="4047c-112">Region files are used to define areas that will respond to a tap, also known as a hit, on a specific button.</span></span> <span data-ttu-id="4047c-113">Для каждого переключателя область в битовой карте области получает определенный веб-цвет (например \# , FF0000, который является значением сплошного красного цвета).</span><span class="sxs-lookup"><span data-stu-id="4047c-113">For each hit button, an area in the Region bitmap is given a specific Web color (such as \#FF0000, which is the value for solid red).</span></span> <span data-ttu-id="4047c-114">Номер цвета задается в определении кнопки региона.</span><span class="sxs-lookup"><span data-stu-id="4047c-114">The color number is specified in the region button definition.</span></span> <span data-ttu-id="4047c-115">Когда пользователь отображает обложку, изображение кнопки переносится на задний план с помощью координат области в битовой карте области.</span><span class="sxs-lookup"><span data-stu-id="4047c-115">When the user displays the skin, the button image is superimposed onto the background using the coordinates of the area in the Region bitmap.</span></span>

<span data-ttu-id="4047c-116">Например, можно нарисовать красный круг в месте, соответствующем расположению кнопки Далее, и окрасить его в красный цвет ( \# FF0000).</span><span class="sxs-lookup"><span data-stu-id="4047c-116">For example, you could draw a red circle in a location corresponding to the location of the Next button and color it solid red (\#FF0000).</span></span> <span data-ttu-id="4047c-117">Затем в определении кнопки можно присвоить значение RGB, равное 255, 0, 0 (то есть RGB-эквивалент \# FF0000).</span><span class="sxs-lookup"><span data-stu-id="4047c-117">Then in the button definition, you could assign a hit RGB value of 255,0,0 (which is the RGB equivalent of \#FF0000).</span></span> <span data-ttu-id="4047c-118">В этом случае кнопка Далее будет реагировать только на касания (попадания) в красном круге.</span><span class="sxs-lookup"><span data-stu-id="4047c-118">In this case, the Next button would only respond to taps (hits) inside the red circle.</span></span>

<span data-ttu-id="4047c-119">Кнопки нажатия используются, если требуется определить фигуры, отличные от прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="4047c-119">Hit buttons are used when you want to define shapes other than rectangles.</span></span> <span data-ttu-id="4047c-120">Необходимо по-прежнему определить координаты каждой кнопки, чтобы дополнительные образы, такие как отправленные и отключенные, могли быть правильно обнаружены.</span><span class="sxs-lookup"><span data-stu-id="4047c-120">You must still define the coordinates for each button so that secondary images such as Pushed and Disabled can be located correctly.</span></span> <span data-ttu-id="4047c-121">На практике каждая кнопка ограничена прямоугольником, и эти мнимые ограничивающие прямоугольники не должны перекрываться.</span><span class="sxs-lookup"><span data-stu-id="4047c-121">In practice, each button is bounded by a rectangle, and these imaginary boundary rectangles must not overlap.</span></span>

> [!Note]  
> <span data-ttu-id="4047c-122">Графические файлы не нужны в обложек проигрывателя Windows Media 10 для мобильных устройств, так как типы кнопок не поддерживаются в проигрывателе Windows Media 10 Mobile или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="4047c-122">Region art files are not needed in Windows Media Player 10 Mobile skins because button types are not supported in Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="4047c-123">На следующем рисунке изображен типичный файл региона.</span><span class="sxs-lookup"><span data-stu-id="4047c-123">The following image is a typical Region file.</span></span>

![файл региона](images/cesdkreg.png)

<span data-ttu-id="4047c-125">Этот файл определяет части обложки для каждой кнопки типа попадания.</span><span class="sxs-lookup"><span data-stu-id="4047c-125">This file defines the parts of the skin for each hit-type button.</span></span> <span data-ttu-id="4047c-126">Каждый цвет будет идентифицироваться по номеру цвета в разделе кнопки файла определения обложки.</span><span class="sxs-lookup"><span data-stu-id="4047c-126">Each color will be identified by its color number in the Buttons section of the skin definition file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4047c-127">См. также</span><span class="sxs-lookup"><span data-stu-id="4047c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4047c-128">**Файлы изображений**</span><span class="sxs-lookup"><span data-stu-id="4047c-128">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




