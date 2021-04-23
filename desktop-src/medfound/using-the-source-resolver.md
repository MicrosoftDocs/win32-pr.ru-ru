---
description: Использование сопоставителя источников
ms.assetid: 94e2a411-96b8-4506-8491-78f4f5f286ce
title: Использование сопоставителя источников
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e992199b097ff3f3337f92216b684d68e46bca13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263886"
---
# <a name="using-the-source-resolver"></a><span data-ttu-id="af4ce-103">Использование сопоставителя источников</span><span class="sxs-lookup"><span data-stu-id="af4ce-103">Using the Source Resolver</span></span>

<span data-ttu-id="af4ce-104">Средство выбора источника принимает URL-адрес или поток байтов и создает соответствующий источник мультимедиа для этого контента.</span><span class="sxs-lookup"><span data-stu-id="af4ce-104">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span> <span data-ttu-id="af4ce-105">Чтобы создать сопоставитель источника, вызовите [**мфкреатесаурцересолвер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver).</span><span class="sxs-lookup"><span data-stu-id="af4ce-105">To create the source resolver, call [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver).</span></span> <span data-ttu-id="af4ce-106">Эта функция возвращает указатель на интерфейс [**имфсаурцересолвер**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) .</span><span class="sxs-lookup"><span data-stu-id="af4ce-106">This function returns an [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface pointer.</span></span>

<span data-ttu-id="af4ce-107">Сопоставитель источников имеет как синхронные, так и асинхронные методы.</span><span class="sxs-lookup"><span data-stu-id="af4ce-107">The source resolver has both synchronous and asynchronous methods.</span></span> <span data-ttu-id="af4ce-108">Если вы используете сопоставитель источника из основного потока приложения, асинхронные методы приводят к более быстрому реагированию пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="af4ce-108">If you are using the source resolver from your main application thread, the asynchronous methods will make your user interface more responsive.</span></span> <span data-ttu-id="af4ce-109">Синхронные методы могут блокироваться в течение длительного времени, особенно если сопоставитель источника должен открыть сетевой ресурс.</span><span class="sxs-lookup"><span data-stu-id="af4ce-109">The synchronous methods can block for a noticeable amount of time, particularly if the source resolver must open a network resource.</span></span>

<span data-ttu-id="af4ce-110">Синхронные методы:</span><span class="sxs-lookup"><span data-stu-id="af4ce-110">The synchronous methods are:</span></span>

-   [<span data-ttu-id="af4ce-111">**Имфсаурцересолвер:: Креатеобжектфромурл**</span><span class="sxs-lookup"><span data-stu-id="af4ce-111">**IMFSourceResolver::CreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)
-   [<span data-ttu-id="af4ce-112">**Имфсаурцересолвер:: Креатеобжектфромбитестреам**</span><span class="sxs-lookup"><span data-stu-id="af4ce-112">**IMFSourceResolver::CreateObjectFromByteStream**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream)

<span data-ttu-id="af4ce-113">Асинхронные методы:</span><span class="sxs-lookup"><span data-stu-id="af4ce-113">The asynchronous methods are:</span></span>

-   [<span data-ttu-id="af4ce-114">**Имфсаурцересолвер:: Бегинкреатеобжектфромурл**</span><span class="sxs-lookup"><span data-stu-id="af4ce-114">**IMFSourceResolver::BeginCreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)
-   [<span data-ttu-id="af4ce-115">**Имфсаурцересолвер:: Бегинкреатеобжектфромбитестреам**</span><span class="sxs-lookup"><span data-stu-id="af4ce-115">**IMFSourceResolver::BeginCreateObjectFromByteStream**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)

<span data-ttu-id="af4ce-116">Для асинхронных методов каждый метод имеет соответствующий **End...** метод для завершения асинхронного запроса и метод **Cancel...** для отмены ожидающего запроса.</span><span class="sxs-lookup"><span data-stu-id="af4ce-116">For the asynchronous methods, each method has a corresponding **End...** method to complete the asynchronous request, and a **Cancel...** method to cancel a pending request.</span></span> <span data-ttu-id="af4ce-117">Дополнительные сведения о асинхронных методах в Media Foundation см. в разделе [асинхронные методы обратного вызова](asynchronous-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="af4ce-117">For more information about asynchronous methods in Media Foundation, see [Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>

<span data-ttu-id="af4ce-118">В следующем примере кода создается источник мультимедиа на основе URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="af4ce-118">The following code example creates a media source from a URL.</span></span> <span data-ttu-id="af4ce-119">В этом примере используется синхронный метод.</span><span class="sxs-lookup"><span data-stu-id="af4ce-119">This example uses the synchronous method.</span></span>


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="af4ce-120">См. также</span><span class="sxs-lookup"><span data-stu-id="af4ce-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af4ce-121">Сопоставитель источников</span><span class="sxs-lookup"><span data-stu-id="af4ce-121">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



