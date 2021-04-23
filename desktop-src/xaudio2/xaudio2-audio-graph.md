---
description: Набор всех голосов, содержащих их результаты и их взаимосвязи, называется графиком обработки звука.
ms.assetid: 4fa45dbf-3811-c91c-7561-3b896e9e1f03
title: XAudio2 Audio Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb265bd6bc2547acd04ca41cceb58ad12896fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272820"
---
# <a name="xaudio2-audio-graph"></a><span data-ttu-id="475a2-103">XAudio2 Audio Graph</span><span class="sxs-lookup"><span data-stu-id="475a2-103">XAudio2 Audio Graph</span></span>

<span data-ttu-id="475a2-104">Набор всех голосов, содержащих их результаты и их взаимосвязи, называется графиком обработки звука.</span><span class="sxs-lookup"><span data-stu-id="475a2-104">The set of all voices, with their contained effects and their interconnections, is referred to as the audio processing graph.</span></span> <span data-ttu-id="475a2-105">Граф принимает набор звуковых потоков от клиента в качестве входных данных, обрабатывает их и передает окончательный результат на звуковое устройство.</span><span class="sxs-lookup"><span data-stu-id="475a2-105">The graph takes a set of audio streams from the client as input, processes them, and delivers the final result to an audio device.</span></span> <span data-ttu-id="475a2-106">Вся обработка звука выполняется в отдельном потоке с периодичностью, определенной тактом графика (в настоящее время 10 миллисекунд на Microsoft Windows, и 5 1/3 миллисекунд на Xbox 360).</span><span class="sxs-lookup"><span data-stu-id="475a2-106">All audio processing takes place in a separate thread with a periodicity defined by the graph's quantum (currently 10 milliseconds on Microsoft Windows, and 5 1/3 milliseconds on Xbox 360).</span></span> <span data-ttu-id="475a2-107">Каждый такт миллисекунда поток выходит из спящего режима и разбросает тактовые миллисекунды звуковых данных через весь граф.</span><span class="sxs-lookup"><span data-stu-id="475a2-107">Every quantum milliseconds, the thread wakes up and disperses quantum milliseconds of audio data through the entire graph.</span></span> <span data-ttu-id="475a2-108">Пример создания простой звуковой диаграммы см. в разделе как [создать базовый график обработки звука](how-to--build-a-basic-audio-processing-graph.md).</span><span class="sxs-lookup"><span data-stu-id="475a2-108">For an example of building a basic audio graph, see How to: [Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span>

<span data-ttu-id="475a2-109">Простая звуковая диаграмма:</span><span class="sxs-lookup"><span data-stu-id="475a2-109">A simple audio graph:</span></span>

![простая звуковая диаграмма](images/xaudio2-audio-graph.png)

<span data-ttu-id="475a2-111">Клиент может управлять состоянием диаграммы динамически во время его выполнения.</span><span class="sxs-lookup"><span data-stu-id="475a2-111">The client can control the graph's state dynamically while it is running.</span></span> <span data-ttu-id="475a2-112">Управляющие действия могут включать добавление и удаление входных и выходных данных, изменение внутренних эффектов и соединений, задание параметров для эффектов, включение и отключение частей графа и т. д.</span><span class="sxs-lookup"><span data-stu-id="475a2-112">Control actions might include adding and removing inputs and outputs, changing the internal effects and interconnections, setting parameters on the effects, enabling and disabling parts of the graph, and so on.</span></span> <span data-ttu-id="475a2-113">Пример динамического изменения звуковой диаграммы см. [в разделе как динамически добавлять или удалять голоса из звуковой диаграммы](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md).</span><span class="sxs-lookup"><span data-stu-id="475a2-113">For an example of dynamically changing an audio graph, see [How to: Dynamically Add or Remove Voices From an Audio Graph](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md).</span></span>

## <a name="processing-the-graph"></a><span data-ttu-id="475a2-114">Обработка графа</span><span class="sxs-lookup"><span data-stu-id="475a2-114">Processing the Graph</span></span>

<span data-ttu-id="475a2-115">Любой вызов метода, который влияет на любой объект в графе, считается влиянием изменения состояния графа.</span><span class="sxs-lookup"><span data-stu-id="475a2-115">Any method call that affects any object in the graph is considered to be effecting a graph state change.</span></span> <span data-ttu-id="475a2-116">Изменения состояния графа включают следующее:</span><span class="sxs-lookup"><span data-stu-id="475a2-116">Graph state changes include the following:</span></span>

