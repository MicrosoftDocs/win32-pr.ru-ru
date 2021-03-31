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
# <a name="how-to-print-with-the-xps-print-api"></a>Практические руководства. печать с помощью API печати XPS

В этом разделе описывается, как использовать [API печати XPS](xpsprint-api.md) для печати из приложения Windows.

[API печати XPS](xpsprint-api.md) позволяет собственным приложениям Windows печатать XPS-документы. Приложение может создать документ XPS с помощью [API документа XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)). В разделе " [Общие задачи программирования документов XPS](/previous-versions/windows/desktop/dd316968(v=vs.85)) " описывается, как это сделать. После создания документа XPS приложение может использовать API печати XPS для его печати.

Использование [API печати XPS](xpsprint-api.md) для печати документа из приложения включает следующие шаги.

-   [Инициализация COM-интерфейса](#initialize-com-interface)
-   [Создание события завершения](#create-a-completion-event)
-   [Запуск задания печати XPS](#start-an-xps-print-job)
-   [Создание интерфейса Икспсомпаккажевритер](#create-an-ixpsompackagewriter-interface)
-   [Закрытие интерфейса Икспсомпаккажевритер](#close-the-ixpsompackagewriter-interface)
-   [Закрытие потока заданий печати](#close-the-print-job-stream)
-   [Ожидание события завершения](#wait-for-the-completion-event)
-   [Высвобождение ресурсов](#release-resources)

Для печати [API печати XPS](xpsprint-api.md) требуется документ XPS. В следующем примере создается документ XPS, так как он отправляется на принтер с помощью API печати XPS. Кроме того, можно создать документ XPS, не отправляя его на принтер с помощью [API документа XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) и сохранив его как XPS-объект или СОХРАНИВ объект XPS в виде XPS-документа. Дополнительные сведения об использовании объектной модели XPS см. в разделе API документа XPS.

### <a name="initialize-com-interface"></a>Инициализация COM-интерфейса

Инициализируйте COM-интерфейс, если приложение еще не сделали этого.


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



### <a name="create-a-completion-event"></a>Создание события завершения

Создайте событие завершения, которое [API печати XPS](xpsprint-api.md) использует для уведомления приложения, когда диспетчер очереди печати получает весь документ из приложения. API печати XPS также поддерживает событие хода выполнения, поэтому приложение может узнать о других действиях с буферизацией.


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



### <a name="start-an-xps-print-job"></a>Запуск задания печати XPS

Запустите задание печати XPS, вызвав [**старткспспринтжоб**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob). **Старткспспринтжоб** возвращает поток, в который приложение будет отсылать документ для печати.


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



### <a name="create-an-ixpsompackagewriter-interface"></a>Создание интерфейса Икспсомпаккажевритер

Создайте интерфейс [**икспсомпаккажевритер**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) , вызвав [**Икспсомобжектфактори:: креатепаккажевритеронстреам**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream) в потоке, возвращенном [**старткспспринтжоб**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).


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



Для каждого документа в этом задании печати запустите новый документ, а затем добавьте в него страницы.

### <a name="start-a-new-document"></a>Начать новый документ

Запустите новый документ в модуле записи пакета, вызвав [**икспсомпаккажевритер:: стартневдокумент**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument). Если документ открыт при вызове этого метода, он закрывается и открывается новый документ.


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



### <a name="add-a-page"></a>Добавление страницы

Вызовите метод [**икспсомпаккажевритер:: addPage**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) , чтобы записать все страницы документа из приложения в новый документ в средстве записи пакета.

> [!Note]  
> Предполагается, что приложение создало страницу перед этим шагом. Дополнительные сведения о создании страниц документов и добавлении в них содержимого см. в разделе [Общие задачи программирования документов XPS](/previous-versions/windows/desktop/dd316968(v=vs.85)).

 


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



### <a name="close-the-ixpsompackagewriter-interface"></a>Закрытие интерфейса Икспсомпаккажевритер

После того как все документы будут записаны для этого задания печати, вызовите метод [**икспсомпаккажевритер:: Close**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close) , чтобы закрыть пакет.


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



### <a name="close-the-print-job-stream"></a>Закрытие потока заданий печати

Закройте поток заданий печати, вызвав [**Close**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjobstream-close), который сообщает диспетчеру очереди печати, что приложение отправляет все задания печати.


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



### <a name="wait-for-the-completion-event"></a>Ожидание события завершения

Дождитесь события завершения задания печати.


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



После получения сигнала о событии завершения вызовите [**жетжобстатус**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjob-getjobstatus) , чтобы получить состояние задания.


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



### <a name="release-resources"></a>Высвобождение ресурсов

После того как состояние задания указывает на завершение, освободите интерфейсы и ресурсы, используемые для этого задания печати.


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



 

 
