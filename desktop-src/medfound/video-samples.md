---
description: Образцы видео
ms.assetid: 1ee2ad6f-5e84-45ba-9849-cd3bd8e7eb29
title: Образцы видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239fecd0947271627abc7fc50ed16f6a7c682b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898693"
---
# <a name="video-samples"></a><span data-ttu-id="36abc-103">Образцы видео</span><span class="sxs-lookup"><span data-stu-id="36abc-103">Video Samples</span></span>

<span data-ttu-id="36abc-104">Пример объекта Video — это Специализированная реализация интерфейса [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) для использования с расширенным модулем [подготовки видео](enhanced-video-renderer.md) (Евр).</span><span class="sxs-lookup"><span data-stu-id="36abc-104">The video sample object is a specialized implementation of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface for use with the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="36abc-105">Чтобы создать экземпляр этого объекта, вызовите функцию [**мфкреатевидеосамплефромсурфаце**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) .</span><span class="sxs-lookup"><span data-stu-id="36abc-105">To create an instance of this object, call the [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) function.</span></span> <span data-ttu-id="36abc-106">Функция принимает указатель на поверхность Direct3D и возвращает указатель на интерфейс **имфсампле** .</span><span class="sxs-lookup"><span data-stu-id="36abc-106">The function takes a pointer to a Direct3D surface and returns a pointer to the **IMFSample** interface.</span></span> <span data-ttu-id="36abc-107">Следующие типы объектов должны выделять примеры с помощью этой функции:</span><span class="sxs-lookup"><span data-stu-id="36abc-107">The following types of objects should allocate samples using this function:</span></span>

-   <span data-ttu-id="36abc-108">Пользовательские Выступающие Евр.</span><span class="sxs-lookup"><span data-stu-id="36abc-108">Custom EVR presenters.</span></span> <span data-ttu-id="36abc-109">Выступающие выделяют видеоролики и отправляет их в метод микшера [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) .</span><span class="sxs-lookup"><span data-stu-id="36abc-109">A presenter allocates video samples and sends them to the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method.</span></span> <span data-ttu-id="36abc-110">Дополнительные сведения см. [в разделе как написать Евр Presenter](how-to-write-an-evr-presenter.md).</span><span class="sxs-lookup"><span data-stu-id="36abc-110">For more information, see [How to Write an EVR Presenter](how-to-write-an-evr-presenter.md).</span></span>

-   <span data-ttu-id="36abc-111">Видеодекодеры, поддерживающие ускорение видео.</span><span class="sxs-lookup"><span data-stu-id="36abc-111">Video decoders that support video acceleration.</span></span> <span data-ttu-id="36abc-112">Дополнительные сведения см. [в разделе Поддержка дксва 2,0 в Media Foundation](supporting-dxva-2-0-in-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="36abc-112">For more information, see [Supporting DXVA 2.0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md).</span></span>

<span data-ttu-id="36abc-113">Пример объекта Video реализует следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="36abc-113">The video sample object implements the following interfaces:</span></span>

-   [<span data-ttu-id="36abc-114">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="36abc-114">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

-   [<span data-ttu-id="36abc-115">**имфдесиредсампле**</span><span class="sxs-lookup"><span data-stu-id="36abc-115">**IMFDesiredSample**</span></span>](/windows/desktop/api/evr/nn-evr-imfdesiredsample)

-   [<span data-ttu-id="36abc-116">**имфтраккедсампле**</span><span class="sxs-lookup"><span data-stu-id="36abc-116">**IMFTrackedSample**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)

<span data-ttu-id="36abc-117">Если параметр *пунксурфаце* объекта [**мфкреатевидеосамплефромсурфаце**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) имеет значение, отличное от **null**, то результирующий пример видео содержит один буфер мультимедиа, который инкапсулирует поверхность Direct3D.</span><span class="sxs-lookup"><span data-stu-id="36abc-117">If the *pUnkSurface* parameter of [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) is non-**NULL**, the resulting video sample contains a single media buffer that encapsulates the Direct3D surface.</span></span> <span data-ttu-id="36abc-118">Этот Буферный объект имеет ограниченную функциональность:</span><span class="sxs-lookup"><span data-stu-id="36abc-118">This buffer object has limited functionality:</span></span>

-   <span data-ttu-id="36abc-119">Метод [**имфмедиабуффер:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) буфера возвращает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="36abc-119">The buffer's [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) method returns E\_NOTIMPL.</span></span>

-   <span data-ttu-id="36abc-120">В буфере не реализован интерфейс [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="36abc-120">The buffer does not implement the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>

<span data-ttu-id="36abc-121">Единственный способ получить доступ к поверхности из буфера — вызвать [**имфжетсервице::-Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice), используя идентификатор службы MR \_ buffer \_ .</span><span class="sxs-lookup"><span data-stu-id="36abc-121">The only way to access the surface from the buffer is to call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice), using the service identifier MR\_BUFFER\_SERVICE.</span></span>

<span data-ttu-id="36abc-122">Если параметр *пунксурфаце* имеет **значение NULL**, пример видео создается с нулевыми буферами носителей.</span><span class="sxs-lookup"><span data-stu-id="36abc-122">If the *pUnkSurface* parameter is **NULL**, the video sample is created with zero media buffers.</span></span> <span data-ttu-id="36abc-123">Чтобы добавить буфер в образец, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="36abc-123">To add a buffer the sample, do the following:</span></span>

1.  <span data-ttu-id="36abc-124">Создайте поверхность Direct3D.</span><span class="sxs-lookup"><span data-stu-id="36abc-124">Create a Direct3D surface.</span></span>

2.  <span data-ttu-id="36abc-125">Создайте буфер Surface, вызвав [**мфкреатедкссурфацебуффер**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer).</span><span class="sxs-lookup"><span data-stu-id="36abc-125">Create a surface buffer by calling [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer).</span></span> <span data-ttu-id="36abc-126">Дополнительные сведения см. в разделе [буфер поверхности DirectX](directx-surface-buffer.md).</span><span class="sxs-lookup"><span data-stu-id="36abc-126">For more information, see [DirectX Surface Buffer](directx-surface-buffer.md).</span></span>

3.  <span data-ttu-id="36abc-127">Добавьте буфер в образец, вызвав [**имфсампле:: аддбуффер**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span><span class="sxs-lookup"><span data-stu-id="36abc-127">Add the buffer to the sample by calling [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span></span>

<span data-ttu-id="36abc-128">Используйте этот подход, если требуется доступ к памяти поверхности через интерфейс [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="36abc-128">Use this approach if you need the surface memory to be accessible through the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36abc-129">См. также</span><span class="sxs-lookup"><span data-stu-id="36abc-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36abc-130">Буферы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="36abc-130">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="36abc-131">Примеры носителей</span><span class="sxs-lookup"><span data-stu-id="36abc-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 
