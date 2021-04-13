---
title: Форматы
description: Форматы
ms.assetid: 7c602643-f1fc-4fbd-a739-4296dc758bc9
keywords:
- Windows Media Format SDK, входные данные
- Windows Media Format SDK, потоки
- Windows Media Format SDK, выходные данные
- Windows Media Format SDK, форматы
- Расширенный формат систем (ASF), входные данные
- ASF (Расширенный системный формат), входные данные
- Расширенный системный формат (ASF), потоки
- ASF (Расширенный системный формат), потоки
- Расширенный формат систем (ASF), выходные данные
- ASF (Расширенный системный формат), выходные данные
- Расширенный формат систем (ASF), форматы
- ASF (Расширенный системный формат), форматы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e7895c27af3eb99e96d7009b79ea8df0011208
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331488"
---
# <a name="formats"></a><span data-ttu-id="8d07b-115">Форматы</span><span class="sxs-lookup"><span data-stu-id="8d07b-115">Formats</span></span>

<span data-ttu-id="8d07b-116">Сведения в формате описывают все, что необходимо знать о конкретном типе носителя.</span><span class="sxs-lookup"><span data-stu-id="8d07b-116">The information in a format describes everything you need to know about a particular type of media.</span></span> <span data-ttu-id="8d07b-117">Каждый формат имеет основной тип, например аудио или видео, и может иметь подтип.</span><span class="sxs-lookup"><span data-stu-id="8d07b-117">Every format has a major type, like audio or video, and may have a subtype.</span></span> <span data-ttu-id="8d07b-118">Форматы содержат различные сведения, основанные на основном типе.</span><span class="sxs-lookup"><span data-stu-id="8d07b-118">Formats contain different information based on major type.</span></span> <span data-ttu-id="8d07b-119">Для форматов аудио и видео требуется гораздо больше информации, чем для других типов.</span><span class="sxs-lookup"><span data-stu-id="8d07b-119">Audio and video formats require much more information than other types.</span></span>

<span data-ttu-id="8d07b-120">Точно так же, как объекты пакета SDK формата Windows Media различаются между входными числами, номерами потоков и выходными номерами (см. раздел [входные данные, потоки и выходные](inputs-streams-and-outputs.md)данные), существуют важные различия между форматами ввода, потоковыми форматами и выходными форматами.</span><span class="sxs-lookup"><span data-stu-id="8d07b-120">Just as the objects of the Windows Media Format SDK differentiate between input numbers, stream numbers, and output numbers (see [Inputs, Streams and Outputs](inputs-streams-and-outputs.md)), there are important distinctions between input formats, stream formats, and output formats.</span></span> <span data-ttu-id="8d07b-121">Эти различия описаны здесь:</span><span class="sxs-lookup"><span data-stu-id="8d07b-121">These differences are described here:</span></span>

## <a name="input-formats"></a><span data-ttu-id="8d07b-122">Форматы входных данных</span><span class="sxs-lookup"><span data-stu-id="8d07b-122">Input Formats</span></span>

<span data-ttu-id="8d07b-123">Входной формат описывает цифровые носители, передаваемые в объект модуля записи.</span><span class="sxs-lookup"><span data-stu-id="8d07b-123">An input format describes the digital media that you pass to the writer object.</span></span> <span data-ttu-id="8d07b-124">Если поток в ASF-файле сжимается с помощью кодека, кодек будет поддерживать только определенные входные форматы.</span><span class="sxs-lookup"><span data-stu-id="8d07b-124">If a stream in an ASF file is compressed with a codec, the codec will support only certain input formats.</span></span> <span data-ttu-id="8d07b-125">При использовании кодеков аудио и видео Windows Media можно перечислить Поддерживаемые входные форматы с помощью объекта модуля записи.</span><span class="sxs-lookup"><span data-stu-id="8d07b-125">When using the Windows Media Audio and Video codecs, you can enumerate the supported input formats using the writer object.</span></span> <span data-ttu-id="8d07b-126">При записи файла вы несете ответственность за выбор формата входных данных, соответствующего входному носителю.</span><span class="sxs-lookup"><span data-stu-id="8d07b-126">When writing a file, you are responsible for selecting an input format that matches your input media.</span></span>

<span data-ttu-id="8d07b-127">Хотя входной формат носителя должен поддерживаться кодеком, который будет сжимать данные, некоторые параметры формата ввода не должны соответствовать формату потока.</span><span class="sxs-lookup"><span data-stu-id="8d07b-127">Although the input media format must be supported by the codec that will compress the data, some input format settings need not match the stream format.</span></span> <span data-ttu-id="8d07b-128">Например, формат ввода для видеопотока может иметь размер кадра, отличный от того, который определен в формате потока.</span><span class="sxs-lookup"><span data-stu-id="8d07b-128">For example, the input format for a video stream may have a frame size that is different from that defined in the stream format.</span></span> <span data-ttu-id="8d07b-129">В этих случаях кодек будет выполнять преобразования.</span><span class="sxs-lookup"><span data-stu-id="8d07b-129">The codec will perform conversions in these cases.</span></span>

