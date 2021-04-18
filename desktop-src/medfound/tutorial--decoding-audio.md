---
description: В этом учебнике показано, как использовать средство чтения исходного кода для декодирования звука из файла мультимедиа и записи звука в ВОЛНовый файл.
ms.assetid: ed40e201-c6ed-444f-bdaa-a5f33d1cc068
title: Учебник. декодирование аудио
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eb6d9f48419b62fa1c379c636abaf2bb0a63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556246"
---
# <a name="tutorial-decoding-audio"></a>Учебник. декодирование аудио

В этом учебнике показано, как использовать [средство чтения исходного кода](source-reader.md) для декодирования звука из файла мультимедиа и записи звука в волновый файл. Учебник основан на образце [аудиоклипа](audio-clip-sample.md) .

-   [Обзор](#overview)
-   [Файлы заголовков и библиотек](#header-and-library-files)
-   [Реализация wmain](#implement-wmain)
-   [Запись файла WAVE](#write-the-wave-file)
-   [Настройка модуля чтения исходного кода](#configure-the-source-reader)
-   [Запись заголовка ВОЛНового файла](#write-the-wave-file-header)
-   [Вычисление максимального размера данных](#calculate-the-maximum-data-size)
-   [Декодирование звука](#decode-the-audio)
-   [Финализировать заголовок файла](#finalize-the-file-header)
-   [См. также](#related-topics)

## <a name="overview"></a>Обзор

В этом руководстве вы создадите консольное приложение, которое принимает два аргумента командной строки: имя входного файла, содержащего аудиопоток, и имя выходного файла. Приложение считывает из входного файла пять секунд звуковых данных и записывает звук в выходной файл в виде ВОЛНовых данных.

Для получения раскодированных звуковых данных приложение использует объект модуля чтения исходного кода. Модуль чтения исходного кода предоставляет интерфейс [**имфсаурцереадер**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) . Для записи декодированного звука в ВОЛНовый файл приложения используют функции ввода-вывода Windows. Этот процесс показан на следующем рисунке.

![Схема, показывающая средство чтения исходного кода, которое получает звуковые данные из исходного файла.](images/audio-clip-tutorial.gif)

В простейшей форме файл WAVE имеет следующую структуру:



| Тип данных                              | Размер (байт) | Значение                                                                 |
|----------------------------------------|--------------|-----------------------------------------------------------------------|
| **FOURCC**                             | 4            | Metallica                                                                |
| **DWORD**                              | 4            | Общий размер файла, не включая первые 8 байт                      |
| **FOURCC**                             | 4            | ЗВУКОВ                                                                |
| **FOURCC**                             | 4            | FMT                                                                |
| **DWORD**                              | 4            | Размер данных [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) , приведенных ниже. |
| [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) | Различается       | Заголовок звукового формата.                                                  |
| **FOURCC**                             | 4            | Data                                                                |
| **DWORD**                              | 4            | Размер звуковых данных.                                               |
| **ДВУХБАЙТОВЫХ**\[\]                           | Различается       | Звуковые данные.                                                           |



 

> [!Note]  
> **FourCC** — это **двойное слово** , сформированное путем сцепления четырех символов ASCII.

 

Эту базовую структуру можно расширить, добавив метаданные файла и другую информацию, которая выходит за рамки данного руководства.

## <a name="header-and-library-files"></a>Файлы заголовков и библиотек

Включите в проект следующие файлы заголовков:


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <mfreadwrite.h>
#include <stdio.h>
#include <mferror.h>
```



Ссылка на следующие библиотеки:

-   мфплат. lib
-   мфреадврите. lib
-   мфууид. lib

## <a name="implement-wmain"></a>Реализация wmain

В следующем коде показана функция точки входа для приложения.


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 3)
    {
        printf("arguments: input_file output_file.wav\n");
        return 1;
    }

    const WCHAR *wszSourceFile = argv[1];
    const WCHAR *wszTargetFile = argv[2];

    const LONG MAX_AUDIO_DURATION_MSEC = 5000; // 5 seconds

    HRESULT hr = S_OK;

    IMFSourceReader *pReader = NULL;
    HANDLE hFile = INVALID_HANDLE_VALUE;

    // Initialize the COM library.
    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    // Initialize the Media Foundation platform.
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
    }

    // Create the source reader to read the input file.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSourceReaderFromURL(wszSourceFile, NULL, &pReader);
        if (FAILED(hr))
        {
            printf("Error opening input file: %S\n", wszSourceFile, hr);
        }
    }

    // Open the output file for writing.
    if (SUCCEEDED(hr))
    {
        hFile = CreateFile(wszTargetFile, GENERIC_WRITE, FILE_SHARE_READ, NULL,
            CREATE_ALWAYS, 0, NULL);

        if (hFile == INVALID_HANDLE_VALUE)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            printf("Cannot create output file: %S\n", wszTargetFile, hr);
        }
    }

    // Write the WAVE file.
    if (SUCCEEDED(hr))
    {
        hr = WriteWaveFile(pReader, hFile, MAX_AUDIO_DURATION_MSEC);
    }

    if (FAILED(hr))
    {
        printf("Failed, hr = 0x%X\n", hr);
    }

    // Clean up.
    if (hFile != INVALID_HANDLE_VALUE)
    {
        CloseHandle(hFile);
    }

    SafeRelease(&pReader);
    MFShutdown();
    CoUninitialize();

    return SUCCEEDED(hr) ? 0 : 1;
};
```



Эта функция выполняет следующие действия:

1.  Вызывает [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) для инициализации библиотеки COM.
2.  Вызывает [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) для инициализации платформы Media Foundation.
3.  Вызывает [**мфкреатесаурцереадерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) для создания модуля чтения исходного кода. Эта функция принимает имя входного файла и получает указатель интерфейса [**имфсаурцереадер**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) .
4.  Создает выходной файл, вызывая функцию **CreateFile** , которая возвращает маркер файла.
5.  Вызывает определяемую приложением функцию [вритевавфиле](#write-the-wave-file) . Эта функция декодирует аудио и записывает звуковой файл.
6.  Освобождает указатель [**имфсаурцереадер**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) и дескриптор файла.
7.  Вызывает [**мфшутдовн**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) для завершения работы платформы Media Foundation.
8.  Вызывает [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) для освобождения библиотеки COM.

## <a name="write-the-wave-file"></a>Запись файла WAVE

Большая часть работы происходит в `WriteWavFile` функции, которая вызывается из `wmain` .


```C++
//-------------------------------------------------------------------
// WriteWaveFile
//
// Writes a WAVE file by getting audio data from the source reader.
//
//-------------------------------------------------------------------

HRESULT WriteWaveFile(
    IMFSourceReader *pReader,   // Pointer to the source reader.
    HANDLE hFile,               // Handle to the output file.
    LONG msecAudioData          // Maximum amount of audio data to write, in msec.
    )
{
    HRESULT hr = S_OK;

    DWORD cbHeader = 0;         // Size of the WAVE file header, in bytes.
    DWORD cbAudioData = 0;      // Total bytes of PCM audio data written to the file.
    DWORD cbMaxAudioData = 0;

    IMFMediaType *pAudioType = NULL;    // Represents the PCM audio format.

    // Configure the source reader to get uncompressed PCM audio from the source file.

    hr = ConfigureAudioStream(pReader, &pAudioType);

    // Write the WAVE file header.
    if (SUCCEEDED(hr))
    {
        hr = WriteWaveHeader(hFile, pAudioType, &cbHeader);
    }

    // Calculate the maximum amount of audio to decode, in bytes.
    if (SUCCEEDED(hr))
    {
        cbMaxAudioData = CalculateMaxAudioDataSize(pAudioType, cbHeader, msecAudioData);

        // Decode audio data to the file.
        hr = WriteWaveData(hFile, pReader, cbMaxAudioData, &cbAudioData);
    }

    // Fix up the RIFF headers with the correct sizes.
    if (SUCCEEDED(hr))
    {
        hr = FixUpChunkSizes(hFile, cbHeader, cbAudioData);
    }

    SafeRelease(&pAudioType);
    return hr;
}
```



Эта функция вызывает ряд других определяемых приложением функций:

1.  Функция [конфигуреаудиостреам](#configure-the-source-reader) Инициализирует модуль чтения исходного кода. Эта функция получает указатель на интерфейс [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , который используется для получения описания раскодированного аудио формата, включая частоту выборки, число каналов и глубину бит (бит на выборку).
2.  Функция Вритевавехеадер записывает первую часть ВОЛНового файла, включая заголовок и начало фрагмента данных.
3.  Функция Калкулатемаксаудиодатасизе вычисляет максимальный объем аудиоданных для записи в файл в байтах.
4.  Функция Вритеваведата записывает звуковые данные PCM в файл.
5.  Функция Фиксупчунксизес записывает сведения о размере файла, которые отображаются после значений "Metallica" и "Data" **FourCC** в волном файле. (Эти значения неизвестны до `WriteWaveData` завершения.)

Эти функции показаны в остальных разделах этого руководства.

## <a name="configure-the-source-reader"></a>Настройка модуля чтения исходного кода

`ConfigureAudioStream`Функция настраивает модуль чтения исходного кода для декодирования звукового потока в исходном файле. Он также возвращает сведения о формате декодированного звука.

В Media Foundation форматы мультимедиа описываются с помощью объектов *типа мультимедиа* . Объект типа мультимедиа предоставляет интерфейс [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , который наследует интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . По сути, тип носителя — это коллекция свойств, описывающих формат. Дополнительные сведения см. в разделе [типы носителей](media-types.md).


```C++
//-------------------------------------------------------------------
// ConfigureAudioStream
//
// Selects an audio stream from the source file, and configures the
// stream to deliver decoded PCM audio.
//-------------------------------------------------------------------

HRESULT ConfigureAudioStream(
    IMFSourceReader *pReader,   // Pointer to the source reader.
    IMFMediaType **ppPCMAudio   // Receives the audio format.
    )
{
    IMFMediaType *pUncompressedAudioType = NULL;
    IMFMediaType *pPartialType = NULL;

    // Select the first audio stream, and deselect all other streams.
    HRESULT hr = pReader->SetStreamSelection(
        (DWORD)MF_SOURCE_READER_ALL_STREAMS, FALSE);

    if (SUCCEEDED(hr))
    {
        hr = pReader->SetStreamSelection(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM, TRUE);
    }

    // Create a partial media type that specifies uncompressed PCM audio.
    hr = MFCreateMediaType(&pPartialType);

    if (SUCCEEDED(hr))
    {
        hr = pPartialType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Audio);
    }

    if (SUCCEEDED(hr))
    {
        hr = pPartialType->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_PCM);
    }

    // Set this type on the source reader. The source reader will
    // load the necessary decoder.
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentMediaType(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            NULL, pPartialType);
    }

    // Get the complete uncompressed format.
    if (SUCCEEDED(hr))
    {
        hr = pReader->GetCurrentMediaType(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            &pUncompressedAudioType);
    }

    // Ensure the stream is selected.
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetStreamSelection(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            TRUE);
    }

    // Return the PCM format to the caller.
    if (SUCCEEDED(hr))
    {
        *ppPCMAudio = pUncompressedAudioType;
        (*ppPCMAudio)->AddRef();
    }

    SafeRelease(&pUncompressedAudioType);
    SafeRelease(&pPartialType);
    return hr;
}
```



`ConfigureAudioStream`Функция выполняет следующие действия:

1.  Вызывает метод [**имфсаурцереадер:: сетстреамселектион**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) , чтобы выбрать аудиопоток и отменить выбор всех остальных потоков. Этот шаг может повысить производительность, так как предотвращает удержание модуля чтения исходного кода на видеокадры, которые не используются приложением.
2.  Создает *частичный* тип носителя, указывающий звук PCM. Функция создает разделяемый тип следующим образом:
    1.  Вызывает [**мфкреатемедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) для создания пустого объекта типа мультимедиа.
    2.  Устанавливает атрибут [**\_ \_ основного \_ типа MF MT**](mf-mt-major-type-attribute.md) в **мфмедиатипе \_ Audio**.
    3.  Устанавливает атрибут [**\_ \_ подтипа MF MT**](mf-mt-subtype-attribute.md) в **мфаудиоформат \_ PCM**.
3.  Вызывает [**имфсаурцереадер:: сеткуррентмедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) для установки разделяемого типа в модуле чтения исходного кода. Если исходный файл содержит закодированный звук, модуль чтения исходного кода автоматически загружает необходимый звуковой декодер.
4.  Вызывает [**имфсаурцереадер:: жеткуррентмедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) , чтобы получить фактический тип носителя PCM. Этот метод возвращает тип носителя со всеми заполненными сведениями о формате, например скорость дискретизации и число каналов.
5.  Вызывает [**имфсаурцереадер:: сетстреамселектион**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) для включения аудиопотока.

## <a name="write-the-wave-file-header"></a>Запись заголовка ВОЛНового файла

`WriteWaveHeader`Функция записывает заголовок волнового файла.

Единственным Media Foundation API, вызываемым из этой функции, является [**мфкреатевавеформатексфроммфмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype), который преобразует тип мультимедиа в структуру [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) .


```C++
//-------------------------------------------------------------------
// WriteWaveHeader
//
// Write the WAVE file header.
//
// Note: This function writes placeholder values for the file size
// and data size, as these values will need to be filled in later.
//-------------------------------------------------------------------

HRESULT WriteWaveHeader(
    HANDLE hFile,               // Output file.
    IMFMediaType *pMediaType,   // PCM audio format.
    DWORD *pcbWritten           // Receives the size of the header.
    )
{
    HRESULT hr = S_OK;
    UINT32 cbFormat = 0;

    WAVEFORMATEX *pWav = NULL;

    *pcbWritten = 0;

    // Convert the PCM audio format into a WAVEFORMATEX structure.
    hr = MFCreateWaveFormatExFromMFMediaType(pMediaType, &pWav, &cbFormat);

    // Write the 'RIFF' header and the start of the 'fmt ' chunk.
    if (SUCCEEDED(hr))
    {
        DWORD header[] = {
            // RIFF header
            FCC('RIFF'),
            0,
            FCC('WAVE'),
            // Start of 'fmt ' chunk
            FCC('fmt '),
            cbFormat
        };

        DWORD dataHeader[] = { FCC('data'), 0 };

        hr = WriteToFile(hFile, header, sizeof(header));

        // Write the WAVEFORMATEX structure.
        if (SUCCEEDED(hr))
        {
            hr = WriteToFile(hFile, pWav, cbFormat);
        }

        // Write the start of the 'data' chunk

        if (SUCCEEDED(hr))
        {
            hr = WriteToFile(hFile, dataHeader, sizeof(dataHeader));
        }

        if (SUCCEEDED(hr))
        {
            *pcbWritten = sizeof(header) + cbFormat + sizeof(dataHeader);
        }
    }


    CoTaskMemFree(pWav);
    return hr;
}
```



`WriteToFile`Функция — это простая вспомогательная функция, которая заключает в оболочку функцию Windows **WriteFile** и возвращает значение **HRESULT** .


```C++
//-------------------------------------------------------------------
//
// Writes a block of data to a file
//
// hFile: Handle to the file.
// p: Pointer to the buffer to write.
// cb: Size of the buffer, in bytes.
//
//-------------------------------------------------------------------

HRESULT WriteToFile(HANDLE hFile, void* p, DWORD cb)
{
    DWORD cbWritten = 0;
    HRESULT hr = S_OK;

    BOOL bResult = WriteFile(hFile, p, cb, &cbWritten, NULL);
    if (!bResult)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    return hr;
}
```



## <a name="calculate-the-maximum-data-size"></a>Вычисление максимального размера данных

Так как размер файла хранится в виде 4-байтового значения в заголовке файла, файл звукозаписи ограничивается максимальным размером в 0xFFFFFFFF байт — примерно 4 ГБ. Это значение включает размер заголовка файла. Звук PCM имеет постоянную скорость, поэтому вы можете вычислить максимальный размер данных из аудио формата следующим образом:


```C++
//-------------------------------------------------------------------
// CalculateMaxAudioDataSize
//
// Calculates how much audio to write to the WAVE file, given the
// audio format and the maximum duration of the WAVE file.
//-------------------------------------------------------------------

DWORD CalculateMaxAudioDataSize(
    IMFMediaType *pAudioType,    // The PCM audio format.
    DWORD cbHeader,              // The size of the WAVE file header.
    DWORD msecAudioData          // Maximum duration, in milliseconds.
    )
{
    UINT32 cbBlockSize = 0;         // Audio frame size, in bytes.
    UINT32 cbBytesPerSecond = 0;    // Bytes per second.

    // Get the audio block size and number of bytes/second from the audio format.

    cbBlockSize = MFGetAttributeUINT32(pAudioType, MF_MT_AUDIO_BLOCK_ALIGNMENT, 0);
    cbBytesPerSecond = MFGetAttributeUINT32(pAudioType, MF_MT_AUDIO_AVG_BYTES_PER_SECOND, 0);

    // Calculate the maximum amount of audio data to write.
    // This value equals (duration in seconds x bytes/second), but cannot
    // exceed the maximum size of the data chunk in the WAVE file.

        // Size of the desired audio clip in bytes:
    DWORD cbAudioClipSize = (DWORD)MulDiv(cbBytesPerSecond, msecAudioData, 1000);

    // Largest possible size of the data chunk:
    DWORD cbMaxSize = MAXDWORD - cbHeader;

    // Maximum size altogether.
    cbAudioClipSize = min(cbAudioClipSize, cbMaxSize);

    // Round to the audio block size, so that we do not write a partial audio frame.
    cbAudioClipSize = (cbAudioClipSize / cbBlockSize) * cbBlockSize;

    return cbAudioClipSize;
}
```



Чтобы избежать частичных звуковых кадров, размер округляется до выравнивания блока, который хранится в атрибуте [**\_ \_ \_ \_ выравнивания звукового блока MF MT**](mf-mt-audio-block-alignment-attribute.md) .

## <a name="decode-the-audio"></a>Декодирование звука

`WriteWaveData`Функция считывает декодированный звук из исходного файла и выполняет запись в волновый файл.


```C++
//-------------------------------------------------------------------
// WriteWaveData
//
// Decodes PCM audio data from the source file and writes it to
// the WAVE file.
//-------------------------------------------------------------------

HRESULT WriteWaveData(
    HANDLE hFile,               // Output file.
    IMFSourceReader *pReader,   // Source reader.
    DWORD cbMaxAudioData,       // Maximum amount of audio data (bytes).
    DWORD *pcbDataWritten       // Receives the amount of data written.
    )
{
    HRESULT hr = S_OK;
    DWORD cbAudioData = 0;
    DWORD cbBuffer = 0;
    BYTE *pAudioData = NULL;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Get audio samples from the source reader.
    while (true)
    {
        DWORD dwFlags = 0;

        // Read the next sample.
        hr = pReader->ReadSample(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            0, NULL, &dwFlags, NULL, &pSample );

        if (FAILED(hr)) { break; }

        if (dwFlags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            printf("Type change - not supported by WAVE file format.\n");
            break;
        }
        if (dwFlags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            printf("End of input file.\n");
            break;
        }

        if (pSample == NULL)
        {
            printf("No sample\n");
            continue;
        }

        // Get a pointer to the audio data in the sample.

        hr = pSample->ConvertToContiguousBuffer(&pBuffer);

        if (FAILED(hr)) { break; }


        hr = pBuffer->Lock(&pAudioData, NULL, &cbBuffer);

        if (FAILED(hr)) { break; }


        // Make sure not to exceed the specified maximum size.
        if (cbMaxAudioData - cbAudioData < cbBuffer)
        {
            cbBuffer = cbMaxAudioData - cbAudioData;
        }

        // Write this data to the output file.
        hr = WriteToFile(hFile, pAudioData, cbBuffer);

        if (FAILED(hr)) { break; }

        // Unlock the buffer.
        hr = pBuffer->Unlock();
        pAudioData = NULL;

        if (FAILED(hr)) { break; }

        // Update running total of audio data.
        cbAudioData += cbBuffer;

        if (cbAudioData >= cbMaxAudioData)
        {
            break;
        }

        SafeRelease(&pSample);
        SafeRelease(&pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        printf("Wrote %d bytes of audio data.\n", cbAudioData);

        *pcbDataWritten = cbAudioData;
    }

    if (pAudioData)
    {
        pBuffer->Unlock();
    }

    SafeRelease(&pBuffer);
    SafeRelease(&pSample);
    return hr;
}
```



`WriteWaveData`Функция выполняет следующие функции в цикле:

1.  Вызывает [**имфсаурцереадер:: реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) для чтения звука из исходного файла. Параметр *dwFlags* получает побитовое **или** из перечисления [**\_ \_ \_ флагов считывания источника MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) . Параметр *псампле* получает указатель на интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , который используется для доступа к звуковым данным. В некоторых случаях вызов **реадсампле** не создает данные, в этом случае указатель **Имфсампле** имеет **значение NULL**.
2.  Проверяет *dwFlags* для следующих флагов:
    -   **MF \_ SOURCE \_ реадерф \_ куррентмедиатипечанжед**. Этот флаг указывает на изменение формата в исходном файле. Файлы WAVE не поддерживают изменения формата.
    -   **MF \_ SOURCE \_ реадерф \_ ENDOFSTREAM**. Этот флаг указывает конец потока.
3.  Вызывает [**имфсампле:: конверттоконтигуаусбуффер**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) для получения указателя на объект буфера.
4.  Вызывает [**имфмедиабуффер:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) для получения указателя на буферную память.
5.  Записывает звуковые данные в выходной файл.
6.  Вызывает метод [**имфмедиабуффер:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) для разблокировки объекта буфера.

Функция выходит из цикла, когда происходит любое из следующих условий:

-   Изменяется формат потока.
-   Достигнут конец потока.
-   Максимальный объем звуковых данных записывается в выходной файл.
-   Возникает ошибка.

## <a name="finalize-the-file-header"></a>Финализировать заголовок файла

Значения размера, хранящиеся в заголовке WAVE, неизвестны до завершения предыдущей функции. `FixUpChunkSizes`Заполнит следующие значения:


```C++
//-------------------------------------------------------------------
// FixUpChunkSizes
//
// Writes the file-size information into the WAVE file header.
//
// WAVE files use the RIFF file format. Each RIFF chunk has a data
// size, and the RIFF header has a total file size.
//-------------------------------------------------------------------

HRESULT FixUpChunkSizes(
    HANDLE hFile,           // Output file.
    DWORD cbHeader,         // Size of the 'fmt ' chuck.
    DWORD cbAudioData       // Size of the 'data' chunk.
    )
{
    HRESULT hr = S_OK;

    LARGE_INTEGER ll;
    ll.QuadPart = cbHeader - sizeof(DWORD);

    if (0 == SetFilePointerEx(hFile, ll, NULL, FILE_BEGIN))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }

    // Write the data size.

    if (SUCCEEDED(hr))
    {
        hr = WriteToFile(hFile, &cbAudioData, sizeof(cbAudioData));
    }

    if (SUCCEEDED(hr))
    {
        // Write the file size.
        ll.QuadPart = sizeof(FOURCC);

        if (0 == SetFilePointerEx(hFile, ll, NULL, FILE_BEGIN))
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }

    if (SUCCEEDED(hr))
    {
        DWORD cbRiffFileSize = cbHeader + cbAudioData - 8;

        // NOTE: The "size" field in the RIFF header does not include
        // the first 8 bytes of the file. (That is, the size of the
        // data that appears after the size field.)

        hr = WriteToFile(hFile, &cbRiffFileSize, sizeof(cbRiffFileSize));
    }

    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Типы звуковых носителей](audio-media-types.md)
</dt> <dt>

[Модуль чтения исходного кода](source-reader.md)
</dt> <dt>

[**имфсаурцереадер**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 
