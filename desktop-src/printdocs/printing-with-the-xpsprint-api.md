---
description: В этом разделе описывается, как использовать API печати XPS для печати из приложения Windows.
ms.assetid: 3d7ab169-412c-434f-a865-4da4af370eaf
title: Практические руководства. печать с помощью API печати XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4be5f083fb31eccaf2dc4b555435bd15a7fb45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912155"
---
# <a name="how-to-print-with-the-xps-print-api"></a><span data-ttu-id="f6e5b-103">Практические руководства. печать с помощью API печати XPS</span><span class="sxs-lookup"><span data-stu-id="f6e5b-103">How To: Print with the XPS Print API</span></span>

<span data-ttu-id="f6e5b-104">В этом разделе описывается, как использовать [API печати XPS](xpsprint-api.md) для печати из приложения Windows.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-104">This topic describes how to use the [XPS Print API](xpsprint-api.md) to print from a Windows application.</span></span>

<span data-ttu-id="f6e5b-105">[API печати XPS](xpsprint-api.md) позволяет собственным приложениям Windows печатать XPS-документы.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-105">The [XPS Print API](xpsprint-api.md) enables native Windows applications to print XPS documents.</span></span> <span data-ttu-id="f6e5b-106">Приложение может создать документ XPS с помощью [API документа XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f6e5b-106">An application can create an XPS document by using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span></span> <span data-ttu-id="f6e5b-107">В разделе " [Общие задачи программирования документов XPS](/previous-versions/windows/desktop/dd316968(v=vs.85)) " описывается, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-107">The [Common XPS Document Programming Tasks](/previous-versions/windows/desktop/dd316968(v=vs.85)) help topic describes how to do this.</span></span> <span data-ttu-id="f6e5b-108">После создания документа XPS приложение может использовать API печати XPS для его печати.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-108">Once an XPS document has been created, the application can use the XPS Print API to print it.</span></span>

<span data-ttu-id="f6e5b-109">Использование [API печати XPS](xpsprint-api.md) для печати документа из приложения включает следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-109">Using the [XPS Print API](xpsprint-api.md) to print a document from an application involves the following steps.</span></span>

