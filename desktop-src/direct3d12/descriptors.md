---
title: Дескрипторы
description: Дескрипторы являются основной единицей привязки для одного ресурса в D3D12.
ms.assetid: f35b5776-46b0-4659-9e61-c6ebfdb55f87
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9576a2d40ade89c9c7a342feb6b069ca1321028e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105019"
---
# <a name="descriptors"></a><span data-ttu-id="efdc5-103">Дескрипторы</span><span class="sxs-lookup"><span data-stu-id="efdc5-103">Descriptors</span></span>

<span data-ttu-id="efdc5-104">Дескрипторы являются основной единицей привязки для одного ресурса в D3D12.</span><span class="sxs-lookup"><span data-stu-id="efdc5-104">Descriptors are the primary unit of binding for a single resource in D3D12.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="efdc5-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="efdc5-105">In this section</span></span>



| <span data-ttu-id="efdc5-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="efdc5-106">Topic</span></span>                                                       | <span data-ttu-id="efdc5-107">Описание</span><span class="sxs-lookup"><span data-stu-id="efdc5-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efdc5-108">Общие сведения о дескрипторах</span><span class="sxs-lookup"><span data-stu-id="efdc5-108">Descriptors Overview</span></span>](descriptors-overview.md)<br/> | <span data-ttu-id="efdc5-109">Дескрипторы создаются вызовами API и определяют ресурсы.</span><span class="sxs-lookup"><span data-stu-id="efdc5-109">Descriptors are created by API calls and identify resources.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="efdc5-110">Создание дескрипторов</span><span class="sxs-lookup"><span data-stu-id="efdc5-110">Creating Descriptors</span></span>](creating-descriptors.md)<br/> | <span data-ttu-id="efdc5-111">Описывает и показывает примеры создания представлений индекса, вершины и буфера констант. ресурс шейдера, целевой объект прорисовки, неупорядоченный доступ, потоковый выход и представления элементов глубины; и пробы.</span><span class="sxs-lookup"><span data-stu-id="efdc5-111">Describes and shows examples for creating index, vertex, and constant buffer views; shader resource, render target, unordered access, stream output and depth-stencil views; and samplers.</span></span> <span data-ttu-id="efdc5-112">Все методы для создания дескрипторов являются свободными потоками.</span><span class="sxs-lookup"><span data-stu-id="efdc5-112">All methods for creating descriptors are free threaded.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="efdc5-113">Копирование дескрипторов</span><span class="sxs-lookup"><span data-stu-id="efdc5-113">Copying Descriptors</span></span>](copying-descriptors.md)<br/>   | <span data-ttu-id="efdc5-114">Методы [**ID3D12Device:: копидескрипторс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) и [**ID3D12Device:: копидескрипторссимпле**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) в интерфейсе устройства используют ЦП для немедленного копирования дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="efdc5-114">The [**ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) and [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) methods on the device interface use the CPU to immediately copy descriptors.</span></span> <span data-ttu-id="efdc5-115">Они могут называться свободными потоками, если несколько потоков в ЦП или GPU не выполняют потенциально конфликтующие записи.</span><span class="sxs-lookup"><span data-stu-id="efdc5-115">They can be called free threaded as long as multiple threads on the CPU or GPU do not perform any potentially conflicting writes.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="efdc5-116">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="efdc5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efdc5-117">Кучи дескрипторов</span><span class="sxs-lookup"><span data-stu-id="efdc5-117">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="efdc5-118">Таблицы дескрипторов</span><span class="sxs-lookup"><span data-stu-id="efdc5-118">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> <dt>

[<span data-ttu-id="efdc5-119">Привязка ресурсов</span><span class="sxs-lookup"><span data-stu-id="efdc5-119">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="efdc5-120">Корневые подписи</span><span class="sxs-lookup"><span data-stu-id="efdc5-120">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





