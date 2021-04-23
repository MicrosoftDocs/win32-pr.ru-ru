---
description: Microsoft MPEG Audio декодер — это синхронное Media Foundation преобразование (MFT), позволяющее декодировать простые форматы потока MPEG с помощью конвейера Media Foundation (MF).
ms.assetid: 29A0491D-CA0D-4909-96F0-5640D5EE77F9
title: Декодер MPEG Audio
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98106ce4610c7c89a5e6212c225fd8eca3e4526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991422"
---
# <a name="mpeg-audio-decoder"></a><span data-ttu-id="ba416-103">Декодер MPEG Audio</span><span class="sxs-lookup"><span data-stu-id="ba416-103">MPEG Audio Decoder</span></span>

<span data-ttu-id="ba416-104">Microsoft MPEG Audio декодер — это синхронное [Media Foundation преобразование](media-foundation-transforms.md) (MFT), позволяющее декодировать простые форматы потока MPEG с помощью конвейера Media Foundation (MF).</span><span class="sxs-lookup"><span data-stu-id="ba416-104">The Microsoft MPEG Audio Decoder is a synchronous [Media Foundation Transform](media-foundation-transforms.md) (MFT) that enables decoding MPEG audio elementary stream formats using the Media Foundation (MF) pipeline.</span></span>

<span data-ttu-id="ba416-105">Декодер поддерживает следующие простые форматы потока MPEG.</span><span class="sxs-lookup"><span data-stu-id="ba416-105">The decoder supports the following MPEG elementary stream formats.</span></span>

