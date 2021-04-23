---
title: Обнаружение формата файла
description: Обнаружение формата файла
ms.assetid: f1b3f811-8161-41ca-a92c-2735c0bec2e8
keywords:
- Диспетчер устройств Windows Media, форматы файлов
- Диспетчер устройств, форматы файлов
- инструкции по программированию, форматы файлов
- Классические приложения, форматы файлов
- Создание приложений диспетчер устройств Windows Media, форматы файлов
- запись файлов на устройства, форматы файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b06c963b01e3b681fd078d8685e1c788c73352e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775239"
---
# <a name="discovering-a-files-format"></a><span data-ttu-id="f96a5-109">Обнаружение формата файла</span><span class="sxs-lookup"><span data-stu-id="f96a5-109">Discovering a File's Format</span></span>

<span data-ttu-id="f96a5-110">Перед отправкой файла на устройство приложение должно определить, поддерживает ли устройство Этот формат файлов.</span><span class="sxs-lookup"><span data-stu-id="f96a5-110">Before sending a file to the device, an application should determine whether the device supports that file format.</span></span>

<span data-ttu-id="f96a5-111">Обнаружение формата файла может быть сложным.</span><span class="sxs-lookup"><span data-stu-id="f96a5-111">Discovering the format of a file can be complex.</span></span> <span data-ttu-id="f96a5-112">Самый простой способ — создать список расширений файлов, сопоставленных с конкретными \_ значениями ПЕРЕЧИСЛЕНИЯ вмдм форматкоде.</span><span class="sxs-lookup"><span data-stu-id="f96a5-112">The simplest way is to create a list of file extensions mapped to specific WMDM\_FORMATCODE enumeration values.</span></span> <span data-ttu-id="f96a5-113">Однако существует несколько проблем с этой системой: одна из них состоит в том, что один формат может иметь несколько расширений (например, JPG, jpe и JPEG для изображений JPEG).</span><span class="sxs-lookup"><span data-stu-id="f96a5-113">However, there are a few problems with this system: one is that a single format can have multiple extensions (such as .jpg, .jpe, and .jpeg for JPEG images).</span></span> <span data-ttu-id="f96a5-114">Кроме того, одно и то же расширение файла может использоваться различными программами в различных форматах.</span><span class="sxs-lookup"><span data-stu-id="f96a5-114">Also, the same file extension can be used by different programs for different formats.</span></span>

<span data-ttu-id="f96a5-115">Чтобы преодолеть ограничения относительного сопоставления, приложение лучше проверить, соответствует ли формат расширению.</span><span class="sxs-lookup"><span data-stu-id="f96a5-115">To overcome the limitations of a strict mapping, it is best for an application to verify that the format matches the extension.</span></span> <span data-ttu-id="f96a5-116">Пакет SDK для DirectShow предоставляет средства, позволяющие приложению обнаруживать ограниченный набор сведений о большинстве типов файлов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f96a5-116">The DirectShow SDK provides tools that enable an application to discover a limited set of details about most media file types.</span></span> <span data-ttu-id="f96a5-117">Пакет SDK для формата Windows Media предоставляет большое количество сведений, но только файлы ASF.</span><span class="sxs-lookup"><span data-stu-id="f96a5-117">The Windows Media Format SDK exposes a large number of details, but only about ASF files.</span></span> <span data-ttu-id="f96a5-118">Так как для всех типов файлов должен быть проверен код формата, по возможности рекомендуется использовать DirectShow для обнаружения или проверки основного кода формата, а также использовать пакет SDK Windows Media Format для обнаружения дополнительных метаданных, необходимых для файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="f96a5-118">Because all file types should have their format code verified if possible, it is therefore best to use DirectShow to discover or verify the basic format code, and use the Windows Media Format SDK to discover any additional metadata desired about ASF files.</span></span> <span data-ttu-id="f96a5-119">Кроме того, DirectShow можно использовать для обнаружения базовых метаданных для файлов, отличных от ASF.</span><span class="sxs-lookup"><span data-stu-id="f96a5-119">DirectShow can also be used to discover basic metadata for non-ASF files.</span></span>

<span data-ttu-id="f96a5-120">Ниже приведен один из способов обнаружения формата файлов с помощью сопоставления расширений и DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f96a5-120">The following is one way to discover a file format using extension mapping and DirectShow.</span></span>

<span data-ttu-id="f96a5-121">Сначала Сравните расширение имени файла со списком известных расширений.</span><span class="sxs-lookup"><span data-stu-id="f96a5-121">First, compare the file name extension to a list of known extensions.</span></span> <span data-ttu-id="f96a5-122">Не забудьте выполнить сравнение без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="f96a5-122">Be sure to make your comparison case-insensitive.</span></span> <span data-ttu-id="f96a5-123">Если расширение не сопоставлено, присвойте формату значение ВМДМ \_ форматкоде \_ undefine.</span><span class="sxs-lookup"><span data-stu-id="f96a5-123">If the extension is not mapped, set the format to WMDM\_FORMATCODE\_UNDEFINED.</span></span>

