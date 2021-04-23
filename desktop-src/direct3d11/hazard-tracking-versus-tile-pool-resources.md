---
title: Отслеживание рисков и ресурсы пула плиток
description: Для ресурсов без мозаичного разбиения Direct3D может предотвратить определенные условия опасности во время подготовки к просмотру, но так как отслеживание угроз будет на уровне плитки для мозаичных ресурсов, отслеживание условий угрозы во время отрисовки мозаичных ресурсов может оказаться слишком дорогостоящим.
ms.assetid: 4106BAB9-3E0C-48F1-B7E2-565A65DBC78F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c75dcd11cb5e49f165105bd932854e36b37308cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410674"
---
# <a name="hazard-tracking-versus-tile-pool-resources"></a><span data-ttu-id="a2d66-103">Отслеживание рисков и ресурсы пула плиток</span><span class="sxs-lookup"><span data-stu-id="a2d66-103">Hazard tracking versus tile pool resources</span></span>

<span data-ttu-id="a2d66-104">Для ресурсов без мозаичного разбиения Direct3D может предотвратить определенные условия опасности во время подготовки к просмотру, но так как отслеживание угроз будет на уровне плитки для мозаичных ресурсов, отслеживание условий угрозы во время отрисовки мозаичных ресурсов может оказаться слишком дорогостоящим.</span><span class="sxs-lookup"><span data-stu-id="a2d66-104">For non-tiled resources, Direct3D can prevent certain hazard conditions during rendering, but because hazard tracking would be at a tile level for tiled resources, tracking hazard conditions during rendering of tiled resources might be too expensive.</span></span>

<span data-ttu-id="a2d66-105">Например, для ресурсов, не являющихся мозаичными, среда выполнения не позволяет привязывать любой заданный подресурс в качестве входных данных (например, Шадерресаурцевиев) и в качестве выходных данных (например, Рендертаржетвиев) в то же время.</span><span class="sxs-lookup"><span data-stu-id="a2d66-105">For example, for non-tiled resources, the runtime doesn't allow any given SubResource to be bound as an input (such as a ShaderResourceView) and as an output (such as a RenderTargetView) at the same time.</span></span> <span data-ttu-id="a2d66-106">При обнаружении такого случая среда выполнения отменяет привязку входных данных.</span><span class="sxs-lookup"><span data-stu-id="a2d66-106">If such a case is encountered, the runtime unbinds the input.</span></span> <span data-ttu-id="a2d66-107">Эти затраты на отслеживание в среде выполнения недешево и выполняются на уровне подресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2d66-107">This tracking overhead in the runtime is cheap and is done at the SubResource level.</span></span> <span data-ttu-id="a2d66-108">Одно из преимуществ этих служебных данных отслеживания заключается в максимальном сокращении вероятности случайной зависимости приложений от порядка выполнения аппаратных шейдеров.</span><span class="sxs-lookup"><span data-stu-id="a2d66-108">One of the benefits of this tracking overhead is to minimize the chances of applications accidentally depending on hardware shader execution order.</span></span> <span data-ttu-id="a2d66-109">Порядок выполнения аппаратных шейдеров может меняться если и не на определенном графическом процессоре (GPU), то определенно на разных графических процессорах.</span><span class="sxs-lookup"><span data-stu-id="a2d66-109">Hardware shader execution order can vary if not on a given graphics processing unit (GPU), then certainly across different GPUs.</span></span>

<span data-ttu-id="a2d66-110">Отслеживание привязки ресурсов может оказаться слишком дорогим для мозаичного заполнения ресурсов, так как отслеживание выполняется на плитке.</span><span class="sxs-lookup"><span data-stu-id="a2d66-110">Tracking how resources are bound might be too expensive for tiled resources because tracking is at a tile level.</span></span> <span data-ttu-id="a2d66-111">Возникли новые проблемы, например, например, при невозможности пропускной попытки отобразить Рендертаржетвиев с одной плиткой, сопоставленной с несколькими областями в рабочей области одновременно.</span><span class="sxs-lookup"><span data-stu-id="a2d66-111">New issues arise such as possibly validating away attempts to render to an RenderTargetView with one tile mapped to multiple areas in the surface simultaneously.</span></span> <span data-ttu-id="a2d66-112">Если такое отслеживание рисков по плиткам окажется слишком требовательным для среды выполнения, его следовало бы использовать хотя бы на уровне отладки.</span><span class="sxs-lookup"><span data-stu-id="a2d66-112">If it turns out this per-tile hazard tracking is too expensive for the runtime, ideally this would at least be an option in the debug layer.</span></span>

<span data-ttu-id="a2d66-113">Приложение должно сообщить видеодрайверу о том, что он выдал операцию записи или чтения в мозаичном ресурсе, который ссылается на память пула плиток, на которую также будут ссылаться отдельные ресурсы в предстоящих операциях чтения или записи, прежде чем можно будет начать выполнение следующих операций.</span><span class="sxs-lookup"><span data-stu-id="a2d66-113">An application must inform the display driver when it has issued a write or read operation to a tiled resource that references tile pool memory that will also be referenced by separate tiled resources in upcoming read or write operations that it is expecting the first operation to complete before the following operations can begin.</span></span> <span data-ttu-id="a2d66-114">Дополнительные сведения об этом условии см. в разделе [**ID3D11DeviceContext2:: тиледресаурцебарриер**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) remarks.</span><span class="sxs-lookup"><span data-stu-id="a2d66-114">For more info about this condition, see [**ID3D11DeviceContext2::TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) remarks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2d66-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a2d66-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2d66-116">Сопоставления в пуле плиток</span><span class="sxs-lookup"><span data-stu-id="a2d66-116">Mappings are into a tile pool</span></span>](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




