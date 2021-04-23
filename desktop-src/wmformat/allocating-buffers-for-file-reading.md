---
title: Выделение буферов для чтения файлов
description: Выделение буферов для чтения файлов
ms.assetid: da66ef5b-ec92-445c-90ba-5ee89e0def36
keywords:
- Windows Media Format SDK, чтение файлов ASF
- Расширенный формат систем (ASF), чтение файлов
- ASF (Расширенный системный формат), чтение файлов
- Windows Media Format SDK, выделение буферов
- Расширенный системный формат (ASF), выделение буферов
- ASF (Расширенный системный формат), выделение буферов
- Расширенный системный формат (ASF), выделение буфера
- ASF (Расширенный системный формат), выделение буфера
- выделение буфера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecdf9ba0a333bbe25c94ec087911237b68f38f74
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412473"
---
# <a name="allocating-buffers-for-file-reading"></a><span data-ttu-id="b2ca3-112">Выделение буферов для чтения файлов</span><span class="sxs-lookup"><span data-stu-id="b2ca3-112">Allocating Buffers for File Reading</span></span>

<span data-ttu-id="b2ca3-113">В самом базовом сценарии чтения файлов буферы, используемые для доставки образцов, выделяются объектом чтения (объектом Reader или синхронным объектом Reader).</span><span class="sxs-lookup"><span data-stu-id="b2ca3-113">In the most basic file-reading scenario, the buffers used to deliver samples are allocated by the reading object (the reader object or the synchronous reader object).</span></span> <span data-ttu-id="b2ca3-114">Однако можно самостоятельно выделить буферы.</span><span class="sxs-lookup"><span data-stu-id="b2ca3-114">You can, however, allocate buffers yourself.</span></span> <span data-ttu-id="b2ca3-115">Дополнительные сведения о преимуществах выделения собственных буферов см. в разделе [Поддержка выводимых пользователем примеров](user-allocated-sample-support.md).</span><span class="sxs-lookup"><span data-stu-id="b2ca3-115">For more information about the benefits of allocating your own buffers, see [User Allocated Sample Support](user-allocated-sample-support.md).</span></span>

<span data-ttu-id="b2ca3-116">Чтобы использовать собственные буферы для чтения файлов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b2ca3-116">To use your own buffers for file reading, perform the following steps.</span></span>

