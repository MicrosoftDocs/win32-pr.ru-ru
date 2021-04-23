---
description: Ошибки могут возникать в XAudio2. в этом разделе описывается, как они сообщаются, и некоторые подходы к их устранению.
ms.assetid: 360d1c5a-82e7-c982-82ea-5b5c7d69bc25
title: Отладка временных сбоев звука в XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 749c2ff69888f3411d86e13f95b84509587f22a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911112"
---
# <a name="debugging-audio-glitches-in-xaudio2"></a><span data-ttu-id="fd61f-103">Отладка временных сбоев звука в XAudio2</span><span class="sxs-lookup"><span data-stu-id="fd61f-103">Debugging Audio Glitches in XAudio2</span></span>

<span data-ttu-id="fd61f-104">Ошибки могут возникать в XAudio2. в этом разделе описывается, как они сообщаются, и некоторые подходы к их устранению.</span><span class="sxs-lookup"><span data-stu-id="fd61f-104">Glitches can occur in XAudio2, this topic covers how they are reported and some approaches to fixing them.</span></span>

<span data-ttu-id="fd61f-105">В этом обзоре рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="fd61f-105">This overview covers the following topics:</span></span>

-   [<span data-ttu-id="fd61f-106">Причины проблем с звуковым выходом или сбоев</span><span class="sxs-lookup"><span data-stu-id="fd61f-106">Causes of audio output problems or glitches</span></span>](#causes-of-audio-output-problems-or-glitches)
-   [<span data-ttu-id="fd61f-107">Как XAudio2 сообщает о проблемах</span><span class="sxs-lookup"><span data-stu-id="fd61f-107">How XAudio2 reports problems</span></span>](#how-xaudio2-reports-problems)
-   [<span data-ttu-id="fd61f-108">Подходы к устранению проблем</span><span class="sxs-lookup"><span data-stu-id="fd61f-108">Approaches to fixing problems</span></span>](#approaches-to-fixing-problems)
-   [<span data-ttu-id="fd61f-109">См. также</span><span class="sxs-lookup"><span data-stu-id="fd61f-109">Related topics</span></span>](#related-topics)

## <a name="causes-of-audio-output-problems-or-glitches"></a><span data-ttu-id="fd61f-110">Причины проблем с звуковым выходом или сбоев</span><span class="sxs-lookup"><span data-stu-id="fd61f-110">Causes of audio output problems or glitches</span></span>

<span data-ttu-id="fd61f-111">Сбои могут возникать в выходных данных XAudio2 по нескольким причинам.</span><span class="sxs-lookup"><span data-stu-id="fd61f-111">Glitches can occur in XAudio2 output for several reasons.</span></span>

-   <span data-ttu-id="fd61f-112">XAudio2 исходный голоса недоступен.</span><span class="sxs-lookup"><span data-stu-id="fd61f-112">An XAudio2 source voice is starved.</span></span> <span data-ttu-id="fd61f-113">Клиент не отправляет на него новые звуковые файлы достаточно быстро.</span><span class="sxs-lookup"><span data-stu-id="fd61f-113">The client is not submitting fresh audio to it fast enough.</span></span> <span data-ttu-id="fd61f-114">Вы получаете бездействия, так как у него нет данных для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="fd61f-114">You get silence because it has no data to play.</span></span>
-   <span data-ttu-id="fd61f-115">XAudio2 в целом является перегруженным.</span><span class="sxs-lookup"><span data-stu-id="fd61f-115">XAudio2 as a whole is overburdened.</span></span> <span data-ttu-id="fd61f-116">Получение *x* МС для звука занимает больше *x* МС.</span><span class="sxs-lookup"><span data-stu-id="fd61f-116">It takes longer than *X* ms to produce *X* ms of audio.</span></span> <span data-ttu-id="fd61f-117">Вы получаете выпадение из-за того, что XAudio2 не может создавать данные так быстро, как это необходимо для звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="fd61f-117">You get dropouts because XAudio2 can't produce data as fast as the audio device needs it.</span></span> <span data-ttu-id="fd61f-118">Возможно, в каждый момент времени выполняется слишком много голосов или эффектов, слишком много работы в ответных вызовах XAudio2 или слишком частое выполнение вызовов API XAudio2.</span><span class="sxs-lookup"><span data-stu-id="fd61f-118">You might be running too many voices or effects at a time, doing too much work in XAudio2 callbacks, or making XAudio2 API calls too frequently.</span></span>
-   <span data-ttu-id="fd61f-119">Поток обработки звука останавливается, так как реализация некоторых обратных вызовов XAudio2 клиентом выполняет действия, которые могут блокировать поток.</span><span class="sxs-lookup"><span data-stu-id="fd61f-119">The audio processing thread is stalling because the client's implementation of some XAudio2 callback is doing things that can block the thread.</span></span> <span data-ttu-id="fd61f-120">Например, он может обращаться к диску, синхронизироваться с другими потоками или вызывать другие функции, которые могут блокироваться.</span><span class="sxs-lookup"><span data-stu-id="fd61f-120">For example, it might be accessing the disk, synchronizing with other threads, or calling other functions that may block.</span></span> <span data-ttu-id="fd61f-121">Используйте фоновый поток с более низким приоритетом, который ответный вызов может передать для выполнения таких задач.</span><span class="sxs-lookup"><span data-stu-id="fd61f-121">Use a lower-priority background thread that the callback can signal to perform such tasks.</span></span>
-   <span data-ttu-id="fd61f-122">Система в целом перегружена.</span><span class="sxs-lookup"><span data-stu-id="fd61f-122">The system as a whole is overloaded.</span></span> <span data-ttu-id="fd61f-123">Другие потоки, работающие с тем же или более высоким приоритетом, чем XAudio2, выполняют слишком много усилий.</span><span class="sxs-lookup"><span data-stu-id="fd61f-123">Other threads running at the same or higher priority than XAudio2 are doing too much work.</span></span> <span data-ttu-id="fd61f-124">Они конкурируют с звуковым потоком на время ЦП.</span><span class="sxs-lookup"><span data-stu-id="fd61f-124">They are competing with the audio thread for CPU time.</span></span>

## <a name="how-xaudio2-reports-problems"></a><span data-ttu-id="fd61f-125">Как XAudio2 сообщает о проблемах</span><span class="sxs-lookup"><span data-stu-id="fd61f-125">How XAudio2 reports problems</span></span>

<span data-ttu-id="fd61f-126">XAudio2 может сообщать о сбоях в отладочной сборке несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="fd61f-126">XAudio2 can communicate glitches in the debug build in several ways.</span></span>

-   <span data-ttu-id="fd61f-127">В случае нехватки голоса XAudio2 отображает сообщение в этой форме.</span><span class="sxs-lookup"><span data-stu-id="fd61f-127">If a voice is being starved, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Voice at 0xNNNNNNNN starved: no more source buffers are available, but no end-of-stream marker was received
    ```

-   <span data-ttu-id="fd61f-128">Если поток звука выполняется слишком долго, XAudio2 отображает сообщение в этой форме.</span><span class="sxs-lookup"><span data-stu-id="fd61f-128">If the audio thread runs for too long, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Spent Xms in audio thread; XAudio2 possibly overloaded
    ```

    <span data-ttu-id="fd61f-129">Как правило, это сообщение появляется со следующим сообщением.</span><span class="sxs-lookup"><span data-stu-id="fd61f-129">Typically, this message occurs with the next message.</span></span>

-   <span data-ttu-id="fd61f-130">Если звуковой драйвер не может поставлять новые звуковые данные вовремя, XAudio2 отображает сообщение в этой форме.</span><span class="sxs-lookup"><span data-stu-id="fd61f-130">If the audio driver can't be fed new audio data on time, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Glitch at output sample X
    ```

-   <span data-ttu-id="fd61f-131">Вызов [**IXAudio2:: жетперформанцедата**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) предоставляет данные о производительности XAudio2, включая общее число сбоев с момента запуска обработчика XAudio2.</span><span class="sxs-lookup"><span data-stu-id="fd61f-131">Calling [**IXAudio2::GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) provides XAudio2 performance data, including the total number of glitches since the XAudio2 engine started.</span></span>

## <a name="approaches-to-fixing-problems"></a><span data-ttu-id="fd61f-132">Подходы к устранению проблем</span><span class="sxs-lookup"><span data-stu-id="fd61f-132">Approaches to fixing problems</span></span>

<span data-ttu-id="fd61f-133">Ниже перечислены возможные способы снижения числа сбоев звука.</span><span class="sxs-lookup"><span data-stu-id="fd61f-133">Possible ways to reduce audio glitches include the following.</span></span>

-   <span data-ttu-id="fd61f-134">В случае недоступности голоса: Увеличьте объем звуковых данных, помещенных в очередь на голоса.</span><span class="sxs-lookup"><span data-stu-id="fd61f-134">In the voice starvation case: Increase the amount of audio data that is queued ahead on a voice.</span></span> <span data-ttu-id="fd61f-135">[**IXAudio2SourceVoice::**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) at можно использовать для обнаружения количества буферов в очереди в данный момент.</span><span class="sxs-lookup"><span data-stu-id="fd61f-135">You can use [**IXAudio2SourceVoice::GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) to discover the number of buffers queued at any moment.</span></span> <span data-ttu-id="fd61f-136">Если вы по-прежнему видите ошибки невозможности передачи голоса, но не можете слышать о сбоях, убедитесь, что вы настраиваете [**\_ буфер XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Флаги** для \_ XAUDIO2 \_ конца \_ потока в конечном буфере звука.</span><span class="sxs-lookup"><span data-stu-id="fd61f-136">If you still see voice starvation errors, but can't hear any glitch, make sure you are setting [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Flags** to XAUDIO2\_END\_OF\_STREAM on the final buffer of a sound.</span></span> <span data-ttu-id="fd61f-137">Это говорит о том, что XAudio2 не ожидается, что все буферы должны быть доступны сразу после завершения этого.</span><span class="sxs-lookup"><span data-stu-id="fd61f-137">This tells XAudio2 not to expect any more buffers necessarily to be available as soon as this one completes.</span></span>

    <span data-ttu-id="fd61f-138">В других случаях:</span><span class="sxs-lookup"><span data-stu-id="fd61f-138">In the other cases:</span></span>

    -   <span data-ttu-id="fd61f-139">Сократите число активных голосов и эффектов в графе, особенно дорогостоящих эффектов, таких как переглаголы.</span><span class="sxs-lookup"><span data-stu-id="fd61f-139">Reduce the number of active voices and effects in the graph, especially expensive effects like reverb.</span></span>
    -   <span data-ttu-id="fd61f-140">Отключите голоса и эффекты, которые вы не используете.</span><span class="sxs-lookup"><span data-stu-id="fd61f-140">Disable voices and effects you're not using.</span></span>
    -   <span data-ttu-id="fd61f-141">Используйте \_ \_ Флаги XAUDIO2 Voice НОСРК и \_ XAUDIO2 \_ в [**IXAudio2:: креатесаурцевоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), когда это возможно.</span><span class="sxs-lookup"><span data-stu-id="fd61f-141">Use the XAUDIO2\_VOICE\_NOSRC and XAUDIO2\_VOICE\_NOPITCH flags in [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), whenever possible.</span></span> <span data-ttu-id="fd61f-142">Преобразование частоты дискретизации является дорогостоящим.</span><span class="sxs-lookup"><span data-stu-id="fd61f-142">Sample rate conversion is costly.</span></span>
    -   <span data-ttu-id="fd61f-143">Уменьшите частоту выборки отдельных голосов.</span><span class="sxs-lookup"><span data-stu-id="fd61f-143">Reduce the sample rate of individual voices.</span></span> <span data-ttu-id="fd61f-144">Например, субмикс голоса, на котором размещено действие, может иметь меньшую частоту выборки, чем отправку исходного голоса.</span><span class="sxs-lookup"><span data-stu-id="fd61f-144">For example, a submix voice hosting a reverb effect can have a lower sample rate than the source voice sending to it.</span></span> <span data-ttu-id="fd61f-145">Такие звуки, как взрывы и гуншотс, которые не нуждаются в высокой точности, также могут быть записаны с низкой частотой выборки.</span><span class="sxs-lookup"><span data-stu-id="fd61f-145">Sounds such as explosions and gunshots that don't need high fidelity can also be recorded at lower sample rates.</span></span>
    -   <span data-ttu-id="fd61f-146">Убедитесь, что реализации обратного вызова выполняют как можно меньше работы и никогда не блокируют.</span><span class="sxs-lookup"><span data-stu-id="fd61f-146">Ensure that callback implementations do as little work as possible and never block.</span></span>
    -   <span data-ttu-id="fd61f-147">Сократите число вызовов XAudio2.</span><span class="sxs-lookup"><span data-stu-id="fd61f-147">Make fewer calls to XAudio2.</span></span> <span data-ttu-id="fd61f-148">Параметры звука обычно не нуждаются в обновлении для каждого кадра видео.</span><span class="sxs-lookup"><span data-stu-id="fd61f-148">Audio parameters usually don't need to be updated for every video frame.</span></span> <span data-ttu-id="fd61f-149">Все равно 30 мс или достаточно.</span><span class="sxs-lookup"><span data-stu-id="fd61f-149">Every 30 ms or so is sufficient.</span></span> <span data-ttu-id="fd61f-150">Необходимо устранить избыточные вызовы, такие как настройка тома несколько раз в ходе быстрой успешной операции.</span><span class="sxs-lookup"><span data-stu-id="fd61f-150">You should eliminate redundant calls, such as setting volume several times in quick succession.</span></span>
    -   <span data-ttu-id="fd61f-151">Сократите общую загрузку ЦП игры.</span><span class="sxs-lookup"><span data-stu-id="fd61f-151">Reduce the game's overall CPU usage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd61f-152">См. также</span><span class="sxs-lookup"><span data-stu-id="fd61f-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd61f-153">Отладочные средства</span><span class="sxs-lookup"><span data-stu-id="fd61f-153">Debugging Facilities</span></span>](debugging-facilities.md)
</dt> <dt>

[<span data-ttu-id="fd61f-154">Справочник по программированию в XAudio2</span><span class="sxs-lookup"><span data-stu-id="fd61f-154">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
