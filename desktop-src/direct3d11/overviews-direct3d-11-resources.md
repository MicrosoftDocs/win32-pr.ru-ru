---
title: Ресурсы
description: В этом разделе описываются аспекты ресурсов Direct3D 11.
ms.assetid: 5b8b1198-73ed-4058-9fc6-a1c43902d732
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9ed73d81d2521fe97b36e6bfc8d71e387f8c9c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104070880"
---
# <a name="resources"></a><span data-ttu-id="72505-103">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="72505-103">Resources</span></span>

<span data-ttu-id="72505-104">Ресурсы предоставляют данные конвейеру и определяют, что отрисовывается во время сцены.</span><span class="sxs-lookup"><span data-stu-id="72505-104">Resources provide data to the pipeline and define what is rendered during your scene.</span></span> <span data-ttu-id="72505-105">Ресурсы могут загружаться из мультимедиа вашей игры или создаваться динамически во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="72505-105">Resources can be loaded from your game media or created dynamically at run time.</span></span> <span data-ttu-id="72505-106">Обычно ресурсы включают данные текстуры, данные вершин и данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="72505-106">Typically, resources include texture data, vertex data, and shader data.</span></span> <span data-ttu-id="72505-107">Большинство приложений Direct3D создают и уничтожают ресурсы в течение всего времени существования.</span><span class="sxs-lookup"><span data-stu-id="72505-107">Most Direct3D applications create and destroy resources extensively throughout their lifespan.</span></span> <span data-ttu-id="72505-108">В этом разделе описываются аспекты ресурсов Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="72505-108">This section describes aspects of Direct3D 11 resources.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="72505-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="72505-109">In this section</span></span>



| <span data-ttu-id="72505-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="72505-110">Topic</span></span>                                                                                             | <span data-ttu-id="72505-111">Описание</span><span class="sxs-lookup"><span data-stu-id="72505-111">Description</span></span>                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72505-112">Общие сведения о ресурсе в Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="72505-112">Introduction to a Resource in Direct3D 11</span></span>](overviews-direct3d-11-resources-intro.md)<br/> | <span data-ttu-id="72505-113">В этом разделе представлены ресурсы Direct3D, такие как буферы и текстуры.</span><span class="sxs-lookup"><span data-stu-id="72505-113">This topic introduces Direct3D resources such as buffers and textures.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="72505-114">Типы ресурсов</span><span class="sxs-lookup"><span data-stu-id="72505-114">Types of Resources</span></span>](overviews-direct3d-11-resources-types.md)<br/>                        | <span data-ttu-id="72505-115">В этом разделе описываются типы ресурсов Direct3D 10, а также новые типы в Direct3D 11, включая структурированные буферы и доступные для записи текстуры и буферы.</span><span class="sxs-lookup"><span data-stu-id="72505-115">This topic describes the types of resources from Direct3D 10, as well as new types in Direct3D 11 including structured buffers and writable textures and buffers.</span></span><br/>                                                                       |
| [<span data-ttu-id="72505-116">Ограничения ресурсов</span><span class="sxs-lookup"><span data-stu-id="72505-116">Resource Limits</span></span>](overviews-direct3d-11-resources-limits.md)<br/>                          | <span data-ttu-id="72505-117">Этот раздел содержит список ресурсов, поддерживаемых Direct3D 11 (в частности, [уровень функций](overviews-direct3d-11-devices-downlevel-intro.md) 11 или 9. x).</span><span class="sxs-lookup"><span data-stu-id="72505-117">This topic contains a list of resources that Direct3D 11 supports (specifically [feature level](overviews-direct3d-11-devices-downlevel-intro.md) 11 or 9.x hardware).</span></span><br/>                                 |
| [<span data-ttu-id="72505-118">Подресурсы</span><span class="sxs-lookup"><span data-stu-id="72505-118">Subresources</span></span>](overviews-direct3d-11-resources-subresources.md)<br/>                       | <span data-ttu-id="72505-119">В этом разделе описываются подресурсы текстуры или части ресурса.</span><span class="sxs-lookup"><span data-stu-id="72505-119">This topic describes texture subresources, or portions of a resource.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="72505-120">Buffers</span><span class="sxs-lookup"><span data-stu-id="72505-120">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)<br/>                                 | <span data-ttu-id="72505-121">Буферы содержат данные, используемые для описания геометрии, индексирования геометрических данных и констант шейдера.</span><span class="sxs-lookup"><span data-stu-id="72505-121">Buffers contain data that is used for describing geometry, indexing geometry information, and shader constants.</span></span> <span data-ttu-id="72505-122">В этом разделе описываются буферы, используемые в Direct3D 11, и ссылки на документацию на основе задач для распространенных сценариев.</span><span class="sxs-lookup"><span data-stu-id="72505-122">This section describes buffers that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span><br/> |
| [<span data-ttu-id="72505-123">Текстуры</span><span class="sxs-lookup"><span data-stu-id="72505-123">Textures</span></span>](overviews-direct3d-11-resources-textures.md)<br/>                               | <span data-ttu-id="72505-124">В этом разделе описываются текстуры, используемые в Direct3D 11, и ссылки на документацию на основе задач для распространенных сценариев.</span><span class="sxs-lookup"><span data-stu-id="72505-124">This section describes textures that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="72505-125">Правила с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="72505-125">Floating-point rules</span></span>](floating-point-rules.md)<br/>                                       | <span data-ttu-id="72505-126">Direct3D 11 поддерживает несколько представлений с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="72505-126">Direct3D 11 supports several floating-point representations.</span></span> <span data-ttu-id="72505-127">Все вычисления с плавающей запятой выполняются в определенном подмножестве 32-битных правил с плавающей запятой одинарной точности IEEE 754.</span><span class="sxs-lookup"><span data-stu-id="72505-127">All floating-point computations operate under a defined subset of the IEEE 754 32-bit single precision floating-point rules.</span></span><br/>                                               |
| [<span data-ttu-id="72505-128">Мозаичные ресурсы</span><span class="sxs-lookup"><span data-stu-id="72505-128">Tiled resources</span></span>](tiled-resources.md)<br/>                                                 | <span data-ttu-id="72505-129">Мозаичные ресурсы можно рассматривать как крупные логические ресурсы, использующие небольшие объемы физической памяти.</span><span class="sxs-lookup"><span data-stu-id="72505-129">Tiled resources can be thought of as large logical resources that use small amounts of physical memory.</span></span><br/>                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="72505-130">См. также</span><span class="sxs-lookup"><span data-stu-id="72505-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72505-131">Руководство по программированию для Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="72505-131">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

 





