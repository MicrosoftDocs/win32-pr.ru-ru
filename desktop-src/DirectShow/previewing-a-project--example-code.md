---
description: 'Предварительный просмотр проекта: пример кода'
ms.assetid: 8a4af82a-5611-4c53-8de8-04eaefd51df9
title: 'Предварительный просмотр проекта: пример кода'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c5527fd93d0f05d5388739cc936e4a4dd203e18
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495045"
---
# <a name="previewing-a-project-example-code"></a><span data-ttu-id="2fb25-103">Предварительный просмотр проекта: пример кода</span><span class="sxs-lookup"><span data-stu-id="2fb25-103">Previewing a Project: Example Code</span></span>

<span data-ttu-id="2fb25-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="2fb25-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="2fb25-105">В следующем примере кода показано, как загрузить и просмотреть проект [служб редактирования DirectShow](directshow-editing-services.md) .</span><span class="sxs-lookup"><span data-stu-id="2fb25-105">The following code example shows how to load and preview a [DirectShow Editing Services](directshow-editing-services.md) project.</span></span> <span data-ttu-id="2fb25-106">Для ясности пропущена проверка ошибок.</span><span class="sxs-lookup"><span data-stu-id="2fb25-106">Error checking is omitted for clarity.</span></span>


```C++
#include <dshow.h>
#include <qedit.h>

// Preview a timeline.
void PreviewTL(IAMTimeline *pTL, IRenderEngine *pRender) 
{
    HRESULT hr;
    IGraphBuilder   *pGraph = NULL;
    IMediaControl   *pControl = NULL;
    IMediaEvent     *pEvent = NULL;

    // Build the graph.
    hr = pRender->SetTimelineObject(pTL);
    hr = pRender->ConnectFrontEnd( );
    hr = pRender->RenderOutputPins( );

    // Run the graph.
    hr = pRender->GetFilterGraph(&pGraph);
    pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
    hr = pControl->Run();

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);
    pControl->Stop();

    // Clean up.
    pEvent->Release();
    pControl->Release();
    pGraph->Release();
}

void main( void )
{
    HRESULT         hr;
    IAMTimeline     *pTL = NULL;
    IRenderEngine   *pRender = NULL; 
    IXml2Dex        *pXML = NULL; 

    CoInitialize(NULL);
    hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
                IID_IAMTimeline, (void**)&pTL);
    hr = CoCreateInstance(CLSID_Xml2Dex, NULL, CLSCTX_INPROC_SERVER, 
                IID_IXml2Dex, (void**)&pXML);
    hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
                IID_IRenderEngine, (void**)&pRender);

    // Load a project file.
    BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.xtl"), 15);
    hr = pXML->ReadXMLFile(pTL, bstrFile); 
    SysFreeString(bstrFile);
    pXML->Release();

    PreviewTL(pTL, pRender);

    // Clean up.    
    pRender->ScrapIt();
    pTL->Release();
    pRender->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a><span data-ttu-id="2fb25-107">См. также</span><span class="sxs-lookup"><span data-stu-id="2fb25-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fb25-108">Загрузка и предварительный просмотр проекта</span><span class="sxs-lookup"><span data-stu-id="2fb25-108">Loading and Previewing a Project</span></span>](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



