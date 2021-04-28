---
description: Кмспкаллбасе чистые виртуальные методы. Эти методы должны быть переопределены производными классами.
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: Чистые виртуальные методы Кмспкаллбасе
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8da8530ab3dae737bf1407f00d5d4a415a1437e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094462"
---
# <a name="cmspcallbase-pure-virtual-methods"></a><span data-ttu-id="c1b42-103">Чистые виртуальные методы Кмспкаллбасе</span><span class="sxs-lookup"><span data-stu-id="c1b42-103">CMSPCallBase Pure Virtual Methods</span></span>

<span data-ttu-id="c1b42-104">Эти методы должны быть переопределены производными классами.</span><span class="sxs-lookup"><span data-stu-id="c1b42-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="c1b42-105">Чистые виртуальные методы Кмспкаллбасе</span><span class="sxs-lookup"><span data-stu-id="c1b42-105">CMSPCallBase pure virtual methods</span></span>                                 | <span data-ttu-id="c1b42-106">Описание</span><span class="sxs-lookup"><span data-stu-id="c1b42-106">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1b42-107">**мспкалладдреф**</span><span class="sxs-lookup"><span data-stu-id="c1b42-107">**MSPCallAddRef**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | <span data-ttu-id="c1b42-108">Закрытый метод AddRef для объекта вызова.</span><span class="sxs-lookup"><span data-stu-id="c1b42-108">Private AddRef method for the call object.</span></span>                                                                                              |
| [<span data-ttu-id="c1b42-109">**мспкаллрелеасе**</span><span class="sxs-lookup"><span data-stu-id="c1b42-109">**MSPCallRelease**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | <span data-ttu-id="c1b42-110">Частный метод освобождения для объекта Call.</span><span class="sxs-lookup"><span data-stu-id="c1b42-110">Private Release method for the call object.</span></span>                                                                                             |
| [<span data-ttu-id="c1b42-111">**Ini**</span><span class="sxs-lookup"><span data-stu-id="c1b42-111">**Init**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | <span data-ttu-id="c1b42-112">Вызывается объектом-адресом MSP (в методе [**креатемспкалл**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) для инициализации объекта вызова MSP.</span><span class="sxs-lookup"><span data-stu-id="c1b42-112">Called by the MSP address object (in the method [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) to initialize the MSP call object.</span></span> |
| [<span data-ttu-id="c1b42-113">**Закрытия**</span><span class="sxs-lookup"><span data-stu-id="c1b42-113">**ShutDown**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | <span data-ttu-id="c1b42-114">Вызывается объектом адреса MSP для завершения вызова..</span><span class="sxs-lookup"><span data-stu-id="c1b42-114">Called by the MSP address object to shut down the call..</span></span>                                                                                |
| [<span data-ttu-id="c1b42-115">**интерналкреатестреам**</span><span class="sxs-lookup"><span data-stu-id="c1b42-115">**InternalCreateStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | <span data-ttu-id="c1b42-116">Вызывается методом [**креатестреам**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) для создания объекта потока.</span><span class="sxs-lookup"><span data-stu-id="c1b42-116">Called by [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) to create a stream object.</span></span>                                               |
| [<span data-ttu-id="c1b42-117">**креатестреамобжект**</span><span class="sxs-lookup"><span data-stu-id="c1b42-117">**CreateStreamObject**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | <span data-ttu-id="c1b42-118">Вызывается методом [**интерналкреатестреам**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) для создания объекта потока.</span><span class="sxs-lookup"><span data-stu-id="c1b42-118">Called by [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) to create a stream object.</span></span>                                  |
| [<span data-ttu-id="c1b42-119">**ремовестреам**</span><span class="sxs-lookup"><span data-stu-id="c1b42-119">**RemoveStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | <span data-ttu-id="c1b42-120">Вызывается приложением для удаления потока из вызова</span><span class="sxs-lookup"><span data-stu-id="c1b42-120">Called by the application to remove a stream from the call</span></span>                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="c1b42-121">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="c1b42-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1b42-122">**кмспкаллбасе**</span><span class="sxs-lookup"><span data-stu-id="c1b42-122">**CMSPCallBase**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
