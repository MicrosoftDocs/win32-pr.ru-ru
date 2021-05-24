---
title: Ресурсы для мозаичного заполнения тома (графика Direct3D 11)
description: Сведения о том, как можно использовать 3D-текстуры в качестве мозаичных ресурсов. Обратите внимание, что разрешение плитки состоит из трех измерений.
ms.assetid: B6BF22A2-EDA3-4765-B545-BF825043D4C4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bf9b3ed8b1db89d9718fa904eefd23ce2e871db
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335438"
---
# <a name="volume-tiled-resources"></a><span data-ttu-id="67b41-104">Объемные плиточные ресурсы</span><span class="sxs-lookup"><span data-stu-id="67b41-104">Volume Tiled Resources</span></span>

<span data-ttu-id="67b41-105">Объемные (трехмерные) текстуры можно использовать в качестве мозаичных ресурсов, отметив, что разрешение плитки состоит из трех измерений.</span><span class="sxs-lookup"><span data-stu-id="67b41-105">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span>

-   [<span data-ttu-id="67b41-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="67b41-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="67b41-107">API-интерфейсы мозаичного ресурса D3D 11.3</span><span class="sxs-lookup"><span data-stu-id="67b41-107">D3D11.3 Tiled Resource APIs</span></span>](#d3d113-tiled-resource-apis)
-   [<span data-ttu-id="67b41-108">См. также</span><span class="sxs-lookup"><span data-stu-id="67b41-108">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="67b41-109">Обзор</span><span class="sxs-lookup"><span data-stu-id="67b41-109">Overview</span></span>

<span data-ttu-id="67b41-110">Мозаичные ресурсы, связанные с объектом-ресурсами D3D из резервной памяти (ресурсы в прошлом имели отношение 1:1 с резервной памятью).</span><span class="sxs-lookup"><span data-stu-id="67b41-110">Tiled resources decouple a D3D Resource object from its backing memory (resources in the past had a 1:1 relationship with their backing memory).</span></span> <span data-ttu-id="67b41-111">Это позволяет использовать различные интересные сценарии, такие как потоковая передача данных текстуры и повторное использование и уменьшение использования памяти.</span><span class="sxs-lookup"><span data-stu-id="67b41-111">This allows for a variety of interesting scenarios such as streaming in texture data and reusing or reducing memory usage</span></span>

<span data-ttu-id="67b41-112">ресурсы мозаичного заполнения двухмерной текстуры поддерживаются в D3D 11.2.</span><span class="sxs-lookup"><span data-stu-id="67b41-112">2D texture tiled resources are supported in D3D11.2.</span></span> <span data-ttu-id="67b41-113">D3D12 и D3D 11.3 добавляют поддержку трехмерных мозаичных текстур.</span><span class="sxs-lookup"><span data-stu-id="67b41-113">D3D12 and D3D11.3 add support for 3D tiled textures.</span></span>

<span data-ttu-id="67b41-114">К типичным измерениям ресурсов, используемым при мозаичном заполнении, относятся 4 x 4 плитки для двумерных текстур и 4 x 4 x 4 плитки для трехмерных текстур.</span><span class="sxs-lookup"><span data-stu-id="67b41-114">The typical resource dimensions used in tiling are 4 x 4 tiles for 2D textures, and 4 x 4 x 4 tiles for 3D textures.</span></span>



| <span data-ttu-id="67b41-115">Бит/пиксель (1 образец или пиксель)</span><span class="sxs-lookup"><span data-stu-id="67b41-115">Bits/pixel (1 sample/pixel)</span></span>                            | <span data-ttu-id="67b41-116">Размеры мозаики (в пикселях, w x x d)</span><span class="sxs-lookup"><span data-stu-id="67b41-116">Tile dimensions (pixels, w x h x d)</span></span>                                    |
|-----------------------------|-------------------------------------|
| <span data-ttu-id="67b41-117">8</span><span class="sxs-lookup"><span data-stu-id="67b41-117">8</span></span>                           | <span data-ttu-id="67b41-118">64x32x32</span><span class="sxs-lookup"><span data-stu-id="67b41-118">64x32x32</span></span>                            |
| <span data-ttu-id="67b41-119">16</span><span class="sxs-lookup"><span data-stu-id="67b41-119">16</span></span>                          | <span data-ttu-id="67b41-120">32x32x32</span><span class="sxs-lookup"><span data-stu-id="67b41-120">32x32x32</span></span>                            |
| <span data-ttu-id="67b41-121">32</span><span class="sxs-lookup"><span data-stu-id="67b41-121">32</span></span>                          | <span data-ttu-id="67b41-122">32x32x16</span><span class="sxs-lookup"><span data-stu-id="67b41-122">32x32x16</span></span>                            |
| <span data-ttu-id="67b41-123">64</span><span class="sxs-lookup"><span data-stu-id="67b41-123">64</span></span>                          | <span data-ttu-id="67b41-124">32x16x16</span><span class="sxs-lookup"><span data-stu-id="67b41-124">32x16x16</span></span>                            |
| <span data-ttu-id="67b41-125">128</span><span class="sxs-lookup"><span data-stu-id="67b41-125">128</span></span>                         | <span data-ttu-id="67b41-126">16x16x16</span><span class="sxs-lookup"><span data-stu-id="67b41-126">16x16x16</span></span>                            |
| <span data-ttu-id="67b41-127">BC 1, 4</span><span class="sxs-lookup"><span data-stu-id="67b41-127">BC 1,4</span></span>                      | <span data-ttu-id="67b41-128">128x64x16</span><span class="sxs-lookup"><span data-stu-id="67b41-128">128x64x16</span></span>                           |
| <span data-ttu-id="67b41-129">BC 2, 3, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="67b41-129">BC 2,3,5,6,7</span></span>                | <span data-ttu-id="67b41-130">64x64x16</span><span class="sxs-lookup"><span data-stu-id="67b41-130">64x64x16</span></span>                            |



 

<span data-ttu-id="67b41-131">Обратите внимание, что следующие форматы не поддерживаются для мозаичных ресурсов: форматы 96bpp, форматы видео, R1 \_ UNORM, R8G8 \_ B8G8 \_ UNORM, R8R8 \_ G8B8 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="67b41-131">Note the following formats are not supported with tiled resources: 96bpp formats, video formats, R1\_UNORM, R8G8\_B8G8\_UNORM, R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="67b41-132">На диаграммах ниже темно-серый цвет представляет НУЛЕВые плитки.</span><span class="sxs-lookup"><span data-stu-id="67b41-132">In the diagrams below dark gray represents NULL tiles.</span></span>

-   [<span data-ttu-id="67b41-133">Сопоставление текстуры трехмерного мозаичного ресурса по умолчанию (наиболее подробное MIP)</span><span class="sxs-lookup"><span data-stu-id="67b41-133">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [<span data-ttu-id="67b41-134">Сопоставление текстуры трехмерного мозаичного ресурса по умолчанию (второй самый подробный MIP)</span><span class="sxs-lookup"><span data-stu-id="67b41-134">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [<span data-ttu-id="67b41-135">Трехмерный мозаичный ресурс текстуры (наиболее подробный MIP)</span><span class="sxs-lookup"><span data-stu-id="67b41-135">Texture 3D Tiled Resource (most detailed mip)</span></span>](#texture-3d-tiled-resource-most-detailed-mip)
-   [<span data-ttu-id="67b41-136">Трехмерный мозаичный ресурс текстуры (второй самый подробный MIP)</span><span class="sxs-lookup"><span data-stu-id="67b41-136">Texture 3D Tiled Resource (second most detailed mip)</span></span>](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [<span data-ttu-id="67b41-137">Трехмерный мозаичный ресурс текстуры (один элемент мозаики)</span><span class="sxs-lookup"><span data-stu-id="67b41-137">Texture 3D Tiled Resource (Single Tile)</span></span>](#texture-3d-tiled-resource-single-tile)
-   [<span data-ttu-id="67b41-138">Трехмерный мозаичный ресурс текстуры (унифицированное поле)</span><span class="sxs-lookup"><span data-stu-id="67b41-138">Texture 3D Tiled Resource (Uniform Box)</span></span>](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a><span data-ttu-id="67b41-139">Сопоставление текстуры трехмерного мозаичного ресурса по умолчанию (наиболее подробное MIP)</span><span class="sxs-lookup"><span data-stu-id="67b41-139">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>

![сопоставление по умолчанию для наиболее подробных MIP](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a><span data-ttu-id="67b41-141">Сопоставление текстуры трехмерного мозаичного ресурса по умолчанию (второй самый подробный MIP)</span><span class="sxs-lookup"><span data-stu-id="67b41-141">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>

![сопоставление по умолчанию для второго наиболее подробного MIP](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a><span data-ttu-id="67b41-143">Трехмерный мозаичный ресурс текстуры (наиболее подробный MIP)</span><span class="sxs-lookup"><span data-stu-id="67b41-143">Texture 3D Tiled Resource (most detailed mip)</span></span>

<span data-ttu-id="67b41-144">Следующий код настраивает трехмерный ресурс мозаичного заполнения в наиболее подробной MIP.</span><span class="sxs-lookup"><span data-stu-id="67b41-144">The following code sets up a 3D tiled resource at the most detailed mip.</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![наиболее подробное сопоставление трехмерного мозаичного ресурса](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a><span data-ttu-id="67b41-146">Трехмерный мозаичный ресурс текстуры (второй самый подробный MIP)</span><span class="sxs-lookup"><span data-stu-id="67b41-146">Texture 3D Tiled Resource (second most detailed mip)</span></span>

<span data-ttu-id="67b41-147">Следующий код настраивает ресурс трехмерной мозаики, а второй самый подробный MIP:</span><span class="sxs-lookup"><span data-stu-id="67b41-147">The following code sets up a 3D tiled resource, and the second most detailed mip:</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![второе наиболее подробное сопоставление трехмерного мозаичного ресурса](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a><span data-ttu-id="67b41-149">Трехмерный мозаичный ресурс текстуры (один элемент мозаики)</span><span class="sxs-lookup"><span data-stu-id="67b41-149">Texture 3D Tiled Resource (Single Tile)</span></span>

<span data-ttu-id="67b41-150">Следующий код настраивает один ресурс плитки:</span><span class="sxs-lookup"><span data-stu-id="67b41-150">The following code sets up a Single Tile resource:</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 1;
trCoord.Z = 1;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![одна плитка](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a><span data-ttu-id="67b41-152">Трехмерный мозаичный ресурс текстуры (унифицированное поле)</span><span class="sxs-lookup"><span data-stu-id="67b41-152">Texture 3D Tiled Resource (Uniform Box)</span></span>

<span data-ttu-id="67b41-153">Следующий код устанавливает унифицированный мозаичный ресурс Box (Обратите внимание на инструкцию `trSize.bUseBox = true;) :`</span><span class="sxs-lookup"><span data-stu-id="67b41-153">The following code sets up a Uniform Box tiled resource (note the statement `trSize.bUseBox = true;) :`</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 0;
trCoord.Y = 1;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![Унифицированное поле](images/vtr-tex3d-uniform.png)

## <a name="d3d113-tiled-resource-apis"></a><span data-ttu-id="67b41-155">API-интерфейсы мозаичного ресурса D3D 11.3</span><span class="sxs-lookup"><span data-stu-id="67b41-155">D3D11.3 Tiled Resource APIs</span></span>

<span data-ttu-id="67b41-156">Для двумерных и трехмерных мозаичных ресурсов используются те же вызовы API:</span><span class="sxs-lookup"><span data-stu-id="67b41-156">The same API calls are used for both 2D and 3D tiled resources:</span></span>

<span data-ttu-id="67b41-157">Перечисления</span><span class="sxs-lookup"><span data-stu-id="67b41-157">Enums</span></span>

-   <span data-ttu-id="67b41-158">[**D3D11 \_ Уровень МОЗАИЧных \_ ресурсов \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : определяет уровень поддержки мозаичных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67b41-158">[**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : determines the level of tiled resource support.</span></span>
-   <span data-ttu-id="67b41-159">[**D3D11 \_ FORMAT \_ SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : используется для проверки поддержки мозаичных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67b41-159">[**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : used to test for tiled resource support.</span></span>
-   <span data-ttu-id="67b41-160">[**D3D11 \_ Флажок "проверить \_ МНОГОвыборочные \_ \_ уровни \_ качества**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) ": определяет поддержку мозаичных ресурсов в многовыборочном ресурсе.</span><span class="sxs-lookup"><span data-stu-id="67b41-160">[**D3D11\_CHECK\_MULTISAMPLE\_QUALITY\_LEVELS\_FLAG**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) : determines tiled resource support in a multi-sampling resource.</span></span>
-   <span data-ttu-id="67b41-161">[**D3D11 \_ \_ \_ Флаги копирования плитки**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : содержит флаги для копирования в и из свиззлед мозаичных ресурсов и линейных буферов.</span><span class="sxs-lookup"><span data-stu-id="67b41-161">[**D3D11\_TILE\_COPY\_FLAGS**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : holds flags for copying to and from swizzled tiled resources and linear buffers.</span></span>

<span data-ttu-id="67b41-162">Структуры</span><span class="sxs-lookup"><span data-stu-id="67b41-162">Structures</span></span>

-   <span data-ttu-id="67b41-163">[**D3D11 \_ \_ \_ КООРДИНАТа мозаичного ресурса**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : содержит координаты x, y и z, а также ссылки на подресурсы.</span><span class="sxs-lookup"><span data-stu-id="67b41-163">[**D3D11\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : holds the x, y, and z co-ordinate, and subresource reference.</span></span> <span data-ttu-id="67b41-164">Обратите внимание, что существует вспомогательный класс: CD3D11 \_ мозаичная \_ \_ координата ресурса.</span><span class="sxs-lookup"><span data-stu-id="67b41-164">Note there is a helper class: CD3D11\_TILED\_RESOURCE\_COORDINATE.</span></span>
-   <span data-ttu-id="67b41-165">[**D3D11 \_ \_ \_ Размер области плитки**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : определяет размер и число плиток мозаичного региона.</span><span class="sxs-lookup"><span data-stu-id="67b41-165">[**D3D11\_TILE\_REGION\_SIZE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : specifies the size, and number of tiles, of the tiled region.</span></span>
-   <span data-ttu-id="67b41-166">[**D3D11 \_ МОЗАИЧная \_ фигура**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : Мозаичная фигура в виде ширины, высоты и глубины в пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="67b41-166">[**D3D11\_TILE\_SHAPE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : the tile shape as a width, height and depth in texels.</span></span>
-   <span data-ttu-id="67b41-167">[**D3D11 \_ FEATURE \_ Data \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): содержит поддерживаемый уровень уровня ресурсов плитки.</span><span class="sxs-lookup"><span data-stu-id="67b41-167">[**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): holds the supported tile resource tier level.</span></span>

<span data-ttu-id="67b41-168">Методы</span><span class="sxs-lookup"><span data-stu-id="67b41-168">Methods</span></span>

-   <span data-ttu-id="67b41-169">[**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : используется для определения того, какие функции и на каком уровне поддерживаются текущим оборудованием.</span><span class="sxs-lookup"><span data-stu-id="67b41-169">[**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : used to determine what features, and at what tier, are supported by the current hardware.</span></span>
-   <span data-ttu-id="67b41-170">[**ID3D11DeviceContext2:: копитилес**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : копирует плитки из буфера в мозаичный ресурс или наоборот.</span><span class="sxs-lookup"><span data-stu-id="67b41-170">[**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copies tiles from buffer to tiled resource or vice versa.</span></span>
-   <span data-ttu-id="67b41-171">[**ID3D11DeviceContext2:: упдатетилемаппингс**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : обновляет сопоставления расположений плиток в мозаичных ресурсах с расположением в памяти в пуле плиток.</span><span class="sxs-lookup"><span data-stu-id="67b41-171">[**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : updates mappings of tile locations in tiled resources to memory locations in a tile pool.</span></span>
-   <span data-ttu-id="67b41-172">[**ID3D11DeviceContext2:: копитилемаппингс**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : копирует сопоставления из исходного мозаичного ресурса в целевой мозаичный ресурс.</span><span class="sxs-lookup"><span data-stu-id="67b41-172">[**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copies mappings from a source tiled resource to a destination tiled resource.</span></span>
-   <span data-ttu-id="67b41-173">[**ID3D11DeviceContext2:: жетресаурцетилинг**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : получает сведения о том, как мозаичный ресурс разбивается на плитки.</span><span class="sxs-lookup"><span data-stu-id="67b41-173">[**ID3D11DeviceContext2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67b41-174">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="67b41-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67b41-175">Функции Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="67b41-175">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> </dl>

 

 




