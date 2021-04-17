---
description: Программная загрузка файла Графедит
ms.assetid: 0e1cff4e-43f8-4d0a-b7a7-b6d0278e9e4a
title: Программная загрузка файла Графедит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a4780ead7b65d883bdd48917c6372425612435
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495063"
---
# <a name="loading-a-graphedit-file-programmatically"></a><span data-ttu-id="875ec-103">Программная загрузка файла Графедит</span><span class="sxs-lookup"><span data-stu-id="875ec-103">Loading a GraphEdit File Programmatically</span></span>

<span data-ttu-id="875ec-104">Приложение может использовать интерфейс **IPersistStream** для загрузки файла графедит (. ГРФ).</span><span class="sxs-lookup"><span data-stu-id="875ec-104">An application can use the **IPersistStream** interface to load a GraphEdit (.grf) file.</span></span> <span data-ttu-id="875ec-105">Используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="875ec-105">Use the following code:</span></span>


```C++
HRESULT LoadGraphFile(IGraphBuilder *pGraph, const WCHAR* wszName)
{
    IStorage *pStorage = 0;
    if (S_OK != StgIsStorageFile(wszName))
    {
        return E_FAIL;
    }
    HRESULT hr = StgOpenStorage(wszName, 0, 
        STGM_TRANSACTED | STGM_READ | STGM_SHARE_DENY_WRITE, 
        0, 0, &pStorage);
    if (FAILED(hr))
    {
        return hr;
    }
    IPersistStream *pPersistStream = 0;
    hr = pGraph->QueryInterface(IID_IPersistStream,
             reinterpret_cast<void**>(&pPersistStream));
    if (SUCCEEDED(hr))
    {
        IStream *pStream = 0;
        hr = pStorage->OpenStream(L"ActiveMovieGraph", 0, 
            STGM_READ | STGM_SHARE_EXCLUSIVE, 0, &pStream);
        if(SUCCEEDED(hr))
        {
            hr = pPersistStream->Load(pStream);
            pStream->Release();
        }
        pPersistStream->Release();
    }
    pStorage->Release();
    return hr;
}

```



> [!Note]  
> <span data-ttu-id="875ec-106">Вызов **IPersistStream:: Load** в предыдущем примере кода может вернуть ошибку DirectShow или код успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="875ec-106">The call to **IPersistStream::Load** in the previous code example can return a DirectShow error or success code.</span></span> <span data-ttu-id="875ec-107">Список возможных возвращаемых значений см. в разделе [коды ошибок и успешности](error-and-success-codes.md).</span><span class="sxs-lookup"><span data-stu-id="875ec-107">For a list of possible return values, see [Error and Success Codes](error-and-success-codes.md).</span></span>

 

<span data-ttu-id="875ec-108">Файлы Графедит предназначены только для тестирования и отладки.</span><span class="sxs-lookup"><span data-stu-id="875ec-108">GraphEdit files are intended only for testing and debugging.</span></span> <span data-ttu-id="875ec-109">Они не предназначены для использования приложениями конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="875ec-109">They are not meant for use by end-user applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="875ec-110">См. также</span><span class="sxs-lookup"><span data-stu-id="875ec-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="875ec-111">Имитация построения графа с помощью Графедит</span><span class="sxs-lookup"><span data-stu-id="875ec-111">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[<span data-ttu-id="875ec-112">**стгиссторажефиле**</span><span class="sxs-lookup"><span data-stu-id="875ec-112">**StgIsStorageFile**</span></span>](/windows/win32/api/coml2api/nf-coml2api-stgisstoragefile)
</dt> <dt>

[<span data-ttu-id="875ec-113">**стгопенстораже**</span><span class="sxs-lookup"><span data-stu-id="875ec-113">**StgOpenStorage**</span></span>](/windows/win32/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 
