---
description: Декодер Windows Media Audio декодирует звуковые потоки, закодированные кодировщиком Windows Media Audio.
ms.assetid: 2d8e4a97-34a7-4eee-9567-7ae98fa282b9
title: Декодер Windows Media Audio (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70f11242f237b8d9709baea6d445a8426236913c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694745"
---
# <a name="windows-media-audio-decoder"></a><span data-ttu-id="a51b8-103">Декодер Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="a51b8-103">Windows Media Audio Decoder</span></span>

<span data-ttu-id="a51b8-104">Декодер Windows Media Audio декодирует звуковые потоки, закодированные [**кодировщиком Windows Media Audio**](windowsmediaaudioencoder.md).</span><span class="sxs-lookup"><span data-stu-id="a51b8-104">The Windows Media Audio decoder decodes audio streams that were encoded by the [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md).</span></span> <span data-ttu-id="a51b8-105">Кодировщик и декодер поддерживают три категории закодированных аудио: Windows Media Audio Standard, Windows Media Audio Professional и Windows Media Audio без потерь.</span><span class="sxs-lookup"><span data-stu-id="a51b8-105">The encoder and decoder support three categories of encoded audio: Windows Media Audio Standard, Windows Media Audio Professional, and Windows Media Audio Lossless.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="a51b8-106">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="a51b8-106">Class Identifier</span></span>

<span data-ttu-id="a51b8-107">Идентификатор класса (CLSID) для декодера Windows Media Audio представлен константой **CLSID \_ квмадекмедиаобжект**.</span><span class="sxs-lookup"><span data-stu-id="a51b8-107">The class identifier (CLSID) for the Windows Media Audio decoder is represented by the constant **CLSID\_CWMADecMediaObject**.</span></span> <span data-ttu-id="a51b8-108">Вы можете создать экземпляр звукового декодера, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="a51b8-108">You can create an instance of the audio decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="a51b8-109">Форматы входных данных</span><span class="sxs-lookup"><span data-stu-id="a51b8-109">Input Formats</span></span>

<span data-ttu-id="a51b8-110">В следующей таблице показаны Теги звукового формата, которые представляют входные категории, поддерживаемые декодером Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="a51b8-110">The following table shows the audio format tags that represent the input categories supported by the Windows Media Audio decoder.</span></span> <span data-ttu-id="a51b8-111">Сведения о том, как задать типы входных и выходных данных для декодера, см. в разделе [Настройка декодирования звука](configuringaudiodecoding.md).</span><span class="sxs-lookup"><span data-stu-id="a51b8-111">For information about how to set the input and output types for the decoder, see [Configuring Audio Decoding](configuringaudiodecoding.md).</span></span>



| <span data-ttu-id="a51b8-112">Формат константы тега</span><span class="sxs-lookup"><span data-stu-id="a51b8-112">Format tag constant</span></span>             | <span data-ttu-id="a51b8-113">Формат значения тега</span><span class="sxs-lookup"><span data-stu-id="a51b8-113">Format tag value</span></span> | <span data-ttu-id="a51b8-114">Формат аудио</span><span class="sxs-lookup"><span data-stu-id="a51b8-114">Audio format</span></span>                     |
|---------------------------------|------------------|----------------------------------|
| <span data-ttu-id="a51b8-115">\_Формат волны \_ WMAUDIO2</span><span class="sxs-lookup"><span data-stu-id="a51b8-115">WAVE\_FORMAT\_WMAUDIO2</span></span>          | <span data-ttu-id="a51b8-116">0x0161</span><span class="sxs-lookup"><span data-stu-id="a51b8-116">0x0161</span></span>           | <span data-ttu-id="a51b8-117">Windows Media Audio Standard</span><span class="sxs-lookup"><span data-stu-id="a51b8-117">Windows Media Audio Standard</span></span>     |
| <span data-ttu-id="a51b8-118">\_Формат волны \_ WMAUDIO3</span><span class="sxs-lookup"><span data-stu-id="a51b8-118">WAVE\_FORMAT\_WMAUDIO3</span></span>          | <span data-ttu-id="a51b8-119">0x0162</span><span class="sxs-lookup"><span data-stu-id="a51b8-119">0x0162</span></span>           | <span data-ttu-id="a51b8-120">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="a51b8-120">Windows Media Audio Professional</span></span> |
| <span data-ttu-id="a51b8-121">\_Формат Wave \_ вмаудио \_ без потерь</span><span class="sxs-lookup"><span data-stu-id="a51b8-121">WAVE\_FORMAT\_WMAUDIO\_LOSSLESS</span></span> | <span data-ttu-id="a51b8-122">0x0163</span><span class="sxs-lookup"><span data-stu-id="a51b8-122">0x0163</span></span>           | <span data-ttu-id="a51b8-123">Windows Media Audio без потерь</span><span class="sxs-lookup"><span data-stu-id="a51b8-123">Windows Media Audio Lossless</span></span>     |



 

## <a name="output-formats"></a><span data-ttu-id="a51b8-124">Форматы выходных данных</span><span class="sxs-lookup"><span data-stu-id="a51b8-124">Output Formats</span></span>

<span data-ttu-id="a51b8-125">В следующей таблице показаны Теги звукового формата, представляющие типы выходных данных, поддерживаемые **декодером Windows Media Audio**.</span><span class="sxs-lookup"><span data-stu-id="a51b8-125">The following table shows the audio format tags that represent the output types supported by the **Windows Media Audio Decoder**.</span></span> <span data-ttu-id="a51b8-126">Сведения о том, как задать типы входных и выходных данных для декодера, см. в разделе [Настройка кодирования звука](configuringaudioencoding.md).</span><span class="sxs-lookup"><span data-stu-id="a51b8-126">For information about how to set the input and output types for the decoder, see [Configuring Audio Encoding](configuringaudioencoding.md).</span></span>



| <span data-ttu-id="a51b8-127">Формат константы тега</span><span class="sxs-lookup"><span data-stu-id="a51b8-127">Format tag constant</span></span>       | <span data-ttu-id="a51b8-128">Формат значения тега</span><span class="sxs-lookup"><span data-stu-id="a51b8-128">Format tag value</span></span> | <span data-ttu-id="a51b8-129">Формат аудио</span><span class="sxs-lookup"><span data-stu-id="a51b8-129">Audio format</span></span>                                          |
|---------------------------|------------------|-------------------------------------------------------|
| <span data-ttu-id="a51b8-130">формат ВОЛНового \_ \_ PCM</span><span class="sxs-lookup"><span data-stu-id="a51b8-130">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="a51b8-131">0x0001</span><span class="sxs-lookup"><span data-stu-id="a51b8-131">0x0001</span></span>           | <span data-ttu-id="a51b8-132">Формат PCM</span><span class="sxs-lookup"><span data-stu-id="a51b8-132">PCM format</span></span>                                            |
| <span data-ttu-id="a51b8-133">\_Формат волны \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="a51b8-133">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="a51b8-134">0x0003</span><span class="sxs-lookup"><span data-stu-id="a51b8-134">0x0003</span></span>           | <span data-ttu-id="a51b8-135">IEEE с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="a51b8-135">IEEE floating point</span></span>                                   |
| <span data-ttu-id="a51b8-136">формат ВОЛНового \_ \_ расширения</span><span class="sxs-lookup"><span data-stu-id="a51b8-136">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="a51b8-137">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="a51b8-137">0xFFFE</span></span>           | <span data-ttu-id="a51b8-138">Формат PCM/IEEE в структуре **вавеформатекстенсибле**</span><span class="sxs-lookup"><span data-stu-id="a51b8-138">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="a51b8-139">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="a51b8-139">Interfaces</span></span>

<span data-ttu-id="a51b8-140">Объект звукового декодера предоставляет интерфейс **имедиаобжект** , чтобы объект можно было использовать в качестве объекта мультимедиа DirectX (DMO), и он предоставляет интерфейс **имфтрансформ** , чтобы объект можно было использовать в качестве Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="a51b8-140">An audio decoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="a51b8-141">Декодер Windows Media Audio работает как DMO или MFT в зависимости от того, какие интерфейсы получены и какая версия Windows работает.</span><span class="sxs-lookup"><span data-stu-id="a51b8-141">A Windows Media Audio decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="a51b8-142">В следующей таблице показаны условия, при которых звуковой декодер ведет себя как DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="a51b8-142">The following table shows the conditions under which an audio decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="a51b8-143">Операционная система</span><span class="sxs-lookup"><span data-stu-id="a51b8-143">Operating system</span></span> | <span data-ttu-id="a51b8-144">Поведение декодера</span><span class="sxs-lookup"><span data-stu-id="a51b8-144">Decoder behavior</span></span>                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a51b8-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a51b8-145">Windows XP</span></span>       | <span data-ttu-id="a51b8-146">Декодер Windows Media Audio всегда ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="a51b8-146">A Windows Media Audio decoder always behaves as a DMO.</span></span>                                                                                                                                |
| <span data-ttu-id="a51b8-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a51b8-147">Windows Vista</span></span>    | <span data-ttu-id="a51b8-148">По умолчанию декодер Windows Media Audio ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="a51b8-148">By default, a Windows Media Audio decoder behaves as a DMO.</span></span> <span data-ttu-id="a51b8-149">Если вы получаете интерфейс **имфтрансформ** или интерфейс **ипропертисторе** для звукового декодера, он ведет себя как MFT.</span><span class="sxs-lookup"><span data-stu-id="a51b8-149">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on an audio decoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="a51b8-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a51b8-150">Windows 7</span></span>        | <span data-ttu-id="a51b8-151">По умолчанию декодер Windows Media Audio ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="a51b8-151">By default, a Windows Media Audio decoder behaves as a DMO.</span></span> <span data-ttu-id="a51b8-152">Если вы получаете интерфейс **имфтрансформ** для звукового декодера, он ведет себя как MFT.</span><span class="sxs-lookup"><span data-stu-id="a51b8-152">If you obtain an **IMFTransform** interface on an audio decoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="properties"></a><span data-ttu-id="a51b8-153">Свойства</span><span class="sxs-lookup"><span data-stu-id="a51b8-153">Properties</span></span>

<span data-ttu-id="a51b8-154">Декодер Windows Media Audio поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a51b8-154">The Windows Media Audio decoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a51b8-155">Свойство</span><span class="sxs-lookup"><span data-stu-id="a51b8-155">Property</span></span></th>
<th><span data-ttu-id="a51b8-156">Описание</span><span class="sxs-lookup"><span data-stu-id="a51b8-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a51b8-157"><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></span><span class="sxs-lookup"><span data-stu-id="a51b8-157"><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></span></span></td>
<td><span data-ttu-id="a51b8-158">Указывает максимальное количество дополнительных выборок PCM, которые могут быть возвращены в конце декодирования файла.</span><span class="sxs-lookup"><span data-stu-id="a51b8-158">Specifies the maximum number of additional PCM samples that might be returned at the end of decoding a file.</span></span><br/> <dl> <span data-ttu-id="a51b8-159">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="a51b8-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="a51b8-160">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="a51b8-160">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="a51b8-161">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a51b8-161">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a51b8-162"><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a51b8-162"><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></span></span></td>
<td><span data-ttu-id="a51b8-163">Указывает режим управления динамическим диапазоном, который будет использоваться декодером аудио.</span><span class="sxs-lookup"><span data-stu-id="a51b8-163">Specifies the dynamic-range control mode that the audio decoder will use.</span></span><br/> <dl> <span data-ttu-id="a51b8-164">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="a51b8-164">Windows XP and later.</span></span><br />
<span data-ttu-id="a51b8-165">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="a51b8-165">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="a51b8-166">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="a51b8-166">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a51b8-167"><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></span><span class="sxs-lookup"><span data-stu-id="a51b8-167"><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></span></span></td>
<td><span data-ttu-id="a51b8-168">Указывает предоставляемые автором коэффициенты свертывания для декодирования многоканального звука для меньшего количества каналов, чем содержит закодированный поток.</span><span class="sxs-lookup"><span data-stu-id="a51b8-168">Specifies the author-supplied fold-down coefficients for decoding multichannel audio for fewer channels than the encoded stream contains.</span></span> <br/> <dl> <span data-ttu-id="a51b8-169">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="a51b8-169">Windows XP and later.</span></span><br />
<span data-ttu-id="a51b8-170">Professional</span><span class="sxs-lookup"><span data-stu-id="a51b8-170">Professional</span></span><br />
<span data-ttu-id="a51b8-171">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="a51b8-171">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a51b8-172"><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a51b8-172"><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></span></span></td>
<td><span data-ttu-id="a51b8-173">Указывает, должен ли декодер звука предоставлять выходные данные высокого разрешения.</span><span class="sxs-lookup"><span data-stu-id="a51b8-173">Specifies whether the audio decoder should deliver high-resolution output.</span></span><br/> <dl> <span data-ttu-id="a51b8-174">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="a51b8-174">Windows XP and later.</span></span><br />
<span data-ttu-id="a51b8-175">Профессиональная, без потерь.</span><span class="sxs-lookup"><span data-stu-id="a51b8-175">Professional, Lossless.</span></span><br />
<span data-ttu-id="a51b8-176">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="a51b8-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a51b8-177"><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a51b8-177"><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></span></span></td>
<td><span data-ttu-id="a51b8-178">Указывает, должен ли звуковой декодер выполняться Lt-Rt свертывания.</span><span class="sxs-lookup"><span data-stu-id="a51b8-178">Specifies whether the audio decoder should perform Lt-Rt fold down.</span></span><br/> <dl> <span data-ttu-id="a51b8-179">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="a51b8-179">Windows Vista and later.</span></span><br />
<span data-ttu-id="a51b8-180">Professional.</span><span class="sxs-lookup"><span data-stu-id="a51b8-180">Professional.</span></span><br />
<span data-ttu-id="a51b8-181">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="a51b8-181">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a51b8-182"><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></span><span class="sxs-lookup"><span data-stu-id="a51b8-182"><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></span></span></td>
<td><span data-ttu-id="a51b8-183">Указывает конфигурацию динамика на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="a51b8-183">Specifies the speaker configuration on the client computer.</span></span><br/> <dl> <span data-ttu-id="a51b8-184">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="a51b8-184">Windows XP and later.</span></span><br />
<span data-ttu-id="a51b8-185">Professional.</span><span class="sxs-lookup"><span data-stu-id="a51b8-185">Professional.</span></span><br />
<span data-ttu-id="a51b8-186">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="a51b8-186">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a51b8-187"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="a51b8-187"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span></span></td>
<td><span data-ttu-id="a51b8-188">Указывает средний уровень громкости звукового содержимого.</span><span class="sxs-lookup"><span data-stu-id="a51b8-188">Specifies the average volume level of audio content.</span></span><br/> <dl> <span data-ttu-id="a51b8-189">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="a51b8-189">Windows XP and later.</span></span><br />
<span data-ttu-id="a51b8-190">Профессиональная, без потерь.</span><span class="sxs-lookup"><span data-stu-id="a51b8-190">Professional, Lossless.</span></span><br />
<span data-ttu-id="a51b8-191">Read/write.</span><span class="sxs-lookup"><span data-stu-id="a51b8-191">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a51b8-192"><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></span><span class="sxs-lookup"><span data-stu-id="a51b8-192"><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></span></span></td>
<td><span data-ttu-id="a51b8-193">Указывает требуемый средний уровень громкости выходного звукового содержимого.</span><span class="sxs-lookup"><span data-stu-id="a51b8-193">Specifies the desired average volume level of output audio content.</span></span><br/> <dl> <span data-ttu-id="a51b8-194">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="a51b8-194">Windows XP and later.</span></span><br />
<span data-ttu-id="a51b8-195">Профессиональная, без потерь.</span><span class="sxs-lookup"><span data-stu-id="a51b8-195">Professional, Lossless.</span></span><br />
<span data-ttu-id="a51b8-196">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="a51b8-196">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a51b8-197"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="a51b8-197"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span></span></td>
<td><span data-ttu-id="a51b8-198">Указывает самый высокий уровень громкости в аудио содержимом.</span><span class="sxs-lookup"><span data-stu-id="a51b8-198">Specifies the highest volume level occurring in audio content.</span></span><br/> <dl> <span data-ttu-id="a51b8-199">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="a51b8-199">Windows XP and later.</span></span><br />
<span data-ttu-id="a51b8-200">Профессиональная, без потерь.</span><span class="sxs-lookup"><span data-stu-id="a51b8-200">Professional, Lossless.</span></span><br />
<span data-ttu-id="a51b8-201">Read/write.</span><span class="sxs-lookup"><span data-stu-id="a51b8-201">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a51b8-202"><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></span><span class="sxs-lookup"><span data-stu-id="a51b8-202"><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></span></span></td>
<td><span data-ttu-id="a51b8-203">Указывает требуемый максимальный уровень громкости выходного аудио содержимого.</span><span class="sxs-lookup"><span data-stu-id="a51b8-203">Specifies the desired maximum volume level of output audio content.</span></span><br/> <dl> <span data-ttu-id="a51b8-204">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="a51b8-204">Windows XP and later.</span></span><br />
<span data-ttu-id="a51b8-205">Профессиональная, без потерь.</span><span class="sxs-lookup"><span data-stu-id="a51b8-205">Professional, Lossless.</span></span><br />
<span data-ttu-id="a51b8-206">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="a51b8-206">Write-only.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="a51b8-207">Требования</span><span class="sxs-lookup"><span data-stu-id="a51b8-207">Requirements</span></span>



| <span data-ttu-id="a51b8-208">Требование</span><span class="sxs-lookup"><span data-stu-id="a51b8-208">Requirement</span></span> | <span data-ttu-id="a51b8-209">Значение</span><span class="sxs-lookup"><span data-stu-id="a51b8-209">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a51b8-210">Клиент</span><span class="sxs-lookup"><span data-stu-id="a51b8-210">Client</span></span><br/> | <span data-ttu-id="a51b8-211">Windows XP, Windows Vista или Windows 7</span><span class="sxs-lookup"><span data-stu-id="a51b8-211">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="a51b8-212">Header</span><span class="sxs-lookup"><span data-stu-id="a51b8-212">Header</span></span><br/> | <dl> <span data-ttu-id="a51b8-213"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a51b8-213"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="a51b8-214">DLL</span><span class="sxs-lookup"><span data-stu-id="a51b8-214">DLL</span></span><br/>    | <dl> <span data-ttu-id="a51b8-215"><dt>Wmadmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a51b8-215"><dt>Wmadmod.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a51b8-216">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a51b8-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a51b8-217">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="a51b8-217">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="a51b8-218">Реализация кодека</span><span class="sxs-lookup"><span data-stu-id="a51b8-218">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 




