---
description: Устройство видеозаписи может поддерживать несколько форматов записи. Форматы обычно отличаются типом сжатия, цветовым пространством (YUV или RGB), размером кадра или частотой кадров.
ms.assetid: 479abaea-f310-4139-9967-f24b03c34558
title: Настройка формата видеозаписи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27cb9c20cbf989ab5db3564733dc96860c7bcb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702119"
---
# <a name="how-to-set-the-video-capture-format"></a><span data-ttu-id="609ad-104">Настройка формата видеозаписи</span><span class="sxs-lookup"><span data-stu-id="609ad-104">How to Set the Video Capture Format</span></span>

<span data-ttu-id="609ad-105">Устройство видеозаписи может поддерживать несколько форматов записи.</span><span class="sxs-lookup"><span data-stu-id="609ad-105">A video capture device might support several capture formats.</span></span> <span data-ttu-id="609ad-106">Форматы обычно отличаются типом сжатия, цветовым пространством (YUV или RGB), размером кадра или частотой кадров.</span><span class="sxs-lookup"><span data-stu-id="609ad-106">Formats typically differ by compression type, color space (YUV or RGB), frame size, or frame rate.</span></span>

<span data-ttu-id="609ad-107">Список поддерживаемых форматов содержится в *дескрипторе презентации*.</span><span class="sxs-lookup"><span data-stu-id="609ad-107">The list of supported formats is contained in the *presentation descriptor*.</span></span> <span data-ttu-id="609ad-108">Дополнительные сведения см. в разделе [дескрипторы представления](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="609ad-108">For more information, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

<span data-ttu-id="609ad-109">Чтобы перечислить Поддерживаемые форматы:</span><span class="sxs-lookup"><span data-stu-id="609ad-109">To enumerate the supported formats:</span></span>

1.  <span data-ttu-id="609ad-110">Создайте источник мультимедиа для устройства записи.</span><span class="sxs-lookup"><span data-stu-id="609ad-110">Create the media source for the capture device.</span></span> <span data-ttu-id="609ad-111">См. раздел [Перечисление устройств видеозаписи](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="609ad-111">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="609ad-112">Вызовите [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) в источнике мультимедиа, чтобы получить дескриптор представления.</span><span class="sxs-lookup"><span data-stu-id="609ad-112">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source to get the presentation descriptor.</span></span>
3.  <span data-ttu-id="609ad-113">Вызовите [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) , чтобы получить дескриптор потока для видеопотока.</span><span class="sxs-lookup"><span data-stu-id="609ad-113">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to get the stream descriptor for the video stream.</span></span>
4.  <span data-ttu-id="609ad-114">Вызовите [**имфстреамдескриптор:: жетмедиатипехандлер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) в дескрипторе потока.</span><span class="sxs-lookup"><span data-stu-id="609ad-114">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span>
5.  <span data-ttu-id="609ad-115">Вызовите метод [**имфмедиатипехандлер:: жетмедиатипекаунт**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) , чтобы получить количество поддерживаемых форматов.</span><span class="sxs-lookup"><span data-stu-id="609ad-115">Call [**IMFMediaTypeHandler::GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) to get the number of supported formats.</span></span>
6.  <span data-ttu-id="609ad-116">В цикле вызовите [**имфмедиатипехандлер:: жетмедиатипебиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) , чтобы получить каждый формат.</span><span class="sxs-lookup"><span data-stu-id="609ad-116">In a loop, call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) to get each format.</span></span> <span data-ttu-id="609ad-117">Формат представлен *типом мультимедиа*.</span><span class="sxs-lookup"><span data-stu-id="609ad-117">The format is represented by a *media type*.</span></span> <span data-ttu-id="609ad-118">Дополнительные сведения см. в разделе [типы видеоклипов](video-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="609ad-118">For more information, see [Video Media Types](video-media-types.md).</span></span>

<span data-ttu-id="609ad-119">В следующем примере перечисляются форматы записи для устройства.</span><span class="sxs-lookup"><span data-stu-id="609ad-119">The following example enumerates the capture formats for a device:</span></span>


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



<span data-ttu-id="609ad-120">`LogMediaType`Функция, используемая в этом примере, указана в разделе [код отладки типа носителя](media-type-debugging-code.md).</span><span class="sxs-lookup"><span data-stu-id="609ad-120">The `LogMediaType` function used in this example is listed in the topic [Media Type Debugging Code](media-type-debugging-code.md).</span></span>

<span data-ttu-id="609ad-121">Чтобы задать формат записи, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="609ad-121">To set the capture format:</span></span>

1.  <span data-ttu-id="609ad-122">Получите указатель на интерфейс [**имфмедиатипехандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) , как показано в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="609ad-122">Get a pointer to the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface, as shown in the previous example.</span></span>
2.  <span data-ttu-id="609ad-123">Вызовите метод [**имфмедиатипехандлер:: жетмедиатипебиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) , чтобы получить нужный формат, указанный по индексу.</span><span class="sxs-lookup"><span data-stu-id="609ad-123">Call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) to get the desired format, specified by index.</span></span>
3.  <span data-ttu-id="609ad-124">Вызовите [**имфмедиатипехандлер:: сеткуррентмедиатипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) , чтобы задать формат.</span><span class="sxs-lookup"><span data-stu-id="609ad-124">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) to set the format.</span></span>

