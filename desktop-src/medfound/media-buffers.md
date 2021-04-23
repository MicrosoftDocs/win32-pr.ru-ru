---
description: Буферы мультимедиа
ms.assetid: 3ee073ea-7bac-4971-9167-93a4e541ab77
title: Буферы мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87316ea64e24173dfa73f2cc2ff280a1281d50f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105720048"
---
# <a name="media-buffers"></a><span data-ttu-id="858d4-103">Буферы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="858d4-103">Media Buffers</span></span>

<span data-ttu-id="858d4-104">Буфер мультимедиа — это COM-объект, который управляет блоком памяти, обычно для хранения данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="858d4-104">A media buffer is a COM object that manages a block of memory, typically to hold media data.</span></span> <span data-ttu-id="858d4-105">Буферы мультимедиа используются для перемещения данных из одного компонента конвейера в следующий.</span><span class="sxs-lookup"><span data-stu-id="858d4-105">Media buffers are used to move data from one pipeline component to the next.</span></span> <span data-ttu-id="858d4-106">Большинство приложений не используют буферы мультимедиа напрямую, так как сеанс мультимедиа обрабатывает весь поток данных между объектами конвейера.</span><span class="sxs-lookup"><span data-stu-id="858d4-106">Most applications do not use media buffers directly, because the Media Session handles all of the data flow between pipeline objects.</span></span> <span data-ttu-id="858d4-107">Буферы мультимедиа необходимо использовать при написании собственного компонента конвейера или при использовании компонента конвейера напрямую без сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="858d4-107">You must use media buffers if you are writing your own pipeline component, or if you are using a pipeline component directly without the Media Session.</span></span>

<span data-ttu-id="858d4-108">Буферы мультимедиа предоставляют интерфейс [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="858d4-108">Media buffers exposes the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span> <span data-ttu-id="858d4-109">Этот интерфейс предназначен для чтения или записи данных любого типа.</span><span class="sxs-lookup"><span data-stu-id="858d4-109">This interface is designed for reading or writing any type of data.</span></span> <span data-ttu-id="858d4-110">Для несжатых видеокадров требуется специальная обработка, так как они могут храниться в областях Direct3D, расположенных в видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="858d4-110">Uncompressed video frames require special handling, because they might be stored in Direct3D surfaces located in video memory.</span></span>

<span data-ttu-id="858d4-111">Этот раздел содержит следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="858d4-111">This section contains the following topics.</span></span>



| <span data-ttu-id="858d4-112">Раздел</span><span class="sxs-lookup"><span data-stu-id="858d4-112">Topic</span></span>                                                        | <span data-ttu-id="858d4-113">Описание</span><span class="sxs-lookup"><span data-stu-id="858d4-113">Description</span></span>                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="858d4-114">Работа с буферами мультимедиа</span><span class="sxs-lookup"><span data-stu-id="858d4-114">Working with Media Buffers</span></span>](working-with-media-buffers.md) | <span data-ttu-id="858d4-115">Описание общего поведения буферов мультимедиа для всех типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="858d4-115">Describes the general behavior of media buffers for all media types.</span></span> |
| [<span data-ttu-id="858d4-116">Несжатые буферы видео</span><span class="sxs-lookup"><span data-stu-id="858d4-116">Uncompressed Video Buffers</span></span>](uncompressed-video-buffers.md) | <span data-ttu-id="858d4-117">Как работать с буферами мультимедиа, которые содержат кадры видео без сжатия.</span><span class="sxs-lookup"><span data-stu-id="858d4-117">How work with media buffers that contain uncompressed video frames.</span></span>  |
| [<span data-ttu-id="858d4-118">Буфер поверхности DirectX</span><span class="sxs-lookup"><span data-stu-id="858d4-118">DirectX Surface Buffer</span></span>](directx-surface-buffer.md)         | <span data-ttu-id="858d4-119">Описывает, как сохранить поверхность Direct3D в буфере мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="858d4-119">Describes how to store a Direct3D surface in a media buffer.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="858d4-120">См. также</span><span class="sxs-lookup"><span data-stu-id="858d4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="858d4-121">Примитивы Media Foundation</span><span class="sxs-lookup"><span data-stu-id="858d4-121">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