-   <span data-ttu-id="475a2-117">Создание и уничтожение голосов</span><span class="sxs-lookup"><span data-stu-id="475a2-117">Creating and destroying voices</span></span>
-   <span data-ttu-id="475a2-118">Запуск или остановка голосов</span><span class="sxs-lookup"><span data-stu-id="475a2-118">Starting or stopping voices</span></span>
-   <span data-ttu-id="475a2-119">Изменение назначений голоса</span><span class="sxs-lookup"><span data-stu-id="475a2-119">Changing the destinations of a voice</span></span>
-   <span data-ttu-id="475a2-120">Изменение цепочек эффектов</span><span class="sxs-lookup"><span data-stu-id="475a2-120">Modifying effect chains</span></span>
-   <span data-ttu-id="475a2-121">Включение или отключение эффектов</span><span class="sxs-lookup"><span data-stu-id="475a2-121">Enabling or disabling effects</span></span>
-   <span data-ttu-id="475a2-122">Задание параметров для эффектов или встроенных Сркс, фильтров, томов и миксерс</span><span class="sxs-lookup"><span data-stu-id="475a2-122">Setting parameters on the effects or on the built-in SRCs, filters, volumes, and mixers</span></span>

<span data-ttu-id="475a2-123">Любой набор изменений состояния графа можно объединить и выполнить как атомарную транзакцию.</span><span class="sxs-lookup"><span data-stu-id="475a2-123">Any set of graph state changes can be combined and performed as an atomic transaction.</span></span> <span data-ttu-id="475a2-124">Эти атомарные операции называются наборами операций.</span><span class="sxs-lookup"><span data-stu-id="475a2-124">These atomic operations are known as operation sets.</span></span> <span data-ttu-id="475a2-125">Они обсуждаются в обзоре [наборов операций XAudio2](xaudio2-operation-sets.md) .</span><span class="sxs-lookup"><span data-stu-id="475a2-125">They are discussed in the [XAudio2 Operation Sets](xaudio2-operation-sets.md) overview.</span></span>

## <a name="internal-data-representation"></a><span data-ttu-id="475a2-126">Внутреннее представление данных</span><span class="sxs-lookup"><span data-stu-id="475a2-126">Internal Data Representation</span></span>

<span data-ttu-id="475a2-127">Звуковые данные в графе XAudio2 всегда сохраняются и обрабатываются в 32-битной форме PCM с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="475a2-127">Audio data within the XAudio2 graph is always stored and processed in 32-bit floating-point PCM form.</span></span> <span data-ttu-id="475a2-128">Однако количество каналов и частота выборки могут различаться в пределах диаграммы.</span><span class="sxs-lookup"><span data-stu-id="475a2-128">However, the channel count and sample rate can vary within the graph.</span></span> <span data-ttu-id="475a2-129">Формат, в котором заданный голосовый процесс определяется типом голоса и параметрами, используемыми для создания голоса.</span><span class="sxs-lookup"><span data-stu-id="475a2-129">The format in which a given voice processes audio is determined by the voice type and parameters used to create the voice.</span></span>



| <span data-ttu-id="475a2-130">Тип голоса</span><span class="sxs-lookup"><span data-stu-id="475a2-130">Voice Type</span></span>                                                                                                      | <span data-ttu-id="475a2-131">Параметры</span><span class="sxs-lookup"><span data-stu-id="475a2-131">Parameters</span></span>                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="475a2-132">**IXAudio2SourceVoice**</span><span class="sxs-lookup"><span data-stu-id="475a2-132">**IXAudio2SourceVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)                                                              | <span data-ttu-id="475a2-133">Число каналов и частота дискретизации голосов, на которые исходный голос отправляет звук.</span><span class="sxs-lookup"><span data-stu-id="475a2-133">The channel count and sample rate of the voices to which the source voice sends audio.</span></span>         |
| <span data-ttu-id="475a2-134">[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) и [ **IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)</span><span class="sxs-lookup"><span data-stu-id="475a2-134">[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) and [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)</span></span> | <span data-ttu-id="475a2-135">Аргументы *инпутчаннелс* и *инпутсамплерате* , используемые для создания субмикс/главной речи.</span><span class="sxs-lookup"><span data-stu-id="475a2-135">The *InputChannels* and *InputSampleRate* arguments used to create the submix/mastering voice.</span></span> |



 

