---
description: Типы несжатых видеоматериалов
ms.assetid: 50bf2947-27ee-4092-9d3a-a1c13ee80e95
title: Типы несжатых видеоматериалов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c90a48aed62f22a492ac22dae93761c1046750a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547343"
---
# <a name="uncompressed-video-media-types"></a><span data-ttu-id="88cf4-103">Типы несжатых видеоматериалов</span><span class="sxs-lookup"><span data-stu-id="88cf4-103">Uncompressed Video Media Types</span></span>

<span data-ttu-id="88cf4-104">В этом разделе описывается создание типа носителя, который описывает формат видео без сжатия.</span><span class="sxs-lookup"><span data-stu-id="88cf4-104">This topic describes how to create a media type that describes an uncompressed video format.</span></span> <span data-ttu-id="88cf4-105">Дополнительные сведения о типах мультимедиа см. в разделе [About Media Types](about-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="88cf4-105">For more information about media types generally, see [About Media Types](about-media-types.md).</span></span>

<span data-ttu-id="88cf4-106">Чтобы создать полный несжатый тип видео, задайте следующие атрибуты в указателе интерфейса [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="88cf4-106">To create a complete uncompressed video type, set the following attributes on the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span>



| <span data-ttu-id="88cf4-107">attribute</span><span class="sxs-lookup"><span data-stu-id="88cf4-107">Attribute</span></span>                                                                            | <span data-ttu-id="88cf4-108">Описание</span><span class="sxs-lookup"><span data-stu-id="88cf4-108">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88cf4-109">**\_ \_ основной тип MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="88cf4-109">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                            | <span data-ttu-id="88cf4-110">Основной тип.</span><span class="sxs-lookup"><span data-stu-id="88cf4-110">Major type.</span></span> <span data-ttu-id="88cf4-111">Задайте значение **мфмедиатипе \_ Video**.</span><span class="sxs-lookup"><span data-stu-id="88cf4-111">Set to **MFMediaType\_Video**.</span></span>                                                                                                                                                                                          |
| [<span data-ttu-id="88cf4-112">**подтип MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="88cf4-112">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                   | <span data-ttu-id="88cf4-113">Подтип.</span><span class="sxs-lookup"><span data-stu-id="88cf4-113">Subtype.</span></span> <span data-ttu-id="88cf4-114">См. раздел [GUID подтипа видео](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="88cf4-114">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="88cf4-115">**MF \_ , \_ шаг по умолчанию \_**</span><span class="sxs-lookup"><span data-stu-id="88cf4-115">**MF\_MT\_DEFAULT\_STRIDE**</span></span>](mf-mt-default-stride-attribute.md)                    | <span data-ttu-id="88cf4-116">Шаг с поверхностью.</span><span class="sxs-lookup"><span data-stu-id="88cf4-116">Surface stride.</span></span> <span data-ttu-id="88cf4-117">*Шаг* — это число байтов, необходимое для перехода от одной строки пикселей к следующей.</span><span class="sxs-lookup"><span data-stu-id="88cf4-117">The *stride* is the number of bytes needed to go from one row of pixels to the next.</span></span> <span data-ttu-id="88cf4-118">Установите этот атрибут, если шаг в байтах не совпадает с шириной видео в байтах.</span><span class="sxs-lookup"><span data-stu-id="88cf4-118">Set this attribute if the stride in bytes is not the same as the video width in bytes.</span></span> <span data-ttu-id="88cf4-119">В противном случае этот атрибут можно опустить.</span><span class="sxs-lookup"><span data-stu-id="88cf4-119">Otherwise, you can omit this attribute.</span></span> |
| [<span data-ttu-id="88cf4-120">**\_ \_ Частота кадров MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="88cf4-120">**MF\_MT\_FRAME\_RATE**</span></span>](mf-mt-frame-rate-attribute.md)                            | <span data-ttu-id="88cf4-121">Частота кадров.</span><span class="sxs-lookup"><span data-stu-id="88cf4-121">Frame rate.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="88cf4-122">**\_ \_ Размер пакета MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="88cf4-122">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)                            | <span data-ttu-id="88cf4-123">Размер кадра.</span><span class="sxs-lookup"><span data-stu-id="88cf4-123">Frame size.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="88cf4-124">**\_ \_ режим чересстрочную РАЗВЕРТКи MF \_**</span><span class="sxs-lookup"><span data-stu-id="88cf4-124">**MF\_MT\_INTERLACE\_MODE**</span></span>](mf-mt-interlace-mode-attribute.md)                    | <span data-ttu-id="88cf4-125">Режим чередования.</span><span class="sxs-lookup"><span data-stu-id="88cf4-125">Interlacing mode.</span></span>                                                                                                                                                                                                                   |
| [<span data-ttu-id="88cf4-126">**MF \_ — \_ все \_ \_ независимые примеры**</span><span class="sxs-lookup"><span data-stu-id="88cf4-126">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) | <span data-ttu-id="88cf4-127">Указывает, является ли каждый выбор независимым.</span><span class="sxs-lookup"><span data-stu-id="88cf4-127">Specifies whether each sample is independent.</span></span> <span data-ttu-id="88cf4-128">Задайте значение **true** для несжатых форматов.</span><span class="sxs-lookup"><span data-stu-id="88cf4-128">Set to **TRUE** for uncompressed formats.</span></span>                                                                                                                                             |
| [<span data-ttu-id="88cf4-129">**пропорции MF \_ MT \_ пикселей \_ \_**</span><span class="sxs-lookup"><span data-stu-id="88cf4-129">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)           | <span data-ttu-id="88cf4-130">Пропорция в пикселях.</span><span class="sxs-lookup"><span data-stu-id="88cf4-130">Pixel aspect ratio.</span></span>                                                                                                                                                                                                                 |



 

<span data-ttu-id="88cf4-131">Кроме того, если вы знакомы с правильными значениями, задайте следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="88cf4-131">In addition, set the following attributes if you know the correct values.</span></span> <span data-ttu-id="88cf4-132">(В противном случае не указывайте эти атрибуты.)</span><span class="sxs-lookup"><span data-stu-id="88cf4-132">(Otherwise, omit these attributes.)</span></span>



| <span data-ttu-id="88cf4-133">attribute</span><span class="sxs-lookup"><span data-stu-id="88cf4-133">Attribute</span></span>                                                                    | <span data-ttu-id="88cf4-134">Описание</span><span class="sxs-lookup"><span data-stu-id="88cf4-134">Description</span></span>        |
|------------------------------------------------------------------------------|--------------------|
| [<span data-ttu-id="88cf4-135">**\_ \_ \_ первичные цвета видео MF MT**</span><span class="sxs-lookup"><span data-stu-id="88cf4-135">**MF\_MT\_VIDEO\_PRIMARIES**</span></span>](mf-mt-video-primaries-attribute.md)          | <span data-ttu-id="88cf4-136">Первичные цвета.</span><span class="sxs-lookup"><span data-stu-id="88cf4-136">Color primaries.</span></span>   |
| [<span data-ttu-id="88cf4-137">**\_ \_ функция перемещения MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="88cf4-137">**MF\_MT\_TRANSFER\_FUNCTION**</span></span>](mf-mt-transfer-function-attribute.md)      | <span data-ttu-id="88cf4-138">Функция перемещения.</span><span class="sxs-lookup"><span data-stu-id="88cf4-138">Transfer function.</span></span> |
| [<span data-ttu-id="88cf4-139">**\_ \_ Матрица MF MT YUV \_**</span><span class="sxs-lookup"><span data-stu-id="88cf4-139">**MF\_MT\_YUV\_MATRIX**</span></span>](mf-mt-yuv-matrix-attribute.md)                    | <span data-ttu-id="88cf4-140">Матрица перемещения.</span><span class="sxs-lookup"><span data-stu-id="88cf4-140">Transfer matrix.</span></span>   |
| [<span data-ttu-id="88cf4-141">**MF \_ Book \_ \_ чрома \_ заблокировано**</span><span class="sxs-lookup"><span data-stu-id="88cf4-141">**MF\_MT\_VIDEO\_CHROMA\_SITING**</span></span>](mf-mt-video-chroma-siting-attribute.md) | <span data-ttu-id="88cf4-142">Чрома заблокировано.</span><span class="sxs-lookup"><span data-stu-id="88cf4-142">Chroma siting.</span></span>     |
| [<span data-ttu-id="88cf4-143">**\_ \_ \_ Номинальный диапазон видео MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="88cf4-143">**MF\_MT\_VIDEO\_NOMINAL\_RANGE**</span></span>](mf-mt-video-nominal-range-attribute.md) | <span data-ttu-id="88cf4-144">Номинальный диапазон.</span><span class="sxs-lookup"><span data-stu-id="88cf4-144">Nominal range.</span></span>     |



 

<span data-ttu-id="88cf4-145">Дополнительные сведения см. в разделе [Расширенные сведения о цвете](extended-color-information.md).</span><span class="sxs-lookup"><span data-stu-id="88cf4-145">For more information, see [Extended Color Information](extended-color-information.md).</span></span> <span data-ttu-id="88cf4-146">Например, если вы создаете тип мультимедиа, описывающий стандарт видео, а стандарт определяет чрома заблокировано, добавьте эти сведения в тип носителя.</span><span class="sxs-lookup"><span data-stu-id="88cf4-146">For example, if you create a media type that describes a video standard, and the standard defines the chroma siting, add this information to the media type.</span></span> <span data-ttu-id="88cf4-147">Это помогает сохранить цветовую точность по всему конвейеру.</span><span class="sxs-lookup"><span data-stu-id="88cf4-147">Doing so helps to preserve color fidelity throughout the pipeline.</span></span>

<span data-ttu-id="88cf4-148">Следующие функции могут быть полезны при создании типа видеоклипа.</span><span class="sxs-lookup"><span data-stu-id="88cf4-148">The following functions might be useful when creating a video media type.</span></span>



| <span data-ttu-id="88cf4-149">Функция</span><span class="sxs-lookup"><span data-stu-id="88cf4-149">Function</span></span>                                                                     | <span data-ttu-id="88cf4-150">Описание</span><span class="sxs-lookup"><span data-stu-id="88cf4-150">Description</span></span>                                                                                                                                                                          |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88cf4-151">**мфаверажетимеперфраметофрамерате**</span><span class="sxs-lookup"><span data-stu-id="88cf4-151">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | <span data-ttu-id="88cf4-152">Вычисляет частоту кадров с учетом средней длительности кадра.</span><span class="sxs-lookup"><span data-stu-id="88cf4-152">Calculates the frame rate, given the average frame duration.</span></span>                                                                                                                         |
| [<span data-ttu-id="88cf4-153">**мфкалкулатеимажесизе**</span><span class="sxs-lookup"><span data-stu-id="88cf4-153">**MFCalculateImageSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | <span data-ttu-id="88cf4-154">Вычисляет размер изображения для несжатого видеоформата.</span><span class="sxs-lookup"><span data-stu-id="88cf4-154">Calculates the image size for an uncompressed video format.</span></span>                                                                                                                          |
| [<span data-ttu-id="88cf4-155">**мффрамератетоаверажетимеперфраме**</span><span class="sxs-lookup"><span data-stu-id="88cf4-155">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | <span data-ttu-id="88cf4-156">Вычисляет среднюю Длительность кадра видео по частоте кадров.</span><span class="sxs-lookup"><span data-stu-id="88cf4-156">Calculates the average duration of a video frame, given the frame rate.</span></span>                                                                                                              |
| [<span data-ttu-id="88cf4-157">**мфжетстридефорбитмапинфохеадер**</span><span class="sxs-lookup"><span data-stu-id="88cf4-157">**MFGetStrideForBitmapInfoHeader**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | <span data-ttu-id="88cf4-158">Возвращает минимальный шаг поверхности для формата видео.</span><span class="sxs-lookup"><span data-stu-id="88cf4-158">Returns the minimum surface stride for a video format.</span></span> <span data-ttu-id="88cf4-159">Дополнительные сведения см. в разделе [Шаг с изображением](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="88cf4-159">For more information, see [Image Stride](image-stride.md).</span></span>                                                                   |
| [<span data-ttu-id="88cf4-160">**мфинитвидеоформат**</span><span class="sxs-lookup"><span data-stu-id="88cf4-160">**MFInitVideoFormat**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfinitvideoformat)                               | <span data-ttu-id="88cf4-161">Инициализирует структуру [**мфвидеоформат**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) для некоторых стандартных видеоформатов, таких как NTSC телевидение.</span><span class="sxs-lookup"><span data-stu-id="88cf4-161">Initializes an [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) structure for some standard video formats, such as NTSC television.</span></span> <span data-ttu-id="88cf4-162">Затем можно использовать структуру для инициализации типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="88cf4-162">You can then use the structure to initialize a media type.</span></span> |
| [<span data-ttu-id="88cf4-163">**мфисформатюв**</span><span class="sxs-lookup"><span data-stu-id="88cf4-163">**MFIsFormatYUV**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | <span data-ttu-id="88cf4-164">Запрашивает, является ли видео форматом YUV.</span><span class="sxs-lookup"><span data-stu-id="88cf4-164">Queries whether a video format is a YUV format.</span></span>                                                                                                                                      |



 

## <a name="examples"></a><span data-ttu-id="88cf4-165">Примеры</span><span class="sxs-lookup"><span data-stu-id="88cf4-165">Examples</span></span>

<span data-ttu-id="88cf4-166">В этом примере показана функция, которая заполняет наиболее распространенные сведения о несжатом видео формате.</span><span class="sxs-lookup"><span data-stu-id="88cf4-166">This example shows a function that fills in the most common information for an uncompressed video format.</span></span> <span data-ttu-id="88cf4-167">Функция возвращает указатель интерфейса [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="88cf4-167">The function returns an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span> <span data-ttu-id="88cf4-168">При необходимости можно добавить дополнительные атрибуты к типу носителя.</span><span class="sxs-lookup"><span data-stu-id="88cf4-168">You can then add additional attributes to the media type as needed.</span></span>


```C++
HRESULT CreateUncompressedVideoType(
    DWORD                fccFormat,  // FOURCC or D3DFORMAT value.     
    UINT32               width, 
    UINT32               height,
    MFVideoInterlaceMode interlaceMode,
    const MFRatio&       frameRate,
    const MFRatio&       par,
    IMFMediaType         **ppType
    )
{
    if (ppType == NULL)
    {
        return E_POINTER;
    }

    GUID    subtype = MFVideoFormat_Base;
    LONG    lStride = 0;
    UINT    cbImage = 0;

    IMFMediaType *pType = NULL;

    // Set the subtype GUID from the FOURCC or D3DFORMAT value.
    subtype.Data1 = fccFormat;

    HRESULT hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_INTERLACE_MODE, interlaceMode);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFSetAttributeSize(pType, MF_MT_FRAME_SIZE, width, height);
    if (FAILED(hr))
    {
        goto done;
    }

    // Calculate the default stride value.
    hr = pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    if (FAILED(hr))
    {
        goto done;
    }

    // Calculate the image size in bytes.
    hr = MFCalculateImageSize(subtype, width, height, &cbImage);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_SAMPLE_SIZE, cbImage);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_FIXED_SIZE_SAMPLES, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Frame rate
    hr = MFSetAttributeRatio(pType, MF_MT_FRAME_RATE, frameRate.Numerator, 
        frameRate.Denominator);
    if (FAILED(hr))
    {
        goto done;
    }

    // Pixel aspect ratio
    hr = MFSetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, par.Numerator, 
        par.Denominator);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppType = pType;
    (*ppType)->AddRef();

done:
    SafeRelease(&pType);
    return hr;
}
```



<span data-ttu-id="88cf4-169">В следующем примере в качестве входных данных используется закодированный видеоформат и создается соответствующий тип несжатого видео.</span><span class="sxs-lookup"><span data-stu-id="88cf4-169">The next example takes an encoded video format as input, and creates a matching uncompressed video type.</span></span> <span data-ttu-id="88cf4-170">Например, этот тип подходит для установки в кодировщике или декодере.</span><span class="sxs-lookup"><span data-stu-id="88cf4-170">This type would be suitable to set on an encoder or decoder, for example.</span></span>


```C++
HRESULT ConvertVideoTypeToUncompressedType(
    IMFMediaType *pType,    // Pointer to an encoded video type.
    const GUID& subtype,    // Uncompressed subtype (eg, RGB-32, AYUV)
    IMFMediaType **ppType   // Receives a matching uncompressed video type.
    )
{
    IMFMediaType *pTypeUncomp = NULL;

    HRESULT hr = S_OK;
    GUID majortype = { 0 };
    MFRatio par = { 0 };

    hr = pType->GetMajorType(&majortype);

    if (majortype != MFMediaType_Video)
    {
        return MF_E_INVALIDMEDIATYPE;
    }

    // Create a new media type and copy over all of the items.
    // This ensures that extended color information is retained.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pTypeUncomp);
    }

    if (SUCCEEDED(hr))
    {
        hr = pType->CopyAllItems(pTypeUncomp);
    }

    // Set the subtype.
    if (SUCCEEDED(hr))
    {
        hr = pTypeUncomp->SetGUID(MF_MT_SUBTYPE, subtype);
    }

    // Uncompressed means all samples are independent.
    if (SUCCEEDED(hr))
    {
        hr = pTypeUncomp->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    }

    // Fix up PAR if not set on the original type.
    if (SUCCEEDED(hr))
    {
        hr = MFGetAttributeRatio(
            pTypeUncomp, 
            MF_MT_PIXEL_ASPECT_RATIO, 
            (UINT32*)&par.Numerator, 
            (UINT32*)&par.Denominator
            );

        // Default to square pixels.
        if (FAILED(hr))
        {
            hr = MFSetAttributeRatio(
                pTypeUncomp, 
                MF_MT_PIXEL_ASPECT_RATIO, 
                1, 1
                );
        }
    }

    if (SUCCEEDED(hr))
    {
        *ppType = pTypeUncomp;
        (*ppType)->AddRef();
    }

    SafeRelease(&pTypeUncomp);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="88cf4-171">См. также</span><span class="sxs-lookup"><span data-stu-id="88cf4-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88cf4-172">Расширенные сведения о цвете</span><span class="sxs-lookup"><span data-stu-id="88cf4-172">Extended Color Information</span></span>](extended-color-information.md)
</dt> <dt>

[<span data-ttu-id="88cf4-173">Шаг изображения</span><span class="sxs-lookup"><span data-stu-id="88cf4-173">Image Stride</span></span>](image-stride.md)
</dt> <dt>

[<span data-ttu-id="88cf4-174">Типы носителей</span><span class="sxs-lookup"><span data-stu-id="88cf4-174">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="88cf4-175">Типы видеоклипов</span><span class="sxs-lookup"><span data-stu-id="88cf4-175">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="88cf4-176">Идентификаторы GUID для подтипов видео</span><span class="sxs-lookup"><span data-stu-id="88cf4-176">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 



