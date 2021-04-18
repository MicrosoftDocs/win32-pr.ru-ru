---
description: Индексатор ASF — это компонент уровня Вмконтаинер, который используется для чтения или записи объектов индекса в файле ASF. В этом разделе содержатся сведения об использовании индексатора ASF для поиска в файле ASF.
ms.assetid: 9c501d33-847e-448e-a19c-39dfbc7757ca
title: Использование индексатора для поиска в файле ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c40c35f876fdc5452c596048d121fb0c2933094a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711691"
---
# <a name="using-the-indexer-to-seek-within-an-asf-file"></a><span data-ttu-id="5014f-104">Использование индексатора для поиска в файле ASF</span><span class="sxs-lookup"><span data-stu-id="5014f-104">Using the Indexer to Seek Within an ASF File</span></span>

<span data-ttu-id="5014f-105">*ИНДЕКСАТОР* ASF — это компонент уровня вмконтаинер, который используется для чтения или записи объектов индекса в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="5014f-105">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="5014f-106">В этом разделе содержатся сведения об использовании индексатора ASF для поиска в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="5014f-106">This topic provides information about using the ASF indexer to seek within an ASF file.</span></span>

-   [<span data-ttu-id="5014f-107">Инициализация индексатора для поиска</span><span class="sxs-lookup"><span data-stu-id="5014f-107">Initializing the Indexer for Seeking</span></span>](#initializing-the-indexer-for-seeking)
-   [<span data-ttu-id="5014f-108">Получение расположения поиска.</span><span class="sxs-lookup"><span data-stu-id="5014f-108">Getting the Seek Position.</span></span>](#getting-the-seek-position)
-   [<span data-ttu-id="5014f-109">См. также</span><span class="sxs-lookup"><span data-stu-id="5014f-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="5014f-110">Сведения о структуре файла ASF см. в разделе [Структура файлов ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="5014f-110">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

## <a name="initializing-the-indexer-for-seeking"></a><span data-ttu-id="5014f-111">Инициализация индексатора для поиска</span><span class="sxs-lookup"><span data-stu-id="5014f-111">Initializing the Indexer for Seeking</span></span>

<span data-ttu-id="5014f-112">Чтобы инициализировать индексатор ASF для поиска, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="5014f-112">To initialize the ASF indexer for seeking:</span></span>

1.  <span data-ttu-id="5014f-113">Вызовите [**мфкреатеасфиндексер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) , чтобы создать новый экземпляр индексатора ASF.</span><span class="sxs-lookup"><span data-stu-id="5014f-113">Call [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) to create a new instance of the ASF indexer.</span></span>
2.  <span data-ttu-id="5014f-114">Вызовите метод [**имфасфиндексер:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) для инициализации индексатора.</span><span class="sxs-lookup"><span data-stu-id="5014f-114">Call [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) to initialize the indexer.</span></span> <span data-ttu-id="5014f-115">Этот метод получает сведения из заголовка ASF, чтобы определить, какие потоки ASF индексируются.</span><span class="sxs-lookup"><span data-stu-id="5014f-115">This method gets information from the ASF header to determine which ASF streams are indexed.</span></span> <span data-ttu-id="5014f-116">По умолчанию объект индексатора настроен для поиска.</span><span class="sxs-lookup"><span data-stu-id="5014f-116">By default, the indexer object is configured for seeking.</span></span>
3.  <span data-ttu-id="5014f-117">Вызовите метод [**имфасфиндексер:: жетиндекспоситион**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) , чтобы найти смещение индекса в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="5014f-117">Call [**IMFASFIndexer::GetIndexPosition**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) to find the offset of the index within the ASF file.</span></span>
4.  <span data-ttu-id="5014f-118">Вызовите функцию [**мфкреатеасфиндексербитестреам**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) , чтобы создать байтовый поток для чтения индекса.</span><span class="sxs-lookup"><span data-stu-id="5014f-118">Call the [**MFCreateASFIndexerByteStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) function to create a byte stream for reading the index.</span></span> <span data-ttu-id="5014f-119">Входные данные функции являются указателем на байтовый поток, который содержит ASF-файл, и смещение индекса (из предыдущего шага).</span><span class="sxs-lookup"><span data-stu-id="5014f-119">The input to this function is a pointer to a byte stream that contains the ASF file, and the offset of the index (from the previous step).</span></span>
5.  <span data-ttu-id="5014f-120">Вызовите метод [**имфасфиндексер:: сетиндексбитестреамс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) , чтобы задать поток байтов индекса в индексаторе.</span><span class="sxs-lookup"><span data-stu-id="5014f-120">Call [**IMFASFIndexer::SetIndexByteStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) to set the index byte stream on the indexer.</span></span>

<span data-ttu-id="5014f-121">В следующем коде показаны следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="5014f-121">The following code shows these steps:</span></span>


```C++
HRESULT CreateASFIndexer(
    IMFByteStream *pContentByteStream,  // Pointer to the content byte stream
    IMFASFContentInfo *pContentInfo,
    IMFASFIndexer **ppIndexer
    )
{
    IMFASFIndexer *pIndexer = NULL;
    IMFByteStream *pIndexerByteStream = NULL;

    QWORD qwLength = 0, qwIndexOffset = 0, qwBytestreamLength = 0;

    // Create the indexer.
    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    //Initialize the indexer to work with this ASF library
    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //Check if the index exists. You can only do this after creating the indexer

    //Get byte stream length
    hr = pContentByteStream->GetLength(&qwLength);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get index offset
    hr = pIndexer->GetIndexPosition(pContentInfo, &qwIndexOffset);
    if (FAILED(hr))
    {
        goto done;
    }

    if ( qwIndexOffset >= qwLength)
    {
        //index object does not exist, release the indexer
        goto done;
    }
    else
    {
        // initialize the indexer
        // Create a byte stream that the Indexer will use to read in
        // and parse the indexers.
         hr = MFCreateASFIndexerByteStream(
             pContentByteStream,
             qwIndexOffset,
             &pIndexerByteStream
             );

        if (FAILED(hr))
        {
            goto done;
        }
   }

    hr = pIndexer->SetIndexByteStreams(&pIndexerByteStream, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    SafeRelease(&pIndexer);
    SafeRelease(&pIndexerByteStream);
    return hr;
}
```



## <a name="getting-the-seek-position"></a><span data-ttu-id="5014f-122">Получение расположения поиска.</span><span class="sxs-lookup"><span data-stu-id="5014f-122">Getting the Seek Position.</span></span>

1.  <span data-ttu-id="5014f-123">Чтобы определить, индексируется ли определенный поток, вызовите метод [**имфасфиндексер:: жетиндексстатус**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus).</span><span class="sxs-lookup"><span data-stu-id="5014f-123">To find out if a particular stream is indexed, call [**IMFASFIndexer::GetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus).</span></span> <span data-ttu-id="5014f-124">Если поток индексируется, параметр *пфисиндексед* получает значение **true**; в противном случае он получает значение **false**.</span><span class="sxs-lookup"><span data-stu-id="5014f-124">If the stream is indexed, the *pfIsIndexed* parameter receives the value **TRUE**; otherwise it receives the value **FALSE**.</span></span>
2.  <span data-ttu-id="5014f-125">По умолчанию индексатор использует поиск вперед.</span><span class="sxs-lookup"><span data-stu-id="5014f-125">By default, the indexer uses forward seeking.</span></span> <span data-ttu-id="5014f-126">Для поиска в обратном порядке (т. е. поиска с конца файла) вызовите метод [**имфасфиндексер:: сетфлагс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) и установите флаг **мфасф \_ \_ Read \_ для \_ реверсеплайбакк** .</span><span class="sxs-lookup"><span data-stu-id="5014f-126">For reverse seeking (that is, seeking from the end of the file), call [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) and set the **MFASF\_INDEXER\_READ\_FOR\_REVERSEPLAYBACK** flag.</span></span> <span data-ttu-id="5014f-127">В противном случае пропустите этот шаг.</span><span class="sxs-lookup"><span data-stu-id="5014f-127">Otherwise, skip this step.</span></span>
3.  <span data-ttu-id="5014f-128">Если поток индексируется, получите положение поиска для указанного времени презентации, вызвав [**имфасфиндексер:: жетсикпоситионфорвалуе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue).</span><span class="sxs-lookup"><span data-stu-id="5014f-128">If the stream is indexed, get the seek position for a specified presentation time by calling [**IMFASFIndexer::GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue).</span></span> <span data-ttu-id="5014f-129">Этот метод считывает индекс ASF и находит запись индекса, ближайшую к запрошенному времени.</span><span class="sxs-lookup"><span data-stu-id="5014f-129">This method reads the ASF index and finds the index entry that is closest to the requested time.</span></span> <span data-ttu-id="5014f-130">Метод возвращает смещение в байтах для пакета данных, указанного в записи индекса.</span><span class="sxs-lookup"><span data-stu-id="5014f-130">The method returns the byte offset of the data packet specified by the index entry.</span></span> <span data-ttu-id="5014f-131">Смещение в байтах задается относительно начала объекта данных ASF.</span><span class="sxs-lookup"><span data-stu-id="5014f-131">The byte offset is relative to the start of the ASF Data Object.</span></span>

<span data-ttu-id="5014f-132">Метод [**жетсикпоситионфорвалуе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) принимает указатель на структуру [**идентификатора ASF- \_ индекса \_**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) .</span><span class="sxs-lookup"><span data-stu-id="5014f-132">The [**GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) method takes a pointer to the [**ASF\_INDEX\_IDENTIFIER**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) structure.</span></span> <span data-ttu-id="5014f-133">Эта структура задает тип индекса и идентификатор потока.</span><span class="sxs-lookup"><span data-stu-id="5014f-133">This structure specifies an index type and a stream identifier.</span></span> <span data-ttu-id="5014f-134">В настоящее время индекс должен иметь тип GUID \_ null, который указывает индексирование на основе времени.</span><span class="sxs-lookup"><span data-stu-id="5014f-134">Currently, the index type must be GUID\_NULL, which specifies time-based indexing.</span></span>

<span data-ttu-id="5014f-135">Следующий код получает положение поиска по заданному идентификатору потока и целевому времени презентации.</span><span class="sxs-lookup"><span data-stu-id="5014f-135">The following code gets a seek position, given a stream identifier and target presentation time.</span></span> <span data-ttu-id="5014f-136">Если вызов завершается, он возвращает смещение данных в параметре *пкбдатаоффсет* и приблизительное фактическое время поиска в *фнсаппрокссиктиме*.</span><span class="sxs-lookup"><span data-stu-id="5014f-136">If the call succeeds, it returns the data offset in the *pcbDataOffset* parameter and the approximate actual seek time in *phnsApproxSeekTime*.</span></span>


```C++
HRESULT GetSeekPositionWithIndexer(
    IMFASFIndexer *pIndexer,
    WORD          wStreamNumber,
    MFTIME        hnsSeekTime,          // Desired seek time, in 100-nsec.
    BOOL          bReverse,
    QWORD         *pcbDataOffset,       // Receives the offset in bytes.
    MFTIME        *phnsApproxSeekTime   // Receives the approximate seek time.
    )
{
    // Query whether the stream is indexed.

    ASF_INDEX_IDENTIFIER IndexIdentifier = { GUID_NULL, wStreamNumber };

    BOOL fIsIndexed = FALSE;

    ASF_INDEX_DESCRIPTOR descriptor;

    DWORD cbIndexDescriptor = sizeof(descriptor);

    HRESULT hr = pIndexer->GetIndexStatus(
        &IndexIdentifier,
        &fIsIndexed,
        (BYTE*)&descriptor,
        &cbIndexDescriptor
        );

    if (hr == MF_E_BUFFERTOOSMALL)
    {
        hr = S_OK;
    }
    else if (FAILED(hr))
    {
        goto done;
    }

    if (!fIsIndexed)
    {
        hr = MF_E_ASF_NOINDEX;
        goto done;
    }

    if (bReverse)
    {
        hr = pIndexer->SetFlags(MFASF_INDEXER_READ_FOR_REVERSEPLAYBACK);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Get the offset from the indexer.

    PROPVARIANT var;

    var.vt = VT_I8;
    var.hVal.QuadPart = hnsSeekTime;

    hr = pIndexer->GetSeekPositionForValue(
        &var,
        &IndexIdentifier,
        pcbDataOffset,
        phnsApproxSeekTime,
        0
        );

done:
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="5014f-137">См. также</span><span class="sxs-lookup"><span data-stu-id="5014f-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5014f-138">Индексатор ASF</span><span class="sxs-lookup"><span data-stu-id="5014f-138">ASF Indexer</span></span>](asf-index-object.md)
</dt> </dl>

 

 



