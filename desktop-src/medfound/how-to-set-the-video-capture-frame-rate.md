---
description: Устройство видеозаписи может поддерживать ряд частот кадров.
ms.assetid: 9578e60d-0339-4382-b798-2d31d2ddbe76
title: Настройка частоты кадров видеозаписи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e105965f5449cb7f4cab59f49410ecfb40221c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701749"
---
# <a name="how-to-set-the-video-capture-frame-rate"></a><span data-ttu-id="d922f-103">Настройка частоты кадров видеозаписи</span><span class="sxs-lookup"><span data-stu-id="d922f-103">How to Set the Video Capture Frame Rate</span></span>

<span data-ttu-id="d922f-104">Устройство видеозаписи может поддерживать ряд частот кадров.</span><span class="sxs-lookup"><span data-stu-id="d922f-104">A video capture device might support a range of frame rates.</span></span> <span data-ttu-id="d922f-105">Если эта информация доступна, минимальные и максимальные частоты кадров хранятся в виде атрибутов типа мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="d922f-105">If this information is available, the minimum and maximum frame rates are stored as media type attributes:</span></span>



| <span data-ttu-id="d922f-106">attribute</span><span class="sxs-lookup"><span data-stu-id="d922f-106">Attribute</span></span>                                                         | <span data-ttu-id="d922f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d922f-107">Description</span></span>         |
|-------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="d922f-108">\_ \_ \_ \_ максимальный диапазон частот кадров MF MT \_</span><span class="sxs-lookup"><span data-stu-id="d922f-108">MF\_MT\_FRAME\_RATE\_RANGE\_MAX</span></span>](mf-mt-frame-rate-range-max.md) | <span data-ttu-id="d922f-109">Максимальная частота кадров.</span><span class="sxs-lookup"><span data-stu-id="d922f-109">Maximum frame rate.</span></span> |
| [<span data-ttu-id="d922f-110">\_ \_ \_ \_ Минимальный диапазон частот кадров MF MT \_</span><span class="sxs-lookup"><span data-stu-id="d922f-110">MF\_MT\_FRAME\_RATE\_RANGE\_MIN</span></span>](mf-mt-frame-rate-range-min.md) | <span data-ttu-id="d922f-111">Минимальная частота кадров.</span><span class="sxs-lookup"><span data-stu-id="d922f-111">Minimum frame rate.</span></span> |



 

<span data-ttu-id="d922f-112">Диапазон может зависеть от формата записи.</span><span class="sxs-lookup"><span data-stu-id="d922f-112">The range can vary depending on the capture format.</span></span> <span data-ttu-id="d922f-113">Например, при больших размерах фрейма максимальная частота кадров может быть уменьшена.</span><span class="sxs-lookup"><span data-stu-id="d922f-113">For example, at larger frame sizes, the maximum frame rate might be reduced.</span></span>

<span data-ttu-id="d922f-114">Чтобы задать частоту кадров, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d922f-114">To set the frame rate:</span></span>

1.  <span data-ttu-id="d922f-115">Создайте источник мультимедиа для устройства записи.</span><span class="sxs-lookup"><span data-stu-id="d922f-115">Create the media source for the capture device.</span></span> <span data-ttu-id="d922f-116">См. раздел [Перечисление устройств видеозаписи](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="d922f-116">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="d922f-117">Вызовите [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) в источнике мультимедиа, чтобы получить дескриптор представления.</span><span class="sxs-lookup"><span data-stu-id="d922f-117">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source to get the presentation descriptor.</span></span>
3.  <span data-ttu-id="d922f-118">Вызовите [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) , чтобы получить дескриптор потока для видеопотока.</span><span class="sxs-lookup"><span data-stu-id="d922f-118">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to get the stream descriptor for the video stream.</span></span>
4.  <span data-ttu-id="d922f-119">Вызовите [**имфстреамдескриптор:: жетмедиатипехандлер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) в дескрипторе потока.</span><span class="sxs-lookup"><span data-stu-id="d922f-119">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span>
5.  <span data-ttu-id="d922f-120">Перечислите форматы записи, как описано в разделе [Настройка формата видеозаписи](how-to-set-the-video-capture-format.md).</span><span class="sxs-lookup"><span data-stu-id="d922f-120">Enumerate the capture formats, as described in [How to Set the Video Capture Format](how-to-set-the-video-capture-format.md).</span></span>
6.  <span data-ttu-id="d922f-121">Выберите нужный выходной формат из списка.</span><span class="sxs-lookup"><span data-stu-id="d922f-121">Select the desired output format from the list.</span></span>
7.  <span data-ttu-id="d922f-122">Запросите тип носителя для атрибутов минимальной частоты [кадров MF с \_ \_ \_ \_ диапазоном \_ ](mf-mt-frame-rate-range-max.md) частота и [MF для \_ \_ \_ \_ диапазона \_ частот](mf-mt-frame-rate-range-min.md) кадров MT.</span><span class="sxs-lookup"><span data-stu-id="d922f-122">Query the media type for the [MF\_MT\_FRAME\_RATE\_RANGE\_MAX](mf-mt-frame-rate-range-max.md) and [MF\_MT\_FRAME\_RATE\_RANGE\_MIN](mf-mt-frame-rate-range-min.md) attributes.</span></span> <span data-ttu-id="d922f-123">Эти значения обеспечивают диапазон поддерживаемых частот кадров.</span><span class="sxs-lookup"><span data-stu-id="d922f-123">This values give the range of supported frame rates.</span></span> <span data-ttu-id="d922f-124">Устройство может поддерживать другие частоты кадров в этом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="d922f-124">The device might support other frame rates within this range.</span></span>
8.  <span data-ttu-id="d922f-125">Чтобы указать нужную частоту кадров, установите атрибут " [**MF \_ MT \_ Frame**](mf-mt-frame-rate-attribute.md) " для типа носителя.</span><span class="sxs-lookup"><span data-stu-id="d922f-125">Set the [**MF\_MT\_FRAME**](mf-mt-frame-rate-attribute.md) attribute on the media type to specify the desired frame rate.</span></span>
9.  <span data-ttu-id="d922f-126">Вызовите [**имфмедиатипехандлер:: сеткуррентмедиатипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) с измененным типом носителя.</span><span class="sxs-lookup"><span data-stu-id="d922f-126">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) with the modified media type.</span></span>

<span data-ttu-id="d922f-127">В следующем примере задается частота кадров, равная максимальной частоте кадров, поддерживаемой устройством:</span><span class="sxs-lookup"><span data-stu-id="d922f-127">The following example sets the frame rate equal to the maximum frame rate that the device supports:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d922f-128">См. также</span><span class="sxs-lookup"><span data-stu-id="d922f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d922f-129">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="d922f-129">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



