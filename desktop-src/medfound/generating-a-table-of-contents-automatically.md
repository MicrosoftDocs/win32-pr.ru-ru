---
description: Автоматическое формирование оглавления
ms.assetid: 3acb9c12-0158-4b89-87c4-4abd35ae8c2f
title: Автоматическое формирование оглавления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22adc4d48ad7f4b1d89a446eb28c25d6011804a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701311"
---
# <a name="generating-a-table-of-contents-automatically"></a><span data-ttu-id="ab13d-103">Автоматическое формирование оглавления</span><span class="sxs-lookup"><span data-stu-id="ab13d-103">Generating a Table of Contents Automatically</span></span>

<span data-ttu-id="ab13d-104">В этом разделе показано, как использовать компонент [**генератора**](/previous-versions/ee264297(v=vs.85)) оглавлений (генератора оглавления) для автоматического создания оглавления для видеофайла.</span><span class="sxs-lookup"><span data-stu-id="ab13d-104">This topic demonstrates how to use [**Table of Contents Generator**](/previous-versions/ee264297(v=vs.85)) (TOC Generator) component to automatically generate a table of contents for a video file.</span></span>

<span data-ttu-id="ab13d-105">Генератор ОГЛАВЛЕНИя — это объект мультимедиа DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="ab13d-105">TOC Generator is a DirectX Media Object (DMO).</span></span> <span data-ttu-id="ab13d-106">Чтобы использовать генератор содержания DMO, создайте граф фильтра DirectX с видеофайлом в качестве источника.</span><span class="sxs-lookup"><span data-stu-id="ab13d-106">To use the TOC Generator DMO, build a DirectX filter graph that has a video file as its source.</span></span> <span data-ttu-id="ab13d-107">Вставьте генератор содержания DMO в граф фильтра и запустите граф.</span><span class="sxs-lookup"><span data-stu-id="ab13d-107">Insert the TOC Generator DMO into the filter graph, and run the graph.</span></span> <span data-ttu-id="ab13d-108">Затем можно получить автоматически созданную оглавление из генератора содержания DMO.</span><span class="sxs-lookup"><span data-stu-id="ab13d-108">You can then obtain the automatically generated table of contents from the TOC Generator DMO.</span></span>

<span data-ttu-id="ab13d-109">Следующая процедура предоставляет более подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="ab13d-109">The following procedure gives the steps in more detail.</span></span>

