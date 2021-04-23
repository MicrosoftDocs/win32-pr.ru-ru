---
title: Функции Direct3D 11,3
description: В следующих разделах описываются функциональные возможности, добавленные в Direct3D 11,3. Эти функции также доступны в Direct3D 12.
ms.assetid: CA79A315-22C4-4141-8E66-89C0DCF29191
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc256b9b85dd807e2e6c923affdec496fe92e075
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104414224"
---
# <a name="direct3d-113-features"></a><span data-ttu-id="5ec75-104">Функции Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="5ec75-104">Direct3D 11.3 Features</span></span>

<span data-ttu-id="5ec75-105">В следующих разделах описываются функциональные возможности, добавленные в Direct3D 11,3.</span><span class="sxs-lookup"><span data-stu-id="5ec75-105">The following sections describe the functionality has been added in Direct3D 11.3.</span></span> <span data-ttu-id="5ec75-106">Эти функции также доступны в Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="5ec75-106">These features are also available in Direct3D 12.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="5ec75-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="5ec75-107">In this section</span></span>



| <span data-ttu-id="5ec75-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="5ec75-108">Topic</span></span>                                                                                               | <span data-ttu-id="5ec75-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5ec75-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ec75-110">Консервативная растеризация</span><span class="sxs-lookup"><span data-stu-id="5ec75-110">Conservative Rasterization</span></span>](conservative-rasterization.md)<br/>                             | <span data-ttu-id="5ec75-111">Консервативная растрирование добавляет некоторую степень уверенности в отрисовку пикселей, что полезно для алгоритмов обнаружения столкновений.</span><span class="sxs-lookup"><span data-stu-id="5ec75-111">Conservative rasterization adds some certainty to pixel rendering, which is helpful in particular to collision detection algorithms.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="5ec75-112">Сопоставление текстур по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5ec75-112">Default Texture Mapping</span></span>](default-texture-mapping.md)<br/>                                   | <span data-ttu-id="5ec75-113">Использование сопоставления текстур по умолчанию сокращает время копирования и использования памяти при совместном использовании данных изображений между GPU и ЦП.</span><span class="sxs-lookup"><span data-stu-id="5ec75-113">The use of default texture mapping reduces copying and memory usage while sharing image data between the GPU and the CPU.</span></span> <span data-ttu-id="5ec75-114">Однако его следует использовать только в конкретных ситуациях.</span><span class="sxs-lookup"><span data-stu-id="5ec75-114">However, it should only be used in specific situations.</span></span> <span data-ttu-id="5ec75-115">Стандартный макет свиззле позволяет избежать копирования или группирующие данных в нескольких макетах.</span><span class="sxs-lookup"><span data-stu-id="5ec75-115">The standard swizzle layout avoids copying or swizzling data in multiple layouts.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="5ec75-116">Представления порядка программной прорисовки</span><span class="sxs-lookup"><span data-stu-id="5ec75-116">Rasterizer Order Views</span></span>](rasterizer-order-views.md)<br/>                                     | <span data-ttu-id="5ec75-117">В упорядоченных представлениях средства растеризации (РОВС) разрешается, что код шейдера пикселей помечает привязки UAV с помощью объявления, изменяющего нормальные требования к порядку результатов графического конвейера для Уавс.</span><span class="sxs-lookup"><span data-stu-id="5ec75-117">Rasterizer ordered views (ROVs) allow pixel shader code to mark UAV bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span> <span data-ttu-id="5ec75-118">Это позволяет использовать алгоритмы независимой прозрачности заказов (OIT), что дает гораздо более лучшие результаты визуализации, когда несколько прозрачных объектов находятся в разных строках в представлении.</span><span class="sxs-lookup"><span data-stu-id="5ec75-118">This enables Order Independent Transparency (OIT) algorithms to work, which give much better rendering results when multiple transparent objects are in line with each other in a view.</span></span> <br/> |
| [<span data-ttu-id="5ec75-119">Контрольное значение трафарета в шейдере</span><span class="sxs-lookup"><span data-stu-id="5ec75-119">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)<br/> | <span data-ttu-id="5ec75-120">Включение шейдера пикселей для вывода значения ссылки на набор элементов вместо использования указанного API-интерфейса обеспечивает очень точный контроль над операциями с набором элементов.</span><span class="sxs-lookup"><span data-stu-id="5ec75-120">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span><br/>                                                                                                                                                                                                              |
| [<span data-ttu-id="5ec75-121">Загружаются неупорядоченные представления доступа</span><span class="sxs-lookup"><span data-stu-id="5ec75-121">Typed Unordered Access View Loads</span></span>](typed-unordered-access-view-loads.md)<br/>               | <span data-ttu-id="5ec75-122">Неупорядоченная типизированная Загрузка представления доступа (UAV) — это способность шейдера считывать из UAV с определенным \_ форматом DXGI.</span><span class="sxs-lookup"><span data-stu-id="5ec75-122">Unordered Access View (UAV) Typed Load is the ability for a shader to read from a UAV with a specific DXGI\_FORMAT.</span></span><br/>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="5ec75-123">Архитектура единой памяти</span><span class="sxs-lookup"><span data-stu-id="5ec75-123">Unified Memory Architecture</span></span>](unified-memory-architecture.md)<br/>                           | <span data-ttu-id="5ec75-124">Запрос на то, поддерживает ли архитектура унифицированной памяти (верхнюю память), может помочь определить способ обработки некоторых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5ec75-124">Querying for whether Unified Memory Architecture (UMA) is supported can help determine how to handle some resources.</span></span><br/>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="5ec75-125">Объемные плиточные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5ec75-125">Volume Tiled Resources</span></span>](volume-tiled-resources.md)<br/>                                     | <span data-ttu-id="5ec75-126">Объемные (трехмерные) текстуры можно использовать в качестве мозаичных ресурсов, отметив, что разрешение плитки состоит из трех измерений.</span><span class="sxs-lookup"><span data-stu-id="5ec75-126">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span><br/>                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="5ec75-127">См. также</span><span class="sxs-lookup"><span data-stu-id="5ec75-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ec75-128">Новые возможности Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="5ec75-128">What's new in Direct3D 11</span></span>](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 





