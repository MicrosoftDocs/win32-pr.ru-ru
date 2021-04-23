---
description: D3DX — это служебная Библиотека, которая предоставляет вспомогательные службы. Это уровень выше компонента Direct3D.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Поддержка текстур в D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9c8d6da498a47d14fe57ca770ba96a6852ae41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701095"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a><span data-ttu-id="85023-104">Поддержка текстур в D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85023-104">Texture Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="85023-105">D3DX — это служебная Библиотека, которая предоставляет вспомогательные службы.</span><span class="sxs-lookup"><span data-stu-id="85023-105">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="85023-106">Это уровень выше компонента Direct3D.</span><span class="sxs-lookup"><span data-stu-id="85023-106">It is a layer above the Direct3D component.</span></span>

## <a name="textures"></a><span data-ttu-id="85023-107">Текстуры</span><span class="sxs-lookup"><span data-stu-id="85023-107">Textures</span></span>

<span data-ttu-id="85023-108">В следующих разделах поддерживаются различные текстуры.</span><span class="sxs-lookup"><span data-stu-id="85023-108">Many different textures are supported in the following topics.</span></span>

-   <span data-ttu-id="85023-109">Стандартная поддержка текстур мипмаппед.</span><span class="sxs-lookup"><span data-stu-id="85023-109">Standard mipmapped texture support.</span></span> <span data-ttu-id="85023-110">См. раздел [Автоматическое создание MIP-карты (Direct3D 9)](automatic-generation-of-mipmaps.md).</span><span class="sxs-lookup"><span data-stu-id="85023-110">See [Automatic Generation of Mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).</span></span>
-   <span data-ttu-id="85023-111">Поддержка схемы куба.</span><span class="sxs-lookup"><span data-stu-id="85023-111">Cube map support.</span></span> <span data-ttu-id="85023-112">См. раздел [сопоставление кубических сред (Direct3D 9)](cubic-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="85023-112">See [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>
-   <span data-ttu-id="85023-113">Поддержка текстуры тома.</span><span class="sxs-lookup"><span data-stu-id="85023-113">Volume texture support.</span></span> <span data-ttu-id="85023-114">См. раздел [ресурсы текстуры для томов (Direct3D 9)](volume-texture-resources.md).</span><span class="sxs-lookup"><span data-stu-id="85023-114">See [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>
-   <span data-ttu-id="85023-115">Поддержка сопоставления среды.</span><span class="sxs-lookup"><span data-stu-id="85023-115">Environment mapping support.</span></span> <span data-ttu-id="85023-116">См. раздел [сопоставление среды (Direct3D 9)](environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="85023-116">See [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>
-   <span data-ttu-id="85023-117">Поддержка сопоставления рельефов.</span><span class="sxs-lookup"><span data-stu-id="85023-117">Bump mapping support.</span></span> <span data-ttu-id="85023-118">См. раздел [«назначение выпуклости» (Direct3D 9)](bump-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="85023-118">See [Bump Mapping (Direct3D 9)](bump-mapping.md).</span></span>

### <a name="texture-color-conversion"></a><span data-ttu-id="85023-119">Преобразование цвета текстуры</span><span class="sxs-lookup"><span data-stu-id="85023-119">Texture Color Conversion</span></span>

<span data-ttu-id="85023-120">При использовании любых функций D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx или D3DXCreateVolumeTexturexxx может потребоваться преобразование цветов.</span><span class="sxs-lookup"><span data-stu-id="85023-120">When using any of the D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx, or D3DXCreateVolumeTexturexxx functions, color conversion might need to be performed.</span></span> <span data-ttu-id="85023-121">Например, одна поверхность может иметь тип RGBA, а другая может быть УВВК.</span><span class="sxs-lookup"><span data-stu-id="85023-121">For example, one surface might be type RGBA and the other might be UVWQ.</span></span> <span data-ttu-id="85023-122">В случае с непохожими форматами используется следующая последовательность преобразования:</span><span class="sxs-lookup"><span data-stu-id="85023-122">For cases of dissimilar formats, the conversion sequence is as follows:</span></span>

### <a name="mapping-rgba-to-uvwq"></a><span data-ttu-id="85023-123">Сопоставление RGBA и УВВК</span><span class="sxs-lookup"><span data-stu-id="85023-123">Mapping RGBA to UVWQ</span></span>

-   <span data-ttu-id="85023-124">R <-> U, канал R сопоставляется с каналом U или наоборот.</span><span class="sxs-lookup"><span data-stu-id="85023-124">R <-> U, R channel is mapped to the U channel, or vice versa.</span></span>
-   <span data-ttu-id="85023-125">G <-> V, G Channel сопоставляется с каналом V или наоборот.</span><span class="sxs-lookup"><span data-stu-id="85023-125">G <-> V, G channel is mapped to the V channel, or vice versa.</span></span>
-   <span data-ttu-id="85023-126">B <-> W, канал B сопоставлен с каналом W или наоборот.</span><span class="sxs-lookup"><span data-stu-id="85023-126">B <-> W, B channel is mapped to the W channel, or vice versa.</span></span>
-   <span data-ttu-id="85023-127">> < Q/L, канал сопоставляется с каналом Q или L (в зависимости от того, какой из них доступен в формате назначения) или наоборот.</span><span class="sxs-lookup"><span data-stu-id="85023-127">A <-> Q/L, A channel is mapped to either the Q or the L channel (depending on which one is available in the destination format), or vice versa.</span></span>


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a><span data-ttu-id="85023-128">Сопоставление UV с RGBA</span><span class="sxs-lookup"><span data-stu-id="85023-128">Mapping UV to RGBA</span></span>

-   <span data-ttu-id="85023-129">U <-> R, канал U сопоставляется с каналом R или наоборот.</span><span class="sxs-lookup"><span data-stu-id="85023-129">U <-> R, U channel is mapped to the R channel, or vice versa.</span></span>
-   <span data-ttu-id="85023-130">V <-> G, канал V сопоставлен с каналом G или наоборот.</span><span class="sxs-lookup"><span data-stu-id="85023-130">V <-> G, V channel is mapped to the G channel, or vice versa.</span></span>
-   <span data-ttu-id="85023-131">1 <-> B, 1 сопоставляется с каналом B или наоборот.</span><span class="sxs-lookup"><span data-stu-id="85023-131">1 <-> B, 1 is mapped to the B channel, or vice versa.</span></span>
-   <span data-ttu-id="85023-132">1 <-> A, 1 сопоставляется с каналом, или наоборот.</span><span class="sxs-lookup"><span data-stu-id="85023-132">1 <-> A, 1 is mapped to the A channel, or vice versa.</span></span>

<span data-ttu-id="85023-133">Если канал не существует в источнике, предполагается, что он равен 1 (за исключением A8, где R, G, B считаются равными 0).</span><span class="sxs-lookup"><span data-stu-id="85023-133">If a channel does not exist in the source, it is assumed to be 1 (with the exception of A8, where R,G,B are assumed to be 0).</span></span> <span data-ttu-id="85023-134">Пример:</span><span class="sxs-lookup"><span data-stu-id="85023-134">For example:</span></span>


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a><span data-ttu-id="85023-135">См. также</span><span class="sxs-lookup"><span data-stu-id="85023-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85023-136">D3DX</span><span class="sxs-lookup"><span data-stu-id="85023-136">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