1.  <span data-ttu-id="ab13d-110">Вызовите [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы создать объект графа фильтра (**CLSID \_ филтерграф**) и получить интерфейс [**играфбуилдер**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="ab13d-110">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a Filter Graph object (**CLSID\_FilterGraph**) and obtain an [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
2.  <span data-ttu-id="ab13d-111">Вызовите [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы создать объект фильтра оболочки DMO (**CLSID \_ дмоврапперфилтер**) и получить интерфейс [**идмоврапперфилтер**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter) .</span><span class="sxs-lookup"><span data-stu-id="ab13d-111">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a DMO Wrapper Filter object (**CLSID\_DMOWrapperFilter**) and obtain an [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter) interface.</span></span>
3.  <span data-ttu-id="ab13d-112">Передавайте **\_ ктокженератордмо CLSID** методу [**init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) фильтра оболочки DMO.</span><span class="sxs-lookup"><span data-stu-id="ab13d-112">Pass **CLSID\_CTocGeneratorDmo** to the [**Init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) method of your DMO wrapper filter.</span></span> <span data-ttu-id="ab13d-113">Это создает генератор содержания DMO и заключает его в фильтр оболочки DMO.</span><span class="sxs-lookup"><span data-stu-id="ab13d-113">This creates a TOC Generator DMO and wraps it in your DMO wrapper filter.</span></span>
4.  <span data-ttu-id="ab13d-114">Вызовите метод [**аддфилтер**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter) интерфейса [**играфбуилдер**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) , чтобы добавить в граф фильтра генератор упакованного содержания DMO.</span><span class="sxs-lookup"><span data-stu-id="ab13d-114">Call the [**AddFilter**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface to add the wrapped TOC Generator DMO to the filter graph.</span></span>
    > [!Note]  
    > <span data-ttu-id="ab13d-115">[**Играфбуилдер**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) наследует от [**ифилтерграф**](/windows/win32/api/strmif/nn-strmif-ifiltergraph).</span><span class="sxs-lookup"><span data-stu-id="ab13d-115">[**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) inherits from [**IFilterGraph**](/windows/win32/api/strmif/nn-strmif-ifiltergraph).</span></span>

     

5.  <span data-ttu-id="ab13d-116">Вызовите метод [**аддсаурцефилтер**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter) интерфейса [**играфбуилдер**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) , чтобы создать фильтр источник и добавить его в граф.</span><span class="sxs-lookup"><span data-stu-id="ab13d-116">Call the [**AddSourceFilter**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface to create a souce filter and add it to the graph.</span></span>
6.  <span data-ttu-id="ab13d-117">Перечислите сигналы в фильтре оболочки DMO и фильтре источника.</span><span class="sxs-lookup"><span data-stu-id="ab13d-117">Enumerate pins on the DMO wrapper filter and the source filter.</span></span> <span data-ttu-id="ab13d-118">Для этого требуется получение интерфейсов [**иенумпинс**](/windows/win32/api/strmif/nn-strmif-ienumpins) и интерфейсов [**Ипин**](/windows/win32/api/strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="ab13d-118">This involves obtaining [**IEnumPins**](/windows/win32/api/strmif/nn-strmif-ienumpins) interfaces and [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) interfaces.</span></span>
7.  <span data-ttu-id="ab13d-119">Подключите фильтр источника и фильтр оболочки, вызвав метод [**Connect**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect) интерфейса [**играфбуилдер**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="ab13d-119">Connect the source filter and the wrapper filter by calling the [**Connect**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
8.  <span data-ttu-id="ab13d-120">Завершите работу графа, вызвав метод [**Render**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render) интерфейса [**играфбуилдер**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="ab13d-120">Complete the graph by calling the [**Render**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
9.  <span data-ttu-id="ab13d-121">Запустите граф ([**имедиаконтрол:: Run**](/windows/win32/api/control/nf-control-imediacontrol-run)) и дождитесь его завершения ([**Имедиаевент:: ваитфоркомплетион**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)).</span><span class="sxs-lookup"><span data-stu-id="ab13d-121">Run the graph ([**IMediaControl::Run**](/windows/win32/api/control/nf-control-imediacontrol-run)), and wait for it to complete ([**IMediaEvent::WaitForCompletion**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)).</span></span>
10. <span data-ttu-id="ab13d-122">Получите интерфейс [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) в оболочке фильтра DMO и получите значение свойства [**мфпкэй \_ токженератор \_ токреади**](/previous-versions/ee264297(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ab13d-122">Obtain an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface on your DMO filter wrapper, and get the value of the [**MFPKEY\_TOCGENERATOR\_TOCREADY**](/previous-versions/ee264297(v=vs.85)) property.</span></span> <span data-ttu-id="ab13d-123">При необходимости повторите операцию, пока оглавление не будет готово.</span><span class="sxs-lookup"><span data-stu-id="ab13d-123">Repeat if necessary until the table of contents is ready.</span></span>
11. <span data-ttu-id="ab13d-124">Используйте интерфейс [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) для получения значения свойства [**мфпкэй \_ токженератор \_ токобжект**](/previous-versions/ee264297(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ab13d-124">Use your [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface to get the value of the [**MFPKEY\_TOCGENERATOR\_TOCOBJECT**](/previous-versions/ee264297(v=vs.85)) property.</span></span> <span data-ttu-id="ab13d-125">Это свойство является интерфейсом [**Иток**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) , который представляет автоматически созданное оглавление.</span><span class="sxs-lookup"><span data-stu-id="ab13d-125">This property is an [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) interface that represents the automatically generated table of contents.</span></span>

<span data-ttu-id="ab13d-126">В следующем коде показана процедура автоматического создания оглавления.</span><span class="sxs-lookup"><span data-stu-id="ab13d-126">The following code demonstrates the procedure for generating a table of contents automatically.</span></span> <span data-ttu-id="ab13d-127">В коде используются три вспомогательные функции ([**буилдграф**](buildgraph-method-for-generating-a-table-of-contents.md), [**рунграфандваит**](rungraphandwait-method-for-generating-a-table-of-contents.md)и [**жетток**](gettoc-method-for-generating-a-table-of-contents.md)), которые показаны на других страницах этой документации.</span><span class="sxs-lookup"><span data-stu-id="ab13d-127">The code uses three helper functions ([**BuildGraph**](buildgraph-method-for-generating-a-table-of-contents.md), [**RunGraphAndWait**](rungraphandwait-method-for-generating-a-table-of-contents.md), and [**GetToc**](gettoc-method-for-generating-a-table-of-contents.md)) that are shown on other pages of this documentation.</span></span>


```C++
#include <dshow.h>
#include <dmodshow.h>
#include <wmcodecdsp.h>
#include <dmoreg.h>
#include <propsys.h>
#include <propidl.h>
#include <initguid.h>

HRESULT GetToc(IDMOWrapperFilter* pWrap, IToc** ppToc);
HRESULT RunGraphAndWait(IGraphBuilder* pGraph);
HRESULT BuildGraph(IGraphBuilder* pGraph, IDMOWrapperFilter* pWrap);

WCHAR g_sourceFile[] = L"c:\\experiment\\Seattle.wmv";

void main()
{
   HRESULT hr = E_FAIL;
   hr = CoInitialize(NULL);

   if(SUCCEEDED(hr))
   {
      IGraphBuilder* pBuilder = NULL;
      hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
         IID_IGraphBuilder, (VOID**)&pBuilder);

      if(SUCCEEDED(hr))
      {
         IDMOWrapperFilter* pWrap = NULL;
         hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, CLSCTX_INPROC, 
            IID_IDMOWrapperFilter, (VOID**)&pWrap);

         if(SUCCEEDED(hr))
         {
            hr = pWrap->Init(CLSID_CTocGeneratorDmo, DMOCATEGORY_VIDEO_EFFECT); 

            if(SUCCEEDED(hr))
            {
               hr = BuildGraph(pBuilder, pWrap);

               if(SUCCEEDED(hr))
               {
                  hr = RunGraphAndWait(pBuilder);

                  if(SUCCEEDED(hr))
                  {
                     IToc* pToc = NULL;
                     hr = GetToc(pWrap, &pToc);

                     if(SUCCEEDED(hr))
                     {
                        // Inspect the table of contents by calling IToc methods.

                        pToc->Release();
                        pToc = NULL;
                     }
                  }
               }
            }

            pWrap->Release();
            pWrap = NULL;
         }

         pBuilder->Release();
         pBuilder = NULL;
      }

      CoUninitialize();
   }
}
```



## <a name="related-topics"></a><span data-ttu-id="ab13d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="ab13d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab13d-129">Функция Буилдграф для создания оглавления</span><span class="sxs-lookup"><span data-stu-id="ab13d-129">BuildGraph Function for Generating a Table of Contents</span></span>](buildgraph-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="ab13d-130">Функция Жетток для создания оглавления</span><span class="sxs-lookup"><span data-stu-id="ab13d-130">GetToc Function for Generating a Table of Contents</span></span>](gettoc-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="ab13d-131">Функция Рунграфандваит для создания оглавления</span><span class="sxs-lookup"><span data-stu-id="ab13d-131">RunGraphAndWait Function for Generating a Table of Contents</span></span>](rungraphandwait-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="ab13d-132">Справочное руководством по программированию синтаксического анализатора содержимого</span><span class="sxs-lookup"><span data-stu-id="ab13d-132">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 
