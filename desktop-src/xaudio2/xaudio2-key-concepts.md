---
description: В этом обзоре представлены основные понятия использования XAudio2.
ms.assetid: 103e939f-7815-51c5-159a-c607da1e99ba
title: Основные понятия XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2c0e173e2205070c9f94e8c25dcd9ce7e548c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719692"
---
# <a name="xaudio2-key-concepts"></a><span data-ttu-id="bc039-103">Основные понятия XAudio2</span><span class="sxs-lookup"><span data-stu-id="bc039-103">XAudio2 Key Concepts</span></span>

<span data-ttu-id="bc039-104">В этом обзоре представлены основные понятия использования XAudio2.</span><span class="sxs-lookup"><span data-stu-id="bc039-104">This overview introduces some key concepts for using XAudio2.</span></span>

-   [<span data-ttu-id="bc039-105">Подсистема XAudio2</span><span class="sxs-lookup"><span data-stu-id="bc039-105">XAudio2 Engine</span></span>](#xaudio2-engine)
-   [<span data-ttu-id="bc039-106">Голоса</span><span class="sxs-lookup"><span data-stu-id="bc039-106">Voices</span></span>](#voices)
-   [<span data-ttu-id="bc039-107">Звуковая диаграмма</span><span class="sxs-lookup"><span data-stu-id="bc039-107">Audio Graph</span></span>](#audio-graph)
-   [<span data-ttu-id="bc039-108">Обратные вызовы</span><span class="sxs-lookup"><span data-stu-id="bc039-108">Callbacks</span></span>](#callbacks)
-   [<span data-ttu-id="bc039-109">См. также</span><span class="sxs-lookup"><span data-stu-id="bc039-109">Related Topics</span></span>](#related-topics)

## <a name="xaudio2-engine"></a><span data-ttu-id="bc039-110">Подсистема XAudio2</span><span class="sxs-lookup"><span data-stu-id="bc039-110">XAudio2 Engine</span></span>

<span data-ttu-id="bc039-111">Интерфейс [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) является ядром обработчика XAudio2.</span><span class="sxs-lookup"><span data-stu-id="bc039-111">The [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) interface is the core of the XAudio2 engine.</span></span> <span data-ttu-id="bc039-112">Создание экземпляра интерфейса **IXAudio2** позволяет клиенту перечислять доступные звуковые устройства, настраивать глобальные свойства API, создавать голоса и отслеживать производительность.</span><span class="sxs-lookup"><span data-stu-id="bc039-112">Creating an instance of the **IXAudio2** interface allows the client to enumerate the available audio devices, to configure global API properties, to create voices, and to monitor performance.</span></span> <span data-ttu-id="bc039-113">Вспомогательная функция [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) выполняет задачи создания экземпляров и инициализации для XAudio2.</span><span class="sxs-lookup"><span data-stu-id="bc039-113">The [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) helper function performs instantiation and initialization tasks for XAudio2.</span></span>

<span data-ttu-id="bc039-114">Экземпляры XAudio2 можно создавать несколько раз в рамках одного процесса.</span><span class="sxs-lookup"><span data-stu-id="bc039-114">You can create instances of XAudio2 multiple times within a single process.</span></span> <span data-ttu-id="bc039-115">Каждый объект XAudio2 работает независимо и имеет свой собственный поток обработки звука.</span><span class="sxs-lookup"><span data-stu-id="bc039-115">Each XAudio2 object operates independently, and has its own audio processing thread.</span></span> <span data-ttu-id="bc039-116">Совместно используются только параметры отладки.</span><span class="sxs-lookup"><span data-stu-id="bc039-116">Only the debug settings are shared.</span></span> <span data-ttu-id="bc039-117">Это важно в Windows, где несколько различных компонентов могут загружаться в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="bc039-117">This is important on Windows where several different components may be loaded in a single process.</span></span> <span data-ttu-id="bc039-118">Например, Internet Explorer может одновременно использовать несколько компонентов XAudio2.</span><span class="sxs-lookup"><span data-stu-id="bc039-118">For example, Internet Explorer might use multiple XAudio2 components simultaneously.</span></span> <span data-ttu-id="bc039-119">Хотя можно создать несколько объектов XAudio2 Engine в одном клиентском приложении, не следует передавать данные между соответствующими графами.</span><span class="sxs-lookup"><span data-stu-id="bc039-119">Although it is possible to create multiple XAudio2 engine objects within a single client application, you should not pass information between their respective graphs.</span></span>

<span data-ttu-id="bc039-120">Пример инициализации подсистемы XAudio2 см. [в разделе как инициализировать XAudio2](how-to--initialize-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="bc039-120">For an example of initializing the XAudio2 engine, see [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>

## <a name="voices"></a><span data-ttu-id="bc039-121">Голоса</span><span class="sxs-lookup"><span data-stu-id="bc039-121">Voices</span></span>

<span data-ttu-id="bc039-122">Голоса — это объекты, которые XAudio2 использовать для обработки, управления и воспроизведения звуковых данных.</span><span class="sxs-lookup"><span data-stu-id="bc039-122">Voices are the objects XAudio2 use to process, to manipulate, and to play audio data.</span></span> <span data-ttu-id="bc039-123">Существует три типа голосов в XAudio2.</span><span class="sxs-lookup"><span data-stu-id="bc039-123">There are three types of voices in XAudio2.</span></span>

-   [<span data-ttu-id="bc039-124">**Исходные голоса**</span><span class="sxs-lookup"><span data-stu-id="bc039-124">**Source Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)

    <span data-ttu-id="bc039-125">Исходные голоса представляют поток звуковых данных.</span><span class="sxs-lookup"><span data-stu-id="bc039-125">Source voices represent a stream of audio data.</span></span> <span data-ttu-id="bc039-126">Исходные голоса отправляют свои данные другим типам голосов.</span><span class="sxs-lookup"><span data-stu-id="bc039-126">Source voices send their data to other types of voices.</span></span>

-   [<span data-ttu-id="bc039-127">**Субмикс голоса**</span><span class="sxs-lookup"><span data-stu-id="bc039-127">**Submix Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)

    <span data-ttu-id="bc039-128">Субмиксные голоса выполняют некоторую обработку звуковых данных, которые они получают.</span><span class="sxs-lookup"><span data-stu-id="bc039-128">Submix voices perform some manipulation of audio data they receive.</span></span> <span data-ttu-id="bc039-129">Одним из примеров обработки звуковых данных может быть преобразование частота дискретизации.</span><span class="sxs-lookup"><span data-stu-id="bc039-129">One example of audio data manipulation might be sample rate conversion.</span></span> <span data-ttu-id="bc039-130">После того, как субмикс голоса обрабатывает данные, они передаются в другой субмикс голоса или в главный Voice.</span><span class="sxs-lookup"><span data-stu-id="bc039-130">After a submix voice processes data, it passes that data to another submix voice or to a master voice.</span></span>

-   [<span data-ttu-id="bc039-131">**Голосовое подглавное**</span><span class="sxs-lookup"><span data-stu-id="bc039-131">**Mastering Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)

    <span data-ttu-id="bc039-132">При сводном голосовом процессе получаются данные из исходных голосов и субмикс голосов, а эти данные отправляются на звуковое оборудование.</span><span class="sxs-lookup"><span data-stu-id="bc039-132">Mastering voices receive data from source voices and submix voices, and sends that data to the audio hardware.</span></span>

<span data-ttu-id="bc039-133">Общие сведения о голосовах XAudio2 см. в разделе [XAudio2 голоса](voices.md) .</span><span class="sxs-lookup"><span data-stu-id="bc039-133">See [XAudio2 Voices](voices.md) for an overview of XAudio2 voices.</span></span>

## <a name="audio-graph"></a><span data-ttu-id="bc039-134">Звуковая диаграмма</span><span class="sxs-lookup"><span data-stu-id="bc039-134">Audio Graph</span></span>

<span data-ttu-id="bc039-135">Звуковая диаграмма — это коллекция голосов XAudio2.</span><span class="sxs-lookup"><span data-stu-id="bc039-135">An audio graph is a collection of XAudio2 voices.</span></span> <span data-ttu-id="bc039-136">Звук начинается с одной стороны аудио графа в исходных голосов, при необходимости проходит через один или несколько голосов субмикс и завершается в основной голосовой системе.</span><span class="sxs-lookup"><span data-stu-id="bc039-136">Audio starts at one side of an audio graph in source voices, optionally passes through one or more submix voices, and ends at a mastering voice.</span></span> <span data-ttu-id="bc039-137">В звуковой диаграмме будет содержаться исходный голос для каждого воспроизводимого звука, ноль или более субмикс голосов и один основной голос.</span><span class="sxs-lookup"><span data-stu-id="bc039-137">An audio graph will contain a source voice for each sound currently playing, zero or more submix voices, and one mastering voice.</span></span> <span data-ttu-id="bc039-138">Простейший звуковой график, а также минимум, необходимый для внесения шума в XAudio2, — это единый исходный голос, который наводится непосредственно на основной голос.</span><span class="sxs-lookup"><span data-stu-id="bc039-138">The simplest audio graph, and the minimum needed to make a noise in XAudio2, is a single source voice outputting directly to a mastering voice.</span></span> <span data-ttu-id="bc039-139">См. статью [как воспроизвести звук с помощью XAudio2](how-to--play-a-sound-with-xaudio2.md) , чтобы получить пример минимальных действий, необходимых для воспроизведения звука с помощью XAudio2.</span><span class="sxs-lookup"><span data-stu-id="bc039-139">See [How to: Play a Sound with XAudio2](how-to--play-a-sound-with-xaudio2.md) for an example of the minimum steps need to play a sound with XAudio2.</span></span>

<span data-ttu-id="bc039-140">Общие сведения о графах XAudio2 Audio см. в статье [XAudio2 Audio Graph](audio-graphs.md) .</span><span class="sxs-lookup"><span data-stu-id="bc039-140">See [XAudio2 Audio Graph](audio-graphs.md) for an overview of XAudio2 audio graphs.</span></span>

## <a name="callbacks"></a><span data-ttu-id="bc039-141">Обратные вызовы</span><span class="sxs-lookup"><span data-stu-id="bc039-141">Callbacks</span></span>

<span data-ttu-id="bc039-142">Обратные вызовы — это механизм, который XAudio2 использует для сигнализации клиентского кода о том, что событие произошло в голоса или в объекте Engine.</span><span class="sxs-lookup"><span data-stu-id="bc039-142">Callbacks are the mechanism XAudio2 uses to signal client code that some event has occurred in a voice or in the engine object.</span></span> <span data-ttu-id="bc039-143">Поскольку воспроизведение звука является асинхронным в ядре XAudio2, обратные вызовы предоставляют единственный способ определить, когда воспроизведение звука закончено.</span><span class="sxs-lookup"><span data-stu-id="bc039-143">Because audio playback is asynchronous in the XAudio2 engine, callbacks provide the only way to determine when a sound is finished playing.</span></span>

<span data-ttu-id="bc039-144">Общие сведения о обратных вызовах XAudio2 см. в разделе [обратные вызовы XAudio2](callbacks.md) .</span><span class="sxs-lookup"><span data-stu-id="bc039-144">See [XAudio2 Callbacks](callbacks.md) for an overview of XAudio2 callbacks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc039-145">См. также</span><span class="sxs-lookup"><span data-stu-id="bc039-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc039-146">Начало работы</span><span class="sxs-lookup"><span data-stu-id="bc039-146">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="bc039-147">Версии XAudio2</span><span class="sxs-lookup"><span data-stu-id="bc039-147">XAudio2 Versions</span></span>](xaudio2-versions.md)
</dt> <dt>

[<span data-ttu-id="bc039-148">Руководство: инициализация XAudio2</span><span class="sxs-lookup"><span data-stu-id="bc039-148">How to: Initialize XAudio2</span></span>](how-to--initialize-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="bc039-149">Как воспроизвести звук с помощью XAudio2</span><span class="sxs-lookup"><span data-stu-id="bc039-149">How to: Play a sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 