-   <span data-ttu-id="f96a5-124">Если код формата не был найден (или вы хотите убедиться, что файл является файлом мультимедиа), можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f96a5-124">If the format code was not found (or you want to verify that a file is a media file), you can perform the following steps:</span></span>
    1.  <span data-ttu-id="f96a5-125">Создайте объект детектора мультимедиа DirectShow, используя **CoCreateInstance**(CLSID \_ медиадет) и извлекая интерфейс **имедиадет** .</span><span class="sxs-lookup"><span data-stu-id="f96a5-125">Create a DirectShow Media Detector object using **CoCreateInstance**(CLSID\_MediaDet), and retrieving the **IMediaDet** interface.</span></span>
    2.  <span data-ttu-id="f96a5-126">Откройте файл, вызвав **имедиадет::p UT \_ filename**.</span><span class="sxs-lookup"><span data-stu-id="f96a5-126">Open the file by calling **IMediaDet::put\_Filename**.</span></span> <span data-ttu-id="f96a5-127">Этот вызов завершится ошибкой, если файл защищен.</span><span class="sxs-lookup"><span data-stu-id="f96a5-127">This call will fail if the file is protected.</span></span>
    3.  <span data-ttu-id="f96a5-128">Получите тип мультимедиа потока по умолчанию, вызвав метод **имедиадет:: Get \_ стреаммедиатипе**, который возвращает **\_ \_ Тип файла AM**.</span><span class="sxs-lookup"><span data-stu-id="f96a5-128">Get the media type of the default stream by calling **IMediaDet::get\_StreamMediaType**, which returns an **AM\_MEDIA\_TYPE**.</span></span>
    4.  <span data-ttu-id="f96a5-129">Получите количество потоков, вызвав метод **имедиадет:: Get \_ аутпутстреамс**.</span><span class="sxs-lookup"><span data-stu-id="f96a5-129">Get the number of streams by calling **IMediaDet::get\_OutputStreams**.</span></span>
        -   <span data-ttu-id="f96a5-130">Если имеется только один поток, и он является звуком, то файл имеет тип ВМДМ \_ форматкоде \_ ундефинедаудио</span><span class="sxs-lookup"><span data-stu-id="f96a5-130">If there is only one stream and it is audio, the file type is WMDM\_FORMATCODE\_UNDEFINEDAUDIO</span></span>
        -   <span data-ttu-id="f96a5-131">Если имеется только один поток и видео, то файл имеет тип ВМДМ \_ форматкоде \_ ундефинедвидео</span><span class="sxs-lookup"><span data-stu-id="f96a5-131">If there is only one stream and it is video, the file type is WMDM\_FORMATCODE\_UNDEFINEDVIDEO</span></span>
        -   <span data-ttu-id="f96a5-132">Если имеется только один поток, и это видео, а скорость потока равна нулю, то файл имеет тип ВМДМ \_ форматкоде \_ виндовсимажеформат.</span><span class="sxs-lookup"><span data-stu-id="f96a5-132">If there is only one stream and it is video and the bit rate is zero, the file type is WMDM\_FORMATCODE\_WINDOWSIMAGEFORMAT.</span></span>

<span data-ttu-id="f96a5-133">Вы также можете попробовать найти соответствующие аудио или видеокодеки из членов **видеоинфохеадер** или **вавеформатекс** , полученных из **Get \_ стреаммедиатипе**.</span><span class="sxs-lookup"><span data-stu-id="f96a5-133">You could also try matching audio or video codecs from the **VIDEOINFOHEADER** or **WAVEFORMATEX** members retrieved from **get\_StreamMediaType**.</span></span>

<span data-ttu-id="f96a5-134">Следующая функция C++ демонстрирует сопоставление расширений файлов и использование DirectShow для анализа неизвестных файлов.</span><span class="sxs-lookup"><span data-stu-id="f96a5-134">The following C++ function demonstrates file extension matching and using DirectShow to try to analyze unknown files.</span></span>


