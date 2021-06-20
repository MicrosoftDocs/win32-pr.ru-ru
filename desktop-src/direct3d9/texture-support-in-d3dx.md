---
description: Сведения о поддержке текстур в D3DX. D3DX — это служебная Библиотека, которая предоставляет вспомогательные службы. Это уровень выше компонента Direct3D.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Поддержка текстур в D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f31a597ddcab317477d31e0d833c9da96f71ed4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404607"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a><span data-ttu-id="08018-105">Поддержка текстур в D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="08018-105">Texture Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="08018-106">D3DX — это служебная Библиотека, которая предоставляет вспомогательные службы.</span><span class="sxs-lookup"><span data-stu-id="08018-106">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="08018-107">Это уровень выше компонента Direct3D.</span><span class="sxs-lookup"><span data-stu-id="08018-107">It is a layer above the Direct3D component.</span></span>

## <a name="textures"></a><span data-ttu-id="08018-108">Текстуры</span><span class="sxs-lookup"><span data-stu-id="08018-108">Textures</span></span>

<span data-ttu-id="08018-109">В следующих разделах поддерживаются различные текстуры.</span><span class="sxs-lookup"><span data-stu-id="08018-109">Many different textures are supported in the following topics.</span></span>

-   <span data-ttu-id="08018-110">Стандартная поддержка текстур мипмаппед.</span><span class="sxs-lookup"><span data-stu-id="08018-110">Standard mipmapped texture support.</span></span> <span data-ttu-id="08018-111">См. раздел [Автоматическое создание MIP-карты (Direct3D 9)](automatic-generation-of-mipmaps.md).</span><span class="sxs-lookup"><span data-stu-id="08018-111">See [Automatic Generation of Mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).</span></span>
-   <span data-ttu-id="08018-112">Поддержка схемы куба.</span><span class="sxs-lookup"><span data-stu-id="08018-112">Cube map support.</span></span> <span data-ttu-id="08018-113">См. раздел [сопоставление кубических сред (Direct3D 9)](cubic-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="08018-113">See [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>
-   <span data-ttu-id="08018-114">Поддержка текстуры тома.</span><span class="sxs-lookup"><span data-stu-id="08018-114">Volume texture support.</span></span> <span data-ttu-id="08018-115">См. раздел [ресурсы текстуры для томов (Direct3D 9)](volume-texture-resources.md).</span><span class="sxs-lookup"><span data-stu-id="08018-115">See [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>
-   <span data-ttu-id="08018-116">Поддержка сопоставления среды.</span><span class="sxs-lookup"><span data-stu-id="08018-116">Environment mapping support.</span></span> <span data-ttu-id="08018-117">См. раздел [сопоставление среды (Direct3D 9)](environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="08018-117">See [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>
-   <span data-ttu-id="08018-118">Поддержка сопоставления рельефов.</span><span class="sxs-lookup"><span data-stu-id="08018-118">Bump mapping support.</span></span> <span data-ttu-id="08018-119">См. раздел [«назначение выпуклости» (Direct3D 9)](bump-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="08018-119">See [Bump Mapping (Direct3D 9)](bump-mapping.md).</span></span>

### <a name="texture-color-conversion"></a><span data-ttu-id="08018-120">Преобразование цвета текстуры</span><span class="sxs-lookup"><span data-stu-id="08018-120">Texture Color Conversion</span></span>

<span data-ttu-id="08018-121">При использовании любых функций D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx или D3DXCreateVolumeTexturexxx может потребоваться преобразование цветов.</span><span class="sxs-lookup"><span data-stu-id="08018-121">When using any of the D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx, or D3DXCreateVolumeTexturexxx functions, color conversion might need to be performed.</span></span> <span data-ttu-id="08018-122">Например, одна поверхность может иметь тип RGBA, а другая может быть УВВК.</span><span class="sxs-lookup"><span data-stu-id="08018-122">For example, one surface might be type RGBA and the other might be UVWQ.</span></span> <span data-ttu-id="08018-123">В случае с непохожими форматами используется следующая последовательность преобразования:</span><span class="sxs-lookup"><span data-stu-id="08018-123">For cases of dissimilar formats, the conversion sequence is as follows:</span></span>

### <a name="mapping-rgba-to-uvwq"></a><span data-ttu-id="08018-124">Сопоставление RGBA и УВВК</span><span class="sxs-lookup"><span data-stu-id="08018-124">Mapping RGBA to UVWQ</span></span>

-   <span data-ttu-id="08018-125">R <-> U, канал R сопоставляется с каналом U или наоборот.</span><span class="sxs-lookup"><span data-stu-id="08018-125">R <-> U, R channel is mapped to the U channel, or vice versa.</span></span>
-   <span data-ttu-id="08018-126">G <-> V, G Channel сопоставляется с каналом V или наоборот.</span><span class="sxs-lookup"><span data-stu-id="08018-126">G <-> V, G channel is mapped to the V channel, or vice versa.</span></span>
-   <span data-ttu-id="08018-127">B <-> W, канал B сопоставлен с каналом W или наоборот.</span><span class="sxs-lookup"><span data-stu-id="08018-127">B <-> W, B channel is mapped to the W channel, or vice versa.</span></span>
-   <span data-ttu-id="08018-128">> < Q/L, канал сопоставляется с каналом Q или L (в зависимости от того, какой из них доступен в формате назначения) или наоборот.</span><span class="sxs-lookup"><span data-stu-id="08018-128">A <-> Q/L, A channel is mapped to either the Q or the L channel (depending on which one is available in the destination format), or vice versa.</span></span>


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a><span data-ttu-id="08018-129">Сопоставление UV с RGBA</span><span class="sxs-lookup"><span data-stu-id="08018-129">Mapping UV to RGBA</span></span>

-   <span data-ttu-id="08018-130">U <-> R, канал U сопоставляется с каналом R или наоборот.</span><span class="sxs-lookup"><span data-stu-id="08018-130">U <-> R, U channel is mapped to the R channel, or vice versa.</span></span>
-   <span data-ttu-id="08018-131">V <-> G, канал V сопоставлен с каналом G или наоборот.</span><span class="sxs-lookup"><span data-stu-id="08018-131">V <-> G, V channel is mapped to the G channel, or vice versa.</span></span>
-   <span data-ttu-id="08018-132">1 <-> B, 1 сопоставляется с каналом B или наоборот.</span><span class="sxs-lookup"><span data-stu-id="08018-132">1 <-> B, 1 is mapped to the B channel, or vice versa.</span></span>
-   <span data-ttu-id="08018-133">1 <-> A, 1 сопоставляется с каналом, или наоборот.</span><span class="sxs-lookup"><span data-stu-id="08018-133">1 <-> A, 1 is mapped to the A channel, or vice versa.</span></span>

<span data-ttu-id="08018-134">Если канал не существует в источнике, предполагается, что он равен 1 (за исключением A8, где R, G, B считаются равными 0).</span><span class="sxs-lookup"><span data-stu-id="08018-134">If a channel does not exist in the source, it is assumed to be 1 (with the exception of A8, where R,G,B are assumed to be 0).</span></span> <span data-ttu-id="08018-135">Пример.</span><span class="sxs-lookup"><span data-stu-id="08018-135">For example:</span></span>


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a><span data-ttu-id="08018-136">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="08018-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08018-137">D3DX</span><span class="sxs-lookup"><span data-stu-id="08018-137">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



