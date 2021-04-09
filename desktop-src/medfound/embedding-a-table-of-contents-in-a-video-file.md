---
description: Внедрение оглавления в видеофайл
ms.assetid: 1546388a-7868-4411-be20-34d28becbe76
title: Внедрение оглавления в видеофайл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8303082e454dde181de336ee0f64ff9d583312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143120"
---
# <a name="embedding-a-table-of-contents-in-a-video-file"></a><span data-ttu-id="aa5fe-103">Внедрение оглавления в видеофайл</span><span class="sxs-lookup"><span data-stu-id="aa5fe-103">Embedding a Table of Contents in a Video File</span></span>

<span data-ttu-id="aa5fe-104">В этом разделе показано, как создать оглавление и внедрить его в видеофайл.</span><span class="sxs-lookup"><span data-stu-id="aa5fe-104">This topic demonstrates how to create a table of contents (TOC) and embed it in a video file.</span></span> <span data-ttu-id="aa5fe-105">Чтобы избежать краткого примера кода, оглавление очень просто. Он содержит только одну запись, а запись заполняется как минимум информацией.</span><span class="sxs-lookup"><span data-stu-id="aa5fe-105">To keep the example code short, the table of contents is very simple; it contains only one entry, and the entry is populated with a minimum of information.</span></span>

<span data-ttu-id="aa5fe-106">Чтобы создать оглавление и внедрить его в файл, необходимо создать следующие четыре объекта, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="aa5fe-106">To create a table of contents and embed it in a file, you must create the following four objects by calling **CoCreateInstance**.</span></span>

-   <span data-ttu-id="aa5fe-107">Запись ОГЛАВЛЕНИя</span><span class="sxs-lookup"><span data-stu-id="aa5fe-107">TOC Entry</span></span>
-   <span data-ttu-id="aa5fe-108">Список записей ОГЛАВЛЕНИя</span><span class="sxs-lookup"><span data-stu-id="aa5fe-108">TOC Entry List</span></span>
-   <span data-ttu-id="aa5fe-109">ОГЛАВЛЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa5fe-109">TOC</span></span>
-   <span data-ttu-id="aa5fe-110">Средство синтаксического анализа ОГЛАВЛЕНИя</span><span class="sxs-lookup"><span data-stu-id="aa5fe-110">TOC Parser</span></span>

<span data-ttu-id="aa5fe-111">Идентификаторы классов для объектов задаются в [идентификаторах классов для средства синтаксического анализа содержимого](class-identifiers-for-toc-parser.md).</span><span class="sxs-lookup"><span data-stu-id="aa5fe-111">Class identifiers for the objects are given in [Class Identifiers for Table of Contents Parser](class-identifiers-for-toc-parser.md).</span></span>

<span data-ttu-id="aa5fe-112">Сначала заполните запись ОГЛАВЛЕНИя информацией, описывающей одну часть видеофайла.</span><span class="sxs-lookup"><span data-stu-id="aa5fe-112">First populate the TOC entry with information that describes one portion of the video file.</span></span> <span data-ttu-id="aa5fe-113">Добавьте запись ОГЛАВЛЕНИя в список элементов ОГЛАВЛЕНИя, а затем добавьте список записей ОГЛАВЛЕНИя в ОГЛАВЛЕНИе.</span><span class="sxs-lookup"><span data-stu-id="aa5fe-113">Add the TOC entry to the TOC entry list, and then add the TOC entry list to the TOC.</span></span> <span data-ttu-id="aa5fe-114">Наконец, добавьте ОГЛАВЛЕНИе в средство синтаксического анализа TOC, которое предоставляет функциональные возможности для внедрения ОГЛАВЛЕНИя в видеофайл.</span><span class="sxs-lookup"><span data-stu-id="aa5fe-114">Finally, add the TOC to the TOC parser, which provides the functionality for embedding the TOC in the video file.</span></span> <span data-ttu-id="aa5fe-115">В следующем списке приведены более подробные инструкции.</span><span class="sxs-lookup"><span data-stu-id="aa5fe-115">The following list gives the steps in more detail.</span></span>

