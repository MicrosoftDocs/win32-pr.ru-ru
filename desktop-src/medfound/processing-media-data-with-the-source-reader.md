---
description: В этом разделе описывается использование модуля чтения исходного кода для обработки данных мультимедиа.
ms.assetid: 583f5736-f767-47c5-8fdc-b3645aed59f6
title: Использование модуля чтения исходного кода для обработки данных мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b19bce4d83298693825037aef92a220d78ed7c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351182"
---
# <a name="using-the-source-reader-to-process-media-data"></a>Использование модуля чтения исходного кода для обработки данных мультимедиа

В этом разделе описывается использование [модуля чтения исходного кода](source-reader.md) для обработки данных мультимедиа.

Чтобы использовать средство чтения исходного кода, выполните следующие основные действия.

1.  Создайте экземпляр модуля чтения исходного кода.
2.  Перечисление возможных форматов вывода.
3.  Задайте фактический выходной формат для каждого потока.
4.  Обработка данных из источника.

В оставшейся части этого раздела подробно описываются эти действия.

-   [Создание модуля чтения исходного кода](#creating-the-source-reader)
-   [Перечисление выходных форматов](#enumerating-output-formats)
-   [Задание форматов выходных данных](#setting-output-formats)
-   [Обработка данных мультимедиа](#using-the-source-reader-to-process-media-data)
-   [Сток конвейера данных](#draining-the-data-pipeline)
-   [Получение длительности файла](#getting-the-file-duration)
-   [Нужна](#seeking)
-   [Скорость воспроизведения](#playback-rate)
-   [Аппаратное ускорение](#hardware-acceleration)
-   [См. также](#related-topics)

## <a name="creating-the-source-reader"></a>Создание модуля чтения исходного кода

Чтобы создать экземпляр модуля чтения исходного кода, вызовите одну из следующих функций:



| Функция                                                                                                                                                                                                                                                        | Описание                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**мфкреатесаурцереадерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)<br/>                                         | Принимает в качестве входных данных URL-адрес. Эта функция использует [сопоставитель источника](source-resolver.md) для создания источника мультимедиа из URL-адреса.<br/>                                                                       |
| <span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**мфкреатесаурцереадерфромбитестреам**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)<br/>      | Принимает указатель на байтовый поток. Эта функция также использует сопоставитель источников для создания источника мультимедиа.<br/>                                                                                        |
| <span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**мфкреатесаурцереадерфроммедиасаурце**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)<br/> | Принимает указатель на источник мультимедиа, который уже был создан. Эта функция полезна для источников мультимедиа, которые сопоставитель источников не может создавать, таких как устройства записи или пользовательские источники мультимедиа.<br/> |



 

Как правило, для файлов мультимедиа используется [**мфкреатесаурцереадерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl). Для устройств, таких как камеры, используйте [**мфкреатесаурцереадерфроммедиасаурце**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource). (Дополнительные сведения о захвате устройств в Microsoft Media Foundation см. в разделе [запись звука и видео](audio-video-capture.md).)

Каждая из этих функций принимает необязательный указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , который используется для задания различных параметров модуля чтения исходного кода, как описано в справочных разделах по этим функциям. Чтобы получить поведение по умолчанию, присвойте этому параметру **значение NULL**. Каждая функция возвращает указатель [**имфсаурцереадер**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) в качестве выходного параметра. Перед вызовом любой из этих функций необходимо вызвать функцию **CoInitialize (ex)** и [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) .

Следующий код создает модуль чтения исходного кода из URL-адреса.


```C++
int __cdecl wmain(int argc, __in_ecount(argc) PCWSTR* argv)
{
    if (argc < 2)
    {
        return 1;
    }

    const WCHAR *pszURL = argv[1];

    // Initialize the COM runtime.
    HRESULT hr = CoInitializeEx(0, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        // Initialize the Media Foundation platform.
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            // Create the source reader.
            IMFSourceReader *pReader;
            hr = MFCreateSourceReaderFromURL(pszURL, NULL, &pReader);
            if (SUCCEEDED(hr))
            {
                ReadMediaFile(pReader);
                pReader->Release();
            }
            // Shut down Media Foundation.
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="enumerating-output-formats"></a>Перечисление выходных форматов

Каждый источник мультимедиа имеет по крайней мере один поток. Например, видеофайл может содержать поток видео и аудиопоток. Формат каждого потока описывается с помощью типа мультимедиа, представленного интерфейсом [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Дополнительные сведения о типах носителей см. в разделе [типы носителей](media-types.md). Необходимо проверить тип носителя, чтобы понять формат данных, получаемых от модуля чтения исходного кода.

Изначально каждый поток имеет формат по умолчанию, который можно найти, вызвав метод [**имфсаурцереадер:: жеткуррентмедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) :

Для каждого потока источник мультимедиа предлагает список возможных типов носителей для этого потока. Количество типов зависит от источника. Если источник представляет файл мультимедиа, обычно существует только один тип для каждого потока. Веб-камера, с другой стороны, может иметь возможность потоковой передачи видео в нескольких разных форматах. В этом случае приложение может выбрать используемый формат из списка типов мультимедиа.

Чтобы получить один из типов мультимедиа для потока, вызовите метод [**имфсаурцереадер:: жетнативемедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) . Этот метод принимает два параметра индекса: индекс потока и индекс в списке типов мультимедиа для потока. Чтобы перечислить все типы для потока, увеличьте индекс списка, сохраняя константу индекса потока. Если индекс списка выходит за пределы диапазона, **жетнативемедиатипе** возвращает **MF E \_ больше \_ \_ \_ типов**.


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



Чтобы перечислить типы носителей для каждого потока, увеличьте индекс потока. Если индекс потока выходит за пределы допустимого диапазона, [**жетнативемедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) возвращает **MF \_ E \_ инвалидстреамнумбер**.


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



## <a name="setting-output-formats"></a>Задание форматов выходных данных

Чтобы изменить формат выходных данных, вызовите метод [**имфсаурцереадер:: сеткуррентмедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) . Этот метод принимает индекс потока и тип мультимедиа:

``` syntax
hr = pReader->SetCurrentMediaType(dwStreamIndex, pMediaType);
```

Для типа носителя он зависит от того, требуется ли вставить декодер.

-   Чтобы получить данные непосредственно из источника без декодирования, используйте один из типов, возвращаемых функцией [**жетнативемедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype).
-   Чтобы декодировать поток, создайте новый тип мультимедиа, описывающий требуемый формат без сжатия.

В случае с декодером Создайте тип мультимедиа следующим образом:

1.  Вызовите [**мфкреатемедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) , чтобы создать новый тип мультимедиа.
2.  Задайте атрибут [**" \_ \_ основной \_ тип MF MT**](mf-mt-major-type-attribute.md) ", чтобы указать аудио или видео.
3.  Установите атрибут [**\_ \_ подтипа MF MT**](mf-mt-subtype-attribute.md) , чтобы указать подтип формата декодирования. (См. раздел [идентификаторы GUID подтипа аудио](audio-subtype-guids.md) и [GUID подтипа видео](video-subtype-guids.md).)
4.  Вызовите [**имфсаурцереадер:: сеткуррентмедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).

Модуль чтения исходного кода автоматически загрузит декодер. Чтобы получить полные сведения о декодированном формате, вызовите метод [**имфсаурцереадер:: жеткуррентмедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) после вызова [**сеткуррентмедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)

Следующий код настраивает поток видео для RGB-32 и звукового потока PCM.


```C++
HRESULT ConfigureDecoder(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    IMFMediaType *pNativeType = NULL;
    IMFMediaType *pType = NULL;

    // Find the native format of the stream.
    HRESULT hr = pReader->GetNativeMediaType(dwStreamIndex, 0, &pNativeType);
    if (FAILED(hr))
    {
        return hr;
    }

    GUID majorType, subtype;

    // Find the major type.
    hr = pNativeType->GetGUID(MF_MT_MAJOR_TYPE, &majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Define the output type.
    hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Select a subtype.
    if (majorType == MFMediaType_Video)
    {
        subtype= MFVideoFormat_RGB32;
    }
    else if (majorType == MFMediaType_Audio)
    {
        subtype = MFAudioFormat_PCM;
    }
    else
    {
        // Unrecognized type. Skip.
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the uncompressed format.
    hr = pReader->SetCurrentMediaType(dwStreamIndex, NULL, pType);
    if (FAILED(hr))
    {
        goto done;
    }

done:
    SafeRelease(&pNativeType);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="processing-media-data"></a>Обработка данных мультимедиа

Чтобы получить данные мультимедиа из источника, вызовите метод [**имфсаурцереадер:: реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) , как показано в следующем коде.


```C++
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );
```



Первый параметр — это индекс потока, для которого необходимо получить данные. Кроме того, можно указать для **\_ \_ средства чтения источника MF \_ любой \_ поток** , чтобы получить следующие доступные данные из любого потока. Второй параметр содержит необязательные флаги. Список этих параметров см. в описании [**\_ \_ \_ \_ флага управления считыванием источника MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) . Третий параметр получает индекс потока, который фактически создает данные. Эти сведения понадобятся, если для первого параметра задать значение **MF \_ \_ Stream считывающего \_ потока в любом \_ потоке**. Четвертый параметр получает флаги состояния, указывающие различные события, которые могут возникнуть при чтении данных, например изменения формата в потоке. Список флагов состояния см. в разделе [**MF \_ source \_ Reader \_ флаг**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).

Если источник мультимедиа способен создавать данные для запрошенного потока, последний параметр [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) получает указатель на интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) образца объекта мультимедиа. Используйте пример носителя для:

-   Получение указателя на данные мультимедиа.
-   Получите время презентации и длительность выборки.
-   Получите атрибуты, описывающие чередование, превосходство полей и другие аспекты образца.

Содержимое данных мультимедиа зависит от формата потока. Для несжатого видеопотока каждый пример носителя содержит один кадр видео. Для несжатого звукового потока каждый пример носителя содержит последовательность звуковых кадров.

Метод [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) может возвращать значение **S \_ ОК** , но не возвращает пример носителя в параметре *псампле* . Например, при достижении конца файла **реадсампле** устанавливает флаг **MF \_ source \_ реадерф \_ ENDOFSTREAM** в *dwFlags* и задает для *псампле* **значение NULL**. В этом случае метод **реадсампле** возвращает значение **S \_ ОК** , так как не возникла ошибка, даже если параметр *псампле* имеет значение **null**. Поэтому всегда следует проверять значение параметра *псампле* перед его разыменованием.

В следующем коде показано, как вызвать [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) в цикле и проверить сведения, возвращаемые методом, пока не будет достигнут конец файла мультимедиа.


```C++
HRESULT ProcessSamples(IMFSourceReader *pReader)
{
    HRESULT hr = S_OK;
    IMFSample *pSample = NULL;
    size_t  cSamples = 0;

    bool quit = false;
    while (!quit)
    {
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );

        if (FAILED(hr))
        {
            break;
        }

        wprintf(L"Stream %d (%I64d)\n", streamIndex, llTimeStamp);
        if (flags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            wprintf(L"\tEnd of stream\n");
            quit = true;
        }
        if (flags & MF_SOURCE_READERF_NEWSTREAM)
        {
            wprintf(L"\tNew stream\n");
        }
        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            wprintf(L"\tNative type changed\n");
        }
        if (flags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            wprintf(L"\tCurrent type changed\n");
        }
        if (flags & MF_SOURCE_READERF_STREAMTICK)
        {
            wprintf(L"\tStream tick\n");
        }

        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            // The format changed. Reconfigure the decoder.
            hr = ConfigureDecoder(pReader, streamIndex);
            if (FAILED(hr))
            {
                break;
            }
        }

        if (pSample)
        {
            ++cSamples;
        }

        SafeRelease(&pSample);
    }

    if (FAILED(hr))
    {
        wprintf(L"ProcessSamples FAILED, hr = 0x%x\n", hr);
    }
    else
    {
        wprintf(L"Processed %d samples\n", cSamples);
    }
    SafeRelease(&pSample);
    return hr;
}
```



## <a name="draining-the-data-pipeline"></a>Сток конвейера данных

Во время обработки данных декодер или другое преобразование могут буферизовать входные образцы. На следующей схеме приложение вызывает [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) и получает пример с временем презентации, равным *T1*. Декодер удерживает примеры для *T2* и *T3*.

![Иллюстрация, показывающая буферизацию в декодере.](images/sourcereader02.png)

При следующем вызове [**Реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample)модуль чтения исходного кода может предоставить декодеру *T4* и вернуть приложению значение *T2* .

Если вы хотите декодировать все образцы, которые в данный момент помещены в буфер декодера, не передавая новые образцы в декодер, установите флаг **\_ \_ \_ \_ слива Контролф для считывания источника MF** в параметре *двконтролфлагс* [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample). Продолжайте делать это в цикле до тех пор, пока **реадсампле** не возвратит указатель образца **null** . В зависимости от способа выборки буферов декодера это может произойти сразу или после нескольких вызовов **реадсампле**.

## <a name="getting-the-file-duration"></a>Получение длительности файла

Чтобы получить длительность файла мультимедиа, вызовите метод [**имфсаурцереадер:: жетпресентатионаттрибуте**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) и запросите атрибут [**Duration MF \_ PD \_**](mf-pd-duration-attribute.md) , как показано в следующем коде.


```C++
HRESULT GetDuration(IMFSourceReader *pReader, LONGLONG *phnsDuration)
{
    PROPVARIANT var;
    HRESULT hr = pReader->GetPresentationAttribute(MF_SOURCE_READER_MEDIASOURCE, 
        MF_PD_DURATION, &var);
    if (SUCCEEDED(hr))
    {
        hr = PropVariantToInt64(var, phnsDuration);
        PropVariantClear(&var);
    }
    return hr;
}
```



Показанная здесь функция возвращает длительность в 100-наносекундных единицах. Чтобы получить длительность в секундах, разделите на 10 000 000.

## <a name="seeking"></a>Нужна

Источник мультимедиа, который получает данные из локального файла, обычно может выполнять поиск произвольной позиции в файле. Устройства записи, такие как камеры, обычно не могут выполнять поиск, так как данные находятся в режиме реального времени. Источник, который осуществляет потоковую передачу данных по сети, может выполнять поиск в зависимости от протокола потоковой передачи по сети.

Чтобы узнать, может ли источник мультимедиа искать, вызовите [**имфсаурцереадер:: жетпресентатионаттрибуте**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) и запросите атрибут [ \_ \_ \_ \_ характеристик медиасаурце для модуля чтения источника MF](mf-source-reader-mediasource-characteristics.md) , как показано в следующем коде:


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



Эта функция возвращает набор флагов возможностей из источника. Эти флаги определяются в перечислении [**\_ характеристик мфмедиасаурце**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) . Для поиска связаны два флага:



| Flag                                                                                                                                      | Описание                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**МФМЕДИАСАУРЦЕ \_ может \_ Искать**<br/>                 | Источник может искать.<br/>                                                                                                                                                                            |
| <span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**МФМЕДИАСАУРЦЕ \_ имеет \_ низкую \_ Поиск**<br/> | Поиск может занять длительное время. Например, источнику может потребоваться загрузить весь файл, прежде чем он сможет выполнить поиск. (Нет никаких условий для возврата этого флага для источника.)<br/> |



 

Следующий код проверяет наличие флага **мфмедиасаурце \_ \_** .


```C++
BOOL SourceCanSeek(IMFSourceReader *pReader)
{
    BOOL bCanSeek = FALSE;
    ULONG flags;
    if (SUCCEEDED(GetSourceFlags(pReader, &flags)))
    {
        bCanSeek = ((flags & MFMEDIASOURCE_CAN_SEEK) == MFMEDIASOURCE_CAN_SEEK);
    }
    return bCanSeek;
}
```



Для поиска вызовите метод [**имфсаурцереадер:: сеткуррентпоситион**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) , как показано в следующем коде.


```C++
HRESULT SetPosition(IMFSourceReader *pReader, const LONGLONG& hnsPosition)
{
    PROPVARIANT var;
    HRESULT hr = InitPropVariantFromInt64(hnsPosition, &var);
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentPosition(GUID_NULL, var);
        PropVariantClear(&var);
    }
    return hr;
}
```



Первый параметр дает формат времени, который используется для указания расположения поиска. Все источники мультимедиа в Media Foundation должны поддерживать единицы измерения 100-наносекундных, обозначенные значением **GUID \_ null**. Второй параметр — это **пропвариант** , содержащий положение поиска. Для единиц времени с 100-наносекундных типом данных является **лонглонг**.

Учтите, что не каждый источник мультимедиа обеспечивает точное Поиск в кадрах. Точность поиска зависит от нескольких факторов, например от интервала опорного кадра, от того, содержит ли файл мультимедиа индекс, а также указывает, имеет ли данные постоянную или переменную скорость. Поэтому после перехода к положению в файле нет никакой гарантии, что метка времени в следующем образце будет точно соответствовать запрошенной должности. Как правило, фактическая точка не будет позднее запрошенной позиции, поэтому можно отбросить выборку, пока не достигнет нужной точки в потоке.

## <a name="playback-rate"></a>Скорость воспроизведения

Хотя скорость воспроизведения можно задать с помощью модуля чтения исходного кода, обычно это не очень полезно по следующим причинам.

-   Модуль чтения исходного кода не поддерживает обратную воспроизведение, даже если источник мультимедиа делает это.
-   Приложение управляет временем презентации, поэтому приложение может реализовать быстрое или низкое воспроизведение, не устанавливая скорость источника.
-   Некоторые источники мультимедиа поддерживают режим *тонкого* режима, где источник доставляет меньшее количество выборок — обычно всего лишь ключевые кадры. Однако если вы хотите удалить неключевые кадры, можно проверить каждый пример для атрибута [мфсампликстенсион \_ клеанпоинт](mfsampleextension-cleanpoint-attribute.md) .

Чтобы задать скорость воспроизведения с помощью модуля чтения исходного кода, вызовите метод [**имфсаурцереадер:: жетсервицефорстреам**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) , чтобы получить интерфейсы [**имфратесуппорт**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) и [**имфратеконтрол**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) из источника мультимедиа.

## <a name="hardware-acceleration"></a>Аппаратное ускорение

Модуль чтения исходного кода совместим с ускорением видео Microsoft DirectX (ДКСВА) 2,0 для декодирования видео с аппаратным ускорением. Чтобы использовать ДКСВА с модулем чтения исходного кода, выполните следующие действия.

1.  Создайте устройство Microsoft Direct3D.
2.  Вызовите функцию [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) , чтобы создать диспетчер устройств Direct3D. Эта функция возвращает указатель на интерфейс [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .
3.  Вызовите метод [**IDirect3DDeviceManager9:: ресетдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) с указателем на устройство Direct3D.
4.  Создайте хранилище атрибутов, вызвав функцию [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .
5.  Создайте модуль чтения исходного кода. Передайте хранилище атрибутов в параметре *паттрибутес* функции создания.

При предоставлении устройства Direct3D модуль чтения исходного кода выделяет видеоматериалы, совместимые с API обработчика видео ДКСВА. Вы можете использовать обработку видео ДКСВА для выполнения аппаратного чередования или смешения видео. Дополнительные сведения см. в разделе [Обработка видео дксва](dxva-video-processing.md). Кроме того, если декодер поддерживает ДКСВА 2,0, он будет использовать устройство Direct3D для выполнения декодирования с аппаратным ускорением.

> [!IMPORTANT]
> Начиная с Windows 8, вместо [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)можно использовать [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) . Для приложений Магазина Windows необходимо использовать **имфдксгидевицеманажер**. Дополнительные сведения см. в статье [API-интерфейсы видео Direct3D 11](direct3d-11-video-apis.md).

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Модуль чтения исходного кода](source-reader.md)
</dt> </dl>

 

 