```C++
// For IMediaDet, you must link to strmiids.lib. Also include the following:
//#include <Qedit.h>  // for IMediaDet declaration.
//#include <Dshow.h>  // for VIDEOINFOHEADER declaration.
WMDM_FORMATCODE CWMDMController::myGetWMDM_FORMATCODE(LPCWSTR pFileName)
{
    HRESULT hr = S_OK;

    // Declare the variable to hold the WMDM format code.
    WMDM_FORMATCODE fmt = WMDM_FORMATCODE_UNDEFINED;
    
    // Get the file extension.
    wstring ext = pFileName;
    ext = ext.substr(ext.find_last_of(L".") + 1);

    // This is not an exhaustive list. 
    // It is also case-sensitive.
    if (ext == L"js" || ext == L"vb")
        fmt = WMDM_FORMATCODE_SCRIPT;
    else if (ext == L".exe")
        fmt = WMDM_FORMATCODE_EXECUTABLE;
    else if (ext == L"txt")
        fmt = WMDM_FORMATCODE_TEXT;
    else if (ext == L"html" || ext == L"htm" || ext == L"shtm")
        fmt = WMDM_FORMATCODE_HTML;
    else if (ext == L"aiff")
        fmt = WMDM_FORMATCODE_AIFF;
    else if (ext == L"wav")
        fmt = WMDM_FORMATCODE_WAVE;
    else if (ext == L"mp3")
        fmt = WMDM_FORMATCODE_MP3;
    else if (ext == L"mpg" || ext == L"mpeg" || ext == L"mp2")
        fmt = WMDM_FORMATCODE_MPEG;
    else if (ext == L"bmp")
        fmt = WMDM_FORMATCODE_IMAGE_BMP;
    else if (ext == L"avi")
        fmt = WMDM_FORMATCODE_AVI;
    else if (ext == L"asf")
        fmt = WMDM_FORMATCODE_ASF;
    else if (ext == L"tif")
        fmt = WMDM_FORMATCODE_IMAGE_TIFF;
    else if (ext == L"gif")
        fmt = WMDM_FORMATCODE_IMAGE_GIF;
    else if (ext == L"pct")
        fmt = WMDM_FORMATCODE_IMAGE_PICT;
    else if (ext == L"png")
        fmt = WMDM_FORMATCODE_IMAGE_PNG;
    else if (ext == L"wma")
        fmt = WMDM_FORMATCODE_WMA;
    else if (ext == L"wpl")
        fmt = WMDM_FORMATCODE_WPLPLAYLIST;
    else if (ext == L"asx")
        fmt = WMDM_FORMATCODE_ASXPLAYLIST;
    else if (ext == L"m3u")
        fmt = WMDM_FORMATCODE_M3UPLAYLIST;
    else if (ext == L"wmv")
        fmt = WMDM_FORMATCODE_WMV;
    else if (ext == L"jpg" || ext == L"jpeg" || ext == L"jpe")
        fmt = WMDM_FORMATCODE_IMAGE_EXIF;
    else if (ext == L"jp2")
        fmt = WMDM_FORMATCODE_IMAGE_JP2;
    else if (ext == L"jpx" || ext == L"jpf")
        fmt = WMDM_FORMATCODE_IMAGE_JPX;

    // If we couldn't get the type from the extension, perhaps DirectShow 
    // can determine the type. You could also modify this to verify that 
    // the major media type matches the file extension (for example, that 
    // a .gif file has a video image stream with a bit rate of zero).
    if (fmt == WMDM_FORMATCODE_UNDEFINED)
    {
        CComPtr<IMediaDet> pIMediaDet;
        hr = pIMediaDet.CoCreateInstance(CLSID_MediaDet, NULL);
        if (hr == S_OK && pIMediaDet != NULL)
        {
            hr = pIMediaDet->put_Filename(BSTR(pFileName));
            if (FAILED(hr)) return WMDM_FORMATCODE_UNDEFINED;

            AM_MEDIA_TYPE mediaType;
            if (hr == S_OK)
            {
                hr = pIMediaDet->get_StreamMediaType(&mediaType);
                CHECK_HR(hr, 
                  "get_StreamMediaType succeeded in myGetWMDM_FORMATCODE.", 
                  "get_StreamMediaType failed in myGetWMDM_FORMATCODE.");
            }

            if (hr == S_OK)
            {
                LONG numStreams = 0;
                hr = pIMediaDet->get_OutputStreams(&numStreams);

                // If there is at least one video stream, the file is video. 
                // If there are only audio streams, it is audio.
                // Loop through all streams or until first video stream is found.
                for (int i = 0; i < numStreams; i++)
                {
                    // Choices are either VIDEOINFOHEADER or WAVEFORMATEX. 
                    // VIDEOINFOHEADER2 is not supported.
                    if (IsEqualGUID(mediaType.formattype, 
                        FORMAT_VideoInfo))
                    {
                        VIDEOINFOHEADER* data = 
                            (VIDEOINFOHEADER*) mediaType.pbFormat;

                        // If only one stream and there was no matching 
                        // extension, it is undefined video. If no 
                        // bit rate, it's a still image.
                        if (data->dwBitRate == 0) fmt = 
                            WMDM_FORMATCODE_WINDOWSIMAGEFORMAT;
                        else fmt = WMDM_FORMATCODE_UNDEFINEDVIDEO;
                        break; // Found video--any additional streams are soundtracks.
                    }
                    if (IsEqualGUID(mediaType.formattype, FORMAT_WaveFormatEx))
                    {
                        // If only one stream and there was no matching 
                        // extension, it is undefined audio. 
                        if (fmt == WMDM_FORMATCODE_UNDEFINED)
                        {
                            fmt = WMDM_FORMATCODE_UNDEFINEDAUDIO;
                        }
                        WAVEFORMATEX* data = 
                            (WAVEFORMATEX*) mediaType.pbFormat;
                    }
                } // Loop through streams.
            }     // Got a stream media type.
        }         // Created a media detector object.
    }
    return fmt;
}
```



## <a name="related-topics"></a><span data-ttu-id="f96a5-135">См. также</span><span class="sxs-lookup"><span data-stu-id="f96a5-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f96a5-136">**Запись файлов на устройство**</span><span class="sxs-lookup"><span data-stu-id="f96a5-136">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




