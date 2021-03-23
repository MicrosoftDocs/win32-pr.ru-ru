---
title: Ресурсы для мозаичного заполнения тома (Direct3D 12)
description: Объемные (трехмерные) текстуры можно использовать в качестве мозаичных ресурсов, отметив, что разрешение плитки состоит из трех измерений.
ms.assetid: F670D15D-BC0F-4F90-99C1-A35192FE8980
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42679155bbd8dc2cec560d2724e430c860f54bc0
ms.sourcegitcommit: 05e7efd3d8de6926d08802669f37e825a2fa2f46
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/12/2020
ms.locfileid: "104548936"
---
# <a name="volume-tiled-resources-direct3d-12"></a><span data-ttu-id="4920c-103">Ресурсы для мозаичного заполнения тома (Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="4920c-103">Volume tiled resources (Direct3D 12)</span></span>

<span data-ttu-id="4920c-104">Объемные (трехмерные) текстуры можно использовать в качестве мозаичных ресурсов, отметив, что разрешение плитки состоит из трех измерений.</span><span class="sxs-lookup"><span data-stu-id="4920c-104">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span>

-   [<span data-ttu-id="4920c-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="4920c-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="4920c-106">API-интерфейсы мозаичного ресурса</span><span class="sxs-lookup"><span data-stu-id="4920c-106">Tiled Resource APIs</span></span>](#tiled-resource-apis)
-   [<span data-ttu-id="4920c-107">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="4920c-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="4920c-108">Обзор</span><span class="sxs-lookup"><span data-stu-id="4920c-108">Overview</span></span>

<span data-ttu-id="4920c-109">Мозаичные ресурсы, связанные с объектом-ресурсами D3D из резервной памяти (ресурсы в прошлом имели отношение 1:1 с резервной памятью).</span><span class="sxs-lookup"><span data-stu-id="4920c-109">Tiled resources decouple a D3D Resource object from its backing memory (resources in the past had a 1:1 relationship with their backing memory).</span></span> <span data-ttu-id="4920c-110">Это позволяет использовать различные интересные сценарии, такие как потоковая передача данных текстуры и повторное использование или уменьшение использования памяти.</span><span class="sxs-lookup"><span data-stu-id="4920c-110">This allows for a variety of interesting scenarios such as streaming in texture data and reusing or reducing memory usage.</span></span>

<span data-ttu-id="4920c-111">ресурсы мозаичного заполнения двухмерной текстуры поддерживаются в D3D 11.2.</span><span class="sxs-lookup"><span data-stu-id="4920c-111">2D texture tiled resources are supported in D3D11.2.</span></span> <span data-ttu-id="4920c-112">Необязательная поддержка трехмерных мозаичных текстур доступна для D3D12 и D3D 11.3 (см. [**\_ \_ \_ уровень мозаичных ресурсов D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).</span><span class="sxs-lookup"><span data-stu-id="4920c-112">Optional support for 3D tiled textures is available for D3D12 and D3D11.3 (refer to [**D3D12\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).</span></span>

<span data-ttu-id="4920c-113">К типичным измерениям ресурсов, используемым при мозаичном заполнении, относятся 4 x 4 плитки для двумерных текстур и 4 x 4 x 4 плитки для трехмерных текстур.</span><span class="sxs-lookup"><span data-stu-id="4920c-113">The typical resource dimensions used in tiling are 4 x 4 tiles for 2D textures, and 4 x 4 x 4 tiles for 3D textures.</span></span>



| <span data-ttu-id="4920c-114">Бит/пиксель (1 образец или пиксель)</span><span class="sxs-lookup"><span data-stu-id="4920c-114">Bits/pixel (1 sample/pixel)</span></span> | <span data-ttu-id="4920c-115">Размеры мозаики (в пикселях, w x x d)</span><span class="sxs-lookup"><span data-stu-id="4920c-115">Tile dimensions (pixels, w x h x d)</span></span> |
|-----------------------------|-------------------------------------|
| <span data-ttu-id="4920c-116">8</span><span class="sxs-lookup"><span data-stu-id="4920c-116">8</span></span>                           | <span data-ttu-id="4920c-117">64x32x32</span><span class="sxs-lookup"><span data-stu-id="4920c-117">64x32x32</span></span>                            |
| <span data-ttu-id="4920c-118">16</span><span class="sxs-lookup"><span data-stu-id="4920c-118">16</span></span>                          | <span data-ttu-id="4920c-119">32x32x32</span><span class="sxs-lookup"><span data-stu-id="4920c-119">32x32x32</span></span>                            |
| <span data-ttu-id="4920c-120">32</span><span class="sxs-lookup"><span data-stu-id="4920c-120">32</span></span>                          | <span data-ttu-id="4920c-121">32x32x16</span><span class="sxs-lookup"><span data-stu-id="4920c-121">32x32x16</span></span>                            |
| <span data-ttu-id="4920c-122">64</span><span class="sxs-lookup"><span data-stu-id="4920c-122">64</span></span>                          | <span data-ttu-id="4920c-123">32x16x16</span><span class="sxs-lookup"><span data-stu-id="4920c-123">32x16x16</span></span>                            |
| <span data-ttu-id="4920c-124">128</span><span class="sxs-lookup"><span data-stu-id="4920c-124">128</span></span>                         | <span data-ttu-id="4920c-125">16x16x16</span><span class="sxs-lookup"><span data-stu-id="4920c-125">16x16x16</span></span>                            |
| <span data-ttu-id="4920c-126">BC 1, 4</span><span class="sxs-lookup"><span data-stu-id="4920c-126">BC 1,4</span></span>                      | <span data-ttu-id="4920c-127">128x64x16</span><span class="sxs-lookup"><span data-stu-id="4920c-127">128x64x16</span></span>                           |
| <span data-ttu-id="4920c-128">BC 2, 3, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="4920c-128">BC 2,3,5,6,7</span></span>                | <span data-ttu-id="4920c-129">64x64x16</span><span class="sxs-lookup"><span data-stu-id="4920c-129">64x64x16</span></span>                            |

<span data-ttu-id="4920c-130">Обратите внимание, что следующие форматы не поддерживаются для мозаичных ресурсов: форматы 96bpp, форматы видео, R1 \_ UNORM, R8G8 \_ B8G8 \_ UNORM, R8R8 \_ G8B8 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="4920c-130">Note the following formats are not supported with tiled resources: 96bpp formats, video formats, R1\_UNORM, R8G8\_B8G8\_UNORM, R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="4920c-131">На диаграммах ниже темно-серый цвет представляет НУЛЕВые плитки.</span><span class="sxs-lookup"><span data-stu-id="4920c-131">In the diagrams below dark gray represents NULL tiles.</span></span>

-   [<span data-ttu-id="4920c-132">Сопоставление текстуры трехмерного мозаичного ресурса по умолчанию (наиболее подробное MIP)</span><span class="sxs-lookup"><span data-stu-id="4920c-132">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [<span data-ttu-id="4920c-133">Сопоставление текстуры трехмерного мозаичного ресурса по умолчанию (второй самый подробный MIP)</span><span class="sxs-lookup"><span data-stu-id="4920c-133">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [<span data-ttu-id="4920c-134">Трехмерный мозаичный ресурс текстуры (наиболее подробный MIP)</span><span class="sxs-lookup"><span data-stu-id="4920c-134">Texture 3D Tiled Resource (most detailed mip)</span></span>](#texture-3d-tiled-resource-most-detailed-mip)
-   [<span data-ttu-id="4920c-135">Трехмерный мозаичный ресурс текстуры (второй самый подробный MIP)</span><span class="sxs-lookup"><span data-stu-id="4920c-135">Texture 3D Tiled Resource (second most detailed mip)</span></span>](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [<span data-ttu-id="4920c-136">Трехмерный мозаичный ресурс текстуры (один элемент мозаики)</span><span class="sxs-lookup"><span data-stu-id="4920c-136">Texture 3D Tiled Resource (Single Tile)</span></span>](#texture-3d-tiled-resource-single-tile)
-   [<span data-ttu-id="4920c-137">Трехмерный мозаичный ресурс текстуры (унифицированное поле)</span><span class="sxs-lookup"><span data-stu-id="4920c-137">Texture 3D Tiled Resource (Uniform Box)</span></span>](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a><span data-ttu-id="4920c-138">Сопоставление текстуры трехмерного мозаичного ресурса по умолчанию (наиболее подробное MIP)</span><span class="sxs-lookup"><span data-stu-id="4920c-138">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>

![сопоставление по умолчанию для мозаичного трехмерного ресурса](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a><span data-ttu-id="4920c-140">Сопоставление текстуры трехмерного мозаичного ресурса по умолчанию (второй самый подробный MIP)</span><span class="sxs-lookup"><span data-stu-id="4920c-140">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>

![показывает второй наиболее подробный MIP](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a><span data-ttu-id="4920c-142">Трехмерный мозаичный ресурс текстуры (наиболее подробный MIP)</span><span class="sxs-lookup"><span data-stu-id="4920c-142">Texture 3D Tiled Resource (most detailed mip)</span></span>

<span data-ttu-id="4920c-143">Следующий код настраивает трехмерный ресурс мозаичного заполнения в наиболее подробной MIP.</span><span class="sxs-lookup"><span data-stu-id="4920c-143">The following code sets up a 3D tiled resource at the most detailed mip.</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![наиболее подробный MIP для трехмерной текстуры](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a><span data-ttu-id="4920c-145">Трехмерный мозаичный ресурс текстуры (второй самый подробный MIP)</span><span class="sxs-lookup"><span data-stu-id="4920c-145">Texture 3D Tiled Resource (second most detailed mip)</span></span>

<span data-ttu-id="4920c-146">Следующий код настраивает ресурс трехмерной мозаики, а второй самый подробный MIP:</span><span class="sxs-lookup"><span data-stu-id="4920c-146">The following code sets up a 3D tiled resource, and the second most detailed mip:</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![второй наиболее подробный MIP для трехмерной текстуры](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a><span data-ttu-id="4920c-148">Трехмерный мозаичный ресурс текстуры (один элемент мозаики)</span><span class="sxs-lookup"><span data-stu-id="4920c-148">Texture 3D Tiled Resource (Single Tile)</span></span>

<span data-ttu-id="4920c-149">Следующий код настраивает один ресурс плитки:</span><span class="sxs-lookup"><span data-stu-id="4920c-149">The following code sets up a Single Tile resource:</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 1;
trCoord.Z = 1;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![один мозаичный трехмерный ресурс](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a><span data-ttu-id="4920c-151">Трехмерный мозаичный ресурс текстуры (унифицированное поле)</span><span class="sxs-lookup"><span data-stu-id="4920c-151">Texture 3D Tiled Resource (Uniform Box)</span></span>

<span data-ttu-id="4920c-152">Следующий код устанавливает унифицированный мозаичный ресурс Box (Обратите внимание на инструкцию `trSize.bUseBox = true;) :`</span><span class="sxs-lookup"><span data-stu-id="4920c-152">The following code sets up a Uniform Box tiled resource (note the statement `trSize.bUseBox = true;) :`</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 0;
trCoord.Y = 1;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![Унифицированное поле](images/vtr-tex3d-uniform.png)

## <a name="tiled-resource-apis"></a><span data-ttu-id="4920c-154">API-интерфейсы мозаичного ресурса</span><span class="sxs-lookup"><span data-stu-id="4920c-154">Tiled Resource APIs</span></span>

<span data-ttu-id="4920c-155">Для двумерных и трехмерных мозаичных ресурсов используются те же вызовы API:</span><span class="sxs-lookup"><span data-stu-id="4920c-155">The same API calls are used for both 2D and 3D tiled resources:</span></span>

<span data-ttu-id="4920c-156">Перечисления</span><span class="sxs-lookup"><span data-stu-id="4920c-156">Enums</span></span>

-   <span data-ttu-id="4920c-157">[**D3D12 \_ Уровень МОЗАИЧных \_ ресурсов \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : определяет уровень поддержки мозаичных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4920c-157">[**D3D12\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : determines the level of tiled resource support.</span></span>
-   <span data-ttu-id="4920c-158">[**D3D12 \_ FORMAT \_ SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) : используется для проверки поддержки мозаичных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4920c-158">[**D3D12\_FORMAT\_SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) : used to test for tiled resource support.</span></span>
-   <span data-ttu-id="4920c-159">[**D3D12 \_ \_ \_ \_ Флаги уровня качества**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) для нескольких образцов: определяет поддержку мозаичных ресурсов в многовыборочном ресурсе.</span><span class="sxs-lookup"><span data-stu-id="4920c-159">[**D3D12\_MULTISAMPLE\_QUALITY\_LEVEL\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) : determines tiled resource support in a multi-sampling resource.</span></span>
-   <span data-ttu-id="4920c-160">[**D3D12 \_ \_ \_ Флаги копирования плитки**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : содержит флаги для копирования в и из свиззлед мозаичных ресурсов и линейных буферов.</span><span class="sxs-lookup"><span data-stu-id="4920c-160">[**D3D12\_TILE\_COPY\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : holds flags for copying to and from swizzled tiled resources and linear buffers.</span></span>

<span data-ttu-id="4920c-161">Структуры</span><span class="sxs-lookup"><span data-stu-id="4920c-161">Structs</span></span>

-   <span data-ttu-id="4920c-162">[**D3D12 \_ \_ \_ КООРДИНАТа мозаичного ресурса**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : содержит координаты x, y и z, а также ссылки на подресурсы.</span><span class="sxs-lookup"><span data-stu-id="4920c-162">[**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : holds the x, y, and z co-ordinate, and subresource reference.</span></span> <span data-ttu-id="4920c-163">Обратите внимание, что существует вспомогательная структура: [**CD3DX12 \_ Мозаичное \_ \_ координата ресурса**](cd3dx12-tiled-resource-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="4920c-163">Note there is a helper structure: [**CD3DX12\_TILED\_RESOURCE\_COORDINATE**](cd3dx12-tiled-resource-coordinate.md).</span></span>
-   <span data-ttu-id="4920c-164">[**D3D12 \_ \_ \_ Размер области плитки**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) : определяет размер и число плиток мозаичного региона.</span><span class="sxs-lookup"><span data-stu-id="4920c-164">[**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) : specifies the size, and number of tiles, of the tiled region.</span></span>
-   <span data-ttu-id="4920c-165">[**D3D12 \_ МОЗАИЧная \_ фигура**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) : Мозаичная фигура в виде ширины, высоты и глубины в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="4920c-165">[**D3D12\_TILE\_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) : the tile shape as a width, height and depth in texels.</span></span>
-   <span data-ttu-id="4920c-166">[**D3D12 \_ \_ \_ \_ Параметры D3D12 данных функции**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : содержит поддерживаемый уровень уровня ресурсов плитки и логическое значение, *волуметиледресаурцессуппортед*, указывающее, поддерживаются ли ресурсы мозаичного распределения томов.</span><span class="sxs-lookup"><span data-stu-id="4920c-166">[**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : holds the supported tile resource tier level and a boolean, *VolumeTiledResourcesSupported*, indicated whether volume tiled resources are supported.</span></span>

<span data-ttu-id="4920c-167">Методы</span><span class="sxs-lookup"><span data-stu-id="4920c-167">Methods</span></span>

-   <span data-ttu-id="4920c-168">[**ID3D12Device:: чеккфеатуресуппорт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : используется для определения того, какие функции и на каком уровне поддерживаются текущим оборудованием.</span><span class="sxs-lookup"><span data-stu-id="4920c-168">[**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : used to determine what features, and at what tier, are supported by the current hardware.</span></span>
-   <span data-ttu-id="4920c-169">[**ID3D12GraphcisCommandList:: копитилес**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) : копирует плитки из буфера в мозаичный ресурс или наоборот.</span><span class="sxs-lookup"><span data-stu-id="4920c-169">[**ID3D12GraphcisCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) : copies tiles from buffer to tiled resource or vice versa.</span></span>
-   <span data-ttu-id="4920c-170">[**ID3D12CommandQueue:: упдатетилемаппингс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : обновляет сопоставления расположений плиток в мозаичных ресурсах с расположениями в памяти в куче ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4920c-170">[**ID3D12CommandQueue::UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : updates mappings of tile locations in tiled resources to memory locations in a resource heap.</span></span>
-   <span data-ttu-id="4920c-171">[**ID3D12CommandQueue:: копитилемаппингс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) : копирует сопоставления из исходного мозаичного ресурса в целевой мозаичный ресурс.</span><span class="sxs-lookup"><span data-stu-id="4920c-171">[**ID3D12CommandQueue::CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) : copies mappings from a source tiled resource to a destination tiled resource.</span></span>
-   <span data-ttu-id="4920c-172">[**ID3D12Device:: жетресаурцетилинг**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : получает сведения о том, как мозаичный ресурс разбивается на плитки.</span><span class="sxs-lookup"><span data-stu-id="4920c-172">[**ID3D12Device::GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4920c-173">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="4920c-173">Related topics</span></span>
* [<span data-ttu-id="4920c-174">Привязка ресурсов</span><span class="sxs-lookup"><span data-stu-id="4920c-174">Resource Binding</span></span>](resource-binding.md)
