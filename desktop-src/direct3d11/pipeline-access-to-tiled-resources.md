---
title: Доступ конвейера к мозаичным ресурсам
description: Ресурсы мозаичного заполнения можно использовать в представлениях ресурсов шейдера (SRV), представлениях целевого объекта отрисовки (РТВ), представления трафарета глубины (DSV) и неупорядоченных представлениях доступа (UAV), а также в некоторых точках привязки, где не используются представления, например привязки буфера вершин.
ms.assetid: D0BC0B6C-2325-4EAF-9E80-E748F58045B1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4a183fcaee90d84985a09c83826a4ad0b6d646
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793092"
---
# <a name="pipeline-access-to-tiled-resources"></a><span data-ttu-id="534a0-103">Доступ конвейера к мозаичным ресурсам</span><span class="sxs-lookup"><span data-stu-id="534a0-103">Pipeline access to tiled resources</span></span>

<span data-ttu-id="534a0-104">Ресурсы мозаичного заполнения можно использовать в представлениях ресурсов шейдера (SRV), представлениях целевого объекта отрисовки (РТВ), представления трафарета глубины (DSV) и неупорядоченных представлениях доступа (UAV), а также в некоторых точках привязки, где не используются представления, например привязки буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="534a0-104">Tiled resources can be used in shader resource views (SRV), render target views (RTV), depth stencil views (DSV) and unordered access views (UAV), as well as some bind points where views aren't used, such as vertex buffer bindings.</span></span> <span data-ttu-id="534a0-105">Список поддерживаемых привязок см. в разделе [Параметры создания мозаичных ресурсов](tiled-resource-creation-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="534a0-105">For the list of supported bindings, see [Tiled resource creation parameters](tiled-resource-creation-parameters.md).</span></span> <span data-ttu-id="534a0-106">\*Операции копирования также работают для мозаичных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="534a0-106">Copy\* operations also work on tiled resources.</span></span>

<span data-ttu-id="534a0-107">Если несколько координат плиток в одном или нескольких представлениях привязаны к одной области памяти, операции чтения и записи для различных путей в одной области памяти являются недетерминистическими и неповторяемыми.</span><span class="sxs-lookup"><span data-stu-id="534a0-107">If multiple tile coordinates in one or more views is bound to the same memory location, reads and writes from different paths to the same memory will occur in a non-deterministic and non-repeatable order of memory accesses.</span></span>

<span data-ttu-id="534a0-108">Если все плитки, связанные с доступом к памяти шейдера, сопоставляются с уникальными плитками, поведение для всех реализаций будет одинаковым, т. е. на поверхности будет одинаковое содержимое памяти без плиток.</span><span class="sxs-lookup"><span data-stu-id="534a0-108">If all tiles behind a memory access footprint from a shader are mapped to unique tiles, behavior is identical on all implementations to the surface having the same memory contents in a non-tiled fashion.</span></span>

<span data-ttu-id="534a0-109">В этом разделе содержатся дополнительные сведения о доступе конвейера к мозаичным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="534a0-109">This section provides more info about pipeline access to tiled resources.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="534a0-110">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="534a0-110">In this section</span></span>



| <span data-ttu-id="534a0-111">Раздел</span><span class="sxs-lookup"><span data-stu-id="534a0-111">Topic</span></span>                                                                                                              | <span data-ttu-id="534a0-112">Описание</span><span class="sxs-lookup"><span data-stu-id="534a0-112">Description</span></span>                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="534a0-113">Поведение SRV с несопоставленными плитками</span><span class="sxs-lookup"><span data-stu-id="534a0-113">SRV behavior with non-mapped tiles</span></span>](srv-behavior-with-non-mapped-tiles.md)<br/>                            | <span data-ttu-id="534a0-114">Поведение операций чтения представления ресурса шейдера (SRV), включающих несопоставленные плитки, зависит от уровня поддержки оборудования.</span><span class="sxs-lookup"><span data-stu-id="534a0-114">Behavior of shader resource view (SRV) reads that involve non-mapped tiles depends on the level of hardware support.</span></span> <br/>                                          |
| [<span data-ttu-id="534a0-115">Поведение UAV с несопоставленными плитками</span><span class="sxs-lookup"><span data-stu-id="534a0-115">UAV behavior with non-mapped tiles</span></span>](uav-behavior-with-non-mapped-tiles.md)<br/>                            | <span data-ttu-id="534a0-116">Поведение операций чтения и записи представлений неупорядоченного доступа (UAV) зависит от уровня поддержки оборудования.</span><span class="sxs-lookup"><span data-stu-id="534a0-116">Behavior of unordered access view (UAV) reads and writes depends on the level of hardware support.</span></span> <br/>                                                            |
| [<span data-ttu-id="534a0-117">Поведение средства программной прорисовки с несопоставленными плитками</span><span class="sxs-lookup"><span data-stu-id="534a0-117">Rasterizer behavior with non-mapped tiles</span></span>](rasterizer-behavior-with-non-mapped-tiles.md)<br/>              | <span data-ttu-id="534a0-118">В этом разделе описывается поведение растеризации несопоставленных плиток.</span><span class="sxs-lookup"><span data-stu-id="534a0-118">This section describes rasterizer behavior with non-mapped tiles.</span></span><br/>                                                                                              |
| [<span data-ttu-id="534a0-119">Ограничения доступа к плитке с повторяющимися сопоставлениями</span><span class="sxs-lookup"><span data-stu-id="534a0-119">Tile access limitations with duplicate mappings</span></span>](tile-access-limitations-with-duplicate-mappings-.md)<br/> | <span data-ttu-id="534a0-120">В этом разделе описаны ограничения на доступ к плиткам с повторяющимися сопоставлениями.</span><span class="sxs-lookup"><span data-stu-id="534a0-120">This section describes tile access limitations with duplicate mappings.</span></span><br/>                                                                                        |
| [<span data-ttu-id="534a0-121">Функции выборки текстур для мозаичных ресурсов</span><span class="sxs-lookup"><span data-stu-id="534a0-121">Tiled resources texture sampling features</span></span>](tiled-resources-texture-sampling-features.md)<br/>              | <span data-ttu-id="534a0-122">В этом разделе описываются функции выборки текстуры для мозаичных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="534a0-122">This section describes tiled resources texture sampling features.</span></span><br/>                                                                                              |
| [<span data-ttu-id="534a0-123">Уязвимость мозаичных ресурсов HLSL</span><span class="sxs-lookup"><span data-stu-id="534a0-123">HLSL tiled resources exposure</span></span>](hlsl-tiled-resources-exposure.md)<br/>                                      | <span data-ttu-id="534a0-124">Новый синтаксис языка шейдера высокого уровня (Майкрософт) (HLSL) необходим для поддержки мозаичных ресурсов в [модели шейдеров 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5).</span><span class="sxs-lookup"><span data-stu-id="534a0-124">New Microsoft High Level Shader Language (HLSL) syntax is required to support tiled resources in [Shader Model 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5).</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="534a0-125">См. также</span><span class="sxs-lookup"><span data-stu-id="534a0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="534a0-126">Мозаичные ресурсы</span><span class="sxs-lookup"><span data-stu-id="534a0-126">Tiled resources</span></span>](tiled-resources.md)
</dt> </dl>

 

