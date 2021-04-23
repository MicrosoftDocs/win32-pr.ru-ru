---
title: Индексирование файла ASF
description: Индексирование файла ASF
ms.assetid: 33175444-365c-4b94-8b91-07198431062f
keywords:
- Windows Media Format SDK, индексирование файлов ASF
- Расширенный системный формат (ASF), индексирование файлов
- ASF (Расширенный системный формат), индексирование файлов
- индексы, индексирование файлов ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7206e1856abb9705e18e885ba06cb8253a93c84b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105681583"
---
# <a name="to-index-an-asf-file"></a><span data-ttu-id="4e55f-107">Индексирование файла ASF</span><span class="sxs-lookup"><span data-stu-id="4e55f-107">To Index an ASF File</span></span>

<span data-ttu-id="4e55f-108">Процесс индексирования ASF-файла очень прост.</span><span class="sxs-lookup"><span data-stu-id="4e55f-108">The process of indexing an ASF file is very simple.</span></span> <span data-ttu-id="4e55f-109">Выполните вызов [**ивминдексер:: startIndex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) и передайте имя файла.</span><span class="sxs-lookup"><span data-stu-id="4e55f-109">Make a call to [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) and pass the file name.</span></span> <span data-ttu-id="4e55f-110">Индексатор выполняет остальные.</span><span class="sxs-lookup"><span data-stu-id="4e55f-110">The indexer does the rest.</span></span> <span data-ttu-id="4e55f-111">Вызов **startIndex** является асинхронным, поэтому состояние должно отслеживаться с помощью обратного вызова **OnStatus** .</span><span class="sxs-lookup"><span data-stu-id="4e55f-111">The call to **StartIndexing** is asynchronous, so status must be monitored using the **OnStatus** callback.</span></span>

<span data-ttu-id="4e55f-112">В следующем коде показано, как индексировать ASF файл.</span><span class="sxs-lookup"><span data-stu-id="4e55f-112">The following code shows how to index an ASF file.</span></span> <span data-ttu-id="4e55f-113">Если необходимо настроить индексатор перед индексацией файла, необходимо включить код из примера, включенного в, [для настройки индексатора](to-configure-the-indexer.md).</span><span class="sxs-lookup"><span data-stu-id="4e55f-113">If you want to configure the indexer prior to indexing the file, you will need to include code from the example included in [To Configure the Indexer](to-configure-the-indexer.md).</span></span>

<span data-ttu-id="4e55f-114">В этом примере маркер, указывающий на событие, должен быть создан как глобальная переменная, поэтому он будет доступен для обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="4e55f-114">For this example, the handle that points to the event must be created as a global variable so it will be accessible by the callback.</span></span> <span data-ttu-id="4e55f-115">Следующее объявление должно отображаться в глобальной области видимости.</span><span class="sxs-lookup"><span data-stu-id="4e55f-115">The following declaration should appear in a global scope.</span></span>


```C++
HANDLE g_hEvent = NULL;

```



<span data-ttu-id="4e55f-116">В более реалистичном сценарии обработчик событий должен быть элементом данных класса, который содержит как обратный вызов, так и логику для запуска индексатора.</span><span class="sxs-lookup"><span data-stu-id="4e55f-116">In a more realistic scenario, the event handle should be a data member of the class that contains both the callback and the logic for starting the indexer.</span></span>

<span data-ttu-id="4e55f-117">Индексатор отправляет несколько событий обратному вызову **OnStatus** после вызова **Ивминдексер:: startIndex**.</span><span class="sxs-lookup"><span data-stu-id="4e55f-117">The indexer sends several events to the **OnStatus** callback after the call to **IWMIndexer::StartIndexing**.</span></span> <span data-ttu-id="4e55f-118">При необходимости их можно перехватить для приложения.</span><span class="sxs-lookup"><span data-stu-id="4e55f-118">You can trap them as needed for your application.</span></span> <span data-ttu-id="4e55f-119">Как минимум необходимо выполнить треппинг ВМТ \_ Closed, который отправляется после завершения индексирования.</span><span class="sxs-lookup"><span data-stu-id="4e55f-119">At a minimum, you need to trap WMT\_CLOSED, which is sent when indexing is complete.</span></span> <span data-ttu-id="4e55f-120">Используйте следующую логику в параметре message в реализации обратного вызова **OnStatus** .</span><span class="sxs-lookup"><span data-stu-id="4e55f-120">Use the following logic within the message switch in your implementation of the **OnStatus** callback.</span></span>


```C++
// Inside the status switch statement.
case WMT_CLOSED:
   // You may want to deal with the HRESULT value passed with the status.
   // If you do, you should do it here.

   // Signal the event.
   SetEvent(g_hEvent);
   break;

```



<span data-ttu-id="4e55f-121">В этом примере предполагается, что реализация обратного вызова **OnStatus** осуществляется через объект с именем микаллбакк.</span><span class="sxs-lookup"><span data-stu-id="4e55f-121">For this example it is assumed that your implementation of the **OnStatus** callback is accessed through an object called MyCallback.</span></span> <span data-ttu-id="4e55f-122">Дополнительные сведения об использовании событий и обратных вызовов с помощью этого пакета SDK см. [в разделе Использование методов обратного вызова](using-the-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="4e55f-122">For more information about using events and callbacks with this SDK, see [Using the Callback Methods](using-the-callback-methods.md).</span></span>


```C++
IWMIndexer* pMyIndexer     = NULL;
HRESULT     hr             = S_OK;
WCHAR       pwszFileName[] = L"C:\SomeFile.wmv";

// Initialize COM.
hr = CoInitialize(NULL);

// Create an event for asynchronous calls.
g_hEvent = CreateEvent(NULL, TRUE, FALSE, NULL);

// Create an indexer.
hr = WMCreateIndexer(&pMyIndexer);

// TODO: Configure the indexer if needed. See To Configure the Indexer.

// Start the indexer.
hr = pMyIndexer->StartIndexing(pwszFileName, &MyCallback, NULL);

// Wait for the indexer to finish.
WaitForSingleObject(g_hEvent, INFINITE);

// Clean up.
pMyIndexer->Release();
pMyIndexer = NULL

CloseHandle(g_hEvent);
g_hEvent = NULL;

```



## <a name="related-topics"></a><span data-ttu-id="4e55f-123">См. также</span><span class="sxs-lookup"><span data-stu-id="4e55f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e55f-124">**Интерфейс Ивминдексер**</span><span class="sxs-lookup"><span data-stu-id="4e55f-124">**IWMIndexer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[<span data-ttu-id="4e55f-125">**Настройка индексатора**</span><span class="sxs-lookup"><span data-stu-id="4e55f-125">**To Configure the Indexer**</span></span>](to-configure-the-indexer.md)
</dt> <dt>

[<span data-ttu-id="4e55f-126">**вмкреатеиндексер**</span><span class="sxs-lookup"><span data-stu-id="4e55f-126">**WMCreateIndexer**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[<span data-ttu-id="4e55f-127">**Работа с индексами**</span><span class="sxs-lookup"><span data-stu-id="4e55f-127">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




