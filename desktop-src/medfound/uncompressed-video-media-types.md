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
# <a name="uncompressed-video-media-types"></a>Типы несжатых видеоматериалов

В этом разделе описывается создание типа носителя, который описывает формат видео без сжатия. Дополнительные сведения о типах мультимедиа см. в разделе [About Media Types](about-media-types.md).

Чтобы создать полный несжатый тип видео, задайте следующие атрибуты в указателе интерфейса [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .



| attribute                                                                            | Описание                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ основной тип MF \_ MT**](mf-mt-major-type-attribute.md)                            | Основной тип. Задайте значение **мфмедиатипе \_ Video**.                                                                                                                                                                                          |
| [**подтип MF \_ MT \_**](mf-mt-subtype-attribute.md)                                   | Подтип. См. раздел [GUID подтипа видео](video-subtype-guids.md).                                                                                                                                                                        |
| [**MF \_ , \_ шаг по умолчанию \_**](mf-mt-default-stride-attribute.md)                    | Шаг с поверхностью. *Шаг* — это число байтов, необходимое для перехода от одной строки пикселей к следующей. Установите этот атрибут, если шаг в байтах не совпадает с шириной видео в байтах. В противном случае этот атрибут можно опустить. |
| [**\_ \_ Частота кадров MF \_ MT**](mf-mt-frame-rate-attribute.md)                            | Частота кадров.                                                                                                                                                                                                                         |
| [**\_ \_ Размер пакета MF \_ MT**](mf-mt-frame-size-attribute.md)                            | Размер кадра.                                                                                                                                                                                                                         |
| [**\_ \_ режим чересстрочную РАЗВЕРТКи MF \_**](mf-mt-interlace-mode-attribute.md)                    | Режим чередования.                                                                                                                                                                                                                   |
| [**MF \_ — \_ все \_ \_ независимые примеры**](mf-mt-all-samples-independent-attribute.md) | Указывает, является ли каждый выбор независимым. Задайте значение **true** для несжатых форматов.                                                                                                                                             |
| [**пропорции MF \_ MT \_ пикселей \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md)           | Пропорция в пикселях.                                                                                                                                                                                                                 |



 

Кроме того, если вы знакомы с правильными значениями, задайте следующие атрибуты. (В противном случае не указывайте эти атрибуты.)



| attribute                                                                    | Описание        |
|------------------------------------------------------------------------------|--------------------|
| [**\_ \_ \_ первичные цвета видео MF MT**](mf-mt-video-primaries-attribute.md)          | Первичные цвета.   |
| [**\_ \_ функция перемещения MF \_ MT**](mf-mt-transfer-function-attribute.md)      | Функция перемещения. |
| [**\_ \_ Матрица MF MT YUV \_**](mf-mt-yuv-matrix-attribute.md)                    | Матрица перемещения.   |
| [**MF \_ Book \_ \_ чрома \_ заблокировано**](mf-mt-video-chroma-siting-attribute.md) | Чрома заблокировано.     |
| [**\_ \_ \_ Номинальный диапазон видео MF MT \_**](mf-mt-video-nominal-range-attribute.md) | Номинальный диапазон.     |



 

Дополнительные сведения см. в разделе [Расширенные сведения о цвете](extended-color-information.md). Например, если вы создаете тип мультимедиа, описывающий стандарт видео, а стандарт определяет чрома заблокировано, добавьте эти сведения в тип носителя. Это помогает сохранить цветовую точность по всему конвейеру.

Следующие функции могут быть полезны при создании типа видеоклипа.



| Функция                                                                     | Описание                                                                                                                                                                          |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**мфаверажетимеперфраметофрамерате**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | Вычисляет частоту кадров с учетом средней длительности кадра.                                                                                                                         |
| [**мфкалкулатеимажесизе**](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | Вычисляет размер изображения для несжатого видеоформата.                                                                                                                          |
| [**мффрамератетоаверажетимеперфраме**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | Вычисляет среднюю Длительность кадра видео по частоте кадров.                                                                                                              |
| [**мфжетстридефорбитмапинфохеадер**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | Возвращает минимальный шаг поверхности для формата видео. Дополнительные сведения см. в разделе [Шаг с изображением](image-stride.md).                                                                   |
| [**мфинитвидеоформат**](/windows/desktop/api/mfapi/nf-mfapi-mfinitvideoformat)                               | Инициализирует структуру [**мфвидеоформат**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) для некоторых стандартных видеоформатов, таких как NTSC телевидение. Затем можно использовать структуру для инициализации типа мультимедиа. |
| [**мфисформатюв**](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | Запрашивает, является ли видео форматом YUV.                                                                                                                                      |



 

## <a name="examples"></a>Примеры

В этом примере показана функция, которая заполняет наиболее распространенные сведения о несжатом видео формате. Функция возвращает указатель интерфейса [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . При необходимости можно добавить дополнительные атрибуты к типу носителя.


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



В следующем примере в качестве входных данных используется закодированный видеоформат и создается соответствующий тип несжатого видео. Например, этот тип подходит для установки в кодировщике или декодере.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Расширенные сведения о цвете](extended-color-information.md)
</dt> <dt>

[Шаг изображения](image-stride.md)
</dt> <dt>

[Типы носителей](media-types.md)
</dt> <dt>

[Типы видеоклипов](video-media-types.md)
</dt> <dt>

[Идентификаторы GUID для подтипов видео](video-subtype-guids.md)
</dt> </dl>

 

 



