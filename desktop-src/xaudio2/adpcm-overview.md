---
description: Адаптивный разностный импульсный код (ADPCM) — это формат сжатия с потерей данных, который реализуется для XAudio2, чтобы предоставить дополнительные возможности для указания размера блока образца сжатия.
ms.assetid: ae8a0a3e-293c-8193-d252-046d79771cfb
title: Общие сведения о ADPCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb918a611cb0840b2f02dfb13b547b795fb3304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712291"
---
# <a name="adpcm-overview"></a><span data-ttu-id="abc2b-103">Общие сведения о ADPCM</span><span class="sxs-lookup"><span data-stu-id="abc2b-103">ADPCM Overview</span></span>

<span data-ttu-id="abc2b-104">Адаптивный разностный импульсный код (ADPCM) — это формат сжатия с потерей данных, который реализуется для XAudio2, чтобы предоставить дополнительные возможности для указания размера блока образца сжатия.</span><span class="sxs-lookup"><span data-stu-id="abc2b-104">Adaptive Differential Pulse Code Modulation (ADPCM) is a lossy compression format that is implemented for XAudio2 to provide additional features for specifying the size of the compression sample block.</span></span> <span data-ttu-id="abc2b-105">При использовании формата сжатия потери данных некоторые данные изменяются и теряются во время сжатия.</span><span class="sxs-lookup"><span data-stu-id="abc2b-105">With a lossy compression format some data is altered and lost during compression.</span></span> <span data-ttu-id="abc2b-106">ADPCM может обеспечить степень сжатия до 4:1.</span><span class="sxs-lookup"><span data-stu-id="abc2b-106">ADPCM can achieve compression ratios of up to 4:1.</span></span>

<span data-ttu-id="abc2b-107">Реализация ADPCM для XAudio2 предоставляет дополнительные возможности для указания размера блока образца сжатия.</span><span class="sxs-lookup"><span data-stu-id="abc2b-107">The implementation of ADPCM for XAudio2 provides additional features to specify the size of the compression sample block.</span></span> <span data-ttu-id="abc2b-108">ADPCM позволяет конструктору аудио выбрать параметр, который является подходящим компромиссом между размером, качеством и разрешением (для размещения точек цикла).</span><span class="sxs-lookup"><span data-stu-id="abc2b-108">ADPCM enables the audio designer to choose a setting that is an appropriate compromise among size, quality, and resolution (for placing loop points).</span></span>

<span data-ttu-id="abc2b-109">XAudio2 использует измененную версию кодека Microsoft ADPCM, поддерживающую расширенное форматирование данных, необходимое для предоставления пользовательских размеров блоков выборки.</span><span class="sxs-lookup"><span data-stu-id="abc2b-109">XAudio2 uses a modified version of the Microsoft ADPCM codec that supports the extended data formatting required to provide custom sample block sizes.</span></span> <span data-ttu-id="abc2b-110">По этой причине звуковые модули не поддерживают эту версию аудиокодека ADPCM, поэтому XAudio2 не могут воспроизводить аудиоданные.</span><span class="sxs-lookup"><span data-stu-id="abc2b-110">For this reason, XAudio2 audio data cannot be played by audio engines that do not support this version of the ADPCM codec.</span></span>

> [!Note]  
> <span data-ttu-id="abc2b-111">В настоящее время сжатие ADPCM доступно только для Windows, включая XNA Game Studio Express для развертываний Windows.</span><span class="sxs-lookup"><span data-stu-id="abc2b-111">Currently, ADPCM compression is only available for Windows, including XNA Game Studio Express for Windows deployments.</span></span>

 

## <a name="adpcm-encoding"></a><span data-ttu-id="abc2b-112">Кодировка ADPCM</span><span class="sxs-lookup"><span data-stu-id="abc2b-112">ADPCM Encoding</span></span>

<span data-ttu-id="abc2b-113">Звуковые данные кодируются в ADPCM с помощью программы командной строки Адпкменкоде.</span><span class="sxs-lookup"><span data-stu-id="abc2b-113">Audio data is encoded to ADPCM using the AdpcmEncode command-line tool.</span></span>