<span data-ttu-id="609ad-125">Если не задать формат записи, устройство будет использовать формат по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="609ad-125">If you do not set the capture format, the device will use its default format.</span></span>

<span data-ttu-id="609ad-126">В следующем примере задается формат записи:</span><span class="sxs-lookup"><span data-stu-id="609ad-126">The following example sets the capture format:</span></span>


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



<span data-ttu-id="609ad-127">Порядок, в котором возвращаются форматы, зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="609ad-127">The order in which formats are returned depends on the device.</span></span> <span data-ttu-id="609ad-128">Как правило, они группируются сначала по типу сжатия или цветовому пространству. а затем от наименьшего размера кадра до самого крупного кадра в пределах каждой группы.</span><span class="sxs-lookup"><span data-stu-id="609ad-128">Typically, they are grouped first by compression type or color space; and then from smallest frame size to largest frame size within each group.</span></span>

<span data-ttu-id="609ad-129">Частота кадров обрабатывается немного иначе, чем другие атрибуты формата.</span><span class="sxs-lookup"><span data-stu-id="609ad-129">The frame rate is handled slightly differently than the other format attributes.</span></span> <span data-ttu-id="609ad-130">Дополнительные сведения см. в разделе [Настройка частоты кадров видеозаписи](how-to-set-the-video-capture-frame-rate.md).</span><span class="sxs-lookup"><span data-stu-id="609ad-130">For more information, see [How to Set the Video Capture Frame Rate](how-to-set-the-video-capture-frame-rate.md).</span></span>

> [!Note]  
> <span data-ttu-id="609ad-131">В некоторых устройствах список формат будет содержать дублирующуюся запись для каждого формата.</span><span class="sxs-lookup"><span data-stu-id="609ad-131">In some devices, the format list will contain a duplicate entry for each format.</span></span> <span data-ttu-id="609ad-132">Например, если устройство поддерживает 15 различных форматов записи, список будет содержать 30 записей.</span><span class="sxs-lookup"><span data-stu-id="609ad-132">For example, if the device supports 15 distinct capture formats, the list will contain 30 entries.</span></span> <span data-ttu-id="609ad-133">В каждой паре один из типов мультимедиа будет иметь [**\_ \_ \_ \_ тип формата MF MT**](mf-mt-am-format-type-attribute.md) , равный **Format \_ видеоинфо**, а другой — **\_ \_ \_ Формат \_ MF MT** , равный **Format \_ VideoInfo2**.</span><span class="sxs-lookup"><span data-stu-id="609ad-133">Within each pair, one of the media types will have the attribute [**MF\_MT\_AM\_FORMAT\_TYPE**](mf-mt-am-format-type-attribute.md) equal to **FORMAT\_VideoInfo**, and the other will have **MF\_MT\_AM\_FORMAT\_TYPE** equal to **FORMAT\_VideoInfo2**.</span></span> <span data-ttu-id="609ad-134">(Эти два значения определены в файле заголовков UUID. h.) Второй тип может также содержать дополнительные сведения о цвете ([Расширенные сведения о цвете](extended-color-information.md)) или показывать другое значение для чередования (MF-в [**\_ \_ \_ режиме чередования**](mf-mt-interlace-mode-attribute.md)).</span><span class="sxs-lookup"><span data-stu-id="609ad-134">(These two values are defined in the header file uuids.h.) The second type might also contain additional color information ([Extended Color Information](extended-color-information.md)) or show a different value for interlacing ([**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md)).</span></span> <span data-ttu-id="609ad-135">Эти дублирующиеся типы существуют для поддержки старых приложений DirectShow.</span><span class="sxs-lookup"><span data-stu-id="609ad-135">These duplicate types exist to support older DirectShow applications.</span></span> <span data-ttu-id="609ad-136">В Media Foundationном приложении следует игнорировать **\_ видеоинфо Format** , когда в списке будет указан дублирующий тип **\_ VideoInfo2 Format** .</span><span class="sxs-lookup"><span data-stu-id="609ad-136">In a Media Foundation application, you should ignore the **FORMAT\_VideoInfo** type whenever a duplicate **FORMAT\_VideoInfo2** type is listed.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="609ad-137">См. также</span><span class="sxs-lookup"><span data-stu-id="609ad-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="609ad-138">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="609ad-138">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



