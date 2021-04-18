---
description: Ресурсы управляемых буферов вершин и буферов индексов не могут быть объявлены динамически при помощи параметра D3DUSAGE \_ dynamic во время создания.
ms.assetid: 440d9d94-3a56-4b34-a5e3-1b4712b078fc
title: Application-Managed ресурсы и стратегии выделения ресурсов (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f5ce23cac4bf46b8580a31d7c6d71fdc3de15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701163"
---
# <a name="application-managed-resources-and-allocation-strategies-direct3d-9"></a><span data-ttu-id="dfb14-103">Application-Managed ресурсы и стратегии выделения ресурсов (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="dfb14-103">Application-Managed Resources and Allocation Strategies (Direct3D 9)</span></span>

<span data-ttu-id="dfb14-104">Ресурсы управляемых буферов вершин и буферов индексов не могут быть объявлены динамически при помощи параметра D3DUSAGE \_ dynamic во время создания.</span><span class="sxs-lookup"><span data-stu-id="dfb14-104">Managed vertex-buffer or index-buffer resources cannot be declared dynamic by specifying D3DUSAGE\_DYNAMIC at creation time.</span></span> <span data-ttu-id="dfb14-105">Это потребует дополнительной копии для каждого изменения содержимого буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="dfb14-105">This would require an additional copy for every modification to the vertex buffer contents.</span></span> <span data-ttu-id="dfb14-106">Динамические буферы вершин предназначены для отрисовки динамической геометрии и данных, извлеченных из двоичных деревьев или других структур данных видимости.</span><span class="sxs-lookup"><span data-stu-id="dfb14-106">Dynamic vertex buffers are intended for rendering dynamic geometry and data pulled in from binary space partitioned trees or other visibility data structures.</span></span> <span data-ttu-id="dfb14-107">Это можно сделать путем предварительного выделения буферов требуемого формата.</span><span class="sxs-lookup"><span data-stu-id="dfb14-107">This can be accomplished by pre-allocating buffers of the desired format.</span></span> <span data-ttu-id="dfb14-108">Затем эти ресурсы отправляются для поддержки приложений, необходимых диспетчеру ресурсов в рамках приложения.</span><span class="sxs-lookup"><span data-stu-id="dfb14-108">These resources are then parceled out to support application needs by a resource manager within the application.</span></span> <span data-ttu-id="dfb14-109">Общее число динамических буферов вершин невелико, так как приложение будет использовать одновременно только несколько различных STRIDE вершин, а другой буфер вершин необходим только для уникальных шагов.</span><span class="sxs-lookup"><span data-stu-id="dfb14-109">The total number of dynamic vertex buffers is small because an application will use simultaneously only a few different vertex strides and because a different vertex buffer is required only for unique strides.</span></span> <span data-ttu-id="dfb14-110">При таком способе управления динамическими ресурсами убедитесь, что высокие требования к ресурсам не снижают производительность приложения.</span><span class="sxs-lookup"><span data-stu-id="dfb14-110">When managing dynamic resources in this way, ensure that high-frequency demands on the resources do not significantly decrease the application's performance.</span></span>

<span data-ttu-id="dfb14-111">При использовании ресурсов, управляемых как Direct3D, так и приложениями, перед созданием ресурсов, управляемых Direct3D, следует выделить ресурсы, управляемые приложением, в \_ памяти D3DPOOL по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dfb14-111">When using resources managed by both Direct3D and applications, allocate application-managed resources in D3DPOOL\_DEFAULT memory prior to creating Direct3D-managed resources.</span></span> <span data-ttu-id="dfb14-112">Это позволяет диспетчеру памяти поддерживать точное количество доступной памяти.</span><span class="sxs-lookup"><span data-stu-id="dfb14-112">This enables the memory manager to maintain an accurate count of available memory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dfb14-113">См. также</span><span class="sxs-lookup"><span data-stu-id="dfb14-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfb14-114">Ресурсы Direct3D</span><span class="sxs-lookup"><span data-stu-id="dfb14-114">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 



