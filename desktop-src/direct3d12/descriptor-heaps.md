---
title: Кучи дескрипторов
description: Куча дескрипторов — это набор смежных выделений дескрипторов, по одному выделению для каждого из них.
ms.assetid: 04d3facf-21ec-45ca-ad9b-78fdcddc7136
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f19821cff5e8730c376e5c80fef07e67974d31d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104667"
---
# <a name="descriptor-heaps"></a><span data-ttu-id="75ec1-103">Кучи дескрипторов</span><span class="sxs-lookup"><span data-stu-id="75ec1-103">Descriptor Heaps</span></span>

<span data-ttu-id="75ec1-104">Куча дескрипторов — это набор смежных выделений дескрипторов, по одному выделению для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="75ec1-104">A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="75ec1-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="75ec1-105">In this section</span></span>



| <span data-ttu-id="75ec1-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="75ec1-106">Topic</span></span>                                                                                             | <span data-ttu-id="75ec1-107">Описание</span><span class="sxs-lookup"><span data-stu-id="75ec1-107">Description</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75ec1-108">Общие сведения о кучах дескрипторов</span><span class="sxs-lookup"><span data-stu-id="75ec1-108">Descriptor Heaps Overview</span></span>](descriptor-heaps-overview.md)<br/>                             | <span data-ttu-id="75ec1-109">Кучи дескрипторов содержат множество типов объектов, которые не являются частью объекта состояния конвейера (PSO), например представления ресурсов шейдера (СРВС), неупорядоченные представления доступа (Уавс), представления постоянного буфера (КБВС) и пробы.</span><span class="sxs-lookup"><span data-stu-id="75ec1-109">Descriptor heaps contain many object types that are not part of a Pipeline State Object (PSO), such as Shader Resource Views (SRVs), Unordered Access Views (UAVs), Constant Buffer Views (CBVs), and Samplers.</span></span> <br/>                |
| [<span data-ttu-id="75ec1-110">Уровни оборудования</span><span class="sxs-lookup"><span data-stu-id="75ec1-110">Hardware Tiers</span></span>](hardware-support.md)<br/>                                                 | <span data-ttu-id="75ec1-111">Уровни оборудования от уровня 1 до уровня 3 увеличивают ресурсы, доступные для конвейера.</span><span class="sxs-lookup"><span data-stu-id="75ec1-111">The levels of hardware from Tier 1 to Tier 3 have increasing resources available to the pipeline.</span></span> <br/>                                                                                                                              |
| [<span data-ttu-id="75ec1-112">Видимые кучи дескрипторов шейдеров</span><span class="sxs-lookup"><span data-stu-id="75ec1-112">Shader Visible Descriptor Heaps</span></span>](shader-visible-descriptor-heaps.md)<br/>                 | <span data-ttu-id="75ec1-113">Видимые кучи дескрипторов шейдеров — это кучи дескрипторов, на которые могут ссылаться шейдеры через таблицы дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="75ec1-113">Shader visible descriptor heaps, are descriptor heaps that can be referenced by shaders through descriptor tables.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="75ec1-114">Видимые кучи дескрипторов без шейдеров</span><span class="sxs-lookup"><span data-stu-id="75ec1-114">Non Shader Visible Descriptor Heaps</span></span>](non-shader-visible-descriptor-heaps.md)<br/>         | <span data-ttu-id="75ec1-115">Шейдеры не могут ссылаться на некоторые кучи дескрипторов через таблицы дескрипторов, но существуют либо для помощи приложению в промежуточной среде перед записью списка команд, либо из-за отсутствия в ней видимой кучи.</span><span class="sxs-lookup"><span data-stu-id="75ec1-115">Some descriptor heaps cannot be referenced by shaders through descriptor tables, but exist either to assist the app in staging the descriptors prior to recording a command list or because no shader-visible heap is required.</span></span><br/> |
| [<span data-ttu-id="75ec1-116">Создание куч дескрипторов</span><span class="sxs-lookup"><span data-stu-id="75ec1-116">Creating Descriptor Heaps</span></span>](creating-descriptor-heaps.md)<br/>                             | <span data-ttu-id="75ec1-117">Чтобы создать и настроить кучу дескрипторов, необходимо выбрать тип кучи дескрипторов, определить количество содержащихся в нем дескрипторов и установить флаги, указывающие, является ли он видимым и/или видимым для шейдера.</span><span class="sxs-lookup"><span data-stu-id="75ec1-117">To create and configure a descriptor heap, you must select a descriptor heap type, determine how many descriptors it contains, and set flags that indicate whether it is CPU visible and/or shader visible.</span></span> <br/>                    |
| [<span data-ttu-id="75ec1-118">Задание и заполнение куч дескрипторов</span><span class="sxs-lookup"><span data-stu-id="75ec1-118">Setting and Populating Descriptor Heaps</span></span>](setting-descriptor-heaps.md)<br/>                | <span data-ttu-id="75ec1-119">Типы кучи дескрипторов, которые могут быть заданы в списке команд, — это те, которые содержат дескрипторы, для которых можно использовать таблицы (не более одного одновременно).</span><span class="sxs-lookup"><span data-stu-id="75ec1-119">The descriptor heap types that can be set on a command list are those that contain descriptors for which descriptor tables can be used (at most one of each at a time).</span></span> <br/>                                                        |
| [<span data-ttu-id="75ec1-120">Сводка по настройке кучи дескрипторов</span><span class="sxs-lookup"><span data-stu-id="75ec1-120">Descriptor Heap Configurability Summary</span></span>](descriptor-heap-configurability-summary.md)<br/> | <span data-ttu-id="75ec1-121">В следующей таблице представлены сведения о поддержке шейдера и видимой кучи без шейдера.</span><span class="sxs-lookup"><span data-stu-id="75ec1-121">The following table summarizes information about Shader and non-Shader visible heap support.</span></span><br/>                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="75ec1-122">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="75ec1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75ec1-123">Дескрипторы</span><span class="sxs-lookup"><span data-stu-id="75ec1-123">Descriptors</span></span>](descriptors.md)
</dt> <dt>

[<span data-ttu-id="75ec1-124">Таблицы дескрипторов</span><span class="sxs-lookup"><span data-stu-id="75ec1-124">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> <dt>

[<span data-ttu-id="75ec1-125">**ID3D12DescriptorHeap**</span><span class="sxs-lookup"><span data-stu-id="75ec1-125">**ID3D12DescriptorHeap**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)
</dt> <dt>

[<span data-ttu-id="75ec1-126">Привязка ресурсов</span><span class="sxs-lookup"><span data-stu-id="75ec1-126">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="75ec1-127">Корневые подписи</span><span class="sxs-lookup"><span data-stu-id="75ec1-127">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





