---
description: В этом руководстве показано, как получить пакеты данных из ASF-файла с помощью разделителя ASF.
ms.assetid: e3a55275-e8f0-4ab7-98db-a2f2c54d5a51
title: Руководство. чтение файла ASF с помощью объектов Вмконтаинер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0225f434f650f0423771122e6fc345022e69ec1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692778"
---
# <a name="tutorial-reading-an-asf-file-by-using-wmcontainer-objects"></a><span data-ttu-id="ddb10-103">Руководство. чтение файла ASF с помощью объектов Вмконтаинер</span><span class="sxs-lookup"><span data-stu-id="ddb10-103">Tutorial: Reading an ASF File by Using WMContainer Objects</span></span>

<span data-ttu-id="ddb10-104">В этом руководстве показано, как получить пакеты данных из ASF-файла с помощью [разделителя ASF](asf-splitter.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-104">This tutorial shows how to get data packets from an Advanced Systems Format (ASF) file using the [ASF Splitter](asf-splitter.md).</span></span> <span data-ttu-id="ddb10-105">В этом руководстве вы создадите простое консольное приложение, которое считывает файл ASF и создает сжатые образцы мультимедиа для первого видеопотока в файле.</span><span class="sxs-lookup"><span data-stu-id="ddb10-105">In this tutorial, you will create a simple console application that reads an ASF file and generates compressed media samples for the first video stream in the file.</span></span> <span data-ttu-id="ddb10-106">Приложение отображает сведения о ключевых кадрах в потоке видео.</span><span class="sxs-lookup"><span data-stu-id="ddb10-106">The application displays information about the key frames in the video stream.</span></span>

<span data-ttu-id="ddb10-107">Этот учебник содержит следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ddb10-107">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="ddb10-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="ddb10-108">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="ddb10-109">1. Настройка проекта</span><span class="sxs-lookup"><span data-stu-id="ddb10-109">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="ddb10-110">2. Открытие файла ASF</span><span class="sxs-lookup"><span data-stu-id="ddb10-110">2. Open an ASF File</span></span>](#2-open-an-asf-file)
-   [<span data-ttu-id="ddb10-111">3. чтение объекта заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="ddb10-111">3. Read the ASF Header Object</span></span>](#3-read-the-asf-header-object)
-   [<span data-ttu-id="ddb10-112">4. Создание разделителя ASF</span><span class="sxs-lookup"><span data-stu-id="ddb10-112">4. Create the ASF Splitter</span></span>](#4-create-the-asf-splitter)
-   [<span data-ttu-id="ddb10-113">5. Выбор потока для синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="ddb10-113">5. Select a Stream for Parsing</span></span>](#5-select-a-stream-for-parsing)
-   [<span data-ttu-id="ddb10-114">6. Создание сжатых образцов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="ddb10-114">6. Generate Compressed Media Samples</span></span>](#6-generate-compressed-media-samples)
-   [<span data-ttu-id="ddb10-115">7. Написание функции Entry-Point</span><span class="sxs-lookup"><span data-stu-id="ddb10-115">7. Write the Entry-Point Function</span></span>](#7-write-the-entry-point-function)
-   [<span data-ttu-id="ddb10-116">Список программ</span><span class="sxs-lookup"><span data-stu-id="ddb10-116">Program Listing</span></span>](#program-listing)
-   [<span data-ttu-id="ddb10-117">См. также</span><span class="sxs-lookup"><span data-stu-id="ddb10-117">Related topics</span></span>](#related-topics)

<span data-ttu-id="ddb10-118">В этом учебнике не рассматривается декодирование сжатых данных, которые приложение получает из разделителя ASF.</span><span class="sxs-lookup"><span data-stu-id="ddb10-118">The tutorial does not cover how to decode the compressed data that the application gets from the ASF splitter.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ddb10-119">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="ddb10-119">Prerequisites</span></span>

<span data-ttu-id="ddb10-120">В этом учебнике предполагается следующее:</span><span class="sxs-lookup"><span data-stu-id="ddb10-120">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="ddb10-121">Вы знакомы со структурой файла ASF и компонентами, предоставляемыми Media Foundation для работы с объектами ASF.</span><span class="sxs-lookup"><span data-stu-id="ddb10-121">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="ddb10-122">К этим компонентам относятся объект Контентинфо, разделитель, мультиплексор и профиль.</span><span class="sxs-lookup"><span data-stu-id="ddb10-122">These components include the ContentInfo object, splitter, multiplexer, and profile.</span></span> <span data-ttu-id="ddb10-123">Дополнительные сведения см. в разделе [компоненты ASF вмконтаинер](wmcontainer-asf-components.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-123">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="ddb10-124">Вы знакомы с [буферами мультимедиа](media-buffers.md) и потоками байтов: в частности, операции с файлами с использованием потока байтов, чтение из потока байтов в буфер мультимедиа и запись содержимого буфера мультимедиа в байтовый поток.</span><span class="sxs-lookup"><span data-stu-id="ddb10-124">You are familiar with [Media Buffers](media-buffers.md) and byte streams: Specifically, file operations using a byte stream, reading from a byte stream into a media buffer, and writing the contents of a media buffer to a byte stream.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="ddb10-125">1. Настройка проекта</span><span class="sxs-lookup"><span data-stu-id="ddb10-125">1. Set up the Project</span></span>

<span data-ttu-id="ddb10-126">Включите в исходный файл следующие заголовки:</span><span class="sxs-lookup"><span data-stu-id="ddb10-126">Include the following headers in your source file:</span></span>


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <Mferror.h>
```



<span data-ttu-id="ddb10-127">Ссылка на следующие файлы библиотеки:</span><span class="sxs-lookup"><span data-stu-id="ddb10-127">Link to the following library files:</span></span>

-   <span data-ttu-id="ddb10-128">мфплат. lib</span><span class="sxs-lookup"><span data-stu-id="ddb10-128">mfplat.lib</span></span>
-   <span data-ttu-id="ddb10-129">MF. lib</span><span class="sxs-lookup"><span data-stu-id="ddb10-129">mf.lib</span></span>
-   <span data-ttu-id="ddb10-130">мфууид. lib</span><span class="sxs-lookup"><span data-stu-id="ddb10-130">mfuuid.lib</span></span>

<span data-ttu-id="ddb10-131">Объявите функцию [саферелеасе](saferelease.md) :</span><span class="sxs-lookup"><span data-stu-id="ddb10-131">Declare the [SafeRelease](saferelease.md) function:</span></span>


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



## <a name="2-open-an-asf-file"></a><span data-ttu-id="ddb10-132">2. Открытие файла ASF</span><span class="sxs-lookup"><span data-stu-id="ddb10-132">2. Open an ASF File</span></span>

<span data-ttu-id="ddb10-133">Затем откройте указанный файл, вызвав функцию [**мфкреатефиле**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="ddb10-133">Next, open the specified file by calling the [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) function.</span></span> <span data-ttu-id="ddb10-134">Метод возвращает указатель на объект байтового потока, который содержит содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="ddb10-134">The method returns a pointer to the byte stream object that contains the contents of the file.</span></span> <span data-ttu-id="ddb10-135">Имя файла задается пользователем с помощью аргументов командной строки приложения.</span><span class="sxs-lookup"><span data-stu-id="ddb10-135">The filename is specified by the user through command line arguments of the application.</span></span>

<span data-ttu-id="ddb10-136">В следующем примере кода принимается имя файла и возвращается указатель на объект байтового потока, который может быть использован для чтения файла.</span><span class="sxs-lookup"><span data-stu-id="ddb10-136">The following example code takes a file name and returns a pointer to a byte stream object that can be used to read the file.</span></span>


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="3-read-the-asf-header-object"></a><span data-ttu-id="ddb10-137">3. чтение объекта заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="ddb10-137">3. Read the ASF Header Object</span></span>

<span data-ttu-id="ddb10-138">Затем создайте [объект ASF контентинфо](asf-contentinfo-object.md) и используйте его для синтаксического анализа объекта заголовка ASF указанного файла.</span><span class="sxs-lookup"><span data-stu-id="ddb10-138">Next, create the [ASF ContentInfo Object](asf-contentinfo-object.md) and use it to parse the ASF Header Object of the specified file.</span></span> <span data-ttu-id="ddb10-139">Объект Контентинфо хранит сведения из заголовка ASF, включая глобальные атрибуты файлов и сведения о каждом потоке.</span><span class="sxs-lookup"><span data-stu-id="ddb10-139">The ContentInfo object stores information from the ASF header, including global file attributes and information about each stream.</span></span> <span data-ttu-id="ddb10-140">Вы будете использовать объект Контентинфо далее в этом руководстве, чтобы инициализировать разделитель ASF и получить номер потока видеопотока.</span><span class="sxs-lookup"><span data-stu-id="ddb10-140">You will use the ContentInfo object later in the tutorial to initialize the ASF splitter and get the stream number of the video stream.</span></span>

<span data-ttu-id="ddb10-141">Чтобы создать объект ASF Контентинфо, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="ddb10-141">To create the ASF ContentInfo object:</span></span>

1.  <span data-ttu-id="ddb10-142">Вызовите функцию [**мфкреатеасфконтентинфо**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , чтобы создать объект контентинфо.</span><span class="sxs-lookup"><span data-stu-id="ddb10-142">Call the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function to create a ContentInfo object.</span></span> <span data-ttu-id="ddb10-143">Метод возвращает указатель на интерфейс [**имфасфконтентинфо**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) .</span><span class="sxs-lookup"><span data-stu-id="ddb10-143">The method returns a pointer to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface.</span></span>
2.  <span data-ttu-id="ddb10-144">Считывает первые 30 байт данных из ASF-файла в буфер мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ddb10-144">Read the first 30 bytes of data from the ASF file into a media buffer.</span></span>
3.  <span data-ttu-id="ddb10-145">Передайте буфер мультимедиа в метод [**имфасфконтентинфо:: жесеадерсизе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) .</span><span class="sxs-lookup"><span data-stu-id="ddb10-145">Pass the media buffer to the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="ddb10-146">Этот метод возвращает общий размер объекта заголовка в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="ddb10-146">This method returns the total size of the Header Object in the ASF file.</span></span>
4.  <span data-ttu-id="ddb10-147">Передайте тот же буфер мультимедиа в метод [**имфасфконтентинфо::P арсехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="ddb10-147">Pass the same media buffer to the [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span>
5.  <span data-ttu-id="ddb10-148">Прочтите оставшуюся часть объекта Header в новый буфер мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ddb10-148">Read the remainder of the Header Object into a new media buffer.</span></span>
6.  <span data-ttu-id="ddb10-149">Передайте второй буфер в метод [**парсехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="ddb10-149">Pass the second buffer to the [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span> <span data-ttu-id="ddb10-150">Укажите 30-байтовое смещение в параметре *кбоффсетвисинхеадер* параметра **парсехеадер**.</span><span class="sxs-lookup"><span data-stu-id="ddb10-150">Specify the 30-byte offset in the *cbOffsetWithinHeader* parameter of **ParseHeader**.</span></span> <span data-ttu-id="ddb10-151">Метод **парсехеадер** Инициализирует объект контентинфо со сведениями, собранными из различных объектов ASF, содержащихся в объекте Header.</span><span class="sxs-lookup"><span data-stu-id="ddb10-151">The **ParseHeader** method initializes the ContentInfo object with information gathered from the various ASF objects contained in the Header Object.</span></span>


```C++
// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 
```



<span data-ttu-id="ddb10-152">Эта функция использует `ReadFromByteStream` функцию для чтения из байтового потока в буфер мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="ddb10-152">This function uses the `ReadFromByteStream` function to read from a byte stream into a media buffer:</span></span>


```C++
// Read data from a byte stream into a media buffer.
//
// This function reads a maximum of cbMax bytes, or up to the size size of the 
// buffer, whichever is smaller. If the end of the byte stream is reached, the 
// actual amount of data read might be less than either of these values.
//
// To find out how much data was read, call IMFMediaBuffer::GetCurrentLength.

HRESULT ReadFromByteStream(
    IMFByteStream *pStream,     // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,    // Pointer to the media buffer.
    DWORD cbMax                 // Maximum amount to read.
    )
{
    DWORD cbBufferMax = 0;
    DWORD cbRead = 0;
    BYTE *pData= NULL;

    HRESULT hr = pBuffer->Lock(&pData, &cbBufferMax, NULL);

    // Do not exceed the maximum size of the buffer.
    if (SUCCEEDED(hr))
    {
        if (cbMax > cbBufferMax)
        {
            cbMax = cbBufferMax;
        }

        // Read up to cbMax bytes.
        hr = pStream->Read(pData, cbMax, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }
    if (pData)
    {
        pBuffer->Unlock();
    }
    return hr;
}
```



## <a name="4-create-the-asf-splitter"></a><span data-ttu-id="ddb10-153">4. Создание разделителя ASF</span><span class="sxs-lookup"><span data-stu-id="ddb10-153">4. Create the ASF Splitter</span></span>

<span data-ttu-id="ddb10-154">Затем создайте объект [разделителя ASF](asf-splitter.md) .</span><span class="sxs-lookup"><span data-stu-id="ddb10-154">Next, create the [ASF Splitter](asf-splitter.md) object.</span></span> <span data-ttu-id="ddb10-155">Разделитель ASF будет использоваться для синтаксического анализа объекта данных ASF, который содержит пакетные данные мультимедиа для файла ASF.</span><span class="sxs-lookup"><span data-stu-id="ddb10-155">You will use the ASF splitter to parse the ASF Data Object, which contains packetized media data for the ASF file.</span></span>

<span data-ttu-id="ddb10-156">Чтобы создать объект разделителя для ASF-файла, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ddb10-156">To create a splitter object for the ASF File:</span></span>

1.  <span data-ttu-id="ddb10-157">Вызовите функцию [**мфкреатеасфсплиттер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) , чтобы создать разделитель ASF.</span><span class="sxs-lookup"><span data-stu-id="ddb10-157">Call the [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) function to create the ASF splitter.</span></span> <span data-ttu-id="ddb10-158">Функция возвращает указатель на интерфейс [**имфасфсплиттер**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="ddb10-158">The function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span>
2.  <span data-ttu-id="ddb10-159">Вызовите метод [**имфасфсплиттер:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) , чтобы инициализировать разделитель ASF.</span><span class="sxs-lookup"><span data-stu-id="ddb10-159">Call [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) to initialize the ASF splitter.</span></span> <span data-ttu-id="ddb10-160">Этот метод принимает указатель на объект Контентинфо, созданный в процедуре 3.</span><span class="sxs-lookup"><span data-stu-id="ddb10-160">This method takes a pointer to the ContentInfo object, which was created in procedure 3.</span></span>


```C++
// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}
```



## <a name="5-select-a-stream-for-parsing"></a><span data-ttu-id="ddb10-161">5. Выбор потока для синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="ddb10-161">5. Select a Stream for Parsing</span></span>

<span data-ttu-id="ddb10-162">Затем перечислите потоки в файле ASF и выберите первый поток видео для синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="ddb10-162">Next, enumerate the streams in the ASF file and select the first video stream for parsing.</span></span> <span data-ttu-id="ddb10-163">Для перечисления потоков используется объект профиля ASF и выполняется поиск потоков с типом видео.</span><span class="sxs-lookup"><span data-stu-id="ddb10-163">To enumerate the streams, you will use an ASF profile object and search for streams that have a video media type.</span></span>

<span data-ttu-id="ddb10-164">Чтобы выбрать поток видео, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="ddb10-164">To select the video stream:</span></span>

1.  <span data-ttu-id="ddb10-165">Вызовите [**имфасфконтентинфо:: onprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile) в объекте контентинфо, чтобы создать профиль ASF.</span><span class="sxs-lookup"><span data-stu-id="ddb10-165">Call [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile) on the ContentInfo object to create an ASF profile.</span></span> <span data-ttu-id="ddb10-166">Помимо прочих сведений, профиль описывает потоки в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="ddb10-166">Among other information, the profile describes the streams in the ASF file.</span></span>
2.  <span data-ttu-id="ddb10-167">Вызовите метод [**имфасфпрофиле:: жетстреамкаунт**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) , чтобы получить количество потоков в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="ddb10-167">Call [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) to get the number of streams in the ASF file.</span></span>
3.  <span data-ttu-id="ddb10-168">Вызовите метод [**имфасфпрофиле::-Stream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) в цикле для перечисления потоков.</span><span class="sxs-lookup"><span data-stu-id="ddb10-168">Call [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) in a loop to enumerate the streams.</span></span> <span data-ttu-id="ddb10-169">Метод возвращает указатель на интерфейс [**имфасфстреамконфиг**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="ddb10-169">The method returns a pointer to the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span> <span data-ttu-id="ddb10-170">Он также возвращает идентификатор потока.</span><span class="sxs-lookup"><span data-stu-id="ddb10-170">It also returns the stream identifier.</span></span>
4.  <span data-ttu-id="ddb10-171">Вызовите метод [**имфасфстреамконфиг:: жетстреамтипе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) , чтобы получить идентификатор GUID основного типа для потока.</span><span class="sxs-lookup"><span data-stu-id="ddb10-171">Call [**IMFASFStreamConfig::GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) to get the major type GUID for the stream.</span></span> <span data-ttu-id="ddb10-172">Если основным типом GUID является Мфмедиатипе \_ Video, поток содержит видео.</span><span class="sxs-lookup"><span data-stu-id="ddb10-172">If the major type GUID is MFMediaType\_Video, the stream contains video.</span></span>
5.  <span data-ttu-id="ddb10-173">Если в шаге 4 был найден поток видео, вызовите метод [**имфасфсплиттер:: селектстреамс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) , чтобы выбрать поток.</span><span class="sxs-lookup"><span data-stu-id="ddb10-173">If you found a video stream in step 4, call [**IMFASFSplitter::SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) to select the stream.</span></span> <span data-ttu-id="ddb10-174">Этот метод принимает массив идентификаторов потоков.</span><span class="sxs-lookup"><span data-stu-id="ddb10-174">This method takes an array of stream identifiers.</span></span> <span data-ttu-id="ddb10-175">В этом руководстве размер массива равен 1, так как приложение будет анализировать один поток.</span><span class="sxs-lookup"><span data-stu-id="ddb10-175">For this tutorial, the array size is 1 because the application will parse a single stream.</span></span>

<span data-ttu-id="ddb10-176">В следующем примере кода выполняется перечисление потоков в файле ASF и выбирается первый поток видео на разделителе ASF:</span><span class="sxs-lookup"><span data-stu-id="ddb10-176">The following example code enumerates the streams in the ASF file and selects the first video stream on the ASF splitter:</span></span>


```C++
// Select the first video stream for parsing with the ASF splitter.

HRESULT SelectVideoStream(IMFASFContentInfo *pContentInfo, 
    IMFASFSplitter *pSplitter, BOOL *pbHasVideo)
{
    DWORD   cStreams = 0;
    WORD    wStreamID = 0;

    IMFASFProfile *pProfile = NULL;
    IMFASFStreamConfig *pStream = NULL;

    // Get the ASF profile from the ContentInfo object.
    HRESULT hr = pContentInfo->GetProfile(&pProfile);

    // Loop through all of the streams in the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&cStreams);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            GUID    streamType = GUID_NULL;

            // Get the stream type and stream identifier.
            hr = pProfile->GetStream(i, &wStreamID, &pStream);
            if (FAILED(hr)) 
            {
                break;
            }

            hr = pStream->GetStreamType(&streamType);
            if (FAILED(hr)) 
            {
                break;
            }

            if (streamType == MFMediaType_Video)
            {
                *pbHasVideo = TRUE;
                break;
            }
            SafeRelease(&pStream);
        }
    }

    // Select the video stream, if found.
    if (SUCCEEDED(hr))
    {
        if (*pbHasVideo)
        {
            // SelectStreams takes an array of stream identifiers.
            hr = pSplitter->SelectStreams(&wStreamID, 1);
        }
    }
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    return hr;
}
```



## <a name="6-generate-compressed-media-samples"></a><span data-ttu-id="ddb10-177">6. Создание сжатых образцов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="ddb10-177">6. Generate Compressed Media Samples</span></span>

<span data-ttu-id="ddb10-178">Затем используйте разделитель ASF для анализа объекта данных ASF и получения пакетов данных для выбранного видеопотока.</span><span class="sxs-lookup"><span data-stu-id="ddb10-178">Next, use the ASF splitter to parse the ASF Data Object and get the data packets for the selected video stream.</span></span> <span data-ttu-id="ddb10-179">Приложение считывает данные из ASF-файла в блоках фиксированного размера и передает их в разделитель ASF.</span><span class="sxs-lookup"><span data-stu-id="ddb10-179">The application reads data from the ASF file in fixed-size blocks and passes the data to the ASF splitter.</span></span> <span data-ttu-id="ddb10-180">Разделитель анализирует данные и создает [примеры носителей](media-samples.md) , содержащие сжатые данные видео.</span><span class="sxs-lookup"><span data-stu-id="ddb10-180">The splitter parses the data and generates [Media Samples](media-samples.md) that contain the compressed video data.</span></span> <span data-ttu-id="ddb10-181">Приложение проверяет, представляет ли каждый пример ключевой кадр.</span><span class="sxs-lookup"><span data-stu-id="ddb10-181">The application checks whether each sample represents a key frame.</span></span> <span data-ttu-id="ddb10-182">Если это так, в приложении отображаются некоторые основные сведения о примере:</span><span class="sxs-lookup"><span data-stu-id="ddb10-182">If so, the application displays some basic information about the sample:</span></span>

-   <span data-ttu-id="ddb10-183">Число буферов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="ddb10-183">Number of media buffers</span></span>
-   <span data-ttu-id="ddb10-184">Общий размер данных</span><span class="sxs-lookup"><span data-stu-id="ddb10-184">Total size of the data</span></span>
-   <span data-ttu-id="ddb10-185">Метка времени</span><span class="sxs-lookup"><span data-stu-id="ddb10-185">Time stamp</span></span>

<span data-ttu-id="ddb10-186">Для создания сжатых образцов мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="ddb10-186">To generate compressed media samples:</span></span>

1.  <span data-ttu-id="ddb10-187">Выделение нового буфера мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ddb10-187">Allocate a new media buffer.</span></span>
2.  <span data-ttu-id="ddb10-188">Считывает данные из байтового потока в буфер мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ddb10-188">Read data from the byte stream into the media buffer.</span></span>
3.  <span data-ttu-id="ddb10-189">Передайте буфер мультимедиа в метод [**имфасфсплиттер::P арседата**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) .</span><span class="sxs-lookup"><span data-stu-id="ddb10-189">Pass the media buffer to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="ddb10-190">Метод анализирует данные ASF в буфере.</span><span class="sxs-lookup"><span data-stu-id="ddb10-190">The method parses the ASF data in the buffer.</span></span>
4.  <span data-ttu-id="ddb10-191">В цикле получите примеры мультимедиа из разделителя, вызвав [**имфасфсплиттер:: жетнекстсампле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="ddb10-191">In a loop, get media samples from the splitter by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample).</span></span> <span data-ttu-id="ddb10-192">Если параметр *пписампле* получает допустимый указатель [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , это означает, что разделитель ASF проанализировал один или несколько пакетов данных.</span><span class="sxs-lookup"><span data-stu-id="ddb10-192">If the *ppISample* parameter receives a valid [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer, it means the ASF splitter has parsed one or more data packets.</span></span> <span data-ttu-id="ddb10-193">Если *пписампле* получает значение **null**, прервать цикл и вернуться к шагу 1.</span><span class="sxs-lookup"><span data-stu-id="ddb10-193">If *ppISample* receives the value **NULL**, break from the loop and go back to step 1.</span></span>
5.  <span data-ttu-id="ddb10-194">Отображает сведения о примере.</span><span class="sxs-lookup"><span data-stu-id="ddb10-194">Display information about the sample.</span></span>
6.  <span data-ttu-id="ddb10-195">Прервать цикл из цикла в следующих условиях:</span><span class="sxs-lookup"><span data-stu-id="ddb10-195">Break from the loop in the following conditions:</span></span>
    -   <span data-ttu-id="ddb10-196">Параметр *пписампле* получает значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ddb10-196">The *ppISample* parameter receives the value **NULL**.</span></span>
    -   <span data-ttu-id="ddb10-197">Параметр *пдвстатусфлагс* не получает флаг **ASF \_ статусфлагс \_ неполный** .</span><span class="sxs-lookup"><span data-stu-id="ddb10-197">The *pdwStatusFlags* parameter does not receive the **ASF\_STATUSFLAGS\_INCOMPLETE** flag.</span></span>

<span data-ttu-id="ddb10-198">Повторяйте эти шаги, пока не дойдете до конца файла.</span><span class="sxs-lookup"><span data-stu-id="ddb10-198">Repeat these steps until you reach the end of the file.</span></span> <span data-ttu-id="ddb10-199">В следующем коде показаны следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="ddb10-199">The following code shows these steps:</span></span>


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



<span data-ttu-id="ddb10-200">Функция noframes проверяет, является ли пример ключевым кадром, путем получения значения атрибута [**мфсампликстенсион \_ клеанпоинт**](mfsampleextension-cleanpoint-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="ddb10-200">The IsKeyFrame function tests whether a sample is a key frame, by getting the value of the [**MFSampleExtension\_CleanPoint**](mfsampleextension-cleanpoint-attribute.md) attribute.</span></span>


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



<span data-ttu-id="ddb10-201">В целях иллюстрации в этом учебнике отображаются некоторые сведения о каждом кадре ключа видео, вызывая следующую функцию:</span><span class="sxs-lookup"><span data-stu-id="ddb10-201">For illustration purposes, this tutorial displays some information for each video key frame, by calling the following function:</span></span>


```C++
void DisplayKeyFrame(IMFSample *pSample)
{
    DWORD   cBuffers = 0;           // Buffer count
    DWORD   cbTotalLength = 0;      // Buffer length
    MFTIME  hnsTime = 0;            // Time stamp

    // Print various information about the key frame.
    if (SUCCEEDED(pSample->GetBufferCount(&cBuffers)))
    {
        wprintf_s(L"Buffer count: %d\n", cBuffers);
    }
    if (SUCCEEDED(pSample->GetTotalLength(&cbTotalLength)))
    {
        wprintf_s(L"Length: %d bytes\n", cbTotalLength);
    }
    if (SUCCEEDED(pSample->GetSampleTime(&hnsTime)))
    {
        // Convert the time stamp to seconds.
        double sec = static_cast<double>(hnsTime / 10000) / 1000;
        wprintf_s(L"Time stamp: %f sec.\n", sec);
    }
    wprintf_s(L"\n");
}
```



<span data-ttu-id="ddb10-202">Типичное приложение будет использовать пакеты данных для декодирования, ремуксинг, отправки по сети или другой задачи.</span><span class="sxs-lookup"><span data-stu-id="ddb10-202">A typical application would use the data packets for decoding, remuxing, sending over the network, or some other task.</span></span>

## <a name="7-write-the-entry-point-function"></a><span data-ttu-id="ddb10-203">7. Написание функции Entry-Point</span><span class="sxs-lookup"><span data-stu-id="ddb10-203">7. Write the Entry-Point Function</span></span>

<span data-ttu-id="ddb10-204">Теперь можно объединить предыдущие шаги в законченное приложение.</span><span class="sxs-lookup"><span data-stu-id="ddb10-204">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="ddb10-205">Перед использованием любого объекта Media Foundation инициализируйте Media Foundationную платформу, вызвав [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="ddb10-205">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="ddb10-206">По завершении вызовите [**мфшутдовн**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="ddb10-206">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="ddb10-207">Для получения дополнительных сведений [инициализируйте Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="ddb10-207">For more information, [Initializing Media Foundation](initializing-media-foundation.md).</span></span>


```C++
int wmain(int argc, WCHAR* argv[])
{
    if (argc != 2)
    {
        _s(L"Usage: %s input.wmv");
        return 0;
    }

    // Start the Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        PCWSTR pszFileName = argv[1]; 
        BOOL   bHasVideo = FALSE;

        IMFByteStream       *pStream = NULL;
        IMFASFContentInfo   *pContentInfo = NULL;
        IMFASFSplitter      *pSplitter = NULL;

        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);

        // Read the ASF header.
        if (SUCCEEDED(hr))
        {
            hr = CreateContentInfo(pStream, &pContentInfo);
        }

        // Create the ASF splitter.
        if (SUCCEEDED(hr))
        {
            hr = CreateASFSplitter(pContentInfo, &pSplitter);
        }

        // Select the first video stream.
        if (SUCCEEDED(hr))
        {
            hr = SelectVideoStream(pContentInfo, pSplitter, &bHasVideo);
        }

        // Parse the ASF file.
        if (SUCCEEDED(hr))
        {
            if (bHasVideo)
            {
                hr = DisplayKeyFrames(pStream, pSplitter);
            }
            else
            {
                wprintf_s(L"No video stream.\n");
            }
        }
        SafeRelease(&pSplitter);
        SafeRelease(&pContentInfo);
        SafeRelease(&pStream);
    
        // Shut down the Media Foundation platform.
        MFShutdown();
    }
    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="program-listing"></a><span data-ttu-id="ddb10-208">Список программ</span><span class="sxs-lookup"><span data-stu-id="ddb10-208">Program Listing</span></span>

<span data-ttu-id="ddb10-209">В следующем коде показан полный список для учебника.</span><span class="sxs-lookup"><span data-stu-id="ddb10-209">The following code shows the complete listing for the tutorial.</span></span>


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <Mferror.h>

#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

// Read data from a byte stream into a media buffer.
//
// This function reads a maximum of cbMax bytes, or up to the size size of the 
// buffer, whichever is smaller. If the end of the byte stream is reached, the 
// actual amount of data read might be less than either of these values.
//
// To find out how much data was read, call IMFMediaBuffer::GetCurrentLength.

HRESULT ReadFromByteStream(
    IMFByteStream *pStream,     // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,    // Pointer to the media buffer.
    DWORD cbMax                 // Maximum amount to read.
    )
{
    DWORD cbBufferMax = 0;
    DWORD cbRead = 0;
    BYTE *pData= NULL;

    HRESULT hr = pBuffer->Lock(&pData, &cbBufferMax, NULL);

    // Do not exceed the maximum size of the buffer.
    if (SUCCEEDED(hr))
    {
        if (cbMax > cbBufferMax)
        {
            cbMax = cbBufferMax;
        }

        // Read up to cbMax bytes.
        hr = pStream->Read(pData, cbMax, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }
    if (pData)
    {
        pBuffer->Unlock();
    }
    return hr;
}


// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 

// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}


// Select the first video stream for parsing with the ASF splitter.

HRESULT SelectVideoStream(IMFASFContentInfo *pContentInfo, 
    IMFASFSplitter *pSplitter, BOOL *pbHasVideo)
{
    DWORD   cStreams = 0;
    WORD    wStreamID = 0;

    IMFASFProfile *pProfile = NULL;
    IMFASFStreamConfig *pStream = NULL;

    // Get the ASF profile from the ContentInfo object.
    HRESULT hr = pContentInfo->GetProfile(&pProfile);

    // Loop through all of the streams in the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&cStreams);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            GUID    streamType = GUID_NULL;

            // Get the stream type and stream identifier.
            hr = pProfile->GetStream(i, &wStreamID, &pStream);
            if (FAILED(hr)) 
            {
                break;
            }

            hr = pStream->GetStreamType(&streamType);
            if (FAILED(hr)) 
            {
                break;
            }

            if (streamType == MFMediaType_Video)
            {
                *pbHasVideo = TRUE;
                break;
            }
            SafeRelease(&pStream);
        }
    }

    // Select the video stream, if found.
    if (SUCCEEDED(hr))
    {
        if (*pbHasVideo)
        {
            // SelectStreams takes an array of stream identifiers.
            hr = pSplitter->SelectStreams(&wStreamID, 1);
        }
    }
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    return hr;
}

inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}

void DisplayKeyFrame(IMFSample *pSample)
{
    DWORD   cBuffers = 0;           // Buffer count
    DWORD   cbTotalLength = 0;      // Buffer length
    MFTIME  hnsTime = 0;            // Time stamp

    // Print various information about the key frame.
    if (SUCCEEDED(pSample->GetBufferCount(&cBuffers)))
    {
        wprintf_s(L"Buffer count: %d\n", cBuffers);
    }
    if (SUCCEEDED(pSample->GetTotalLength(&cbTotalLength)))
    {
        wprintf_s(L"Length: %d bytes\n", cbTotalLength);
    }
    if (SUCCEEDED(pSample->GetSampleTime(&hnsTime)))
    {
        // Convert the time stamp to seconds.
        double sec = static_cast<double>(hnsTime / 10000) / 1000;
        wprintf_s(L"Time stamp: %f sec.\n", sec);
    }
    wprintf_s(L"\n");
}


// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}

int wmain(int argc, WCHAR* argv[])
{
    if (argc != 2)
    {
        _s(L"Usage: %s input.wmv");
        return 0;
    }

    // Start the Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        PCWSTR pszFileName = argv[1]; 
        BOOL   bHasVideo = FALSE;

        IMFByteStream       *pStream = NULL;
        IMFASFContentInfo   *pContentInfo = NULL;
        IMFASFSplitter      *pSplitter = NULL;

        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);

        // Read the ASF header.
        if (SUCCEEDED(hr))
        {
            hr = CreateContentInfo(pStream, &pContentInfo);
        }

        // Create the ASF splitter.
        if (SUCCEEDED(hr))
        {
            hr = CreateASFSplitter(pContentInfo, &pSplitter);
        }

        // Select the first video stream.
        if (SUCCEEDED(hr))
        {
            hr = SelectVideoStream(pContentInfo, pSplitter, &bHasVideo);
        }

        // Parse the ASF file.
        if (SUCCEEDED(hr))
        {
            if (bHasVideo)
            {
                hr = DisplayKeyFrames(pStream, pSplitter);
            }
            else
            {
                wprintf_s(L"No video stream.\n");
            }
        }
        SafeRelease(&pSplitter);
        SafeRelease(&pContentInfo);
        SafeRelease(&pStream);
    
        // Shut down the Media Foundation platform.
        MFShutdown();
    }
    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="ddb10-210">См. также</span><span class="sxs-lookup"><span data-stu-id="ddb10-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddb10-211">Компоненты ASF Вмконтаинер</span><span class="sxs-lookup"><span data-stu-id="ddb10-211">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="ddb10-212">Поддержка ASF в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ddb10-212">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



