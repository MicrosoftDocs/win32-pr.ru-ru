---
description: В этом учебнике демонстрируется запись нового звукового файла (WMA) путем извлечения мультимедийного содержимого из файла звукозаписи (. wav) и его сжатия в формате ASF.
ms.assetid: f310c6ed-52e7-4828-9d4c-2f7ced9080c5
title: Учебник. запись файла WMA с помощью объектов Вмконтаинер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d156b75ced6cde2953ec90362ed13b0cc53bb83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898705"
---
# <a name="tutorial-writing-a-wma-file-by-using-wmcontainer-objects"></a>Учебник. запись файла WMA с помощью объектов Вмконтаинер

В этом учебнике демонстрируется запись нового звукового файла (WMA) путем извлечения мультимедийного содержимого из файла звукозаписи (. wav) и его сжатия в формате ASF. Для преобразования используется режим кодирования с [постоянным битом скорости](constant-bit-rate-encoding.md) (CBR). В этом режиме перед сеансом кодирования приложение указывает целевую скорость, которую должен достичь кодировщик.

В этом руководстве вы создадите консольное приложение, которое принимает входные и выходные имена файлов в качестве аргументов. Приложение получает примеры несжатого носителя из приложения для анализа волнового файла, которое предоставляется в этом руководстве. Эти примеры отправляются в кодировщик для преобразования в формат Windows Media Audio 9. Кодировщик настраивается для кодирования CBR и использует первую скорость потока, доступную во время согласования типа носителя, в качестве целевой скорости. Закодированные образцы отправляются мультиплексору для пакетирования в формате ASF. Эти пакеты будут записаны в байтовый поток, представляющий объект данных ASF. После того как раздел данных будет готов, вы создадите звуковой файл ASF и запишете новый объект заголовка ASF, который объединяет все данные заголовка, а затем добавляет байтовый поток данных ASF.

Этот учебник содержит следующие подразделы:

