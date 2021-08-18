---
description: Устройство видеозаписи может поддерживать несколько форматов записи. Форматы обычно отличаются типом сжатия, цветовым пространством (YUV или RGB), размером кадра или частотой кадров.
ms.assetid: 479abaea-f310-4139-9967-f24b03c34558
title: Настройка формата видеозаписи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0968560772345bea91f5acfb79e7157a6376f388a5c0065634a273196b7552cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974403"
---
# <a name="how-to-set-the-video-capture-format"></a>Настройка формата видеозаписи

Устройство видеозаписи может поддерживать несколько форматов записи. Форматы обычно отличаются типом сжатия, цветовым пространством (YUV или RGB), размером кадра или частотой кадров.

Список поддерживаемых форматов содержится в *дескрипторе презентации*. Дополнительные сведения см. в разделе [дескрипторы представления](presentation-descriptors.md).

Чтобы перечислить Поддерживаемые форматы:

1.  Создайте источник мультимедиа для устройства записи. См. раздел [Перечисление устройств видеозаписи](enumerating-video-capture-devices.md).
2.  Вызовите [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) в источнике мультимедиа, чтобы получить дескриптор представления.
3.  Вызовите [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) , чтобы получить дескриптор потока для видеопотока.
4.  Вызовите [**имфстреамдескриптор:: жетмедиатипехандлер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) в дескрипторе потока.
5.  Вызовите метод [**имфмедиатипехандлер:: жетмедиатипекаунт**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) , чтобы получить количество поддерживаемых форматов.
6.  В цикле вызовите [**имфмедиатипехандлер:: жетмедиатипебиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) , чтобы получить каждый формат. Формат представлен *типом мультимедиа*. Дополнительные сведения см. в разделе [типы видеоклипов](video-media-types.md).

В следующем примере перечисляются форматы записи для устройства.


```C++
HRESULT EnumerateCaptureFormats(IMFMediaSource *pSource)
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
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cTypes = 0;
    hr = pHandler->GetMediaTypeCount(&cTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cTypes; i++)
    {
        hr = pHandler->GetMediaTypeByIndex(i, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        LogMediaType(pType);
        OutputDebugString(L"\n");

        SafeRelease(&pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



`LogMediaType`Функция, используемая в этом примере, указана в разделе [код отладки типа носителя](media-type-debugging-code.md).

Чтобы задать формат записи, сделайте следующее:

1.  Получите указатель на интерфейс [**имфмедиатипехандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) , как показано в предыдущем примере.
2.  Вызовите метод [**имфмедиатипехандлер:: жетмедиатипебиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) , чтобы получить нужный формат, указанный по индексу.
3.  Вызовите [**имфмедиатипехандлер:: сеткуррентмедиатипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) , чтобы задать формат.

Если не задать формат записи, устройство будет использовать формат по умолчанию.

В следующем примере задается формат записи:


```C++
HRESULT SetDeviceFormat(IMFMediaSource *pSource, DWORD dwFormatIndex)
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
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetMediaTypeByIndex(dwFormatIndex, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->SetCurrentMediaType(pType);

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



Порядок, в котором возвращаются форматы, зависит от устройства. Как правило, они группируются сначала по типу сжатия или цветовому пространству. а затем от наименьшего размера кадра до самого крупного кадра в пределах каждой группы.

Частота кадров обрабатывается немного иначе, чем другие атрибуты формата. Дополнительные сведения см. в разделе [Настройка частоты кадров видеозаписи](how-to-set-the-video-capture-frame-rate.md).

> [!Note]  
> В некоторых устройствах список формат будет содержать дублирующуюся запись для каждого формата. Например, если устройство поддерживает 15 различных форматов записи, список будет содержать 30 записей. В каждой паре один из типов мультимедиа будет иметь [**\_ \_ \_ \_ тип формата MF MT**](mf-mt-am-format-type-attribute.md) , равный **Format \_ видеоинфо**, а другой — **\_ \_ \_ Формат \_ MF MT** , равный **Format \_ VideoInfo2**. (Эти два значения определены в файле заголовков UUID. h.) Второй тип может также содержать дополнительные сведения о цвете ([Расширенные сведения о цвете](extended-color-information.md)) или показывать другое значение для чередования (MF-в [**\_ \_ \_ режиме чередования**](mf-mt-interlace-mode-attribute.md)). для поддержки старых DirectShow приложений существуют дублирующиеся типы. В Media Foundationном приложении следует игнорировать **\_ видеоинфо Format** , когда в списке будет указан дублирующий тип **\_ VideoInfo2 Format** .

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Видеозапись](video-capture.md)
</dt> </dl>

 

 



