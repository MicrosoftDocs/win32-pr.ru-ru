---
description: Чтение объекта заголовка ASF существующего файла
ms.assetid: 0e37f0d3-a37b-4f36-a133-7b1922e9944b
title: Чтение объекта заголовка ASF существующего файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b231cb0b9af6b24f84efaa6403a4774e66bbb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701797"
---
# <a name="reading-the-asf-header-object-of-an-existing-file"></a><span data-ttu-id="aa91b-103">Чтение объекта заголовка ASF существующего файла</span><span class="sxs-lookup"><span data-stu-id="aa91b-103">Reading the ASF Header Object of an Existing File</span></span>

<span data-ttu-id="aa91b-104">В объекте ASF Контентинфо хранятся сведения, представляющие объекты заголовка ASF файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="aa91b-104">The ASF ContentInfo object stores information that represents the ASF Header Objects of a media file.</span></span> <span data-ttu-id="aa91b-105">Заполненный объект Контентинфо необходим для чтения и анализа существующего ASF-файла.</span><span class="sxs-lookup"><span data-stu-id="aa91b-105">A populated ContentInfo object is required in order to read and parse an existing ASF file.</span></span>

<span data-ttu-id="aa91b-106">После создания объекта Контентинфо путем вызова функции [**мфкреатеасфконтентинфо**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) приложение должно инициализировать его с информацией заголовка из ASF-файла, который требуется считать.</span><span class="sxs-lookup"><span data-stu-id="aa91b-106">After creating the ContentInfo object by calling the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function, the application must initialize it with header information from the ASF file that is to be read.</span></span> <span data-ttu-id="aa91b-107">Чтобы заполнить объект, вызовите [**имфасфконтентинфо::P арсехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span><span class="sxs-lookup"><span data-stu-id="aa91b-107">To populate the object, call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span></span>

<span data-ttu-id="aa91b-108">Для **парсехеадер** требуется буфер мультимедиа, содержащий объект заголовка ASF-файла.</span><span class="sxs-lookup"><span data-stu-id="aa91b-108">**ParseHeader** requires a media buffer that contains the Header Object of the ASF file.</span></span> <span data-ttu-id="aa91b-109">Один из вариантов — заполнить буфер мультимедиа с помощью объекта Header, чтобы создать байтовый поток для файла, а затем считать первые 30 байт данных из байтового потока в буфер мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="aa91b-109">One option is to fill a media buffer with the Header Object to create a byte stream for the file and then read the first 30 bytes of data from the byte stream into a media buffer.</span></span> <span data-ttu-id="aa91b-110">Затем можно получить размер, передав первые 24 байта объекта заголовка методу [**имфасфконтентинфо:: жесеадерсизе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) .</span><span class="sxs-lookup"><span data-stu-id="aa91b-110">You can then get the size by passing the first 24 bytes of the Header Object to the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="aa91b-111">После получения размера можно прочитать весь объект заголовка в буфере мультимедиа и передать его в **парсехеадер**.</span><span class="sxs-lookup"><span data-stu-id="aa91b-111">After getting the size, you can read the entire Header Object in a media buffer and pass it to **ParseHeader**.</span></span> <span data-ttu-id="aa91b-112">Метод начинает синтаксический анализ со смещением от начала буфера мультимедиа, указанного в параметре *кбоффсетвисинхеадер* .</span><span class="sxs-lookup"><span data-stu-id="aa91b-112">The method starts parsing at the offset from the start of the media buffer specified in the *cbOffsetWithinHeader* parameter.</span></span>

<span data-ttu-id="aa91b-113">В следующем примере кода создается и инициализируется объект Контентинфо для чтения существующего ASF-файла, содержащегося в байтовом потоке.</span><span class="sxs-lookup"><span data-stu-id="aa91b-113">The following example code creates and initializes a ContentInfo object for reading an existing ASF file contained in a byte stream.</span></span> <span data-ttu-id="aa91b-114">Во-первых, мы определим вспомогательную функцию, которая считывает данные из байтового потока и выделяет буфер мультимедиа для хранения данных:</span><span class="sxs-lookup"><span data-stu-id="aa91b-114">First, we define a helper function that reads data from a byte stream and allocates a media buffer to hold the data:</span></span>


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



<span data-ttu-id="aa91b-115">В следующем примере считывается объект заголовка ASF из байтового потока и заполняется объект ASF Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="aa91b-115">The next example reads the ASF Header Object from a byte stream and populates an ASF ContentInfo object.</span></span>


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



> [!Note]  
> <span data-ttu-id="aa91b-116">В этих примерах для освобождения указателей интерфейса используется функция [саферелеасе](saferelease.md) .</span><span class="sxs-lookup"><span data-stu-id="aa91b-116">These examples use the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="aa91b-117">См. также</span><span class="sxs-lookup"><span data-stu-id="aa91b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa91b-118">Объект Контентинфо ASF</span><span class="sxs-lookup"><span data-stu-id="aa91b-118">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> <dt>

[<span data-ttu-id="aa91b-119">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="aa91b-119">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="aa91b-120">Поддержка ASF в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aa91b-120">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="aa91b-121">Получение сведений из объектов заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="aa91b-121">Getting Information from ASF Header Objects</span></span>](getting-information-from-asf-header-objects.md)
</dt> </dl>

 

 



