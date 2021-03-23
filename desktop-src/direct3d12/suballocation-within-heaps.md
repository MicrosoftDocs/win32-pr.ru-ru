---
title: Подраспределение в кучах
description: Кучи ресурсов передают данные из ЦП в графический процессор (передача) и из GPU в ЦП (чтение обратно).
ms.assetid: 7E319BCF-FF3F-43CB-9C48-A9DD2A043592
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 701e68e31e698bbf2c955a252bd46876f45d6b7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104079"
---
# <a name="suballocation-within-heaps"></a><span data-ttu-id="3e90f-103">Подраспределение в кучах</span><span class="sxs-lookup"><span data-stu-id="3e90f-103">Suballocation Within Heaps</span></span>

<span data-ttu-id="3e90f-104">Кучи ресурсов передают данные из ЦП в графический процессор (передача) и из GPU в ЦП (чтение обратно).</span><span class="sxs-lookup"><span data-stu-id="3e90f-104">Resource heaps transfer data from the CPU to the GPU (upload), and from the GPU to the CPU (read back).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3e90f-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="3e90f-105">In this section</span></span>



| <span data-ttu-id="3e90f-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="3e90f-106">Topic</span></span>                                                                                       | <span data-ttu-id="3e90f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3e90f-107">Description</span></span>                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e90f-108">Присвоение псевдонимов памяти и наследование данных</span><span class="sxs-lookup"><span data-stu-id="3e90f-108">Memory Aliasing and Data Inheritance</span></span>](memory-aliasing-and-data-inheritance.md)<br/> | <span data-ttu-id="3e90f-109">Размещенный и зарезервированный ресурс может быть псевдонимом физической памяти в куче.</span><span class="sxs-lookup"><span data-stu-id="3e90f-109">Placed and reserved resource may alias physical memory within a heap.</span></span> <span data-ttu-id="3e90f-110">Размещенные ресурсы обеспечивают дополнительные сценарии наследования данных, чем зарезервированные ресурсы, если в куче установлен общий флаг или если ресурсы с псевдонимами имеют полностью определенные макеты памяти.</span><span class="sxs-lookup"><span data-stu-id="3e90f-110">Placed resources enable more data inheritance scenarios than reserved resources when the heap has the shared flag set or when the aliased resources have fully defined memory layouts.</span></span> <br/> |
| [<span data-ttu-id="3e90f-111">Общие кучи</span><span class="sxs-lookup"><span data-stu-id="3e90f-111">Shared Heaps</span></span>](shared-heaps.md)<br/>                                                 | <span data-ttu-id="3e90f-112">Общий доступ удобен для многопроцессных и многоадаптерных архитектур.</span><span class="sxs-lookup"><span data-stu-id="3e90f-112">Sharing is useful for multi-process and multi-adapter architectures.</span></span><br/>                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="3e90f-113">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="3e90f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e90f-114">**ID3D12Device:: CreateHeap**</span><span class="sxs-lookup"><span data-stu-id="3e90f-114">**ID3D12Device::CreateHeap**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap)
</dt> <dt>

[<span data-ttu-id="3e90f-115">**ID3D12Heap**</span><span class="sxs-lookup"><span data-stu-id="3e90f-115">**ID3D12Heap**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[<span data-ttu-id="3e90f-116">Управление памятью</span><span class="sxs-lookup"><span data-stu-id="3e90f-116">Memory Management</span></span>](memory-management.md)
</dt> </dl>

 

 





