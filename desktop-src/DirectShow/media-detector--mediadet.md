---
description: Детектор мультимедиа (Медиадет)
ms.assetid: 5cdbb6ca-d2c3-4123-b545-198863fed25f
title: Детектор мультимедиа (Медиадет)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f34b1dc267480d3d6ea9efe9b9a743623a917b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104157019"
---
# <a name="media-detector-mediadet"></a><span data-ttu-id="25ec6-103">Детектор мультимедиа (Медиадет)</span><span class="sxs-lookup"><span data-stu-id="25ec6-103">Media Detector (MediaDet)</span></span>

> [!Note]  
> <span data-ttu-id="25ec6-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="25ec6-104">\[Deprecated.</span></span> <span data-ttu-id="25ec6-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="25ec6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="25ec6-106">Объект детектора мультимедиа (Медиадет) получает сведения о форматировании и все еще кадры из исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="25ec6-106">The Media Detector (MediaDet) object retrieves format information and still frames from file sources.</span></span> <span data-ttu-id="25ec6-107">Для работы средства обнаружения носителей не требуется, чтобы диспетчер графа фильтров функционировал.</span><span class="sxs-lookup"><span data-stu-id="25ec6-107">The Media Detector does not require the Filter Graph Manager to function.</span></span> <span data-ttu-id="25ec6-108">Чтобы создать этот объект, вызовите **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="25ec6-108">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="25ec6-109">Идентификатор класса — CLSID \_ медиадет.</span><span class="sxs-lookup"><span data-stu-id="25ec6-109">The class identifier is CLSID\_MediaDet.</span></span>

<span data-ttu-id="25ec6-110">Для чтения™ файлов Windows Media приложение должно предоставить сертификат программного обеспечения, который также называется ключом.</span><span class="sxs-lookup"><span data-stu-id="25ec6-110">To read Windows Media™ files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="25ec6-111">Зарегистрируйте приложение в качестве поставщика ключей через интерфейс **IObjectWithSite** средства обнаружения носителей.</span><span class="sxs-lookup"><span data-stu-id="25ec6-111">Register the application as a key provider through the Media Detector's **IObjectWithSite** interface.</span></span> <span data-ttu-id="25ec6-112">Дополнительные сведения см. [в разделе Разблокировка пакета SDK Windows Media Format](unlocking-the-windows-media-format-sdk.md).</span><span class="sxs-lookup"><span data-stu-id="25ec6-112">For more information, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="25ec6-113">Объект Медиадет предоставляет следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="25ec6-113">The MediaDet object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="25ec6-114">**имедиадет**</span><span class="sxs-lookup"><span data-stu-id="25ec6-114">**IMediaDet**</span></span>](imediadet.md)
-   <span data-ttu-id="25ec6-115">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="25ec6-115">**IObjectWithSite**</span></span>

## <a name="related-topics"></a><span data-ttu-id="25ec6-116">См. также</span><span class="sxs-lookup"><span data-stu-id="25ec6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25ec6-117">Работа с источниками</span><span class="sxs-lookup"><span data-stu-id="25ec6-117">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



