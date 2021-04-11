---
description: В этом разделе описаны шаги по заполнению структур, необходимых для воспроизведения звуковых данных в XAudio2.
ms.assetid: caeb522e-d4f6-91e2-5e85-ea0af0f61300
title: 'Руководство: загрузка файлов звуковых данных в XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659b4d8e106b6f0b2eb942505f99562f56fdada7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154611"
---
# <a name="how-to-load-audio-data-files-in-xaudio2"></a><span data-ttu-id="a17ae-103">Руководство: загрузка файлов звуковых данных в XAudio2</span><span class="sxs-lookup"><span data-stu-id="a17ae-103">How to: Load Audio Data Files in XAudio2</span></span>

> [!Note]  
> <span data-ttu-id="a17ae-104">Это содержимое применимо только к классическим приложениям, и для работы в приложении Магазина Windows потребуется редакция.</span><span class="sxs-lookup"><span data-stu-id="a17ae-104">This content applies only to desktop apps and will require revision to function in a Windows Store app.</span></span> <span data-ttu-id="a17ae-105">Обратитесь к документации по [**CreateFile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2), [**креативентекс**](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [**сетфилепоинтерекс**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)и [**жетоверлаппедресултекс**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex).</span><span class="sxs-lookup"><span data-stu-id="a17ae-105">Please refer to the documentation for [**CreateFile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2), [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [**SetFilePointerEx**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex), and [**GetOverlappedResultEx**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex).</span></span> <span data-ttu-id="a17ae-106">См. Саундфилереадер. h/. cpp в образце Басиксаунд Windows 8 из [коллекции примеров Windows SDK](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208)).</span><span class="sxs-lookup"><span data-stu-id="a17ae-106">See SoundFileReader.h/.cpp in the BasicSound Windows 8 sample from the [Windows SDK Samples Gallery](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208)).</span></span>

 