-   <span data-ttu-id="ba416-106">Звуковые слои MPEG-1 I и II (ISO/IEC 11172-3).</span><span class="sxs-lookup"><span data-stu-id="ba416-106">MPEG-1 audio layers I and II (ISO/IEC 11172-3).</span></span> <span data-ttu-id="ba416-107">2.</span><span class="sxs-lookup"><span data-stu-id="ba416-107">2.</span></span> <span data-ttu-id="ba416-108">Обратная совместимость MPEG-2, слои I и II (ISO</span><span class="sxs-lookup"><span data-stu-id="ba416-108">MPEG-2 backward-compatible, layers I and II (ISO</span></span>

-   <span data-ttu-id="ba416-109">Обратная совместимость MPEG-2, слои I и II (ISO/IEC 13818-3), моно и стерео</span><span class="sxs-lookup"><span data-stu-id="ba416-109">MPEG-2 backward-compatible, layers I and II (ISO/IEC 13818-3), mono and stereo only</span></span>

## <a name="class-identifier"></a><span data-ttu-id="ba416-110">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="ba416-110">Class Identifier</span></span>

<span data-ttu-id="ba416-111">Идентификатором класса (CLSID) декодера MPEG является **CLSID \_ мсмпегауддекмфт**, определенный в файле заголовка вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="ba416-111">The class identifier (CLSID) of the MPEG Audio decoder is **CLSID\_MSMPEGAudDecMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="input-media-types"></a><span data-ttu-id="ba416-112">Типы входных носителей</span><span class="sxs-lookup"><span data-stu-id="ba416-112">Input Media Types</span></span>

<span data-ttu-id="ba416-113">Декодер MPEG поддерживает следующие атрибуты входного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="ba416-113">The MPEG Audio decoder supports the following input media type attributes.</span></span>



| <span data-ttu-id="ba416-114">attribute</span><span class="sxs-lookup"><span data-stu-id="ba416-114">Attribute</span></span>                                                                               | <span data-ttu-id="ba416-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ba416-115">Value</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba416-116">**\_ \_ основной тип MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="ba416-116">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="ba416-117">**Мфмедиатипе \_ аудио**</span><span class="sxs-lookup"><span data-stu-id="ba416-117">**MFMediaType\_Audio**</span></span>                                                                                                                                                                                                                                                |
| [<span data-ttu-id="ba416-118">**подтип MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="ba416-118">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="ba416-119">**Мфаудиоформат \_ MPEG**</span><span class="sxs-lookup"><span data-stu-id="ba416-119">**MFAudioFormat\_MPEG**</span></span>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="ba416-120">**\_ \_ каналы аудиосигнала MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ba416-120">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="ba416-121">Используемых Обычно 1 для Mono или 2 для стерео, но может иметь до 6 каналов.</span><span class="sxs-lookup"><span data-stu-id="ba416-121">(Optional) Usually 1 for mono or 2 for stereo, but can be up to 6 channels.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="ba416-122">**\_ \_ \_ Маска канала MF MT \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="ba416-122">**MF\_MT\_AUDIO\_CHANNEL\_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)              | <span data-ttu-id="ba416-123">Используемых Обычно 0x4 для Mono или 0x3 для стерео, но также может быть одной из масок каналов, связанных с до 6 каналов (3/2/1, 3/2, 3/1, 2/2, 2/1).</span><span class="sxs-lookup"><span data-stu-id="ba416-123">(Optional) Usually 0x4 for mono or 0x3 for stereo, but can also be any one of the channel masks associated with up to 6 channels (3/2/1, 3/2, 3/1, 2/2, 2/1).</span></span> <span data-ttu-id="ba416-124">При наличии маски канал должен соответствовать заданному входному числу каналов.</span><span class="sxs-lookup"><span data-stu-id="ba416-124">If present, the channel mask must be consistent with the specified input number of channels.</span></span><br/> |
| [<span data-ttu-id="ba416-125">**\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду**</span><span class="sxs-lookup"><span data-stu-id="ba416-125">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="ba416-126">Используемых Одно из следующих: 16000, 22050, 24000, 32000, 44100, 48000.</span><span class="sxs-lookup"><span data-stu-id="ba416-126">(Optional) One of the following: 16000, 22050, 24000, 32000, 44100, 48000.</span></span> <span data-ttu-id="ba416-127">Если задано значение, скорость выборки должна быть одной из допустимых частот выборки MPEG.</span><span class="sxs-lookup"><span data-stu-id="ba416-127">If specified, the input sampling rate must be one of the valid MPEG sampling rates.</span></span><br/>                                                                                             |



 

## <a name="output-media-types"></a><span data-ttu-id="ba416-128">Типы выходных данных мультимедиа</span><span class="sxs-lookup"><span data-stu-id="ba416-128">Output Media Types</span></span>

<span data-ttu-id="ba416-129">Декодер MPEG Audio будет поддерживать до четырех выходных подтипов носителей в следующем порядке.</span><span class="sxs-lookup"><span data-stu-id="ba416-129">The MPEG Audio decoder will support up to four output media subtypes, in the following order.</span></span>

<dl> 1. <span data-ttu-id="ba416-130">Стерео, с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="ba416-130">Stereo, floating point.</span></span>  
2. <span data-ttu-id="ba416-131">Стерео, 16-разрядный PCM.</span><span class="sxs-lookup"><span data-stu-id="ba416-131">Stereo, 16-bit PCM.</span></span>  
3. <span data-ttu-id="ba416-132">Моно, с плавающей запятой (только если входные данные — Mono или Dual-Mono).</span><span class="sxs-lookup"><span data-stu-id="ba416-132">Mono, floating point (only if the input is mono or dual-mono).</span></span>  
4. <span data-ttu-id="ba416-133">Моно, 16-разрядный PCM (только если входные данные — Mono или Dual-Mono).</span><span class="sxs-lookup"><span data-stu-id="ba416-133">Mono, 16-bit PCM (only if the input is mono or dual-mono).</span></span>  
</dl>

<span data-ttu-id="ba416-134">Декодер всегда поддерживает стерео вывод, и он передается в качестве первого выходного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="ba416-134">The decoder always supports stereo output and it is enumerated as the first output media type.</span></span>

<span data-ttu-id="ba416-135">Декодер поддерживает следующие атрибуты типа выходных данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ba416-135">The decoder supports the following output media type attributes.</span></span>



| <span data-ttu-id="ba416-136">attribute</span><span class="sxs-lookup"><span data-stu-id="ba416-136">Attribute</span></span>                                                                           | <span data-ttu-id="ba416-137">Значение</span><span class="sxs-lookup"><span data-stu-id="ba416-137">Value</span></span>                                                                      |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="ba416-138">\_ \_ основной тип MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="ba416-138">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="ba416-139">**Мфмедиатипе \_ аудио**</span><span class="sxs-lookup"><span data-stu-id="ba416-139">**MFMediaType\_Audio**</span></span>                                                     |
| [<span data-ttu-id="ba416-140">подтип MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="ba416-140">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="ba416-141">Либо **мфаудиоформат \_ PCM** , либо **мфаудиоформат \_ float**</span><span class="sxs-lookup"><span data-stu-id="ba416-141">Either **MFAudioFormat\_PCM** or **MFAudioFormat\_Float**</span></span>                  |
| [<span data-ttu-id="ba416-142">\_ \_ звуковый бит MF MT \_ \_ на \_ выборку</span><span class="sxs-lookup"><span data-stu-id="ba416-142">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)       | <span data-ttu-id="ba416-143">16 или 32</span><span class="sxs-lookup"><span data-stu-id="ba416-143">16 or 32</span></span>                                                                   |
| [<span data-ttu-id="ba416-144">\_ \_ каналы аудиосигнала MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="ba416-144">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="ba416-145">1 или 2</span><span class="sxs-lookup"><span data-stu-id="ba416-145">1 or 2</span></span>                                                                     |
| [<span data-ttu-id="ba416-146">\_ \_ \_ Маска канала MF MT \_ Audio</span><span class="sxs-lookup"><span data-stu-id="ba416-146">MF\_MT\_AUDIO\_CHANNEL\_MASK</span></span>](mf-mt-audio-channel-mask-attribute.md)              | <span data-ttu-id="ba416-147">0x4 для Mono или 0x3 для стерео</span><span class="sxs-lookup"><span data-stu-id="ba416-147">0x4 for mono or 0x3 for stereo</span></span>                                             |
| [<span data-ttu-id="ba416-148">\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду</span><span class="sxs-lookup"><span data-stu-id="ba416-148">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="ba416-149">Одно из следующих: 16000, 22050, 24000, 32000, 44100, 48000.</span><span class="sxs-lookup"><span data-stu-id="ba416-149">One of the following: 16000, 22050, 24000, 32000, 44100, 48000.</span></span><br/> |



 

## <a name="transform-attributes"></a><span data-ttu-id="ba416-150">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="ba416-150">Transform Attributes</span></span>

<span data-ttu-id="ba416-151">Декодер MPEG Audio реализует метод [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="ba416-151">The MPEG Audio decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="ba416-152">Приложения могут использовать этот метод для получения или установки следующих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="ba416-152">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="ba416-153">attribute</span><span class="sxs-lookup"><span data-stu-id="ba416-153">Attribute</span></span>                                                                               | <span data-ttu-id="ba416-154">Описание</span><span class="sxs-lookup"><span data-stu-id="ba416-154">Description</span></span>                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba416-155">**КОДЕКАПИ \_ авдекаудиодуалмоно**</span><span class="sxs-lookup"><span data-stu-id="ba416-155">**CODECAPI\_AVDecAudioDualMono**</span></span>](../directshow/avdecaudiodualmono-property.md)                   | <span data-ttu-id="ba416-156">Указывает, является ли декодированным многоканальным аудиовыходом два моно или нет.</span><span class="sxs-lookup"><span data-stu-id="ba416-156">Specifies whether 2-channel audio being decoded is dual mono or not.</span></span> <span data-ttu-id="ba416-157">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ba416-157">Read-only.</span></span> <span data-ttu-id="ba416-158">Задается MFT.</span><span class="sxs-lookup"><span data-stu-id="ba416-158">Set by the MFT.</span></span> <span data-ttu-id="ba416-159">Дополнительные сведения см. в разделе [**еавдекаудиодуалмоно**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span><span class="sxs-lookup"><span data-stu-id="ba416-159">For more information see [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span></span>                                                                                                                               |
| [<span data-ttu-id="ba416-160">**КОДЕКАПИ \_ авдекаудиодуалмонорепромоде**</span><span class="sxs-lookup"><span data-stu-id="ba416-160">**CODECAPI\_AVDecAudioDualMonoReproMode**</span></span>](../directshow/avdecaudiodualmonorepromode-property.md) | <span data-ttu-id="ba416-161">Указывает, как декодер воспроизводит два моно аудио.</span><span class="sxs-lookup"><span data-stu-id="ba416-161">Specifies how the decoder reproduces dual mono audio.</span></span> <span data-ttu-id="ba416-162">По умолчанию используется значение **еавдекаудиодуалмонорепромоде \_ Left \_ Mono**.</span><span class="sxs-lookup"><span data-stu-id="ba416-162">The default value is **eAVDecAudioDualMonoReproMode\_LEFT\_MONO**.</span></span><br/> <span data-ttu-id="ba416-163">Чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="ba416-163">Read/Write.</span></span> <span data-ttu-id="ba416-164">Приложения могут установить это свойство, чтобы изменить поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ba416-164">Applications can set this property to change the default behavior.</span></span> <span data-ttu-id="ba416-165">Дополнительные сведения см. в разделе [**еавдекаудиодуалмоно**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span><span class="sxs-lookup"><span data-stu-id="ba416-165">For more information see [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span></span><br/> |
| [<span data-ttu-id="ba416-166">**КОДЕКАПИ \_ авенккоммонмеанбитрате**</span><span class="sxs-lookup"><span data-stu-id="ba416-166">**CODECAPI\_AVEncCommonMeanBitRate**</span></span>](../directshow/avenccommonmeanbitrate-property.md)           | <span data-ttu-id="ba416-167">Указывает скорость потока сжатых потоков.</span><span class="sxs-lookup"><span data-stu-id="ba416-167">Specifies the compressed stream bit rate.</span></span> <span data-ttu-id="ba416-168">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ba416-168">Read-only.</span></span> <span data-ttu-id="ba416-169">Задается MFT.</span><span class="sxs-lookup"><span data-stu-id="ba416-169">Set by the MFT.</span></span>                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="ba416-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba416-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba416-171">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="ba416-171">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
