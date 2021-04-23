---
description: В этом учебнике показано, как использовать API перекодировки для кодирования файла MP4 с помощью H. 264 для видеопотока и AAC для аудиопотока.
ms.assetid: 60873aa6-46ec-4a73-94b9-0d8ac602f850
title: Учебник. Кодирование файла MP4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae895ef321b35f080bf946384ee32d83c2c539fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263888"
---
# <a name="tutorial-encoding-an-mp4-file"></a><span data-ttu-id="cd021-103">Учебник. Кодирование файла MP4</span><span class="sxs-lookup"><span data-stu-id="cd021-103">Tutorial: Encoding an MP4 File</span></span>

<span data-ttu-id="cd021-104">В этом учебнике показано, как использовать [API](transcode-api.md) перекодировки для кодирования файла MP4 с помощью H. 264 для видеопотока и AAC для аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="cd021-104">This tutorial shows how to use the [Transcode API](transcode-api.md) to encode an MP4 file, using H.264 for the video stream and AAC for the audio stream.</span></span>

-   [<span data-ttu-id="cd021-105">Файлы заголовков и библиотек</span><span class="sxs-lookup"><span data-stu-id="cd021-105">Headers and Library Files</span></span>](#headers-and-library-files)
-   [<span data-ttu-id="cd021-106">Определение профилей кодирования</span><span class="sxs-lookup"><span data-stu-id="cd021-106">Define the Encoding Profiles</span></span>](#define-the-encoding-profiles)
-   [<span data-ttu-id="cd021-107">Написание функции wmain</span><span class="sxs-lookup"><span data-stu-id="cd021-107">Write the wmain Function</span></span>](#write-the-wmain-function)
-   [<span data-ttu-id="cd021-108">Кодирование файла</span><span class="sxs-lookup"><span data-stu-id="cd021-108">Encode the File</span></span>](#encode-the-file)
    -   [<span data-ttu-id="cd021-109">Создание источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="cd021-109">Create the Media Source</span></span>](#create-the-media-source)
    -   [<span data-ttu-id="cd021-110">Получить длительность источника</span><span class="sxs-lookup"><span data-stu-id="cd021-110">Get the Source Duration</span></span>](#get-the-source-duration)
    -   [<span data-ttu-id="cd021-111">Создание профиля перекодирования</span><span class="sxs-lookup"><span data-stu-id="cd021-111">Create the Transcode Profile</span></span>](#create-the-transcode-profile)
    -   [<span data-ttu-id="cd021-112">Запуск сеанса кодирования</span><span class="sxs-lookup"><span data-stu-id="cd021-112">Run the Encoding Session</span></span>](#run-the-encoding-session)
-   [<span data-ttu-id="cd021-113">Вспомогательный модуль сеанса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="cd021-113">Media Session Helper</span></span>](#media-session-helper)
-   [<span data-ttu-id="cd021-114">См. также</span><span class="sxs-lookup"><span data-stu-id="cd021-114">Related topics</span></span>](#related-topics)

## <a name="headers-and-library-files"></a><span data-ttu-id="cd021-115">Файлы заголовков и библиотек</span><span class="sxs-lookup"><span data-stu-id="cd021-115">Headers and Library Files</span></span>

<span data-ttu-id="cd021-116">Включите следующие файлы заголовков.</span><span class="sxs-lookup"><span data-stu-id="cd021-116">Include the following header files.</span></span>


```C++
#include <new>
#include <iostream>
#include <windows.h>
#include <mfapi.h>
#include <Mfidl.h>
#include <shlwapi.h>
```



<span data-ttu-id="cd021-117">Свяжите следующие файлы библиотеки.</span><span class="sxs-lookup"><span data-stu-id="cd021-117">Link the following library files.</span></span>


```C++
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "shlwapi")
```



## <a name="define-the-encoding-profiles"></a><span data-ttu-id="cd021-118">Определение профилей кодирования</span><span class="sxs-lookup"><span data-stu-id="cd021-118">Define the Encoding Profiles</span></span>

<span data-ttu-id="cd021-119">Одним из подходов к кодированию является определение списка целевых профилей кодирования, известных заранее.</span><span class="sxs-lookup"><span data-stu-id="cd021-119">One approach to encoding is to define a list of target encoding profiles that are known in advance.</span></span> <span data-ttu-id="cd021-120">В этом учебнике мы используем относительно простой подход и сохраняем список форматов кодирования для H. 264 Video и AAC Audio.</span><span class="sxs-lookup"><span data-stu-id="cd021-120">For this tutorial, we take a relatively simple approach, and store a list of encoding formats for H.264 video and AAC audio.</span></span>

<span data-ttu-id="cd021-121">Для H. 264 наиболее важными атрибутами формата являются профили H. 264, частота кадров, размер кадра и скорость кодирования.</span><span class="sxs-lookup"><span data-stu-id="cd021-121">For H.264, the most important format attributes are the H.264 profile, the frame rate, the frame size, and the encoded bit rate.</span></span> <span data-ttu-id="cd021-122">Следующий массив содержит список форматов кодирования H. 264.</span><span class="sxs-lookup"><span data-stu-id="cd021-122">The following array contains a list of H.264 encoding formats.</span></span>


```C++
struct H264ProfileInfo
{
    UINT32  profile;
    MFRatio fps;
    MFRatio frame_size;
    UINT32  bitrate;
};

H264ProfileInfo h264_profiles[] = 
{
    { eAVEncH264VProfile_Base, { 15, 1 },       { 176, 144 },   128000 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 30, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 29970, 1000 }, { 320, 240 },   528560 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 720, 576 },  4000000 },
    { eAVEncH264VProfile_Main, { 25, 1 },       { 720, 576 }, 10000000 },
    { eAVEncH264VProfile_Main, { 30, 1 },       { 352, 288 }, 10000000 },
};
```



<span data-ttu-id="cd021-123">Профили H. 264 указываются с помощью перечисления [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .</span><span class="sxs-lookup"><span data-stu-id="cd021-123">H.264 profiles are specified using the [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) enumeration.</span></span> <span data-ttu-id="cd021-124">Можно также указать уровень H. 264, но [**кодировщик видео Microsoft Media Foundation H. 264**](h-264-video-encoder.md) может наследовать соответствующий уровень для данного видеопотока, поэтому рекомендуется не переопределять выбранный уровень кодировщика.</span><span class="sxs-lookup"><span data-stu-id="cd021-124">You could also specify the H.264 level, but the Microsoft Media Foundation [**H.264 Video Encoder**](h-264-video-encoder.md) can derive the proper level for a given video stream, so it is recommended not to override the encoder's selected level.</span></span> <span data-ttu-id="cd021-125">Для содержимого с чередованием также можно указать режим чересстрочная развертки (см. [видео чередование](video-interlacing.md)).</span><span class="sxs-lookup"><span data-stu-id="cd021-125">For interlaced content, you would also specify the interlace mode (see [Video Interlacing](video-interlacing.md)).</span></span>

<span data-ttu-id="cd021-126">Для AAC Audio наиболее важными атрибутами формата являются звуковые примеры, количество каналов, количество бит на выборку и скорость кодирования.</span><span class="sxs-lookup"><span data-stu-id="cd021-126">For AAC audio, the most important format attributes are the audio sample rate, the number of channels, the number of bits per sample, and the encoded bit rate.</span></span> <span data-ttu-id="cd021-127">При необходимости можно задать указание уровня профиля аудиоподсистемы AAC.</span><span class="sxs-lookup"><span data-stu-id="cd021-127">Optionally, you can set the AAC audio profile level indication.</span></span> <span data-ttu-id="cd021-128">Дополнительные сведения см. в разделе [**кодировщик AAC**](aac-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="cd021-128">For more information, see [**AAC Encoder**](aac-encoder.md).</span></span> <span data-ttu-id="cd021-129">Следующий массив содержит список форматов кодирования AAC.</span><span class="sxs-lookup"><span data-stu-id="cd021-129">The following array contains a list of AAC encoding formats.</span></span>


```C++
struct AACProfileInfo
{
    UINT32  samplesPerSec;
    UINT32  numChannels;
    UINT32  bitsPerSample;
    UINT32  bytesPerSec;
    UINT32  aacProfile;
};

AACProfileInfo aac_profiles[] = 
{
    { 96000, 2, 16, 24000, 0x29}, 
    { 48000, 2, 16, 24000, 0x29}, 
    { 44100, 2, 16, 16000, 0x29}, 
    { 44100, 2, 16, 12000, 0x29}, 
};
```



> [!Note]  
> <span data-ttu-id="cd021-130">`H264ProfileInfo`Структуры и, `AACProfileInfo` определенные здесь, не являются частью Media Foundation API.</span><span class="sxs-lookup"><span data-stu-id="cd021-130">The `H264ProfileInfo` and `AACProfileInfo` structures defined here are not part of the Media Foundation API.</span></span>

 

## <a name="write-the-wmain-function"></a><span data-ttu-id="cd021-131">Написание функции wmain</span><span class="sxs-lookup"><span data-stu-id="cd021-131">Write the wmain Function</span></span>

<span data-ttu-id="cd021-132">В следующем коде показана точка входа для консольного приложения.</span><span class="sxs-lookup"><span data-stu-id="cd021-132">The following code shows the entry point for the console application.</span></span>


```C++
int video_profile = 0;
int audio_profile = 0;

int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc < 3 || argc > 5)
    {
        std::cout << "Usage:" << std::endl;
        std::cout << "input output [ audio_profile video_profile ]" << std::endl;
        return 1;
    }

    if (argc > 3)
    {
        audio_profile = _wtoi(argv[3]);
    }
    if (argc > 4)
    {
        video_profile = _wtoi(argv[4]);
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            hr = EncodeFile(argv[1], argv[2]);
            MFShutdown();
        }
        CoUninitialize();
    }

    if (SUCCEEDED(hr))
    {
        std::cout << "Done." << std::endl;
    }
    else
    {
        std::cout << "Error: " << std::hex << hr << std::endl;
    }

    return 0;
}
```



<span data-ttu-id="cd021-133">`wmain`Функция выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="cd021-133">The `wmain` function does the following:</span></span>

1.  <span data-ttu-id="cd021-134">Вызывает функцию [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) для инициализации библиотеки COM.</span><span class="sxs-lookup"><span data-stu-id="cd021-134">Calls the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library.</span></span>
2.  <span data-ttu-id="cd021-135">Вызывает функцию [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) для инициализации Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="cd021-135">Calls the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function to initialize Media Foundation.</span></span>
3.  <span data-ttu-id="cd021-136">Вызывает определяемую приложением `EncodeFile` функцию.</span><span class="sxs-lookup"><span data-stu-id="cd021-136">Calls the application-defined `EncodeFile` function.</span></span> <span data-ttu-id="cd021-137">Эта функция перекодировать входной файл в выходной файл и показан в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="cd021-137">This function transcodes the input file to the output file, and is shown in the next section.</span></span>
4.  <span data-ttu-id="cd021-138">Вызывает функцию [**мфшутдовн**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) для завершения работы Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="cd021-138">Calls the [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) function to shut down Media Foundation.</span></span>
5.  <span data-ttu-id="cd021-139">Вызовите функцию [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) , чтобы отменить инициализацию библиотеки COM.</span><span class="sxs-lookup"><span data-stu-id="cd021-139">Call the [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function to uninitialize the COM library.</span></span>

## <a name="encode-the-file"></a><span data-ttu-id="cd021-140">Кодирование файла</span><span class="sxs-lookup"><span data-stu-id="cd021-140">Encode the File</span></span>

<span data-ttu-id="cd021-141">В следующем коде показана `EncodeFile` функция, которая выполняет перекодировку.</span><span class="sxs-lookup"><span data-stu-id="cd021-141">The following code shows `EncodeFile` function, which performs the transcoding.</span></span> <span data-ttu-id="cd021-142">Эта функция состоит в основном из вызовов других определяемых приложением функций, которые показаны Далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="cd021-142">This function consists mostly of calls to other application-defined functions, which are shown later in this topic.</span></span>


```C++
HRESULT EncodeFile(PCWSTR pszInput, PCWSTR pszOutput)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFMediaSource *pSource = NULL;
    IMFTopology *pTopology = NULL;
    CSession *pSession = NULL;

    MFTIME duration = 0;

    HRESULT hr = CreateMediaSource(pszInput, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetSourceDuration(pSource, &duration);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateTranscodeTopology(pSource, pszOutput, pProfile, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CSession::Create(&pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->StartEncodingSession(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = RunEncodingSession(pSession, duration);

done:            
    if (pSource)
    {
        pSource->Shutdown();
    }

    SafeRelease(&pSession);
    SafeRelease(&pProfile);
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="cd021-143">`EncodeFile`Функция выполняет следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cd021-143">The `EncodeFile` function performs the following steps.</span></span>

1.  <span data-ttu-id="cd021-144">Создает источник мультимедиа для входного файла, используя URL-адрес или путь к входному файлу.</span><span class="sxs-lookup"><span data-stu-id="cd021-144">Creates a media source for the input file, using the URL or file path of the input file.</span></span> <span data-ttu-id="cd021-145">(См. раздел [Создание источника мультимедиа](#create-the-media-source).)</span><span class="sxs-lookup"><span data-stu-id="cd021-145">(See [Create the Media Source](#create-the-media-source).)</span></span>
2.  <span data-ttu-id="cd021-146">Возвращает длительность входного файла.</span><span class="sxs-lookup"><span data-stu-id="cd021-146">Gets the duration of the input file.</span></span> <span data-ttu-id="cd021-147">(См. статью [Получение исходного времени](#get-the-source-duration).)</span><span class="sxs-lookup"><span data-stu-id="cd021-147">(See [Get the Source Duration](#get-the-source-duration).)</span></span>
3.  <span data-ttu-id="cd021-148">Создайте профиль перекодирования.</span><span class="sxs-lookup"><span data-stu-id="cd021-148">Create the transcode profile.</span></span> <span data-ttu-id="cd021-149">(См. раздел [Создание профиля перекодирования](#create-the-transcode-profile).)</span><span class="sxs-lookup"><span data-stu-id="cd021-149">(See [Create the Transcode Profile](#create-the-transcode-profile).)</span></span>
4.  <span data-ttu-id="cd021-150">Вызовите [**мфкреатетранскодетопологи**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) , чтобы создать частичную топологию перекодирования.</span><span class="sxs-lookup"><span data-stu-id="cd021-150">Call [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) to create the partial transcode topology.</span></span>
5.  <span data-ttu-id="cd021-151">Создание вспомогательного объекта, управляющего сеансом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cd021-151">Create a helper object that manages the Media Session.</span></span> <span data-ttu-id="cd021-152">(См. раздел помощник по сеансу мультимедиа).</span><span class="sxs-lookup"><span data-stu-id="cd021-152">(See Media Session Helper).</span></span>
6.  <span data-ttu-id="cd021-153">Запустите сеанс кодирования и дождитесь его завершения.</span><span class="sxs-lookup"><span data-stu-id="cd021-153">Run the encoding session and wait for it to complete.</span></span> <span data-ttu-id="cd021-154">(См. раздел [Запуск сеанса кодирования](#run-the-encoding-session).)</span><span class="sxs-lookup"><span data-stu-id="cd021-154">(See [Run the Encoding Session](#run-the-encoding-session).)</span></span>
7.  <span data-ttu-id="cd021-155">Вызовите [**имфмедиасаурце:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) , чтобы завершить работу источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cd021-155">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the media source.</span></span>
8.  <span data-ttu-id="cd021-156">Освободить указатели интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cd021-156">Release interface pointers.</span></span> <span data-ttu-id="cd021-157">Этот код использует функцию [саферелеасе](saferelease.md) для освобождения указателей интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cd021-157">This code uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span> <span data-ttu-id="cd021-158">Другой вариант — использовать класс интеллектуального указателя COM, например **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="cd021-158">Another option is to use a COM smart pointer class, such as **CComPtr**.</span></span>

### <a name="create-the-media-source"></a><span data-ttu-id="cd021-159">Создание источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="cd021-159">Create the Media Source</span></span>

<span data-ttu-id="cd021-160">Источник мультимедиа — это объект, который считывает и анализирует входной файл.</span><span class="sxs-lookup"><span data-stu-id="cd021-160">The media source is the object that reads and parses the input file.</span></span> <span data-ttu-id="cd021-161">Чтобы создать источник мультимедиа, передайте URL-адрес входного файла в [сопоставитель источника](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="cd021-161">To create the media source, pass the URL of the input file to the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="cd021-162">В следующем примере кода показано, как это сделать:</span><span class="sxs-lookup"><span data-stu-id="cd021-162">The following code shows how to do this.</span></span>


```C++
HRESULT CreateMediaSource(PCWSTR pszURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source
    hr = pResolver->CreateObjectFromURL(pszURL, MF_RESOLUTION_MEDIASOURCE, 
        NULL, &ObjectType, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pResolver);
    SafeRelease(&pSource);
    return hr;
}
```



<span data-ttu-id="cd021-163">Дополнительные сведения см. [в разделе Использование сопоставителя источников](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="cd021-163">For more information, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>

### <a name="get-the-source-duration"></a><span data-ttu-id="cd021-164">Получить длительность источника</span><span class="sxs-lookup"><span data-stu-id="cd021-164">Get the Source Duration</span></span>

<span data-ttu-id="cd021-165">Хотя это и не является обязательным, полезно запрашивать источник носителя о продолжительности входного файла.</span><span class="sxs-lookup"><span data-stu-id="cd021-165">Although not required, it is useful to query the media source for the duration of the input file.</span></span> <span data-ttu-id="cd021-166">Это значение можно использовать для отслеживания хода выполнения кодирования.</span><span class="sxs-lookup"><span data-stu-id="cd021-166">This value can be used to track the encoding progress.</span></span> <span data-ttu-id="cd021-167">Длительность сохраняется в атрибуте " [**\_ \_ Продолжительность MF PD**](mf-pd-duration-attribute.md) " дескриптора представления.</span><span class="sxs-lookup"><span data-stu-id="cd021-167">The duration is stored in the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute of the presentation descriptor.</span></span> <span data-ttu-id="cd021-168">Получите дескриптор представления, вызвав [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="cd021-168">Get the presentation descriptor by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



### <a name="create-the-transcode-profile"></a><span data-ttu-id="cd021-169">Создание профиля перекодирования</span><span class="sxs-lookup"><span data-stu-id="cd021-169">Create the Transcode Profile</span></span>

<span data-ttu-id="cd021-170">В профиле перекодировки описываются параметры кодирования.</span><span class="sxs-lookup"><span data-stu-id="cd021-170">The transcode profile describes the encoding parameters.</span></span> <span data-ttu-id="cd021-171">Дополнительные сведения о создании профиля перекодирования см. в разделе [Использование API-интерфейса для перекодирования](fast-transcode-objects.md).</span><span class="sxs-lookup"><span data-stu-id="cd021-171">For more information about creating a transcode profile, see [Using the Transcode API](fast-transcode-objects.md).</span></span> <span data-ttu-id="cd021-172">Чтобы создать профиль, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cd021-172">To create the profile, perform the following steps.</span></span>

1.  <span data-ttu-id="cd021-173">Вызовите [**мфкреатетранскодепрофиле**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) , чтобы создать пустой профиль.</span><span class="sxs-lookup"><span data-stu-id="cd021-173">Call [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) to create the empty profile.</span></span>
2.  <span data-ttu-id="cd021-174">Создайте тип носителя для аудиопотока AAC.</span><span class="sxs-lookup"><span data-stu-id="cd021-174">Create a media type for the AAC audio stream.</span></span> <span data-ttu-id="cd021-175">Добавьте его в профиль, вызвав [**имфтранскодепрофиле:: сетаудиоаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span><span class="sxs-lookup"><span data-stu-id="cd021-175">Add it to the profile by calling [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span></span>
3.  <span data-ttu-id="cd021-176">Создайте тип мультимедиа для видеопотока H. 264.</span><span class="sxs-lookup"><span data-stu-id="cd021-176">Create a media type for the H.264 video stream.</span></span> <span data-ttu-id="cd021-177">Добавьте его в профиль, вызвав [**имфтранскодепрофиле:: сетвидеоаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span><span class="sxs-lookup"><span data-stu-id="cd021-177">Add it to the profile by calling [**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span></span>
4.  <span data-ttu-id="cd021-178">Вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать хранилище атрибутов для атрибутов уровня контейнера.</span><span class="sxs-lookup"><span data-stu-id="cd021-178">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store for the container-level attributes.</span></span>
5.  <span data-ttu-id="cd021-179">Задайте атрибут [ \_ \_ КОНТАИНЕРТИПЕ для перекодировки MF](mf-transcode-containertype.md) .</span><span class="sxs-lookup"><span data-stu-id="cd021-179">Set the [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute.</span></span> <span data-ttu-id="cd021-180">Это единственный обязательный атрибут уровня контейнера.</span><span class="sxs-lookup"><span data-stu-id="cd021-180">This is the only required container-level attribute.</span></span> <span data-ttu-id="cd021-181">Для выходных данных файла MP4 установите для этого атрибута значение **мфтранскодеконтаинертипе \_ MPEG4**.</span><span class="sxs-lookup"><span data-stu-id="cd021-181">For MP4 file output, set this attribute to **MFTranscodeContainerType\_MPEG4**.</span></span>
6.  <span data-ttu-id="cd021-182">Вызовите метод [**имфтранскодепрофиле:: сетконтаинераттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) , чтобы задать атрибуты уровня контейнера.</span><span class="sxs-lookup"><span data-stu-id="cd021-182">Call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) to set the container-level attributes.</span></span>

<span data-ttu-id="cd021-183">Эти действия показаны в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="cd021-183">The following code shows these steps.</span></span>


```C++
HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFAttributes *pAudio = NULL;
    IMFAttributes *pVideo = NULL;
    IMFAttributes *pContainer = NULL;

    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Audio attributes.
    hr = CreateAACProfile(audio_profile, &pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetAudioAttributes(pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Video attributes.
    hr = CreateH264Profile(video_profile, &pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetVideoAttributes(pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_MPEG4);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetContainerAttributes(pContainer);
    if (FAILED(hr)) 
    {
        goto done;
    }

    *ppProfile = pProfile;
    (*ppProfile)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pAudio);
    SafeRelease(&pVideo);
    SafeRelease(&pContainer);
    return hr;
}
```



<span data-ttu-id="cd021-184">Чтобы указать атрибуты для видеопотока H. 264, создайте хранилище атрибутов и задайте следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="cd021-184">To specify the attributes for the H.264 video stream, create an attribute store and set the following attributes:</span></span>



| <span data-ttu-id="cd021-185">attribute</span><span class="sxs-lookup"><span data-stu-id="cd021-185">Attribute</span></span>                                                       | <span data-ttu-id="cd021-186">Описание</span><span class="sxs-lookup"><span data-stu-id="cd021-186">Desription</span></span>                      |
|-----------------------------------------------------------------|---------------------------------|
| [<span data-ttu-id="cd021-187">**подтип MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="cd021-187">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)              | <span data-ttu-id="cd021-188">Задайте для параметра значение **мфвидеоформат \_ H264 Single bitrate**.</span><span class="sxs-lookup"><span data-stu-id="cd021-188">Set to **MFVideoFormat\_H264**.</span></span> |
| [<span data-ttu-id="cd021-189">**\_Профиль MF MT \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="cd021-189">**MF\_MT\_MPEG2\_PROFILE**</span></span>](mf-mt-mpeg2-profile-attribute.md) | <span data-ttu-id="cd021-190">Профиль H. 264.</span><span class="sxs-lookup"><span data-stu-id="cd021-190">H.264 profile.</span></span>                  |
| [<span data-ttu-id="cd021-191">**\_ \_ Размер пакета MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="cd021-191">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)       | <span data-ttu-id="cd021-192">Размер кадра.</span><span class="sxs-lookup"><span data-stu-id="cd021-192">Frame size.</span></span>                     |
| [<span data-ttu-id="cd021-193">**\_ \_ Частота кадров MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="cd021-193">**MF\_MT\_FRAME\_RATE**</span></span>](mf-mt-frame-rate-attribute.md)       | <span data-ttu-id="cd021-194">Частота кадров.</span><span class="sxs-lookup"><span data-stu-id="cd021-194">Frame rate.</span></span>                     |
| [<span data-ttu-id="cd021-195">**\_ \_ Средняя скорость MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="cd021-195">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)     | <span data-ttu-id="cd021-196">Скорость кодирования.</span><span class="sxs-lookup"><span data-stu-id="cd021-196">Encoded bit rate.</span></span>               |



 

<span data-ttu-id="cd021-197">Чтобы указать атрибуты для аудиопотока AAC, создайте хранилище атрибутов и задайте следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="cd021-197">To specify the attributes for the AAC audio stream, create an attribute store and set the following attributes:</span></span>



| <span data-ttu-id="cd021-198">attribute</span><span class="sxs-lookup"><span data-stu-id="cd021-198">Attribute</span></span>                                                                                      | <span data-ttu-id="cd021-199">Описание</span><span class="sxs-lookup"><span data-stu-id="cd021-199">Desription</span></span>                               |
|------------------------------------------------------------------------------------------------|------------------------------------------|
| [<span data-ttu-id="cd021-200">**подтип MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="cd021-200">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="cd021-201">Задайте значение **мфаудиоформат \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="cd021-201">Set to **MFAudioFormat\_AAC**</span></span>            |
| [<span data-ttu-id="cd021-202">**\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду**</span><span class="sxs-lookup"><span data-stu-id="cd021-202">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="cd021-203">Частота дискретизации.</span><span class="sxs-lookup"><span data-stu-id="cd021-203">Audio sample rate.</span></span>                       |
| [<span data-ttu-id="cd021-204">**\_ \_ звуковый бит MF MT \_ \_ на \_ выборку**</span><span class="sxs-lookup"><span data-stu-id="cd021-204">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)              | <span data-ttu-id="cd021-205">Пример битов на аудио.</span><span class="sxs-lookup"><span data-stu-id="cd021-205">Bits per audio sample.</span></span>                   |
| [<span data-ttu-id="cd021-206">**\_ \_ каналы аудиосигнала MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd021-206">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="cd021-207">Число аудиоканалов.</span><span class="sxs-lookup"><span data-stu-id="cd021-207">Number of audio channels.</span></span>                |
| [<span data-ttu-id="cd021-208">**\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT**</span><span class="sxs-lookup"><span data-stu-id="cd021-208">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)   | <span data-ttu-id="cd021-209">Скорость кодирования.</span><span class="sxs-lookup"><span data-stu-id="cd021-209">Encoded bit rate.</span></span>                        |
| [<span data-ttu-id="cd021-210">**\_ \_ Выравнивание звукового \_ блока MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="cd021-210">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)               | <span data-ttu-id="cd021-211">Задан равным 1.</span><span class="sxs-lookup"><span data-stu-id="cd021-211">Set to 1.</span></span>                                |
| [<span data-ttu-id="cd021-212">\_ \_ \_ Указание уровня звукового \_ профиля \_ MF MT AAC \_</span><span class="sxs-lookup"><span data-stu-id="cd021-212">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="cd021-213">Указание уровня профиля AAC (необязательно).</span><span class="sxs-lookup"><span data-stu-id="cd021-213">AAC profile level indication (optional).</span></span> |



 

<span data-ttu-id="cd021-214">Следующий код создает атрибуты потока видео.</span><span class="sxs-lookup"><span data-stu-id="cd021-214">The following code creates the video stream attributes.</span></span>


```C++
HRESULT CreateH264Profile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    IMFAttributes *pAttributes = NULL;

    const H264ProfileInfo& profile = h264_profiles[index];

    HRESULT hr = MFCreateAttributes(&pAttributes, 5);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_H264);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_MPEG2_PROFILE, profile.profile);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(
            pAttributes, MF_MT_FRAME_SIZE, 
            profile.frame_size.Numerator, profile.frame_size.Numerator);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(
            pAttributes, MF_MT_FRAME_RATE, 
            profile.fps.Numerator, profile.fps.Denominator);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AVG_BITRATE, profile.bitrate);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



<span data-ttu-id="cd021-215">Следующий код создает атрибуты аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="cd021-215">The following code creates the audio stream attributes.</span></span>


```C++
HRESULT CreateAACProfile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    const AACProfileInfo& profile = aac_profiles[index];

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 7);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_AAC);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_BITS_PER_SAMPLE, profile.bitsPerSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_SAMPLES_PER_SECOND, profile.samplesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_NUM_CHANNELS, profile.numChannels);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_AVG_BYTES_PER_SECOND, profile.bytesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AUDIO_BLOCK_ALIGNMENT, 1);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION, profile.aacProfile);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



<span data-ttu-id="cd021-216">Обратите внимание, что API перекодирования не требует истинного типа мультимедиа, хотя он использует атрибуты типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cd021-216">Note that the transcode API does not require a true media type, although it uses media-type attributes.</span></span> <span data-ttu-id="cd021-217">В частности, атрибут [**\_ \_ основного \_ типа MF MT**](mf-mt-major-type-attribute.md) не требуется, так как методы [**сетвидеоаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) и [**сетаудиоаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) подразумевают основной тип.</span><span class="sxs-lookup"><span data-stu-id="cd021-217">In particular, the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute it not required, because the [**SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) and [**SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) methods imply the major type.</span></span> <span data-ttu-id="cd021-218">Однако он также может передавать в эти методы фактический тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cd021-218">However, it also valid to pass an actual media type to these methods.</span></span> <span data-ttu-id="cd021-219">(Интерфейс [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) наследует [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).)</span><span class="sxs-lookup"><span data-stu-id="cd021-219">(The [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface inherits [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).)</span></span>

### <a name="run-the-encoding-session"></a><span data-ttu-id="cd021-220">Запуск сеанса кодирования</span><span class="sxs-lookup"><span data-stu-id="cd021-220">Run the Encoding Session</span></span>

<span data-ttu-id="cd021-221">Следующий код запускает сеанс кодирования.</span><span class="sxs-lookup"><span data-stu-id="cd021-221">The following code runs the encoding session.</span></span> <span data-ttu-id="cd021-222">В нем используется класс поддержки сеанса мультимедиа, который показан в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="cd021-222">It uses the Media Session helper class, which is shown in the next section.</span></span>


```C++
HRESULT RunEncodingSession(CSession *pSession, MFTIME duration)
{
    const DWORD WAIT_PERIOD = 500;
    const int   UPDATE_INCR = 5;

    HRESULT hr = S_OK;
    MFTIME pos;
    LONGLONG prev = 0;
    while (1)
    {
        hr = pSession->Wait(WAIT_PERIOD);
        if (hr == E_PENDING)
        {
            hr = pSession->GetEncodingPosition(&pos);

            LONGLONG percent = (100 * pos) / duration ;
            if (percent >= prev + UPDATE_INCR)
            {
                std::cout << percent << "% .. ";  
                prev = percent;
            }
        }
        else
        {
            std::cout << std::endl;
            break;
        }
    }
    return hr;
}
```



## <a name="media-session-helper"></a><span data-ttu-id="cd021-223">Вспомогательный модуль сеанса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="cd021-223">Media Session Helper</span></span>

<span data-ttu-id="cd021-224">[Сеанс мультимедиа](media-session.md) описан более подробно в разделе [архитектура Media Foundation](media-foundation-architecture.md) этой документации.</span><span class="sxs-lookup"><span data-stu-id="cd021-224">The [Media Session](media-session.md) is described more fully in the [Media Foundation Architecture](media-foundation-architecture.md) section of this documentation.</span></span> <span data-ttu-id="cd021-225">В сеансе мультимедиа используется асинхронная модель событий.</span><span class="sxs-lookup"><span data-stu-id="cd021-225">The Media Session uses an asynchronous event model.</span></span> <span data-ttu-id="cd021-226">В приложении GUI следует реагировать на события сеанса, не блокируя поток пользовательского интерфейса для ожидания следующего события.</span><span class="sxs-lookup"><span data-stu-id="cd021-226">In a GUI application, you should respond to session events without blocking the UI thread to wait for the next event.</span></span> <span data-ttu-id="cd021-227">В руководстве по [воспроизведению незащищенных файлов мультимедиа](how-to-play-unprotected-media-files.md) показано, как это сделать в приложении воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="cd021-227">The tutorial [How to Play Unprotected Media Files](how-to-play-unprotected-media-files.md) shows how to do this in a playback application.</span></span> <span data-ttu-id="cd021-228">Для кодировки принцип является тем же, но имеет значение меньшее количество событий:</span><span class="sxs-lookup"><span data-stu-id="cd021-228">For encoding, the principle is the same, but fewer events are relevant:</span></span>



| <span data-ttu-id="cd021-229">Событие</span><span class="sxs-lookup"><span data-stu-id="cd021-229">Event</span></span>                                  | <span data-ttu-id="cd021-230">Описание</span><span class="sxs-lookup"><span data-stu-id="cd021-230">Desription</span></span>                                                                                                                                                       |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd021-231">месессионендед</span><span class="sxs-lookup"><span data-stu-id="cd021-231">MESessionEnded</span></span>](mesessionended.md)   | <span data-ttu-id="cd021-232">Возникает после завершения кодирования.</span><span class="sxs-lookup"><span data-stu-id="cd021-232">Raised when the encoding is complete.</span></span>                                                                                                                            |
| [<span data-ttu-id="cd021-233">месессионклосед</span><span class="sxs-lookup"><span data-stu-id="cd021-233">MESessionClosed</span></span>](mesessionclosed.md) | <span data-ttu-id="cd021-234">Возникает при завершении метода [**имфмедиасессион:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) .</span><span class="sxs-lookup"><span data-stu-id="cd021-234">Raised when the [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) method completes.</span></span> <span data-ttu-id="cd021-235">После возникновения этого события можно спокойно завершить сеанс мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cd021-235">After this event is raised, it is safe to shut down the Media Session.</span></span> |



 

<span data-ttu-id="cd021-236">Для консольного приложения разумно блокировать и ожидать события.</span><span class="sxs-lookup"><span data-stu-id="cd021-236">For a console application, it is reasonable to block and wait for events.</span></span> <span data-ttu-id="cd021-237">В зависимости от исходного файла и параметров кодировки для завершения кодирования может потребоваться некоторое время.</span><span class="sxs-lookup"><span data-stu-id="cd021-237">Depending on the source file and the encoding settings, it might take awhile to complete the encoding.</span></span> <span data-ttu-id="cd021-238">Обновления хода выполнения можно получить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cd021-238">You can get progress updates as follows:</span></span>

1.  <span data-ttu-id="cd021-239">Вызовите [**имфмедиасессион:: Clock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) , чтобы получить часы презентации.</span><span class="sxs-lookup"><span data-stu-id="cd021-239">Call [**IMFMediaSession::GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) to get the presentation clock.</span></span>
2.  <span data-ttu-id="cd021-240">Запросите часы для интерфейса [**имфпресентатионклокк**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) .</span><span class="sxs-lookup"><span data-stu-id="cd021-240">Query the clock for the [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) interface.</span></span>
3.  <span data-ttu-id="cd021-241">Чтобы получить текущую точку, вызовите метод [**имфпресентатионклокк:: Time**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) .</span><span class="sxs-lookup"><span data-stu-id="cd021-241">Call [**IMFPresentationClock::GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) to get the current position.</span></span>
4.  <span data-ttu-id="cd021-242">Это значение указывается в единицах времени.</span><span class="sxs-lookup"><span data-stu-id="cd021-242">The position is given in units of time.</span></span> <span data-ttu-id="cd021-243">Чтобы получить процент завершения, используйте значение `(100 * position) / duration` .</span><span class="sxs-lookup"><span data-stu-id="cd021-243">To get the percentage completed, use the value `(100 * position) / duration`.</span></span>

<span data-ttu-id="cd021-244">Ниже приведено объявление `CSession` класса.</span><span class="sxs-lookup"><span data-stu-id="cd021-244">Here is the declaration of the `CSession` class.</span></span>


```C++
class CSession  : public IMFAsyncCallback 
{
public:
    static HRESULT Create(CSession **ppSession);

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IMFAsyncCallback methods
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
    STDMETHODIMP Invoke(IMFAsyncResult *pResult);

    // Other methods
    HRESULT StartEncodingSession(IMFTopology *pTopology);
    HRESULT GetEncodingPosition(MFTIME *pTime);
    HRESULT Wait(DWORD dwMsec);

private:
    CSession() : m_cRef(1), m_pSession(NULL), m_pClock(NULL), m_hrStatus(S_OK), m_hWaitEvent(NULL)
    {
    }
    virtual ~CSession()
    {
        if (m_pSession)
        {
            m_pSession->Shutdown();
        }

        SafeRelease(&m_pClock);
        SafeRelease(&m_pSession);
        CloseHandle(m_hWaitEvent);
    }

    HRESULT Initialize();

private:
    IMFMediaSession      *m_pSession;
    IMFPresentationClock *m_pClock;
    HRESULT m_hrStatus;
    HANDLE  m_hWaitEvent;
    long    m_cRef;
};
```



<span data-ttu-id="cd021-245">В следующем коде показана полная реализация `CSession` класса.</span><span class="sxs-lookup"><span data-stu-id="cd021-245">The following code shows the complete implementation of the `CSession` class.</span></span>


```C++
HRESULT CSession::Create(CSession **ppSession)
{
    *ppSession = NULL;

    CSession *pSession = new (std::nothrow) CSession();
    if (pSession == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pSession->Initialize();
    if (FAILED(hr))
    {
        pSession->Release();
        return hr;
    }
    *ppSession = pSession;
    return S_OK;
}

STDMETHODIMP CSession::QueryInterface(REFIID riid, void** ppv)
{
    static const QITAB qit[] = 
    {
        QITABENT(CSession, IMFAsyncCallback),
        { 0 }
    };
    return QISearch(this, qit, riid, ppv);
}

STDMETHODIMP_(ULONG) CSession::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

STDMETHODIMP_(ULONG) CSession::Release()
{
    long cRef = InterlockedDecrement(&m_cRef);
    if (cRef == 0)
    {
        delete this;
    }
    return cRef;
}

HRESULT CSession::Initialize()
{
    IMFClock *pClock = NULL;

    HRESULT hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->GetClock(&pClock);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pClock->QueryInterface(IID_PPV_ARGS(&m_pClock));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->BeginGetEvent(this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_hWaitEvent = CreateEvent(NULL, FALSE, FALSE, NULL);  
    if (m_hWaitEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
done:
    SafeRelease(&pClock);
    return hr;
}

// Implements IMFAsyncCallback::Invoke
STDMETHODIMP CSession::Invoke(IMFAsyncResult *pResult)
{
    IMFMediaEvent* pEvent = NULL;
    MediaEventType meType = MEUnknown;
    HRESULT hrStatus = S_OK;

    HRESULT hr = m_pSession->EndGetEvent(pResult, &pEvent);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEvent->GetStatus(&hrStatus);
    if (FAILED(hr))
    {
        goto done;
    }

    if (FAILED(hrStatus))
    {
        hr = hrStatus;
        goto done;
    }

    switch (meType)
    {
    case MESessionEnded:
        hr = m_pSession->Close();
        if (FAILED(hr))
        {
            goto done;
        }
        break;

    case MESessionClosed:
        SetEvent(m_hWaitEvent);
        break;
    }

    if (meType != MESessionClosed)
    {
        hr = m_pSession->BeginGetEvent(this, NULL);
    }

done:
    if (FAILED(hr))
    {
        m_hrStatus = hr;
        m_pSession->Close();
    }

    SafeRelease(&pEvent);
    return hr;
}

HRESULT CSession::StartEncodingSession(IMFTopology *pTopology)
{
    HRESULT hr = m_pSession->SetTopology(0, pTopology);
    if (SUCCEEDED(hr))
    {
        PROPVARIANT varStart;
        PropVariantClear(&varStart);
        hr = m_pSession->Start(&GUID_NULL, &varStart);
    }
    return hr;
}

HRESULT CSession::GetEncodingPosition(MFTIME *pTime)
{
    return m_pClock->GetTime(pTime);
}

HRESULT CSession::Wait(DWORD dwMsec)
{
    HRESULT hr = S_OK;

    DWORD dwTimeoutStatus = WaitForSingleObject(m_hWaitEvent, dwMsec);
    if (dwTimeoutStatus != WAIT_OBJECT_0)
    {
        hr = E_PENDING;
    }
    else
    {
        hr = m_hrStatus;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="cd021-246">См. также</span><span class="sxs-lookup"><span data-stu-id="cd021-246">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd021-247">**Кодировщик AAC**</span><span class="sxs-lookup"><span data-stu-id="cd021-247">**AAC Encoder**</span></span>](aac-encoder.md)
</dt> <dt>

[<span data-ttu-id="cd021-248">**Кодировщик видео H. 264**</span><span class="sxs-lookup"><span data-stu-id="cd021-248">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="cd021-249">Сеанс мультимедиа</span><span class="sxs-lookup"><span data-stu-id="cd021-249">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="cd021-250">Типы носителей</span><span class="sxs-lookup"><span data-stu-id="cd021-250">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="cd021-251">API перекодирования</span><span class="sxs-lookup"><span data-stu-id="cd021-251">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 