-   <span data-ttu-id="abc2b-114">адпкменкоде</span><span class="sxs-lookup"><span data-stu-id="abc2b-114">AdpcmEncode</span></span>

    <span data-ttu-id="abc2b-115">Чтобы кодировать звуковые файлы как ADPCM для использования с XAudio2, используйте программу командной строки **адпкменкоде** .</span><span class="sxs-lookup"><span data-stu-id="abc2b-115">In order to encode audio files as ADPCM for use with XAudio2, use the **AdpcmEncode** command-line tool.</span></span>

## <a name="adpcm-decoding"></a><span data-ttu-id="abc2b-116">ADPCM декодирование</span><span class="sxs-lookup"><span data-stu-id="abc2b-116">ADPCM Decoding</span></span>

<span data-ttu-id="abc2b-117">Программное декодирование ADPCM поддерживается в XAudio2.</span><span class="sxs-lookup"><span data-stu-id="abc2b-117">Software decoding of ADPCM is supported in XAudio2.</span></span>

-   <span data-ttu-id="abc2b-118">XAudio2</span><span class="sxs-lookup"><span data-stu-id="abc2b-118">XAudio2</span></span>

    <span data-ttu-id="abc2b-119">Чтобы использовать данные в кодировке ADPCM в XAudio2, необходимо инициализировать структуру **адпкмвавеформат** с использованием значений, характерных для ADPCM, и передать ее в качестве аргумента в [**IXAudio2:: креатесаурцевоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) при создании исходного голоса.</span><span class="sxs-lookup"><span data-stu-id="abc2b-119">In order to use ADPCM encoded data in XAudio2, you need to initialize a **ADPCMWAVEFORMAT** structure with ADPCM specific values, and pass it as an argument to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) when you create a source voice.</span></span> <span data-ttu-id="abc2b-120">Пример загрузки и воспроизведения звука в XAudio2 см. в статье [как воспроизвести звук с помощью XAudio2](how-to--play-a-sound-with-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="abc2b-120">For an example of loading and playing a sound in XAudio2, see [How to: Play a Sound with XAudio2](how-to--play-a-sound-with-xaudio2.md).</span></span>

## <a name="samplesperblock"></a><span data-ttu-id="abc2b-121">самплесперблокк</span><span class="sxs-lookup"><span data-stu-id="abc2b-121">SamplesPerBlock</span></span>

<span data-ttu-id="abc2b-122">Сжатие ADPCM выполняется путем разделения звуковой волны на блоки и прогнозирования вариации образцов аудио в каждом блоке.</span><span class="sxs-lookup"><span data-stu-id="abc2b-122">ADPCM compression works by separating the waveform into blocks, and predicting the variation of the waveform samples within each block.</span></span> <span data-ttu-id="abc2b-123">Размер блоков измеряется в примерах.</span><span class="sxs-lookup"><span data-stu-id="abc2b-123">The size of the blocks is measured in samples.</span></span> <span data-ttu-id="abc2b-124">Наименьшим размером блока является 32 выборок, а самым высоким — 512.</span><span class="sxs-lookup"><span data-stu-id="abc2b-124">The smallest block size is 32 samples, and the highest is 512 samples.</span></span>

<span data-ttu-id="abc2b-125">Более крупные блоки позволяют лучше сжимать, что приводит к уменьшению размеров файлов, но за счет увеличения качества звука и разрешения для выровняйте точки цикла.</span><span class="sxs-lookup"><span data-stu-id="abc2b-125">Larger blocks allow better compression, which results in smaller file sizes, but at the expense of sound quality and resolution for aligning loop points.</span></span>

<span data-ttu-id="abc2b-126">Как правило, изменение значения Самплесперблокк приводит к следующим компромиссам:</span><span class="sxs-lookup"><span data-stu-id="abc2b-126">In general, modifying the SamplesPerBlock value results in these tradeoffs:</span></span>



| <span data-ttu-id="abc2b-127">Если Самплесперблокк...</span><span class="sxs-lookup"><span data-stu-id="abc2b-127">If SamplesPerBlock...</span></span>      | <span data-ttu-id="abc2b-128">Сжатие файлов</span><span class="sxs-lookup"><span data-stu-id="abc2b-128">File Compression</span></span> | <span data-ttu-id="abc2b-129">Качество звука</span><span class="sxs-lookup"><span data-stu-id="abc2b-129">Sound Quality</span></span> | <span data-ttu-id="abc2b-130">Разрешение точки цикла</span><span class="sxs-lookup"><span data-stu-id="abc2b-130">Loop Point Resolution</span></span> |
|----------------------------|------------------|---------------|-----------------------|
| <span data-ttu-id="abc2b-131">Увеличение (до максимума 512)</span><span class="sxs-lookup"><span data-stu-id="abc2b-131">Increases (up to max 512)</span></span>  | <span data-ttu-id="abc2b-132">Повышения</span><span class="sxs-lookup"><span data-stu-id="abc2b-132">Increases</span></span>        | <span data-ttu-id="abc2b-133">Уменьшать</span><span class="sxs-lookup"><span data-stu-id="abc2b-133">Decreases</span></span>     | <span data-ttu-id="abc2b-134">Уменьшать</span><span class="sxs-lookup"><span data-stu-id="abc2b-134">Decreases</span></span>             |
| <span data-ttu-id="abc2b-135">Уменьшение (до минимума 32)</span><span class="sxs-lookup"><span data-stu-id="abc2b-135">Decreases (down to min 32)</span></span> | <span data-ttu-id="abc2b-136">Уменьшать</span><span class="sxs-lookup"><span data-stu-id="abc2b-136">Decreases</span></span>        | <span data-ttu-id="abc2b-137">Повышения</span><span class="sxs-lookup"><span data-stu-id="abc2b-137">Increases</span></span>     | <span data-ttu-id="abc2b-138">Повышения</span><span class="sxs-lookup"><span data-stu-id="abc2b-138">Increases</span></span>             |



 

## <a name="restrictions"></a><span data-ttu-id="abc2b-139">Ограничения</span><span class="sxs-lookup"><span data-stu-id="abc2b-139">Restrictions</span></span>

<span data-ttu-id="abc2b-140">Так как в ADPCM используются блоки примеров, которые вычисляются по одному за другим, волна, сжатая с помощью ADPCM, может иметь незаконченный, незавершенный блок в конце.</span><span class="sxs-lookup"><span data-stu-id="abc2b-140">Because ADPCM uses sample blocks that are aligned one after the other, a wave compressed with ADPCM may have an unfinished, partial block at its end.</span></span> <span data-ttu-id="abc2b-141">Декодер ADPCM создает бездействия в оставшейся части этого частичного блока, что позволяет эффективно выполнять циклическое воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="abc2b-141">The ADPCM decoder generates silence for the remainder of this partial block, which keeps the wave from looping seamlessly.</span></span>

<span data-ttu-id="abc2b-142">Значение параметра *самплесперблокк* влияет на разрешение, с помощью которого можно выстроить волновые данные и точки цикла.</span><span class="sxs-lookup"><span data-stu-id="abc2b-142">The value of the *SamplesPerBlock* parameter affects the resolution with which you can align wave data and loop points.</span></span>

<span data-ttu-id="abc2b-143">Если вы попытаетесь применить сжатие к неоднородной волновой волны, будет выдано сообщение об ошибке или предупреждение в зависимости от того, используется ли волна в любом цикле событий воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="abc2b-143">If you try to apply compression to a non-aligned wave, you will get an error or a warning depending on whether the wave is used in any looping play events.</span></span> <span data-ttu-id="abc2b-144">Нельзя сжимать волн, используемый в циклах событий воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="abc2b-144">You cannot compress a wave used in any looping play events.</span></span> <span data-ttu-id="abc2b-145">Удалите его из цикла событий воспроизведения и повторно примените сжатие.</span><span class="sxs-lookup"><span data-stu-id="abc2b-145">Remove it from the looping play events, and re-apply compression.</span></span>

<span data-ttu-id="abc2b-146">При использовании волн исключительно в режиме без цикла ограничение по выравниванию блока выборки не применяется.</span><span class="sxs-lookup"><span data-stu-id="abc2b-146">If you use the wave exclusively in non-looping mode, the sample block alignment restriction does not apply.</span></span>

## <a name="adpcm-file-structure"></a><span data-ttu-id="abc2b-147">Файловая структура ADPCM</span><span class="sxs-lookup"><span data-stu-id="abc2b-147">ADPCM File Structure</span></span>

<span data-ttu-id="abc2b-148">ADPCM-файл — это стандартный файл Metallica со следующими типами блоков.</span><span class="sxs-lookup"><span data-stu-id="abc2b-148">An ADPCM file is a standard RIFF file with the following chunk types.</span></span>



| <span data-ttu-id="abc2b-149">Блок FCC</span><span class="sxs-lookup"><span data-stu-id="abc2b-149">Chunk FCC</span></span>     | <span data-ttu-id="abc2b-150">Описание</span><span class="sxs-lookup"><span data-stu-id="abc2b-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abc2b-151">RIFF</span><span class="sxs-lookup"><span data-stu-id="abc2b-151">RIFF</span></span>          | <span data-ttu-id="abc2b-152">Стандартный блок Metallica, содержащий тип файла со значением WAVE в первых четырех байтах его раздела данных, а также другие фрагменты в файле в оставшейся части его раздела данных.</span><span class="sxs-lookup"><span data-stu-id="abc2b-152">Standard RIFF chunk containing a file type with the value WAVE in the first four bytes of its data section and the other chunks in the file in the remainder of its data section.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="abc2b-153">FMT</span><span class="sxs-lookup"><span data-stu-id="abc2b-153">fmt</span></span>           | <span data-ttu-id="abc2b-154">Содержит заголовок Format для файла ADPCM.</span><span class="sxs-lookup"><span data-stu-id="abc2b-154">Contains the format header for the ADPCM file.</span></span> <span data-ttu-id="abc2b-155">Данные в этом блоке соответствуют структуре **адпкмвавеформат** .</span><span class="sxs-lookup"><span data-stu-id="abc2b-155">The data in this chunk corresponds to a **ADPCMWAVEFORMAT** structure.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="abc2b-156">.</span><span class="sxs-lookup"><span data-stu-id="abc2b-156">data</span></span>          | <span data-ttu-id="abc2b-157">Содержит закодированные звуковые данные ADPCM.</span><span class="sxs-lookup"><span data-stu-id="abc2b-157">Contains the encoded ADPCM audio data.</span></span> <span data-ttu-id="abc2b-158">При использовании ADPCM в XAudio2 необходимо прочитать содержимое фрагмента данных в буфер и передать его в исходный голоса в качестве элемента **паудиодата** в структуре [**\_ буфера XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="abc2b-158">When you use ADPCM in XAudio2, you need to read the contents of the data chunk into a buffer, and pass it to a source voice as the **pAudioData** member of an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="abc2b-159">Содержимое блока данных не нужно менять байтами.</span><span class="sxs-lookup"><span data-stu-id="abc2b-159">You don't need to byte swap the contents of the data chunk.</span></span>                                                                                                                            |
| <span data-ttu-id="abc2b-160">СМПЛ и всмп</span><span class="sxs-lookup"><span data-stu-id="abc2b-160">smpl and wsmp</span></span> | <span data-ttu-id="abc2b-161">Необязательные типы блоков, содержащие сведения о циклах для файла ADPCM.</span><span class="sxs-lookup"><span data-stu-id="abc2b-161">Optional chunk types containing the looping information for the ADPCM file.</span></span> <span data-ttu-id="abc2b-162">При использовании ADPCM в XAudio2 значения, содержащиеся в блоках СМПЛ или всмп, используются для заполнения **лупбегинлупленгс** и **лупкаунт** элементов структуры [**\_ буфера XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="abc2b-162">When you use ADPCM in XAudio2, the values contained in the smpl or wsmp chunks are used to populate the **LoopBeginLoopLength** and **LoopCount** members of the [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="abc2b-163">На Xbox 360 необходимо переключить данные, загружаемые из СМПЛ фрагмента, в учетную запись порядок следования байтов разницы между Windows и Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="abc2b-163">On the Xbox 360, you need to byte swap the data loaded from a smpl chunk to account for the endianness difference between Windows and Xbox 360.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="abc2b-164">См. также</span><span class="sxs-lookup"><span data-stu-id="abc2b-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abc2b-165">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="abc2b-165">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
