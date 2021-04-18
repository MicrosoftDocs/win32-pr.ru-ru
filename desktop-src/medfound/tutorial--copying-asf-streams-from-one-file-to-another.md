---
description: Один из способов создания файла ASF заключается в копировании потоков ASF из существующего файла.
ms.assetid: 158fe3a1-42e6-461d-b56b-5419cd961fca
title: Руководство. копирование потоков ASF с помощью объектов Вмконтаинер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44bac13626a8c80f474eeb029db4eb1351273910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692780"
---
# <a name="tutorial-copying-asf-streams-by-using-wmcontainer-objects"></a><span data-ttu-id="e7045-103">Руководство. копирование потоков ASF с помощью объектов Вмконтаинер</span><span class="sxs-lookup"><span data-stu-id="e7045-103">Tutorial: Copying ASF Streams by Using WMContainer Objects</span></span>

<span data-ttu-id="e7045-104">Один из способов создания файла ASF заключается в копировании потоков ASF из существующего файла.</span><span class="sxs-lookup"><span data-stu-id="e7045-104">One way to create an ASF file is to copy ASF streams from an existing file.</span></span> <span data-ttu-id="e7045-105">Для этого можно получить данные мультимедиа из исходного файла и выполнить запись в выходной файл.</span><span class="sxs-lookup"><span data-stu-id="e7045-105">To do this, you can retrieve the media data from the source file and write to the output file.</span></span> <span data-ttu-id="e7045-106">Если исходный файл является ASF-файлом, можно скопировать образцы потоков без распаковки и повторного сжатия.</span><span class="sxs-lookup"><span data-stu-id="e7045-106">If the source file is an ASF file, you can copy stream samples without decompressing and recompressing them.</span></span>

<span data-ttu-id="e7045-107">В этом руководстве демонстрируется, как извлечь первый аудиопоток из файла аудио-видео ASF (WMV) и скопировать его в новый звуковой файл ASF (WMA).</span><span class="sxs-lookup"><span data-stu-id="e7045-107">This tutorial demonstrates this scenario by extracting the first audio stream from an ASF audio-video file (.wmv) and copying it to a new ASF audio file (.wma).</span></span> <span data-ttu-id="e7045-108">В этом руководстве вы создадите консольное приложение, которое принимает входные и выходные имена файлов в качестве аргументов.</span><span class="sxs-lookup"><span data-stu-id="e7045-108">In this tutorial, you will create a console application that takes the input and output filenames as arguments.</span></span> <span data-ttu-id="e7045-109">Приложение использует разделитель ASF для анализа примеров входного потока, а затем отправляет их мультиплексору ASF для записи пакетов данных ASF для аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="e7045-109">The application uses the ASF Splitter to parse the input stream samples and then sends them to the ASF Multiplexer to write the ASF data packets for the audio stream.</span></span>

