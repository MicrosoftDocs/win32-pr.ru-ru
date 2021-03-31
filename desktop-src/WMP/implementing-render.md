---
title: Реализация отрисовки
description: Реализация отрисовки
ms.assetid: 9b3a64f6-6803-457c-8e63-e8a799089e18
keywords:
- визуализации, события с превышением времени
- Пользовательские визуализации, события с превышением времени
- визуализации, функция Render
- Пользовательские визуализации, функция Render
- визуализации, функция Рендервиндов
- Пользовательские визуализации, функция Рендервиндов
- Функция Render, параметры
- Функция Рендервиндов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99db0a96a07c361d18de579fb0235befa11838c8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069573"
---
# <a name="implementing-render"></a><span data-ttu-id="8f9a2-111">Реализация отрисовки</span><span class="sxs-lookup"><span data-stu-id="8f9a2-111">Implementing Render</span></span>

<span data-ttu-id="8f9a2-112">Самый простой способ представить программирование визуализации — создать обработчик для события с превышением времени.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-112">The easiest way to think of visualization programming is that you are creating a handler for a timed event.</span></span> <span data-ttu-id="8f9a2-113">Через определенные интервалы проигрыватель Windows Media создает моментальный снимок воспроизводимых звуковых данных и предоставляет данные моментального снимка загруженной в данный момент визуализации.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-113">At specific intervals, Windows Media Player takes a snapshot of the audio data it is playing, and provides the snapshot data to the currently loaded visualization.</span></span> <span data-ttu-id="8f9a2-114">Это аналогично программированию на основе событий и является частью модели программирования Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-114">This is similar to event-driven programming and is part of the programming model of Microsoft Windows.</span></span> <span data-ttu-id="8f9a2-115">Написание кода и ожидание его вызова с помощью определенного события.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-115">You write code and wait for it to be called by a particular event.</span></span>

<span data-ttu-id="8f9a2-116">Если код является реализацией функции [ивмпеффектс:: Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) для отрисовки в режиме без окон, он получает следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="8f9a2-116">If your code is an implementation of the [IWMPEffects::Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) function for rendering in windowless mode, it receives the following parameters:</span></span>

<span data-ttu-id="8f9a2-117">*тимедлевел*</span><span class="sxs-lookup"><span data-stu-id="8f9a2-117">*TimedLevel*</span></span>

<span data-ttu-id="8f9a2-118">Это структура, определяющая звуковые данные, которые будет анализировать ваш код.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-118">This is a structure that defines the audio data your code will be analyzing.</span></span> <span data-ttu-id="8f9a2-119">Структура состоит из двух массивов.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-119">The structure is composed of two arrays.</span></span> <span data-ttu-id="8f9a2-120">Первый массив основан на сведениях о частоте и содержит моментальный снимок спектра звука, разделенного на части 1024.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-120">The first array is based on frequency information and contains a snapshot of the audio spectrum divided into 1024 portions.</span></span> <span data-ttu-id="8f9a2-121">Каждая ячейка массива содержит значение от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-121">Each cell of the array contains a value from 0 to 255.</span></span> <span data-ttu-id="8f9a2-122">Первая ячейка начинается с 20 Гц, а последняя — в 22050 Гц.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-122">The first cell starts at 20 Hz and the last at 22050 Hz.</span></span> <span data-ttu-id="8f9a2-123">Массив является двумя размерами для представления стерео аудио.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-123">The array is two dimensional to represent stereo audio.</span></span> <span data-ttu-id="8f9a2-124">Второй массив основан на сведениях о звуковой волны и соответствует питанию звука, где, в большей степени, это большее значение.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-124">The second array is based on waveform information and corresponds to audio power, where the stronger the wave is, the larger the value.</span></span> <span data-ttu-id="8f9a2-125">Массив форм-волнового сигнала — это детализированный моментальный снимок последних 1024 срезов звукового питания, которые потребовались через небольшие интервалы времени.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-125">The waveform array is a granular snapshot of the last 1024 slices of audio power taken at very small time intervals.</span></span> <span data-ttu-id="8f9a2-126">Этот массив также является двумя размерами для представления стерео аудио.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-126">This array also is two dimensional to represent stereo audio.</span></span>

<span data-ttu-id="8f9a2-127">*HDC*</span><span class="sxs-lookup"><span data-stu-id="8f9a2-127">*HDC*</span></span>

<span data-ttu-id="8f9a2-128">Это обработчик Microsoft Windows для контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-128">This is a Microsoft Windows handle to a device context.</span></span> <span data-ttu-id="8f9a2-129">Это позволяет опознать поверхность рисования в Windows.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-129">This gives a way to identify the drawing surface to Windows.</span></span> <span data-ttu-id="8f9a2-130">Его не нужно создавать, нужно просто использовать его для конкретных вызовов функций рисования.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-130">You do not need to create it, you just need to use it for specific drawing function calls.</span></span>

<span data-ttu-id="8f9a2-131">*ПЕРЕТАСКИВАЕМЫЕ*</span><span class="sxs-lookup"><span data-stu-id="8f9a2-131">*RECT*</span></span>

