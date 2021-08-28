---
description: Устройство видеозаписи может поддерживать ряд частот кадров.
ms.assetid: 9578e60d-0339-4382-b798-2d31d2ddbe76
title: Настройка частоты кадров видеозаписи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0e80c26c5a53a89cbc87ca509f25db1ebccf4571b4dda2e83ea63717c7d91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827974"
---
# <a name="how-to-set-the-video-capture-frame-rate"></a>Настройка частоты кадров видеозаписи

Устройство видеозаписи может поддерживать ряд частот кадров. Если эта информация доступна, минимальные и максимальные частоты кадров хранятся в виде атрибутов типа мультимедиа:



| attribute                                                         | Описание         |
|-------------------------------------------------------------------|---------------------|
| [\_ \_ \_ \_ максимальный диапазон частот кадров MF MT \_](mf-mt-frame-rate-range-max.md) | Максимальная частота кадров. |
| [\_ \_ \_ \_ Минимальный диапазон частот кадров MF MT \_](mf-mt-frame-rate-range-min.md) | Минимальная частота кадров. |



 

Диапазон может зависеть от формата записи. Например, при больших размерах фрейма максимальная частота кадров может быть уменьшена.

Чтобы задать частоту кадров, выполните следующие действия.

1.  Создайте источник мультимедиа для устройства записи. См. раздел [Перечисление устройств видеозаписи](enumerating-video-capture-devices.md).
2.  Вызовите [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) в источнике мультимедиа, чтобы получить дескриптор представления.
3.  Вызовите [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) , чтобы получить дескриптор потока для видеопотока.
4.  Вызовите [**имфстреамдескриптор:: жетмедиатипехандлер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) в дескрипторе потока.
5.  Перечислите форматы записи, как описано в разделе [Настройка формата видеозаписи](how-to-set-the-video-capture-format.md).
6.  Выберите нужный выходной формат из списка.
7.  Запросите тип носителя для атрибутов минимальной частоты [кадров MF с \_ \_ \_ \_ диапазоном \_ ](mf-mt-frame-rate-range-max.md) частота и [MF для \_ \_ \_ \_ диапазона \_ частот](mf-mt-frame-rate-range-min.md) кадров MT. Эти значения обеспечивают диапазон поддерживаемых частот кадров. Устройство может поддерживать другие частоты кадров в этом диапазоне.
8.  Чтобы указать нужную частоту кадров, установите атрибут " [**MF \_ MT \_ Frame**](mf-mt-frame-rate-attribute.md) " для типа носителя.
9.  Вызовите [**имфмедиатипехандлер:: сеткуррентмедиатипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) с измененным типом носителя.

В следующем примере задается частота кадров, равная максимальной частоте кадров, поддерживаемой устройством:


```C++
HRESULT SetMaxFrameRate(IMFMediaSource *pSource, DWORD dwTypeIndex)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFStreamDescriptor *pSD = NULL;
    IMFMediaTypeHandler *pHandler = NULL;
    IMFMediaType *pType = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL fSelected;
    hr = pPD->GetStreamDescriptorByIndex(dwTypeIndex, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetCurrentMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the maximum frame rate for the selected capture format.

    // Note: To get the minimum frame rate, use the 
    // MF_MT_FRAME_RATE_RANGE_MIN attribute instead.

    PROPVARIANT var;
    if (SUCCEEDED(pType->GetItem(MF_MT_FRAME_RATE_RANGE_MAX, &var)))
    {
        hr = pType->SetItem(MF_MT_FRAME_RATE, var);

        PropVariantClear(&var);

        if (FAILED(hr))
        {
            goto done;
        }

        hr = pHandler->SetCurrentMediaType(pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Видеозапись](video-capture.md)
</dt> </dl>

 

 