## <a name="stream-formats"></a><span data-ttu-id="8d07b-130">Форматы потоков</span><span class="sxs-lookup"><span data-stu-id="8d07b-130">Stream Formats</span></span>

<span data-ttu-id="8d07b-131">Формат потока описывает форму носителя, который хранится в ASF-файле.</span><span class="sxs-lookup"><span data-stu-id="8d07b-131">A stream format describes the form of the media as it is stored in the ASF file.</span></span> <span data-ttu-id="8d07b-132">Формат потока является форматом, описанным в профиле, и может быть и не совпадать с форматом ввода и выходным форматом.</span><span class="sxs-lookup"><span data-stu-id="8d07b-132">The stream format is the format described in the profile, and may or may not be the same as the input format and output format.</span></span> <span data-ttu-id="8d07b-133">Если для сжатия данных в потоке используется кодек, формат потока будет отличаться от форматов ввода и вывода.</span><span class="sxs-lookup"><span data-stu-id="8d07b-133">If a codec is used to compress the data in a stream, the stream format will be different than the input and output formats.</span></span>

<span data-ttu-id="8d07b-134">При использовании кодеков аудио и видео Windows Media необходимо получить список поддерживаемых форматов потоков из кодека, чтобы не пытаться указать формат, который не поддерживается кодом.</span><span class="sxs-lookup"><span data-stu-id="8d07b-134">When using the Windows Media Audio and Video codecs, you must obtain a list of supported stream formats from the codec to ensure that you are not attempting to specify a format that the code does not support.</span></span> <span data-ttu-id="8d07b-135">Некоторые параметры форматирования, такие как размер и глубина цвета видеокадра, необходимо настроить вручную после получения формата кодека.</span><span class="sxs-lookup"><span data-stu-id="8d07b-135">Some format settings, such as the size and color depth of a video frame, must be configured manually after the codec format is retrieved.</span></span>

## <a name="output-formats"></a><span data-ttu-id="8d07b-136">Форматы выходных данных</span><span class="sxs-lookup"><span data-stu-id="8d07b-136">Output Formats</span></span>

<span data-ttu-id="8d07b-137">Формат вывода описывает цифровые носители, которые читатель (или синхронное средство чтения) доставляет в приложение.</span><span class="sxs-lookup"><span data-stu-id="8d07b-137">An output format describes the digital media that the reader (or synchronous reader) delivers to your application.</span></span> <span data-ttu-id="8d07b-138">Если поток в ASF-файле сжимается с помощью кодека, кодек будет поддерживать только определенные форматы вывода.</span><span class="sxs-lookup"><span data-stu-id="8d07b-138">If a stream in an ASF file is compressed with a codec, the codec will support only certain output formats.</span></span> <span data-ttu-id="8d07b-139">При использовании кодеков аудио и видео Windows Media можно перечислить Поддерживаемые форматы вывода с помощью объекта Reader.</span><span class="sxs-lookup"><span data-stu-id="8d07b-139">When using the Windows Media Audio and Video codecs, you can enumerate the supported output formats by using the reader object.</span></span> <span data-ttu-id="8d07b-140">Каждый из кодеков Windows Media имеет формат вывода по умолчанию, но для образца доставки можно выбрать любой поддерживаемый формат вывода.</span><span class="sxs-lookup"><span data-stu-id="8d07b-140">Each of the Windows Media codecs has a default output format, but you can select any supported output format for sample delivery.</span></span>

<span data-ttu-id="8d07b-141">Хотя формат выходных данных мультимедиа должен поддерживаться кодеком, который сжимает данные, некоторые параметры формата вывода не должны соответствовать формату потока.</span><span class="sxs-lookup"><span data-stu-id="8d07b-141">Although the output media format must be supported by the codec that compressed the data, some output format settings need not match the stream format.</span></span> <span data-ttu-id="8d07b-142">Например, формат вывода видеопотока может отличаться от размера кадра, определенного в формате потока.</span><span class="sxs-lookup"><span data-stu-id="8d07b-142">For example, the output format for a video stream may have a frame size that is different from that defined in the stream format.</span></span> <span data-ttu-id="8d07b-143">В этих случаях кодек будет выполнять преобразования.</span><span class="sxs-lookup"><span data-stu-id="8d07b-143">The codec will perform conversions in these cases.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d07b-144">См. также</span><span class="sxs-lookup"><span data-stu-id="8d07b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d07b-145">**Основные понятия**</span><span class="sxs-lookup"><span data-stu-id="8d07b-145">**Concepts**</span></span>](concepts.md)
</dt> </dl>

 

 