<span data-ttu-id="8f9a2-132">Это прямоугольник Microsoft Windows, который определяет размер поверхности рисования.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-132">This is a Microsoft Windows rectangle that defines the size of a drawing surface.</span></span> <span data-ttu-id="8f9a2-133">Это простой прямоугольник с четырьмя свойствами: **слева**, **справа**, **сверху** и **снизу**.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-133">This is a simple rectangle with four properties: **left**, **right**, **top**, and **bottom**.</span></span> <span data-ttu-id="8f9a2-134">Фактические значения предоставляются проигрывателем Windows Media, что позволяет определить, каким образом пользователь или Обложка определяет размер окна, на котором будет проводиться рисование.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-134">The actual values are supplied by Windows Media Player so that you can determine how the user or skin developer has sized the window you will draw on.</span></span> <span data-ttu-id="8f9a2-135">Он также определяет расположение в HDC, на котором ожидается отрисовка результата.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-135">It also determines the position on the HDC that the effect is supposed to render on.</span></span>

<span data-ttu-id="8f9a2-136">Если код является реализацией функции **IWMPEffects2:: рендервиндовед** для отрисовки в окне, он получает следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="8f9a2-136">If your code is an implementation of the **IWMPEffects2::RenderWindowed** function for rendering in a window, it receives the following parameters:</span></span>

<span data-ttu-id="8f9a2-137">*тимедлевел*</span><span class="sxs-lookup"><span data-stu-id="8f9a2-137">*TimedLevel*</span></span>

<span data-ttu-id="8f9a2-138">Это те же сведения, которые получает функция **Render** .</span><span class="sxs-lookup"><span data-stu-id="8f9a2-138">This is the same information that the **Render** function receives.</span></span>

<span data-ttu-id="8f9a2-139">*фрекуиредрендер*</span><span class="sxs-lookup"><span data-stu-id="8f9a2-139">*fRequiredRender*</span></span>

<span data-ttu-id="8f9a2-140">Параметр *фрекуиредрендер* информирует вас, что визуализация должна перерисовываться, например, когда на него перетаскивается другое окно.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-140">The *fRequiredRender* parameter informs you that your visualization must repaint itself—for example, when another window is dragged over it.</span></span> <span data-ttu-id="8f9a2-141">Если это значение равно false, можно спокойно пропустить код отрисовки, если текущий элемент мультимедиа остановлен или приостановлен.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-141">When this value is false, you can safely skip over the rendering code if the current media item is stopped or paused.</span></span> <span data-ttu-id="8f9a2-142">Это позволяет избежать необязательного использования циклов ЦП.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-142">This lets you avoid consuming CPU cycles unnecessarily.</span></span>

<span data-ttu-id="8f9a2-143">Образец подключаемого модуля, созданный мастером подключаемых модулей, не предоставляет пользовательскую реализацию для **рендервиндовед**.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-143">The sample plug-in generated by the Plug-in Wizard does not provide a custom implementation for **RenderWindowed**.</span></span> <span data-ttu-id="8f9a2-144">Вместо этого пример кода подключаемого модуля получает контекст устройства из родительского окна, предоставляемого проигрывателем Windows Media в [IWMPEffects2:: Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create), затем получает размеры родительского окна в виде структуры Rect, а затем вызывает метод для **отрисовки** с использованием контекста устройства, Rect и указателя на уровень времени из **рендервиндовед**.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-144">Instead, the sample plug-in code retrieves the device context from the parent window provided by Windows Media Player in [IWMPEffects2::Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create), then retrieves the dimensions of the parent window as a RECT structure, and then calls through to **Render** using the device context, the RECT, and the timed level pointer from **RenderWindowed**.</span></span>

<span data-ttu-id="8f9a2-145">В следующих разделах содержатся дополнительные сведения о реализации **отрисовки**.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-145">The following sections provide more information about implementing **Render**:</span></span>

-   [<span data-ttu-id="8f9a2-146">Использование уровней времени</span><span class="sxs-lookup"><span data-stu-id="8f9a2-146">Using Timed Levels</span></span>](using-timed-levels.md)
-   [<span data-ttu-id="8f9a2-147">Использование контекстов устройств</span><span class="sxs-lookup"><span data-stu-id="8f9a2-147">Using Device Contexts</span></span>](using-device-contexts.md)
-   [<span data-ttu-id="8f9a2-148">Использование прямоугольников</span><span class="sxs-lookup"><span data-stu-id="8f9a2-148">Using Rectangles</span></span>](using-rectangles.md)
-   [<span data-ttu-id="8f9a2-149">Пример кода рендеринга</span><span class="sxs-lookup"><span data-stu-id="8f9a2-149">Sample Render Code</span></span>](sample-render-code.md)

## <a name="related-topics"></a><span data-ttu-id="8f9a2-150">См. также</span><span class="sxs-lookup"><span data-stu-id="8f9a2-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f9a2-151">**Реализация кода**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-151">**Implementing Your Code**</span></span>](implementing-your-code.md)
</dt> </dl>

 

 