-   [<span data-ttu-id="f6e5b-110">Инициализация COM-интерфейса</span><span class="sxs-lookup"><span data-stu-id="f6e5b-110">Initialize COM Interface</span></span>](#initialize-com-interface)
-   [<span data-ttu-id="f6e5b-111">Создание события завершения</span><span class="sxs-lookup"><span data-stu-id="f6e5b-111">Create a Completion Event</span></span>](#create-a-completion-event)
-   [<span data-ttu-id="f6e5b-112">Запуск задания печати XPS</span><span class="sxs-lookup"><span data-stu-id="f6e5b-112">Start an XPS Print Job</span></span>](#start-an-xps-print-job)
-   [<span data-ttu-id="f6e5b-113">Создание интерфейса Икспсомпаккажевритер</span><span class="sxs-lookup"><span data-stu-id="f6e5b-113">Create an IXpsOMPackageWriter Interface</span></span>](#create-an-ixpsompackagewriter-interface)
-   [<span data-ttu-id="f6e5b-114">Закрытие интерфейса Икспсомпаккажевритер</span><span class="sxs-lookup"><span data-stu-id="f6e5b-114">Close the IXpsOMPackageWriter Interface</span></span>](#close-the-ixpsompackagewriter-interface)
-   [<span data-ttu-id="f6e5b-115">Закрытие потока заданий печати</span><span class="sxs-lookup"><span data-stu-id="f6e5b-115">Close the Print Job Stream</span></span>](#close-the-print-job-stream)
-   [<span data-ttu-id="f6e5b-116">Ожидание события завершения</span><span class="sxs-lookup"><span data-stu-id="f6e5b-116">Wait for the Completion Event</span></span>](#wait-for-the-completion-event)
-   [<span data-ttu-id="f6e5b-117">Высвобождение ресурсов</span><span class="sxs-lookup"><span data-stu-id="f6e5b-117">Release Resources</span></span>](#release-resources)

<span data-ttu-id="f6e5b-118">Для печати [API печати XPS](xpsprint-api.md) требуется документ XPS.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-118">The [XPS Print API](xpsprint-api.md) requires an XPS document to print.</span></span> <span data-ttu-id="f6e5b-119">В следующем примере создается документ XPS, так как он отправляется на принтер с помощью API печати XPS.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-119">In the following example, the XPS document is created as it is sent to the printer by the XPS Print API.</span></span> <span data-ttu-id="f6e5b-120">Кроме того, можно создать документ XPS, не отправляя его на принтер с помощью [API документа XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) и сохранив его как XPS-объект или СОХРАНИВ объект XPS в виде XPS-документа.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-120">It is also possible to create an XPS document without sending it to a printer by using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) and maintaining it as an XPS OM or by saving the XPS OM as an XPS document.</span></span> <span data-ttu-id="f6e5b-121">Дополнительные сведения об использовании объектной модели XPS см. в разделе API документа XPS.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-121">For more information about using an XPS OM, see the XPS Document API.</span></span>

### <a name="initialize-com-interface"></a><span data-ttu-id="f6e5b-122">Инициализация COM-интерфейса</span><span class="sxs-lookup"><span data-stu-id="f6e5b-122">Initialize COM Interface</span></span>

<span data-ttu-id="f6e5b-123">Инициализируйте COM-интерфейс, если приложение еще не сделали этого.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-123">Initialize the COM interface, if the application has not already done so.</span></span>


```C++
    // Initialize the COM interface, if the application has not 
    //  already done so.
    if (FAILED(hr = CoInitializeEx(0, COINIT_MULTITHREADED)))
    {
        fwprintf(stderr, 
            L"ERROR: CoInitializeEx failed with HRESULT 0x%X\n", hr);
        return 1;
    }
```



### <a name="create-a-completion-event"></a><span data-ttu-id="f6e5b-124">Создание события завершения</span><span class="sxs-lookup"><span data-stu-id="f6e5b-124">Create a Completion Event</span></span>

<span data-ttu-id="f6e5b-125">Создайте событие завершения, которое [API печати XPS](xpsprint-api.md) использует для уведомления приложения, когда диспетчер очереди печати получает весь документ из приложения.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-125">Create a completion event, which the [XPS Print API](xpsprint-api.md) uses to notify the application when the print spooler has received the entire document from the application.</span></span> <span data-ttu-id="f6e5b-126">API печати XPS также поддерживает событие хода выполнения, поэтому приложение может узнать о других действиях с буферизацией.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-126">The XPS Print API also supports a progress event so an application can know about other spooling activity.</span></span>


```C++
        // Create the completion event
        completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
        if (!completionEvent)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            fwprintf(stderr, 
                L"ERROR: Could not create completion event: %08X\n", hr);
        }
```



### <a name="start-an-xps-print-job"></a><span data-ttu-id="f6e5b-127">Запуск задания печати XPS</span><span class="sxs-lookup"><span data-stu-id="f6e5b-127">Start an XPS Print Job</span></span>

<span data-ttu-id="f6e5b-128">Запустите задание печати XPS, вызвав [**старткспспринтжоб**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).</span><span class="sxs-lookup"><span data-stu-id="f6e5b-128">Start an XPS print job by calling [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).</span></span> <span data-ttu-id="f6e5b-129">**Старткспспринтжоб** возвращает поток, в который приложение будет отсылать документ для печати.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-129">**StartXpsPrintJob** returns a stream into which the application will send the document to be printed.</span></span>


```C++
        // Start an XPS Print Job
        if (FAILED(hr = StartXpsPrintJob(
                    printerName,
                    NULL,
                    NULL,
                    NULL,
                    completionEvent,
                    NULL,
                    0,
                    &job,
                    &jobStream,
                    NULL
                    )))
        {
            fwprintf(stderr, 
                L"ERROR: Could not start XPS print job: %08X\n", hr);
        }
```



### <a name="create-an-ixpsompackagewriter-interface"></a><span data-ttu-id="f6e5b-130">Создание интерфейса Икспсомпаккажевритер</span><span class="sxs-lookup"><span data-stu-id="f6e5b-130">Create an IXpsOMPackageWriter Interface</span></span>

<span data-ttu-id="f6e5b-131">Создайте интерфейс [**икспсомпаккажевритер**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) , вызвав [**Икспсомобжектфактори:: креатепаккажевритеронстреам**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream) в потоке, возвращенном [**старткспспринтжоб**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).</span><span class="sxs-lookup"><span data-stu-id="f6e5b-131">Create an [**IXpsOMPackageWriter**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface by calling [**IXpsOMObjectFactory::CreatePackageWriterOnStream**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream) on the stream returned by [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).</span></span>


```C++
    // Create an XPS OM Object Factory. If one has already been 
    //  created by the application, a new one is not necessary.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = CoCreateInstance(
                __uuidof(XpsOMObjectFactory), 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&xpsFactory))))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create XPS OM Object Factory: %08X\n", 
                hr);
        }
    }
    // Create the Part URI for the Fixed Document Sequence. The
    //  Fixed Document Sequence is the top-level element in the
    //  package hierarchy of objects. There is one Fixed Document
    //  Sequence in an XPS document.
    //
    // The part name is not specified by the XML Paper Specification,
    //  however, the name used in this example is the part name
    //  used by convention.
    //
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePartUri(
                    L"/FixedDocumentSequence.fdseq", 
                    &partUri)))
        {
            fwprintf(stderr, 
                L"ERROR: Could not create part URI: %08X\n", hr);
        }
    }

    // Create the package writer on the print job stream.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePackageWriterOnStream(
                    jobStream,
                    TRUE,
                    XPS_INTERLEAVING_ON,
                    partUri,
                    NULL,
                    NULL,
                    NULL,
                    NULL,
                    &packageWriter
                    )
                )
           )
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create package writer: 0x%X\n", 
                hr);
        }
    }

    // Release the part URI interface.
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }
```



<span data-ttu-id="f6e5b-132">Для каждого документа в этом задании печати запустите новый документ, а затем добавьте в него страницы.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-132">For each document in this print job, start a new document and then add pages to that document.</span></span>

### <a name="start-a-new-document"></a><span data-ttu-id="f6e5b-133">Начать новый документ</span><span class="sxs-lookup"><span data-stu-id="f6e5b-133">Start a New Document</span></span>

<span data-ttu-id="f6e5b-134">Запустите новый документ в модуле записи пакета, вызвав [**икспсомпаккажевритер:: стартневдокумент**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).</span><span class="sxs-lookup"><span data-stu-id="f6e5b-134">Start a new document in the package writer by calling [**IXpsOMPackageWriter::StartNewDocument**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).</span></span> <span data-ttu-id="f6e5b-135">Если документ открыт при вызове этого метода, он закрывается и открывается новый документ.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-135">If a document is open when this method is called, it is closed and a new document is opened.</span></span>


```C++
    // Create the Part URI for the Fixed Document. The
    //  Fixed Document part contains the pages of the document. 
    //  There can be one or more Fixed Documents in an XPS document.
    //
    // The part name is not specified by the XML Paper Specification,
    //  however, the name format used in this example is the format 
    //  used by convention. The number "1" in this example must be 
    //  changed for each document in the package. For example, 1 
    //  for the first document, 2 for the second, and so on.
    //

    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePartUri(
                    L"/Documents/1/FixedDocument.fdoc", 
                    &partUri)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create part URI: %08X\n", 
                hr);
        }
    }

    // Start the new document.
    //
    //  If there was already a document started in this page,
    //  this call will close it and start a new one.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = packageWriter->StartNewDocument(
                    partUri, 
                    NULL, 
                    NULL, 
                    NULL,
                    NULL)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not start new document: 0x%X\n", 
                hr);
        }
    }
    
    // Release the part URI interface
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }
```



### <a name="add-a-page"></a><span data-ttu-id="f6e5b-136">Добавление страницы</span><span class="sxs-lookup"><span data-stu-id="f6e5b-136">Add a Page</span></span>

<span data-ttu-id="f6e5b-137">Вызовите метод [**икспсомпаккажевритер:: addPage**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) , чтобы записать все страницы документа из приложения в новый документ в средстве записи пакета.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-137">Call [**IXpsOMPackageWriter::AddPage**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) to write each of the document's pages from the application to the new document in the package writer.</span></span>

> [!Note]  
> <span data-ttu-id="f6e5b-138">Предполагается, что приложение создало страницу перед этим шагом.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-138">The application is assumed to have created the page prior to this step.</span></span> <span data-ttu-id="f6e5b-139">Дополнительные сведения о создании страниц документов и добавлении в них содержимого см. в разделе [Общие задачи программирования документов XPS](/previous-versions/windows/desktop/dd316968(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f6e5b-139">For more information about creating document pages and adding content to them, see the [Common XPS Document Programming Tasks](/previous-versions/windows/desktop/dd316968(v=vs.85)).</span></span>

 


```C++
    if (SUCCEEDED(hr))
    {
        // Add the current page to the document.
        if (FAILED(hr = packageWriter->AddPage(
                    xpsPage,
                    &pageSize,
                    NULL,
                    NULL,
                    NULL,
                    NULL
                    )))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not add page to document: %08X\n", 
                hr);
        }
    }
```



### <a name="close-the-ixpsompackagewriter-interface"></a><span data-ttu-id="f6e5b-140">Закрытие интерфейса Икспсомпаккажевритер</span><span class="sxs-lookup"><span data-stu-id="f6e5b-140">Close the IXpsOMPackageWriter Interface</span></span>

<span data-ttu-id="f6e5b-141">После того как все документы будут записаны для этого задания печати, вызовите метод [**икспсомпаккажевритер:: Close**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close) , чтобы закрыть пакет.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-141">After all the documents have been written for this print job, call [**IXpsOMPackageWriter::Close**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close) to close the package.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = packageWriter->Close()))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not close package writer: %08X\n", 
                hr);
        }
    }
```



### <a name="close-the-print-job-stream"></a><span data-ttu-id="f6e5b-142">Закрытие потока заданий печати</span><span class="sxs-lookup"><span data-stu-id="f6e5b-142">Close the Print Job Stream</span></span>

<span data-ttu-id="f6e5b-143">Закройте поток заданий печати, вызвав [**Close**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjobstream-close), который сообщает диспетчеру очереди печати, что приложение отправляет все задания печати.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-143">Close the print job stream by calling [**Close**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjobstream-close), which tells the print spooler that the entire print job has been sent by the application.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = jobStream->Close()))
        {
            fwprintf(
                stderr,
                L"ERROR: Could not close job stream: %08X\n",
                hr);
        }
    }
    else
    {
        // Only cancel the job if we succeeded in creating a job.
        if (job)
        {
            // Tell the XPS Print API that we're giving up.  
            //  Don't overwrite hr with the return from this function.
            job->Cancel();
        }
    }
```



### <a name="wait-for-the-completion-event"></a><span data-ttu-id="f6e5b-144">Ожидание события завершения</span><span class="sxs-lookup"><span data-stu-id="f6e5b-144">Wait for the Completion Event</span></span>

<span data-ttu-id="f6e5b-145">Дождитесь события завершения задания печати.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-145">Wait for the print job's completion event.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        wprintf(L"Waiting for job completion...\n");

        if (WaitForSingleObject(completionEvent, INFINITE) != 
                                                    WAIT_OBJECT_0)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            fwprintf(
                stderr, 
                L"ERROR: Wait for completion event failed: %08X\n", 
                hr);
        }
    }
```



<span data-ttu-id="f6e5b-146">После получения сигнала о событии завершения вызовите [**жетжобстатус**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjob-getjobstatus) , чтобы получить состояние задания.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-146">After the completion event is signaled, call [**GetJobStatus**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjob-getjobstatus) to get the job status.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = job->GetJobStatus(&jobStatus)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not get job status: %08X\n", 
                hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        switch (jobStatus.completion)
        {
            case XPS_JOB_COMPLETED:
                break;
            case XPS_JOB_CANCELLED:
                fwprintf(stderr, L"ERROR: job was cancelled\n");
                hr = E_FAIL;
                break;
            case XPS_JOB_FAILED:
                fwprintf(
                    stderr, 
                    L"ERROR: Print job failed: %08X\n", 
                    jobStatus.jobStatus);
                hr = E_FAIL;
                break;
            default:
                fwprintf(stderr, L"ERROR: unexpected failure\n");
                hr = E_UNEXPECTED;
                break;
        }
    }
```



### <a name="release-resources"></a><span data-ttu-id="f6e5b-147">Высвобождение ресурсов</span><span class="sxs-lookup"><span data-stu-id="f6e5b-147">Release Resources</span></span>

<span data-ttu-id="f6e5b-148">После того как состояние задания указывает на завершение, освободите интерфейсы и ресурсы, используемые для этого задания печати.</span><span class="sxs-lookup"><span data-stu-id="f6e5b-148">After a job status indicates completion, release the interfaces and resources used for this print job.</span></span>


```C++
    if (packageWriter)
    {
        packageWriter->Release();
        packageWriter = NULL;
    }

    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }

    if (xpsFactory)
    {
        xpsFactory->Release();
        xpsFactory = NULL;
    }

    if (jobStream)
    {
        jobStream->Release();
        jobStream = NULL;
    }

    if (job)
    {
        job->Release();
        job = NULL;
    }

    if (completionEvent)
    {
        CloseHandle(completionEvent);
        completionEvent = NULL;
    }
```



 

 
