---
description: Настройка формата вывода видео
ms.assetid: 1969072e-575e-49b4-88db-4c7e7a5a1c37
title: Настройка формата вывода видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d09ac64d7f43e6c39377277544867491a93a6f3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104556989"
---
# <a name="configure-the-video-output-format"></a><span data-ttu-id="4e51a-103">Настройка формата вывода видео</span><span class="sxs-lookup"><span data-stu-id="4e51a-103">Configure the Video Output Format</span></span>

> [!Note]  
> <span data-ttu-id="4e51a-104">Функциональные возможности, описанные в этом разделе, являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="4e51a-104">The functionality described in this topic is deprecated.</span></span> <span data-ttu-id="4e51a-105">Чтобы настроить выходной формат устройства записи, приложение должно использовать структуру [**\_ \_ типа данных AM Media**](/windows/win32/api/strmif/ns-strmif-am_media_type) , возвращенную функцией [**иамстреамконфиг::-Format**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) в параметре *ПЛТ* .</span><span class="sxs-lookup"><span data-stu-id="4e51a-105">To configure a capture device's output format, an application should use the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure returned by [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) in the *pmt* parameter.</span></span>

 

<span data-ttu-id="4e51a-106">Устройство записи может поддерживать диапазон выходных форматов.</span><span class="sxs-lookup"><span data-stu-id="4e51a-106">A capture device can support a range of output formats.</span></span> <span data-ttu-id="4e51a-107">Например, устройство может поддерживать 16-разрядный RGB, 32-разрядный RGB и ЮИВ.</span><span class="sxs-lookup"><span data-stu-id="4e51a-107">For example, a device might support 16-bit RGB, 32-bit RGB, and YUYV.</span></span> <span data-ttu-id="4e51a-108">В каждом из этих форматов устройство может поддерживать диапазон размеров кадров.</span><span class="sxs-lookup"><span data-stu-id="4e51a-108">Within each of these formats, the device can support a range of frame sizes.</span></span>

<span data-ttu-id="4e51a-109">В устройстве WDM интерфейс [**иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) используется для сообщения о том, какие форматы поддерживает устройство, и для задания формата.</span><span class="sxs-lookup"><span data-stu-id="4e51a-109">In a WDM device, the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface is used to report which formats the device supports, and to set the format.</span></span> <span data-ttu-id="4e51a-110">(Для устаревших устройств VFW используйте диалоговое окно VFW в формате видео, как описано в разделе [Отображение диалоговых окон VFW Capture](display-vfw-capture-dialog-boxes.md).) Интерфейс **иамстреамконфиг** предоставляется на ПИН-коде записи фильтра записи, предварительный просмотр ПИН-кода или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="4e51a-110">(For legacy VFW devices, use the Video Format VFW dialog box, as described in [Display VFW Capture Dialog Boxes](display-vfw-capture-dialog-boxes.md).) The **IAMStreamConfig** interface is exposed on the capture filter's capture pin, preview pin, or both.</span></span> <span data-ttu-id="4e51a-111">Чтобы получить указатель интерфейса, используйте метод [**ICaptureGraphBuilder2:: финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) :</span><span class="sxs-lookup"><span data-stu-id="4e51a-111">Use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to get the interface pointer:</span></span>


```C++
IAMStreamConfig *pConfig = NULL;
hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, // Preview pin.
    0,    // Any media type.
    pCap, // Pointer to the capture filter.
    IID_IAMStreamConfig, (void**)&pConfig);
```



<span data-ttu-id="4e51a-112">Устройство имеет список поддерживаемых типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4e51a-112">The device has a list of media types that it supports.</span></span> <span data-ttu-id="4e51a-113">Для каждого типа носителя устройство также предоставляет набор возможностей.</span><span class="sxs-lookup"><span data-stu-id="4e51a-113">For each media type, the device also provides a set of capabilities.</span></span> <span data-ttu-id="4e51a-114">К ним относятся диапазон размеров кадров, доступных для этого формата, то, насколько хорошо устройство может растянуть или сжать изображение, а также диапазон частот кадров.</span><span class="sxs-lookup"><span data-stu-id="4e51a-114">These include the range of frame sizes that are available for that format, how well the device can stretch or shrink the image, and the range of frame rates.</span></span>

