---
title: Управление памятью в Direct3D 12
description: Переход на D3D12 включает в себя правильную синхронизацию и управление местонахождение памяти.
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b8091c2893f8906fe2ab5baadbf1288a1474cd
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481809"
---
# <a name="memory-management-in-direct3d-12"></a><span data-ttu-id="fdd15-103">Управление памятью в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="fdd15-103">Memory Management in Direct3D 12</span></span>

<span data-ttu-id="fdd15-104">Переход на D3D12 включает в себя правильную синхронизацию и управление местонахождение памяти.</span><span class="sxs-lookup"><span data-stu-id="fdd15-104">Moving to D3D12 involves doing proper synchronization and management of memory residency.</span></span> <span data-ttu-id="fdd15-105">Управление памятью местонахождение означает, что необходимо выполнить еще больше синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fdd15-105">Managing memory residency means even more synchronization must be done.</span></span> <span data-ttu-id="fdd15-106">В этом разделе описываются стратегии управления памятью и подраспределение в кучах и буферах.</span><span class="sxs-lookup"><span data-stu-id="fdd15-106">This section covers memory management strategies, and suballocation within heaps and buffers.</span></span>

-   [<span data-ttu-id="fdd15-107">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="fdd15-107">In this section</span></span>](#in-this-section)
-   [<span data-ttu-id="fdd15-108">См. также</span><span class="sxs-lookup"><span data-stu-id="fdd15-108">Related topics</span></span>](#related-topics)

## <a name="in-this-section"></a><span data-ttu-id="fdd15-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="fdd15-109">In this section</span></span>



| <span data-ttu-id="fdd15-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="fdd15-110">Topic</span></span>                                                                       | <span data-ttu-id="fdd15-111">Описание</span><span class="sxs-lookup"><span data-stu-id="fdd15-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fdd15-112">Стратегии управления памятью</span><span class="sxs-lookup"><span data-stu-id="fdd15-112">Memory Management Strategies</span></span>](memory-management-strategies.md)<br/> | <span data-ttu-id="fdd15-113">Диспетчер памяти для Direct3D 12 может очень усложнить работу со всеми различными уровнями поддержки, для сетевых карт, а также с существенным спектром различий в архитектуре между адаптерами GPU.</span><span class="sxs-lookup"><span data-stu-id="fdd15-113">A memory manager for Direct3D 12 could get very complicated quickly with all the different tiers of support, for UMA or discrete (non-UMA) adapters, and with a considerable range of architecture differences between GPU adapters.</span></span><br/> <span data-ttu-id="fdd15-114">Рекомендуемой стратегией для управления памятью Direct3D 12, описанной в этом разделе, является классификация, бюджет и поток.</span><span class="sxs-lookup"><span data-stu-id="fdd15-114">The recommended strategy for Direct3D 12 memory management , described in this section, is "classify, budget and stream".</span></span><br/> |
| [<span data-ttu-id="fdd15-115">Подраспределение в буферах</span><span class="sxs-lookup"><span data-stu-id="fdd15-115">Suballocation Within Buffers</span></span>](large-buffers.md)<br/>                | <span data-ttu-id="fdd15-116">Буферы имеют все функции, необходимые в D3D12 для того, чтобы приложения могли передавать большой диапазон временных данных из ЦП в GPU.</span><span class="sxs-lookup"><span data-stu-id="fdd15-116">Buffers have all the features necessary in D3D12 for applications to transfer a large range of transient data from the CPU to the GPU.</span></span> <span data-ttu-id="fdd15-117">В этом разделе рассматриваются четыре распространенных сценария использования ресурсов и буферов и управления ими.</span><span class="sxs-lookup"><span data-stu-id="fdd15-117">This section covers four common scenarios for the use and management of resources and buffers.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="fdd15-118">Подраспределение в кучах</span><span class="sxs-lookup"><span data-stu-id="fdd15-118">Suballocation Within Heaps</span></span>](suballocation-within-heaps.md)<br/>     | <span data-ttu-id="fdd15-119">Кучи ресурсов передают данные из ЦП в графический процессор (передача) и из GPU в ЦП (чтение обратно).</span><span class="sxs-lookup"><span data-stu-id="fdd15-119">Resource heaps transfer data from the CPU to the GPU (upload), and from the GPU to the CPU (read back).</span></span> <br/>                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="fdd15-120">Размещение</span><span class="sxs-lookup"><span data-stu-id="fdd15-120">Residency</span></span>](residency.md)<br/>                                       | <span data-ttu-id="fdd15-121">Объект считается *резидентным* , когда он доступен для GPU.</span><span class="sxs-lookup"><span data-stu-id="fdd15-121">An object is considered to be *resident* when it is accessible by the GPU.</span></span><br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="fdd15-122">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="fdd15-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdd15-123">Руководство по программированию для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="fdd15-123">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="fdd15-124">Привязка ресурсов</span><span class="sxs-lookup"><span data-stu-id="fdd15-124">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 





