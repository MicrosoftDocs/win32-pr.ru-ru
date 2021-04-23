---
description: 'Когда устройство успешно сбрасывается (IDirect3DDevice9:: Reset) или создается (IDirect3D9:: Креатедевице) в полноэкранных операциях, объект Direct3D, создавший устройство, помечается как владелец всех адаптеров в этой системе.'
ms.assetid: df3b6ed7-830b-4635-9295-fff05cc35891
title: Операции Multiple-Monitor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04427db6c91ff85706040589a89f6fdcfb3761e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710628"
---
# <a name="multiple-monitor-operations-direct3d-9"></a><span data-ttu-id="a323a-103">Операции Multiple-Monitor (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a323a-103">Multiple-Monitor Operations (Direct3D 9)</span></span>

<span data-ttu-id="a323a-104">Когда устройство успешно сбрасывается ([**IDirect3DDevice9:: Reset**](/windows/desktop/api)) или создается ([**IDirect3D9:: креатедевице**](/windows/desktop/api)) в полноэкранных операциях, объект Direct3D, создавший устройство, помечается как владелец всех адаптеров в этой системе.</span><span class="sxs-lookup"><span data-stu-id="a323a-104">When a device is successfully reset ([**IDirect3DDevice9::Reset**](/windows/desktop/api)) or created ([**IDirect3D9::CreateDevice**](/windows/desktop/api)) in full-screen operations, the Direct3D object that created the device is marked as owning all adapters on that system.</span></span> <span data-ttu-id="a323a-105">Это состояние известно как монопольный режим, а объект Direct3D владеет монопольным режимом.</span><span class="sxs-lookup"><span data-stu-id="a323a-105">This state is known as exclusive mode, and the Direct3D object owns exclusive mode.</span></span> <span data-ttu-id="a323a-106">Режим монопольного доступа означает, что устройства, созданные любым другим объектом Direct3D, не могут предпринимать полноэкранные операции и выделять видеопамять.</span><span class="sxs-lookup"><span data-stu-id="a323a-106">Exclusive mode means that devices created by any other Direct3D object can neither assume full-screen operations nor allocate video memory.</span></span> <span data-ttu-id="a323a-107">Кроме того, когда объект Direct3D предполагает монопольный режим, все устройства, кроме тех, которые находятся в полноэкранном режиме, помещаются в состояние «утрачено».</span><span class="sxs-lookup"><span data-stu-id="a323a-107">In addition, when a Direct3D object assumes exclusive mode, all devices other than the one that went full-screen are placed in lost state.</span></span> <span data-ttu-id="a323a-108">Дополнительные сведения см. в разделе [потерянные устройства (Direct3D 9)](lost-devices.md).</span><span class="sxs-lookup"><span data-stu-id="a323a-108">For details, see [Lost Devices (Direct3D 9)](lost-devices.md).</span></span>

<span data-ttu-id="a323a-109">Наряду с монопольным режимом объект Direct3D сообщает о окне фокуса, которое будет использоваться устройством.</span><span class="sxs-lookup"><span data-stu-id="a323a-109">Along with exclusive mode, the Direct3D object is informed of the focus window that the device will use.</span></span> <span data-ttu-id="a323a-110">Монопольный режим освобождается, когда окончательное полноэкранное устройство, принадлежащее этому объекту Direct3D, либо сбрасывается в оконный режим, либо уничтожается.</span><span class="sxs-lookup"><span data-stu-id="a323a-110">Exclusive mode is released when the final full-screen device owned by that Direct3D object is either reset to windowed mode or destroyed.</span></span>

<span data-ttu-id="a323a-111">Устройства можно разделить на две категории, когда объект Direct3D владеет монопольным режимом.</span><span class="sxs-lookup"><span data-stu-id="a323a-111">Devices can be divided into two categories when a Direct3D object owns exclusive mode.</span></span> <span data-ttu-id="a323a-112">Первая категория устройств имеет следующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="a323a-112">The first category of devices have the following characteristics.</span></span>

-   <span data-ttu-id="a323a-113">Они создаются с помощью того же объекта Direct3D, который создал устройство в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="a323a-113">They are created by the same Direct3D object that created the device that is full-screen.</span></span>
-   <span data-ttu-id="a323a-114">Они имеют то же окно фокуса, что и устройство, которое находится в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="a323a-114">They have the same focus window as the device that is full-screen.</span></span>
-   <span data-ttu-id="a323a-115">Они представляют разные адаптеры из любого полноэкранного устройства.</span><span class="sxs-lookup"><span data-stu-id="a323a-115">They represent a different adapter from any full-screen device.</span></span>

<span data-ttu-id="a323a-116">Устройства в этой категории не имеют ограничений, касающихся их возможности сброса или создания и не находятся в состоянии «потеря».</span><span class="sxs-lookup"><span data-stu-id="a323a-116">Devices in this category have no restrictions concerning their ability to be reset or created, and they are not placed in lost state.</span></span> <span data-ttu-id="a323a-117">Устройства в этой категории можно даже перевести в полноэкранный режим.</span><span class="sxs-lookup"><span data-stu-id="a323a-117">Devices in this category can even be put into full-screen mode.</span></span>

<span data-ttu-id="a323a-118">Устройства, которые не входят в первую категорию — устройства, созданные другим объектом Direct3D, созданные в другом окне фокуса и созданные для адаптера с уже полноэкранным устройством, не могут быть сброшены и остаются в состоянии потери до тех пор, пока не будет утрачен монопольный режим.</span><span class="sxs-lookup"><span data-stu-id="a323a-118">Devices that do not fall in the first category - devices created by another Direct3D object, created with a different focus window, and created for an adapter with a device that is already full-screen - cannot be reset and remain in lost state until the exclusive mode is lost.</span></span> <span data-ttu-id="a323a-119">В результате приложение с несколькими мониторами может размещать несколько устройств в полноэкранном режиме, но только если все эти устройства предназначены для разных адаптеров, созданы одним и тем же объектом Direct3D и совместно используют одно и то же окно фокуса.</span><span class="sxs-lookup"><span data-stu-id="a323a-119">As a result, a multiple-monitor application can place several devices in full-screen mode, but only if all these devices are for different adapters, were created by the same Direct3D object, and share the same focus window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a323a-120">См. также</span><span class="sxs-lookup"><span data-stu-id="a323a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a323a-121">Представление сцены</span><span class="sxs-lookup"><span data-stu-id="a323a-121">Presenting a Scene</span></span>](presenting-a-scene.md)
</dt> </dl>

 

 



