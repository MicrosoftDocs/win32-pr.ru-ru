---
description: Буфер поверхности DirectX
ms.assetid: 2c82c023-4436-4f8a-b896-7f4765f989b3
title: Буфер поверхности DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02211d268e23bd7185cd480bee4e4dff297293b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143132"
---
# <a name="directx-surface-buffer"></a><span data-ttu-id="7b815-103">Буфер поверхности DirectX</span><span class="sxs-lookup"><span data-stu-id="7b815-103">DirectX Surface Buffer</span></span>

<span data-ttu-id="7b815-104">Объект буфера поверхности DirectX — это буфер мультимедиа, который управляет поверхностью Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7b815-104">The DirectX surface buffer object is a media buffer that manages a Direct3D surface.</span></span> <span data-ttu-id="7b815-105">Чтобы создать экземпляр этого объекта, вызовите [**мфкреатедкссурфацебуффер**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) и передайте указатель на поверхность DirectX.</span><span class="sxs-lookup"><span data-stu-id="7b815-105">To create an instance of this object, call [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) and pass in a pointer to the DirectX surface.</span></span> <span data-ttu-id="7b815-106">Буфер поверхности DirectX предоставляет следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="7b815-106">The DirectX surface buffer exposes the following interfaces:</span></span>

-   [<span data-ttu-id="7b815-107">**имфмедиабуффер**</span><span class="sxs-lookup"><span data-stu-id="7b815-107">**IMFMediaBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
-   [<span data-ttu-id="7b815-108">**IMF2DBuffer**</span><span class="sxs-lookup"><span data-stu-id="7b815-108">**IMF2DBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)
-   [<span data-ttu-id="7b815-109">**имфжетсервице**</span><span class="sxs-lookup"><span data-stu-id="7b815-109">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)

<span data-ttu-id="7b815-110">Существует несколько способов доступа к памяти Surface из объекта buffer:</span><span class="sxs-lookup"><span data-stu-id="7b815-110">There are several ways to access the surface memory from the buffer object:</span></span>

-   <span data-ttu-id="7b815-111">Рекомендуется: вызовите [**имфжетсервице:: WebService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) в буфере.</span><span class="sxs-lookup"><span data-stu-id="7b815-111">Recommended: Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the buffer.</span></span> <span data-ttu-id="7b815-112">Используйте **\_ \_ службу "Mr buffer**" идентификатора службы.</span><span class="sxs-lookup"><span data-stu-id="7b815-112">Use the service identifier **MR\_BUFFER\_SERVICE**.</span></span> <span data-ttu-id="7b815-113">Метод возвращает указатель на базовую поверхность Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7b815-113">The method returns a pointer to the underlying Direct3D surface.</span></span>
-   <span data-ttu-id="7b815-114">Вызовите [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d).</span><span class="sxs-lookup"><span data-stu-id="7b815-114">Call [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d).</span></span> <span data-ttu-id="7b815-115">Этот метод вызывает **IDirect3DSurface9:: локкрект** непосредственно на поверхности.</span><span class="sxs-lookup"><span data-stu-id="7b815-115">This method calls **IDirect3DSurface9::LockRect** directly on the surface.</span></span> <span data-ttu-id="7b815-116">Метод [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) вызывает **унлоккрект** на поверхности.</span><span class="sxs-lookup"><span data-stu-id="7b815-116">The [**IMF2DBuffer::Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) method calls **UnlockRect** on the surface.</span></span>
-   <span data-ttu-id="7b815-117">Вызовите [**имфмедиабуффер:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span><span class="sxs-lookup"><span data-stu-id="7b815-117">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span></span> <span data-ttu-id="7b815-118">Как правило, это не рекомендуется, поскольку он заставляет объект копировать память из поверхности Direct3D, а затем обратно.</span><span class="sxs-lookup"><span data-stu-id="7b815-118">Generally this is not recommended, because it forces the object to copy memory from the Direct3D surface and then back again.</span></span> <span data-ttu-id="7b815-119">Метод [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) более эффективен.</span><span class="sxs-lookup"><span data-stu-id="7b815-119">The [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) method is more efficient.</span></span>

<span data-ttu-id="7b815-120">[**Блокировка**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) и [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) могут завершаться ошибкой, если базовая поверхность не является блокируемой.</span><span class="sxs-lookup"><span data-stu-id="7b815-120">Both [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) and [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) can fail if the underlying surface is not lockable.</span></span> <span data-ttu-id="7b815-121">Буфер поверхности DirectX реализует эти два метода в основном для компонентов, которые не предназначены для работы с областями Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7b815-121">The DirectX surface buffer implements these two methods primarily for components that are not designed to work with Direct3D surfaces.</span></span>

<span data-ttu-id="7b815-122">Расширенный обработчик видео (Евр) создает буферы поверхности DirectX, если декодер не настроен для ускорения видео DirectX (ДКСВА).</span><span class="sxs-lookup"><span data-stu-id="7b815-122">The enhanced video renderer (EVR) creates DirectX surface buffers when the decoder is not configured for DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="7b815-123">Дополнительные сведения см. в разделе [**имфвидеосамплеаллокатор**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).</span><span class="sxs-lookup"><span data-stu-id="7b815-123">For more information, see [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).</span></span>

### <a name="obtaining-the-direct3d-surface"></a><span data-ttu-id="7b815-124">Получение поверхности Direct3D</span><span class="sxs-lookup"><span data-stu-id="7b815-124">Obtaining the Direct3D Surface</span></span>

<span data-ttu-id="7b815-125">Чтобы получить поверхность Direct3D из примера видео, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7b815-125">To get a Direct3D surface from a video sample, do the following:</span></span>

1.  <span data-ttu-id="7b815-126">Вызовите [**имфсампле:: жетбуффербиндекс**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) со значением индекса, равным нулю.</span><span class="sxs-lookup"><span data-stu-id="7b815-126">Call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) with an index value of zero.</span></span>
2.  <span data-ttu-id="7b815-127">Вызовите [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) и укажите идентификатор службы **\_ буфера \_ MR** .</span><span class="sxs-lookup"><span data-stu-id="7b815-127">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) and specify the **MR\_BUFFER\_SERVICE** service identifier.</span></span>

<span data-ttu-id="7b815-128">В следующем коде показаны следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="7b815-128">The following code shows these steps:</span></span>


```C++
HRESULT GetD3DSurfaceFromSample(IMFSample *pSample, IDirect3DSurface9 **ppSurface)
{
    *ppSurface = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    HRESULT hr = pSample->GetBufferByIndex(0, &pBuffer);
    if (SUCCEEDED(hr))
    {
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(ppSurface));
        pBuffer->Release();
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="7b815-129">См. также</span><span class="sxs-lookup"><span data-stu-id="7b815-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b815-130">Буферы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="7b815-130">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="7b815-131">Образцы видео</span><span class="sxs-lookup"><span data-stu-id="7b815-131">Video Samples</span></span>](video-samples.md)
</dt> </dl>

 

 



