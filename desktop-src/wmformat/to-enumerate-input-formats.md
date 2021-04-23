---
title: Перечисление входных форматов
description: Перечисление входных форматов
ms.assetid: 482adfc4-d9ed-403d-912b-1a5a70baf04c
keywords:
- Расширенный системный формат (ASF), перечисление входных форматов
- ASF (Расширенный системный формат), перечисление входных форматов
- профили, перечисление входных форматов
- кодеки, перечисление входных форматов
- Расширенные системные форматы (ASF), перечисления входного формата
- ASF (Расширенный системный формат), перечисления входного формата
- профили, перечисления входных форматов
- кодеки, перечисления входного формата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18360d3172af785fd1c00648ba0c9e869fb7fbc6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104069699"
---
# <a name="to-enumerate-input-formats"></a><span data-ttu-id="91512-111">Перечисление входных форматов</span><span class="sxs-lookup"><span data-stu-id="91512-111">To Enumerate Input Formats</span></span>

<span data-ttu-id="91512-112">Каждый кодек Windows Media поддерживает один или несколько типов входных носителей для сжатия.</span><span class="sxs-lookup"><span data-stu-id="91512-112">Each of the Windows Media codecs accepts one or more types of input media for compression.</span></span> <span data-ttu-id="91512-113">Пакет SDK для формата Windows Media позволяет вводить более широкий спектр форматов, чем поддерживаемые кодеками.</span><span class="sxs-lookup"><span data-stu-id="91512-113">The Windows Media Format SDK enables you to input a wider variety of formats than those supported by the codecs.</span></span> <span data-ttu-id="91512-114">Пакет SDK делает это путем выполнения предварительной обработки преобразований для входных данных, например для изменения размера кадров видео или перевыборки звука.</span><span class="sxs-lookup"><span data-stu-id="91512-114">The SDK does this by performing pre-processing transformations on the inputs when necessary, such as resizing video frames or resampling audio.</span></span> <span data-ttu-id="91512-115">В любом случае необходимо убедиться, что форматы ввода для файлов, которые вы пишете, совпадают с данными, отправляемыми в модуль записи.</span><span class="sxs-lookup"><span data-stu-id="91512-115">In any case, you must ensure that the input formats for the files you write match the data you send to the writer.</span></span> <span data-ttu-id="91512-116">Каждый кодек имеет входной формат носителя по умолчанию, который задается в модуле записи при загрузке профиля.</span><span class="sxs-lookup"><span data-stu-id="91512-116">Each codec has a default input media format that is set in the writer when the profile is loaded.</span></span> <span data-ttu-id="91512-117">Вы можете проверить формат ввода по умолчанию, вызвав [**ивмвритер:: жетинпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span><span class="sxs-lookup"><span data-stu-id="91512-117">You can examine the default input format by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>

<span data-ttu-id="91512-118">Видеокодеки поддерживают следующие форматы: ИЙУВ, I420, YV12, YUY2, UYVY, ИВЮ, YVU9, RGB 32, RGB 24, RGB 565, RGB 555 и RGB 8.</span><span class="sxs-lookup"><span data-stu-id="91512-118">The video codecs support the following formats: IYUV, I420, YV12, YUY2, UYVY, YVYU, YVU9, RGB 32, RGB 24, RGB 565, RGB 555, and RGB 8.</span></span> <span data-ttu-id="91512-119">Аудиокодеки поддерживают аудио PCM.</span><span class="sxs-lookup"><span data-stu-id="91512-119">The audio codecs support PCM audio.</span></span>

<span data-ttu-id="91512-120">Чтобы перечислить входные форматы, поддерживаемые кодеком, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="91512-120">To enumerate the input formats supported by a codec, perform the following steps:</span></span>

1.  <span data-ttu-id="91512-121">Создайте объект модуля записи и задайте профиль для использования.</span><span class="sxs-lookup"><span data-stu-id="91512-121">Create a writer object and set a profile to use.</span></span> <span data-ttu-id="91512-122">Дополнительные сведения о настройке профилей в средстве записи см. [в разделе Использование профилей с модулем записи](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="91512-122">For more information about setting profiles in the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
2.  <span data-ttu-id="91512-123">Укажите номер входного номера, для которого необходимо проверить форматы.</span><span class="sxs-lookup"><span data-stu-id="91512-123">Identify the input number for which you want to check the formats.</span></span> <span data-ttu-id="91512-124">Дополнительные сведения об идентификации входных номеров см. [в разделе Определение входных данных по номеру](to-identify-inputs-by-number.md).</span><span class="sxs-lookup"><span data-stu-id="91512-124">For more information about identifying input numbers, see [To Identify Inputs By Number](to-identify-inputs-by-number.md).</span></span>
3.  <span data-ttu-id="91512-125">Получите общее число входных форматов, поддерживаемых требуемыми входными данными, вызвав [**ивмвритер:: жетинпутформаткаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount).</span><span class="sxs-lookup"><span data-stu-id="91512-125">Retrieve the total number of input formats supported by the desired input by calling [**IWMWriter::GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount).</span></span>
4.  <span data-ttu-id="91512-126">Выполните цикл по всем поддерживаемым входным форматам, выполнив следующие действия для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="91512-126">Loop through all of the supported input formats, performing the following steps for each.</span></span>
    -   <span data-ttu-id="91512-127">Получите интерфейс [**ивминпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) для входного формата, вызвав [**Ивмвритер:: жетинпутформат**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat).</span><span class="sxs-lookup"><span data-stu-id="91512-127">Retrieve the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input format by calling [**IWMWriter::GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat).</span></span>
    -   <span data-ttu-id="91512-128">Получение структуры [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) для формата входных данных.</span><span class="sxs-lookup"><span data-stu-id="91512-128">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the input format.</span></span> <span data-ttu-id="91512-129">Вызовите метод [**ивммедиапропс:: жетмедиатипе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), передав параметру *птипе* **значение NULL** , чтобы получить размер структуры.</span><span class="sxs-lookup"><span data-stu-id="91512-129">Call [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), passing **NULL** for the *pType* parameter to get the size of the structure.</span></span> <span data-ttu-id="91512-130">Затем выделите память для хранения структуры и снова вызовите **жетмедиатипе** , чтобы получить структуру.</span><span class="sxs-lookup"><span data-stu-id="91512-130">Then allocate memory to hold the structure and call **GetMediaType** again to get the structure.</span></span> <span data-ttu-id="91512-131">[**Ивминпутмедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) наследует от [**ивммедиапропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops), поэтому можно выполнять вызовы **жетмедиатипе** из экземпляра **ивминпутмедиапропс** , полученного на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="91512-131">[**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) inherits from [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops), so you can make the calls to **GetMediaType** from the instance of **IWMInputMediaProps** retrieved in the previous step.</span></span>
    -   <span data-ttu-id="91512-132">Формат, описанный в разделе Структура [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) , содержит все необходимые сведения о формате входных данных.</span><span class="sxs-lookup"><span data-stu-id="91512-132">The format described in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure contains all of the pertinent information about the input format.</span></span> <span data-ttu-id="91512-133">Базовый формат носителя определяется с помощью **WM \_ Media \_ Type.** подтип.</span><span class="sxs-lookup"><span data-stu-id="91512-133">The basic format of the media is identified by **WM\_MEDIA\_TYPE.subtype**.</span></span> <span data-ttu-id="91512-134">Для видеопотоков элемент **пбформат** указывает на динамически выделенную структуру [**вмвидеоинфохеадер**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) , которая содержит дополнительные сведения о потоке, включая размер прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="91512-134">For video streams, the **pbFormat** member points to a dynamically allocated [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) structure which contains further details about the stream, including rectangle size.</span></span> <span data-ttu-id="91512-135">Размер входных кадров не обязательно должен точно соответствовать размеру, поддерживаемому кодеком.</span><span class="sxs-lookup"><span data-stu-id="91512-135">The size of the input frames is not required to match exactly a size supported by the codec.</span></span> <span data-ttu-id="91512-136">Если они не совпадают, компоненты времени выполнения пакета SDK, во многих случаях, автоматически изменяют размер входных видеокадров на то, что может принимать кодек.</span><span class="sxs-lookup"><span data-stu-id="91512-136">If they do not match, the SDK run-time components, in many cases, will automatically resize the input video frames to something the codec can accept.</span></span>

<span data-ttu-id="91512-137">В следующем примере кода выполняется поиск входного формата подтипа, переданного в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="91512-137">The following example code finds the input format of the subtype passed as a parameter.</span></span> <span data-ttu-id="91512-138">Дополнительные сведения об использовании этого кода см. [в разделе Использование примеров кода](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="91512-138">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT FindInputFormat(IWMWriter* pWriter, 
                       DWORD dwInput,
                       GUID guidSubType,
                       IWMInputMediaProps** ppProps)
{
    DWORD   cFormats = 0;
    DWORD   cbSize   = 0;

    WM_MEDIA_TYPE*      pType  = NULL;
    IWMInputMediaProps* pProps = NULL;

    // Set the ppProps parameter to point to NULL. This will
    //  be used to check the results of the function later.
    *ppProps = NULL;

    // Find the number of formats supported by this input.
    HRESULT hr = pWriter->GetInputFormatCount(dwInput, &cFormats);
    if (FAILED(hr))
    {
        goto Exit;
    }
    // Loop through all of the supported formats.
    for (DWORD formatIndex = 0; formatIndex < cFormats; formatIndex++)
    {
        // Get the input media properties for the input format.
        hr = pWriter->GetInputFormat(dwInput, formatIndex, &pProps);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Get the size of the media type structure.
        hr = pProps->GetMediaType(NULL, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Allocate memory for the media type structure.
        pType = (WM_MEDIA_TYPE*) new (std::nothrow) BYTE[cbSize];
        if (pType == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }
        
        // Get the media type structure.
        hr = pProps->GetMediaType(pType, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }

        if(pType->subtype == guidSubType)
        {
            *ppProps = pProps;
            (*ppProps)->AddRef();
            goto Exit;
        }

        // Clean up for next iteration.
        delete [] pType;
        pType = NULL;
        SAFE_RELEASE(pProps);
    } // End for formatIndex.

    // If execution made it to this point, no matching format was found.
    hr = NS_E_INVALID_INPUT_FORMAT;

Exit:
    delete [] pType;
    SAFE_RELEASE(pProps);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="91512-139">См. также</span><span class="sxs-lookup"><span data-stu-id="91512-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91512-140">**Интерфейс Ивмвритер**</span><span class="sxs-lookup"><span data-stu-id="91512-140">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="91512-141">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="91512-141">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




