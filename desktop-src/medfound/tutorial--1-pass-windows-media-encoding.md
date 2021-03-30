---
description: Кодирование означает процесс преобразования цифрового мультимедиа из одного формата в другой. Например, преобразование MP3 Audio в формат Windows Media Audio в соответствии со спецификацией ASF.
ms.assetid: 4fe202d8-c8f5-4e9a-ad40-1aea8f767362
title: Учебник. 1. Передача кодирования мультимедиа Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d670b107f315966a048a2f847183431f9a57bd4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820301"
---
# <a name="tutorial-1-pass-windows-media-encoding"></a>Учебник. 1. Передача кодирования мультимедиа Windows

Кодирование означает процесс преобразования цифрового мультимедиа из одного формата в другой. Например, преобразование MP3 Audio в формат Windows Media Audio в соответствии со спецификацией ASF.

**Примечание**  .  Спецификация ASF определяет тип контейнера для выходного файла (. WMA или. wmv), который может содержать данные мультимедиа в любом формате, сжатом или несжатом. Например, контейнер ASF, такой как WMA-файл, может содержать данные мультимедиа в формате MP3. Процесс кодирования преобразует фактический формат данных, содержащихся в файле.

В этом руководстве демонстрируется кодирование источника входных данных (без защиты от DRM) в содержимое Windows Media и запись их в новый файл ASF (. WM \* ) с использованием компонентов ASF уровня конвейера. Эти компоненты будут использоваться для создания топологии с частичным кодированием, которая будет управляться экземпляром сеанса мультимедиа.

В этом руководстве вы создадите консольное приложение, которое принимает входные и выходные имена файлов, а также режим кодирования в качестве аргументов. Входной файл может находиться в сжатом или несжатом формате носителя. Допустимыми режимами кодирования являются "CBR" (Постоянная скорость потока) или "VBR" (переменная скорость). Приложение создает источник мультимедиа, который представляет источник, указанный в имени входного файла, и приемник ASF-файлов для архивации закодированного содержимого исходного файла в ASF-файл. Чтобы обеспечить простоту реализации сценария, выходной файл будет иметь только один звуковой поток и один поток видео. Приложение вставляет кодек Windows Media Audio 9,1 Professional для преобразования формата звукового потока и кодек Windows Media Video 9 для видеопотока.

Для кодирования постоянной скорости потока перед началом сеанса кодирования кодировщику необходимо указать целевую скорость, которую он должен достичь. В этом руководстве для режима "CBR" приложение использует скорость потока, доступную в первом выходном типе носителя, который извлекается из кодировщика во время согласования типа носителя в качестве целевой скорости. В этом учебнике в этом руководстве демонстрируется кодирование с переменной скоростью, задавая уровень качества. Звуковые потоки кодируются на уровне качества 98 и видеопотоков на уровне качества 95.

Следующая процедура описывает действия по кодированию содержимого мультимедиа Windows в контейнере ASF с помощью 1-проходного режима кодирования.

1.  Создайте источник мультимедиа для указанного с помощью сопоставителя источников.
2.  Перечисление потоков в источнике мультимедиа.
3.  Создайте приемник мультимедиа ASF и добавьте приемники потоков в зависимости от потоков в источнике носителя, который необходимо закодировать.
4.  Настройте приемник мультимедиа с требуемыми свойствами кодировки.
5.  Создайте кодировщики Windows Media для потоков в выходном файле.
6.  Настройте кодировщики с помощью свойств, установленных в приемнике мультимедиа.
7.  Создайте неполную топологию кодирования.
8.  Создайте экземпляр сеанса мультимедиа и задайте топологию для сеанса мультимедиа.
9.  Запустите сеанс кодирования, управляя сеансом мультимедиа и получением всех соответствующих событий из сеанса мультимедиа.
10. Для кодирования VBR получите значения свойств кодировки из кодировщика и задайте их в приемнике мультимедиа.
11. Закройте и завершите сеанс кодирования.

Этот учебник содержит следующие подразделы:

-   [Предварительные условия](#prerequisites)
-   [Настройка проекта](#set-up-the-project)
-   [Создание источника мультимедиа](#create-the-media-source)
-   [Создание приемника файлов ASF](#create-the-asf-file-sink)
    -   [Создание объекта профиля ASF](#create-the-asf-profile-object)
    -   [Создание типа сжатого звукового носителя](#create-a-compressed-audio-media-type)
    -   [Создание типа носителя с сжатым видео](#create-a-compressed-video-media-type)
    -   [Создание объекта Контентинфо ASF](#create-the-asf-contentinfo-object)
    -   [Создание приемника файлов ASF](#create-the-asf-file-sink)
-   [Создание топологии частичной кодировки](#build-the-partial-encoding-topology)
    -   [Создание исходного узла топологии для источника мультимедиа](#create-the-source-topology-node-for-the-media-source)
    -   [Создайте экземпляры требуемых кодировщиков и создавайте узлы преобразования.](#instantiate-the-required-encoders-and-create-the-transform-nodes)
    -   [Создание выходных узлов топологии для приемника файлов](#create-the-output-topology-nodes-for-the-file-sink)
    -   [Подключение узлов источника, преобразования и приемника](#connect-the-source-transform-and-sink-nodes)
-   [Обработка сеанса кодирования](#handling-the-encoding-session)
-   [Обновление свойств кодировки в приемнике файла](#update-encoding-properties-in-the-file-sink)
-   [Реализация Main](#implement-main)
-   [Проверка выходного файла](#test-the-output-file)
-   [Распространенные коды ошибок и советы по отладке](#common-error-codes-and-debugging-tips)
-   [См. также](#related-topics)

## <a name="prerequisites"></a>Предварительные условия

В этом учебнике предполагается следующее:

-   Вы знакомы со [структурой файлов ASF](asf-file-structure.md), [компоненты ASF уровня конвейера](pipeline-layer-asf-components.md) , предоставляемые Media Foundation для работы с объектами ASF. К этим компонентам относятся следующие объекты:
    -   [Источники мультимедиа](media-sources.md)

        **Примечание**  .  Если вы выполняете преобразование (преобразуя файл более высокой разрядной скорости в файл с меньшей скоростью, не изменяя форматы), вы будете использовать [источник медиа ASF](asf-media-source.md).

    -   [Кодировщики Windows Media](windows-media-encoders.md)
    -   [Приемники мультимедиа ASF](asf-media-sinks.md)
    -   [Объект Контентинфо ASF](asf-contentinfo-object.md)
    -   [Профиль ASF](asf-profile.md)

-   Вы знакомы с кодировщиками Windows Media, а также с различными типами кодировок, в частности с [постоянным кодированием битовой скорости](constant-bit-rate-encoding.md) и [кодированием битовой переменной на основе качества](quality-based-variable-bit-rate--vbr--encoding.md).
-   Вы знакомы с операциями MFT кодировщика. В частности, создание экземпляра кодировщика и установка входных и выходных типов в кодировщике.
-   Вы знакомы с объектами топологии и созданием топологии кодирования. Дополнительные сведения о топологиях и узлах топологии см. в разделе [Создание топологий](creating-topologies.md).
-   Вы знакомы с моделью событий [сеанса мультимедиа](media-session.md)и операциями управления потоком. Дополнительные сведения см. в разделе [события сеанса мультимедиа](media-session-events.md).

## <a name="set-up-the-project"></a>Настройка проекта

1.  Включите в исходный файл следующие заголовки:

    ```C++
    #include <new>
    #include <mfidl.h>            // Media Foundation interfaces
    #include <mfapi.h>            // Media Foundation platform APIs
    #include <mferror.h>        // Media Foundation error codes
    #include <wmcontainer.h>    // ASF-specific components
    #include <wmcodecdsp.h>        // Windows Media DSP interfaces
    #include <Dmo.h>            // DMO objects
    #include <uuids.h>            // Definition for FORMAT_VideoInfo
    #include <propvarutil.h>
    
    ```

    

2.  Ссылка на следующие файлы библиотеки:

    ```C++
    // The required link libraries 
    #pragma comment(lib, "mfplat")
    #pragma comment(lib, "mf")
    #pragma comment(lib, "mfuuid")
    #pragma comment(lib, "msdmo")
    #pragma comment(lib, "strmiids")
    #pragma comment(lib, "propsys")
    
    ```

    

3.  Объявите функцию [саферелеасе](saferelease.md) .

    ```C++
    template <class T> void SafeRelease(T **ppT)
    {
        if (*ppT)
        {
            (*ppT)->Release();
            *ppT = NULL;
        }
    }
    ```

    

4.  Объявите \_ перечисление режима кодирования для определения типов кодирования CBR и VBR.

    ```C++
    // Encoding mode
    typedef enum ENCODING_MODE {
      NONE  = 0x00000000,
      CBR   = 0x00000001,
      VBR   = 0x00000002,
    } ;
    
    ```

    

5.  Определите константу окна буфера для видеопотока.

    ```C++
    // Video buffer window
    const INT32 VIDEO_WINDOW_MSEC = 3000;
    
    ```

    

## <a name="create-the-media-source"></a>Создание источника мультимедиа

Создайте источник носителя для источника входных данных. Media Foundation предоставляет встроенные источники мультимедиа для различных форматов мультимедиа: MP3, MP4/3GP, AVI/WAVE. Сведения о форматах, поддерживаемых Media Foundation, см. [в разделе Поддерживаемые форматы мультимедиа в Media Foundation](supported-media-formats-in-media-foundation.md).

Чтобы создать источник мультимедиа, используйте [сопоставитель источника](source-resolver.md). Этот объект анализирует URL-адрес, указанный для исходного файла, и создает соответствующий источник мультимедиа.

Выполните следующие вызовы:

-   [**мфкреатесаурцересолвер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver)
-   [**Имфсаурцересолвер:: Креатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)

    Дополнительные сведения об этих вызовах см. [в разделе Использование сопоставителя источников](using-the-source-resolver.md).

    Если входной файл имеет формат ASF и вы хотите преобразовать его в другой файл с битовой скоростью без изменения формата, то исходный поисковый компьютер создает экземпляр [источника мультимедиа ASF](asf-media-source.md).

В следующем примере кода показана функция Креатемедиасаурце, которая создает источник мультимедиа для указанного файла.


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="create-the-asf-file-sink"></a>Создание приемника файлов ASF

Создайте экземпляр приемника файлов ASF, который будет архивировать закодированные данные мультимедиа в файл ASF в конце сеанса кодирования.

В этом руководстве вы создадите объект активации для приемника файлов ASF. Чтобы создать необходимые приемники потоков, приемнику файла необходимы следующие сведения.

-   Потоки, которые должны быть закодированы и записаны в окончательный файл.
-   Свойства кодировки, используемые для кодирования мультимедийного содержимого, такие как тип кодирования, число проходов кодирования и связанные свойства.
-   Глобальные свойства файла, указывающие на приемник мультимедиа, следует ли автоматически настраивать параметры сегмента утечки (скорость и размер буфера).

Сведения о потоке настраиваются в объекте профиля ASF, а свойства Encoding и Global задаются в хранилище свойств, управляемом объектом ASF Контентинфо.

Общие сведения о приемнике файлов ASF см. в статье [приемники мультимедиа ASF](asf-media-sinks.md).

### <a name="create-the-asf-profile-object"></a>Создание объекта профиля ASF

Чтобы приемник файлов ASF написал закодированные данные мультимедиа в файл ASF, приемнику необходимо получить сведения о количестве потоков и типе потоков, для которых создаются приемники потоков. В этом учебнике вы извлечете эти сведения из источника мультимедиа и создадите соответствующие выходные потоки. Ограничьте выходные потоки одним звуковым потоком и одним видеопотоком. Для каждого выбранного потока в источнике Создайте целевой поток и добавьте его в профиль.

Для реализации этого шага необходимы следующие объекты.

-   [Профиль ASF](asf-profile.md)
-   Дескриптор представления для источника мультимедиа
-   Дескрипторы потоков для выбранных потоков в источнике мультимедиа.
-   Типы носителей для выбранных потоков.

Ниже описан процесс создания профиля ASF и целевых потоков.

**Создание профиля ASF**

1.  Вызовите [**мфкреатеасфпрофиле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) , чтобы создать пустой объект профиля.
2.  Вызовите [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) , чтобы создать дескриптор представления для источника мультимедиа, созданного на шаге, описанном в разделе "Создание источника мультимедиа" этого руководства.
3.  Вызовите [**имфпресентатиондескриптор:: жетстреамдескрипторкаунт**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) , чтобы получить количество потоков в источнике мультимедиа.
4.  Вызовите [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) для каждого потока в источнике мультимедиа и получите дескриптор потока потока.
5.  Вызовите [**имфстреамдескриптор:: жетмедиатипехандлер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) , а затем [**Имфмедиатипехандлер:: жетмедиатипебиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) и получите первый тип носителя для потока.

    **Примечание**   .   Чтобы избежать сложных вызовов, предположим, что для каждого потока существует только один тип мультимедиа и выбирается первый тип носителя потока. Для сложных потоков необходимо перечислить каждый тип носителя из обработчика типа мультимедиа и выбрать тип носителя для кодирования.

6.  Вызовите метод I [**имфмедиатипе:: жетмажортипе**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) , чтобы получить основной тип потока, чтобы определить, содержит ли поток аудио или видео.
7.  В зависимости от основного типа потока Создайте типы целевых носителей. Эти типы носителей будут содержать сведения о формате, которые будут использоваться кодировщиком во время сеанса кодирования. В следующих разделах этого руководства описывается процесс создания типов целевых носителей.
    -   Создание типа сжатого звукового носителя
    -   Создание типа носителя с сжатым видео
8.  Создайте поток на основе типа целевого носителя, настройте поток в соответствии с требованиями приложения и добавьте поток в профиль. Дополнительные сведения см. в разделе [Добавление потоковых данных в приемник файлов ASF](adding-stream-information-to-the-asf-file-sink.md).

    1.  Вызовите [**имфасфпрофиле:: креатестреам**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) и передайте целевой тип носителя, чтобы создать выходной поток. Метод получает интерфейс Имфасфстреамконфиг объекта потока.
    2.  Настройте поток.
        -   Вызовите метод [**имфасфстреамконфиг:: сетстреамнумбер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) , чтобы присвоить номер потоку. Этот параметр является обязательным.
        -   При необходимости настройте параметры контейнера утечки, расширение полезных данных, взаимное исключение для каждого потока, вызвав методы [**имфасфстреамконфиг**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) и соответствующие атрибуты конфигурации потока.
    3.  Добавьте свойства кодировки уровня потока с помощью объекта ASF Контентинфо. Дополнительные сведения об этом шаге см. в подразделе «Создание объекта ASF Контентинфо» этого руководства.
    4.  Вызовите [**имфасфпрофиле:: сетстреам**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) , чтобы добавить поток в профиль.

    В следующем примере кода создается выходной поток звука.

    ```C++
    //-------------------------------------------------------------------
    //  CreateAudioStream
    //  Create an audio stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //-------------------------------------------------------------------

    HRESULT CreateAudioStream(IMFASFProfile* pProfile, WORD wStreamNumber)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        IMFMediaType* pAudioType = NULL;
        IMFASFStreamConfig* pAudioStream = NULL;
        
        //Create an output type from the encoder
        HRESULT hr = GetOutputTypeFromWMAEncoder(&pAudioType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Create a new stream with the audio type
        hr = pProfile->CreateStream(pAudioType, &pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set stream number
        hr = pAudioStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Add the stream to the profile
        hr = pProfile->SetStream(pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Audio Stream created. Stream Number: %d.\n", wStreamNumber);

    done:
        SafeRelease(&pAudioStream);
        SafeRelease(&pAudioType);
        return hr;
    }
    ```

    

    В следующем примере кода создается выходной поток видео.

    ```C++
    //-------------------------------------------------------------------
    //  CreateVideoStream
    //  Create an video stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //    pType: A pointer to the source's video media type.
    //-------------------------------------------------------------------

    HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        HRESULT hr = S_OK;

        
        IMFMediaType* pVideoType = NULL;
        IMFASFStreamConfig* pVideoStream = NULL;

        UINT32 dwBitRate = 0;
            
        //Create a new video type from the source type
        hr = CreateCompressedVideoType(pType, &pVideoType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Create a new stream with the video type
        hr = pProfile->CreateStream(pVideoType, &pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }
        

        //Set a valid stream number
        hr = pVideoStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }

        //Add the stream to the profile
        hr = pProfile->SetStream(pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

    done:

        SafeRelease(&pVideoStream);
        SafeRelease(&pVideoType);

        return hr;
    }
    ```

    

В следующем примере кода создаются выходные потоки в зависимости от потоков в источнике.


```C++
    //For each stream in the source, add target stream information in the profile
    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        //Get the media type handler
        hr = pStreamDesc->GetMediaTypeHandler(&pHandler);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the first media type 
        hr = pHandler->GetMediaTypeByIndex(0, &pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the major type
        hr = pMediaType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        // If this is a video stream, create the target video stream
        if (guidMajor == MFMediaType_Video)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateVideoStream(pProfile, wStreamID, pMediaType);

            if (FAILED(hr))
            {
                goto done;
            }
        }
        
        // If this is an audio stream, create the target audio stream
        if (guidMajor == MFMediaType_Audio)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateAudioStream(pProfile, wStreamID);

            if (FAILED(hr))
            {
                goto done;
            }
        }

        //Get stream's encoding property
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set the stream-level encoding properties
        hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
        if (FAILED(hr))
        {
            goto done;
        }


        SafeRelease(&pMediaType);
        SafeRelease(&pStreamDesc);
        SafeRelease(&pContentInfoProps);
        wStreamID++;
    }
```



### <a name="create-a-compressed-audio-media-type"></a>Создание типа сжатого звукового носителя

Если в выходной файл необходимо включить аудиопоток, создайте тип аудио, указав характеристики закодированного типа, задав необходимые атрибуты. Чтобы убедиться, что тип аудио совместим с кодировщиком Windows Media Audio, создайте экземпляр файла MFT кодировщика, задайте свойства кодировки и получите тип мультимедиа, вызвав [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype). Получите требуемый тип выходных данных, перебирая все доступные типы, получая атрибуты каждого типа мультимедиа и выбрав тип, ближайший к вашим требованиям. В этом руководстве вы получите первый доступный тип из списка типов выходных носителей, поддерживаемых кодировщиком.

**Примечание**  .  В Windows 7 Media Foundation предоставляет новую функцию [**мфтранскодежетаудиуутпутаваилаблетипес**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) , которая получает список совместимых типов аудио. Эта функция получает только типы носителей для кодирования CBR.

Для полного звукового типа должны быть заданы следующие атрибуты:

-   [**\_ \_ основной тип MF \_ MT**](mf-mt-major-type-attribute.md)
-   [**подтип MF \_ MT \_**](mf-mt-subtype-attribute.md)
-   [**\_ \_ каналы аудиосигнала MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)
-   [**\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду**](mf-mt-audio-samples-per-second-attribute.md)
-   [**\_ \_ Выравнивание звукового \_ блока MF MT \_**](mf-mt-audio-block-alignment-attribute.md)
-   [**\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [**\_ \_ звуковый бит MF MT \_ \_ на \_ выборку**](mf-mt-audio-bits-per-sample-attribute.md)

В следующем примере кода создается сжатый тип звука путем получения совместимого типа из кодировщика Windows Media Audio. Реализация для Сетенкодингпропертиес показана в разделе "Создание объекта Контентинфо ASF" этого руководства.


```C++
//-------------------------------------------------------------------
//  GetOutputTypeFromWMAEncoder
//  Gets a compatible output type from the Windows Media audio encoder.
//
//  ppAudioType: Receives a pointer to the media type.
//-------------------------------------------------------------------

HRESULT GetOutputTypeFromWMAEncoder(IMFMediaType** ppAudioType)
{
    if (!ppAudioType)
    {
        return E_POINTER;
    }

    IMFTransform* pMFT = NULL;
    IMFMediaType* pType = NULL;
    IPropertyStore* pProps = NULL;

    //We need to find a suitable output media type
    //We need to create the encoder to get the available output types
    //and discard the instance.

    CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
    UINT32 cCLSID = 0;            // Size of the array.

    MFT_REGISTER_TYPE_INFO tinfo;
    
    tinfo.guidMajorType = MFMediaType_Audio;
    tinfo.guidSubtype = MFAudioFormat_WMAudioV9;

    // Look for an encoder.
    HRESULT hr = MFTEnum(
        MFT_CATEGORY_AUDIO_ENCODER,
        0,                  // Reserved
        NULL,                // Input type to match. None.
        &tinfo,             // WMV encoded type.
        NULL,               // Attributes to match. (None.)
        &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
        &cCLSID             // Receives the size of the array.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // MFTEnum can return zero matches.
    if (cCLSID == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
        goto done;
    }
    else
    {
        // Create the MFT decoder
        hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));

        if (FAILED(hr))
        {
            goto done;
        }

    }

    // Get the encoder's property store

    hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Set encoding properties
    hr = SetEncodingProperties(MFMediaType_Audio, pProps);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get the first output type
    //You can loop through the available output types to choose 
    //the one that meets your target requirements
    hr = pMFT->GetOutputAvailableType(0, 0, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return to the caller
    *ppAudioType = pType;
    (*ppAudioType)->AddRef();
    
done:
    SafeRelease(&pProps);
    SafeRelease(&pType);
    SafeRelease(&pMFT);
    CoTaskMemFree(pMFTCLSIDs);
    return hr;
}
```



### <a name="create-a-compressed-video-media-type"></a>Создание типа носителя с сжатым видео

Если вы хотите включить в выходной файл поток видео, создайте тип видео с полным кодированием. Полный тип носителя должен включать требуемую скорость потока и частные данные кодека.

Существует два способа создания носителя с полным типом видео.

-   Создайте пустой тип мультимедиа и скопируйте атрибуты типа мультимедиа из исходного видеотипа и перезапишите атрибут [**\_ \_ подтипа MF MT**](mf-mt-subtype-attribute.md) с помощью константы GUID мфвидеоформат \_ WMV3.

    Для полного типа видео должны быть заданы следующие атрибуты:

    -   \_ \_ основной тип MF \_ MT
    -   подтип MF \_ MT \_
    -   \_ \_ Частота кадров MF \_ MT
    -   \_ \_ Размер пакета MF \_ MT
    -   \_ \_ режим чересстрочную РАЗВЕРТКи MF \_
    -   пропорции MF \_ MT \_ пикселей \_ \_
    -   \_ \_ Средняя скорость MF \_ MT
    -   \_ \_ данные пользователя MF \_ MT

    В следующем примере кода создается сжатый тип видео из типа видео источника.

    ```C++
    //-------------------------------------------------------------------
    //  CreateCompressedVideoType
    //  Creates an output type from source's video media type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateCompressedVideoType(
            IMFMediaType* pType, 
            IMFMediaType** ppVideoType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppVideoType)
        {
            return E_POINTER;
        }
        
        HRESULT hr = S_OK;
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 fSamplesIndependent = 0;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->CopyAllItems(pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Fill the missing attributes
        //1. Frame rate
        hr = MFGetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

            hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////2. Frame size
        hr = MFGetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;
                
            hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////3. Interlace mode
        
        if (FAILED(pMediaType->GetUINT32(MF_MT_INTERLACE_MODE, &interlace)))
        {
            hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        ////4. Pixel aspect Ratio
        hr = MFGetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            par.Numerator = par.Denominator = 1;
            hr = MFSetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32)par.Numerator, (UINT32)par.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        //6. bit rate
        if (FAILED(pMediaType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate)))
        {
            hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, 1000000);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_WMV3);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppVideoType = pMediaType;
        (*ppVideoType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    
    ```

    

-   Получите совместимый тип мультимедиа от кодировщика видео Windows Media, задав свойства кодировки и вызвав [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype). Этот метод возвращает частичный тип. Убедитесь, что разделяемый тип преобразован в полный тип, добавив следующие сведения:

    -   Установите скорость воспроизведения видео в атрибуте [**" \_ \_ Средняя \_ скорость" MF MT**](mf-mt-avg-bitrate-attribute.md) .
    -   Добавьте частные данные кодека, задав [**атрибут \_ \_ \_ данных пользователя MF MT**](mf-mt-user-data-attribute.md) . Подробные инструкции см. в разделе "данные частного кодека" раздела [Настройка кодировщика WMV](configuring-a-wmv-encoder.md).

    Так как [**ивмкодекприватедата:: жетприватедата**](../wmformat/iwmcodecprivatedata-getprivatedata.md) проверяет скорость потока перед возвратом частных данных кодека, перед получением частных данных кодека необходимо установить скорость.

    В следующем примере кода создается сжатый тип видео путем получения совместимого типа из кодировщика видео Windows Media. Он также создает несжатый тип видео и задает его в качестве входных данных кодировщика. Это реализуется в вспомогательной функции Креатеункомпресседвидеотипе. Жетаутпуттипефромвмвенкодер преобразует возвращаемый разделяемый тип в полный тип путем добавления частных данных кодека. Реализация для Сетенкодингпропертиес показана в разделе "Создание объекта Контентинфо ASF" этого руководства.

    ```C++
    //-------------------------------------------------------------------
    //  GetOutputTypeFromWMVEncoder
    //  Gets a compatible output type from the Windows Media video encoder.
    //
    //  pType: A pointer to the source video stream's media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT GetOutputTypeFromWMVEncoder(IMFMediaType* pType, IMFMediaType** ppVideoType)
    {
        if (!ppVideoType)
        {
            return E_POINTER;
        }

        IMFTransform* pMFT = NULL;
        IPropertyStore* pProps = NULL;
        IMFMediaType* pInputType = NULL;
        IMFMediaType* pOutputType = NULL;
        
        UINT32 cBitrate = 0;

        //We need to find a suitable output media type
        //We need to create the encoder to get the available output types
        //and discard the instance.

        CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
        UINT32 cCLSID = 0;          // Size of the array.

        MFT_REGISTER_TYPE_INFO tinfo;
        
        tinfo.guidMajorType = MFMediaType_Video;
        tinfo.guidSubtype = MFVideoFormat_WMV3;

        // Look for an encoder.
        HRESULT hr = MFTEnum(
            MFT_CATEGORY_VIDEO_ENCODER,
            0,                  // Reserved
            NULL,               // Input type to match. None.
            &tinfo,             // WMV encoded type.
            NULL,               // Attributes to match. (None.)
            &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
            &cCLSID             // Receives the size of the array.
            );
        if (FAILED(hr))
        {
            goto done;
        }

        // MFTEnum can return zero matches.
        if (cCLSID == 0)
        {
            hr = MF_E_TOPO_CODEC_NOT_FOUND;
            goto done;
        }
        else
        {
            //Create the MFT decoder
            hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
                CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));
            if (FAILED(hr))
            {
                goto done;
            }

        }
        
        //Get the video encoder property store
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
        if (FAILED(hr))
        {
            goto done;
        }

        //Set encoding properties
        hr = SetEncodingProperties(MFMediaType_Video, pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = CreateUncompressedVideoType(pType, &pInputType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMFT->SetInputType(0, pInputType, 0);

        //Get the first output type
        //You can loop through the available output types to choose 
        //the one that meets your target requirements
        hr =  pMFT->GetOutputAvailableType(0, 0, &pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        //Now set the bit rate
        hr = pOutputType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddPrivateData(pMFT, pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Return to the caller
        *ppVideoType = pOutputType;
        (*ppVideoType)->AddRef();
        
    done:
        SafeRelease(&pProps);
        SafeRelease(&pOutputType);
        SafeRelease(&pInputType);
        SafeRelease(&pMFT);
        CoTaskMemFree(pMFTCLSIDs);
        return hr;
    }
    ```

    

    В следующем примере кода создается несжатый тип видео.

    ```C++
    //-------------------------------------------------------------------
    //  CreateUncompressedVideoType
    //  Creates an uncompressed video type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateUncompressedVideoType(IMFMediaType* pType, IMFMediaType** ppMediaType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppMediaType)
        {
            return E_POINTER;
        }
        
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        HRESULT hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFGetAttributeRatio(pType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

        }
        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;

        }

        interlace = MFGetAttributeUINT32(pType, MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);

        hr = MFGetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (FAILED(hr))
        {
            par.Numerator = par.Denominator = 1;
        }

        cBitrate = MFGetAttributeUINT32(pType, MF_MT_AVG_BITRATE, 1000000);

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_MAJOR_TYPE, guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_RGB32);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, 2);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppMediaType = pMediaType;
        (*ppMediaType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    ```

    

    В следующем примере кода частные данные кодека добавляются в указанный тип видеоматериала.

    ```C++
    //
    // AddPrivateData
    // Appends the private codec data to a media type.
    //
    // pMFT: The video encoder
    // pTypeOut: A video type from the encoder's type list.
    //
    // The function modifies pTypeOut by adding the codec data.
    //

    HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
    {
        HRESULT hr = S_OK;
        ULONG cbData = 0;
        BYTE *pData = NULL;

        IWMCodecPrivateData *pPrivData = NULL;

        DMO_MEDIA_TYPE mtOut = { 0 };

        // Convert the type to a DMO type.
        hr = MFInitAMMediaTypeFromMFMediaType(
            pTypeOut, 
            FORMAT_VideoInfo, 
            (AM_MEDIA_TYPE*)&mtOut
            );
        
        if (SUCCEEDED(hr))
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
        }

        if (SUCCEEDED(hr))
        {
            hr = pPrivData->SetPartialOutputType(&mtOut);
        }

        //
        // Get the private codec data
        //

        // First get the buffer size.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(NULL, &cbData);
        }

        if (SUCCEEDED(hr))
        {
            pData = new BYTE[cbData];

            if (pData == NULL)
            {
                hr = E_OUTOFMEMORY;
            }
        }

        // Now get the data.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(pData, &cbData);
        }

        // Add the data to the media type.
        if (SUCCEEDED(hr))
        {
            hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
        }

        delete [] pData;
        MoFreeMediaType(&mtOut);
        SafeRelease(&pPrivData);
        return hr;
    }
    ```

    

### <a name="create-the-asf-contentinfo-object"></a>Создание объекта Контентинфо ASF

Объект ASF Контентинфо является компонентом уровня Вмконтаинер, который в основном предназначен для хранения сведений об объекте заголовка ASF. Приемник ASF-файлов реализует объект Контентинфо для хранения сведений (в хранилище свойств), которые будут использоваться для записи объекта заголовка ASF закодированного файла. Для этого необходимо создать и настроить следующий набор данных для объекта Контентинфо перед началом сеанса кодирования.

1.  Вызовите [**мфкреатеасфконтентинфо**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , чтобы создать пустой объект контентинфо.

    В следующем примере кода создается пустой объект Контентинфо.

    ```C++
        // Create an empty ContentInfo object
        hr = MFCreateASFContentInfo(&pContentInfo);
        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  Вызовите [**имфасфконтентинфо:: жетенкодингконфигуратионпропертисторе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) , чтобы получить хранилище свойств уровня потока для приемника файла. В этом вызове необходимо передать номер потока, назначенный для потока, при создании профиля ASF.
3.  Задайте [Свойства кодировки](configuring-the-encoder.md) на уровне потока в хранилище свойств потока для приемника файла. Дополнительные сведения см. в разделе "свойства кодировки потока" раздела [Задание свойств в приемнике файла](setting-properties-in-the-file-sink.md).

    В следующем примере кода устанавливаются свойства уровня потока в хранилище свойств приемника файла.

    ```C++
            //Get stream's encoding property
            hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
            if (FAILED(hr))
            {
                goto done;
            }

            //Set the stream-level encoding properties
            hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
            if (FAILED(hr))
            {
                goto done;
            }

    
    ```

    

    В следующем примере кода показана реализация для Сетенкодингпропертиес. Эта функция задает свойства кодирования на уровне потока для CBR и VBR.

    ```C++
    //-------------------------------------------------------------------
    //  SetEncodingProperties
    //  Create a media source from a URL.
    //
    //  guidMT:  Major type of the stream, audio or video
    //  pProps:  A pointer to the property store in which 
    //           to set the required encoding properties.
    //-------------------------------------------------------------------

    HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
    {
        if (!pProps)
        {
            return E_INVALIDARG;
        }

        if (EncodingMode == NONE)
        {
            return MF_E_NOT_INITIALIZED;
        }
       
        HRESULT hr = S_OK;

        PROPVARIANT var;

        switch (EncodingMode)
        {
            case CBR:
                // Set VBR to false.
                hr = InitPropVariantFromBoolean(FALSE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the video buffer window.
                if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            case VBR:
                //Set VBR to true.
                hr = InitPropVariantFromBoolean(TRUE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Number of encoding passes is 1.

                hr = InitPropVariantFromInt32(1, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the quality level.

                if (guidMT == MFMediaType_Audio)
                {
                    hr = InitPropVariantFromUInt32(98, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                else if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromUInt32(95, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            default:
                hr = E_UNEXPECTED;
                break;
        }    

    done:
        PropVariantClear(&var);
        return hr;
    }
    ```

    

4.  Вызовите [**имфасфконтентинфо:: жетенкодингконфигуратионпропертисторе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) , чтобы получить глобальное хранилище свойств приемника файла. В этом вызове необходимо передать 0 в первом параметре. Дополнительные сведения см. в разделе "свойства глобального приемника файлов" раздела [Настройка свойств в приемнике файла](setting-properties-in-the-file-sink.md).
5.  Установите для параметра [**мфпкэй \_ АСФМЕДИАСИНК \_ Автокорректировка \_ скорость**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) значение Variant \_ true, чтобы значения сегмента утечки в мультиплексоре ASF были правильно настроены. Сведения об этом свойстве см. в разделе "Инициализация мультиплексора и параметры сегмента утечки" раздела [Создание объекта мультиплексора](creating-the-multiplexer-object.md).

    В следующем примере кода устанавливаются свойства уровня потока в хранилище свойств приемника файла.

    ```C++
        //Now we need to set global properties that will be set on the media sink
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(0, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Auto adjust Bitrate
        var.vt = VT_BOOL;
        var.boolVal = VARIANT_TRUE;

        hr = pContentInfoProps->SetValue(MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE, var);
        
        //Initialize with the profile
        hr = pContentInfo->SetProfile(pProfile);
        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

    > [!Note]  
    > Существуют и другие свойства, которые можно задать на глобальном уровне для приемника файла. Дополнительные сведения см. в разделе "Настройка объекта Контентинфо с помощью параметров кодировщика" раздела [Настройка свойств в объекте контентинфо](setting-properties-in-the-contentinfo-object.md).

     

Вы будете использовать настроенный ASF Контентинфо для создания объекта активации для приемника файлов ASF (описывается в следующем разделе).

При создании необработанного приемника файла ([**мфкреатеасфмедиасинкактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)), который использует объект активации, можно использовать настроенный объект контентинфо для создания экземпляра приемника ASF Media (описывается в следующем разделе). Если создается внутрипроцессный приемник файлов ([**мфкреатеасфмедиасинк**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)), вместо создания пустого объекта контентинфо, как описано в шаге 1, получите ссылку на интерфейс [**имфасфконтентинфо**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , вызвав **имфмедиасинк:: QueryInterface** в приемнике файла. Затем необходимо настроить объект Контентинфо, как описано в этом разделе.

### <a name="create-the-asf-file-sink"></a>Создание приемника файлов ASF

На этом этапе работы с руководством вы будете использовать настроенный файл ASF Контентинфо, созданный на предыдущем шаге, для создания объекта активации для приемника файлов ASF путем вызова функции [**мфкреатеасфмедиасинкактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) . Дополнительные сведения см. [в разделе Создание приемника файлов ASF](creating-the-asf-file-sink.md).

В следующем примере кода создается объект активации для приемника файла.


```C++
    //Create the activation object for the  file sink
    hr = MFCreateASFMediaSinkActivate(sURL, pContentInfo, &pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

```



## <a name="build-the-partial-encoding-topology"></a>Создание топологии частичной кодировки

Далее предстоит создать топологию с частичным кодированием, создав узлы топологии для источника мультимедиа, необходимые кодировщики Windows Media и приемник ASF-файлов. После добавления узлов топологии вы подключаете узлы источника, преобразования и приемника. Перед добавлением узлов топологии необходимо создать пустой объект Topology, вызвав [**мфкреатетопологи**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).

### <a name="create-the-source-topology-node-for-the-media-source"></a>Создание исходного узла топологии для источника мультимедиа

На этом шаге вы создадите узел топологии источника для источника мультимедиа.

Для создания этого узла необходимы следующие ссылки:

-   Указатель на источник мультимедиа, созданный на шаге, описанном в разделе "Создание источника мультимедиа" этого руководства.
-   Указатель на дескриптор представления для источника мультимедиа. Ссылку на интерфейс Имфпресентатиондескриптор источника мультимедиа можно получить, вызвав [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).
-   Указатель на дескриптор потока для каждого потока в источнике мультимедиа, для которого был создан целевой поток на шаге, описанном в разделе "Создание объекта профиля ASF" этого руководства.

Дополнительные сведения о создании исходных узлов и пример кода см. в разделе [Создание исходных узлов](creating-source-nodes.md).

В следующем примере кода создается частичная топология путем добавления исходного узла и требуемых узлов преобразования. Этот код вызывает вспомогательные функции Аддсаурценоде и Аддтрансформаутпутнодес. Эти функции включены далее в этом руководстве.


```C++
//-------------------------------------------------------------------
//  BuildPartialTopology
//  Create a partial encoding topology by adding the source and the sink.
//
//  pSource:  A pointer to the media source to enumerate the source streams.
//  pSinkActivate: A pointer to the activation object for ASF file sink.
//  ppTopology:  Receives a pointer to the topology.
//-------------------------------------------------------------------

HRESULT BuildPartialTopology(
       IMFMediaSource *pSource, 
       IMFActivate* pSinkActivate,
       IMFTopology** ppTopology)
{
    if (!pSource || !pSinkActivate)
    {
        return E_INVALIDARG;
    }
    if (!ppTopology)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    IMFPresentationDescriptor* pPD = NULL;
    IMFStreamDescriptor *pStreamDesc = NULL;
    IMFMediaTypeHandler* pMediaTypeHandler = NULL;
    IMFMediaType* pSrcType = NULL;

    IMFTopology* pTopology = NULL;
    IMFTopologyNode* pSrcNode = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;


    DWORD cElems = 0;
    DWORD dwSrcStream = 0;
    DWORD StreamID = 0;
    GUID guidMajor = GUID_NULL;
    BOOL fSelected = FALSE;


    //Create the topology that represents the encoding pipeline
    hr = MFCreateTopology (&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

        
    hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPD->GetStreamDescriptorCount(&dwSrcStream);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        hr = AddSourceNode(pTopology, pSource, pPD, pStreamDesc, &pSrcNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamDesc->GetMediaTypeHandler (&pMediaTypeHandler);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pStreamDesc->GetStreamIdentifier(&StreamID);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaTypeHandler->GetMediaTypeByIndex(0, &pSrcType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSrcType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddTransformOutputNodes(pTopology, pSinkActivate, pSrcType, &pEncoderNode);
        if (FAILED(hr))
        {
            goto done;
        }

        //now we have the transform node, connect it to the source node
        hr = pSrcNode->ConnectOutput(0, pEncoderNode, 0);
        if (FAILED(hr))
        {
            goto done;
        }
                

        SafeRelease(&pStreamDesc);
        SafeRelease(&pMediaTypeHandler);
        SafeRelease(&pSrcType);
        SafeRelease(&pEncoderNode);
        SafeRelease(&pOutputNode);
        guidMajor = GUID_NULL;
    }

    *ppTopology = pTopology;
   (*ppTopology)->AddRef();


    wprintf_s(L"Partial Topology Built.\n");

done:
    SafeRelease(&pStreamDesc);
    SafeRelease(&pMediaTypeHandler);
    SafeRelease(&pSrcType);
    SafeRelease(&pEncoderNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pTopology);

    return hr;
}
```



В следующем примере кода создается и добавляется узел топологии источника в топологию кодирования. Он принимает указатели на ранее созданный объект Topology, источник мультимедиа для перечисления исходных потоков, дескриптор представления источника мультимедиа и дескриптор потока источника мультимедиа. Вызывающий объект получает указатель на узел исходной топологии.


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



### <a name="instantiate-the-required-encoders-and-create-the-transform-nodes"></a>Создайте экземпляры требуемых кодировщиков и создавайте узлы преобразования.

Media Foundation конвейер не вставляет необходимые кодировщики Windows Media для потоков, которые необходимо кодировать, автоматически. Приложение должно добавить кодировщики вручную. Для этого перечислите потоки в профиле ASF, которые были созданы на шаге, описанном в разделе "Создание объекта профиля ASF" этого руководства. Для каждого потока в источнике и соответствующего потока в профиле создайте экземпляр требуемых кодировщиков. Для этого шага требуется указатель на объект активации для приемника файла, созданного на шаге, описанном в подразделе "Создание приемника файлов ASF" этого руководства.

Общие сведения о создании кодировщиков с помощью объектов активации см. в разделе [использование объектов активации кодировщика](using-an-encoder-s-activation-objects.md).

Следующая процедура описывает шаги, необходимые для создания экземпляра требуемых кодировщиков.

1.  Получите ссылку на объект Контентинфо приемника, вызвав [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) в приемнике файла, и затем запросите [**имфасфконтентинфо**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) из приемника файла, вызвав **QueryInterface**.
2.  Получите профиль ASF, связанный с объектом Контентинфо, вызвав [**имфасфконтентинфо:: onprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).
3.  Перечисление потоков в профиле. Для этого потребуется число потоков и ссылка на интерфейс [**имфасфстреамконфиг**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) каждого потока.

    Вызовите следующие методы:

    -   [**Имфасфпрофиле:: Жетстреамкаунт**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)
    -   [**Имфасфпрофиле:: Stream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream)

4.  Для каждого потока получает основной тип и свойства кодировки потока из объекта Контентинфо.

    Вызовите следующие методы:

    -   [**Имфасфстреамконфиг:: Жетмедиатипе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype)
    -   [**Имфмедиатипе:: Жетмажортипе**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype)
    -   [**Имфасфконтентинфо:: Жетенкодингконфигуратионпропертисторе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)

        Для этого вызова требуется номер потока, полученный вызовом [**имфасфпрофиле:: Stream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) .

5.  В зависимости от типа потока, аудио или видео создайте экземпляр объекта активации для кодировщика, вызвав [**мфкреатевмаенкодерактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) или [**мфкреатевмвенкодерактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).

    Для вызова этих функций необходимы следующие ссылки:

    -   Указатель на тип мультимедиа потока, полученный с помощью [**имфасфстреамконфиг:: жетмедиатипе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) на предыдущем шаге.
    -   Указатель на хранилище свойств кодирования потока, полученное с помощью [**имфасфконтентинфо:: жетенкодингконфигуратионпропертисторе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore). Передавая указатель на хранилище свойств, свойства потока, заданные в приемнике файла, копируются в файл MFT кодировщика.

6.  Обновите параметр контейнера с утечкой для аудиопотока.

    [**Мфкреатевмаенкодерактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) задает тип выходных данных для основного файла MFT кодировщика для аудиокодека Windows Media Audio. После того как выходной тип носителя установлен, кодировщик получает среднюю скорость потока из выходного типа носителя, вычисляет скорость поразрядного окна буфера и устанавливает значения сегментов утечки, которые будут использоваться во время сеанса кодирования. Эти значения можно обновить в приемнике файлов, запросив кодировщика или задавая пользовательские значения. Чтобы обновить значения, требуется следующий набор данных:

    -   Средняя скорость потока: средняя скорость по скорости от среднего числа [**\_ байт MF \_ в \_ \_ \_ \_ секунду**](mf-mt-audio-avg-bytes-per-second-attribute.md) , заданных для типа выходного носителя, выбранного при согласовании типа носителя.
    -   Окно буфера. его можно извлечь, вызвав [**ивмкодеклеакибуккет:: жетбуфферсизебитс**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).
    -   Начальный размер буфера: значение 0.

    Создайте массив значений типа DWORD и задайте значение в свойстве [**мфпкэй \_ асфстреамсинк \_ исправлен \_ леакибуккет**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) приемника аудиопотока. Если не указать обновленные значения, сеанс мультимедиа задает их соответствующим образом.

    Дополнительные сведения см. [в разделе Модель буфера для сегмента утечки](the-leaky-bucket-buffer-model.md).

Объекты активации, созданные на шаге 5, должны быть добавлены в топологию как узлы топологии преобразования. Дополнительные сведения и пример кода см. в разделе «Создание узла преобразования из объекта активации» раздела [Создание узлов преобразования](creating-transform-nodes.md).

В следующем примере кода создается и добавляется требуемый кодировщик. Он принимает указатели на ранее созданный объект Topology, объект активации приемника файла и тип носителя исходного потока. Он также вызывает Аддаутпутноде (см. Следующий пример кода), который создает и добавляет узел приемника в топологию кодирования. Вызывающий объект получает указатель на узел исходной топологии.


```C++
//-------------------------------------------------------------------
//  AddTransformOutputNodes
//  Creates and adds the sink node to the encoding topology.
//  Creates and adds the required encoder activates.

//  pTopology:  A pointer to the topology.
//  pSinkActivate:  A pointer to the file sink's activation object.
//  pSourceType: A pointer to the source stream's media type.
//  ppNode:  Receives a pointer to the topology node.
//-------------------------------------------------------------------

HRESULT AddTransformOutputNodes(
    IMFTopology* pTopology,
    IMFActivate* pSinkActivate,
    IMFMediaType* pSourceType,
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    if (!pTopology || !pSinkActivate || !pSourceType)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNode* pEncNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFProfile* pProfile = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFMediaType* pMediaType = NULL;
    IPropertyStore* pProps = NULL;
    IMFActivate *pEncoderActivate = NULL;
    IMFMediaSink *pSink = NULL; 

    GUID guidMT = GUID_NULL;
    GUID guidMajor = GUID_NULL;

    DWORD cStreams = 0;
    WORD wStreamNumber = 0;

    HRESULT hr = S_OK;
        
    hr = pSourceType->GetMajorType(&guidMajor);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Activate the sink
    hr = pSinkActivate->ActivateObject(__uuidof(IMFMediaSink), (void**)&pSink);
    if (FAILED(hr))
    {
        goto done;
    }
    //find the media type in the sink
    //Get content info from the sink
    hr = pSink->QueryInterface(__uuidof(IMFASFContentInfo), (void**)&pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }
    

    hr = pContentInfo->GetProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->GetStreamCount(&cStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreams ; index++)
    {
        hr = pProfile->GetStream(index, &wStreamNumber, &pStream);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pStream->GetMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->GetMajorType(&guidMT);
        if (FAILED(hr))
        {
            goto done;
        }
        if (guidMT!=guidMajor)
        {
            SafeRelease(&pStream);
            SafeRelease(&pMediaType);
            guidMT = GUID_NULL;

            continue;
        }
        //We need to activate the encoder
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamNumber, &pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMT == MFMediaType_Audio)
        {
             hr = MFCreateWMAEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Audio Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
        if (guidMT == MFMediaType_Video)
        {
            hr = MFCreateWMVEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Video Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
    }

    // Set the object pointer.
    hr = pEncNode->SetObject(pEncoderActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output node to this node.
    hr = AddOutputNode(pTopology, pSinkActivate, wStreamNumber, &pOutputNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //now we have the output node, connect it to the transform node
    hr = pEncNode->ConnectOutput(0, pOutputNode, 0);
    if (FAILED(hr))
    {
        goto done;
    }

   // Return the pointer to the caller.
    *ppNode = pEncNode;
    (*ppNode)->AddRef();


done:
    SafeRelease(&pEncNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pEncoderActivate);
    SafeRelease(&pMediaType);
    SafeRelease(&pProps);
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    SafeRelease(&pContentInfo);
    SafeRelease(&pSink);
    return hr;
}
```



### <a name="create-the-output-topology-nodes-for-the-file-sink"></a>Создание выходных узлов топологии для приемника файлов

На этом шаге вы создадите узел выходной топологии для приемника файлов ASF.

Для создания этого узла необходимы следующие ссылки:

-   Указатель на объект активации, созданный на шаге, описанном в подразделе "Создание приемника файлов ASF" этого руководства.
-   Номера потоков для обнаружения приемников потока, добавляемых в приемник файла. Номера потоков соответствуют идентификации потока, установленного во время создания потока.

Дополнительные сведения о создании выходных узлов и пример кода см. в разделе «Создание выходного узла из объекта активации» раздела [Создание выходных узлов](creating-output-nodes.md).

Если вы не используете объект активации для приемника файла, необходимо перечислить приемники потока в приемнике файлов ASF и установить каждый приемник потока в качестве выходного узла в топологии. Дополнительные сведения о перечислении приемников потоков см. в разделе "Перечисление приемников потоков" статьи [Добавление потоковых данных в приемник файлов ASF](adding-stream-information-to-the-asf-file-sink.md).

В следующем примере кода создается и добавляется узел приемника в топологию кодирования. Он принимает указатели на ранее созданный объект Topology, объект активации приемника файла и идентификационный номер потока. Вызывающий объект получает указатель на узел исходной топологии.


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



В следующем примере кода перечисляются приемники потока для заданного приемника мультимедиа.


```C++
//-------------------------------------------------------------------
//  EnumerateStreamSinks
//  Enumerates the stream sinks within the specified media sink.
//
//  pSink:  A pointer to the media sink.
//-------------------------------------------------------------------
HRESULT EnumerateStreamSinks (IMFMediaSink* pSink)
{
    if (!pSink)
    {
        return E_INVALIDARG;
    }
    
    IMFStreamSink* pStreamSink = NULL;
    DWORD cStreamSinks = 0;

    HRESULT hr = pSink->GetStreamSinkCount(&cStreamSinks);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreamSinks; index++)
    {
        hr = pSink->GetStreamSinkByIndex (index, &pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        //Use the stream sink
        //Not shown.
    }
done:
    SafeRelease(&pStreamSink);

    return hr;
}
```



### <a name="connect-the-source-transform-and-sink-nodes"></a>Подключение узлов источника, преобразования и приемника

На этом шаге вы подключаете исходный узел к узлу преобразования, который ссылается на кодировку, которая активируется на шаге, описанном в разделе "создание экземпляров необходимых кодировщиков и создание узлов преобразования" этого руководства. Узел преобразования будет подключен к выходному узлу, содержащему объект активации для приемника файла.

## <a name="handling-the-encoding-session"></a>Обработка сеанса кодирования

На этом шаге выполняются следующие действия.

1.  Вызовите [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) , чтобы создать сеанс кодирования.
2.  Вызовите [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) , чтобы задать топологию кодирования для сеанса. Если вызов завершается, сеанс мультимедиа оценивает узлы топологии и вставляет дополнительные объекты преобразования, такие как декодер, который преобразует указанный сжатый источник в несжатые образцы в поток в качестве входных данных для кодировщика.
3.  Вызовите [**имфмедиасессион:: четный**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) , чтобы запросить события, вызванные сеансом мультимедиа.

    В цикле событий вы начнете и закроете сеанс кодирования в зависимости от событий, вызванных сеансом мультимедиа. Вызов [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) приводит к тому, что сеанс мультимедиа вызывает событие [месессионтопологистатус](mesessiontopologystatus.md) с \_ \_ установленным флагом подключения MF топостатус. Все события создаются асинхронно, и приложение может получать эти события синхронно или асинхронно. Поскольку приложение в этом руководстве является консольным приложением и блокирует потоки пользовательского интерфейса, мы будем получать события из сеанса мультимедиа синхронно.

    Для асинхронного получения событий приложение должно реализовать интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . Дополнительные сведения и пример реализации этого интерфейса см. в разделе "обработка событий сеанса" раздела [Воспроизведение мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md).

В цикле событий для получения событий сеанса мультимедиа дождитесь события [месессионтопологистатус](mesessiontopologystatus.md) , которое возникает при завершении [**Имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) и разрешении топологии. После получения события Месессионтопологистатус запустите сеанс кодирования, вызвав [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start). Сеанс мультимедиа создает событие [миндофпресентатион](meendofpresentation.md) при завершении всех операций кодирования. Это событие должно быть обработано для кодирования VBR и рассматривается в следующем разделе "Обновление свойств кодировки в приемнике файлов для кодирования VBR" этого руководства.

Сеанс мультимедиа создает объект заголовка ASF и завершает файл после завершения сеанса кодирования, а затем вызывает событие [месессионклосед](mesessionclosed.md) . Это событие должно быть обработано путем выполнения правильных операций завершения работы в сеансе мультимедиа. Чтобы начать операцию завершения работы, вызовите метод [**имфмедиасессион:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown). После закрытия сеанса кодирования нельзя задать другую топологию для кодирования в том же экземпляре сеанса мультимедиа. Для кодирования другого файла текущий сеанс мультимедиа должен быть закрыт и освобожден, а новая топология должна быть установлена во вновь созданном сеансе мультимедиа. В следующем примере кода создается сеанс мультимедиа, задается топология кодирования и обрабатываются события сеанса мультимедиа.

В следующем примере кода создается сеанс мультимедиа, задается топология кодирования и осуществляется управление сеансом кодирования путем обработки событий из сеанса мультимедиа.


```C++
//-------------------------------------------------------------------
//  Encode
//  Controls the encoding session and handles events from the media session.
//
//  pTopology:  A pointer to the encoding topology.
//-------------------------------------------------------------------

HRESULT Encode(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }
    
    IMFMediaSession *pSession = NULL;
    IMFMediaEvent* pEvent = NULL;
    IMFTopology* pFullTopology = NULL;
    IUnknown* pTopoUnk = NULL;


    MediaEventType meType = MEUnknown;  // Event type

    HRESULT hr = S_OK;
    HRESULT hrStatus = S_OK;            // Event status
                
    MF_TOPOSTATUS TopoStatus = MF_TOPOSTATUS_INVALID; // Used with MESessionTopologyStatus event.    
        

    hr = MFCreateMediaSession(NULL, &pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->SetTopology(MFSESSION_SETTOPOLOGY_IMMEDIATE, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get media session events synchronously
    while (1)
    {
        hr = pSession->GetEvent(0, &pEvent);
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

       switch(meType)
        {
            case MESessionTopologyStatus:
                {
                    // Get the status code.
                    MF_TOPOSTATUS status = (MF_TOPOSTATUS)MFGetAttributeUINT32(
                                             pEvent, MF_EVENT_TOPOLOGY_STATUS, MF_TOPOSTATUS_INVALID);

                    if (status == MF_TOPOSTATUS_READY)
                    {
                        PROPVARIANT var;
                        PropVariantInit(&var);
                        wprintf_s(L"Topology resolved and set on the media session.\n");

                        hr = pSession->Start(NULL, &var);
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                    }
                    if (status == MF_TOPOSTATUS_STARTED_SOURCE)
                    {
                        wprintf_s(L"Encoding started.\n");
                        break;
                    }
                    if (status == MF_TOPOSTATUS_ENDED)
                    {
                        wprintf_s(L"Encoding complete.\n");
                        hr = pSession->Close();
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                        break;
                    }
                }
                break;


            case MESessionEnded:
                wprintf_s(L"Encoding complete.\n");
                hr = pSession->Close();
                if (FAILED(hr))
                {
                    goto done;
                }
                break;

            case MEEndOfPresentation:
                {
                    if (EncodingMode == VBR)
                    {
                        hr = pSession->GetFullTopology(MFSESSION_GETFULLTOPOLOGY_CURRENT, 0, &pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        hr = PostEncodingUpdate(pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        wprintf_s(L"Updated sinks for VBR. \n");
                    }
                }
                break;

            case MESessionClosed:
                wprintf_s(L"Encoding session closed.\n");

                hr = pSession->Shutdown();
                goto done;
        }
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pEvent);

    }
done:
    SafeRelease(&pEvent);
    SafeRelease(&pSession);
    SafeRelease(&pFullTopology);
    SafeRelease(&pTopoUnk);
    return hr;
}
```



## <a name="update-encoding-properties-in-the-file-sink"></a>Обновление свойств кодировки в приемнике файла

Некоторые свойства кодировки, такие как скорость кодирования и точные значения сегментов утечки, неизвестны до завершения кодирования, особенно для кодирования VBR. Чтобы получить правильные значения, приложение должно подождать события [миндофпресентатион](meendofpresentation.md) , указывающего на то, что сеанс кодирования завершен. Значения контейнеров утечки необходимо обновить в приемнике, чтобы объект заголовка ASF мог отражать точные значения.

Следующая процедура описывает шаги, необходимые для прохода по узлам в топологии кодирования, чтобы получить узел приемника файлов и задать необходимые свойства сегмента утечки.

**Обновление значений свойств кодировки POST в приемнике файлов ASF**

1.  Вызовите метод [**имфтопологи:: жетаутпутнодеколлектион**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) , чтобы получить коллекцию выходных узлов из топологии кодирования.
2.  Для каждого узла получите указатель на приемник потока в узле, вызвав [**имфтопологиноде:: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject). Запрос интерфейса [**имфстреамсинк**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) для указателя [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , возвращаемого методом **имфтопологиноде:: GetObject**.
3.  Для каждого приемника потока получите нисходящий узел (кодировщик), вызвав [**имфтопологиноде:: input**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput).
4.  Запросите узел, чтобы получить указатель [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) из узла кодировщика.
5.  Запросите у кодировщика указатель [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , чтобы получить хранилище свойств кодирования из кодировщика.
6.  Запросите приемник потока для указателя [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , чтобы получить хранилище свойств приемника потока.
7.  Вызовите метод [**ипропертисторе:: GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , чтобы получить требуемые значения свойств из хранилища свойств кодировщика и скопировать их в хранилище свойств приемника потока, вызвав **Ипропертисторе:: SetValue**.

В следующей таблице показаны значения свойств кодировки POST, которые должны быть заданы в приемнике потока для видеопотока.



| Тип кодировки                                                                                  | Имя свойства (GetValue)                                                                        | Имя свойства (SetValue)                                                                                                |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Кодирование постоянной скорости потока](constant-bit-rate-encoding.md)                                   | МФПКЭЙ \_ бавг<br/> МФПКЭЙ \_ равг<br/>                                                 | МФПКЭЙ \_ stat \_ бавг<br/> МФПКЭЙ \_ stat \_ равг<br/>                                                             |
| [Кодирование скорости переменной с учетом качества](quality-based-variable-bit-rate--vbr--encoding.md) | МФПКЭЙ \_ бавг<br/> МФПКЭЙ \_ равг<br/> МФПКЭЙ \_ бмакс<br/> МФПКЭЙ \_ рмакс<br/> | МФПКЭЙ \_ stat \_ бавг<br/> МФПКЭЙ \_ stat \_ равг<br/> МФПКЭЙ \_ stat \_ бмакс<br/> МФПКЭЙ \_ stat \_ рмакс<br/> |



 

В следующем примере кода задаются значения свойств после кодирования.


```C++
//-------------------------------------------------------------------
//  PostEncodingUpdate
//  Updates the file sink with encoding properties set on the encoder
//  during the encoding session.
    //1. Get the output nodes
    //2. For each node, get the downstream node
    //3. For the downstream node, get the MFT
    //4. Get the property store
    //5. Get the required values
    //6. Set them on the stream sink
//
//  pTopology: A pointer to the full topology retrieved from the media session.
//-------------------------------------------------------------------

HRESULT PostEncodingUpdate(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFCollection* pOutputColl = NULL;
    IUnknown* pNodeUnk = NULL;
    IMFMediaType* pType = NULL;
    IMFTopologyNode* pNode = NULL;
    IUnknown* pSinkUnk = NULL;
    IMFStreamSink* pStreamSink = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IUnknown* pEncoderUnk = NULL;
    IMFTransform* pEncoder = NULL;
    IPropertyStore* pStreamSinkProps = NULL;
    IPropertyStore* pEncoderProps = NULL;

    GUID guidMajorType = GUID_NULL;

    PROPVARIANT var;
    PropVariantInit( &var );

    DWORD cElements = 0;

    hr = pTopology->GetOutputNodeCollection( &pOutputColl);
    if (FAILED(hr))
    {
        goto done;
    }


    hr = pOutputColl->GetElementCount(&cElements);
    if (FAILED(hr))
    {
        goto done;
    }


    for(DWORD index = 0; index < cElements; index++)
    {
        hr = pOutputColl->GetElement(index, &pNodeUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNodeUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInputPrefType(0, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->GetMajorType( &guidMajorType );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetObject(&pSinkUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSinkUnk->QueryInterface(IID_IMFStreamSink, (void**)&pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInput( 0, &pEncoderNode, NULL );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderNode->GetObject(&pEncoderUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderUnk->QueryInterface(IID_IMFTransform, (void**)&pEncoder);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamSink->QueryInterface(IID_IPropertyStore, (void**)&pStreamSinkProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoder->QueryInterface(IID_IPropertyStore, (void**)&pEncoderProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if( guidMajorType == MFMediaType_Video )
        {            
            hr = pEncoderProps->GetValue( MFPKEY_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_BMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else if( guidMajorType == MFMediaType_Audio )
        {      
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BMAX, &var);
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var );         
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, var );         
            if (FAILED(hr))
            {
                goto done;
            }
        } 
        PropVariantClear( &var ); 
   }
done:
    SafeRelease (&pOutputColl);
    SafeRelease (&pNodeUnk);
    SafeRelease (&pType);
    SafeRelease (&pNode);
    SafeRelease (&pSinkUnk);
    SafeRelease (&pStreamSink);
    SafeRelease (&pEncoderNode);
    SafeRelease (&pEncoderUnk);
    SafeRelease (&pEncoder);
    SafeRelease (&pStreamSinkProps);
    SafeRelease (&pEncoderProps);

    return hr;
   
}
```



## <a name="implement-main"></a>Реализация Main

В следующем примере кода показана основная функция консольного приложения.


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 4)
    {
        wprintf_s(L"Usage: %s inputaudio.mp3, %s output.wm*, %Encoding Type: CBR, VBR\n");
        return 0;
    }


    HRESULT             hr = S_OK;

    IMFMediaSource* pSource = NULL;
    IMFTopology* pTopology = NULL;
    IMFActivate* pFileSinkActivate = NULL;

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the requested encoding mode
    if (wcscmp(argv[3], L"CBR")==0)
    {
        EncodingMode = CBR;
    }
    else if (wcscmp(argv[3], L"VBR")==0)
    {
        EncodingMode = VBR;
    }
    else
    {
        EncodingMode = CBR;
    }

    // Start up Media Foundation platform.
    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the media source
    hr = CreateMediaSource(argv[1], &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the file sink activate
    hr = CreateMediaSink(argv[2], pSource, &pFileSinkActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    //Build the encoding topology.
    hr = BuildPartialTopology(pSource, pFileSinkActivate, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Instantiate the media session and start encoding
    hr = Encode(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }


done:
    // Clean up.
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    SafeRelease(&pFileSinkActivate);

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the output file due to 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="test-the-output-file"></a>Проверка выходного файла

В следующем списке приводится список флажков для проверки закодированного файла. Эти значения можно проверить в диалоговом окне Свойства файла, которое можно отобразить, щелкнув закодированный файл правой кнопкой мыши и выбрав пункт **Свойства** в контекстном меню.

-   Путь к закодированному файлу является точным.
-   Размер файла превышает 0 КБ, а длительность воспроизведения совпадает с длительностью исходного файла.
-   Для видеопотока проверьте ширину и высоту кадра, а также частоту кадров. Эти значения должны соответствовать значениям, указанным в профиле ASF, созданном на шаге "Создание объекта профиля ASF".
-   Для аудиопотока скорость потока должна быть близко к значению, указанному на целевом типе носителя.
-   Откройте файл в проигрывателе Windows Media и проверьте качество кодирования.
-   Откройте файл ASF в Асфвиевер, чтобы увидеть структуру файла ASF. Это средство можно загрузить с [веб-сайта Майкрософт](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).

## <a name="common-error-codes-and-debugging-tips"></a>Распространенные коды ошибок и советы по отладке

В следующем списке описаны распространенные коды ошибок, которые могут быть получены, и советы по отладке.

-   Вызов [**имфсаурцересолвер:: креатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) приостанавливается к приложению.

    Убедитесь, что вы инициализируи Media Foundationную платформу, вызвав [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). Эта функция устанавливает асинхронную платформу, используемую всеми методами, которые запускают асинхронные операции, такие как [**имфсаурцересолвер:: креатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), внутренне.

-   [**Имфсаурцересолвер:: креатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) возвращает значение HRESULT 0x80070002 "системе не удается найти указанный файл.

    Убедитесь, что имя входного файла, указанное пользователем в первом аргументе, существует.

-   HRESULT 0x80070020 "процесс не может получить доступ к файлу, так как он используется другим процессом. "

    Убедитесь, что входные и выходные файлы в настоящее время не используются другим ресурсом в системе.

-   Вызовы методов [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) возвращают MF \_ E \_ инвалидмедиатипе.

    Убедитесь, что выполнены следующие условия.

    -   Указанный тип входных данных или тип выхода совместим с типами мультимедиа, поддерживаемыми кодировщиком.
    -   Указанные типы носителей завершены. Для выполнения типов мультимедиа ознакомьтесь с необходимыми атрибутами в подразделах "Создание типа сжатого аудио носителя" и "Создание сжатого видеоматериала" этого руководства.
    -   Убедитесь, что задана Целевая скорость по отношению к частичному типу носителя, к которому добавляются частные данные кодека.

-   Сеанс мультимедиа возвращает \_ \_ из состояния события MF E неподдерживаемый \_ \_ тип D3D.

    Эта ошибка возвращается, если тип носителя источника указывает смешанный режим чередования, который не поддерживается кодировщиком видео Windows Media. Если для типа сжатого видео выбрано значение использовать прогрессивный режим, то конвейер должен использовать преобразование «de-чередование». Поскольку конвейеру не удается найти совпадение (обозначено этим кодом ошибки), необходимо вручную вставить дезагруженный обработчик видео (перекодировать видеопроцессор) между узлами декодера и кодировщика.

-   Сеанс мультимедиа возвращает E \_ INVALIDARG в состоянии события.

    Эта ошибка возвращается в том случае, если атрибуты типа носителя источника несовместимы с атрибутами выходного типа носителя, заданного в кодировщике Windows Media.

-   [**Ивмкодекприватедата:: жетприватедата**](../wmformat/iwmcodecprivatedata-getprivatedata.md) возвращает значение HRESULT 0x80040203 "при попытке вычислить строку запроса произошла синтаксическая ошибка"

    Убедитесь, что тип входных данных задан в файле MFT кодировщика.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Компоненты ASF уровня конвейера](pipeline-layer-asf-components.md)
</dt> </dl>

 

 
