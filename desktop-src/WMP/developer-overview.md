---
title: Обзор для разработчиков
description: Обзор для разработчиков
ms.assetid: 72a330b4-5957-4159-b5e8-0c9a4491b589
keywords:
- Подключаемые модули проигрывателя Windows Media, визуализации
- подключаемые модули, визуализации
- визуализации, обзор для разработчиков
- Пользовательские визуализации, обзор для разработчиков
- визуализации, элементы управления COM
- Пользовательские визуализации, элементы управления COM
- визуализации, звуковые входные данные
- Пользовательские визуализации, звуковые входные данные
- визуализации, графические выходные данные
- Пользовательские визуализации, графические выходные данные
- визуализации, средства рисования
- Пользовательские визуализации, средства рисования
- визуализации, язык программирования
- Пользовательские визуализации, язык программирования
- визуализации, Visual C++
- Пользовательские визуализации, Visual C++
- визуализации, мастер подключаемых модулей
- Пользовательские визуализации, мастер подключаемых модулей
- Мастер подключаемых модулей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ec8632bd5611e081a4a17d1b0390dc99a09703
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331115"
---
# <a name="developer-overview"></a><span data-ttu-id="1b752-122">Обзор для разработчиков</span><span class="sxs-lookup"><span data-stu-id="1b752-122">Developer Overview</span></span>

<span data-ttu-id="1b752-123">С точки зрения разработчика визуализации представляют собой программные программы, которые принимают звуковые данные, предоставляемые проигрывателем Windows Media, и преобразуют эти данные в графические объекты, которые будут видеть пользователь.</span><span class="sxs-lookup"><span data-stu-id="1b752-123">From the developer's point of view, visualizations are software programs that take audio data provided by Windows Media Player and convert that data to graphics that will please the eye of the user.</span></span> <span data-ttu-id="1b752-124">Основные темы, которые разработчику необходимо понять для создания новой визуализации, следующие:</span><span class="sxs-lookup"><span data-stu-id="1b752-124">The main subjects a developer needs to understand to create a new visualization are the following:</span></span>

## <a name="visualization-packaging"></a><span data-ttu-id="1b752-125">Упаковка визуализации</span><span class="sxs-lookup"><span data-stu-id="1b752-125">Visualization Packaging</span></span>

<span data-ttu-id="1b752-126">Визуализации — это элементы управления COM, которые проигрыватель Windows Media использует для преобразования звуковых сигналов в анимированную графику в Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1b752-126">Visualizations are COM controls that Windows Media Player uses to turn audio waveforms into animated graphics in Microsoft Windows.</span></span> <span data-ttu-id="1b752-127">Элементы управления COM упаковываются в виде библиотек динамической компоновки (DLL) Microsoft Windows и должны быть зарегистрированы в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="1b752-127">The COM controls are packaged as Microsoft Windows dynamic-link libraries (DLLs) and must be registered in the Windows registry.</span></span> <span data-ttu-id="1b752-128">При запуске проигрывателя Windows Media зарегистрированные пользовательские визуализации загружаются и просматриваются в соответствии с инструкциями обложки, которые использует проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1b752-128">When Windows Media Player runs, registered custom visualizations are loaded and viewed in accordance with the instructions of the skin that Windows Media Player is using.</span></span>

## <a name="audio-input"></a><span data-ttu-id="1b752-129">Звуковые входные данные</span><span class="sxs-lookup"><span data-stu-id="1b752-129">Audio Input</span></span>

<span data-ttu-id="1b752-130">Проигрыватель Windows Media предоставляет коду моментальные снимки частоты звука и данных волны через определенные интервалы времени, измеряемые в долях секунды.</span><span class="sxs-lookup"><span data-stu-id="1b752-130">Windows Media Player provides your code with snapshots of audio frequency and waveform data at timed intervals measured in fractions of a second.</span></span> <span data-ttu-id="1b752-131">Интервал моментальных снимков внутренне определяется проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1b752-131">The snapshot interval is internally determined by the Windows Media Player.</span></span>

## <a name="graphical-output"></a><span data-ttu-id="1b752-132">Графические выходные данные</span><span class="sxs-lookup"><span data-stu-id="1b752-132">Graphical Output</span></span>

