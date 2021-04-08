---
description: ПИН-коды порта видео
ms.assetid: a6be24e5-7937-48f1-abeb-3f29c3deeafd
title: ПИН-коды порта видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d13ab4ad63995dd38460bf29064035c9c1802dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911052"
---
# <a name="video-port-pins"></a><span data-ttu-id="28322-103">ПИН-коды порта видео</span><span class="sxs-lookup"><span data-stu-id="28322-103">Video Port Pins</span></span>

<span data-ttu-id="28322-104">Устройство записи с видеопортом оборудования может использовать расширения видеопортов (впе) в Microsoft® DirectX®.</span><span class="sxs-lookup"><span data-stu-id="28322-104">A capture device with a hardware video port might use the video port extensions (VPE) in Microsoft® DirectX®.</span></span> <span data-ttu-id="28322-105">Если да, то фильтр записи будет иметь ПИН-код для порта видео (президента).</span><span class="sxs-lookup"><span data-stu-id="28322-105">If so, the capture filter will have a video port (VP) pin.</span></span> <span data-ttu-id="28322-106">Данные видео не передаются с закрепления вице-президента через граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="28322-106">No video data travels from the VP pin through the filter graph.</span></span> <span data-ttu-id="28322-107">Вместо этого видеокадры создаются на оборудовании и отправляются непосредственно в видеопамять.</span><span class="sxs-lookup"><span data-stu-id="28322-107">Instead, video frames are produced in hardware and sent directly to video memory.</span></span> <span data-ttu-id="28322-108">ПИН-код президента позволяет отправлять управляющие сообщения на оборудование.</span><span class="sxs-lookup"><span data-stu-id="28322-108">The VP pin allows control messages to be sent to the hardware.</span></span>

<span data-ttu-id="28322-109">Важно подключить ПИН-код президента, даже если приложение выполняет только запись файлов без предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="28322-109">It is important to connect the VP pin, even if your application only performs file capture with no preview.</span></span> <span data-ttu-id="28322-110">Если оставить ПИН-код неподключенным, граф будет работать неправильно.</span><span class="sxs-lookup"><span data-stu-id="28322-110">If you leave the pin unconnected, the graph will not run correctly.</span></span> <span data-ttu-id="28322-111">Это отличается от предварительного просмотра ПИН-кодов, которые не должны быть подключены.</span><span class="sxs-lookup"><span data-stu-id="28322-111">This is different from preview pins, which do not have to be connected.</span></span>

<span data-ttu-id="28322-112">Различные модули подготовки видео DirectShow обеспечивают разную поддержку ПИН-кодов вице-президента:</span><span class="sxs-lookup"><span data-stu-id="28322-112">The different DirectShow video renderers provide varying support for VP pins:</span></span>

-   <span data-ttu-id="28322-113">Модуль подготовки видео. Подключите ПИН-код президента, чтобы закрепить 0 в фильтре [микшера наложения](overlay-mixer-filter.md) , и подключите Фильтр микшера наложения к модулю подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="28322-113">Video Renderer: Connect the VP pin to pin 0 on the [Overlay Mixer](overlay-mixer-filter.md) filter, and connect the Overlay Mixer filter to the Video Renderer.</span></span>
-   <span data-ttu-id="28322-114">VMR-7. подключение к фильтру [диспетчера видеопортов](video-port-manager.md) и подключение диспетчера видеопортов к фильтру VMR-7.</span><span class="sxs-lookup"><span data-stu-id="28322-114">VMR-7: Connect the VP pin to the [Video Port Manager](video-port-manager.md) filter, and connect the Video Port Manager to the VMR-7.</span></span>
-   <span data-ttu-id="28322-115">VMR-9. Вы не можете использовать VMR-9, если у устройства есть свой вице-президент, так как Direct3D 9 не поддерживает видеопорты.</span><span class="sxs-lookup"><span data-stu-id="28322-115">VMR-9: You cannot use the VMR-9 if the device has a VP pin, because Direct3D 9 does not support video ports.</span></span> <span data-ttu-id="28322-116">Используйте модуль подготовки видео или VMR-7.</span><span class="sxs-lookup"><span data-stu-id="28322-116">Use either the Video Renderer or the VMR-7.</span></span>

<span data-ttu-id="28322-117">Для сценариев видеопортов рекомендуется использовать микшер наложения и модуль подготовки видео для диспетчера видеопортов и VMR-7, так как не все драйверы поддерживают диспетчер видеопортов.</span><span class="sxs-lookup"><span data-stu-id="28322-117">For video port scenarios, the Overlay Mixer and Video Renderer are recommended over the Video Port Manager and VMR-7, because not all drivers support the Video Port Manager.</span></span> <span data-ttu-id="28322-118">Как правило, микшер наложения является наиболее надежным вариантом для видеопортов.</span><span class="sxs-lookup"><span data-stu-id="28322-118">In general, the Overlay Mixer is the most reliable option for video ports.</span></span>