-   [Предварительные условия](#prerequisites)
-   [Терминология](#terminology)
-   [1. Настройка проекта](#1-set-up-the-project)
-   [2. объявление вспомогательных функций](#2-declare-helper-functions)
-   [3. Открытие звукового файла](#3-open-an-audio-file)
-   [4. Настройка кодировщика](#4-configure-the-encoder)
-   [5. Создайте объект ASF Контентинфо.](#5-create-the-asf-contentinfo-object)
-   [6. Создание мультиплексора ASF](#6-create-the-asf-multiplexer)
-   [7. Генерация новых пакетов данных ASF](#7-generate-new-asf-data-packets)
-   [8. запись файла ASF](#8-write-the-asf-file)
-   [9. определение функции Entry-Point](#9-define-the-entry-point-function)
-   [См. также](#related-topics)

## <a name="prerequisites"></a>Предварительные условия

В этом учебнике предполагается следующее:

-   Вы знакомы со структурой файла ASF и компонентами, предоставляемыми Media Foundation для работы с объектами ASF. К таким компонентам относятся Контентинфо, Splitter, мультиплексор и объекты профиля. Дополнительные сведения см. в разделе [компоненты ASF вмконтаинер](wmcontainer-asf-components.md).
-   Вы знакомы с кодировщиками Windows Media и различными типами кодировок, особенно CBR. Дополнительные сведения см. в разделе [кодировщики Windows Media](windows-media-encoders.md) .
-   Вы знакомы с [буферами мультимедиа](media-buffers.md) и потоками байтов: в частности, операции с файлами с использованием потока байтов и запись содержимого буфера мультимедиа в байтовый поток.

## <a name="terminology"></a>Терминология

В этом учебнике используются следующие термины:

-   Тип исходного носителя: объект типа мультимедиа, предоставляет интерфейс [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , описывающий содержимое входного файла.
-   Звуковой профиль: объект Profile, предоставляет интерфейс [**имфасфпрофиле**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) , который содержит только звуковые потоки выходного файла.
-   Пример Stream: пример носителя, предоставляющий интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , представляет данные носителя входного файла, полученные из кодировщика в сжатом состоянии.
-   Объект Контентинфо: [ASF контентинфо](asf-contentinfo-object.md), предоставляет интерфейс [**имфасфконтентинфо**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , который представляет объект заголовка ASF выходного файла.
-   Поток байтов данных: объект потока байтов, предоставляет интерфейс [**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , представляющий всю часть объекта данных ASF в выходном файле.
-   Пример пакета данных: носитель, предоставляющий интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , созданный [мультиплексором ASF](asf-multiplexer.md); представляет пакет данных ASF, который будет записан в поток байтов данных.
-   Выходной поток байтов: объект потока байтов, предоставляющий интерфейс [**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , который содержит содержимое выходного файла.

## <a name="1-set-up-the-project"></a>1. Настройка проекта

1.  Включите в исходный файл следующие заголовки:

    ```C++
    #include <new>
    #include <stdio.h>       // Standard I/O
    #include <windows.h>     // Windows headers
    #include <mfapi.h>       // Media Foundation platform
    #include <wmcontainer.h> // ASF interfaces
    #include <mferror.h>     // Media Foundation error codes
    ```

    

2.  Ссылка на следующие файлы библиотеки:

    -   мфплат. lib
    -   MF. lib
    -   мфууид. lib

3.  Объявите функцию [саферелеасе](saferelease.md) .
4.  Включите класс Квмаенкодер в проект. Полный исходный код этого класса см. в разделе [пример кода кодировщика](encoder-example-code.md).

## <a name="2-declare-helper-functions"></a>2. объявление вспомогательных функций

В этом руководстве используются следующие вспомогательные функции для чтения и записи из байтового потока.

-   `AppendToByteStream`: Добавляет содержимое одного потока байтов в другой поток байтов.
-   Вритебуффертобитестреам: записывает данные из буфера мультимедиа в байтовый поток.

Дополнительные сведения см. в разделе [**имфбитестреам:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write). В следующем коде показаны эти вспомогательные функции:


```C++
//-------------------------------------------------------------------
// AppendToByteStream
//
// Reads the contents of pSrc and writes them to pDest.
//-------------------------------------------------------------------

HRESULT AppendToByteStream(IMFByteStream *pSrc, IMFByteStream *pDest)
{
    HRESULT hr = S_OK;

    const DWORD READ_SIZE = 1024;

    BYTE buffer[READ_SIZE];

    while (1)
    {
        ULONG cbRead;

        hr = pSrc->Read(buffer, READ_SIZE, &cbRead);

        if (FAILED(hr)) { break; }

        if (cbRead == 0)
        {
            break;
        }

        hr = pDest->Write(buffer, cbRead, &cbRead);

        if (FAILED(hr)) { break; }
    }

    return hr;
}
```




```C++
//-------------------------------------------------------------------
// WriteBufferToByteStream
//
// Writes data from a media buffer to a byte stream.
//-------------------------------------------------------------------

HRESULT WriteBufferToByteStream(
    IMFByteStream *pStream,   // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,  // Pointer to the media buffer.
    DWORD *pcbWritten         // Receives the number of bytes written.
    )
{
    HRESULT hr = S_OK;
    DWORD cbData = 0;
    DWORD cbWritten = 0;
    BYTE *pMem = NULL;

    hr = pBuffer->Lock(&pMem, NULL, &cbData);

    if (SUCCEEDED(hr))
    {
        hr = pStream->Write(pMem, cbData, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        if (pcbWritten)
        {
            *pcbWritten = cbWritten;
        }
    }

    if (pMem)
    {
        pBuffer->Unlock();
    }
    return hr;
}
```



## <a name="3-open-an-audio-file"></a>3. Открытие звукового файла

В этом учебнике предполагается, что приложение создаст несжатый звук для кодирования. Для этой цели в этом учебнике объявляются две функции:


```C++
HRESULT OpenAudioFile(PCWSTR pszURL, IMFMediaType **ppAudioFormat);
HRESULT GetNextAudioSample(BOOL *pbEOS, IMFSample **ppSample);
```



Реализация этих функций остается в модуле чтения.

-   `OpenAudioFile`Функция должна открыть файл мультимедиа, заданный параметром *псзурл* , и вернуть указатель на тип носителя, описывающий аудиопоток.
-   `GetNextAudioSample`Функция должна считывать несжатый звуковой файл PCM из файла, открытого с помощью `OpenAudioFile` . По достижении конца файла *пбеос* получает значение **true**. В противном случае *ппсампле* получает пример мультимедиа, содержащий буфер аудио.

## <a name="4-configure-the-encoder"></a>4. Настройка кодировщика

Затем создайте кодировщик, настройте его для создания примеров потока в кодировке CBR и согласования входных и выходных типов мультимедиа.

В Media Foundation кодировщики (предоставляют интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ) реализуются как [преобразования Media Foundation](media-foundation-transforms.md) (MFT).

В этом руководстве кодировщик реализуется в `CWmaEncoder` классе, который предоставляет оболочку для MFT. Полный исходный код этого класса см. в разделе [пример кода кодировщика](encoder-example-code.md).

> [!Note]  
> При необходимости можно указать тип кодировки CBR. По умолчанию кодировщик настроен на использование кодировки CBR. Дополнительные сведения см. в статье [кодирование постоянной скорости потока](constant-bit-rate-encoding.md). Вы можете задать дополнительные свойства в зависимости от типа кодировки. Дополнительные сведения о свойствах, характерных для режима кодирования, см. в разделе [кодирование переменной с переменным качеством](quality-based-variable-bit-rate--vbr--encoding.md), [кодирование неограниченной переменной скорости](unconstrained-variable-bit-rate--vbr--encoding.md)и [кодирование переменной с ограничением пиковой](peak-constrained-variable-bit-rate--vbr--encoding.md)скорости.

 


```C++
    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="5-create-the-asf-contentinfo-object"></a>5. Создайте объект ASF Контентинфо.

[Объект ASF контентинфо](asf-contentinfo-object.md) содержит сведения о различных объектах заголовка выходного файла.

Сначала создайте профиль ASF для аудиопотока:

1.  Вызовите [**мфкреатеасфпрофиле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) , чтобы создать пустой объект профиля ASF. Профиль ASF предоставляет интерфейс [**имфасфпрофиле**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) . Дополнительные сведения см. в разделе [Создание и настройка потоков ASF](creating-and-configuring-asf-streams.md).
2.  Получите закодированный аудио формат из `CWmaEncoder` объекта.
3.  Вызовите метод [**имфасфпрофиле:: креатестреам**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) , чтобы создать новый поток для профиля ASF. Передайте указатель на интерфейс [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , который представляет формат потока.
4.  Вызовите метод [**имфасфстреамконфиг:: сетстреамнумбер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) , чтобы назначить идентификатор потока.
5.  Задайте параметры "сегмент утечки", установив атрибут [**MF \_ асфстреамконфиг \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) в объекте потока.
6.  Вызовите [**имфасфпрофиле:: сетстреам**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) , чтобы добавить новый поток в профиль.

Теперь создайте объект ASF Контентинфо следующим образом:

1.  Вызовите [**мфкреатеасфконтентинфо**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , чтобы создать пустой объект контентинфо.
2.  Вызовите [**имфасфконтентинфо:: сетпрофиле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) , чтобы задать профиль ASF.

В следующем коде показаны следующие шаги.


```C++
HRESULT CreateASFContentInfo(
    CWmaEncoder* pEncoder,
    IMFASFContentInfo** ppContentInfo
    )
{
    HRESULT hr = S_OK;
    
    IMFASFProfile* pProfile = NULL;
    IMFMediaType* pMediaType = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFASFContentInfo* pContentInfo = NULL;

    // Create the ASF profile object.

    hr = MFCreateASFProfile(&pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a stream description for the encoded audio.

    hr = pEncoder->GetOutputType(&pMediaType); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->CreateStream(pMediaType, &pStream); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetStreamNumber(DEFAULT_STREAM_NUMBER); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Set "leaky bucket" values.

    LeakyBucket bucket;

    hr = pEncoder->GetLeakyBucket1(&bucket);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetBlob(
        MF_ASFSTREAMCONFIG_LEAKYBUCKET1, 
        (UINT8*)&bucket, 
        sizeof(bucket)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile

    hr = pProfile->SetStream(pStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the ASF ContentInfo object.

    hr = MFCreateASFContentInfo(&pContentInfo); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContentInfo->SetProfile(pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.

    *ppContentInfo = pContentInfo;
    (*ppContentInfo)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pStream);
    SafeRelease(&pMediaType);
    SafeRelease(&pContentInfo);
    return hr;
}
```



## <a name="6-create-the-asf-multiplexer"></a>6. Создание мультиплексора ASF

[Мультиплексор ASF](asf-multiplexer.md) создает пакеты данных ASF.

1.  Вызовите [**мфкреатеасфмултиплексер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) , чтобы создать мультиплексор ASF.
2.  Вызовите метод [**имфасфмултиплексер:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) для инициализации мультиплексора. Передайте указатель на объект сведений о содержимом ASF, который был создан в предыдущем разделе.
3.  Вызовите [**имфасфмултиплексер:: сетфлагс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) , чтобы задать флаг **\_ \_ авторегулировки скорости \_ для мфасф мультиплексора** . При использовании этого параметра мультиплексор автоматически корректирует скорость передачи содержимого ASF в соответствии с характеристиками мультиплексированных потоков.


```C++
HRESULT CreateASFMux( 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer** ppMultiplexer
    )
{
    HRESULT hr = S_OK;
    
    IMFMediaType* pMediaType = NULL;
    IMFASFMultiplexer *pMultiplexer = NULL;

    // Create and initialize the ASF Multiplexer object.

    hr = MFCreateASFMultiplexer(&pMultiplexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pMultiplexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Enable automatic bit-rate adjustment.

    hr = pMultiplexer->SetFlags(MFASF_MULTIPLEXER_AUTOADJUST_BITRATE);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppMultiplexer = pMultiplexer;
    (*ppMultiplexer)->AddRef();

done:
    SafeRelease(&pMultiplexer);
    return hr;
}
```



## <a name="7-generate-new-asf-data-packets"></a>7. Генерация новых пакетов данных ASF

Затем создайте пакеты данных ASF для нового файла. Эти пакеты данных будут составлять окончательный объект данных ASF для нового файла. Чтобы создать новые пакеты данных ASF, выполните следующие действия.

1.  Вызовите [**мфкреатетемпфиле**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) , чтобы создать временный байтовый поток для хранения пакетов данных ASF.
2.  Вызовите функцию, определяемую приложением, `GetNextAudioSample` чтобы получить несжатые звуковые данные для кодировщика.
3.  Передача несжатого звука в кодировщик для сжатия. Дополнительные сведения см. [в разделе Обработка данных в кодировщике](processing-data-in-the-encoder.md) .
4.  Вызовите [**имфасфмултиплексер::P роцесссампле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) , чтобы отправить сжатые аудио примеры в мультиплексор ASF для пакетирования.
5.  Получите пакеты ASF из мультиплексора и запишите их во временный байтовый поток. Дополнительные сведения см. в разделе [Создание новых пакетов данных ASF](generating-new-asf-data-packets.md).
6.  При достижении конца исходного потока остановите кодировщик и извлекайте оставшиеся сжатые образцы из кодировщика. Дополнительные сведения о стоке MFT см. в разделе [Базовая модель обработки MFT](basic-mft-processing-model.md).
7.  После отправки всех образцов в мультиплексор вызовите [**имфасфмултиплексер:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) и извлекают оставшиеся пакеты ASF из мультиплексора.
8.  Вызовите [**имфасфмултиплексер:: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end).

Следующий код создает пакеты данных ASF. Функция возвращает указатель на байтовый поток, содержащий объект данных ASF.


```C++
HRESULT EncodeData(
    CWmaEncoder* pEncoder, 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer* pMux, 
    IMFByteStream** ppDataStream) 
{
    HRESULT hr = S_OK;

    IMFByteStream* pStream = NULL;
    IMFSample* pInputSample = NULL;
    IMFSample* pWmaSample = NULL;

    BOOL bEOF = FALSE;

   // Create a temporary file to hold the data stream.
   hr = MFCreateTempFile(
        MF_ACCESSMODE_READWRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        &pStream
        );

   if (FAILED(hr))
   {
       goto done;
   }

    BOOL bNeedInput = TRUE;

    while (TRUE)
    {
        if (bNeedInput)
        {
            hr = GetNextAudioSample(&bEOF, &pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            if (bEOF)
            {
                // Reached the end of the input file.
                break;
            }

            // Encode the uncompressed audio sample.
            hr = pEncoder->ProcessInput(pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            bNeedInput = FALSE;
        }

        if (bNeedInput == FALSE)
        {
            // Get data from the encoder.

            hr = pEncoder->ProcessOutput(&pWmaSample);
            if (FAILED(hr))
            {
                goto done;
            }

            // pWmaSample can be NULL if the encoder needs more input.

            if (pWmaSample)
            {
                hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
                if (FAILED(hr))
                {
                    goto done;
                }

                //Collect the data packets and write them to a stream
                hr = GenerateASFDataPackets(pMux, pStream);
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else
            {
                bNeedInput = TRUE;
            }
        }
        
        SafeRelease(&pInputSample);
        SafeRelease(&pWmaSample);
    }

    // Drain the MFT and pull any remaining samples from the encoder.

    hr = pEncoder->Drain();
    if (FAILED(hr))
    {
        goto done;
    }

    while (TRUE)
    {
        hr = pEncoder->ProcessOutput(&pWmaSample);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pWmaSample == NULL)
        {
            break;
        }

        hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
        if (FAILED(hr))
        {
            goto done;
        }

        //Collect the data packets and write them to a stream
        hr = GenerateASFDataPackets(pMux, pStream);
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pWmaSample);
    }

    // Flush the mux and get any pending ASF data packets.
    hr = pMux->Flush();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GenerateASFDataPackets(pMux, pStream);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Update the ContentInfo object
    hr = pMux->End(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return stream to the caller that contains the ASF encoded data.
    *ppDataStream = pStream;
    (*ppDataStream)->AddRef();

done:
    SafeRelease(&pStream);
    SafeRelease(&pInputSample);
    SafeRelease(&pWmaSample);
    return hr;
}
```



Код для `GenerateASFDataPackets` функции показан в разделе [Создание новых пакетов данных ASF](generating-new-asf-data-packets.md).

## <a name="8-write-the-asf-file"></a>8. запись файла ASF

Затем запишите заголовок ASF в буфер мультимедиа, вызвав [**имфасфконтентинфо:: женератехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader). Этот метод преобразует данные, хранящиеся в объекте Контентинфо, в двоичные данные в формате файла заголовка ASF. Дополнительные сведения см. [в разделе Создание нового объекта заголовка ASF](generating-a-new-asf-header-object.md).

После создания нового объекта заголовка ASF создайте поток байтов для выходного файла. Сначала запишите объект заголовка в выходной поток байтов. Используйте объект заголовка с объектом данных, содержащимся в потоке байтов данных.


```C++
HRESULT WriteASFFile( 
     IMFASFContentInfo *pContentInfo, 
     IMFByteStream *pDataStream,
     PCWSTR pszFile
     )
{
    HRESULT hr = S_OK;
    
    IMFMediaBuffer* pHeaderBuffer = NULL;
    IMFByteStream* pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    //Create output file
    hr = MFCreateFile(MF_ACCESSMODE_WRITE, MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE, pszFile, &pWmaStream);

    if (FAILED(hr))
    {
        goto done;
    }


    // Get the size of the ASF Header Object.
    hr = pContentInfo->GenerateHeader (NULL, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a media buffer.
    hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Populate the media buffer with the ASF Header Object.
    hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF header to the output file.
    hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    if (FAILED(hr))
    {
        goto done;
    }

    // Append the data stream to the file.

    hr = pDataStream->SetCurrentPosition(0);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = AppendToByteStream(pDataStream, pWmaStream);

done:
    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);
    return hr;
}
```



## <a name="9-define-the-entry-point-function"></a>9. определение функции Entry-Point

Теперь можно объединить предыдущие шаги в законченное приложение. Перед использованием любого объекта Media Foundation инициализируйте Media Foundationную платформу, вызвав [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). По завершении вызовите [**мфшутдовн**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown). Дополнительные сведения см. в разделе [инициализация Media Foundation](initializing-media-foundation.md).

В следующем коде показано полное консольное приложение. Аргумент командной строки задает имя файла для преобразования и имя нового звукового файла.


```C++
int wmain(int argc, WCHAR* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 3)
    {
        wprintf_s(L"Usage: %s input.wmv, %s output.wma");
        return 0;
    }

    const WCHAR* sInputFileName = argv[1];    // Source file name
    const WCHAR* sOutputFileName = argv[2];  // Output file name
    
    IMFMediaType* pInputType = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFMultiplexer* pMux = NULL;
    IMFByteStream* pDataStream = NULL;

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    HRESULT hr = CoInitializeEx(
        NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the WMContainer objects.
    hr = CreateASFContentInfo(pEncoder, &pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateASFMux(pContentInfo, &pMux);
    if (FAILED(hr))
    {
        goto done;
    }

    // Convert uncompressed data to ASF format.
    hr = EncodeData(pEncoder, pContentInfo, pMux, &pDataStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF objects to the output file.
    hr = WriteASFFile(pContentInfo, pDataStream, sOutputFileName);

done:
    SafeRelease(&pInputType);
    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);
    SafeRelease(&pDataStream);
    delete pEncoder;

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }

    return 0;
} 
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Компоненты ASF Вмконтаинер](wmcontainer-asf-components.md)
</dt> <dt>

[Поддержка ASF в Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