<span data-ttu-id="1b752-133">Графические выходные данные визуализации представляют собой контекст устройства Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1b752-133">The graphical output from your visualization is a Microsoft Windows device context.</span></span> <span data-ttu-id="1b752-134">Это Стандартная поверхность рисования Windows, которую можно рисовать при каждом предоставлении моментального снимка звука.</span><span class="sxs-lookup"><span data-stu-id="1b752-134">This is a standard Windows drawing surface that you can draw upon every time an audio snapshot is provided.</span></span> <span data-ttu-id="1b752-135">Все фоновые технологии Windows выполняются самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="1b752-135">All of the background Windows technology is taken care of for you.</span></span> <span data-ttu-id="1b752-136">Вам нужно просто рисовать в контексте устройства с помощью предоставленных звуковых данных.</span><span class="sxs-lookup"><span data-stu-id="1b752-136">You just have to draw on the device context with the audio data provided.</span></span>

## <a name="drawing-tools"></a><span data-ttu-id="1b752-137">Средства рисования</span><span class="sxs-lookup"><span data-stu-id="1b752-137">Drawing Tools</span></span>

<span data-ttu-id="1b752-138">Вы можете рисовать в контексте устройства с помощью стандартных функций Microsoft Windows интерфейс графических устройств (GDI), используя перья и кисти для создания макетов, которые изменяются в виде звуковых данных, предоставляемых проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1b752-138">You can draw on the device context with standard Microsoft Windows Graphics Device Interface (GDI) functions, using pens and brushes to create designs that are modified by the audio data supplied to you by Windows Media Player.</span></span> <span data-ttu-id="1b752-139">GDI предоставляет широкий набор средств рисования, которые могут создавать различные виды визуальных эффектов.</span><span class="sxs-lookup"><span data-stu-id="1b752-139">GDI provides a rich set of drawing tools that can create many kinds of visual effects.</span></span>

## <a name="programming-language"></a><span data-ttu-id="1b752-140">Язык программирования</span><span class="sxs-lookup"><span data-stu-id="1b752-140">Programming Language</span></span>

<span data-ttu-id="1b752-141">Microsoft Visual C++ 6,0 и более поздних версий — это единственный поддерживаемый язык для создания пользовательских визуализаций.</span><span class="sxs-lookup"><span data-stu-id="1b752-141">Microsoft Visual C++ 6.0 and higher is the only supported language for creating custom visualizations.</span></span>

## <a name="plug-in-wizard"></a><span data-ttu-id="1b752-142">Мастер подключаемых модулей</span><span class="sxs-lookup"><span data-stu-id="1b752-142">Plug-in Wizard</span></span>

<span data-ttu-id="1b752-143">Проигрыватель Windows Media предоставляет мастер COM, который можно добавить в Visual C++, который создаст базовый код, необходимый для визуализации.</span><span class="sxs-lookup"><span data-stu-id="1b752-143">Windows Media Player provides a COM wizard that you can add to Visual C++ that will generate the underlying code needed for your visualization.</span></span> <span data-ttu-id="1b752-144">Не только предоставляются исходные файлы, но и создается пример обложки для упрощения тестирования визуализации.</span><span class="sxs-lookup"><span data-stu-id="1b752-144">Not only are all source files provided, but a sample skin is generated to make it easy to test your visualization.</span></span> <span data-ttu-id="1b752-145">Созданный код создает визуализацию, похожую на линейчатые с двумя предустановками.</span><span class="sxs-lookup"><span data-stu-id="1b752-145">The generated code creates a visualization similar to Bars, with two presets.</span></span> <span data-ttu-id="1b752-146">Затем можно изменить код, чтобы создать собственную визуализацию.</span><span class="sxs-lookup"><span data-stu-id="1b752-146">You can then modify the code to create your own visualization.</span></span> <span data-ttu-id="1b752-147">Файл реестра также создается для регистрации визуализации, чтобы проигрыватель Windows Media мог загрузить его.</span><span class="sxs-lookup"><span data-stu-id="1b752-147">A registry file is also generated to register your visualization so that Windows Media Player can load it.</span></span>

<span data-ttu-id="1b752-148">В следующем разделе описано, как код визуализации обрабатывает звуковые данные.</span><span class="sxs-lookup"><span data-stu-id="1b752-148">The following topic describes how visualization code processes audio data:</span></span>

-   [<span data-ttu-id="1b752-149">Поток управления</span><span class="sxs-lookup"><span data-stu-id="1b752-149">Flow of Control</span></span>](flow-of-control.md)

## <a name="related-topics"></a><span data-ttu-id="1b752-150">См. также</span><span class="sxs-lookup"><span data-stu-id="1b752-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b752-151">**О пользовательских визуализациях**</span><span class="sxs-lookup"><span data-stu-id="1b752-151">**About Custom Visualizations**</span></span>](about-custom-visualizations.md)
</dt> </dl>

 

 




