---
description: Описывает, как отправить OM XPS на принтер в виде документа XPS.
ms.assetid: eb1068c4-6a6a-4ef2-8ed6-033a6a2c273b
title: Печать OM-объекта XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01ae1081c4f0c58c66efedc30406e310dd8dd9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080966"
---
# <a name="print-an-xps-om"></a><span data-ttu-id="d4ad4-103">Печать OM-объекта XPS</span><span class="sxs-lookup"><span data-stu-id="d4ad4-103">Print an XPS OM</span></span>

<span data-ttu-id="d4ad4-104">Описывает, как отправить OM XPS на принтер в виде документа XPS.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-104">Describes how to send an XPS OM to a printer as an XPS document.</span></span>

<span data-ttu-id="d4ad4-105">Инструкции по печати объектной модели XPS, содержащей полный документ XPS, см. в статье [Печать полной модели XPS](#print-a-complete-xps-om).</span><span class="sxs-lookup"><span data-stu-id="d4ad4-105">For instructions on how to print an XPS OM that contains a complete XPS document, see [Print a complete XPS OM](#print-a-complete-xps-om).</span></span> <span data-ttu-id="d4ad4-106">Чтобы включить документ XPS, в модели XPS должна содержаться список элементов, перечисленных в статье [Создание пустой модели XPS](create-a-blank-xps-om.md).</span><span class="sxs-lookup"><span data-stu-id="d4ad4-106">To contain an XPS document, an XPS OM must include the items listed in [Create a Blank XPS OM](create-a-blank-xps-om.md).</span></span>

<span data-ttu-id="d4ad4-107">Инструкции по печати объектной модели XPS, которая создается или обрабатывается по одной странице за раз, см. в разделе [добавочная печать объекта XPS](#incrementally-print-an-xps-om).</span><span class="sxs-lookup"><span data-stu-id="d4ad4-107">For instructions on how to print an XPS OM that is being created or processed one page at a time, see [Incrementally print an XPS OM](#incrementally-print-an-xps-om).</span></span>

<span data-ttu-id="d4ad4-108">Прежде чем использовать эти примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования документов XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="d4ad4-108">Before using these code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

<span data-ttu-id="d4ad4-109">В этом разделе вы узнаете, как выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="d4ad4-109">In this topic, you will learn how to perform the following tasks:</span></span>

-   [<span data-ttu-id="d4ad4-110">Печать полной модели XPS</span><span class="sxs-lookup"><span data-stu-id="d4ad4-110">Print a complete XPS OM</span></span>](#print-a-complete-xps-om)
-   [<span data-ttu-id="d4ad4-111">Добавочная печать объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="d4ad4-111">Incrementally print an XPS OM</span></span>](#incrementally-print-an-xps-om)
-   [<span data-ttu-id="d4ad4-112">См. также</span><span class="sxs-lookup"><span data-stu-id="d4ad4-112">Related topics</span></span>](#related-topics)

## <a name="print-a-complete-xps-om"></a><span data-ttu-id="d4ad4-113">Печать полной модели XPS</span><span class="sxs-lookup"><span data-stu-id="d4ad4-113">Print a complete XPS OM</span></span>

<span data-ttu-id="d4ad4-114">Когда OM XPS содержит полный XPS-документ, метод [**вритетостреам**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) интерфейса [**икспсомпаккаже**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) может отправить содержимое объектной модели XPS на принтер или в очередь печати.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-114">When an XPS OM contains a complete XPS document, the [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface can send the contents of the XPS OM to a printer or a print queue.</span></span>

<span data-ttu-id="d4ad4-115">Чтобы определить, когда задание печати завершено, создайте обработчик событий, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-115">To detect when the print job has completed, create an event handle as shown in the following example.</span></span>


```C++
    HANDLE completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



<span data-ttu-id="d4ad4-116">Чтобы распечатать полную модель XPS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-116">To print a complete XPS OM:</span></span>

1.  <span data-ttu-id="d4ad4-117">Создайте новый поток заданий печати, вызвав [**старткспспринтжоб**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span><span class="sxs-lookup"><span data-stu-id="d4ad4-117">Create a new print job stream by calling [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span></span>
2.  <span data-ttu-id="d4ad4-118">Отправьте содержимое объектной модели XPS в поток, вызвав метод [**вритетостреам**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) пакета.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-118">Send the contents of the XPS OM to the stream by calling the package's [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) method.</span></span>
3.  <span data-ttu-id="d4ad4-119">Закройте поток заданий печати, вызвав метод **Close** потока.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-119">Close the print job stream by calling the stream's **Close** method.</span></span>
4.  <span data-ttu-id="d4ad4-120">Дождитесь, пока задание печати сообщит о завершении.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-120">Wait for the print job to signal that it has completed.</span></span>
5.  <span data-ttu-id="d4ad4-121">Проверьте состояние завершения.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-121">Check the completion status.</span></span>
6.  <span data-ttu-id="d4ad4-122">Закройте и освободите ресурсы.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-122">Close and release resources.</span></span>


```C++
    IXpsPrintJob *job = NULL;
    IXpsPrintJobStream *jobStream = NULL;
    hr = StartXpsPrintJob(
                printerName,
                NULL,
                NULL,
                NULL,
                completionEvent,
                NULL,
                0,
                &job,
                &jobStream,
                NULL);

    // Write package to print job stream
    hr = package->WriteToStream (jobStream, FALSE);

    // Close the stream to tell the print job
    // that the entire document has been sent.
    hr = jobStream->Close();

    // Wait for the print job to finish spooling...
    if (NULL != completionEvent) {
        if (WaitForSingleObject(completionEvent, INFINITE) == WAIT_OBJECT_0)
        {
            // Get the print job status to see why the wait completed.
            //  Note that without waiting for a completion event, 
            //  the print job may not be complete when the status is queried.
            XPS_JOB_STATUS jobStatus;
            hr = job->GetJobStatus(&jobStatus);

            // Evaluate the job status returned.
            switch (jobStatus.completion)
            {
                case XPS_JOB_COMPLETED:
                    // The job completed as expected.
                    hr = S_OK;
                    break;
                case XPS_JOB_CANCELLED:
                    // The job was canceled.
                    hr = E_FAIL;
                    break;
                case XPS_JOB_FAILED:
                    // The job failed, 
                    // jobStatus.jobStatus has the reason.
                    hr = E_FAIL;
                    break;
                default:
                    // An unexpected value was returned.
                    hr = E_UNEXPECTED;
                    break;
            }
                
            // Release completion event handle
            CloseHandle(completionEvent);
        }
        else
        {    // there was a problem, set hr to error status
            hr  = HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // hr contains the result of the print operation

    CoUninitialize(); // if COM is no longer needed in this thread
```



## <a name="incrementally-print-an-xps-om"></a><span data-ttu-id="d4ad4-123">Добавочная печать объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="d4ad4-123">Incrementally print an XPS OM</span></span>

<span data-ttu-id="d4ad4-124">Вы можете постепенно отправить компоненты документа модели XPS в задание печати, создав поток заданий печати XPS, а затем передать отдельные компоненты документа в поток заданий печати по одному за раз.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-124">You can send the document components of an XPS OM to a printer job incrementally, by creating an XPS print job stream and then passing the individual document components to the print job stream, one at a time.</span></span> <span data-ttu-id="d4ad4-125">Последовательность, в которой отправляются компоненты документа, определяет, как они будут отображаться в готовом документе.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-125">The sequence in which the document components are sent determines how they will appear in the finished document.</span></span> <span data-ttu-id="d4ad4-126">Таким образом, прежде чем программа сможет вызвать код в этом примере, она должна правильно организовывать компоненты документа.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-126">Thus, before a program can call the code in this example, it must correctly organize the document components.</span></span>

<span data-ttu-id="d4ad4-127">Перед использованием интерфейсов OM в XPS инициализируйте COM в потоке, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-127">Before using XPS OM interfaces, initialize COM in the thread as shown in the following example code.</span></span>


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



<span data-ttu-id="d4ad4-128">Чтобы отслеживать завершение задания печати, создайте обработчик событий, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-128">To monitor the print job completion, create an event handle as shown in the following example code.</span></span>


```C++
    HANDLE completionEvent = NULL;
    completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



<span data-ttu-id="d4ad4-129">Создайте новый поток заданий печати и новый модуль записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-129">Create a new print job stream and a new package writer.</span></span> <span data-ttu-id="d4ad4-130">Передайте каждый из компонентов документа в соответствующие методы записи пакета в той же последовательности, в которой они будут отображаться в готовом документе.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-130">Pass each of the document components to the corresponding package writer methods in the same sequence as they will appear in the finished document.</span></span>

<span data-ttu-id="d4ad4-131">Запустите каждый документ New, а затем добавьте в него страницы.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-131">Start each document new, then add pages to it.</span></span> <span data-ttu-id="d4ad4-132">После передачи всех компонентов документа в поток заданий печати закройте поток, дождитесь завершения задания печати, а затем закройте и отпустите открытые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-132">After passing all document components to the print job stream, close the stream, wait for the print job to complete, and then close and release open resources.</span></span>

1.  <span data-ttu-id="d4ad4-133">Создайте новый поток заданий печати, вызвав [**старткспспринтжоб**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span><span class="sxs-lookup"><span data-stu-id="d4ad4-133">Create a new print job stream by calling [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span></span>
2.  <span data-ttu-id="d4ad4-134">Создайте URI части для части FixedDocumentSequence.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-134">Create a part URI for the FixedDocumentSequence part.</span></span>
3.  <span data-ttu-id="d4ad4-135">Создайте новый модуль записи пакетов в потоке задания печати.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-135">Create a new package writer on the print job stream.</span></span>
4.  <span data-ttu-id="d4ad4-136">Для каждого документа, который необходимо записать:</span><span class="sxs-lookup"><span data-stu-id="d4ad4-136">For each document to be written:</span></span>
    1.  <span data-ttu-id="d4ad4-137">Создайте новый универсальный код ресурса (URI) части для части FixedDocument.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-137">Create a new part URI for the FixedDocument part.</span></span>
    2.  <span data-ttu-id="d4ad4-138">Запустите новый документ в модуле записи пакета.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-138">Start a new document in the package writer.</span></span>
    3.  <span data-ttu-id="d4ad4-139">Для каждой страницы в текущем документе Создайте универсальный код ресурса (URI) части для элемента FixedPage и добавьте страницу в модуль записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-139">For each page in the current document, create a part URI for the FixedPage part and add the page to the package writer.</span></span>
5.  <span data-ttu-id="d4ad4-140">После добавления всех страниц в модуль записи пакетов закройте его.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-140">After all pages have been added to the package writer, close it.</span></span>
6.  <span data-ttu-id="d4ad4-141">Закройте поток заданий печати.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-141">Close the print job stream.</span></span>
7.  <span data-ttu-id="d4ad4-142">Дождитесь завершения задания печати.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-142">Wait for the print job to complete.</span></span>
8.  <span data-ttu-id="d4ad4-143">Проверьте состояние завершения.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-143">Check the completion status.</span></span>
9.  <span data-ttu-id="d4ad4-144">Закройте и выпустите открытые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-144">Close and release open resources.</span></span>


```C++
    IXpsPrintJob* job = NULL;
    IXpsPrintJobStream* jobStream = NULL;
    hr = StartXpsPrintJob(
                argv[1],
                NULL,
                NULL,
                NULL,
                completionEvent,
                NULL,
                0,
                &job,
                &jobStream,
                NULL);

    // Note the implicit requirement that CoInitializeEx 
    //  has previously been called from this thread.
    IXpsOMObjectFactory *xpsFactory = NULL;
    hr = CoCreateInstance(
                __uuidof(XpsOMObjectFactory),
                NULL,
                CLSCTX_INPROC_SERVER,
                __uuidof(IXpsOMObjectFactory),
                reinterpret_cast<void**>(&xpsFactory)
                );
    // Create part URI for FixedDocumentSequence part
    //  This can use a static string because there is only one
    //  FixedDocumentSequence part in the print job.
    IOpcPartUri *partUri = NULL;
    hr = xpsFactory->CreatePartUri(L"/FixedDocumentSequence.fdseq", &partUri);

    // Create the package writer on the print job stream
    //  Note that the interleaving parameter set to 
    //  XPS_INTERLEAVING_ON, the package writer will create
    //  empty print ticket parts when a NULL pointer is
    //  passed in the print ticket argument of this method,
    //  the StartNewDocument method, and the AddPage method.
    //  For more information, see the help for these methods.
    IXpsOMPackageWriter *packageWriter = NULL;
    hr = xpsFactory->CreatePackageWriterOnStream(
            jobStream,
            TRUE,
            XPS_INTERLEAVING_ON, // to create blank print ticket objects
            partUri,
            NULL,
            NULL,
            NULL,
            NULL,
            &packageWriter);
    // release partUri after it's been used to create new doc. seq.
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }

    // Add document content to the print job stream.
    int docNumber = 1;
    int docsInPackage = 1; // Change this value as required.
    while (docNumber <= docsInPackage) {

        // Create a unique part URI for the current document.
        WCHAR DocPartUri[MAX_PATH];
        hr = MakeDocumentPartUri (docNumber, MAX_PATH, DocPartUri);
        hr = xpsFactory->CreatePartUri(DocPartUri, &partUri);
        
        // Initialize the new document in the package writer.
        hr = packageWriter->StartNewDocument(partUri, NULL, NULL, NULL, NULL);

        // release part URI after it's been used to create new doc.
        if (partUri)
        {
            partUri->Release();
            partUri = NULL;
        }

        // Add the pages
        int pageNumber = 1;
        int pagesInDocument = 1; // Change this value as required.
        while (pageNumber <= pagesInDocument) {

            // Create a unique part URI for the current page
            WCHAR PagePartUri[MAX_PATH];
            hr = MakePagePartUri (
                docNumber, 
                pageNumber, 
                MAX_PATH, 
                PagePartUri);
            hr = xpsFactory->CreatePartUri(PagePartUri, &partUri);

            // create page in OM
            XPS_SIZE pageSize = {816, 1056};
            IXpsOMPage *xpsPage = NULL;
            hr = xpsFactory->CreatePage(
                &pageSize, 
                L"en-US", 
                partUri, 
                &xpsPage);

            // release pagePartUri after it's been used to create the page
            if (partUri)
            {
                partUri->Release();
                partUri = NULL;
            }

            // add content to the page or retrieve 
            //  the page from the XPS OM.
            //  (not shown in this example)

            // add page to document
            hr = packageWriter->AddPage(
                        xpsPage,
                        &pageSize,
                        NULL,
                        NULL,
                        NULL,
                        NULL);

             if (xpsPage)
              {
                 xpsPage->Release();
                 xpsPage = NULL;
             }

            // go to the next page
            pageNumber++;
        }
        // the fixed document does not need to be closed.
        // it will be closed when a new fixed doc is opened
        // or the package is closed.

        // go to the next document
        docNumber++;
    }

    // Close the package writer when finished
    hr = packageWriter->Close();

    if (SUCCEEDED(hr))
    {
        // Close the print stream to tell the print
        //  job that the all document contents have
        //  been sent
        hr = jobStream->Close();
        // Wait for the print job to finish spooling...
        if (NULL != completionEvent) {
            if (WaitForSingleObject(completionEvent, INFINITE) == WAIT_OBJECT_0)
            {
                // Get the print job status to see why the wait completed.
                //  Note that without waiting for a completion event, 
                //  the print job may not be complete when the status is queried.
                XPS_JOB_STATUS jobStatus;
                hr = job->GetJobStatus(&jobStatus);

                // Evaluate the job status returned.
                switch (jobStatus.completion)
                {
                    case XPS_JOB_COMPLETED:
                        // The job completed as expected.
                        hr = S_OK;
                        break;
                    case XPS_JOB_CANCELLED:
                        // The job was canceled.
                        hr = E_FAIL;
                        break;
                    case XPS_JOB_FAILED:
                        // The job failed, 
                        // jobStatus.jobStatus has the reason.
                        hr = E_FAIL;
                        break;
                    default:
                        // An unexpected value was returned.
                        hr = E_UNEXPECTED;
                        break;
                }
                    
                // Release completion event handle
                CloseHandle(completionEvent);
            }
            else
            {    // there was a problem, set hr to error status
                hr  = HRESULT_FROM_WIN32(GetLastError());
            }
        }
    } 
    else
    {
        // cancel the job, if one exists, because
        //  the close call returned an error
        if (job) job->Cancel();
    }
    // hr contains the result of the print operation

    // free/release pointers and handles used.

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

    CoUninitialize(); // If done with COM in this thread.
```



<span data-ttu-id="d4ad4-145">Когда программа записывает компоненты документа постепенно, как показано в этом примере, он должен создать имена частей для каждой части документа, которая отправляется в поток заданий печати.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-145">When the program is writing the document components incrementally, as shown in this example, it must generate the part names for each document part that it sends to the print job stream.</span></span> <span data-ttu-id="d4ad4-146">В предыдущем примере URI части FixedDocumentSequence создается из статической строки, так как в документе XPS есть одна и только одна такая часть.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-146">In the preceding example, the FixedDocumentSequence part URI is created from a static string because there is one and only one such part in the XPS document.</span></span> <span data-ttu-id="d4ad4-147">URI каждой части FixedPage и FixedDocument должны быть уникальными в пределах документа XPS.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-147">The URI of each FixedPage and FixedDocument part must be unique within the XPS document.</span></span> <span data-ttu-id="d4ad4-148">Создание универсального кода ресурса (URI) части с помощью индекса этих компонентов может обеспечить уникальность результирующей строки URI в документе XPS.</span><span class="sxs-lookup"><span data-stu-id="d4ad4-148">Building the part URI by using the index of these components can help ensure that the resulting URI string is unique within the XPS document.</span></span>


```C++
HRESULT MakeDocumentPartUri (
                              __in int docNumber,
                              __in DWORD partUriStringLength,
                              __inout LPWSTR partUriStringBuffer
                              )
{
    // create a Part URI string using the document number
    //  that was passed as an argument
    // for example, "/Documents/1/FixedDocument.fdoc"
    //  where "1" specifies the document number, which would
    //  change with each document printed
    return S_OK;
}
 
HRESULT MakePagePartUri (
                              __in int docNumber,
                              __in int pageNumber,
                              __in DWORD partUriStringLength,
                              __inout LPWSTR partUriStringBuffer
                              )
{
    // create a Part URI string using the document number
    //   and page number that were passed as an argument
    // for example: "/Documents/1/Pages/1.fpage"
    //  where the first "1" between Documents and Pages 
    //  specifies the document number, which would change with
    //  each document. The second "1" specifies the page number,
    //  which would change with each page in the document.
    return S_OK;
}
```



<span data-ttu-id="d4ad4-149">Дополнительные сведения о структуре документа XPS см. в [спецификации XML Paper](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span><span class="sxs-lookup"><span data-stu-id="d4ad4-149">For more information on the structure of an XPS document, see the [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4ad4-150">См. также</span><span class="sxs-lookup"><span data-stu-id="d4ad4-150">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d4ad4-151">**Следующие шаги**</span><span class="sxs-lookup"><span data-stu-id="d4ad4-151">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="d4ad4-152">Запись объектной модели XPS в документ XPS</span><span class="sxs-lookup"><span data-stu-id="d4ad4-152">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

<span data-ttu-id="d4ad4-153">**Используется в этом разделе**</span><span class="sxs-lookup"><span data-stu-id="d4ad4-153">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="d4ad4-154">**CoInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="d4ad4-154">**CoInitializeEx**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
</dt> <dt>

[<span data-ttu-id="d4ad4-155">**CreateEvent**</span><span class="sxs-lookup"><span data-stu-id="d4ad4-155">**CreateEvent**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="d4ad4-156">**иопкпартури**</span><span class="sxs-lookup"><span data-stu-id="d4ad4-156">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="d4ad4-157">**икспсомпаккаже**</span><span class="sxs-lookup"><span data-stu-id="d4ad4-157">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="d4ad4-158">**икспсомпаккажевритер**</span><span class="sxs-lookup"><span data-stu-id="d4ad4-158">**IXpsOMPackageWriter**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[<span data-ttu-id="d4ad4-159">**икспспринтжоб**</span><span class="sxs-lookup"><span data-stu-id="d4ad4-159">**IXpsPrintJob**</span></span>](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjob)
</dt> <dt>

[<span data-ttu-id="d4ad4-160">**икспспринтжобстреам**</span><span class="sxs-lookup"><span data-stu-id="d4ad4-160">**IXpsPrintJobStream**</span></span>](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjobstream)
</dt> <dt>

[<span data-ttu-id="d4ad4-161">**старткспспринтжоб**</span><span class="sxs-lookup"><span data-stu-id="d4ad4-161">**StartXpsPrintJob**</span></span>](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)
</dt> <dt>

[<span data-ttu-id="d4ad4-162">**WaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="d4ad4-162">**WaitForSingleObject**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)
</dt> <dt>

<span data-ttu-id="d4ad4-163">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="d4ad4-163">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="d4ad4-164">Инициализация объектной модели XPS</span><span class="sxs-lookup"><span data-stu-id="d4ad4-164">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="d4ad4-165">Справочник по API документов XPS</span><span class="sxs-lookup"><span data-stu-id="d4ad4-165">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="d4ad4-166">XPS</span><span class="sxs-lookup"><span data-stu-id="d4ad4-166">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