1.  <span data-ttu-id="aa5fe-116">Создайте объект элемента ОГЛАВЛЕНИя и получите на нем интерфейс [**итоцентри**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) .</span><span class="sxs-lookup"><span data-stu-id="aa5fe-116">Create a TOC Entry object and obtain an [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) interface on it.</span></span>
2.  <span data-ttu-id="aa5fe-117">Заполните [**структуру \_ \_ дескриптора записи оглавления**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) и передайте ее в [**итоцентри:: сетдескриптор**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor).</span><span class="sxs-lookup"><span data-stu-id="aa5fe-117">Populate a [**TOC\_ENTRY\_DESCRIPTOR**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) structure and pass it to [**ITocEntry::SetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor).</span></span>
3.  <span data-ttu-id="aa5fe-118">Создайте объект списка записей ОГЛАВЛЕНИя и получите на нем интерфейс [**итоцентрилист**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) .</span><span class="sxs-lookup"><span data-stu-id="aa5fe-118">Create a TOC Entry List object and obtain an [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) interface on it.</span></span>
4.  <span data-ttu-id="aa5fe-119">Добавьте объект записи ОГЛАВЛЕНИя, созданный на шаге 1, в объект списка записей ОГЛАВЛЕНИя, вызвав [**итоцентрилист:: аддентрибиндекс**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex).</span><span class="sxs-lookup"><span data-stu-id="aa5fe-119">Add the TOC Entry object you created in step 1 to the TOC Entry List object by calling [**ITocEntryList::AddEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex).</span></span>
5.  <span data-ttu-id="aa5fe-120">Создайте объект TOC и получите на нем интерфейс [**Иток**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) .</span><span class="sxs-lookup"><span data-stu-id="aa5fe-120">Create a TOC object and obtain an [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) interface on it.</span></span>
6.  <span data-ttu-id="aa5fe-121">Добавьте объект списка записей ОГЛАВЛЕНИя, созданный на шаге 3, в объект TOC, вызвав [**Иток:: аддентрилистбиндекс**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex).</span><span class="sxs-lookup"><span data-stu-id="aa5fe-121">Add the TOC Entry List object you created in step 3 to the TOC object by calling [**IToc::AddEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex).</span></span>
7.  <span data-ttu-id="aa5fe-122">Создайте объект средства синтаксического анализа ОГЛАВЛЕНИя и получите на нем интерфейс [**итокпарсер**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) .</span><span class="sxs-lookup"><span data-stu-id="aa5fe-122">Create a TOC Parser object and obtain an [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface on it.</span></span>
8.  <span data-ttu-id="aa5fe-123">Вызовите метод [**итокпарсер:: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) , чтобы инициализировать объект средства синтаксического анализа оглавления и связать его с видеофайлом.</span><span class="sxs-lookup"><span data-stu-id="aa5fe-123">Call [**ITocParser::Init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) to initialize the TOC Parser object and associate it with a video file.</span></span>
9.  <span data-ttu-id="aa5fe-124">Добавьте объект TOC, созданный на шаге 5, в объект средства синтаксического анализа ОГЛАВЛЕНИя, вызвав [**итокпарсер:: аддток**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc).</span><span class="sxs-lookup"><span data-stu-id="aa5fe-124">Add the TOC object you created in step 5 to the TOC Parser object by calling [**ITocParser::AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc).</span></span>
10. <span data-ttu-id="aa5fe-125">Внедрите оглавление в видеофайл, вызвав [**итокпарсер:: Commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit).</span><span class="sxs-lookup"><span data-stu-id="aa5fe-125">Embed the table of contents in the video file by calling [**ITocParser::Commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit).</span></span>

<span data-ttu-id="aa5fe-126">В следующем коде показаны шаги, приведенные в предыдущем списке.</span><span class="sxs-lookup"><span data-stu-id="aa5fe-126">The following code demonstrates the steps given in the preceding list.</span></span>


```C++
#include <wmcodecdsp.h>
HRESULT InitTocParserAndCommit(IToc* pToc);

void main()
{
   HRESULT hr = CoInitialize(NULL);
   
   if(SUCCEEDED(hr))
   {    
      ITocEntry* pEntry = NULL;
      hr = CoCreateInstance(CLSID_CTocEntry, NULL, 
         CLSCTX_INPROC_SERVER, IID_ITocEntry, (VOID**)&pEntry); 

      if(SUCCEEDED(hr))
      {
         TOC_ENTRY_DESCRIPTOR tocDesc = {0};
         tocDesc.qwStartTime = 4; 
         tocDesc.qwEndTime = 8;
         pEntry->SetDescriptor(&tocDesc); // HRESULT ignored for simplicity.    
    
         ITocEntryList* pEntryList = NULL;
         hr = CoCreateInstance(CLSID_CTocEntryList, NULL, 
            CLSCTX_INPROC_SERVER, IID_ITocEntryList, (VOID**)&pEntryList);

         if(SUCCEEDED(hr))
         {
            pEntryList->AddEntryByIndex(0, pEntry); // HRESULT ignored.
      
            IToc* pToc = NULL;
            hr = CoCreateInstance(CLSID_CToc, NULL, 
               CLSCTX_INPROC_SERVER, IID_IToc, (VOID**)&pToc);

            if(SUCCEEDED(hr))
            {
               pToc->AddEntryListByIndex(0, pEntryList); // HRESULT ignored.
               hr = InitTocParserAndCommit(pToc);
            }
         }
      }
     
      CoUninitialize();
   }
}

HRESULT InitTocParserAndCommit(IToc* pToc)
{
   ITocParser* pTocParser = NULL;
   HRESULT hr = CoCreateInstance(CLSID_CTocParser, NULL, 
      CLSCTX_INPROC_SERVER, IID_ITocParser, (VOID**)&pTocParser);

   if(SUCCEEDED(hr))
   {
      hr = pTocParser->Init(L"\\\\?\\c:\\experiment\\seattle.wmv");

      if(SUCCEEDED(hr))
      {
         DWORD tocIndex = 0;
         hr = pTocParser->AddToc(TOC_POS_TOPLEVELOBJECT, pToc, &tocIndex);

         if(SUCCEEDED(hr))
         {
            hr = pTocParser->Commit();
         }
      }

      pTocParser->Release();
      pTocParser = NULL;
   }

   return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="aa5fe-127">См. также</span><span class="sxs-lookup"><span data-stu-id="aa5fe-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa5fe-128">Чтение оглавления из файла видео</span><span class="sxs-lookup"><span data-stu-id="aa5fe-128">Reading a Table of Contents From a Video File</span></span>](reading-a-table-of-contents-from-a-video-file.md)
</dt> <dt>

[<span data-ttu-id="aa5fe-129">Таблица объектов средства синтаксического анализа содержимого</span><span class="sxs-lookup"><span data-stu-id="aa5fe-129">Table of Contents Parser Objects</span></span>](toc-parser-objects.md)
</dt> <dt>

[<span data-ttu-id="aa5fe-130">Справочное руководством по программированию синтаксического анализатора содержимого</span><span class="sxs-lookup"><span data-stu-id="aa5fe-130">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 



