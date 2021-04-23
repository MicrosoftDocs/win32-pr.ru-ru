---
description: 'Существует три типа голосовых объектов XAudio2: источник, субмикс и голосовое руководство.'
ms.assetid: 3a4acc03-e47a-ff33-dee8-a374051f85f6
title: Речь в XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b11300cea770f59485e8a78b0d30110b5469befe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703029"
---
# <a name="xaudio2-voices"></a><span data-ttu-id="f0599-103">Речь в XAudio2</span><span class="sxs-lookup"><span data-stu-id="f0599-103">XAudio2 Voices</span></span>

<span data-ttu-id="f0599-104">Существует три типа голосовых объектов XAudio2: *источник*, *субмикс* и голосовое  руководство.</span><span class="sxs-lookup"><span data-stu-id="f0599-104">There are three types of XAudio2 voice objects: *source*, *submix*, and *mastering* voices.</span></span> <span data-ttu-id="f0599-105">Исходные голосовые объекты берутся из звуковых данных, предоставленных клиентом.</span><span class="sxs-lookup"><span data-stu-id="f0599-105">Source voices operate on audio data provided by the client.</span></span> <span data-ttu-id="f0599-106">Данные исходных и комбинированных голосов используются для получения одного или более комбинированных или обработанных голосов.</span><span class="sxs-lookup"><span data-stu-id="f0599-106">Source and submix voices send their output to one or more submix or mastering voices.</span></span> <span data-ttu-id="f0599-107">Комбинированные и обработанные голоса смешивают звуковые сигналы из всех голосов, чьи данные они получают, и работают с итоговым звуком.</span><span class="sxs-lookup"><span data-stu-id="f0599-107">Submix and mastering voices mix the audio from all voices feeding them, and operate on the result.</span></span> <span data-ttu-id="f0599-108">Обработанные голоса записываются в виде звуковых данных на аудиоустройство.</span><span class="sxs-lookup"><span data-stu-id="f0599-108">Mastering voices write audio data to an audio device.</span></span>

## <a name="actions-performed-by-all-voices"></a><span data-ttu-id="f0599-109">Действия, выполняемые всеми голосовыми операциями</span><span class="sxs-lookup"><span data-stu-id="f0599-109">Actions Performed by All Voices</span></span>

<span data-ttu-id="f0599-110">Все голоса выполняют следующие действия, посмотрев на звук, который перемещает их.</span><span class="sxs-lookup"><span data-stu-id="f0599-110">All voices perform the following actions in order on the audio that travels though them.</span></span>

1.  <span data-ttu-id="f0599-111">Общая коррекция громкости, влияющая на все каналы звука.</span><span class="sxs-lookup"><span data-stu-id="f0599-111">Overall volume adjustment, affecting all audio channels.</span></span> <span data-ttu-id="f0599-112">См. раздел [**IXAudio2Voice:: сетволуме**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).</span><span class="sxs-lookup"><span data-stu-id="f0599-112">See [**IXAudio2Voice::SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).</span></span>
2.  <span data-ttu-id="f0599-113">Необязательная клиентская цепочка из одного или нескольких эффектов DSP, например встроенная перекоманда или пользовательский эффект, определенный интерфейсом [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo) .</span><span class="sxs-lookup"><span data-stu-id="f0599-113">An optional client-specified chain of one or more DSP effects, such as the built-in reverb or a user effect defined by the [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) interface.</span></span> <span data-ttu-id="f0599-114">См. [XAudio2 Audio Effects](xaudio2-audio-effects.md).</span><span class="sxs-lookup"><span data-stu-id="f0599-114">See [XAudio2 Audio Effects](xaudio2-audio-effects.md).</span></span>
3.  <span data-ttu-id="f0599-115">Корректировка исходящего объема на канале.</span><span class="sxs-lookup"><span data-stu-id="f0599-115">Per-channel output volume adjustment.</span></span> <span data-ttu-id="f0599-116">См. раздел [**IXAudio2Voice:: сетчаннелволумес**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).</span><span class="sxs-lookup"><span data-stu-id="f0599-116">See [**IXAudio2Voice::SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).</span></span>
4.  <span data-ttu-id="f0599-117">Разделяйте сочетание матрицы с каждым из целевых голосов или на устройство вывода звука для голосов.</span><span class="sxs-lookup"><span data-stu-id="f0599-117">Separate matrix mix to each of the destination voices or to the audio output device for mastering voices.</span></span> <span data-ttu-id="f0599-118">При необходимости этот набор изменяет количество каналов в аудио.</span><span class="sxs-lookup"><span data-stu-id="f0599-118">This mix changes the number of channels in the audio, if necessary.</span></span>

