---
title: Объект индексатора
description: Объект индексатора
ms.assetid: 652e04a5-ed6e-4e92-acf4-55ed82f77ef1
keywords:
- Пакет SDK Windows Media Format, объекты индексаторов
- Расширенный системный формат (ASF), объекты индексаторов
- ASF (Расширенный системный формат), объекты индексатора
- объекты, объекты индексаторов
- объекты индексатора
- индексы, объекты индексаторов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c9aa8c1c3ff694ae8e125e17dc0190451c7f21
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "104069681"
---
# <a name="indexer-object"></a><span data-ttu-id="2f3fb-109">Объект индексатора</span><span class="sxs-lookup"><span data-stu-id="2f3fb-109">Indexer Object</span></span>

<span data-ttu-id="2f3fb-110">Объект индексатора создает индекс в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="2f3fb-110">The indexer object creates an index in an ASF file.</span></span> <span data-ttu-id="2f3fb-111">Индекс представляет собой стандартную часть ASF-файла, которая дает выборку видеороликов со временем, номерами кадров или (если применимо) с помощью стандартных меток времени SMPTE.</span><span class="sxs-lookup"><span data-stu-id="2f3fb-111">An index is a standard part of an ASF file that equates video samples with times, frame numbers, or (if applicable) Society of Motion Picture and Television Engineers (SMPTE) standard time stamps.</span></span> <span data-ttu-id="2f3fb-112">Без индекса ни объект чтения, ни синхронный объект Reader не могут перейти к точке в середине файла.</span><span class="sxs-lookup"><span data-stu-id="2f3fb-112">Without an index, neither the reader object nor the synchronous reader object can seek to a point in the middle of a file.</span></span>

<span data-ttu-id="2f3fb-113">Индексы, созданные этим объектом, необходимы только в том случае, если файл содержит один или несколько видеопотоков.</span><span class="sxs-lookup"><span data-stu-id="2f3fb-113">Indexes created by this object are only necessary if the file contains one or more video streams.</span></span> <span data-ttu-id="2f3fb-114">Это связано с тем, что звуковые данные не сжимаются временно, что упрощает поиск определенного времени в звуковом потоке.</span><span class="sxs-lookup"><span data-stu-id="2f3fb-114">This is because audio data is not temporally compressed, making it easy to find a given time in an audio stream.</span></span>

<span data-ttu-id="2f3fb-115">Объект индексатора создается функцией [**вмкреатеиндексер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) , которая устанавливает указатель на интерфейс **ивминдексер** .</span><span class="sxs-lookup"><span data-stu-id="2f3fb-115">The indexer object is created by the [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) function, which sets a pointer to an **IWMIndexer** interface.</span></span> <span data-ttu-id="2f3fb-116">Другие интерфейсы объекта индексатора можно получить, вызвав метод **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="2f3fb-116">The other interfaces of the indexer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="2f3fb-117">Объект индексатора поддерживает следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="2f3fb-117">The following interfaces are supported by the indexer object.</span></span>



| <span data-ttu-id="2f3fb-118">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="2f3fb-118">Interface</span></span>                          | <span data-ttu-id="2f3fb-119">Описание</span><span class="sxs-lookup"><span data-stu-id="2f3fb-119">Description</span></span>                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f3fb-120">**ивминдексер**</span><span class="sxs-lookup"><span data-stu-id="2f3fb-120">**IWMIndexer**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)   | <span data-ttu-id="2f3fb-121">Запускает и останавливает процесс индексирования.</span><span class="sxs-lookup"><span data-stu-id="2f3fb-121">Starts and stops the indexing process.</span></span>                                              |
| [<span data-ttu-id="2f3fb-122">**IWMIndexer2**</span><span class="sxs-lookup"><span data-stu-id="2f3fb-122">**IWMIndexer2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer2) | <span data-ttu-id="2f3fb-123">Настраивает индексатор, позволяя индексировать по кадрам, по времени или по коду времени SMPTE.</span><span class="sxs-lookup"><span data-stu-id="2f3fb-123">Configures the indexer, enabling indexing by frame, by time, or by SMPTE time code.</span></span> |



 

<span data-ttu-id="2f3fb-124">Для использования объекта индексатора в приложении должен быть реализован следующий интерфейс обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="2f3fb-124">The following callback interface must be implemented by the application in order to use the indexer object.</span></span>



| <span data-ttu-id="2f3fb-125">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="2f3fb-125">Interface</span></span>                                      | <span data-ttu-id="2f3fb-126">Описание</span><span class="sxs-lookup"><span data-stu-id="2f3fb-126">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="2f3fb-127">**ивмстатускаллбакк**</span><span class="sxs-lookup"><span data-stu-id="2f3fb-127">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="2f3fb-128">Получает сообщения о состоянии от процессов, выполняемых в отдельном потоке.</span><span class="sxs-lookup"><span data-stu-id="2f3fb-128">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2f3fb-129">См. также</span><span class="sxs-lookup"><span data-stu-id="2f3fb-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f3fb-130">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="2f3fb-130">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="2f3fb-131">**Работа с индексами**</span><span class="sxs-lookup"><span data-stu-id="2f3fb-131">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




