---
description: 'Кодировщик Windows Media Audio кодирует звуковые потоки. Кодировщик поддерживает три категории закодированных выходных данных: Windows Media Audio Standard, Windows Media Audio Professional и Windows Media Audio без потерь.'
ms.assetid: 1f6a3a9f-b534-4a6b-b773-0315c759624e
title: Кодировщик Windows Media Audio (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f1d5b9e5f890a43958bcc304dd2d305844fdb4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718090"
---
# <a name="windows-media-audio-encoder"></a><span data-ttu-id="dca92-104">Кодировщик Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="dca92-104">Windows Media Audio Encoder</span></span>

<span data-ttu-id="dca92-105">Кодировщик Windows Media Audio кодирует звуковые потоки.</span><span class="sxs-lookup"><span data-stu-id="dca92-105">The Windows Media Audio encoder encodes audio streams.</span></span> <span data-ttu-id="dca92-106">Кодировщик поддерживает три категории закодированных выходных данных: Windows Media Audio Standard, Windows Media Audio Professional и Windows Media Audio без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-106">The encoder supports three categories of encoded output: Windows Media Audio Standard, Windows Media Audio Professional, and Windows Media Audio Lossless.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="dca92-107">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="dca92-107">Class Identifier</span></span>

<span data-ttu-id="dca92-108">Идентификатор класса (CLSID) для кодировщика Windows Media Audio представлен константой **CLSID \_ квмаенкмедиаобжект**.</span><span class="sxs-lookup"><span data-stu-id="dca92-108">The class identifier (CLSID) for the Windows Media Audio Encoder is represented by the constant **CLSID\_CWMAEncMediaObject**.</span></span> <span data-ttu-id="dca92-109">Вы можете создать экземпляр звукового кодировщика, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="dca92-109">You can create an instance of the audio encoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="dca92-110">Форматы входных данных</span><span class="sxs-lookup"><span data-stu-id="dca92-110">Input Formats</span></span>

<span data-ttu-id="dca92-111">В следующей таблице показаны Теги звукового формата, представляющие входные категории, поддерживаемые кодировщиком Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="dca92-111">The following table shows the audio format tags that represent the input categories supported by the Windows Media Audio encoder.</span></span> <span data-ttu-id="dca92-112">Сведения о том, как задать типы входных и выходных данных для кодировщика, см. в разделе [Настройка кодирования звука](configuringaudioencoding.md).</span><span class="sxs-lookup"><span data-stu-id="dca92-112">For information about how to set the input and output types for the encoder, see [Configuring Audio Encoding](configuringaudioencoding.md).</span></span>



| <span data-ttu-id="dca92-113">Формат константы тега</span><span class="sxs-lookup"><span data-stu-id="dca92-113">Format tag constant</span></span>       | <span data-ttu-id="dca92-114">Формат значения тега</span><span class="sxs-lookup"><span data-stu-id="dca92-114">Format tag value</span></span> | <span data-ttu-id="dca92-115">Формат аудио</span><span class="sxs-lookup"><span data-stu-id="dca92-115">Audio format</span></span>                                          |
|---------------------------|------------------|-------------------------------------------------------|
| <span data-ttu-id="dca92-116">формат ВОЛНового \_ \_ PCM</span><span class="sxs-lookup"><span data-stu-id="dca92-116">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="dca92-117">0x0001</span><span class="sxs-lookup"><span data-stu-id="dca92-117">0x0001</span></span>           | <span data-ttu-id="dca92-118">Формат PCM</span><span class="sxs-lookup"><span data-stu-id="dca92-118">PCM format</span></span>                                            |
| <span data-ttu-id="dca92-119">\_Формат волны \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="dca92-119">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="dca92-120">0x0003</span><span class="sxs-lookup"><span data-stu-id="dca92-120">0x0003</span></span>           | <span data-ttu-id="dca92-121">IEEE с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="dca92-121">IEEE floating point</span></span>                                   |
| <span data-ttu-id="dca92-122">формат ВОЛНового \_ \_ расширения</span><span class="sxs-lookup"><span data-stu-id="dca92-122">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="dca92-123">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="dca92-123">0xFFFE</span></span>           | <span data-ttu-id="dca92-124">Формат PCM/IEEE в структуре **вавеформатекстенсибле**</span><span class="sxs-lookup"><span data-stu-id="dca92-124">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="dca92-125">Форматы выходных данных</span><span class="sxs-lookup"><span data-stu-id="dca92-125">Output Formats</span></span>

<span data-ttu-id="dca92-126">В следующей таблице показаны Теги звукового формата, представляющие категории вывода, поддерживаемые кодировщиком Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="dca92-126">The following table shows the audio format tags that represent the output categories supported by the Windows Media Audio encoder.</span></span>



| <span data-ttu-id="dca92-127">Формат константы тега</span><span class="sxs-lookup"><span data-stu-id="dca92-127">Format tag constant</span></span>             | <span data-ttu-id="dca92-128">Формат значения тега</span><span class="sxs-lookup"><span data-stu-id="dca92-128">Format tag value</span></span> | <span data-ttu-id="dca92-129">Формат аудио</span><span class="sxs-lookup"><span data-stu-id="dca92-129">Audio format</span></span>                     |
|---------------------------------|------------------|----------------------------------|
| <span data-ttu-id="dca92-130">\_Формат волны \_ WMAUDIO2</span><span class="sxs-lookup"><span data-stu-id="dca92-130">WAVE\_FORMAT\_WMAUDIO2</span></span>          | <span data-ttu-id="dca92-131">0x0161</span><span class="sxs-lookup"><span data-stu-id="dca92-131">0x0161</span></span>           | <span data-ttu-id="dca92-132">Windows Media Audio Standard</span><span class="sxs-lookup"><span data-stu-id="dca92-132">Windows Media Audio Standard</span></span>     |
| <span data-ttu-id="dca92-133">\_Формат волны \_ WMAUDIO3</span><span class="sxs-lookup"><span data-stu-id="dca92-133">WAVE\_FORMAT\_WMAUDIO3</span></span>          | <span data-ttu-id="dca92-134">0x0162</span><span class="sxs-lookup"><span data-stu-id="dca92-134">0x0162</span></span>           | <span data-ttu-id="dca92-135">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="dca92-135">Windows Media Audio Professional</span></span> |
| <span data-ttu-id="dca92-136">\_Формат Wave \_ вмаудио \_ без потерь</span><span class="sxs-lookup"><span data-stu-id="dca92-136">WAVE\_FORMAT\_WMAUDIO\_LOSSLESS</span></span> | <span data-ttu-id="dca92-137">0x0163</span><span class="sxs-lookup"><span data-stu-id="dca92-137">0x0163</span></span>           | <span data-ttu-id="dca92-138">Windows Media Audio без потерь</span><span class="sxs-lookup"><span data-stu-id="dca92-138">Windows Media Audio Lossless</span></span>     |



 

## <a name="interfaces"></a><span data-ttu-id="dca92-139">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="dca92-139">Interfaces</span></span>

<span data-ttu-id="dca92-140">Объект audio ендодер предоставляет интерфейс **имедиаобжект** , чтобы объект можно было использовать в качестве объекта мультимедиа DirectX (DMO), и он предоставляет интерфейс **имфтрансформ** , чтобы объект можно было использовать в качестве Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="dca92-140">An audio endoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="dca92-141">Кодировщик Windows Media Audio работает как DMO или MFT в зависимости от того, какие интерфейсы получены и какая версия Windows работает.</span><span class="sxs-lookup"><span data-stu-id="dca92-141">A Windows Media Audio encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="dca92-142">В следующей таблице показаны условия, при которых звуковый кодировщик ведет себя как DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="dca92-142">The following table shows the conditions under which an audio encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="dca92-143">Операционная система</span><span class="sxs-lookup"><span data-stu-id="dca92-143">Operating system</span></span> | <span data-ttu-id="dca92-144">Поведение кодировщика</span><span class="sxs-lookup"><span data-stu-id="dca92-144">Encoder behavior</span></span>                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dca92-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dca92-145">Windows XP</span></span>       | <span data-ttu-id="dca92-146">Кодировщик Windows Media Audio всегда ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="dca92-146">A Windows Media Audio encoder always behaves as a DMO.</span></span>                                                                                                                                |
| <span data-ttu-id="dca92-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dca92-147">Windows Vista</span></span>    | <span data-ttu-id="dca92-148">По умолчанию кодировщик Windows Media Audio ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="dca92-148">By default, a Windows Media Audio encoder behaves as a DMO.</span></span> <span data-ttu-id="dca92-149">Если вы получаете интерфейс **имфтрансформ** или интерфейс **ипропертисторе** в звуковом кодировщике, он ведет себя как MFT.</span><span class="sxs-lookup"><span data-stu-id="dca92-149">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on an audio encoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="dca92-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dca92-150">Windows 7</span></span>        | <span data-ttu-id="dca92-151">По умолчанию кодировщик Windows Media Audio ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="dca92-151">By default, a Windows Media Audio encoder behaves as a DMO.</span></span> <span data-ttu-id="dca92-152">Если вы получаете интерфейс **имфтрансформ** в звуковом кодировщике, он ведет себя как MFT.</span><span class="sxs-lookup"><span data-stu-id="dca92-152">If you obtain an **IMFTransform** interface on an audio encoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="encoder-properties"></a><span data-ttu-id="dca92-153">Свойства кодировщика</span><span class="sxs-lookup"><span data-stu-id="dca92-153">Encoder Properties</span></span>

<span data-ttu-id="dca92-154">Кодировщик Windows Media Audio поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dca92-154">The Windows Media Audio encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dca92-155">Свойство</span><span class="sxs-lookup"><span data-stu-id="dca92-155">Property</span></span></th>
<th><span data-ttu-id="dca92-156">Описание</span><span class="sxs-lookup"><span data-stu-id="dca92-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dca92-157"><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-157"><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></span></span></td>
<td><span data-ttu-id="dca92-158">Указывает, использует ли кодировщик среднее-управляемое кодирование VBR.</span><span class="sxs-lookup"><span data-stu-id="dca92-158">Specifies whether the encoder uses average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="dca92-159">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-160">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-160">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-161">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-161">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-162"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-162"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="dca92-163">Указывает окно буфера (в миллисекундах) для потока с переменным числом переменных с переменной скоростью (VBR) с пиковой скоростью.</span><span class="sxs-lookup"><span data-stu-id="dca92-163">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate.</span></span><br/> <dl> <span data-ttu-id="dca92-164">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-164">Windows XP and later.</span></span><br />
<span data-ttu-id="dca92-165">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="dca92-165">Standard, Professional.</span></span><br />
<span data-ttu-id="dca92-166">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-166">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-167"><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-167"><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></span></span></td>
<td><span data-ttu-id="dca92-168">Указывает, должен ли кодировщик проверять согласованность данных между проходами при выполнении двусторонней кодировки VBR.</span><span class="sxs-lookup"><span data-stu-id="dca92-168">Specifies whether whether the encoder should check for data consistency across passes when performing two-pass VBR encoding.</span></span> <br/> <dl> <span data-ttu-id="dca92-169">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-169">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-170">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-170">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-171">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dca92-171">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-172"><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-172"><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></span></span></td>
<td><span data-ttu-id="dca92-173">Указывает, ограничивается ли кодировщик максимальным требованием к задержке декодера.</span><span class="sxs-lookup"><span data-stu-id="dca92-173">Specifies whether the encoder is constrained by a maximum decoder latency requirement.</span></span><br/> <dl> <span data-ttu-id="dca92-174">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-174">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-175">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-175">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-176">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-176">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-177"><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-177"><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="dca92-178">Указывает, ограничена ли сложность алгоритма кодирования.</span><span class="sxs-lookup"><span data-stu-id="dca92-178">Specifies whether the complexity of the encoding algorithm is constrained.</span></span><br/> <dl> <span data-ttu-id="dca92-179">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-179">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-180">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-180">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-181">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-181">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-182"><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-182"><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></span></span></td>
<td><span data-ttu-id="dca92-183">Указывает, ограничивается ли кодировщик максимальным требованием к задержке.</span><span class="sxs-lookup"><span data-stu-id="dca92-183">Specifies whether the encoder is constrained by a maximum latency requirement.</span></span><br/> <dl> <span data-ttu-id="dca92-184">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-184">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-185">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-185">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-186">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-186">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-187"><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-187"><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="dca92-188">Указывает, ограничены ли режимы, перечисленные кодировщиком, теми, которые соответствуют требованиям к качеству.</span><span class="sxs-lookup"><span data-stu-id="dca92-188">Specifies whether modes enumerated by the encoder are limited to those that meet a quality requirement.</span></span><br/> <dl> <span data-ttu-id="dca92-189">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-189">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-190">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-190">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-191">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-191">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-192"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-192"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="dca92-193">Указывает профиль сложности закодированного содержимого.</span><span class="sxs-lookup"><span data-stu-id="dca92-193">Specifies the complexity profile of the encoded content.</span></span><br/> <dl> <span data-ttu-id="dca92-194">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-194">Windows XP and later.</span></span><br />
<span data-ttu-id="dca92-195">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-195">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-196">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dca92-196">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-197"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-197"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="dca92-198">Задает требуемый уровень качества для кодирования VBR.</span><span class="sxs-lookup"><span data-stu-id="dca92-198">Specifies the desired quality level for VBR encoding.</span></span><br/> <dl> <span data-ttu-id="dca92-199">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-199">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-200">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-200">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-201">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="dca92-201">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-202"><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-202"><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></span></span></td>
<td><span data-ttu-id="dca92-203">Указывает, использует ли кодировщик подстановку шума.</span><span class="sxs-lookup"><span data-stu-id="dca92-203">Specifies whether the encoder uses noise substitution.</span></span><br/> <dl> <span data-ttu-id="dca92-204">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-204">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-205">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-205">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-206">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-206">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-207"><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-207"><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></span></span></td>
<td><span data-ttu-id="dca92-208">Указывает, использует ли кодировщик ограничение диапазона PCM.</span><span class="sxs-lookup"><span data-stu-id="dca92-208">Specifies whether the encoder uses PCM range limiting.</span></span><br/> <dl> <span data-ttu-id="dca92-209">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-209">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-210">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-210">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-211">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-211">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-212"><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-212"><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></span></span></td>
<td><span data-ttu-id="dca92-213">Указывает максимальную закодированную пропускную способность, допустимую при усечении полосы пропускания в кодировщике.</span><span class="sxs-lookup"><span data-stu-id="dca92-213">Specifies the maximum coded bandwidth allowed by band truncation in the encoder.</span></span><br/> <dl> <span data-ttu-id="dca92-214">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-214">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-215">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-215">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-216">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-216">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-217"><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-217"><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></span></span></td>
<td><span data-ttu-id="dca92-218">Указывает минимальную закодированную пропускную способность, допустимую при усечении полосы пропускания в кодировщике.</span><span class="sxs-lookup"><span data-stu-id="dca92-218">Specifies the minimum coded bandwidth allowed by band truncation in the encoder.</span></span><br/> <dl> <span data-ttu-id="dca92-219">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-219">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-220">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-220">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-221">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-221">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-222"><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-222"><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></span></span></td>
<td><span data-ttu-id="dca92-223">Определяет качество, при котором разрешена Минимальная пропускная способность.</span><span class="sxs-lookup"><span data-stu-id="dca92-223">Specifies the quality at which minimum coded bandwidth is allowed.</span></span> <br/> <dl> <span data-ttu-id="dca92-224">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-224">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-225">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-225">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-226">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-226">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-227"><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-227"><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></span></span></td>
<td><span data-ttu-id="dca92-228">Определяет качество, при котором разрешена максимальная пропускная способность.</span><span class="sxs-lookup"><span data-stu-id="dca92-228">Specifies the quality at which maximum coded bandwidth is allowed.</span></span><br/> <dl> <span data-ttu-id="dca92-229">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-229">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-230">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-230">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-231">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-231">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-232"><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-232"><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></span></span></td>
<td><span data-ttu-id="dca92-233">Указывает, выполняет ли кодировщик чередование усечения.</span><span class="sxs-lookup"><span data-stu-id="dca92-233">Specifies whether the encoder performs band truncation.</span></span><br/> <dl> <span data-ttu-id="dca92-234">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-234">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-235">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-235">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-236">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-236">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-237"><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-237"><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></span></span></td>
<td><span data-ttu-id="dca92-238">Указывает, использует ли кодировщик стиль вычисления маски, выполняемый в версии 7 кодировщика Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="dca92-238">Specifies whether the encoder uses the style of mask computation performed by version 7 of the Windows Media Audio encoder.</span></span><br/> <dl> <span data-ttu-id="dca92-239">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-239">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-240">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-240">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-241">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-241">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-242"><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-242"><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></span></span></td>
<td><span data-ttu-id="dca92-243">Указывает, выполняет ли кодировщик обработку стерео изображений.</span><span class="sxs-lookup"><span data-stu-id="dca92-243">Specifies whether the encoder performs stereo image processing.</span></span> <br/> <dl> <span data-ttu-id="dca92-244">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-244">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-245">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-245">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-246">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-246">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-247"><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-247"><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="dca92-248">Указывает окно буфера (в миллисекундах) для кодировщика, который настроен для использования среднего управляемого кодирования VBR.</span><span class="sxs-lookup"><span data-stu-id="dca92-248">Specifies the buffer window, in milliseconds, for an encoder that is configured to use average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="dca92-249">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-249">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-250">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-250">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-251">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-251">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-252"><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-252"><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="dca92-253">Указывает среднюю скорость потока в битах в секунду для кодировщика, который настроен для использования среднего управляемого кодирования VBR.</span><span class="sxs-lookup"><span data-stu-id="dca92-253">Specifies the average bit rate, in bits per second, for an encoder that is configured to use average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="dca92-254">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-254">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-255">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-255">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-256">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-256">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-257"><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-257"><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="dca92-258">Указывает сложность алгоритма кодирования.</span><span class="sxs-lookup"><span data-stu-id="dca92-258">Specifies the complexity of the encoding algorithm.</span></span><br/> <dl> <span data-ttu-id="dca92-259">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-259">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-260">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-260">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-261">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-261">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-262"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-262"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="dca92-263">Задает конец прохода кодирования.</span><span class="sxs-lookup"><span data-stu-id="dca92-263">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="dca92-264">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-264">Windows XP and later.</span></span><br />
<span data-ttu-id="dca92-265">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="dca92-265">Standard, Professional.</span></span><br />
<span data-ttu-id="dca92-266">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="dca92-266">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-267"><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-267"><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></span></span></td>
<td><span data-ttu-id="dca92-268">Указывает, использует ли основной кодировщик &quot; функцию «плюс» &quot; .</span><span class="sxs-lookup"><span data-stu-id="dca92-268">Specifies whether the core encoder uses the &quot;Plus&quot; feature.</span></span><br/> <dl> <span data-ttu-id="dca92-269">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-269">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-270">Professional.</span><span class="sxs-lookup"><span data-stu-id="dca92-270">Professional.</span></span><br />
<span data-ttu-id="dca92-271">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-271">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-272"><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-272"><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></span></span></td>
<td><span data-ttu-id="dca92-273">Указывает максимальную задержку для декодера в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="dca92-273">Specifies the maximum latency for the decoder, in milliseconds.</span></span><br/> <dl> <span data-ttu-id="dca92-274">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-274">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-275">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-275">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-276">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="dca92-276">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-277"><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-277"><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></span></span></td>
<td><span data-ttu-id="dca92-278">Указывает максимальную задержку кодировщика в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="dca92-278">Specifies the maximum latency for the encoder, in milliseconds.</span></span><br/> <dl> <span data-ttu-id="dca92-279">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-279">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-280">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-280">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-281">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="dca92-281">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-282"><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-282"><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="dca92-283">Задает уровень качества VBR последнего перечислимого типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="dca92-283">Specifies the VBR quality level of the most recently enumerated output type.</span></span><br/> <dl> <span data-ttu-id="dca92-284">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-284">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-285">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-285">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-286">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dca92-286">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-287"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-287"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="dca92-288">Указывает максимальное число проходов, поддерживаемое кодировщиком.</span><span class="sxs-lookup"><span data-stu-id="dca92-288">Specifies the maximum number of passes supported by the encoder.</span></span><br/> <dl> <span data-ttu-id="dca92-289">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-289">Windows XP and later.</span></span><br />
<span data-ttu-id="dca92-290">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-290">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-291">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dca92-291">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-292"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-292"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="dca92-293">Указывает число проходов, которые кодировщик будет использовать для кодирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="dca92-293">Specifies the number of passes that the encoder will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="dca92-294">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-294">Windows XP and later.</span></span><br />
<span data-ttu-id="dca92-295">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-295">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-296">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-296">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-297"><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-297"><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></span></span></td>
<td><span data-ttu-id="dca92-298">Указывает, ограничивается ли скорость кодировщика пиковым битом.</span><span class="sxs-lookup"><span data-stu-id="dca92-298">Specifies whether the encoder is constrained by a peak bit rate.</span></span><br/> <dl> <span data-ttu-id="dca92-299">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-299">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-300">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="dca92-300">Standard, Professional.</span></span><br />
<span data-ttu-id="dca92-301">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-301">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-302"><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-302"><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></span></span></td>
<td><span data-ttu-id="dca92-303">Указывает предпочтительное количество выборок на кадр.</span><span class="sxs-lookup"><span data-stu-id="dca92-303">Specifies the preferred number of samples per frame.</span></span><br/> <dl> <span data-ttu-id="dca92-304">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-304">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-305">Professional.</span><span class="sxs-lookup"><span data-stu-id="dca92-305">Professional.</span></span><br />
<span data-ttu-id="dca92-306">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-306">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-307"><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-307"><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></span></span></td>
<td><span data-ttu-id="dca92-308">Указывает, должен ли кодировщик использовать предпочтительный размер кадра.</span><span class="sxs-lookup"><span data-stu-id="dca92-308">Specifies whether the encoder should use a preferred frame size.</span></span><br/> <dl> <span data-ttu-id="dca92-309">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-309">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-310">Professional.</span><span class="sxs-lookup"><span data-stu-id="dca92-310">Professional.</span></span><br />
<span data-ttu-id="dca92-311">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-311">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-312"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-312"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="dca92-313">Указывает пиковую скорость потока (в битах в секунду), используемую для ограниченного 2-прохода с переменной скоростью (VBR).</span><span class="sxs-lookup"><span data-stu-id="dca92-313">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) encoding.</span></span> <br/> <dl> <span data-ttu-id="dca92-314">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-314">Windows XP and later.</span></span><br />
<span data-ttu-id="dca92-315">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="dca92-315">Standard, Professional.</span></span><br />
<span data-ttu-id="dca92-316">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-316">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-317"><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-317"><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="dca92-318">Указывает среднее окно буфера (в миллисекундах) закодированного потока.</span><span class="sxs-lookup"><span data-stu-id="dca92-318">Specifies the average buffer window, in milliseconds, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="dca92-319">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-319">Windows XP and later.</span></span><br />
<span data-ttu-id="dca92-320">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-320">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-321">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dca92-321">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-322"><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-322"><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="dca92-323">Указывает максимальное окно буфера (в миллисекундах) закодированного потока.</span><span class="sxs-lookup"><span data-stu-id="dca92-323">Specifies the maximum buffer window, in milliseconds, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="dca92-324">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-324">Windows XP and later.</span></span><br />
<span data-ttu-id="dca92-325">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-325">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-326">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dca92-326">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-327"><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-327"><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="dca92-328">Указывает среднюю скорость в битах в секунду для закодированного потока.</span><span class="sxs-lookup"><span data-stu-id="dca92-328">Specifies the average bit rate, in bits per second, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="dca92-329">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-329">Windows XP and later.</span></span><br />
<span data-ttu-id="dca92-330">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-330">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-331">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dca92-331">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-332"><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-332"><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="dca92-333">Указывает максимальную скорость в битах в секунду для закодированного потока.</span><span class="sxs-lookup"><span data-stu-id="dca92-333">Specifies the maximum bit rate, in bits per second, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="dca92-334">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-334">Windows XP and later.</span></span><br />
<span data-ttu-id="dca92-335">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-335">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-336">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dca92-336">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-337"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-337"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="dca92-338">Указывает, использует ли кодировщик кодирование VBR.</span><span class="sxs-lookup"><span data-stu-id="dca92-338">Specifies whether the encoder uses VBR encoding.</span></span><br/> <dl> <span data-ttu-id="dca92-339">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-339">Windows XP and later.</span></span><br />
<span data-ttu-id="dca92-340">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-340">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-341">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-341">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-342"><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-342"><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></span></span></td>
<td><span data-ttu-id="dca92-343">В настоящее время это свойство не используется кодеком Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="dca92-343">This property is currently not used by the Windows Media Audio codec.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-344"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-344"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span></span></td>
<td><span data-ttu-id="dca92-345">Указывает средний уровень громкости звукового содержимого.</span><span class="sxs-lookup"><span data-stu-id="dca92-345">Specifies the average volume level of audio content.</span></span><br/> <dl> <span data-ttu-id="dca92-346">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-346">Windows XP and later.</span></span><br />
<span data-ttu-id="dca92-347">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-347">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-348">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dca92-348">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-349"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-349"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span></span></td>
<td><span data-ttu-id="dca92-350">Указывает самый высокий уровень громкости в аудио содержимом.</span><span class="sxs-lookup"><span data-stu-id="dca92-350">Specifies the highest volume level occurring in audio content.</span></span><br/> <dl> <span data-ttu-id="dca92-351">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-351">Windows XP and later.</span></span><br />
<span data-ttu-id="dca92-352">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-352">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-353">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dca92-353">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-354"><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-354"><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></span></span></td>
<td><span data-ttu-id="dca92-355">Указывает среднее число байтов в секунду для звука с кодировкой VBR.</span><span class="sxs-lookup"><span data-stu-id="dca92-355">Specifies the average bytes per second for VBR encoded audio.</span></span><br/> <dl> <span data-ttu-id="dca92-356">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-356">Windows XP and later.</span></span><br />
<span data-ttu-id="dca92-357">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-357">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-358">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dca92-358">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-359"><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-359"><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></span></span></td>
<td><span data-ttu-id="dca92-360">Указывает, должен ли кодировщик создавать 1 пакет WMA на кадр.</span><span class="sxs-lookup"><span data-stu-id="dca92-360">Specifies whether the encoder should produce 1 WMA packet per frame.</span></span><br/> <dl> <span data-ttu-id="dca92-361">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-361">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-362">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-362">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-363">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-363">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-364"><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-364"><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></span></span></td>
<td><span data-ttu-id="dca92-365">Указывает, должен ли кодировщик создавать динамические параметры управления диапазоном.</span><span class="sxs-lookup"><span data-stu-id="dca92-365">Specifies whether the encoder should generate dynamic range control parameters.</span></span><br/> <dl> <span data-ttu-id="dca92-366">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-366">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-367">Standard, Professional, без потерь.</span><span class="sxs-lookup"><span data-stu-id="dca92-367">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="dca92-368">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-368">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dca92-369"><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-369"><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></span></span></td>
<td><span data-ttu-id="dca92-370">Указывает структуру <strong>вавеформатекс</strong> , описывающую входное звуковое содержимое.</span><span class="sxs-lookup"><span data-stu-id="dca92-370">Specifies the <strong>WAVEFORMATEX</strong> structure describing the input audio content.</span></span><br/> <dl> <span data-ttu-id="dca92-371">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-371">Windows XP and later.</span></span><br />
<span data-ttu-id="dca92-372">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="dca92-372">Standard, Professional.</span></span><br />
<span data-ttu-id="dca92-373">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-373">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dca92-374"><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></span><span class="sxs-lookup"><span data-stu-id="dca92-374"><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></span></span></td>
<td><span data-ttu-id="dca92-375">Указывает, должен ли кодировщик включать кодирование S/PDIF в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="dca92-375">Specifies whether the encoder should enable real-time S/PDIF encoding .</span></span><br/> <dl> <span data-ttu-id="dca92-376">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="dca92-376">Windows Vista and later.</span></span><br />
<span data-ttu-id="dca92-377">Professional.</span><span class="sxs-lookup"><span data-stu-id="dca92-377">Professional.</span></span><br />
<span data-ttu-id="dca92-378">Read/write.</span><span class="sxs-lookup"><span data-stu-id="dca92-378">Read/write.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="dca92-379">Требования</span><span class="sxs-lookup"><span data-stu-id="dca92-379">Requirements</span></span>



| <span data-ttu-id="dca92-380">Требование</span><span class="sxs-lookup"><span data-stu-id="dca92-380">Requirement</span></span> | <span data-ttu-id="dca92-381">Значение</span><span class="sxs-lookup"><span data-stu-id="dca92-381">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dca92-382">Клиент</span><span class="sxs-lookup"><span data-stu-id="dca92-382">Client</span></span><br/> | <span data-ttu-id="dca92-383">Windows XP, Windows Vista или Windows 7</span><span class="sxs-lookup"><span data-stu-id="dca92-383">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="dca92-384">Header</span><span class="sxs-lookup"><span data-stu-id="dca92-384">Header</span></span><br/> | <dl> <span data-ttu-id="dca92-385"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="dca92-385"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="dca92-386">DLL</span><span class="sxs-lookup"><span data-stu-id="dca92-386">DLL</span></span><br/>    | <dl> <span data-ttu-id="dca92-387"><dt>Wmadmoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dca92-387"><dt>Wmadmoe.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="dca92-388">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dca92-388">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dca92-389">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="dca92-389">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="dca92-390">Реализация кодека</span><span class="sxs-lookup"><span data-stu-id="dca92-390">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 




