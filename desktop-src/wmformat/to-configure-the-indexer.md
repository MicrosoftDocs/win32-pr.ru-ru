---
title: Настройка индексатора
description: Настройка индексатора
ms.assetid: 0e28e8dd-1586-45e6-8a08-5245d465d068
keywords:
- Пакет SDK для Windows Media Format, Настройка индексаторов
- Расширенный системный формат (ASF), Настройка индексаторов
- ASF (Расширенный системный формат), Настройка индексаторов
- индексы, Настройка индексаторов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618316e22b13ca05ff0fc1bbfb6b4583e79ca858
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412543"
---
# <a name="to-configure-the-indexer"></a><span data-ttu-id="45687-107">Настройка индексатора</span><span class="sxs-lookup"><span data-stu-id="45687-107">To Configure the Indexer</span></span>

<span data-ttu-id="45687-108">Вы можете настроить индексатор перед его использованием для индексирования файла ASF.</span><span class="sxs-lookup"><span data-stu-id="45687-108">You can configure the indexer before using it to index an ASF file.</span></span> <span data-ttu-id="45687-109">Каждый поток в файле может быть настроен отдельно или же можно задать одинаковую конфигурацию для всех потоков.</span><span class="sxs-lookup"><span data-stu-id="45687-109">Each stream in the file can be configured separately, or you can set the same configuration for all streams.</span></span>

<span data-ttu-id="45687-110">Если вы настраиваете несколько потоков для индексирования в файле, необходимо настроить их все, а затем начать индексирование.</span><span class="sxs-lookup"><span data-stu-id="45687-110">If you are configuring multiple steams for indexing in a file, you must configure them all and then begin indexing.</span></span> <span data-ttu-id="45687-111">Если вы настраиваете и индексируете поток, а затем настраиваете другой поток в том же файле, повторный запуск индексатора приведет к удалению первого индекса.</span><span class="sxs-lookup"><span data-stu-id="45687-111">If you configure and index a stream and then configure another stream in the same file, starting the indexer again will delete the first index.</span></span> <span data-ttu-id="45687-112">Это соответствует формату ASF-файлов.</span><span class="sxs-lookup"><span data-stu-id="45687-112">This is to comply with the ASF file format.</span></span>

<span data-ttu-id="45687-113">В следующем коде показано, как настроить индексатор.</span><span class="sxs-lookup"><span data-stu-id="45687-113">The following code shows how to configure the indexer.</span></span> <span data-ttu-id="45687-114">В коде предполагается, что индексируемый файл имеет два потока: Первый — это звуковой поток, который не нужно индексировать, а второй — видеопоток.</span><span class="sxs-lookup"><span data-stu-id="45687-114">The code assumes that the file to be indexed has two streams: the first is an audio stream which does not need to be indexed, and the second is a video stream.</span></span> <span data-ttu-id="45687-115">В этом коде показано, как настроить индексатор.</span><span class="sxs-lookup"><span data-stu-id="45687-115">This code shows only how to configure the indexer.</span></span> <span data-ttu-id="45687-116">Чтобы индексировать файл, необходимо выполнить действия, описанные в разделе [для индексирования ASF-файла](to-index-an-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="45687-116">To index a file, you must follow the steps presented in [To Index an ASF File](to-index-an-asf-file.md).</span></span>


```C++
IWMIndexer*  pBaseIndexer = NULL;
IWMIndexer2* pMyIndexer   = NULL;

DWORD          dwInterval;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create an indexer.
hr = WMCreateIndexer(&pBaseIndexer);

// Retrieve an IWMIndexer2 interface pointer for the indexer just created.
hr = pBaseIndexer->QueryInterface(IID_IWMIndexer2, (void**)&pMyIndexer);

// Release the base indexer.
pBaseIndexer->Release();
pBaseIndexer = NULL;

// Set the index interval to 5 frames.
dwInterval = 5;

// Configure the indexer to create a frame-based index.
hr = pMyIndexer->Configure(2,                    // Stream Number.
                           WMT_IT_FRAME_NUMBERS, // Indexer type.
                           (void *)&dwInterval,  // Index interval.
                           NULL;        // Index type, use default.

// TODO: Index the file. See To Index an ASF File.

// Release the remaining interface.
pMyIndexer->Release();
pMyIndexer = NULL;

```



> [!Note]  
> <span data-ttu-id="45687-117">Тип индекса по умолчанию — ВМТ \_ его \_ ближайшую \_ чистую \_ точку.</span><span class="sxs-lookup"><span data-stu-id="45687-117">The default index type is WMT\_IT\_NEAREST\_CLEAN\_POINT.</span></span> <span data-ttu-id="45687-118">Хотя можно задать тип индекса другие значения, это приведет к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="45687-118">Although you can set the index type to other values, doing so will degrade seeking performance.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="45687-119">См. также</span><span class="sxs-lookup"><span data-stu-id="45687-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45687-120">**IWMIndexer2:: Configure**</span><span class="sxs-lookup"><span data-stu-id="45687-120">**IWMIndexer2::Configure**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)
</dt> <dt>

[<span data-ttu-id="45687-121">**Индексирование файла ASF**</span><span class="sxs-lookup"><span data-stu-id="45687-121">**To Index an ASF File**</span></span>](to-index-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="45687-122">**вмкреатеиндексер**</span><span class="sxs-lookup"><span data-stu-id="45687-122">**WMCreateIndexer**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[<span data-ttu-id="45687-123">**Работа с индексами**</span><span class="sxs-lookup"><span data-stu-id="45687-123">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