## <a name="format-conversion"></a><span data-ttu-id="475a2-136">Преобразование формата</span><span class="sxs-lookup"><span data-stu-id="475a2-136">Format Conversion</span></span>

<span data-ttu-id="475a2-137">XAudio2 обрабатывает любые преобразования частоты выборки или канала, необходимые для передачи звука с одного голоса на другой, со следующими ограничениями.</span><span class="sxs-lookup"><span data-stu-id="475a2-137">XAudio2 handles any sample rate or channel conversions that are required as audio travels from one voice to another, with the following limitations:</span></span>

-   <span data-ttu-id="475a2-138">Все целевые голоса для определенного голоса должны выполняться с одинаковой частотой выборки</span><span class="sxs-lookup"><span data-stu-id="475a2-138">All destination voices for a particular voice must be running at the same sample rate</span></span>
-   <span data-ttu-id="475a2-139">Эффекты в цепочке эффектов могут изменить число каналов звука, но не частоту выборки</span><span class="sxs-lookup"><span data-stu-id="475a2-139">Effects in an effect chain can change the audio's channel count, but not its sample rate</span></span>
-   <span data-ttu-id="475a2-140">Число каналов вывода цепочки эффектов должно совпадать с количеством голосов, которые он отправляет.</span><span class="sxs-lookup"><span data-stu-id="475a2-140">An effect chain's output channel count must match that of the voices to which it sends</span></span>
-   <span data-ttu-id="475a2-141">Невозможно выполнить динамическое изменение графа, что приведет к нарушению правил выше</span><span class="sxs-lookup"><span data-stu-id="475a2-141">No dynamic graph change can be made which would break the rules above</span></span>

<span data-ttu-id="475a2-142">На стороне входа исходные голоса могут считывать данные в любом допустимом формате PCM или в любом из сжатых форматов, поддерживаемых XAudio2.</span><span class="sxs-lookup"><span data-stu-id="475a2-142">On the input side, source voices can read data in any valid PCM format, or in any of the compressed formats supported by XAudio2.</span></span> <span data-ttu-id="475a2-143">Если входные данные сжимаются, они декодированы в PCM с плавающей запятой до завершения дальнейшей обработки.</span><span class="sxs-lookup"><span data-stu-id="475a2-143">If the input data is compressed, it is decoded to floating-point PCM before any further processing is done.</span></span>

<span data-ttu-id="475a2-144">На стороне вывода выходные голоса могут формировать только данные PCM.</span><span class="sxs-lookup"><span data-stu-id="475a2-144">On the output side, mastering voices can only produce PCM data.</span></span> <span data-ttu-id="475a2-145">Эти данные всегда будут соответствовать тем же ограничениям, которые описаны выше для входных данных PCM.</span><span class="sxs-lookup"><span data-stu-id="475a2-145">This data will always satisfy the same restrictions described above for input PCM data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="475a2-146">См. также</span><span class="sxs-lookup"><span data-stu-id="475a2-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="475a2-147">Графики воспроизведения</span><span class="sxs-lookup"><span data-stu-id="475a2-147">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="475a2-148">Руководство по программированию для XAudio2</span><span class="sxs-lookup"><span data-stu-id="475a2-148">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="475a2-149">Руководство: создание базовой схемы обработки звука</span><span class="sxs-lookup"><span data-stu-id="475a2-149">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="475a2-150">Руководство: динамическое добавление речи или удаление ее из звуковой схемы</span><span class="sxs-lookup"><span data-stu-id="475a2-150">How to: Dynamically Add or Remove Voices From an Audio Graph</span></span>](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)
</dt> <dt>

[<span data-ttu-id="475a2-151">Руководство: использование субмикшированной речи</span><span class="sxs-lookup"><span data-stu-id="475a2-151">How to: Use Submix Voices</span></span>](how-to--use-submix-voices.md)
</dt> <dt>

[<span data-ttu-id="475a2-152">Руководство: создание цепи эффектов</span><span class="sxs-lookup"><span data-stu-id="475a2-152">How to: Create an Effect Chain</span></span>](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 



