---
description: В этом разделе показано, как написать индекс для ASF-файла.
ms.assetid: a14e3bef-0232-4259-930a-d860ed9230fd
title: Использование индексатора для записи нового индекса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d37922b693c83a8417dea4006fc38397b805fb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811525"
---
# <a name="using-the-indexer-to-write-a-new-index"></a><span data-ttu-id="ce34b-103">Использование индексатора для записи нового индекса</span><span class="sxs-lookup"><span data-stu-id="ce34b-103">Using the Indexer to Write a New Index</span></span>

<span data-ttu-id="ce34b-104">В этом разделе показано, как написать индекс для ASF-файла.</span><span class="sxs-lookup"><span data-stu-id="ce34b-104">This topic shows how to write an index for an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="ce34b-105">Ниже приведена общая процедура создания индекса ASF.</span><span class="sxs-lookup"><span data-stu-id="ce34b-105">Here is the general procedure for creating an ASF index:</span></span>

1.  <span data-ttu-id="ce34b-106">Инициализирует новый экземпляр объекта индексатора ASF, как описано в разделе [Создание и Настройка индексатора](indexer-creation-and-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="ce34b-106">Initialize a new instance of the ASF indexer object, as described in [Indexer Creation and Configuration](indexer-creation-and-configuration.md).</span></span>
2.  <span data-ttu-id="ce34b-107">При необходимости настройте индексатор.</span><span class="sxs-lookup"><span data-stu-id="ce34b-107">Optionally, configure the indexer.</span></span>
3.  <span data-ttu-id="ce34b-108">Отправка пакетов данных ASF в индексатор.</span><span class="sxs-lookup"><span data-stu-id="ce34b-108">Send ASF data packets to the indexer.</span></span>
4.  <span data-ttu-id="ce34b-109">Зафиксируйте индекс.</span><span class="sxs-lookup"><span data-stu-id="ce34b-109">Commit the index.</span></span>
5.  <span data-ttu-id="ce34b-110">Получите завершенный индекс из индексатора и запишите его в поток.</span><span class="sxs-lookup"><span data-stu-id="ce34b-110">Get the completed index from the indexer, and write it to a stream.</span></span>

## <a name="configure-the-indexer"></a><span data-ttu-id="ce34b-111">Настройка индексатора</span><span class="sxs-lookup"><span data-stu-id="ce34b-111">Configure the Indexer</span></span>

<span data-ttu-id="ce34b-112">Чтобы использовать индексатор для записи нового объекта индекса, в объекте индексатора должен быть установлен флаг МФАСФ, чтобы \_ индексатор \_ записывал \_ новый \_ набор индексов с вызовом [**имфасфиндексер:: сетфлагс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) перед его инициализацией с помощью [**имфасфиндексер:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize).</span><span class="sxs-lookup"><span data-stu-id="ce34b-112">To use the indexer to write a new index object, the indexer object must have the flag MFASF\_INDEXER\_WRITE\_NEW\_INDEX set with a call to [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) before it is initialized with [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize).</span></span>

<span data-ttu-id="ce34b-113">Если для создания индекса настроен индексатор, вызывающий объект выбирает потоки для индексирования.</span><span class="sxs-lookup"><span data-stu-id="ce34b-113">When the indexer is configured for writing an index, the caller chooses the streams to be indexed.</span></span> <span data-ttu-id="ce34b-114">По умолчанию индексатор пытается создать объект индекса для всех потоков.</span><span class="sxs-lookup"><span data-stu-id="ce34b-114">By default, the indexer attempts to create an Index Object for all streams.</span></span> <span data-ttu-id="ce34b-115">По умолчанию интервал времени равен одной секунде.</span><span class="sxs-lookup"><span data-stu-id="ce34b-115">The default time interval is one second.</span></span>

<span data-ttu-id="ce34b-116">[**Имфасфиндексер:: сетиндексстатус**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) можно использовать для переопределения выбора потоков и типов индекса по умолчанию для объекта индексатора.</span><span class="sxs-lookup"><span data-stu-id="ce34b-116">[**IMFASFIndexer::SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) can be used to override the indexer object's default choice of streams and index types.</span></span>

<span data-ttu-id="ce34b-117">В следующем примере кода показана инициализация \_ \_ дескриптора и идентификатора ASF-индекса \_ \_ перед вызовом [**сетиндексстатус**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span><span class="sxs-lookup"><span data-stu-id="ce34b-117">The following example code shows the initialization of an ASF\_INDEX\_DESCRIPTOR and an ASF\_INDEX\_IDENTIFIER before a call to [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span></span>


```
ASF_INDEX_DESCRIPTOR IndexerType;
ZeroMemory(&IndexerType, sizeof(ASF_INDEX_DESCRIPTOR));

ASF_INDEX_IDENTIFIER IndexIdentifier;
ZeroMemory(&IndexIdentifier, sizeof(ASF_INDEX_IDENTIFIER));

IndexIdentifier.guidIndexType = GUID_NULL;
IndexIdentifier.wStreamNumber = 1;

IndexerType.Identifier = IndexIdentifier;
IndexerType.cPerEntryBytes  = MFASFINDEXER_PER_ENTRY_BYTES_DYNAMIC;
IndexerType.dwInterval  = MFASFINDEXER_NO_FIXED_INTERVAL;

hr = pIndexer->SetIndexStatus((BYTE*)&IndexerType, sizeof(ASF_INDEX_DESCRIPTOR), TRUE);
```



<span data-ttu-id="ce34b-118">Для идентификатора индекса GUID должен быть задан тип GUID \_ null, чтобы указать, что для типа индекса будет использоваться время представления.</span><span class="sxs-lookup"><span data-stu-id="ce34b-118">The index identifier must have its GUID index type set to GUID\_NULL to indicate that the index type will be presentation time-based.</span></span> <span data-ttu-id="ce34b-119">Идентификатор индекса также должен быть инициализирован с помощью номера потока ASF Stream для индексирования.</span><span class="sxs-lookup"><span data-stu-id="ce34b-119">The index identifier must also be initialized with the stream number of the ASF stream to be indexed.</span></span> <span data-ttu-id="ce34b-120">После задания идентификатора индекса используйте его для инициализации дескриптора индекса.</span><span class="sxs-lookup"><span data-stu-id="ce34b-120">After the index identifier is set, use it to initialize the index descriptor.</span></span>

<span data-ttu-id="ce34b-121">Структура дескриптора индекса содержит элементы, которые должны быть заданы перед вызовом [**сетиндексстатус**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span><span class="sxs-lookup"><span data-stu-id="ce34b-121">The index descriptor structure has members which must be set before the call to [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span></span> <span data-ttu-id="ce34b-122">**Идентификатор** — это [**Структура \_ \_ идентификатора ASF-индекса**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) , которая определяет номер потока и тип индекса.</span><span class="sxs-lookup"><span data-stu-id="ce34b-122">**Identifier** is an [**ASF\_INDEX\_IDENTIFIER**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) structure that identifies the stream number and the type of index.</span></span> <span data-ttu-id="ce34b-123">**кперентрибитес** — число байтов, используемых для каждой записи индекса.</span><span class="sxs-lookup"><span data-stu-id="ce34b-123">**cPerEntryBytes** is the number of bytes used for each index entry.</span></span> <span data-ttu-id="ce34b-124">Если значение МФАСФИНДЕКСЕР \_ в \_ \_ динамическом байте записи \_ , то элементы индекса имеют переменный размер.</span><span class="sxs-lookup"><span data-stu-id="ce34b-124">If the value is MFASFINDEXER\_PER\_ENTRY\_BYTES\_DYNAMIC, the index entries have variable size.</span></span> <span data-ttu-id="ce34b-125">**двинтервал** — интервал индексирования.</span><span class="sxs-lookup"><span data-stu-id="ce34b-125">**dwInterval** is the indexing interval.</span></span> <span data-ttu-id="ce34b-126">Значение МФАСФИНДЕКСЕР \_ без \_ фиксированного \_ интервала указывает на отсутствие фиксированного интервала индексирования.</span><span class="sxs-lookup"><span data-stu-id="ce34b-126">A value of MFASFINDEXER\_NO\_FIXED\_INTERVAL indicates that there is no fixed indexing interval.</span></span>

## <a name="send-asf-data-packets-to-the-indexer"></a><span data-ttu-id="ce34b-127">Отправка пакетов данных ASF в индексатор</span><span class="sxs-lookup"><span data-stu-id="ce34b-127">Send ASF Data Packets to the Indexer</span></span>

<span data-ttu-id="ce34b-128">Поскольку индексатор является объектом уровня Вмконтаинер, он должен использоваться вместе с мультиплексором во время создания пакета.</span><span class="sxs-lookup"><span data-stu-id="ce34b-128">Because the indexer is a WMContainer level object, it must be used in conjunction with the multiplexer during packet generation.</span></span>

<span data-ttu-id="ce34b-129">Пакеты, возвращаемые из [**жетнекстпаккет**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) , могут быть отправлены в объект индексатора с помощью вызовов [**женератеиндексентриес**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) , где он создает записи индекса для каждого отправленного пакета.</span><span class="sxs-lookup"><span data-stu-id="ce34b-129">Packets returned from [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) can be sent to the indexer object through calls to [**GenerateIndexEntries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) where it creates index entries for each packet sent.</span></span>

<span data-ttu-id="ce34b-130">В следующем коде показано, как это можно сделать:</span><span class="sxs-lookup"><span data-stu-id="ce34b-130">The following code demonstrates how this may be done:</span></span>


```C++
HRESULT SendSampleToMux(
    IMFASFMultiplexer *pMux,
    IMFASFIndexer *pIndex,
    IMFSample *pSample,
    WORD wStream,
    IMFByteStream *pDestStream
    )
{
    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacket = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    HRESULT hr = pMux->ProcessSample(wStream, pSample, 0);
    if (FAILED(hr))
    {
        goto done;
    }

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pOutputSample)
        {
            // Send the data packet to the indexer
            hr = pIndex->GenerateIndexEntries(pOutputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            // Convert the sample to a contiguous buffer.
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacket);
            if (FAILED(hr))
            {
                goto done;
            }

            // Write the buffer to the byte stream.
            hr = WriteBufferToByteStream(pDestStream, pDataPacket, NULL);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        SafeRelease(&pOutputSample);
        SafeRelease(&pDataPacket);
    }

done:
    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacket);
    return hr;
}
```



<span data-ttu-id="ce34b-131">Дополнительные сведения см. в разделе [Создание новых пакетов данных ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="ce34b-131">For more information, see [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>

## <a name="commit-the-index"></a><span data-ttu-id="ce34b-132">Фиксация индекса</span><span class="sxs-lookup"><span data-stu-id="ce34b-132">Commit the Index</span></span>

<span data-ttu-id="ce34b-133">После того, как последний пакет создал запись индекса для него, индекс должен быть зафиксирован.</span><span class="sxs-lookup"><span data-stu-id="ce34b-133">After the last packet has had an index entry created for it, the index must be committed.</span></span> <span data-ttu-id="ce34b-134">Это делается с помощью вызова [**имфасфиндексер:: коммитиндекс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex).</span><span class="sxs-lookup"><span data-stu-id="ce34b-134">This is done with a call to [**IMFASFIndexer::CommitIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex).</span></span> <span data-ttu-id="ce34b-135">**Коммитиндекс** принимает указатель на объект контентинфо, описывающий содержимое ASF-файла.</span><span class="sxs-lookup"><span data-stu-id="ce34b-135">**CommitIndex** takes a pointer to the ContentInfo object which describes the content of the ASF file.</span></span> <span data-ttu-id="ce34b-136">Фиксация индекса завершает индексирование и обновляет заголовок новыми сведениями о размере файла и возобновлении поиска.</span><span class="sxs-lookup"><span data-stu-id="ce34b-136">Committing the index finishes the indexing and updates the header with new information about file size and seekability.</span></span>

## <a name="get-the-completed-index"></a><span data-ttu-id="ce34b-137">Получение завершенного индекса</span><span class="sxs-lookup"><span data-stu-id="ce34b-137">Get the Completed Index</span></span>

<span data-ttu-id="ce34b-138">Чтобы получить завершенный индекс из индексатора, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ce34b-138">To get the completed index from the indexer, perform the following steps:</span></span>

1.  <span data-ttu-id="ce34b-139">Вызовите [**имфасфиндексер:: жетиндексвритеспаце**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) , чтобы получить размер индекса.</span><span class="sxs-lookup"><span data-stu-id="ce34b-139">Call [**IMFASFIndexer::GetIndexWriteSpace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) to get the size of the index.</span></span>
2.  <span data-ttu-id="ce34b-140">Вызовите [**мфкреатемеморибуффер**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) , чтобы создать буфер мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ce34b-140">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer.</span></span> <span data-ttu-id="ce34b-141">Можно либо выделить буфер, достаточно большой для хранения всего индекса, чтобы выделить буфер меньшего размера и получить индекс в виде фрагментов.</span><span class="sxs-lookup"><span data-stu-id="ce34b-141">You can either allocate an buffer that is large enough to hold the entire index, of allocate a smaller buffer and get the index in chunks.</span></span>
3.  <span data-ttu-id="ce34b-142">Вызовите метод [**имфасфиндексер:: жеткомплетединдекс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) , чтобы получить данные индекса.</span><span class="sxs-lookup"><span data-stu-id="ce34b-142">Call [**IMFASFIndexer::GetCompletedIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) to get the index data.</span></span> <span data-ttu-id="ce34b-143">При первом вызове задайте для параметра *кбоффсетвисининдекс* значение 0.</span><span class="sxs-lookup"><span data-stu-id="ce34b-143">On the first call, set the *cbOffsetWithinIndex* parameter to zero.</span></span> <span data-ttu-id="ce34b-144">Если индекс получается в виде фрагментов, каждый раз увеличивается значение *кбоффсетвисининдекс* в размере данных из предыдущего вызова.</span><span class="sxs-lookup"><span data-stu-id="ce34b-144">If you get the index in chunks, increment *cbOffsetWithinIndex* each time by the size of the data from the previous call.</span></span>
4.  <span data-ttu-id="ce34b-145">Вызовите [**имфмедиабуффер:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) , чтобы получить указатель на данные индекса и размер данных.</span><span class="sxs-lookup"><span data-stu-id="ce34b-145">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the index data and the size of the data.</span></span>
5.  <span data-ttu-id="ce34b-146">Запишите данные индекса в файл ASF.</span><span class="sxs-lookup"><span data-stu-id="ce34b-146">Write the index data to the ASF file.</span></span>
6.  <span data-ttu-id="ce34b-147">Вызовите метод [**имфмедиабуффер:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) , чтобы разблокировать буфер мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ce34b-147">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the media buffer.</span></span>
7.  <span data-ttu-id="ce34b-148">Повторите шаги 3 – 6, пока не запишете весь индекс.</span><span class="sxs-lookup"><span data-stu-id="ce34b-148">Repeat steps 3–6 until you have written the entire index.</span></span>

<span data-ttu-id="ce34b-149">В следующем коде показаны следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="ce34b-149">The following code shows these steps:</span></span>


```C++
HRESULT WriteASFIndex(IMFASFIndexer *pIndex,IMFByteStream *pStream)
{
    const DWORD cbChunkSize = 4096;

    IMFMediaBuffer *pBuffer = NULL;

    QWORD cbIndex = 0;
    DWORD cbIndexWritten = 0;

    HRESULT hr = pIndex->GetIndexWriteSpace(&cbIndex);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateMemoryBuffer(cbChunkSize, &pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    while (cbIndexWritten < cbIndex)
    {
        BYTE *pData = NULL;
        DWORD cbData = 0;
        DWORD cbWritten = 0;

        hr = pIndex->GetCompletedIndex(pBuffer, cbIndexWritten);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pBuffer->Lock(&pData, NULL, &cbData);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStream->Write(pData, cbData, &cbWritten);

        (void)pBuffer->Unlock();

        if (FAILED(hr))
        {
            goto done;
        }

        cbIndexWritten += cbData;
    }

done:
    SafeRelease(&pBuffer);
    return hr;
};
```



## <a name="related-topics"></a><span data-ttu-id="ce34b-150">См. также</span><span class="sxs-lookup"><span data-stu-id="ce34b-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce34b-151">Индексатор ASF</span><span class="sxs-lookup"><span data-stu-id="ce34b-151">ASF Indexer</span></span>](asf-index-object.md)
</dt> </dl>

 

 