<span data-ttu-id="a17ae-107">В этом разделе описаны шаги по заполнению структур, необходимых для воспроизведения звуковых данных в XAudio2.</span><span class="sxs-lookup"><span data-stu-id="a17ae-107">This topic describes the steps to populate the structures required to play audio data in XAudio2.</span></span> <span data-ttu-id="a17ae-108">Следующие шаги загружают фрагменты "fmt" и "Data" звукового файла и используют их для заполнения структуры **вавеформатекстенсибле** и структуры [**\_ буфера XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="a17ae-108">The following steps load the 'fmt ' and 'data' chunks of an audio file, and uses them to populate a **WAVEFORMATEXTENSIBLE** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span>

-   [<span data-ttu-id="a17ae-109">Подготовка к синтаксическому анализу звукового файла.</span><span class="sxs-lookup"><span data-stu-id="a17ae-109">Preparing to parse the audio file.</span></span>](#preparing-to-parse-the-audio-file)
-   [<span data-ttu-id="a17ae-110">Заполнение структур XAudio2 содержимым блоков Metallica.</span><span class="sxs-lookup"><span data-stu-id="a17ae-110">Populating XAudio2 structures with the contents of RIFF chunks.</span></span>](#populating-xaudio2-structures-with-the-contents-of-riff-chunks)

## <a name="preparing-to-parse-the-audio-file"></a><span data-ttu-id="a17ae-111">Подготовка к синтаксическому анализу звукового файла</span><span class="sxs-lookup"><span data-stu-id="a17ae-111">Preparing to parse the audio file</span></span>

<span data-ttu-id="a17ae-112">Звуковые файлы, поддерживаемые XAudio2, используют формат файла обмена ресурсами (Metallica).</span><span class="sxs-lookup"><span data-stu-id="a17ae-112">Audio files supported by XAudio2 use the Resource Interchange File Format (RIFF).</span></span> <span data-ttu-id="a17ae-113">Metallica описывается в обзоре [формата файла обмена ресурсами (Metallica)](resource-interchange-file-format--riff-.md) .</span><span class="sxs-lookup"><span data-stu-id="a17ae-113">RIFF is described in the [Resource Interchange File Format (RIFF)](resource-interchange-file-format--riff-.md) overview.</span></span> <span data-ttu-id="a17ae-114">Звуковые данные в файле Metallica загружаются путем поиска фрагмента Metallica и последующего прохода по блоку для поиска отдельных блоков, содержащихся в фрагменте Metallica.</span><span class="sxs-lookup"><span data-stu-id="a17ae-114">Audio data in a RIFF file is loaded by finding the RIFF chunk and then looping through the chunk to find individual chunks contained in the RIFF chunk.</span></span> <span data-ttu-id="a17ae-115">Следующие функции являются примерами кода для поиска фрагментов и загрузки данных, содержащихся в фрагментах.</span><span class="sxs-lookup"><span data-stu-id="a17ae-115">The following functions are examples of code to find chunks and load data contained in the chunks.</span></span>

-   <span data-ttu-id="a17ae-116">Чтобы найти фрагмент в файле Metallica, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a17ae-116">To find a chunk in a RIFF file:</span></span>

    ```
    #ifdef _XBOX //Big-Endian
    #define fourccRIFF 'RIFF'
    #define fourccDATA 'data'
    #define fourccFMT 'fmt '
    #define fourccWAVE 'WAVE'
    #define fourccXWMA 'XWMA'
    #define fourccDPDS 'dpds'
    #endif

    #ifndef _XBOX //Little-Endian
    #define fourccRIFF 'FFIR'
    #define fourccDATA 'atad'
    #define fourccFMT ' tmf'
    #define fourccWAVE 'EVAW'
    #define fourccXWMA 'AMWX'
    #define fourccDPDS 'sdpd'
    #endif
    HRESULT FindChunk(HANDLE hFile, DWORD fourcc, DWORD & dwChunkSize, DWORD & dwChunkDataPosition)
    {
        HRESULT hr = S_OK;
        if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, 0, NULL, FILE_BEGIN ) )
            return HRESULT_FROM_WIN32( GetLastError() );

        DWORD dwChunkType;
        DWORD dwChunkDataSize;
        DWORD dwRIFFDataSize = 0;
        DWORD dwFileType;
        DWORD bytesRead = 0;
        DWORD dwOffset = 0;

        while (hr == S_OK)
        {
            DWORD dwRead;
            if( 0 == ReadFile( hFile, &dwChunkType, sizeof(DWORD), &dwRead, NULL ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );

            if( 0 == ReadFile( hFile, &dwChunkDataSize, sizeof(DWORD), &dwRead, NULL ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );

            switch (dwChunkType)
            {
            case fourccRIFF:
                dwRIFFDataSize = dwChunkDataSize;
                dwChunkDataSize = 4;
                if( 0 == ReadFile( hFile, &dwFileType, sizeof(DWORD), &dwRead, NULL ) )
                    hr = HRESULT_FROM_WIN32( GetLastError() );
                break;

            default:
                if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, dwChunkDataSize, NULL, FILE_CURRENT ) )
                return HRESULT_FROM_WIN32( GetLastError() );            
            }

            dwOffset += sizeof(DWORD) * 2;
            
            if (dwChunkType == fourcc)
            {
                dwChunkSize = dwChunkDataSize;
                dwChunkDataPosition = dwOffset;
                return S_OK;
            }

            dwOffset += dwChunkDataSize;
            
            if (bytesRead >= dwRIFFDataSize) return S_FALSE;

        }

        return S_OK;
        
    }
    ```

    

-   <span data-ttu-id="a17ae-117">Для чтения данных в блоке после их обнаружения.</span><span class="sxs-lookup"><span data-stu-id="a17ae-117">To read data in a chunk after it has been located.</span></span>

    <span data-ttu-id="a17ae-118">После обнаружения требуемого фрагмента его данные можно прочитать, настроив указатель файла на начало раздела данных фрагмента.</span><span class="sxs-lookup"><span data-stu-id="a17ae-118">Once a desired chunk is found, its data can be read by adjusting the file pointer to the beginning of the data section of the chunk.</span></span> <span data-ttu-id="a17ae-119">Функция для считывания данных из фрагмента после их обнаружения может выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="a17ae-119">A function to read the data from a chunk once it is found might look like this.</span></span>

    ```
    HRESULT ReadChunkData(HANDLE hFile, void * buffer, DWORD buffersize, DWORD bufferoffset)
    {
        HRESULT hr = S_OK;
        if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, bufferoffset, NULL, FILE_BEGIN ) )
            return HRESULT_FROM_WIN32( GetLastError() );
        DWORD dwRead;
        if( 0 == ReadFile( hFile, buffer, buffersize, &dwRead, NULL ) )
            hr = HRESULT_FROM_WIN32( GetLastError() );
        return hr;
    }
    ```

    

## <a name="populating-xaudio2-structures-with-the-contents-of-riff-chunks"></a><span data-ttu-id="a17ae-120">Заполнение структур XAudio2 содержимым блоков Metallica</span><span class="sxs-lookup"><span data-stu-id="a17ae-120">Populating XAudio2 structures with the contents of RIFF chunks</span></span>

<span data-ttu-id="a17ae-121">Чтобы XAudio2 воспроизводил звук с исходным голосом, ему необходима структура **вавеформатекс** и структура [**\_ буфера XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="a17ae-121">In order for XAudio2 to play audio with a source voice, it needs a **WAVEFORMATEX** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="a17ae-122">Структура **вавеформатекс** может быть более крупной структурой, такой как **вавеформатекстенсибле** , которая содержит структуру **вавеформатекс** в качестве первого элемента.</span><span class="sxs-lookup"><span data-stu-id="a17ae-122">The **WAVEFORMATEX** structure may be a larger structure such as **WAVEFORMATEXTENSIBLE** that contains a **WAVEFORMATEX** structure as its first member.</span></span> <span data-ttu-id="a17ae-123">Дополнительные сведения см. на странице справочника по **вавеформатекс** .</span><span class="sxs-lookup"><span data-stu-id="a17ae-123">See the **WAVEFORMATEX** reference page for more information.</span></span>

<span data-ttu-id="a17ae-124">В этом примере используется **вавеформатекстенсибле** , чтобы разрешить загрузку звуковых файлов PCM с более чем двумя каналами.</span><span class="sxs-lookup"><span data-stu-id="a17ae-124">In this example a **WAVEFORMATEXTENSIBLE** is being used to allow loading of PCM audio files with more than two channels.</span></span>

<span data-ttu-id="a17ae-125">Следующие шаги иллюстрируют использование описанных выше функций для заполнения структуры **вавеформатекстенсибле** и структуры [**\_ буфера XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="a17ae-125">The following steps illustrate using the functions described above to populate a **WAVEFORMATEXTENSIBLE** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="a17ae-126">В этом случае загружаемый аудио-файл содержит данные PCM и будет содержать только фрагменты «Metallica», «FMT» и «Data».</span><span class="sxs-lookup"><span data-stu-id="a17ae-126">In this case, the audio file being loaded contains PCM data, and will only contain a 'RIFF', 'fmt ', and 'data' chunk.</span></span> <span data-ttu-id="a17ae-127">Другие форматы могут содержать дополнительные типы блоков, как описано в разделе [Формат файла обмена ресурсами (Metallica)](resource-interchange-file-format--riff-.md).</span><span class="sxs-lookup"><span data-stu-id="a17ae-127">Other formats may contain additional chunk types as described in [Resource Interchange File Format (RIFF)](resource-interchange-file-format--riff-.md).</span></span>

1.  <span data-ttu-id="a17ae-128">Объявите [**\_ буферные**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) структуры **вавеформатекстенсибле** и XAUDIO2.</span><span class="sxs-lookup"><span data-stu-id="a17ae-128">Declare **WAVEFORMATEXTENSIBLE** and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structures.</span></span>
    ```
    WAVEFORMATEXTENSIBLE wfx = {0};
    XAUDIO2_BUFFER buffer = {0};
    ```

    

2.  <span data-ttu-id="a17ae-129">Откройте звуковой файл с помощью CreateFile.</span><span class="sxs-lookup"><span data-stu-id="a17ae-129">Open the audio file with CreateFile.</span></span>
    ```
    #ifdef _XBOX
    char * strFileName = "game:\\media\\MusicMono.wav";
    #else
    TCHAR * strFileName = _TEXT("media\\MusicMono.wav");
    #endif
    // Open the file
    HANDLE hFile = CreateFile(
        strFileName,
        GENERIC_READ,
        FILE_SHARE_READ,
        NULL,
        OPEN_EXISTING,
        0,
        NULL );

    if( INVALID_HANDLE_VALUE == hFile )
        return HRESULT_FROM_WIN32( GetLastError() );

    if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, 0, NULL, FILE_BEGIN ) )
        return HRESULT_FROM_WIN32( GetLastError() );
    ```

    

3.  <span data-ttu-id="a17ae-130">Поиск фрагмента "Metallica" в звуковом файле и проверка типа файла.</span><span class="sxs-lookup"><span data-stu-id="a17ae-130">Locate the 'RIFF' chunk in the audio file, and check the file type.</span></span>
    ```
    DWORD dwChunkSize;
    DWORD dwChunkPosition;
    //check the file type, should be fourccWAVE or 'XWMA'
    FindChunk(hFile,fourccRIFF,dwChunkSize, dwChunkPosition );
    DWORD filetype;
    ReadChunkData(hFile,&filetype,sizeof(DWORD),dwChunkPosition);
    if (filetype != fourccWAVE)
        return S_FALSE;
    ```

    

4.  <span data-ttu-id="a17ae-131">Нахождение блока fmt и копирование его содержимого в структуру **вавеформатекстенсибле** .</span><span class="sxs-lookup"><span data-stu-id="a17ae-131">Locate the 'fmt ' chunk, and copy its contents into a **WAVEFORMATEXTENSIBLE** structure.</span></span>
    ```
    FindChunk(hFile,fourccFMT, dwChunkSize, dwChunkPosition );
    ReadChunkData(hFile, &wfx, dwChunkSize, dwChunkPosition );
    ```

    

5.  <span data-ttu-id="a17ae-132">Нахождение фрагмента данных и считывание его содержимого в буфер.</span><span class="sxs-lookup"><span data-stu-id="a17ae-132">Locate the 'data' chunk, and read its contents into a buffer.</span></span>
    ```
    //fill out the audio data buffer with the contents of the fourccDATA chunk
    FindChunk(hFile,fourccDATA,dwChunkSize, dwChunkPosition );
    BYTE * pDataBuffer = new BYTE[dwChunkSize];
    ReadChunkData(hFile, pDataBuffer, dwChunkSize, dwChunkPosition);
    ```

    

6.  <span data-ttu-id="a17ae-133">Заполнение структуры [**\_ буфера XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="a17ae-133">Populate an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span>
    ```
    buffer.AudioBytes = dwChunkSize;  //size of the audio buffer in bytes
    buffer.pAudioData = pDataBuffer;  //buffer containing audio data
    buffer.Flags = XAUDIO2_END_OF_STREAM; // tell the source voice not to expect any data after this buffer
    ```

    

## <a name="related-topics"></a><span data-ttu-id="a17ae-134">См. также</span><span class="sxs-lookup"><span data-stu-id="a17ae-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a17ae-135">Начало работы</span><span class="sxs-lookup"><span data-stu-id="a17ae-135">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="a17ae-136">Руководство: воспроизведение звука при помощи XAudio2</span><span class="sxs-lookup"><span data-stu-id="a17ae-136">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="a17ae-137">Справочник по программированию в XAudio2</span><span class="sxs-lookup"><span data-stu-id="a17ae-137">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