## <a name="source-voices"></a><span data-ttu-id="f0599-119">Исходные голоса</span><span class="sxs-lookup"><span data-stu-id="f0599-119">Source Voices</span></span>

<span data-ttu-id="f0599-120">Используйте исходные голоса для отправки звуковых данных в конвейер обработки XAudio2.</span><span class="sxs-lookup"><span data-stu-id="f0599-120">Use source voices to submit audio data into the XAudio2 processing pipeline.</span></span> <span data-ttu-id="f0599-121">Они являются точками входа в [XAudio2 Audio Graph](xaudio2-audio-graph.md).</span><span class="sxs-lookup"><span data-stu-id="f0599-121">They are the entry points into the [XAudio2 Audio Graph](xaudio2-audio-graph.md).</span></span> <span data-ttu-id="f0599-122">Необходимо отправить голосовые данные на основной голос, чтобы они были слышны либо напрямую, либо через промежуточные голоса субмикс.</span><span class="sxs-lookup"><span data-stu-id="f0599-122">You must send voice data to a mastering voice to be heard, either directly or through intermediate submix voices.</span></span>

<span data-ttu-id="f0599-123">В дополнение к действиям, выполняемым всеми голосовами, исходные голоса выполняют следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f0599-123">In addition to the actions performed by all voices, source voices perform the following actions.</span></span>

