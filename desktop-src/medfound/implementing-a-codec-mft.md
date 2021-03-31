---
description: В этом разделе приводятся некоторые рекомендации по реализации декодера или кодировщика в качестве Media Foundation преобразования (MFT).
ms.assetid: b15bda0a-0fdd-4601-975d-a71c47c974bf
title: Реализация MFT кодека
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4412db23747e9a6b3468e9e428120d099b2445ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272508"
---
# <a name="implementing-a-codec-mft"></a><span data-ttu-id="18a61-103">Реализация MFT кодека</span><span class="sxs-lookup"><span data-stu-id="18a61-103">Implementing a Codec MFT</span></span>

<span data-ttu-id="18a61-104">В этом разделе приводятся некоторые рекомендации по реализации декодера или кодировщика в качестве Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="18a61-104">This topic provides some guidelines for implementing a decoder or encoder as a Media Foundation Transform (MFT) .</span></span>

-   [<span data-ttu-id="18a61-105">Кодировщики</span><span class="sxs-lookup"><span data-stu-id="18a61-105">Encoders</span></span>](#encoders)
    -   [<span data-ttu-id="18a61-106">Согласование формата кодировщика</span><span class="sxs-lookup"><span data-stu-id="18a61-106">Encoder Format Negotiation</span></span>](#encoder-format-negotiation)
-   [<span data-ttu-id="18a61-107">Декодеров</span><span class="sxs-lookup"><span data-stu-id="18a61-107">Decoders</span></span>](#decoders)
    -   [<span data-ttu-id="18a61-108">Декодеры только для кодирования</span><span class="sxs-lookup"><span data-stu-id="18a61-108">Transcode-Only Decoders</span></span>](#transcode-only-decoders)
    -   [<span data-ttu-id="18a61-109">Атрибуты чересстрочности</span><span class="sxs-lookup"><span data-stu-id="18a61-109">Telecine Attributes</span></span>](#telecine-attributes)
-   [<span data-ttu-id="18a61-110">См. также</span><span class="sxs-lookup"><span data-stu-id="18a61-110">Related topics</span></span>](#related-topics)

## <a name="encoders"></a><span data-ttu-id="18a61-111">Кодировщики</span><span class="sxs-lookup"><span data-stu-id="18a61-111">Encoders</span></span>

### <a name="encoder-format-negotiation"></a><span data-ttu-id="18a61-112">Согласование формата кодировщика</span><span class="sxs-lookup"><span data-stu-id="18a61-112">Encoder Format Negotiation</span></span>

<span data-ttu-id="18a61-113">Для инициализации кодировщика используется следующая процедура:</span><span class="sxs-lookup"><span data-stu-id="18a61-113">The following procedure is used to initialize an encoder:</span></span>

1.  <span data-ttu-id="18a61-114">Запросите таблицу MFT для интерфейса [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="18a61-114">Query the MFT for the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>
2.  <span data-ttu-id="18a61-115">Вызовите метод [**икодекапи:: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) , чтобы задать свойства кодировки.</span><span class="sxs-lookup"><span data-stu-id="18a61-115">Call [**ICodecAPI::SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) to set encoding properties.</span></span>
3.  <span data-ttu-id="18a61-116">Вызовите метод [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , чтобы задать формат кодирования.</span><span class="sxs-lookup"><span data-stu-id="18a61-116">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the encoding format.</span></span>
4.  <span data-ttu-id="18a61-117">Вызовите метод [**имфтрансформ:: жетинпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) , чтобы получить список совместимых входных типов.</span><span class="sxs-lookup"><span data-stu-id="18a61-117">Call [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) to get a list of compatible input types.</span></span> <span data-ttu-id="18a61-118">(Этот шаг можно пропустить.)</span><span class="sxs-lookup"><span data-stu-id="18a61-118">(This step might be skipped.)</span></span>
5.  <span data-ttu-id="18a61-119">Вызовите метод [**имфтрансформ:: сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) , чтобы задать несжатый входной формат.</span><span class="sxs-lookup"><span data-stu-id="18a61-119">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the uncompressed input format.</span></span>

<span data-ttu-id="18a61-120">После того как тип выходных данных задан на шаге 3, метод [**жетинпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) должен возвращать список входных типов, совместимых с текущим типом выходных данных.</span><span class="sxs-lookup"><span data-stu-id="18a61-120">After the output type is set in step 3, the [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) method must return a list of input types that are compatible with the current output type.</span></span> <span data-ttu-id="18a61-121">Иными словами, все типы, возвращаемые функцией **жетинпутаваилаблетипе** в этой точке, должны быть допустимыми для [**сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span><span class="sxs-lookup"><span data-stu-id="18a61-121">In other words, any types returned by **GetInputAvailableType** at this point must be valid for [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span>

<span data-ttu-id="18a61-122">Для декодеров порядок, в котором устанавливаются типы, изменяется на обратный: сначала устанавливается тип входных данных, а затем тип выходных данных.</span><span class="sxs-lookup"><span data-stu-id="18a61-122">For decoders, the order in which types are set is reversed: The input type is set first, followed by the output type.</span></span> <span data-ttu-id="18a61-123">После установки входного типа метод [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) должен возвращать список типов, которые могут быть переданы в метод [**Имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) .</span><span class="sxs-lookup"><span data-stu-id="18a61-123">After the input type is set, the [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method must return a list of types that can be passed to the [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) method.</span></span>

<span data-ttu-id="18a61-124">Кодировщики и декодеры должны поддерживать NV12 как распространенный несжатый формат.</span><span class="sxs-lookup"><span data-stu-id="18a61-124">Encoders and decoders should support NV12 as a common uncompressed format.</span></span> <span data-ttu-id="18a61-125">Это гарантирует, что компоненты конвейера могут взаимодействовать с минимальными колорспаце преобразованиями.</span><span class="sxs-lookup"><span data-stu-id="18a61-125">This ensures that pipeline components can interoperate with minimal colorspace conversions.</span></span> <span data-ttu-id="18a61-126">Конечно же, также поддерживаются и другие форматы.</span><span class="sxs-lookup"><span data-stu-id="18a61-126">Of course, other formats can be supported as well.</span></span>

## <a name="decoders"></a><span data-ttu-id="18a61-127">Декодеров</span><span class="sxs-lookup"><span data-stu-id="18a61-127">Decoders</span></span>

### <a name="transcode-only-decoders"></a><span data-ttu-id="18a61-128">Transcode-Only декодеры</span><span class="sxs-lookup"><span data-stu-id="18a61-128">Transcode-Only Decoders</span></span>

<span data-ttu-id="18a61-129">Некоторые декодеры оптимизированы для перекодирования (декодирования и повторного кодирования потока) и не подходят для использования во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="18a61-129">Some decoders are optimized for transcoding (decoding and then re-encoding a stream) and are not suitable for use during playback.</span></span>

<span data-ttu-id="18a61-130">Если таблица MFT декодера предназначена только для перекодировки, установите **флаг \_ перечисления MFT Enum \_ \_ \_ только** при регистрации MFT.</span><span class="sxs-lookup"><span data-stu-id="18a61-130">If a decoder MFT is intended only for transcoding, set the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag when you register the MFT.</span></span> <span data-ttu-id="18a61-131">(См. [**мфтрегистер**](/windows/desktop/api/mfapi/nf-mfapi-mftregister).)</span><span class="sxs-lookup"><span data-stu-id="18a61-131">(See [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister).)</span></span>

<span data-ttu-id="18a61-132">По умолчанию декодированные декодеры не возвращаются функцией [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="18a61-132">By default, transcode decoders are not returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span> <span data-ttu-id="18a61-133">Чтобы перечислить декодеры перекодировки, вызовите **мфтенумекс** и установите флаг перечисления MFT "флаг" **\_ \_ \_ \_ только** в параметре *flags* .</span><span class="sxs-lookup"><span data-stu-id="18a61-133">To enumerate transcode decoders, call **MFTEnumEx** and set the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag in *Flags* parameter.</span></span> <span data-ttu-id="18a61-134">При использовании в функции **мфтенумекс** этот флаг перечисляет как декодеры кодирования, так и другие декодеры.</span><span class="sxs-lookup"><span data-stu-id="18a61-134">When used in the **MFTEnumEx** function, this flag enumerated both transcode decoders and other decoders.</span></span>



| <span data-ttu-id="18a61-135">**\_ Перечисление \_ флагов \_ \_ перечисления MFT** мфтрегистер</span><span class="sxs-lookup"><span data-stu-id="18a61-135">MFTRegister **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY**</span></span> | <span data-ttu-id="18a61-136">**\_ Перечисление \_ флагов \_ \_ перечисления MFT** мфтенумекс</span><span class="sxs-lookup"><span data-stu-id="18a61-136">MFTEnumEx **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY**</span></span> | <span data-ttu-id="18a61-137">Перечислен ли MFT?</span><span class="sxs-lookup"><span data-stu-id="18a61-137">Is MFT Enumerated?</span></span> |
|--------------------------------------------------|------------------------------------------------|--------------------|
| <span data-ttu-id="18a61-138">1</span><span class="sxs-lookup"><span data-stu-id="18a61-138">1</span></span>                                                | <span data-ttu-id="18a61-139">1</span><span class="sxs-lookup"><span data-stu-id="18a61-139">1</span></span>                                              | <span data-ttu-id="18a61-140">Да</span><span class="sxs-lookup"><span data-stu-id="18a61-140">Yes</span></span>                |
| <span data-ttu-id="18a61-141">1</span><span class="sxs-lookup"><span data-stu-id="18a61-141">1</span></span>                                                | <span data-ttu-id="18a61-142">0</span><span class="sxs-lookup"><span data-stu-id="18a61-142">0</span></span>                                              | <span data-ttu-id="18a61-143">Нет</span><span class="sxs-lookup"><span data-stu-id="18a61-143">No</span></span>                 |
| <span data-ttu-id="18a61-144">0</span><span class="sxs-lookup"><span data-stu-id="18a61-144">0</span></span>                                                | <span data-ttu-id="18a61-145">1</span><span class="sxs-lookup"><span data-stu-id="18a61-145">1</span></span>                                              | <span data-ttu-id="18a61-146">Да</span><span class="sxs-lookup"><span data-stu-id="18a61-146">Yes</span></span>                |
| <span data-ttu-id="18a61-147">0</span><span class="sxs-lookup"><span data-stu-id="18a61-147">0</span></span>                                                | <span data-ttu-id="18a61-148">0</span><span class="sxs-lookup"><span data-stu-id="18a61-148">0</span></span>                                              | <span data-ttu-id="18a61-149">Да</span><span class="sxs-lookup"><span data-stu-id="18a61-149">Yes</span></span>                |



 

### <a name="telecine-attributes"></a><span data-ttu-id="18a61-150">Атрибуты чересстрочности</span><span class="sxs-lookup"><span data-stu-id="18a61-150">Telecine Attributes</span></span>

<span data-ttu-id="18a61-151">Источник мультимедиа может присоединить следующие атрибуты чересстрочности к примерам мультимедиа, которые он доставляет.</span><span class="sxs-lookup"><span data-stu-id="18a61-151">The media source might attach the following telecine attributes to the media samples that it delivers.</span></span>



| <span data-ttu-id="18a61-152">attribute</span><span class="sxs-lookup"><span data-stu-id="18a61-152">Attribute</span></span>                                                                                   | <span data-ttu-id="18a61-153">Описание</span><span class="sxs-lookup"><span data-stu-id="18a61-153">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="18a61-154">**Мфсампликстенсион \_ репеатфирстфиелд**</span><span class="sxs-lookup"><span data-stu-id="18a61-154">**MFSampleExtension\_RepeatFirstField**</span></span>](mfsampleextension-repeatfirstfield-attribute.md) | <span data-ttu-id="18a61-155">Эквивалентно флагу "повторить первое поле" (РФФ).</span><span class="sxs-lookup"><span data-stu-id="18a61-155">Equivalent to "repeat first field" (RFF) flag.</span></span> |
| [<span data-ttu-id="18a61-156">**Мфсампликстенсион \_ боттомфиелдфирст**</span><span class="sxs-lookup"><span data-stu-id="18a61-156">**MFSampleExtension\_BottomFieldFirst**</span></span>](mfsampleextension-bottomfieldfirst-attribute.md) | <span data-ttu-id="18a61-157">Обратный флаг "первое поле" (ТФФ).</span><span class="sxs-lookup"><span data-stu-id="18a61-157">Inverse of "top field first" (TFF) flag.</span></span>       |



 

<span data-ttu-id="18a61-158">Эти флаги предоставляют подсказку расширенному обработчику видео (Евр) при выполнении дечередования.</span><span class="sxs-lookup"><span data-stu-id="18a61-158">These flags provide a hint to the enhanced video renderer (EVR) when it performs deinterlacing.</span></span> <span data-ttu-id="18a61-159">Декодер должен распространять эти флаги в нисходящем порядке, копируя их в выходные образцы, чтобы они достигли Евр.</span><span class="sxs-lookup"><span data-stu-id="18a61-159">A decoder should propagate these flags downstream by copying them to the output samples, so that they reach the EVR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18a61-160">См. также</span><span class="sxs-lookup"><span data-stu-id="18a61-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18a61-161">Запись пользовательского MFT</span><span class="sxs-lookup"><span data-stu-id="18a61-161">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
