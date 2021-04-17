---
description: Индексатор ASF
ms.assetid: 3f95b0ac-d70f-4bc2-8524-c7de1df34afa
title: Индексатор ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c729b547339149ee578a90283c570ec8460b0c57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692092"
---
# <a name="asf-indexer"></a><span data-ttu-id="e9fea-103">Индексатор ASF</span><span class="sxs-lookup"><span data-stu-id="e9fea-103">ASF Indexer</span></span>

<span data-ttu-id="e9fea-104">*ИНДЕКСАТОР* ASF — это компонент уровня вмконтаинер, который используется для чтения или записи объектов индекса в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="e9fea-104">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="e9fea-105">Сведения о структуре файла ASF см. в разделе [Структура файлов ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="e9fea-105">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="e9fea-106">Приложение может использовать индексатор для выполнения поиска на основе времени презентации или создания новых записей индекса для файла ASF.</span><span class="sxs-lookup"><span data-stu-id="e9fea-106">An application can use the indexer to perform seeking based on presentation time or to generate new index entries for an ASF file.</span></span> <span data-ttu-id="e9fea-107">Индексатор ASF реализует интерфейс [**имфасфиндексер**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) .</span><span class="sxs-lookup"><span data-stu-id="e9fea-107">The ASF indexer implements the [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) interface.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e9fea-108">Тип индекса</span><span class="sxs-lookup"><span data-stu-id="e9fea-108">Index type</span></span></th>
<th><span data-ttu-id="e9fea-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e9fea-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e9fea-110">Индекс на основе времени презентации</span><span class="sxs-lookup"><span data-stu-id="e9fea-110">Presentation time-based Index</span></span></td>
<td><span data-ttu-id="e9fea-111">Предоставляет индексирование на основе времени представления для потоков аудио и видео в блоках индексов, чтобы сделать индексирование более эффективным.</span><span class="sxs-lookup"><span data-stu-id="e9fea-111">Provides presentation time-based indexing for audio and video streams in index blocks to make indexing more space efficient.</span></span> <span data-ttu-id="e9fea-112">Каждый блок индекса ссылается на элементы индекса, которые содержат смещение в байтах.</span><span class="sxs-lookup"><span data-stu-id="e9fea-112">Each index block references index entries that contain a byte offset.</span></span> <br/> <span data-ttu-id="e9fea-113">Смещение — это позиция искомого пакета данных относительно начала объекта данных ASF.</span><span class="sxs-lookup"><span data-stu-id="e9fea-113">The offset is the position of the data packet being seeked, relative to the start of the ASF Data Object.</span></span><br/> <span data-ttu-id="e9fea-114">GUID_NULL должен использоваться в качестве типа GUID для идентификатора индекса.</span><span class="sxs-lookup"><span data-stu-id="e9fea-114">GUID_NULL must be used as the GUID type for the index identifier.</span></span> <span data-ttu-id="e9fea-115">Для получения дополнительных сведений; см. раздел <a href="using-the-indexer-to-write-a-new-index.md">Использование индексатора для записи нового индекса</a>.</span><span class="sxs-lookup"><span data-stu-id="e9fea-115">For more information; see <a href="using-the-indexer-to-write-a-new-index.md">Using the Indexer to Write a New Index</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9fea-116">Индекс времени</span><span class="sxs-lookup"><span data-stu-id="e9fea-116">Timecode Index</span></span></td>
<td><span data-ttu-id="e9fea-117">Облегчает поиск по времени в потоках, содержащих метаданные времени.</span><span class="sxs-lookup"><span data-stu-id="e9fea-117">Facilitates seeking by timecode in streams which contain timecode metadata.</span></span> <span data-ttu-id="e9fea-118">Коды времени соответствуют формату SMPTE (<em>hours: minutes: seconds: frames</em>).</span><span class="sxs-lookup"><span data-stu-id="e9fea-118">The timecodes conform to a SMPTE format (<em>Hours:Minutes:Seconds:Frames</em>).</span></span> <span data-ttu-id="e9fea-119">Каждый блок индекса ссылается на элементы индекса, которые содержат смещение в байтах.</span><span class="sxs-lookup"><span data-stu-id="e9fea-119">Each index block references index entries that contain a byte offset.</span></span> <br/> <span data-ttu-id="e9fea-120">Смещение — это позиция искомого пакета данных относительно начала объекта данных ASF.</span><span class="sxs-lookup"><span data-stu-id="e9fea-120">The offset is the position of the data packet being seeked, relative to the start of the ASF Data Object.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e9fea-121">Объекты индекса времени в настоящее время не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="e9fea-121">Timecode index objects are not currently supported.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e9fea-122">Индекс на основе фрейма</span><span class="sxs-lookup"><span data-stu-id="e9fea-122">Frame-based Index</span></span></td>
<td><span data-ttu-id="e9fea-123">Предоставляет индексирование на основе кадров для видеопотоков.</span><span class="sxs-lookup"><span data-stu-id="e9fea-123">Provides frame-based indexing for video streams.</span></span> <span data-ttu-id="e9fea-124">Индексы в индексе на основе кадров находятся в виде номеров кадров, а первый кадр для потока в ASF-файле соответствует записи 0 в объекте индекса на основе фрейма.</span><span class="sxs-lookup"><span data-stu-id="e9fea-124">Indexes into the frame-based index are in terms of frame numbers, with the first frame for a stream in the ASF file corresponding to entry 0 in the frame-based index object.</span></span> <span data-ttu-id="e9fea-125">Каждый блок индекса ссылается на элементы индекса, которые содержат смещение в байтах.</span><span class="sxs-lookup"><span data-stu-id="e9fea-125">Each index block references index entries that contain a byte offset.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e9fea-126">Объекты индексов на основе кадров в настоящее время не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="e9fea-126">Frame-based index objects are not currently supported.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e9fea-127">Этот раздел содержит следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="e9fea-127">This section contains the following topics.</span></span>



| <span data-ttu-id="e9fea-128">Раздел</span><span class="sxs-lookup"><span data-stu-id="e9fea-128">Topic</span></span>                                                                                | <span data-ttu-id="e9fea-129">Описание</span><span class="sxs-lookup"><span data-stu-id="e9fea-129">Description</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9fea-130">Создание и Настройка индексатора</span><span class="sxs-lookup"><span data-stu-id="e9fea-130">Indexer Creation and Configuration</span></span>](indexer-creation-and-configuration.md)         | <span data-ttu-id="e9fea-131">Создание объекта индексатора и его настройка для чтения существующего индекса или записи нового объекта индекса ASF для файла.</span><span class="sxs-lookup"><span data-stu-id="e9fea-131">How to create an indexer object and configure it for reading an existing index or for writing a new ASF Index Object for a file.</span></span> |
| [<span data-ttu-id="e9fea-132">Использование индексатора для поиска в файле</span><span class="sxs-lookup"><span data-stu-id="e9fea-132">Using the Indexer to Seek in a File</span></span>](using-the-indexer-to-seek.md)                 | <span data-ttu-id="e9fea-133">Использование индексатора для поиска в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="e9fea-133">How to use the indexer to seek within an ASF file.</span></span>                                                                               |
| [<span data-ttu-id="e9fea-134">Использование индексатора для записи нового индекса</span><span class="sxs-lookup"><span data-stu-id="e9fea-134">Using the Indexer to Write a New Index</span></span>](using-the-indexer-to-write-a-new-index.md) | <span data-ttu-id="e9fea-135">Использование индексатора для создания записей индекса и записи нового объекта индекса для ASF-файла.</span><span class="sxs-lookup"><span data-stu-id="e9fea-135">How to use the indexer to generate index entries and write a new Index Object for an ASF file.</span></span>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="e9fea-136">См. также</span><span class="sxs-lookup"><span data-stu-id="e9fea-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9fea-137">Компоненты ASF Вмконтаинер</span><span class="sxs-lookup"><span data-stu-id="e9fea-137">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="e9fea-138">Поддержка ASF в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e9fea-138">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