<span data-ttu-id="e7045-110">Этот учебник содержит следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e7045-110">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="e7045-111">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="e7045-111">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="e7045-112">Терминология</span><span class="sxs-lookup"><span data-stu-id="e7045-112">Terminology</span></span>](#terminology)
-   [<span data-ttu-id="e7045-113">1. Настройка проекта</span><span class="sxs-lookup"><span data-stu-id="e7045-113">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="e7045-114">2. объявление вспомогательных функций</span><span class="sxs-lookup"><span data-stu-id="e7045-114">2. Declare Helper Functions</span></span>](#2-declare-helper-functions)
-   [<span data-ttu-id="e7045-115">3. Откройте входной ASF файл.</span><span class="sxs-lookup"><span data-stu-id="e7045-115">3. Open the Input ASF File</span></span>](#3-open-the-input-asf-file)
-   [<span data-ttu-id="e7045-116">4. Инициализация объектов для входного файла</span><span class="sxs-lookup"><span data-stu-id="e7045-116">4. Initialize Objects for the Input File</span></span>](#4-initialize-objects-for-the-input-file)
-   [<span data-ttu-id="e7045-117">5. Создание профиля аудиоподсистемы</span><span class="sxs-lookup"><span data-stu-id="e7045-117">5. Create an Audio Profile</span></span>](#5-create-an-audio-profile)
-   [<span data-ttu-id="e7045-118">6. Инициализация объектов для выходного файла</span><span class="sxs-lookup"><span data-stu-id="e7045-118">6. Initialize Objects for the Output File</span></span>](#6-initialize-objects-for-the-output-file)
-   [<span data-ttu-id="e7045-119">7. Генерация новых пакетов данных ASF</span><span class="sxs-lookup"><span data-stu-id="e7045-119">7. Generate New ASF Data Packets</span></span>](#7-generate-new-asf-data-packets)
-   [<span data-ttu-id="e7045-120">8. запись объектов ASF в новый файл</span><span class="sxs-lookup"><span data-stu-id="e7045-120">8. Write the ASF Objects in the New File</span></span>](#8-write-the-asf-objects-in-the-new-file)
-   [<span data-ttu-id="e7045-121">9. Написание функции Entry-Point</span><span class="sxs-lookup"><span data-stu-id="e7045-121">9 Write the Entry-Point Function</span></span>](#9-write-the-entry-point-function)
-   [<span data-ttu-id="e7045-122">См. также</span><span class="sxs-lookup"><span data-stu-id="e7045-122">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="e7045-123">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="e7045-123">Prerequisites</span></span>

<span data-ttu-id="e7045-124">В этом учебнике предполагается следующее:</span><span class="sxs-lookup"><span data-stu-id="e7045-124">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="e7045-125">Вы знакомы со структурой файла ASF и компонентами, предоставляемыми Media Foundation для работы с объектами ASF.</span><span class="sxs-lookup"><span data-stu-id="e7045-125">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="e7045-126">К таким компонентам относятся Контентинфо, Splitter, мультиплексор и объекты профиля.</span><span class="sxs-lookup"><span data-stu-id="e7045-126">These components include ContentInfo, splitter, multiplexer, and profile objects.</span></span> <span data-ttu-id="e7045-127">Дополнительные сведения см. в разделе [компоненты ASF вмконтаинер](wmcontainer-asf-components.md).</span><span class="sxs-lookup"><span data-stu-id="e7045-127">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="e7045-128">Вы знакомы с процессом синтаксического анализа объекта заголовка ASF и пакетов данных ASF существующего файла и создания сжатых образцов потока с помощью разделителя.</span><span class="sxs-lookup"><span data-stu-id="e7045-128">You are familiar with the process of parsing the ASF Header Object and the ASF data packets of an existing file and generating compressed stream samples by using the splitter.</span></span> <span data-ttu-id="e7045-129">Дополнительные сведения см. [в разделе Учебник. чтение файла ASF](tutorial--reading-an-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="e7045-129">For more information see [Tutorial: Reading an ASF File](tutorial--reading-an-asf-file.md).</span></span>
-   <span data-ttu-id="e7045-130">Вы знакомы с буферами мультимедиа и потоками байтов: в частности, операции с файлами с использованием потока байтов и запись содержимого буфера мультимедиа в поток байтов.</span><span class="sxs-lookup"><span data-stu-id="e7045-130">You are familiar with media buffers and byte streams: Specifically, file operations using a byte stream, and writing the contents of a media buffer into a byte stream.</span></span> <span data-ttu-id="e7045-131">(См [. раздел 2. Объявление вспомогательных функций](#2-declare-helper-functions).)</span><span class="sxs-lookup"><span data-stu-id="e7045-131">(See [2. Declare Helper Functions](#2-declare-helper-functions).)</span></span>

## <a name="terminology"></a><span data-ttu-id="e7045-132">Терминология</span><span class="sxs-lookup"><span data-stu-id="e7045-132">Terminology</span></span>

<span data-ttu-id="e7045-133">В этом учебнике используются следующие термины:</span><span class="sxs-lookup"><span data-stu-id="e7045-133">This tutorial uses the following terms:</span></span>

-   <span data-ttu-id="e7045-134">Исходный поток байтов: объект потока байтов, предоставляющий интерфейс [**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , который содержит содержимое входного файла.</span><span class="sxs-lookup"><span data-stu-id="e7045-134">Source byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the input file.</span></span>
-   <span data-ttu-id="e7045-135">Исходный объект Контентинфо: Контентинфо, предоставляет интерфейс [**имфасфконтентинфо**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , представляющий объект заголовка ASF входного файла.</span><span class="sxs-lookup"><span data-stu-id="e7045-135">Source ContentInfo object: ContentInfo object, exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the input file.</span></span>
-   <span data-ttu-id="e7045-136">Звуковой профиль: объект Profile, предоставляет интерфейс [**имфасфпрофиле**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) , который содержит только звуковые потоки входного файла.</span><span class="sxs-lookup"><span data-stu-id="e7045-136">Audio profile: Profile object, exposes [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface, which contains only audio streams of the input file.</span></span>
-   <span data-ttu-id="e7045-137">Пример Stream: пример носителя, предоставляющий интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , созданный разделителем, представляет данные мультимедиа выбранного потока, полученные из входного файла в сжатом состоянии.</span><span class="sxs-lookup"><span data-stu-id="e7045-137">Stream sample: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the splitter represents the selected stream's media data obtained from the input file in compressed state.</span></span>
-   <span data-ttu-id="e7045-138">Выходной объект Контентинфо: Контентинфо предоставляет интерфейс [**имфасфконтентинфо**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , который представляет объект заголовка ASF выходного файла.</span><span class="sxs-lookup"><span data-stu-id="e7045-138">Output ContentInfo object: ContentInfo object, exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the output file.</span></span>
-   <span data-ttu-id="e7045-139">Поток байтов данных: объект потока байтов, предоставляет интерфейс [**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , представляющий всю часть объекта данных ASF в выходном файле.</span><span class="sxs-lookup"><span data-stu-id="e7045-139">Data byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which represents the entire ASF Data Object portion of the output file.</span></span>
-   <span data-ttu-id="e7045-140">Пример пакета данных: носитель, предоставляющий интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , созданный мультиплексором, представляет пакет данных ASF, который будет записан в поток байтов данных.</span><span class="sxs-lookup"><span data-stu-id="e7045-140">Data packet: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the multiplexer represents an ASF data packet that will be written to the data byte stream.</span></span>
-   <span data-ttu-id="e7045-141">Выходной поток байтов: объект потока байтов, предоставляющий интерфейс [**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , который содержит содержимое выходного файла.</span><span class="sxs-lookup"><span data-stu-id="e7045-141">Output byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the output file.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="e7045-142">1. Настройка проекта</span><span class="sxs-lookup"><span data-stu-id="e7045-142">1. Set up the Project</span></span>

<span data-ttu-id="e7045-143">Включите в исходный файл следующие заголовки:</span><span class="sxs-lookup"><span data-stu-id="e7045-143">Include the following headers in your source file:</span></span>


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <mferror.h>     // Media Foundation error codes
```



<span data-ttu-id="e7045-144">Ссылка на следующие файлы библиотеки:</span><span class="sxs-lookup"><span data-stu-id="e7045-144">Link to the following library files:</span></span>

-   <span data-ttu-id="e7045-145">мфплат. lib</span><span class="sxs-lookup"><span data-stu-id="e7045-145">mfplat.lib</span></span>
-   <span data-ttu-id="e7045-146">MF. lib</span><span class="sxs-lookup"><span data-stu-id="e7045-146">mf.lib</span></span>
-   <span data-ttu-id="e7045-147">мфууид. lib</span><span class="sxs-lookup"><span data-stu-id="e7045-147">mfuuid.lib</span></span>

<span data-ttu-id="e7045-148">Объявите функцию [саферелеасе](saferelease.md) :</span><span class="sxs-lookup"><span data-stu-id="e7045-148">Declare the [SafeRelease](saferelease.md) function:</span></span>


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



## <a name="2-declare-helper-functions"></a><span data-ttu-id="e7045-149">2. объявление вспомогательных функций</span><span class="sxs-lookup"><span data-stu-id="e7045-149">2. Declare Helper Functions</span></span>

<span data-ttu-id="e7045-150">В этом руководстве используются следующие вспомогательные функции для чтения и записи из байтового потока.</span><span class="sxs-lookup"><span data-stu-id="e7045-150">This tutorial uses the following helper functions to read and write from a byte stream.</span></span>

<span data-ttu-id="e7045-151">`AllocReadFromByteStream`Функция считывает данные из байтового потока и выделяет новый буфер мультимедиа для хранения данных.</span><span class="sxs-lookup"><span data-stu-id="e7045-151">The `AllocReadFromByteStream` function reads data from a byte stream and allocates a new media buffer to hold the data.</span></span> <span data-ttu-id="e7045-152">Дополнительные сведения см. в разделе [**имфбитестреам:: Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).</span><span class="sxs-lookup"><span data-stu-id="e7045-152">For more information, see [**IMFByteStream::Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).</span></span>


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



<span data-ttu-id="e7045-153">`WriteBufferToByteStream`Функция записывает данные из буфера мультимедиа в байтовый поток.</span><span class="sxs-lookup"><span data-stu-id="e7045-153">The `WriteBufferToByteStream` function writes data from a media buffer to a byte stream.</span></span> <span data-ttu-id="e7045-154">Дополнительные сведения см. в разделе [**имфбитестреам:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span><span class="sxs-lookup"><span data-stu-id="e7045-154">For more information, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span>


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



<span data-ttu-id="e7045-155">`AppendToByteStream`Функция добавляет содержимое одного потока байтов в другой:</span><span class="sxs-lookup"><span data-stu-id="e7045-155">The `AppendToByteStream` function appends the contents of one byte stream to another:</span></span>


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



## <a name="3-open-the-input-asf-file"></a><span data-ttu-id="e7045-156">3. Откройте входной ASF файл.</span><span class="sxs-lookup"><span data-stu-id="e7045-156">3. Open the Input ASF File</span></span>

<span data-ttu-id="e7045-157">Откройте входной файл, вызвав функцию [**мфкреатефиле**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="e7045-157">Open the input file by calling the [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) function.</span></span> <span data-ttu-id="e7045-158">Метод возвращает указатель на объект байтового потока, который содержит содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="e7045-158">The method returns a pointer to the byte stream object that contains the contents of the file.</span></span> <span data-ttu-id="e7045-159">Имя файла задается пользователем с помощью аргументов командной строки приложения.</span><span class="sxs-lookup"><span data-stu-id="e7045-159">The filename is specified by the user through command line arguments of the application.</span></span>

<span data-ttu-id="e7045-160">В следующем примере кода принимается имя файла и возвращается указатель на объект байтового потока, который может быть использован для чтения файла.</span><span class="sxs-lookup"><span data-stu-id="e7045-160">The following example code takes a file name and returns a pointer to a byte stream object that can be used to read the file.</span></span>


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="4-initialize-objects-for-the-input-file"></a><span data-ttu-id="e7045-161">4. Инициализация объектов для входного файла</span><span class="sxs-lookup"><span data-stu-id="e7045-161">4. Initialize Objects for the Input File</span></span>

<span data-ttu-id="e7045-162">Далее предстоит создать и инициализировать исходный объект Контентинфо и разделитель для создания примеров потока.</span><span class="sxs-lookup"><span data-stu-id="e7045-162">Next, you will create and initialize the source ContentInfo object and the splitter for generating stream samples.</span></span>

<span data-ttu-id="e7045-163">Этот исходный поток байтов, созданный на шаге 2, будет использоваться для синтаксического анализа объекта заголовка ASF и заполнения исходного объекта Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="e7045-163">This source byte stream created in step 2 will be used to parse the ASF Header Object and populate the source ContentInfo object.</span></span> <span data-ttu-id="e7045-164">Этот объект будет использоваться для инициализации разделителя, чтобы упростить анализ пакетов данных ASF для звукового потока во входном файле.</span><span class="sxs-lookup"><span data-stu-id="e7045-164">This object will be used to initialize the splitter to facilitate the parsing of the ASF data packets for the audio stream in the input file.</span></span> <span data-ttu-id="e7045-165">Вы также получите длину объекта данных ASF во входном файле и смещение первого пакета данных ASF относительно начала файла.</span><span class="sxs-lookup"><span data-stu-id="e7045-165">You will also retrieve the length of the ASF Data Object in the input file and the offset to the first ASF data packet relative to the start of the file.</span></span> <span data-ttu-id="e7045-166">Эти атрибуты будут использоваться разделителем для создания образцов звуковых потоков.</span><span class="sxs-lookup"><span data-stu-id="e7045-166">These attributes will be used by the splitter to generate audio stream samples.</span></span>

<span data-ttu-id="e7045-167">Чтобы создать и инициализировать компоненты ASF для входного файла, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e7045-167">To create and initialize ASF components for the input file:</span></span>

1.  <span data-ttu-id="e7045-168">Вызовите [**мфкреатеасфконтентинфо**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , чтобы создать объект контентинфо.</span><span class="sxs-lookup"><span data-stu-id="e7045-168">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create the ContentInfo object.</span></span> <span data-ttu-id="e7045-169">Эта функция возвращает указатель на интерфейс [**имфасфконтентинфо**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) .</span><span class="sxs-lookup"><span data-stu-id="e7045-169">This function returns a pointer to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface.</span></span>
2.  <span data-ttu-id="e7045-170">Вызовите [**имфасфконтентинфо::P арсехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) , чтобы проанализировать заголовок ASF.</span><span class="sxs-lookup"><span data-stu-id="e7045-170">Call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) to parse the ASF Header.</span></span> <span data-ttu-id="e7045-171">Дополнительные сведения об этом шаге см. [в разделе чтение объекта заголовка ASF существующего файла](reading-the-asf-header-object-of-an-existing-file.md).</span><span class="sxs-lookup"><span data-stu-id="e7045-171">For more information about this step, see [Reading the ASF Header Object of an Existing File](reading-the-asf-header-object-of-an-existing-file.md).</span></span>
3.  <span data-ttu-id="e7045-172">Вызовите [**мфкреатеасфсплиттер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) , чтобы создать объект разделителя ASF.</span><span class="sxs-lookup"><span data-stu-id="e7045-172">Call [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) to create the ASF splitter object.</span></span> <span data-ttu-id="e7045-173">Эта функция возвращает указатель на интерфейс [**имфасфсплиттер**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="e7045-173">This function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span>
4.  <span data-ttu-id="e7045-174">Вызовите [**имфасфсплиттер:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize), передав указатель [**имфасфконтентинфо**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo).</span><span class="sxs-lookup"><span data-stu-id="e7045-174">Call [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize), passing in the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)pointer.</span></span> <span data-ttu-id="e7045-175">Дополнительные сведения об этом шаге см. [в разделе Создание объекта РАЗДЕЛИТЕЛЯ ASF](creating-the-asf-splitter-object.md).</span><span class="sxs-lookup"><span data-stu-id="e7045-175">For more information about this step, see [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md).</span></span>
5.  <span data-ttu-id="e7045-176">Вызовите [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) , чтобы получить дескриптор представления для ASF-файла.</span><span class="sxs-lookup"><span data-stu-id="e7045-176">Call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) to get a presentation descriptor for the ASF file.</span></span>
6.  <span data-ttu-id="e7045-177">Получите значение атрибута [**\_ \_ \_ \_ \_ смещения начальной загрузки данных MF PD ASF**](mf-pd-asf-data-start-offset-attribute.md) из дескриптора презентации.</span><span class="sxs-lookup"><span data-stu-id="e7045-177">Get the value of the [**MF\_PD\_ASF\_DATA\_START\_OFFSET**](mf-pd-asf-data-start-offset-attribute.md) attribute from the presentation descriptor.</span></span> <span data-ttu-id="e7045-178">Это значение представляет собой расположение объекта данных ASF в файле в виде смещения в байтах от начала файла.</span><span class="sxs-lookup"><span data-stu-id="e7045-178">This value is the location of the ASF Data Object in the file, as a byte offset from the start of the file.</span></span>
7.  <span data-ttu-id="e7045-179">Получите значение атрибута [**\_ \_ \_ \_ длины данных в формате MF PD ASF**](mf-pd-asf-data-length-attribute.md) из дескриптора презентации.</span><span class="sxs-lookup"><span data-stu-id="e7045-179">Get the value of the [**MF\_PD\_ASF\_DATA\_LENGTH**](mf-pd-asf-data-length-attribute.md) attribute from the presentation descriptor.</span></span> <span data-ttu-id="e7045-180">Это значение представляет собой общий размер объекта данных ASF в байтах.</span><span class="sxs-lookup"><span data-stu-id="e7045-180">This value is the total size of the ASF Data Object, in bytes.</span></span> <span data-ttu-id="e7045-181">Дополнительные сведения см. [в разделе Получение сведений из объектов заголовка ASF](getting-information-from-asf-header-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e7045-181">For more information, see [Getting Information from ASF Header Objects](getting-information-from-asf-header-objects.md).</span></span>

<span data-ttu-id="e7045-182">В следующем примере кода показана функция, которая объединяет все шаги.</span><span class="sxs-lookup"><span data-stu-id="e7045-182">The following example code shows a function that consolidates all of the steps.</span></span> <span data-ttu-id="e7045-183">Эта функция принимает указатель на исходный поток байтов и возвращает указатели на исходный объект Контентинфо и разделитель.</span><span class="sxs-lookup"><span data-stu-id="e7045-183">This function takes a pointer to the source byte stream and returns pointers to the source ContentInfo object and the splitter.</span></span> <span data-ttu-id="e7045-184">Кроме того, он получает длину и смещение для объекта данных ASF.</span><span class="sxs-lookup"><span data-stu-id="e7045-184">Also, it receives the length and offsets to the ASF Data Object.</span></span>


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



## <a name="5-create-an-audio-profile"></a><span data-ttu-id="e7045-185">5. Создание профиля аудиоподсистемы</span><span class="sxs-lookup"><span data-stu-id="e7045-185">5. Create an Audio Profile</span></span>

<span data-ttu-id="e7045-186">Далее предстоит создать объект профиля для входного файла, получая его из исходного объекта Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="e7045-186">Next, you will create a profile object for the input file by obtaining it from the source ContentInfo object.</span></span> <span data-ttu-id="e7045-187">Затем вы настроите профиль таким образом, чтобы он содержал только звуковые потоки входного файла.</span><span class="sxs-lookup"><span data-stu-id="e7045-187">You will then configure the profile so that it contains only the audio streams of the input file.</span></span> <span data-ttu-id="e7045-188">Для этого перечислите потоки и удалите из профиля потоки, не являющиеся звуками.</span><span class="sxs-lookup"><span data-stu-id="e7045-188">To do this, enumerate the streams and remove non-audio streams from the profile.</span></span> <span data-ttu-id="e7045-189">Объект профиля аудиоподсистемы будет использоваться далее в этом руководстве для инициализации выходного объекта Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="e7045-189">The audio profile object will be used later in this tutorial to initialize the output ContentInfo object.</span></span>

<span data-ttu-id="e7045-190">Создание профиля аудиоподсистемы</span><span class="sxs-lookup"><span data-stu-id="e7045-190">To create an audio profile</span></span>

1.  <span data-ttu-id="e7045-191">Получите объект профиля для входного файла из исходного объекта Контентинфо, вызвав [**имфасфконтентинфо:: i Profile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="e7045-191">Get the profile object for the input file from the source ContentInfo object by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span> <span data-ttu-id="e7045-192">Метод возвращает указатель на объект Profile, содержащий все потоки во входном файле.</span><span class="sxs-lookup"><span data-stu-id="e7045-192">The method returns a pointer to a profile object that contains all of the streams in the input file.</span></span> <span data-ttu-id="e7045-193">Дополнительные сведения см. [в разделе Создание профиля ASF](creating-an-asf-profile.md).</span><span class="sxs-lookup"><span data-stu-id="e7045-193">For more information see [Creating an ASF Profile](creating-an-asf-profile.md).</span></span>
2.  <span data-ttu-id="e7045-194">Удалите из профиля все взаимоисключающие объекты.</span><span class="sxs-lookup"><span data-stu-id="e7045-194">Remove any mutual exclusion objects from the profile.</span></span> <span data-ttu-id="e7045-195">Этот шаг необходим, так как потоки, не являющиеся звуками, будут удалены из профиля, что может сделать недействительными взаимоисключающие объекты.</span><span class="sxs-lookup"><span data-stu-id="e7045-195">This step is required because non-audio streams will be removed from the profile, which could invalidate the mutual exclusion objects.</span></span>
3.  <span data-ttu-id="e7045-196">Удалите все незвуковые потоки из профиля следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e7045-196">Remove all non-audio streams from the profile, as follows:</span></span>
    -   <span data-ttu-id="e7045-197">Вызовите метод [**имфасфпрофиле:: жетстреамкаунт**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) , чтобы получить количество потоков.</span><span class="sxs-lookup"><span data-stu-id="e7045-197">Call [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) to get the number of streams.</span></span>
    -   <span data-ttu-id="e7045-198">В цикле вызовите [**имфасфпрофиле::-Stream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) , чтобы получить каждый поток по индексу.</span><span class="sxs-lookup"><span data-stu-id="e7045-198">In a loop, call [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) to get each stream by index.</span></span>
    -   <span data-ttu-id="e7045-199">Вызовите метод [**имфасфстреамконфиг:: жетстреамтипе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) , чтобы получить тип потока.</span><span class="sxs-lookup"><span data-stu-id="e7045-199">Call [**IMFASFStreamConfig::GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) to get the stream type.</span></span>
    -   <span data-ttu-id="e7045-200">Для незвуковых потоков вызовите метод [**имфасфпрофиле:: ремовестреам**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) , чтобы удалить поток.</span><span class="sxs-lookup"><span data-stu-id="e7045-200">For non-audio streams, call [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) to remove the stream.</span></span>
4.  <span data-ttu-id="e7045-201">Сохранить номер потока первого звукового потока.</span><span class="sxs-lookup"><span data-stu-id="e7045-201">Store the stream number of the first audio stream.</span></span> <span data-ttu-id="e7045-202">Он будет выбран в разделителе для создания примеров потока.</span><span class="sxs-lookup"><span data-stu-id="e7045-202">This will be selected on the splitter to generate stream samples.</span></span> <span data-ttu-id="e7045-203">Если номер потока равен нулю, вызывающий объект может предположить, что отсутствует файл звуковых потоков.</span><span class="sxs-lookup"><span data-stu-id="e7045-203">If the stream number is zero, the caller can assume that there were no audio streams file.</span></span>

<span data-ttu-id="e7045-204">Эти действия выполняются в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="e7045-204">The following code these steps:</span></span>


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



<span data-ttu-id="e7045-205">`RemoveMutexes`Функция удаляет все взаимоисключающие объекты из профиля:</span><span class="sxs-lookup"><span data-stu-id="e7045-205">The `RemoveMutexes` function removes any mutual exclusion objects from the profile:</span></span>


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



## <a name="6-initialize-objects-for-the-output-file"></a><span data-ttu-id="e7045-206">6. Инициализация объектов для выходного файла</span><span class="sxs-lookup"><span data-stu-id="e7045-206">6. Initialize Objects for the Output File</span></span>

<span data-ttu-id="e7045-207">Далее предстоит создать выходной объект Контентинфо и мультиплексор для создания пакетов данных для выходного файла.</span><span class="sxs-lookup"><span data-stu-id="e7045-207">Next, you will create the output ContentInfo object and the multiplexer for generating data packets for the output file.</span></span>

<span data-ttu-id="e7045-208">Звуковой профиль, созданный на шаге 4, будет использоваться для заполнения выходного объекта Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="e7045-208">The audio profile created in step 4 will be used to populate the output ContentInfo object.</span></span> <span data-ttu-id="e7045-209">Этот объект содержит такие сведения, как глобальные атрибуты файлов и свойства потока.</span><span class="sxs-lookup"><span data-stu-id="e7045-209">This object contains information such as global file attributes and stream properties.</span></span> <span data-ttu-id="e7045-210">Выходной объект Контентинфо будет использоваться для инициализации мультиплексора, который будет формировать пакеты данных для выходного файла.</span><span class="sxs-lookup"><span data-stu-id="e7045-210">The output ContentInfo object will be used to initialize the multiplexer that will generate data packets for the output file.</span></span> <span data-ttu-id="e7045-211">После создания пакетов данных необходимо обновить объект Контентинфо, чтобы отразить новые значения.</span><span class="sxs-lookup"><span data-stu-id="e7045-211">After the data packets are generated, the ContentInfo object must be updated to reflect the new values.</span></span>

<span data-ttu-id="e7045-212">Создание и инициализация компонентов ASF для выходного файла</span><span class="sxs-lookup"><span data-stu-id="e7045-212">To create and initialize ASF components for the output file</span></span>

1.  <span data-ttu-id="e7045-213">Создайте пустой объект Контентинфо, вызвав [**мфкреатеасфконтентинфо**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , и заполните его данными из аудио профиля, созданного на шаге 3, вызвав [**Имфасфконтентинфо:: сетпрофиле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span><span class="sxs-lookup"><span data-stu-id="e7045-213">Create an empty ContentInfo object by calling [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) and populate it with information from the audio profile created in step 3 by calling [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span></span> <span data-ttu-id="e7045-214">Дополнительные сведения см. [в разделе Инициализация объекта Контентинфо нового ASF-файла](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="e7045-214">For more information, see [Initializing the ContentInfo Object of a New ASF File](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span></span>
2.  <span data-ttu-id="e7045-215">Создайте и инициализируйте объект мультиплексора с помощью выходного объекта Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="e7045-215">Create and initialize the multiplexer object by using the output ContentInfo object.</span></span> <span data-ttu-id="e7045-216">Дополнительные сведения см. [в разделе Создание объекта мультиплексора](creating-the-multiplexer-object.md).</span><span class="sxs-lookup"><span data-stu-id="e7045-216">For more information, see [Creating the Multiplexer Object](creating-the-multiplexer-object.md).</span></span>

<span data-ttu-id="e7045-217">В следующем примере кода показана функция, которая объединяет шаги.</span><span class="sxs-lookup"><span data-stu-id="e7045-217">The following example code shows a function that consolidates the steps.</span></span> <span data-ttu-id="e7045-218">Эта функция принимает указатель на объект Profile и возвращает указатели на выходной объект Контентинфо и мультиплексор.</span><span class="sxs-lookup"><span data-stu-id="e7045-218">This function takes a pointer to a profile object and returns pointers to the output ContentInfo object and the multiplexer.</span></span>


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



## <a name="7-generate-new-asf-data-packets"></a><span data-ttu-id="e7045-219">7. Генерация новых пакетов данных ASF</span><span class="sxs-lookup"><span data-stu-id="e7045-219">7. Generate New ASF Data Packets</span></span>

<span data-ttu-id="e7045-220">Далее предстоит создать образцы звуковых потоков из исходного потока байтов с помощью разделителя и отправить их мультиплексору для создания пакетов данных ASF.</span><span class="sxs-lookup"><span data-stu-id="e7045-220">Next, you will generate audio stream samples from the source byte stream by using the splitter and send them to the multiplexer to create ASF data packets.</span></span> <span data-ttu-id="e7045-221">Эти пакеты данных будут составлять окончательный объект данных ASF для нового файла.</span><span class="sxs-lookup"><span data-stu-id="e7045-221">These data packets will constitute the final ASF Data Object for the new file.</span></span>

<span data-ttu-id="e7045-222">Создание образцов аудиопотока</span><span class="sxs-lookup"><span data-stu-id="e7045-222">To generate audio stream samples</span></span>

1.  <span data-ttu-id="e7045-223">Выберите первый аудиопоток в разделителе, вызвав [**имфасфсплиттер:: селектстреамс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams).</span><span class="sxs-lookup"><span data-stu-id="e7045-223">Select the first audio stream on the splitter by calling [**IMFASFSplitter::SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams).</span></span>
2.  <span data-ttu-id="e7045-224">Чтение блоков фиксированного размера данных мультимедиа из исходного потока байтов в буфер мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e7045-224">Read fixed-size blocks of media data from the source byte stream into a media buffer.</span></span>
3.  <span data-ttu-id="e7045-225">Собирайте примеры потоков как образцы мультимедиа из разделителя, вызывая [**имфасфсплиттер:: жетнекстсампле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) в цикле, если он получает \_ флаг ASF статусфлагс \_ неполный в параметре *пдвстатусфлагс* .</span><span class="sxs-lookup"><span data-stu-id="e7045-225">Collect the stream samples as media samples from the splitter by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in a loop as long as it receives the ASF\_STATUSFLAGS\_INCOMPLETE flag in the *pdwStatusFlags* parameter.</span></span> <span data-ttu-id="e7045-226">Дополнительные сведения см. в разделе Создание образцов для пакетов данных ASF статьи [Создание примеров потоков из существующего объекта данных ASF](generating-stream-samples-from-an-existing-asf-data-object.md).</span><span class="sxs-lookup"><span data-stu-id="e7045-226">For more information, see Generating Samples for ASF Data Packets" in [Generating Stream Samples from an Existing ASF Data Object](generating-stream-samples-from-an-existing-asf-data-object.md).</span></span>
4.  <span data-ttu-id="e7045-227">Для каждого примера носителя вызовите [**имфасфмултиплексер::P роцесссампле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) , чтобы отправить пример мультимедиа в мультиплексор.</span><span class="sxs-lookup"><span data-stu-id="e7045-227">For each media sample, call [**IMFASFMultiplexer::ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) to send the media sample to the multiplexer.</span></span> <span data-ttu-id="e7045-228">Мультиплексор создает пакеты данных для объекта данных ASF.</span><span class="sxs-lookup"><span data-stu-id="e7045-228">The multiplexer generates the data packets for the ASF Data Object.</span></span>
5.  <span data-ttu-id="e7045-229">Запишите пакет данных, созданный мультиплексором, в поток байтов данных.</span><span class="sxs-lookup"><span data-stu-id="e7045-229">Write the data packet generated by the multiplexer to the data byte stream.</span></span>
6.  <span data-ttu-id="e7045-230">После создания всех пакетов данных вызовите метод [**имфасфмултиплексер:: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) , чтобы обновить выходной объект контентинфо со сведениями, собранными во время создания пакета данных ASF.</span><span class="sxs-lookup"><span data-stu-id="e7045-230">After all the data packets have been generated, call [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) to update the output ContentInfo object with information collected during ASF data packet generation.</span></span>

<span data-ttu-id="e7045-231">В следующем примере кода создаются образцы Stream из разделителя ASF и они отправляются в мультиплексор.</span><span class="sxs-lookup"><span data-stu-id="e7045-231">The following example code generates stream samples from the ASF splitter and sends them to the multiplexer.</span></span> <span data-ttu-id="e7045-232">Мультиплексор создает пакеты данных ASF и записывает их в поток.</span><span class="sxs-lookup"><span data-stu-id="e7045-232">The multiplexer generates ASF data packets and writes it to a stream.</span></span>


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



<span data-ttu-id="e7045-233">Чтобы получить пакеты из разделителя ASF, предыдущий код вызывает `GetPacketsFromSplitter` функцию, показанную ниже:</span><span class="sxs-lookup"><span data-stu-id="e7045-233">To get packets from the ASF splitter, the previous code calls the `GetPacketsFromSplitter` function, shown here:</span></span>


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



<span data-ttu-id="e7045-234">`GenerateDataPackets`Функция получает пакеты данных от мультиплексора.</span><span class="sxs-lookup"><span data-stu-id="e7045-234">The `GenerateDataPackets` function gets data packets from multiplexer.</span></span> <span data-ttu-id="e7045-235">Дополнительные сведения см. в разделе [Получение пакетов данных ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="e7045-235">For more information, see [Getting ASF Data Packets](generating-new-asf-data-packets.md).</span></span>


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



## <a name="8-write-the-asf-objects-in-the-new-file"></a><span data-ttu-id="e7045-236">8. запись объектов ASF в новый файл</span><span class="sxs-lookup"><span data-stu-id="e7045-236">8. Write the ASF Objects in the New File</span></span>

<span data-ttu-id="e7045-237">Далее предстоит записать содержимое выходного объекта Контентинфо в буфер мультимедиа, вызвав [**имфасфконтентинфо:: женератехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span><span class="sxs-lookup"><span data-stu-id="e7045-237">Next, you will write the contents of the output ContentInfo object to a media buffer by calling [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="e7045-238">Этот метод преобразует данные, хранящиеся в объекте Контентинфо, в двоичные данные в формате файла заголовка ASF.</span><span class="sxs-lookup"><span data-stu-id="e7045-238">This method converts data stored in the ContentInfo object into binary data in ASF Header Object format.</span></span> <span data-ttu-id="e7045-239">Дополнительные сведения см. [в разделе Создание нового объекта заголовка ASF](generating-a-new-asf-header-object.md).</span><span class="sxs-lookup"><span data-stu-id="e7045-239">For more information, see [Generating a New ASF Header Object](generating-a-new-asf-header-object.md).</span></span>

<span data-ttu-id="e7045-240">После создания нового объекта заголовка ASF запишите выходной файл, сначала записав объект заголовка в выходной поток байтов, созданный на шаге 2, вызвав вспомогательную функцию Вритебуффертобитестреам.</span><span class="sxs-lookup"><span data-stu-id="e7045-240">After the new ASF Header Object has been generated, write the output file by first writing the Header Object to the output byte stream created in step 2 by calling the helper function WriteBufferToByteStream.</span></span> <span data-ttu-id="e7045-241">Используйте объект заголовка с объектом данных, содержащимся в потоке байтов данных.</span><span class="sxs-lookup"><span data-stu-id="e7045-241">Follow the Header Object with the Data Object contained in the data byte stream.</span></span> <span data-ttu-id="e7045-242">В примере кода показана функция, которая передает содержимое потока байтов данных в выходной поток байтов.</span><span class="sxs-lookup"><span data-stu-id="e7045-242">The example code shows a function that transfers contents of the data bytes stream to the output byte stream.</span></span>


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



## <a name="9-write-the-entry-point-function"></a><span data-ttu-id="e7045-243">9. Написание функции Entry-Point</span><span class="sxs-lookup"><span data-stu-id="e7045-243">9 Write the Entry-Point Function</span></span>

<span data-ttu-id="e7045-244">Теперь можно объединить предыдущие шаги в законченное приложение.</span><span class="sxs-lookup"><span data-stu-id="e7045-244">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="e7045-245">Перед использованием любого объекта Media Foundation инициализируйте Media Foundationную платформу, вызвав [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="e7045-245">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="e7045-246">По завершении вызовите [**мфшутдовн**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="e7045-246">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="e7045-247">Дополнительные сведения см. в разделе [инициализация Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="e7045-247">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>

<span data-ttu-id="e7045-248">В следующем коде показано полное консольное приложение.</span><span class="sxs-lookup"><span data-stu-id="e7045-248">The following code shows the complete console application.</span></span> <span data-ttu-id="e7045-249">Аргумент командной строки задает имя файла для преобразования и имя нового звукового файла.</span><span class="sxs-lookup"><span data-stu-id="e7045-249">The command-line argument specifies the name of the file to convert and the name of the new audio file.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e7045-250">См. также</span><span class="sxs-lookup"><span data-stu-id="e7045-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7045-251">Компоненты ASF Вмконтаинер</span><span class="sxs-lookup"><span data-stu-id="e7045-251">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="e7045-252">Поддержка ASF в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e7045-252">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



