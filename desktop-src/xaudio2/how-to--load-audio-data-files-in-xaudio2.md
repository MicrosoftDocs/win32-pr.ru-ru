---
description: В этом разделе описаны шаги по заполнению структур, необходимых для воспроизведения звуковых данных в XAudio2.
ms.assetid: caeb522e-d4f6-91e2-5e85-ea0af0f61300
title: 'Руководство: загрузка файлов звуковых данных в XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bacf08e8f16e5cd9c42409776b02846990b9d66d685a0186314445742f23341
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962663"
---
# <a name="how-to-load-audio-data-files-in-xaudio2"></a>Руководство: загрузка файлов звуковых данных в XAudio2

> [!Note]  
> это содержимое применяется только к классическим приложениям, и для работы в приложении для магазина Windows потребуется редакция. Обратитесь к документации по [**CreateFile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2), [**креативентекс**](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [**сетфилепоинтерекс**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)и [**жетоверлаппедресултекс**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex). см. саундфилереадер. h/. cpp в образце басиксаунд Windows 8 из [коллекции примеров Windows SDK](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208)).

 

В этом разделе описаны шаги по заполнению структур, необходимых для воспроизведения звуковых данных в XAudio2. Следующие шаги загружают фрагменты "fmt" и "Data" звукового файла и используют их для заполнения структуры **вавеформатекстенсибле** и структуры [**\_ буфера XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .

-   [Подготовка к синтаксическому анализу звукового файла.](#preparing-to-parse-the-audio-file)
-   [Заполнение структур XAudio2 содержимым блоков Metallica.](#populating-xaudio2-structures-with-the-contents-of-riff-chunks)

## <a name="preparing-to-parse-the-audio-file"></a>Подготовка к синтаксическому анализу звукового файла

Звуковые файлы, поддерживаемые XAudio2, используют формат файла обмена ресурсами (Metallica). Metallica описывается в обзоре [формата файла обмена ресурсами (Metallica)](resource-interchange-file-format--riff-.md) . Звуковые данные в файле Metallica загружаются путем поиска фрагмента Metallica и последующего прохода по блоку для поиска отдельных блоков, содержащихся в фрагменте Metallica. Следующие функции являются примерами кода для поиска фрагментов и загрузки данных, содержащихся в фрагментах.

-   Чтобы найти фрагмент в файле Metallica, выполните следующие действия.

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

    

-   Для чтения данных в блоке после их обнаружения.

    После обнаружения требуемого фрагмента его данные можно прочитать, настроив указатель файла на начало раздела данных фрагмента. Функция для считывания данных из фрагмента после их обнаружения может выглядеть следующим образом.

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

    

## <a name="populating-xaudio2-structures-with-the-contents-of-riff-chunks"></a>Заполнение структур XAudio2 содержимым блоков Metallica

Чтобы XAudio2 воспроизводил звук с исходным голосом, ему необходима структура **вавеформатекс** и структура [**\_ буфера XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . Структура **вавеформатекс** может быть более крупной структурой, такой как **вавеформатекстенсибле** , которая содержит структуру **вавеформатекс** в качестве первого элемента. Дополнительные сведения см. на странице справочника по **вавеформатекс** .

В этом примере используется **вавеформатекстенсибле** , чтобы разрешить загрузку звуковых файлов PCM с более чем двумя каналами.

Следующие шаги иллюстрируют использование описанных выше функций для заполнения структуры **вавеформатекстенсибле** и структуры [**\_ буфера XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . В этом случае загружаемый аудио-файл содержит данные PCM и будет содержать только фрагменты «Metallica», «FMT» и «Data». Другие форматы могут содержать дополнительные типы блоков, как описано в разделе [Формат файла обмена ресурсами (Metallica)](resource-interchange-file-format--riff-.md).

1.  Объявите [**\_ буферные**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) структуры **вавеформатекстенсибле** и XAUDIO2.
    ```
    WAVEFORMATEXTENSIBLE wfx = {0};
    XAUDIO2_BUFFER buffer = {0};
    ```

    

2.  Откройте звуковой файл с помощью CreateFile.
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

    

3.  Поиск фрагмента "Metallica" в звуковом файле и проверка типа файла.
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

    

4.  Нахождение блока fmt и копирование его содержимого в структуру **вавеформатекстенсибле** .
    ```
    FindChunk(hFile,fourccFMT, dwChunkSize, dwChunkPosition );
    ReadChunkData(hFile, &wfx, dwChunkSize, dwChunkPosition );
    ```

    

5.  Нахождение фрагмента данных и считывание его содержимого в буфер.
    ```
    //fill out the audio data buffer with the contents of the fourccDATA chunk
    FindChunk(hFile,fourccDATA,dwChunkSize, dwChunkPosition );
    BYTE * pDataBuffer = new BYTE[dwChunkSize];
    ReadChunkData(hFile, pDataBuffer, dwChunkSize, dwChunkPosition);
    ```

    

6.  Заполнение структуры [**\_ буфера XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .
    ```
    buffer.AudioBytes = dwChunkSize;  //size of the audio buffer in bytes
    buffer.pAudioData = pDataBuffer;  //buffer containing audio data
    buffer.Flags = XAUDIO2_END_OF_STREAM; // tell the source voice not to expect any data after this buffer
    ```

    

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Начало работы](getting-started.md)
</dt> <dt>

[Руководство: воспроизведение звука при помощи XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[Справочник по программированию в XAudio2](programming-reference.md)
</dt> </dl>

 

 