-   <span data-ttu-id="f0599-124">При необходимости декодер сначала выполняется для преобразования закодированных исходных данных в импульсный код (PCM).</span><span class="sxs-lookup"><span data-stu-id="f0599-124">If necessary, a decoder runs first to convert encoded source data to Pulse Code Modulation (PCM).</span></span>
-   <span data-ttu-id="f0599-125">При преобразовании частоты выборки с частотой дискретизации (SRC) исходные звуковые данные голоса преобразуются в частоту выборки, ожидаемую при необходимости, а также динамические изменения высоты.</span><span class="sxs-lookup"><span data-stu-id="f0599-125">A variable-rate sample rate conversion (SRC) converts the voice's source audio data to the sample rate expected by its destination voices, if necessary, and also supports dynamic pitch changes.</span></span>
-   <span data-ttu-id="f0599-126">Необязательный фильтр переменных состояния можно использовать для цвета звука различными способами.</span><span class="sxs-lookup"><span data-stu-id="f0599-126">An optional state-variable filter can be used to color the sound in various ways.</span></span> <span data-ttu-id="f0599-127">См. раздел [**IXAudio2Voice:: сетфилтерпараметерс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="f0599-127">See [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span></span>
-   <span data-ttu-id="f0599-128">К выходным данным голоса можно применить необязательный фильтр.</span><span class="sxs-lookup"><span data-stu-id="f0599-128">An optional filter can be applied to the voice's outputs.</span></span> <span data-ttu-id="f0599-129">См. раздел [**IXAudio2Voice:: сетаутпутфилтерпараметерс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="f0599-129">See [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span></span>

## <a name="submix-voices"></a><span data-ttu-id="f0599-130">Субмикс голоса</span><span class="sxs-lookup"><span data-stu-id="f0599-130">Submix Voices</span></span>

<span data-ttu-id="f0599-131">Субмикс Voice используется в основном для повышения производительности и обработки эффектов.</span><span class="sxs-lookup"><span data-stu-id="f0599-131">A submix voice is used primarily for performance improvements and effects processing.</span></span> <span data-ttu-id="f0599-132">Вы не можете отправлять буферы данных непосредственно в субмиксные голоса.</span><span class="sxs-lookup"><span data-stu-id="f0599-132">You cannot submit data buffers directly to submix voices.</span></span> <span data-ttu-id="f0599-133">Он не будет звуковым, если вы не отправите его на основной Voice.</span><span class="sxs-lookup"><span data-stu-id="f0599-133">It will not be audible unless you submit it to a mastering voice.</span></span> <span data-ttu-id="f0599-134">Вы можете использовать субмикс голоса, чтобы обеспечить преобразование определенного набора голосов данных в тот же формат и для того, чтобы конкретная цепочка эффектов обрабатывалась в совокупном результате.</span><span class="sxs-lookup"><span data-stu-id="f0599-134">You can use a submix voice to ensure that a particular set of voice data is converted to the same format and to have a particular effect chain processed on the collective result.</span></span>

<span data-ttu-id="f0599-135">Помимо действий, выполняемых всеми голосовыми действиями, субмиксные голоса выполняют следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f0599-135">In addition to the actions performed by all voices, submix voices perform the following actions.</span></span>

-   <span data-ttu-id="f0599-136">При необходимости SRC с фиксированной ставкой выполняется в выходных данных голоса, чтобы преобразовать звук в частоту выборки, ожидаемую для его целевых голосов.</span><span class="sxs-lookup"><span data-stu-id="f0599-136">A fixed-rate SRC runs on the voice's output, if necessary, to convert the audio to the sample rate expected by its destination voices.</span></span>
-   <span data-ttu-id="f0599-137">Необязательный фильтр переменных состояния можно использовать для цвета звука различными способами.</span><span class="sxs-lookup"><span data-stu-id="f0599-137">An optional state-variable filter can be used to color the sound in various ways.</span></span> <span data-ttu-id="f0599-138">См. раздел [**IXAudio2Voice:: сетфилтерпараметерс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="f0599-138">See [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span></span>
-   <span data-ttu-id="f0599-139">К выходным данным голоса можно применить необязательный фильтр.</span><span class="sxs-lookup"><span data-stu-id="f0599-139">An optional filter can be applied to the voice's outputs.</span></span> <span data-ttu-id="f0599-140">См. раздел [**IXAudio2Voice:: сетаутпутфилтерпараметерс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="f0599-140">See [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span></span>

## <a name="mastering-voices"></a><span data-ttu-id="f0599-141">Голосовое подглавное</span><span class="sxs-lookup"><span data-stu-id="f0599-141">Mastering Voices</span></span>

<span data-ttu-id="f0599-142">Используйте основной голос для представления устройства вывода звука.</span><span class="sxs-lookup"><span data-stu-id="f0599-142">Use a mastering voice to represent the audio output device.</span></span> <span data-ttu-id="f0599-143">Вы не можете отправлять буферы данных непосредственно в голосовые голоса, но данные, отправляемые другим типам голосов, должны передаваться на основной голос.</span><span class="sxs-lookup"><span data-stu-id="f0599-143">You cannot submit data buffers directly to mastering voices, but data submitted to other types of voices must go to a mastering voice to be heard.</span></span>

<span data-ttu-id="f0599-144">В дополнение к действиям, выполняемым всеми голосовыми голосовами, они выполняют следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f0599-144">In addition to the actions performed by all voices, mastering voices perform the following actions.</span></span>

-   <span data-ttu-id="f0599-145">Если вы создаете основной голос с явно указанным значением *инпутсамплерате* , которое не поддерживается звуковым устройством, для преобразования в ближайшую частоту выборки, поддерживаемую устройством, используется значение src с фиксированной ставкой.</span><span class="sxs-lookup"><span data-stu-id="f0599-145">If you create the mastering voice with an explicit *InputSampleRate* value that is not supported by the audio device, a fixed-rate SRC is used to convert to the closest sample rate supported by the device.</span></span>
-   <span data-ttu-id="f0599-146">Обрезает окончательный выходной звук, если это требуется для выходного устройства.</span><span class="sxs-lookup"><span data-stu-id="f0599-146">Clip the final output audio, if it is required by the output device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0599-147">См. также</span><span class="sxs-lookup"><span data-stu-id="f0599-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0599-148">Голоса</span><span class="sxs-lookup"><span data-stu-id="f0599-148">Voices</span></span>](voices.md)
</dt> <dt>

[<span data-ttu-id="f0599-149">Руководство по программированию для XAudio2</span><span class="sxs-lookup"><span data-stu-id="f0599-149">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="f0599-150">**IXAudio2SourceVoice**</span><span class="sxs-lookup"><span data-stu-id="f0599-150">**IXAudio2SourceVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)
</dt> <dt>

[<span data-ttu-id="f0599-151">**IXAudio2SubmixVoice**</span><span class="sxs-lookup"><span data-stu-id="f0599-151">**IXAudio2SubmixVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)
</dt> <dt>

[<span data-ttu-id="f0599-152">**IXAudio2MasteringVoice**</span><span class="sxs-lookup"><span data-stu-id="f0599-152">**IXAudio2MasteringVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)
</dt> </dl>

 

 
