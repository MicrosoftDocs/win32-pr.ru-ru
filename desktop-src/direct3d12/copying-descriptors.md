---
title: Копирование дескрипторов
description: Методы ID3D12Device Копидескрипторс и ID3D12Device Копидескрипторссимпле в интерфейсе устройства используют ЦП для немедленного копирования дескрипторов.
ms.assetid: 65AE4D96-6221-46B5-BF55-F86479FCF97C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14fdec6c76f29800f2a0e42bde76b32ebc794275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104083"
---
# <a name="copying-descriptors"></a><span data-ttu-id="79886-103">Копирование дескрипторов</span><span class="sxs-lookup"><span data-stu-id="79886-103">Copying Descriptors</span></span>

<span data-ttu-id="79886-104">Методы [**ID3D12Device:: копидескрипторс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) и [**ID3D12Device:: копидескрипторссимпле**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) в интерфейсе устройства используют ЦП для немедленного копирования дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="79886-104">The [**ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) and [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) methods on the device interface use the CPU to immediately copy descriptors.</span></span> <span data-ttu-id="79886-105">Они могут называться свободными потоками, если несколько потоков в ЦП или GPU не выполняют потенциально конфликтующие записи.</span><span class="sxs-lookup"><span data-stu-id="79886-105">They can be called free threaded as long as multiple threads on the CPU or GPU do not perform any potentially conflicting writes.</span></span>

## <a name="copying-descriptors-immediately-cpu-timeline"></a><span data-ttu-id="79886-106">Немедленное копирование дескрипторов (временная шкала ЦП)</span><span class="sxs-lookup"><span data-stu-id="79886-106">Copying Descriptors Immediately (CPU Timeline)</span></span>

<span data-ttu-id="79886-107">Число исходных дескрипторов (для копирования из), заданных в виде набора диапазонов дескрипторов, должно равняться количеству целевых дескрипторов (для копирования в), указанных в виде отдельного набора диапазонов дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="79886-107">The number of source descriptors (to copy from), specified as a set of descriptor ranges, must equal the number of destination descriptors (to copy to), specified as a separate set of descriptor ranges.</span></span> <span data-ttu-id="79886-108">Исходные и конечные диапазоны в противном случае не должны выровняться.</span><span class="sxs-lookup"><span data-stu-id="79886-108">The source and destination ranges do not otherwise have to line up.</span></span> <span data-ttu-id="79886-109">Например, разреженный набор дескрипторов может быть скопирован в непрерывное назначение, наоборот или в некоторой комбинации.</span><span class="sxs-lookup"><span data-stu-id="79886-109">For example, a sparse set of descriptors could be copied to a contiguous destination, vice versa, or in some combination.</span></span>

<span data-ttu-id="79886-110">В операцию копирования можно вовлечение нескольких куч дескриптора — как источника, так и назначения.</span><span class="sxs-lookup"><span data-stu-id="79886-110">Multiple descriptor heaps can be involved in the copy operation, both as source and destination.</span></span> <span data-ttu-id="79886-111">Использование дескрипторов дескрипторов в качестве параметров означает, что методы копирования не важны для тех куч, в которых находится данный дескриптор, — они являются всего лишь памятью.</span><span class="sxs-lookup"><span data-stu-id="79886-111">The use of descriptor handles as parameters means the copy methods don’t care about which heaps any given descriptor lies in – they are all just memory.</span></span>

<span data-ttu-id="79886-112">Типы кучи дескрипторов, копируемые из и в, должны совпадать, поэтому методы принимают в качестве входных данных один тип кучи дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="79886-112">The descriptor heap types being copied from and to must match, so the methods take a single descriptor heap type as input.</span></span> <span data-ttu-id="79886-113">Драйверу необходимо знать тип кучи всех дескрипторов в данной операции копирования, чтобы он знал, какой размер данных участвует в операции копирования.</span><span class="sxs-lookup"><span data-stu-id="79886-113">The driver needs to know the heap type of all the descriptors in the given copy operation, so it knows what size of data is involved in the copy operation.</span></span> <span data-ttu-id="79886-114">Драйверу также может потребоваться выполнить пользовательскую работу по копированию, если данный тип кучи дескрипторов гарантирует его — подробности реализации.</span><span class="sxs-lookup"><span data-stu-id="79886-114">The driver might also need to do custom copying work if a given descriptor heap type warrants it – an implementation detail.</span></span> <span data-ttu-id="79886-115">Обратите внимание, что дескрипторы дескрипторов сами по себе не определяют тип, на который они указывают. Поэтому для операции копирования требуется дополнительный параметр.</span><span class="sxs-lookup"><span data-stu-id="79886-115">Note that descriptor handles themselves do not otherwise identify what type they are pointing to; therefore, an additional parameter is required for the copy operation.</span></span>

<span data-ttu-id="79886-116">Альтернативный API для [**копидескрипторс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) предоставляется для простого случая копирования одного диапазона дескрипторов из одного расположения в другое – [**копидескрипторссимпле**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple).</span><span class="sxs-lookup"><span data-stu-id="79886-116">An alternative API to [**CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) is provided for the simple case of copying a single range of descriptors from one location to another – [**CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple).</span></span>

<span data-ttu-id="79886-117">Для этих методов копирования дескрипторов, основанных на устройствах (временной шкале ЦП), исходные дескрипторы должны исходить из кучи-видимого нешейдера.</span><span class="sxs-lookup"><span data-stu-id="79886-117">For these device based (CPU timeline) descriptor copy methods, source descriptors must come from a non-shader visible descriptor heap.</span></span> <span data-ttu-id="79886-118">Конечные дескрипторы могут находиться в любой куче дескрипторов, видимой для ЦП (шейдер видимым или нет).</span><span class="sxs-lookup"><span data-stu-id="79886-118">The destination descriptors can be in any descriptor heap that is CPU visible (shader visible or not).</span></span>

## <a name="related-topics"></a><span data-ttu-id="79886-119">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="79886-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79886-120">Дескрипторы</span><span class="sxs-lookup"><span data-stu-id="79886-120">Descriptors</span></span>](descriptors.md)
</dt> </dl>

 

 




