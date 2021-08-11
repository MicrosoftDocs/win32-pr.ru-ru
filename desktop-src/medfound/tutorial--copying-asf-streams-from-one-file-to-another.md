---
description: Один из способов создания файла ASF заключается в копировании потоков ASF из существующего файла.
ms.assetid: 158fe3a1-42e6-461d-b56b-5419cd961fca
title: руководство. копирование ASF Потоки с помощью объектов вмконтаинер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2149358d216e044f3392b882a997ef4aa455ae799b6ece450bca11f0f22a6781
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237878"
---
# <a name="tutorial-copying-asf-streams-by-using-wmcontainer-objects"></a>руководство. копирование ASF Потоки с помощью объектов вмконтаинер

Один из способов создания файла ASF заключается в копировании потоков ASF из существующего файла. Для этого можно получить данные мультимедиа из исходного файла и выполнить запись в выходной файл. Если исходный файл является ASF-файлом, можно скопировать образцы потоков без распаковки и повторного сжатия.

В этом руководстве демонстрируется, как извлечь первый аудиопоток из файла аудио-видео ASF (WMV) и скопировать его в новый звуковой файл ASF (WMA). В этом руководстве вы создадите консольное приложение, которое принимает входные и выходные имена файлов в качестве аргументов. Приложение использует разделитель ASF для анализа примеров входного потока, а затем отправляет их мультиплексору ASF для записи пакетов данных ASF для аудиопотока.

Этот учебник содержит следующие действия.

