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
# <a name="tutorial-encoding-an-mp4-file"></a>Учебник. Кодирование файла MP4

В этом учебнике показано, как использовать [API](transcode-api.md) перекодировки для кодирования файла MP4 с помощью H. 264 для видеопотока и AAC для аудиопотока.

-   [Файлы заголовков и библиотек](#headers-and-library-files)
-   [Определение профилей кодирования](#define-the-encoding-profiles)
-   [Написание функции wmain](#write-the-wmain-function)
-   [Кодирование файла](#encode-the-file)
    -   [Создание источника мультимедиа](#create-the-media-source)
    -   [Получить длительность источника](#get-the-source-duration)
    -   [Создание профиля перекодирования](#create-the-transcode-profile)
    -   [Запуск сеанса кодирования](#run-the-encoding-session)
-   [Вспомогательный модуль сеанса мультимедиа](#media-session-helper)
-   [См. также](#related-topics)

## <a name="headers-and-library-files"></a>Файлы заголовков и библиотек

Включите следующие файлы заголовков.


```C++
#include <new>
#include <iostream>
#include <windows.h>
#include <mfapi.h>
#include <Mfidl.h>
#include <shlwapi.h>
```



Свяжите следующие файлы библиотеки.


```C++
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "shlwapi")
```



## <a name="define-the-encoding-profiles"></a>Определение профилей кодирования

Одним из подходов к кодированию является определение списка целевых профилей кодирования, известных заранее. В этом учебнике мы используем относительно простой подход и сохраняем список форматов кодирования для H. 264 Video и AAC Audio.

Для H. 264 наиболее важными атрибутами формата являются профили H. 264, частота кадров, размер кадра и скорость кодирования. Следующий массив содержит список форматов кодирования H. 264.


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



Профили H. 264 указываются с помощью перечисления [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) . Можно также указать уровень H. 264, но [**кодировщик видео Microsoft Media Foundation H. 264**](h-264-video-encoder.md) может наследовать соответствующий уровень для данного видеопотока, поэтому рекомендуется не переопределять выбранный уровень кодировщика. Для содержимого с чередованием также можно указать режим чересстрочная развертки (см. [видео чередование](video-interlacing.md)).

Для AAC Audio наиболее важными атрибутами формата являются звуковые примеры, количество каналов, количество бит на выборку и скорость кодирования. При необходимости можно задать указание уровня профиля аудиоподсистемы AAC. Дополнительные сведения см. в разделе [**кодировщик AAC**](aac-encoder.md). Следующий массив содержит список форматов кодирования AAC.


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
> `H264ProfileInfo`Структуры и, `AACProfileInfo` определенные здесь, не являются частью Media Foundation API.

 

## <a name="write-the-wmain-function"></a>Написание функции wmain

В следующем коде показана точка входа для консольного приложения.


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



`wmain`Функция выполняет следующие действия:

1.  Вызывает функцию [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) для инициализации библиотеки COM.
2.  Вызывает функцию [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) для инициализации Media Foundation.
3.  Вызывает определяемую приложением `EncodeFile` функцию. Эта функция перекодировать входной файл в выходной файл и показан в следующем разделе.
4.  Вызывает функцию [**мфшутдовн**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) для завершения работы Media Foundation.
5.  Вызовите функцию [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) , чтобы отменить инициализацию библиотеки COM.

## <a name="encode-the-file"></a>Кодирование файла

В следующем коде показана `EncodeFile` функция, которая выполняет перекодировку. Эта функция состоит в основном из вызовов других определяемых приложением функций, которые показаны Далее в этом разделе.


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



`EncodeFile`Функция выполняет следующие действия.

1.  Создает источник мультимедиа для входного файла, используя URL-адрес или путь к входному файлу. (См. раздел [Создание источника мультимедиа](#create-the-media-source).)
2.  Возвращает длительность входного файла. (См. статью [Получение исходного времени](#get-the-source-duration).)
3.  Создайте профиль перекодирования. (См. раздел [Создание профиля перекодирования](#create-the-transcode-profile).)
4.  Вызовите [**мфкреатетранскодетопологи**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) , чтобы создать частичную топологию перекодирования.
5.  Создание вспомогательного объекта, управляющего сеансом мультимедиа. (См. раздел помощник по сеансу мультимедиа).
6.  Запустите сеанс кодирования и дождитесь его завершения. (См. раздел [Запуск сеанса кодирования](#run-the-encoding-session).)
7.  Вызовите [**имфмедиасаурце:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) , чтобы завершить работу источника мультимедиа.
8.  Освободить указатели интерфейса. Этот код использует функцию [саферелеасе](saferelease.md) для освобождения указателей интерфейса. Другой вариант — использовать класс интеллектуального указателя COM, например **CComPtr**.

### <a name="create-the-media-source"></a>Создание источника мультимедиа

Источник мультимедиа — это объект, который считывает и анализирует входной файл. Чтобы создать источник мультимедиа, передайте URL-адрес входного файла в [сопоставитель источника](source-resolver.md). В следующем примере кода показано, как это сделать:


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



Дополнительные сведения см. [в разделе Использование сопоставителя источников](using-the-source-resolver.md).

### <a name="get-the-source-duration"></a>Получить длительность источника

Хотя это и не является обязательным, полезно запрашивать источник носителя о продолжительности входного файла. Это значение можно использовать для отслеживания хода выполнения кодирования. Длительность сохраняется в атрибуте " [**\_ \_ Продолжительность MF PD**](mf-pd-duration-attribute.md) " дескриптора представления. Получите дескриптор представления, вызвав [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).


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



### <a name="create-the-transcode-profile"></a>Создание профиля перекодирования

В профиле перекодировки описываются параметры кодирования. Дополнительные сведения о создании профиля перекодирования см. в разделе [Использование API-интерфейса для перекодирования](fast-transcode-objects.md). Чтобы создать профиль, выполните следующие действия.

1.  Вызовите [**мфкреатетранскодепрофиле**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) , чтобы создать пустой профиль.
2.  Создайте тип носителя для аудиопотока AAC. Добавьте его в профиль, вызвав [**имфтранскодепрофиле:: сетаудиоаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).
3.  Создайте тип мультимедиа для видеопотока H. 264. Добавьте его в профиль, вызвав [**имфтранскодепрофиле:: сетвидеоаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).
4.  Вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать хранилище атрибутов для атрибутов уровня контейнера.
5.  Задайте атрибут [ \_ \_ КОНТАИНЕРТИПЕ для перекодировки MF](mf-transcode-containertype.md) . Это единственный обязательный атрибут уровня контейнера. Для выходных данных файла MP4 установите для этого атрибута значение **мфтранскодеконтаинертипе \_ MPEG4**.
6.  Вызовите метод [**имфтранскодепрофиле:: сетконтаинераттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) , чтобы задать атрибуты уровня контейнера.

Эти действия показаны в следующем коде.


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



Чтобы указать атрибуты для видеопотока H. 264, создайте хранилище атрибутов и задайте следующие атрибуты:



| attribute                                                       | Описание                      |
|-----------------------------------------------------------------|---------------------------------|
| [**подтип MF \_ MT \_**](mf-mt-subtype-attribute.md)              | Задайте для параметра значение **мфвидеоформат \_ H264 Single bitrate**. |
| [**\_Профиль MF MT \_ MPEG2 \_**](mf-mt-mpeg2-profile-attribute.md) | Профиль H. 264.                  |
| [**\_ \_ Размер пакета MF \_ MT**](mf-mt-frame-size-attribute.md)       | Размер кадра.                     |
| [**\_ \_ Частота кадров MF \_ MT**](mf-mt-frame-rate-attribute.md)       | Частота кадров.                     |
| [**\_ \_ Средняя скорость MF \_ MT**](mf-mt-avg-bitrate-attribute.md)     | Скорость кодирования.               |



 

Чтобы указать атрибуты для аудиопотока AAC, создайте хранилище атрибутов и задайте следующие атрибуты:



| attribute                                                                                      | Описание                               |
|------------------------------------------------------------------------------------------------|------------------------------------------|
| [**подтип MF \_ MT \_**](mf-mt-subtype-attribute.md)                                             | Задайте значение **мфаудиоформат \_ AAC**            |
| [**\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду**](mf-mt-audio-samples-per-second-attribute.md)        | Частота дискретизации.                       |
| [**\_ \_ звуковый бит MF MT \_ \_ на \_ выборку**](mf-mt-audio-bits-per-sample-attribute.md)              | Пример битов на аудио.                   |
| [**\_ \_ каналы аудиосигнала MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)                     | Число аудиоканалов.                |
| [**\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md)   | Скорость кодирования.                        |
| [**\_ \_ Выравнивание звукового \_ блока MF MT \_**](mf-mt-audio-block-alignment-attribute.md)               | Задан равным 1.                                |
| [\_ \_ \_ Указание уровня звукового \_ профиля \_ MF MT AAC \_](mf-mt-aac-audio-profile-level-indication.md) | Указание уровня профиля AAC (необязательно). |



 

Следующий код создает атрибуты потока видео.


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



Следующий код создает атрибуты аудиопотока.


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



Обратите внимание, что API перекодирования не требует истинного типа мультимедиа, хотя он использует атрибуты типа мультимедиа. В частности, атрибут [**\_ \_ основного \_ типа MF MT**](mf-mt-major-type-attribute.md) не требуется, так как методы [**сетвидеоаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) и [**сетаудиоаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) подразумевают основной тип. Однако он также может передавать в эти методы фактический тип мультимедиа. (Интерфейс [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) наследует [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).)

### <a name="run-the-encoding-session"></a>Запуск сеанса кодирования

Следующий код запускает сеанс кодирования. В нем используется класс поддержки сеанса мультимедиа, который показан в следующем разделе.


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



## <a name="media-session-helper"></a>Вспомогательный модуль сеанса мультимедиа

[Сеанс мультимедиа](media-session.md) описан более подробно в разделе [архитектура Media Foundation](media-foundation-architecture.md) этой документации. В сеансе мультимедиа используется асинхронная модель событий. В приложении GUI следует реагировать на события сеанса, не блокируя поток пользовательского интерфейса для ожидания следующего события. В руководстве по [воспроизведению незащищенных файлов мультимедиа](how-to-play-unprotected-media-files.md) показано, как это сделать в приложении воспроизведения. Для кодировки принцип является тем же, но имеет значение меньшее количество событий:



| Событие                                  | Описание                                                                                                                                                       |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [месессионендед](mesessionended.md)   | Возникает после завершения кодирования.                                                                                                                            |
| [месессионклосед](mesessionclosed.md) | Возникает при завершении метода [**имфмедиасессион:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) . После возникновения этого события можно спокойно завершить сеанс мультимедиа. |



 

Для консольного приложения разумно блокировать и ожидать события. В зависимости от исходного файла и параметров кодировки для завершения кодирования может потребоваться некоторое время. Обновления хода выполнения можно получить следующим образом:

1.  Вызовите [**имфмедиасессион:: Clock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) , чтобы получить часы презентации.
2.  Запросите часы для интерфейса [**имфпресентатионклокк**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) .
3.  Чтобы получить текущую точку, вызовите метод [**имфпресентатионклокк:: Time**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) .
4.  Это значение указывается в единицах времени. Чтобы получить процент завершения, используйте значение `(100 * position) / duration` .

Ниже приведено объявление `CSession` класса.


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



В следующем коде показана полная реализация `CSession` класса.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Кодировщик AAC**](aac-encoder.md)
</dt> <dt>

[**Кодировщик видео H. 264**](h-264-video-encoder.md)
</dt> <dt>

[Сеанс мультимедиа](media-session.md)
</dt> <dt>

[Типы носителей](media-types.md)
</dt> <dt>

[API перекодирования](transcode-api.md)
</dt> </dl>

 

 