<span data-ttu-id="4e51a-115">Чтобы получить количество типов мультимедиа, вызовите метод [**иамстреамконфиг:: жетнумберофкапабилитиес**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="4e51a-115">To get the number of media types, call the [**IAMStreamConfig::GetNumberOfCapabilities**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities) method.</span></span> <span data-ttu-id="4e51a-116">Метод возвращает два значения:</span><span class="sxs-lookup"><span data-stu-id="4e51a-116">The method returns two values:</span></span>

-   <span data-ttu-id="4e51a-117">Число типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4e51a-117">The number of media types.</span></span>
-   <span data-ttu-id="4e51a-118">Размер структуры, содержащей сведения о возможностях.</span><span class="sxs-lookup"><span data-stu-id="4e51a-118">The size of the structure that holds the capabilities information.</span></span>

<span data-ttu-id="4e51a-119">Значение размера необходимо, так как интерфейс [**иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) используется как для аудио, так и для видео (и может быть расширен для других типов мультимедиа).</span><span class="sxs-lookup"><span data-stu-id="4e51a-119">The size value is necessary because the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface is used for both audio and video (and could be extended to other media types).</span></span> <span data-ttu-id="4e51a-120">Для видео возможности описываются с помощью структуры " [**\_ \_ \_ заглушки конфигурации видеопотока**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) ", а в Audio используется структура [**\_ \_ \_ CAPS в конфигурации**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="4e51a-120">For video, the capabilities are described using the [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure, while audio uses the [**AUDIO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) structure.</span></span>

<span data-ttu-id="4e51a-121">Чтобы перечислить типы мультимедиа, вызовите метод [**иамстреамконфиг:: жетстреамкапс**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) с индексом, начинающимся с нуля.</span><span class="sxs-lookup"><span data-stu-id="4e51a-121">To enumerate the media types, call the [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method with a zero-based index.</span></span> <span data-ttu-id="4e51a-122">Метод **жетстреамкапс** Возвращает тип мультимедиа и соответствующую структуру возможностей:</span><span class="sxs-lookup"><span data-stu-id="4e51a-122">The **GetStreamCaps** method returns a media type and the corresponding capability structure:</span></span>


```C++
int iCount = 0, iSize = 0;
hr = pConfig->GetNumberOfCapabilities(&iCount, &iSize);

// Check the size to make sure we pass in the correct structure.
if (iSize == sizeof(VIDEO_STREAM_CONFIG_CAPS))
{
    // Use the video capabilities structure.

    for (int iFormat = 0; iFormat < iCount; iFormat++)
    {
        VIDEO_STREAM_CONFIG_CAPS scc;
        AM_MEDIA_TYPE *pmtConfig;
        hr = pConfig->GetStreamCaps(iFormat, &pmtConfig, (BYTE*)&scc);
        if (SUCCEEDED(hr))
        {
            /* Examine the format, and possibly use it. */

            // Delete the media type when you are done.
            DeleteMediaType(pmtConfig);
        }
}
```



<span data-ttu-id="4e51a-123">Обратите внимание на то, как распределяются структуры для метода [**жетстреамкапс**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) .</span><span class="sxs-lookup"><span data-stu-id="4e51a-123">Note how the structures are allocated for the [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method.</span></span> <span data-ttu-id="4e51a-124">Метод выделяет структуру типа мультимедиа, в то время как вызывающий объект выделяет структуру возможностей.</span><span class="sxs-lookup"><span data-stu-id="4e51a-124">The method allocates the media type structure, whereas the caller allocates the capabilities structure.</span></span> <span data-ttu-id="4e51a-125">Приведение структуры возможностей к указателю массива байтов.</span><span class="sxs-lookup"><span data-stu-id="4e51a-125">Coerce the capabilities structure to a byte array pointer.</span></span> <span data-ttu-id="4e51a-126">После завершения работы с типом мультимедиа удалите структуру [**\_ \_ типа файлов мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , а также блок формата типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4e51a-126">After you are done with the media type, delete the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, along with the media type's format block.</span></span>

<span data-ttu-id="4e51a-127">Можно настроить устройство для использования формата, возвращаемого методом [**жетстреамкапс**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) .</span><span class="sxs-lookup"><span data-stu-id="4e51a-127">You can configure the device to use a format returned in the [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method.</span></span> <span data-ttu-id="4e51a-128">Просто вызовите [**иамстреамконфиг:: сетформат**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) с типом мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="4e51a-128">Simply call [**IAMStreamConfig::SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) with the media type:</span></span>


```C++
hr = pConfig->SetFormat(pmtConfig);
```



<span data-ttu-id="4e51a-129">Если ПИН-код не подключен, будет предпринята попытка использовать этот формат при подключении.</span><span class="sxs-lookup"><span data-stu-id="4e51a-129">If the pin is not connected, it will attempt to use this format when it does connect.</span></span> <span data-ttu-id="4e51a-130">Если ПИН-код уже подключен, он пытается подключиться с помощью нового формата.</span><span class="sxs-lookup"><span data-stu-id="4e51a-130">If the pin is already connected, it attempts to reconnect using the new format.</span></span> <span data-ttu-id="4e51a-131">В любом случае возможно, что нисходящий фильтр отклонит формат.</span><span class="sxs-lookup"><span data-stu-id="4e51a-131">In either case, it is possible that the downstream filter will reject the format.</span></span>

<span data-ttu-id="4e51a-132">Кроме того, можно изменить тип носителя перед его передачей методу [**сетформат**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) .</span><span class="sxs-lookup"><span data-stu-id="4e51a-132">You can also modify the media type before passing it to the [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) method.</span></span> <span data-ttu-id="4e51a-133">Именно в этом случае используется структура [**\_ \_ \_ CAPS в конфигурации потока видео**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) .</span><span class="sxs-lookup"><span data-stu-id="4e51a-133">This is where the [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure comes in.</span></span> <span data-ttu-id="4e51a-134">В нем описываются все допустимые способы изменения типа носителя.</span><span class="sxs-lookup"><span data-stu-id="4e51a-134">It describes all of the valid ways to change the media type.</span></span> <span data-ttu-id="4e51a-135">Чтобы использовать эти сведения, необходимо ознакомиться с подробными сведениями о конкретном типе носителя.</span><span class="sxs-lookup"><span data-stu-id="4e51a-135">To use this information, you must understand the details of that particular media type.</span></span>

<span data-ttu-id="4e51a-136">Например, предположим, что [**жетстреамкапс**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) возвращает 24-битный формат RGB с размером кадра 320 x 240 пикселей.</span><span class="sxs-lookup"><span data-stu-id="4e51a-136">For example, suppose that [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) returns a 24-bit RGB format, with a frame size of 320 x 240 pixels.</span></span> <span data-ttu-id="4e51a-137">Эти сведения можно получить, изучив основной тип, подтип и блок формата типа мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="4e51a-137">You can get this information by examining the major type, subtype, and format block of the media type:</span></span>


```C++
if ((pmtConfig.majortype == MEDIATYPE_Video) &&
    (pmtConfig.subtype == MEDIASUBTYPE_RGB24) &&
    (pmtConfig.formattype == FORMAT_VideoInfo) &&
    (pmtConfig.cbFormat >= sizeof (VIDEOINFOHEADER)) &&
    (pmtConfig.pbFormat != NULL))
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)pmtConfig.pbFormat;
    // pVih contains the detailed format information.
    LONG lWidth = pVih->bmiHeader.biWidth;
    LONG lHeight = pVih->bmiHeader.biHeight;
}
```



<span data-ttu-id="4e51a-138">Структура [**\_ \_ \_ Caps config в конфигурации потока видео**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) предоставляет минимальную и максимальную ширину и высоту, которые можно использовать для этого типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4e51a-138">The [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure gives the minimum and maximum width and height that can be used for this media type.</span></span> <span data-ttu-id="4e51a-139">Он также дает «шаг», который определяет приращение, на которое можно изменить ширину или высоту.</span><span class="sxs-lookup"><span data-stu-id="4e51a-139">It also gives you the "step" size, which defines the increments by which you can adjust the width or height.</span></span> <span data-ttu-id="4e51a-140">Например, устройство может вернуть следующее:</span><span class="sxs-lookup"><span data-stu-id="4e51a-140">For example, the device might return the following:</span></span>

-   <span data-ttu-id="4e51a-141">Минаутпутсизе: 160 x 120</span><span class="sxs-lookup"><span data-stu-id="4e51a-141">MinOutputSize: 160 x 120</span></span>
-   <span data-ttu-id="4e51a-142">Максаутпутсизе: 320 x 240</span><span class="sxs-lookup"><span data-stu-id="4e51a-142">MaxOutputSize: 320 x 240</span></span>
-   <span data-ttu-id="4e51a-143">Аутпутгрануларитикс: 8 пикселей (горизонтальный размер шага)</span><span class="sxs-lookup"><span data-stu-id="4e51a-143">OutputGranularityX: 8 pixels (horizontal step size)</span></span>
-   <span data-ttu-id="4e51a-144">Аутпутгрануларитии: 8 пикселей (вертикальный размер шага)</span><span class="sxs-lookup"><span data-stu-id="4e51a-144">OutputGranularityY: 8 pixels (vertical step size)</span></span>

<span data-ttu-id="4e51a-145">Учитывая эти числа, можно установить ширину для любого значения в диапазоне (160, 168, 176,... 304, 312, 320) и высота по всем значениям в диапазоне (120, 128, 136,... 104, 112, 120).</span><span class="sxs-lookup"><span data-stu-id="4e51a-145">Given these numbers, you could set the width to anything in the range (160, 168, 176, ... 304, 312, 320) and the height to anything in the range (120, 128, 136, ... 104, 112, 120).</span></span> <span data-ttu-id="4e51a-146">Этот процесс представлен на схеме ниже.</span><span class="sxs-lookup"><span data-stu-id="4e51a-146">The following diagram illustrates this process.</span></span>

![Размеры видеоформатов](images/strmcap3.png)

<span data-ttu-id="4e51a-148">Чтобы задать новый размер кадра, непосредственно измените структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , возвращаемую в [**жетстреамкапс**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps):</span><span class="sxs-lookup"><span data-stu-id="4e51a-148">To set a new frame size, directly modify the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure returned in [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps):</span></span>


```C++
pVih->bmiHeader.biWidth = 160;
pVih->bmiHeader.biHeight = 120;
pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader);
```



<span data-ttu-id="4e51a-149">Затем передайте тип мультимедиа методу [**сетформат**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) , как описано выше.</span><span class="sxs-lookup"><span data-stu-id="4e51a-149">Then pass the media type to the [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) method, as described previously.</span></span>

<span data-ttu-id="4e51a-150">Элементы **минфрамеинтервал** и **максфрамеинтервал** с [**\_ \_ \_ ограничениями конфигурации видеопотока**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) — это минимальная и максимальная длина каждого кадра видео, которую можно преобразовать в частоту кадров следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4e51a-150">The **MinFrameInterval** and **MaxFrameInterval** members of [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) are the minimum and maximum length of each video frame, which you can translate into frame rates as follows:</span></span>

`frames per second = 10,000,000 / frame duration`

<span data-ttu-id="4e51a-151">Чтобы запросить определенную частоту кадров, измените значение **авгтимеперфраме** в структуре [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) или [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) в типе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4e51a-151">To request a particular frame rate, modify the value of **AvgTimePerFrame** in the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure in the media type.</span></span> <span data-ttu-id="4e51a-152">Устройство может не поддерживать все возможные значения между минимальным и максимальным значениями, поэтому драйвер будет использовать ближайшее значение, которое это возможно.</span><span class="sxs-lookup"><span data-stu-id="4e51a-152">The device may not support every possible value between the minimum and maximum, so the driver will use the closest value that it can.</span></span> <span data-ttu-id="4e51a-153">Чтобы узнать, какое значение использует драйвер, вызовите [**иамстреамконфиг::**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) сетформат после вызова [](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat).</span><span class="sxs-lookup"><span data-stu-id="4e51a-153">To see what value the driver actually used, call [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) after you call [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat).</span></span>

<span data-ttu-id="4e51a-154">Некоторые драйверы могут сообщать **макслонглонг** (0x7FFFFFFFFFFFFFFF) о значении **максфрамеинтервал**, что фактически означает отсутствие максимальной длительности.</span><span class="sxs-lookup"><span data-stu-id="4e51a-154">Some drivers may report **MAXLONGLONG** (0x7FFFFFFFFFFFFFFF) for the value of **MaxFrameInterval**, which in effect means there is no maximum duration.</span></span> <span data-ttu-id="4e51a-155">Однако может потребоваться принудительно применить минимальную частоту кадров в приложении, например 1 кадр/с.</span><span class="sxs-lookup"><span data-stu-id="4e51a-155">However, you might want to enforce a minimum frame rate in your application, such as 1 fps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e51a-156">См. также</span><span class="sxs-lookup"><span data-stu-id="4e51a-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e51a-157">О типах носителей</span><span class="sxs-lookup"><span data-stu-id="4e51a-157">About Media Types</span></span>](about-media-types.md)
</dt> <dt>

[<span data-ttu-id="4e51a-158">Настройка устройства видеозаписи</span><span class="sxs-lookup"><span data-stu-id="4e51a-158">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