-   [Предварительные требования](#prerequisites)
-   [Терминология](#terminology)
-   [1. Настройка Project](#1-set-up-the-project)
-   [2. объявление вспомогательных функций](#2-declare-helper-functions)
-   [3. Откройте входной ASF файл.](#3-open-the-input-asf-file)
-   [4. Инициализация объектов для входного файла](#4-initialize-objects-for-the-input-file)
-   [5. Создание профиля аудиоподсистемы](#5-create-an-audio-profile)
-   [6. Инициализация объектов для выходного файла](#6-initialize-objects-for-the-output-file)
-   [7. Генерация новых пакетов данных ASF](#7-generate-new-asf-data-packets)
-   [8. запись объектов ASF в новый файл](#8-write-the-asf-objects-in-the-new-file)
-   [9. Написание функции Entry-Point](#9-write-the-entry-point-function)
-   [Связанные темы](#related-topics)

## <a name="prerequisites"></a>Предварительные требования

В этом учебнике предполагается следующее:

-   Вы знакомы со структурой файла ASF и компонентами, предоставляемыми Media Foundation для работы с объектами ASF. К таким компонентам относятся Контентинфо, Splitter, мультиплексор и объекты профиля. Дополнительные сведения см. в разделе [компоненты ASF вмконтаинер](wmcontainer-asf-components.md).
-   Вы знакомы с процессом синтаксического анализа объекта заголовка ASF и пакетов данных ASF существующего файла и создания сжатых образцов потока с помощью разделителя. Дополнительные сведения см. [в разделе Учебник. чтение файла ASF](tutorial--reading-an-asf-file.md).
-   Вы знакомы с буферами мультимедиа и потоками байтов: в частности, операции с файлами с использованием потока байтов и запись содержимого буфера мультимедиа в поток байтов. (См [. раздел 2. Объявление вспомогательных функций](#2-declare-helper-functions).)

## <a name="terminology"></a>Терминология

В этом учебнике используются следующие термины:

-   Исходный поток байтов: объект потока байтов, предоставляющий интерфейс [**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , который содержит содержимое входного файла.
-   Исходный объект Контентинфо: Контентинфо, предоставляет интерфейс [**имфасфконтентинфо**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , представляющий объект заголовка ASF входного файла.
-   Звуковой профиль: объект Profile, предоставляет интерфейс [**имфасфпрофиле**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) , который содержит только звуковые потоки входного файла.
-   Пример Stream: пример носителя, предоставляющий интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , созданный разделителем, представляет данные мультимедиа выбранного потока, полученные из входного файла в сжатом состоянии.
-   Выходной объект Контентинфо: Контентинфо предоставляет интерфейс [**имфасфконтентинфо**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , который представляет объект заголовка ASF выходного файла.
-   Поток байтов данных: объект потока байтов, предоставляет интерфейс [**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , представляющий всю часть объекта данных ASF в выходном файле.
-   Пример пакета данных: носитель, предоставляющий интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , созданный мультиплексором, представляет пакет данных ASF, который будет записан в поток байтов данных.
-   Выходной поток байтов: объект потока байтов, предоставляющий интерфейс [**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , который содержит содержимое выходного файла.

## <a name="1-set-up-the-project"></a>1. Настройка Project

Включите в исходный файл следующие заголовки:


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <mferror.h>     // Media Foundation error codes
```



Ссылка на следующие файлы библиотеки:

-   мфплат. lib
-   MF. lib
-   мфууид. lib

Объявите функцию [саферелеасе](saferelease.md) :


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



## <a name="2-declare-helper-functions"></a>2. объявление вспомогательных функций

В этом руководстве используются следующие вспомогательные функции для чтения и записи из байтового потока.

`AllocReadFromByteStream`Функция считывает данные из байтового потока и выделяет новый буфер мультимедиа для хранения данных. Дополнительные сведения см. в разделе [**имфбитестреам:: Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).


```C++
//-------------------------------------------------------------------
// AllocReadFromByteStream
//
// Reads data from a byte stream and returns a media buffer that
// contains the data.
//-------------------------------------------------------------------

HRESULT AllocReadFromByteStream(
    IMFByteStream *pStream,         // Pointer to the byte stream.
    DWORD cbToRead,                 // Number of bytes to read.
    IMFMediaBuffer **ppBuffer       // Receives a pointer to the media buffer. 
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;
    DWORD cbRead = 0;   // Actual amount of data read.

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer. 
    // This function allocates the memory for the buffer.
    hr = MFCreateMemoryBuffer(cbToRead, &pBuffer);

    // Get a pointer to the memory buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    // Read the data from the byte stream.
    if (SUCCEEDED(hr))
    {
        hr = pStream->Read(pData, cbToRead, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    if (pData)
    {
        pBuffer->Unlock();
    }
    SafeRelease(&pBuffer);
    return hr;
}
```



`WriteBufferToByteStream`Функция записывает данные из буфера мультимедиа в байтовый поток. Дополнительные сведения см. в разделе [**имфбитестреам:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).


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



`AppendToByteStream`Функция добавляет содержимое одного потока байтов в другой:


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



## <a name="3-open-the-input-asf-file"></a>3. Откройте входной ASF файл.

Откройте входной файл, вызвав функцию [**мфкреатефиле**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) . Метод возвращает указатель на объект байтового потока, который содержит содержимое файла. Имя файла задается пользователем с помощью аргументов командной строки приложения.

В следующем примере кода принимается имя файла и возвращается указатель на объект байтового потока, который может быть использован для чтения файла.


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="4-initialize-objects-for-the-input-file"></a>4. Инициализация объектов для входного файла

Далее предстоит создать и инициализировать исходный объект Контентинфо и разделитель для создания примеров потока.

Этот исходный поток байтов, созданный на шаге 2, будет использоваться для синтаксического анализа объекта заголовка ASF и заполнения исходного объекта Контентинфо. Этот объект будет использоваться для инициализации разделителя, чтобы упростить анализ пакетов данных ASF для звукового потока во входном файле. Вы также получите длину объекта данных ASF во входном файле и смещение первого пакета данных ASF относительно начала файла. Эти атрибуты будут использоваться разделителем для создания образцов звуковых потоков.

Чтобы создать и инициализировать компоненты ASF для входного файла, выполните следующие действия.

1.  Вызовите [**мфкреатеасфконтентинфо**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , чтобы создать объект контентинфо. Эта функция возвращает указатель на интерфейс [**имфасфконтентинфо**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) .
2.  Вызовите [**имфасфконтентинфо::P арсехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) , чтобы проанализировать заголовок ASF. Дополнительные сведения об этом шаге см. [в разделе чтение объекта заголовка ASF существующего файла](reading-the-asf-header-object-of-an-existing-file.md).
3.  Вызовите [**мфкреатеасфсплиттер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) , чтобы создать объект разделителя ASF. Эта функция возвращает указатель на интерфейс [**имфасфсплиттер**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .
4.  Вызовите [**имфасфсплиттер:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize), передав указатель [**имфасфконтентинфо**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo). Дополнительные сведения об этом шаге см. [в разделе Создание объекта РАЗДЕЛИТЕЛЯ ASF](creating-the-asf-splitter-object.md).
5.  Вызовите [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) , чтобы получить дескриптор представления для ASF-файла.
6.  Получите значение атрибута [**\_ \_ \_ \_ \_ смещения начальной загрузки данных MF PD ASF**](mf-pd-asf-data-start-offset-attribute.md) из дескриптора презентации. Это значение представляет собой расположение объекта данных ASF в файле в виде смещения в байтах от начала файла.
7.  Получите значение атрибута [**\_ \_ \_ \_ длины данных в формате MF PD ASF**](mf-pd-asf-data-length-attribute.md) из дескриптора презентации. Это значение представляет собой общий размер объекта данных ASF в байтах. Дополнительные сведения см. [в разделе Получение сведений из объектов заголовка ASF](getting-information-from-asf-header-objects.md).

В следующем примере кода показана функция, которая объединяет все шаги. Эта функция принимает указатель на исходный поток байтов и возвращает указатели на исходный объект Контентинфо и разделитель. Кроме того, он получает длину и смещение для объекта данных ASF.


```C++
//-------------------------------------------------------------------
// CreateSourceParsers
//
// Creates the ASF splitter and the ASF Content Info object for the 
// source file.
// 
// This function also calulates the offset and length of the ASF 
// Data Object.
//-------------------------------------------------------------------

HRESULT CreateSourceParsers(
    IMFByteStream *pSourceStream,
    IMFASFContentInfo **ppSourceContentInfo,
    IMFASFSplitter **ppSplitter,
    UINT64 *pcbDataOffset,
    UINT64 *pcbDataLength
    )
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;

    IMFMediaBuffer *pBuffer = NULL;
    IMFPresentationDescriptor *pPD = NULL;
    IMFASFContentInfo *pSourceContentInfo = NULL;
    IMFASFSplitter *pSplitter = NULL;

    QWORD cbHeader = 0;

    /*------- Parse the ASF header. -------*/

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pSourceContentInfo);
    
    // Read the first 30 bytes to find the total header size.
    if (SUCCEEDED(hr))
    {
        hr = AllocReadFromByteStream(
            pSourceStream, 
            MIN_ASF_HEADER_SIZE, 
            &pBuffer
            );
    }

    // Get the header size.
    if (SUCCEEDED(hr))
    {
        hr = pSourceContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Release the buffer; we will reuse it.
    SafeRelease(&pBuffer);
    
    // Read the entire header into a buffer.
    if (SUCCEEDED(hr))
    {
        hr = pSourceStream->SetCurrentPosition(0);
    }

    if (SUCCEEDED(hr))
    {
        hr = AllocReadFromByteStream(
            pSourceStream, 
            (DWORD)cbHeader, 
            &pBuffer
            );
    }

    // Parse the buffer and populate the header object.
    if (SUCCEEDED(hr))
    {
        hr = pSourceContentInfo->ParseHeader(pBuffer, 0);
    }

    /*------- Initialize the ASF splitter. -------*/

    // Create the splitter.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFSplitter(&pSplitter);
    }
    
    // initialize the splitter with the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pSourceContentInfo);
    }


    /*------- Get the offset and size of the ASF Data Object. -------*/

    // Generate the presentation descriptor.
    if (SUCCEEDED(hr))
    {
        hr =  pSourceContentInfo->GeneratePresentationDescriptor(&pPD);
    }

    // Get the offset to the start of the Data Object.
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_DATA_START_OFFSET, pcbDataOffset);
    }

    // Get the length of the Data Object.
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_DATA_LENGTH, pcbDataLength);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppSourceContentInfo = pSourceContentInfo;
        (*ppSourceContentInfo)->AddRef();

        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();

    }

    SafeRelease(&pPD);
    SafeRelease(&pBuffer);
    SafeRelease(&pSourceContentInfo);
    SafeRelease(&pSplitter);

    return S_OK;
}
```



## <a name="5-create-an-audio-profile"></a>5. Создание профиля аудиоподсистемы

Далее предстоит создать объект профиля для входного файла, получая его из исходного объекта Контентинфо. Затем вы настроите профиль таким образом, чтобы он содержал только звуковые потоки входного файла. Для этого перечислите потоки и удалите из профиля потоки, не являющиеся звуками. Объект профиля аудиоподсистемы будет использоваться далее в этом руководстве для инициализации выходного объекта Контентинфо.

Создание профиля аудиоподсистемы

1.  Получите объект профиля для входного файла из исходного объекта Контентинфо, вызвав [**имфасфконтентинфо:: i Profile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile). Метод возвращает указатель на объект Profile, содержащий все потоки во входном файле. Дополнительные сведения см. [в разделе Создание профиля ASF](creating-an-asf-profile.md).
2.  Удалите из профиля все взаимоисключающие объекты. Этот шаг необходим, так как потоки, не являющиеся звуками, будут удалены из профиля, что может сделать недействительными взаимоисключающие объекты.
3.  Удалите все незвуковые потоки из профиля следующим образом:
    -   Вызовите метод [**имфасфпрофиле:: жетстреамкаунт**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) , чтобы получить количество потоков.
    -   В цикле вызовите [**имфасфпрофиле::-Stream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) , чтобы получить каждый поток по индексу.
    -   Вызовите метод [**имфасфстреамконфиг:: жетстреамтипе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) , чтобы получить тип потока.
    -   Для незвуковых потоков вызовите метод [**имфасфпрофиле:: ремовестреам**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) , чтобы удалить поток.
4.  Сохранить номер потока первого звукового потока. Он будет выбран в разделителе для создания примеров потока. Если номер потока равен нулю, вызывающий объект может предположить, что отсутствует файл звуковых потоков.

Эти действия выполняются в следующем коде:


```C++
//-------------------------------------------------------------------
// GetAudioProfile
//
// Gets the ASF profile from the source file and removes any video
// streams from the profile.
//-------------------------------------------------------------------

HRESULT GetAudioProfile(
    IMFASFContentInfo *pSourceContentInfo, 
    IMFASFProfile **ppAudioProfile, 
    WORD *pwSelectStreamNumber
    )
{
    IMFASFStreamConfig *pStream = NULL;
    IMFASFProfile *pProfile = NULL;

    DWORD dwTotalStreams = 0;
    WORD  wStreamNumber = 0; 
    GUID guidMajorType = GUID_NULL;
    
    // Get the profile object from the source ContentInfo object.
    HRESULT hr = pSourceContentInfo->GetProfile(&pProfile);

    // Remove mutexes from the profile
    if (SUCCEEDED(hr))
    {
        hr = RemoveMutexes(pProfile);
    }

    // Get the total number of streams on the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&dwTotalStreams);
    }

    // Enumerate the streams and remove the non-audio streams.
    if (SUCCEEDED(hr))
    {
        for (DWORD index = 0; index < dwTotalStreams; )
        {
            hr = pProfile->GetStream(index, &wStreamNumber, &pStream);

            if (FAILED(hr)) { break; }

            hr = pStream->GetStreamType(&guidMajorType);

            SafeRelease(&pStream);

            if (FAILED(hr)) { break; }

            if (guidMajorType != MFMediaType_Audio)
            {
                hr = pProfile->RemoveStream(wStreamNumber);
    
                if (FAILED(hr)) { break; }

                index = 0;
                dwTotalStreams--;
            }
            else
            {
                // Store the first audio stream number. 
                // This will be selected on the splitter.

                if (*pwSelectStreamNumber == 0)
                {
                    *pwSelectStreamNumber = wStreamNumber;
                }

                index++;
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        *ppAudioProfile = pProfile;
        (*ppAudioProfile)->AddRef();
    }

    SafeRelease(&pStream);
    SafeRelease(&pProfile);

    return S_OK;
}
```



`RemoveMutexes`Функция удаляет все взаимоисключающие объекты из профиля:


```C++
HRESULT RemoveMutexes(IMFASFProfile *pProfile)
{
    DWORD cMutex = 0;
    HRESULT hr = pProfile->GetMutualExclusionCount(&cMutex);

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cMutex; i++)
        {
            hr = pProfile->RemoveMutualExclusion(0);

            if (FAILED(hr))
            {
                break;
            }
        }
    }

    return hr;
}
```



## <a name="6-initialize-objects-for-the-output-file"></a>6. Инициализация объектов для выходного файла

Далее предстоит создать выходной объект Контентинфо и мультиплексор для создания пакетов данных для выходного файла.

Звуковой профиль, созданный на шаге 4, будет использоваться для заполнения выходного объекта Контентинфо. Этот объект содержит такие сведения, как глобальные атрибуты файлов и свойства потока. Выходной объект Контентинфо будет использоваться для инициализации мультиплексора, который будет формировать пакеты данных для выходного файла. После создания пакетов данных необходимо обновить объект Контентинфо, чтобы отразить новые значения.

Создание и инициализация компонентов ASF для выходного файла

1.  Создайте пустой объект Контентинфо, вызвав [**мфкреатеасфконтентинфо**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , и заполните его данными из аудио профиля, созданного на шаге 3, вызвав [**Имфасфконтентинфо:: сетпрофиле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile). Дополнительные сведения см. [в разделе Инициализация объекта Контентинфо нового ASF-файла](initializing-the-contentinfo-object-of-a-new-asf-file.md).
2.  Создайте и инициализируйте объект мультиплексора с помощью выходного объекта Контентинфо. Дополнительные сведения см. [в разделе Создание объекта мультиплексора](creating-the-multiplexer-object.md).

В следующем примере кода показана функция, которая объединяет шаги. Эта функция принимает указатель на объект Profile и возвращает указатели на выходной объект Контентинфо и мультиплексор.


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



## <a name="7-generate-new-asf-data-packets"></a>7. Генерация новых пакетов данных ASF

Далее предстоит создать образцы звуковых потоков из исходного потока байтов с помощью разделителя и отправить их мультиплексору для создания пакетов данных ASF. Эти пакеты данных будут составлять окончательный объект данных ASF для нового файла.

Создание образцов аудиопотока

1.  Выберите первый аудиопоток в разделителе, вызвав [**имфасфсплиттер:: селектстреамс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams).
2.  Чтение блоков фиксированного размера данных мультимедиа из исходного потока байтов в буфер мультимедиа.
3.  Собирайте примеры потоков как образцы мультимедиа из разделителя, вызывая [**имфасфсплиттер:: жетнекстсампле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) в цикле, если он получает \_ флаг ASF статусфлагс \_ неполный в параметре *пдвстатусфлагс* . Дополнительные сведения см. в разделе Создание образцов для пакетов данных ASF статьи [Создание примеров потоков из существующего объекта данных ASF](generating-stream-samples-from-an-existing-asf-data-object.md).
4.  Для каждого примера носителя вызовите [**имфасфмултиплексер::P роцесссампле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) , чтобы отправить пример мультимедиа в мультиплексор. Мультиплексор создает пакеты данных для объекта данных ASF.
5.  Запишите пакет данных, созданный мультиплексором, в поток байтов данных.
6.  После создания всех пакетов данных вызовите метод [**имфасфмултиплексер:: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) , чтобы обновить выходной объект контентинфо со сведениями, собранными во время создания пакета данных ASF.

В следующем примере кода создаются образцы Stream из разделителя ASF и они отправляются в мультиплексор. Мультиплексор создает пакеты данных ASF и записывает их в поток.


```C++
//-------------------------------------------------------------------
// GenerateASFDataObject
// 
// Creates a byte stream that contains the ASF Data Object for the
// output file.
//-------------------------------------------------------------------

HRESULT GenerateASFDataObject(
    IMFByteStream *pSourceStream, 
    IMFASFSplitter *pSplitter, 
    IMFASFMultiplexer *pMux, 
    UINT64   cbDataOffset,
    UINT64   cbDataLength,
    IMFByteStream **ppDataStream
    )
{
    IMFMediaBuffer *pBuffer = NULL;
    IMFByteStream *pDataStream = NULL;
    
    const DWORD READ_SIZE = 1024 * 4;

    // Flush the splitter to remove any pending samples.
    HRESULT hr = pSplitter->Flush();

    if (SUCCEEDED(hr))
    {
        hr = MFCreateTempFile(
            MF_ACCESSMODE_READWRITE, 
            MF_OPENMODE_DELETE_IF_EXIST,
            MF_FILEFLAGS_NONE,
            &pDataStream
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = pSourceStream->SetCurrentPosition(cbDataOffset);
    }

    if (SUCCEEDED(hr))
    {
        while (cbDataLength > 0)
        {
            DWORD cbRead = min(READ_SIZE, (DWORD)cbDataLength);

            hr = AllocReadFromByteStream(
                pSourceStream, 
                cbRead, 
                &pBuffer
                );

            if (FAILED(hr)) 
            { 
                break; 
            }

            cbDataLength -= cbRead;

            // Push data on the splitter.
            hr =  pSplitter->ParseData(pBuffer, 0, 0);

            if (FAILED(hr)) 
            { 
                break; 
            }

            // Get ASF packets from the splitter and feed them to the mux.
            hr = GetPacketsFromSplitter(pSplitter, pMux, pDataStream);

            if (FAILED(hr)) 
            { 
                break; 
            }

            SafeRelease(&pBuffer);
        }
    }

    // Flush the mux and generate any remaining samples.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Flush();
    }

    if (SUCCEEDED(hr))
    {
        hr = GenerateASFDataPackets(pMux, pDataStream);
    }

     // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppDataStream = pDataStream;
        (*ppDataStream)->AddRef();
    }

    SafeRelease(&pBuffer);
    SafeRelease(&pDataStream);
    return hr;
}
```



Чтобы получить пакеты из разделителя ASF, предыдущий код вызывает `GetPacketsFromSplitter` функцию, показанную ниже:


```C++
//-------------------------------------------------------------------
// GetPacketsFromSplitter
//
// Gets samples from the ASF splitter.
//
// This function is called after calling IMFASFSplitter::ParseData.
//-------------------------------------------------------------------

HRESULT GetPacketsFromSplitter(
    IMFASFSplitter *pSplitter,
    IMFASFMultiplexer *pMux,
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;
    DWORD   dwStatus = ASF_STATUSFLAGS_INCOMPLETE;
    WORD    wStreamNum = 0;

    IMFSample *pSample = NULL;

    while (dwStatus & ASF_STATUSFLAGS_INCOMPLETE) 
    {
        hr = pSplitter->GetNextSample(&dwStatus, &wStreamNum, &pSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pSample)
        {
            //Send to the multiplexer to convert it into ASF format
            hr = pMux->ProcessSample(wStreamNum, pSample, 0);

            if (FAILED(hr)) 
            { 
                break; 
            }

            hr = GenerateASFDataPackets(pMux, pDataStream);

            if (FAILED(hr)) 
            { 
                break; 
            }
        }

        SafeRelease(&pSample);
    }

    SafeRelease(&pSample);
    return hr;
}
```



`GenerateDataPackets`Функция получает пакеты данных от мультиплексора. Дополнительные сведения см. в разделе [Получение пакетов данных ASF](generating-new-asf-data-packets.md).


```C++
//-------------------------------------------------------------------
// GenerateASFDataPackets
// 
// Gets data packets from the mux. This function is called after 
// calling IMFASFMultiplexer::ProcessSample. 
//-------------------------------------------------------------------

HRESULT GenerateASFDataPackets( 
    IMFASFMultiplexer *pMux, 
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;

    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacketBuffer = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pOutputSample)
        {
            //Convert to contiguous buffer
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacketBuffer);
            
            if (FAILED(hr))
            {
                break;
            }

            //Write buffer to byte stream
            hr = WriteBufferToByteStream(pDataStream, pDataPacketBuffer, NULL);

            if (FAILED(hr))
            {
                break;
            }
        }

        SafeRelease(&pDataPacketBuffer);
        SafeRelease(&pOutputSample);
    }

    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacketBuffer);
    return hr;
}
```



## <a name="8-write-the-asf-objects-in-the-new-file"></a>8. запись объектов ASF в новый файл

Далее предстоит записать содержимое выходного объекта Контентинфо в буфер мультимедиа, вызвав [**имфасфконтентинфо:: женератехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader). Этот метод преобразует данные, хранящиеся в объекте Контентинфо, в двоичные данные в формате файла заголовка ASF. Дополнительные сведения см. [в разделе Создание нового объекта заголовка ASF](generating-a-new-asf-header-object.md).

После создания нового объекта заголовка ASF запишите выходной файл, сначала записав объект заголовка в выходной поток байтов, созданный на шаге 2, вызвав вспомогательную функцию Вритебуффертобитестреам. Используйте объект заголовка с объектом данных, содержащимся в потоке байтов данных. В примере кода показана функция, которая передает содержимое потока байтов данных в выходной поток байтов.


```C++
//-------------------------------------------------------------------
// WriteASFFile
//
// Writes the complete ASF file.
//-------------------------------------------------------------------

HRESULT WriteASFFile( 
    IMFASFContentInfo *pContentInfo, // ASF Content Info for the output file.
    IMFByteStream *pDataStream,      // Data stream.
    PCWSTR pszFile                   // Output file name.
    )
{
    
    IMFMediaBuffer *pHeaderBuffer = NULL;
    IMFByteStream *pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    // Create output file.
    HRESULT hr = MFCreateFile(
        MF_ACCESSMODE_WRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        pszFile,
        &pWmaStream
        );

    // Get the size of the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(NULL, &cbHeaderSize);
    }

    // Create a media buffer.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    }

    // Populate the media buffer with the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    }
 
    // Write the header contents to the byte stream for the output file.
    if (SUCCEEDED(hr))
    {
        hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        hr = pDataStream->SetCurrentPosition(0);
    }

    // Append the data stream to the file.

    if (SUCCEEDED(hr))
    {
        hr = AppendToByteStream(pDataStream, pWmaStream);
    }

    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);

    return hr;
}
```



## <a name="9-write-the-entry-point-function"></a>9. Написание функции Entry-Point

Теперь можно объединить предыдущие шаги в законченное приложение. Перед использованием любого объекта Media Foundation инициализируйте Media Foundationную платформу, вызвав [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). По завершении вызовите [**мфшутдовн**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown). Дополнительные сведения см. в разделе [инициализация Media Foundation](initializing-media-foundation.md).

В следующем коде показано полное консольное приложение. Аргумент командной строки задает имя файла для преобразования и имя нового звукового файла.


```C++
int wmain(int argc, WCHAR* argv[])
{
    if (argc != 3)
    {
        wprintf_s(L"Usage: %s input.wmv, %s output.wma\n");
        return 0;
    }

    HRESULT hr = MFStartup(MF_VERSION);

    if (FAILED(hr))
    {
        wprintf_s(L"MFStartup failed: 0x%X\n", hr);
        return 0;
    }

    PCWSTR pszInputFile = argv[1];      
    PCWSTR pszOutputFile = argv[2];     
    
    IMFByteStream      *pSourceStream = NULL;       
    IMFASFContentInfo  *pSourceContentInfo = NULL;  
    IMFASFProfile      *pAudioProfile = NULL;       
    IMFASFContentInfo  *pOutputContentInfo = NULL;  
    IMFByteStream      *pDataStream = NULL;         
    IMFASFSplitter     *pSplitter = NULL;           
    IMFASFMultiplexer  *pMux = NULL;                

    UINT64  cbDataOffset = 0;           
    UINT64  cbDataLength = 0;           
    WORD    wSelectStreamNumber = 0;    

    // Open the input file.

    hr = OpenFile(pszInputFile, &pSourceStream);

    // Initialize the objects that will parse the source file.

    if (SUCCEEDED(hr))
    {
        hr = CreateSourceParsers(
            pSourceStream, 
            &pSourceContentInfo,    // ASF Header for the source file.
            &pSplitter,             // Generates audio samples.
            &cbDataOffset,          // Offset to the first data packet.
            &cbDataLength           // Length of the ASF Data Object.
            );
    }

    // Create a profile object for the audio streams in the source file.

    if (SUCCEEDED(hr))
    {
        hr = GetAudioProfile(
            pSourceContentInfo, 
            &pAudioProfile,         // ASF profile for the audio stream.
            &wSelectStreamNumber    // Stream number of the first audio stream.
            );
    }

    // Initialize the objects that will generate the output data.

    if (SUCCEEDED(hr))
    {
        hr = CreateOutputGenerators(
            pAudioProfile, 
            &pOutputContentInfo,    // ASF Header for the output file.
            &pMux                   // Generates ASF data packets.
            );
    }

    // Set up the splitter to generate samples for the first
    // audio stream in the source media.

    if (SUCCEEDED(hr))
    {
        hr = pSplitter->SelectStreams(&wSelectStreamNumber, 1);
    }
    
    // Generate ASF Data Packets and store them in a byte stream.

    if (SUCCEEDED(hr))
    {
        hr = GenerateASFDataObject(
               pSourceStream, 
               pSplitter, 
               pMux, 
               cbDataOffset, 
               cbDataLength, 
               &pDataStream    // Byte stream for the ASF data packets.    
               );
    }

    // Update the header with new information if any.

    if (SUCCEEDED(hr))
    {
        hr = pMux->End(pOutputContentInfo);
    }

    //Write the ASF objects to the output file
    if (SUCCEEDED(hr))
    {
        hr = WriteASFFile(pOutputContentInfo, pDataStream, pszOutputFile);
    }

    // Clean up.
    SafeRelease(&pMux);
    SafeRelease(&pSplitter);
    SafeRelease(&pDataStream);
    SafeRelease(&pOutputContentInfo);
    SafeRelease(&pAudioProfile);
    SafeRelease(&pSourceContentInfo);
    SafeRelease(&pSourceStream);

    MFShutdown();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the audio file: 0x%X\n", hr);
    }

    return 0;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Компоненты ASF Вмконтаинер](wmcontainer-asf-components.md)
</dt> <dt>

[Поддержка ASF в Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