<span data-ttu-id="28322-119">Метод [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) автоматически вставляет микшер оверлея при наличии ПИН-кода президента.</span><span class="sxs-lookup"><span data-stu-id="28322-119">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically inserts the Overlay Mixer if there is a VP pin.</span></span> <span data-ttu-id="28322-120">Если вы создаете граф без использования этого метода, проверьте ПИН-код видеопорта в фильтре записи и, если он существует, подключите его к фильтру микшера наложения, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="28322-120">If you are building the graph without using this method, you should check for a video port pin on the capture filter, and if one is present, connect it to the Overlay Mixer filter, as shown in the following diagram.</span></span>

![Подключение ПИН-кода к видеопорту к фильтру микшера наложения.](images/vidcap11.png)

<span data-ttu-id="28322-122">Для поиска ПИН-кода президента в фильтре записи можно использовать метод [**ICaptureGraphBuilder2:: финдпин**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) :</span><span class="sxs-lookup"><span data-stu-id="28322-122">You can use the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method to search for a VP pin on the capture filter:</span></span>


```C++
hr = pBuild->FindPin(
    pCap,                    // Pointer to the capture filter.
    PINDIR_OUTPUT,           // Look for an output pin.
    &PIN_CATEGORY_VIDEOPORT, // Look for a video port pin.
    NULL,                    // Any media type.
    FALSE,                   // Pin can be connected.
    0,                       // Retrieve the first matching pin.
    &pVPPin                  // Receives a pointer to the pin.
);
```



<span data-ttu-id="28322-123">После добавления микшера наложения на граф вызовите **финдпин** еще раз, чтобы найти ПИН-код 0 в микшере наложения.</span><span class="sxs-lookup"><span data-stu-id="28322-123">After you add the Overlay Mixer to the graph, call **FindPin** again to find pin 0 on the Overlay Mixer.</span></span> <span data-ttu-id="28322-124">ПИН-код 0 всегда является первым входным закреплением фильтра.</span><span class="sxs-lookup"><span data-stu-id="28322-124">Pin 0 is always the first input pin on the filter.</span></span>


```C++
pBuild->FindPin(pOvMix, PINDIR_INPUT, NULL, NULL, TRUE, 0, &pOVPin);
```



<span data-ttu-id="28322-125">Соедините два контакта, вызвав [**играфбуилдер:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).</span><span class="sxs-lookup"><span data-stu-id="28322-125">Connect the two pins by calling [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).</span></span>


```C++
pGraph->Connect(pVPPin, pOvPin);
```



<span data-ttu-id="28322-126">Затем подключите выходное крепление микшера наложения к фильтру модуля подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="28322-126">Then connect the Overlay Mixer's output pin to the Video Renderer filter.</span></span> <span data-ttu-id="28322-127">Видео можно скрыть, вызвав методы [**ивидеовиндов::p UT \_ автоотображения**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) и [**ивидеовиндов::P UT \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) в диспетчере графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="28322-127">You can hide the video by calling the [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) and [**IVideoWindow::put\_Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) methods on the Filter Graph Manager.</span></span>

<span data-ttu-id="28322-128">Для ТВ-тюнеров фильтр записи может также иметь ВБИ PIN (закрепить \_ категорию \_ видеопорт \_ ВБИ).</span><span class="sxs-lookup"><span data-stu-id="28322-128">For TV tuners, the capture filter might also have a video port VBI pin (PIN\_CATEGORY\_VIDEOPORT\_VBI).</span></span> <span data-ttu-id="28322-129">Если да, подключите этот ПИН-код к фильтру [распределителя ВБИ Surface](vbi-surface-allocator.md) .</span><span class="sxs-lookup"><span data-stu-id="28322-129">If so, connect that pin to the [VBI Surface Allocator](vbi-surface-allocator.md) filter.</span></span> <span data-ttu-id="28322-130">Дополнительные сведения см. в разделе [Просмотр скрытых субтитров](viewing-closed-captions.md).</span><span class="sxs-lookup"><span data-stu-id="28322-130">For more information, see [Viewing Closed Captions](viewing-closed-captions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="28322-131">См. также</span><span class="sxs-lookup"><span data-stu-id="28322-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28322-132">Разделы, посвященные расширенному записи</span><span class="sxs-lookup"><span data-stu-id="28322-132">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="28322-133">Использование микшера наложения в видеозаписи</span><span class="sxs-lookup"><span data-stu-id="28322-133">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