1.  <span data-ttu-id="b2ca3-117">Реализуйте обратный вызов или обратные вызовы, чтобы средство чтения вызывало, когда требуется буфер.</span><span class="sxs-lookup"><span data-stu-id="b2ca3-117">Implement a callback or callbacks for the reader to call when it needs a buffer.</span></span> <span data-ttu-id="b2ca3-118">При чтении выходных образцов используйте [**ивмреадераллокаторекс:: аллокатефораутпутекс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex).</span><span class="sxs-lookup"><span data-stu-id="b2ca3-118">If you are reading output samples, use [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex).</span></span> <span data-ttu-id="b2ca3-119">При чтении образцов потоков используйте [**ивмреадераллокаторекс:: аллокатефорстреамекс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span><span class="sxs-lookup"><span data-stu-id="b2ca3-119">If you are reading stream samples, use [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span></span> <span data-ttu-id="b2ca3-120">Включите любую логику для управления буферами, которые подходят для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="b2ca3-120">Include whatever logic for managing buffers that suits your application.</span></span>
2.  <span data-ttu-id="b2ca3-121">Выделите пул буферов, которые будут использоваться для чтения файлов.</span><span class="sxs-lookup"><span data-stu-id="b2ca3-121">Allocate a pool of buffers that you will use for file reading.</span></span>
    -   <span data-ttu-id="b2ca3-122">Определите размер, необходимый для буферов, вызвав [**ивмреадерадванцед:: жетмаксаутпутсамплесизе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) или [**Ивмреадерадванцед:: жетмаксстреамсамплесизе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) для каждого выхода и (или) потока, для которого используется буфер.</span><span class="sxs-lookup"><span data-stu-id="b2ca3-122">Find the size required for your buffers by calling [**IWMReaderAdvanced::GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) or [**IWMReaderAdvanced::GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) for each output and/or stream for which the buffer is used.</span></span> <span data-ttu-id="b2ca3-123">При использовании синхронного модуля чтения используйте вместо него [**ивмсинкреадер:: жетмаксаутпутсамплесизе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) или [**Ивмсинкреадер:: жетмаксстреамсамплесизе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) .</span><span class="sxs-lookup"><span data-stu-id="b2ca3-123">If using the synchronous reader, use [**IWMSyncReader::GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) or [**IWMSyncReader::GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) instead.</span></span>
    -   <span data-ttu-id="b2ca3-124">Создайте каждый буфер для пула.</span><span class="sxs-lookup"><span data-stu-id="b2ca3-124">Create each buffer for the pool.</span></span>
3.  <span data-ttu-id="b2ca3-125">Настройка модуля чтения или синхронного модуля чтения для чтения.</span><span class="sxs-lookup"><span data-stu-id="b2ca3-125">Set up the reader or synchronous reader for reading.</span></span> <span data-ttu-id="b2ca3-126">Дополнительные сведения см. в статье [чтение файлов с помощью асинхронного модуля чтения](reading-files-with-the-asynchronous-reader.md) или [чтение файлов с помощью синхронного модуля чтения](reading-files-with-the-synchronous-reader.md).</span><span class="sxs-lookup"><span data-stu-id="b2ca3-126">For more information see [Reading Files with the Asynchronous Reader](reading-files-with-the-asynchronous-reader.md) or [Reading Files with the Synchronous Reader](reading-files-with-the-synchronous-reader.md).</span></span>
4.  <span data-ttu-id="b2ca3-127">Прежде чем начать запись, вызовите [**ивмреадерадванцед:: сеталлокатефораутпут**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) или [**Ивмреадерадванцед:: сеталлокатефорстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) для каждого выхода и потока, для которого производится выделение буферов с помощью объекта Reader.</span><span class="sxs-lookup"><span data-stu-id="b2ca3-127">Before beginning writing, call [**IWMReaderAdvanced::SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) or [**IWMReaderAdvanced::SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) for each output and stream for which you are allocating buffers using the reader object.</span></span> <span data-ttu-id="b2ca3-128">Для синхронного модуля чтения вызовите метод [**IWMSyncReader2:: сеталлокатефораутпут**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) или [**IWMSyncReader2:: сеталлокатефорстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) .</span><span class="sxs-lookup"><span data-stu-id="b2ca3-128">For the synchronous reader, call [**IWMSyncReader2::SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) or [**IWMSyncReader2::SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) instead.</span></span>
5.  <span data-ttu-id="b2ca3-129">Начните чтение файла.</span><span class="sxs-lookup"><span data-stu-id="b2ca3-129">Begin reading the file.</span></span>

<span data-ttu-id="b2ca3-130">Объект чтения будет вызывать соответствующий обратный вызов распределителя и получать примеры из приложения.</span><span class="sxs-lookup"><span data-stu-id="b2ca3-130">The reading object will make calls to the appropriate allocator callback and get samples from your application.</span></span> <span data-ttu-id="b2ca3-131">Логика управления буфером должна включать способ сигнализации о том, что буфер может быть снова использован.</span><span class="sxs-lookup"><span data-stu-id="b2ca3-131">Your buffer management logic must include a way to signal that a buffer is free to be used again.</span></span> <span data-ttu-id="b2ca3-132">Как правило, буфер помещается обратно в пул, когда его содержимое готовится к просмотру.</span><span class="sxs-lookup"><span data-stu-id="b2ca3-132">Typically, a buffer is put back into the pool when its contents are rendered.</span></span> <span data-ttu-id="b2ca3-133">В зависимости от приложения может потребоваться всего несколько буферов в пуле или многие из них.</span><span class="sxs-lookup"><span data-stu-id="b2ca3-133">Depending upon your application, you may need just a few buffers in the pool or many.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2ca3-134">См. также</span><span class="sxs-lookup"><span data-stu-id="b2ca3-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2ca3-135">**Чтение файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="b2ca3-135">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




