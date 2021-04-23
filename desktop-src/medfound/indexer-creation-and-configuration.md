---
description: В этом разделе содержатся сведения о создании объекта индексатора по умолчанию, предоставляемого Media Foundation.
ms.assetid: 3a2caf11-808b-4910-b83c-a272a026f0d3
title: Создание и Настройка индексатора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21e97bb558866fda021245b1597ead2a073c659c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265514"
---
# <a name="indexer-creation-and-configuration"></a><span data-ttu-id="72d2b-103">Создание и Настройка индексатора</span><span class="sxs-lookup"><span data-stu-id="72d2b-103">Indexer Creation and Configuration</span></span>

<span data-ttu-id="72d2b-104">*ИНДЕКСАТОР* ASF — это компонент уровня вмконтаинер, который используется для чтения или записи объектов индекса в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="72d2b-104">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="72d2b-105">В этом разделе содержатся сведения о создании объекта индексатора по умолчанию, предоставляемого Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="72d2b-105">This topic provides information about creating the default indexer object provided by Media Foundation.</span></span>

<span data-ttu-id="72d2b-106">Сведения о структуре файла ASF см. в разделе [Структура файлов ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="72d2b-106">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="72d2b-107">**Создание и инициализация индексатора ASF**</span><span class="sxs-lookup"><span data-stu-id="72d2b-107">**To create and initialize the ASF indexer**</span></span>

1.  <span data-ttu-id="72d2b-108">Вызовите функцию [**мфкреатеасфиндексер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) , чтобы получить указатель [**имфасфиндексер**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) на объект индексатора.</span><span class="sxs-lookup"><span data-stu-id="72d2b-108">Call the [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) function to receive an [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) pointer to the indexer object.</span></span>
2.  <span data-ttu-id="72d2b-109">Вызовите метод [**имфасфиндексер:: сетфлагс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) , чтобы указать режим чтения или записи для объекта индексатора.</span><span class="sxs-lookup"><span data-stu-id="72d2b-109">Call [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) to specify the read or write mode for indexer object.</span></span> <span data-ttu-id="72d2b-110">По умолчанию индексатор настроен для прямого поиска.</span><span class="sxs-lookup"><span data-stu-id="72d2b-110">By default, the indexer is configured for forward seeking.</span></span>

    

    | <span data-ttu-id="72d2b-111">Использовать</span><span class="sxs-lookup"><span data-stu-id="72d2b-111">Use</span></span>                       | <span data-ttu-id="72d2b-112">Flag</span><span class="sxs-lookup"><span data-stu-id="72d2b-112">Flag</span></span>                                           |
    |---------------------------|------------------------------------------------|
    | <span data-ttu-id="72d2b-113">Чтение (прямой поиск)</span><span class="sxs-lookup"><span data-stu-id="72d2b-113">Reading (forward seeking)</span></span> | <span data-ttu-id="72d2b-114">Ноль (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="72d2b-114">Zero (default)</span></span>                                 |
    | <span data-ttu-id="72d2b-115">Чтение (обратная попытка поиска)</span><span class="sxs-lookup"><span data-stu-id="72d2b-115">Reading (reverse seeking)</span></span> | <span data-ttu-id="72d2b-116">**\_Чтение индексатора \_ мфасф \_ для \_ реверсеплайбакк**</span><span class="sxs-lookup"><span data-stu-id="72d2b-116">**MFASF\_INDEXER\_READ\_FOR\_REVERSEPLAYBACK**</span></span> |
    | <span data-ttu-id="72d2b-117">Запись</span><span class="sxs-lookup"><span data-stu-id="72d2b-117">Writing</span></span>                   | <span data-ttu-id="72d2b-118">МФАСФный \_ индексатор \_ записи \_ нового \_ индекса</span><span class="sxs-lookup"><span data-stu-id="72d2b-118">MFASF\_INDEXER\_WRITE\_NEW\_INDEX</span></span>              |

    

     

    > [!Note]  
    > <span data-ttu-id="72d2b-119">Один и тот же экземпляр индексатора нельзя использовать как для чтения, так и для записи.</span><span class="sxs-lookup"><span data-stu-id="72d2b-119">The same instance of the indexer cannot be used for both reading and writing.</span></span> <span data-ttu-id="72d2b-120">Необходимо настроить индексатор для одного или другого.</span><span class="sxs-lookup"><span data-stu-id="72d2b-120">You must configure the indexer for one or the other.</span></span>

     

3.  <span data-ttu-id="72d2b-121">Вызовите метод [**имфасфиндексер:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) для инициализации индексатора, указав указатель [**имфасфконтентинфо**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) объекта контентинфо, который описывает файл, который необходимо записать или прочитать.</span><span class="sxs-lookup"><span data-stu-id="72d2b-121">Call [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) to initialize the indexer by specifying the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer of the ContentInfo object that describes the file to be written or read.</span></span> <span data-ttu-id="72d2b-122">Объект Контентинфо содержит сведения, составляющие [объект заголовка ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="72d2b-122">The ContentInfo object contains information that constitutes the [ASF Header Object](asf-file-structure.md).</span></span> <span data-ttu-id="72d2b-123">Перед созданием или чтением записей индекса ASF-файла объект индексатора требует допустимый объект Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="72d2b-123">The indexer object requires a valid ContentInfo object before generating or reading index entries of an ASF file.</span></span>

<span data-ttu-id="72d2b-124">В следующем примере кода показано, как приложение может создать и инициализировать объект индексатора для работы с конкретным содержимым ASF.</span><span class="sxs-lookup"><span data-stu-id="72d2b-124">The following code example shows how an application can create and initialize the indexer object to work with specific ASF content.</span></span> <span data-ttu-id="72d2b-125">Объект Контентинфо представляет объект заголовка ASF; содержимое передается в виде потока байтов.</span><span class="sxs-lookup"><span data-stu-id="72d2b-125">The ContentInfo object represents the ASF Header Object; the content is passed as a byte stream.</span></span>


```C++
HRESULT CreateASFIndexer(
    IMFASFContentInfo* pContentInfo, 
    DWORD dwFlags,
    IMFASFIndexer** ppIndexer
    )
{
    *ppIndexer = NULL;

    IMFASFIndexer *pIndexer = NULL;

    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pIndexer->SetFlags(dwFlags);
    if (FAILED(hr))
    {
        goto done;
    }

    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the object to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    // Clean up.
    SafeRelease(&pIndexer);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="72d2b-126">См. также</span><span class="sxs-lookup"><span data-stu-id="72d2b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72d2b-127">Индексатор ASF</span><span class="sxs-lookup"><span data-stu-id="72d2b-127">ASF Indexer</span></span>](asf-index-object.md)
</dt> <dt>

[<span data-ttu-id="72d2b-128">Использование индексатора для поиска в файле ASF</span><span class="sxs-lookup"><span data-stu-id="72d2b-128">Using the Indexer to Seek Within an ASF File</span></span>](using-the-indexer-to-seek.md)
</dt> <dt>

[<span data-ttu-id="72d2b-129">Использование индексатора для записи нового индекса</span><span class="sxs-lookup"><span data-stu-id="72d2b-129">Using the Indexer to Write a New Index</span></span>](using-the-indexer-to-write-a-new-index.md)
</dt> </dl>

 

 



