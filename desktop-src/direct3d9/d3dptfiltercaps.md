---
description: Константы фильтрации текстур.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46adc4759290691e93ef68a8a4e212eacf5b6451
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343089"
---
# <a name="d3dptfiltercaps"></a><span data-ttu-id="3a0e9-103">D3DPTFILTERCAPS</span><span class="sxs-lookup"><span data-stu-id="3a0e9-103">D3DPTFILTERCAPS</span></span>

<span data-ttu-id="3a0e9-104">Константы фильтрации текстур.</span><span class="sxs-lookup"><span data-stu-id="3a0e9-104">Texture filtering constants.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3a0e9-105">#определенно</span><span class="sxs-lookup"><span data-stu-id="3a0e9-105">#define</span></span></td>
<td><span data-ttu-id="3a0e9-106">Описание</span><span class="sxs-lookup"><span data-stu-id="3a0e9-106">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a0e9-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span><span class="sxs-lookup"><span data-stu-id="3a0e9-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span></span></td>
<td><span data-ttu-id="3a0e9-108">Устройство поддерживает фильтрацию свертки по монохромному свертыванию.</span><span class="sxs-lookup"><span data-stu-id="3a0e9-108">Device supports monochrome convolution filtering.</span></span> <span data-ttu-id="3a0e9-109">Этот фильтр представлен элементом D3DTEXF_CONVOLUTIONMONO перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3a0e9-109">This filter is represented by the D3DTEXF_CONVOLUTIONMONO member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3a0e9-110">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="3a0e9-110">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="3a0e9-111">Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="3a0e9-111">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a0e9-112">D3DPTFILTERCAPS_MAGFPOINT</span><span class="sxs-lookup"><span data-stu-id="3a0e9-112">D3DPTFILTERCAPS_MAGFPOINT</span></span></td>
<td><span data-ttu-id="3a0e9-113">Устройство поддерживает многоэтапную фильтрацию на основе точек для увеличения текстур.</span><span class="sxs-lookup"><span data-stu-id="3a0e9-113">Device supports per-stage point-sample filtering for magnifying textures.</span></span> <span data-ttu-id="3a0e9-114">Фильтр увеличения точки-образца представлен элементом D3DTEXF_POINT перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3a0e9-114">The point-sample magnification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a0e9-115">D3DPTFILTERCAPS_MAGFLINEAR</span><span class="sxs-lookup"><span data-stu-id="3a0e9-115">D3DPTFILTERCAPS_MAGFLINEAR</span></span></td>
<td><span data-ttu-id="3a0e9-116">Устройство поддерживает фильтрацию билинейной интерполяции на уровне для увеличения MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="3a0e9-116">Device supports per-stage bilinear interpolation filtering for magnifying mipmaps.</span></span> <span data-ttu-id="3a0e9-117">Фильтр функции текстурирования интерполяции билинейной представлен элементом D3DTEXF_LINEAR перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3a0e9-117">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a0e9-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="3a0e9-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span></span></td>
<td><span data-ttu-id="3a0e9-119">Устройство поддерживает анизотропную фильтрацию по этапам для увеличения текстур.</span><span class="sxs-lookup"><span data-stu-id="3a0e9-119">Device supports per-stage anisotropic filtering for magnifying textures.</span></span> <span data-ttu-id="3a0e9-120">Фильтр анизотропной лупы представлен элементом D3DTEXF_ANISOTROPIC перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3a0e9-120">The anisotropic magnification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a0e9-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="3a0e9-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="3a0e9-122">Устройство поддерживает многоэтапную фильтрацию образцов для увеличения текстур.</span><span class="sxs-lookup"><span data-stu-id="3a0e9-122">Device supports per-stage pyramidal sample filtering for magnifying textures.</span></span> <span data-ttu-id="3a0e9-123">Фильтр попирамидальной лупы представляется элементом D3DTEXF_PYRAMIDALQUAD перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3a0e9-123">The pyramidal magnifying filter is represented by the D3DTEXF_PYRAMIDALQUAD member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a0e9-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="3a0e9-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="3a0e9-125">Устройство поддерживает грубую фильтрацию по Гауссу для увеличенных текстур.</span><span class="sxs-lookup"><span data-stu-id="3a0e9-125">Device supports per-stage Gaussian quad filtering for magnifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a0e9-126">D3DPTFILTERCAPS_MINFPOINT</span><span class="sxs-lookup"><span data-stu-id="3a0e9-126">D3DPTFILTERCAPS_MINFPOINT</span></span></td>
<td><span data-ttu-id="3a0e9-127">Устройство поддерживает многоэтапную фильтрацию на основе точек для текстур Минификация.</span><span class="sxs-lookup"><span data-stu-id="3a0e9-127">Device supports per-stage point-sample filtering for minifying textures.</span></span> <span data-ttu-id="3a0e9-128">Фильтр минификации в виде образца представляется элементом D3DTEXF_POINT перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3a0e9-128">The point-sample minification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a0e9-129">D3DPTFILTERCAPS_MINFLINEAR</span><span class="sxs-lookup"><span data-stu-id="3a0e9-129">D3DPTFILTERCAPS_MINFLINEAR</span></span></td>
<td><span data-ttu-id="3a0e9-130">Устройство поддерживает линейную фильтрацию по этапам для текстур Минификация.</span><span class="sxs-lookup"><span data-stu-id="3a0e9-130">Device supports per-stage linear filtering for minifying textures.</span></span> <span data-ttu-id="3a0e9-131">Фильтр линейного минификации представляется элементом D3DTEXF_LINEAR перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3a0e9-131">The linear minification filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a0e9-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="3a0e9-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span></span></td>
<td><span data-ttu-id="3a0e9-133">Устройство поддерживает анизотропную фильтрацию по этапам для текстур Минификация.</span><span class="sxs-lookup"><span data-stu-id="3a0e9-133">Device supports per-stage anisotropic filtering for minifying textures.</span></span> <span data-ttu-id="3a0e9-134">Фильтр анизотропной минификации представляется элементом D3DTEXF_ANISOTROPIC перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3a0e9-134">The anisotropic minification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a0e9-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="3a0e9-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="3a0e9-136">Устройство поддерживает фильтрацию образцов с поэтапным примером для текстур Минификация.</span><span class="sxs-lookup"><span data-stu-id="3a0e9-136">Device supports per-stage pyramidal sample filtering for minifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a0e9-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="3a0e9-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="3a0e9-138">Устройство поддерживает грубую фильтрацию по Гауссу для текстур Минификация.</span><span class="sxs-lookup"><span data-stu-id="3a0e9-138">Device supports per-stage Gaussian quad filtering for minifying textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a0e9-139">D3DPTFILTERCAPS_MIPFPOINT</span><span class="sxs-lookup"><span data-stu-id="3a0e9-139">D3DPTFILTERCAPS_MIPFPOINT</span></span></td>
<td><span data-ttu-id="3a0e9-140">Устройство поддерживает фильтрацию точек на уровне этапа для MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="3a0e9-140">Device supports per-stage point-sample filtering for mipmaps.</span></span> <span data-ttu-id="3a0e9-141">Фильтр функции текстурирования в виде образца представляется элементом D3DTEXF_POINT перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3a0e9-141">The point-sample mipmapping filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a0e9-142">D3DPTFILTERCAPS_MIPFLINEAR</span><span class="sxs-lookup"><span data-stu-id="3a0e9-142">D3DPTFILTERCAPS_MIPFLINEAR</span></span></td>
<td><span data-ttu-id="3a0e9-143">Устройство поддерживает фильтрацию билинейной интерполяции на уровне MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="3a0e9-143">Device supports per-stage bilinear interpolation filtering for mipmaps.</span></span> <span data-ttu-id="3a0e9-144">Фильтр функции текстурирования интерполяции билинейной представлен элементом D3DTEXF_LINEAR перечислимого типа <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3a0e9-144">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3a0e9-145">Эти константы используются членами Текстурефилтеркапс, Кубетекстурефилтеркапс, Волуметекстурефилтеркапс и Вертекстекстурефилтеркапс в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="3a0e9-145">These constants are used by TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps, and VertexTextureFilterCaps members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="3a0e9-146">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="3a0e9-146">Constant Information</span></span>



|  <span data-ttu-id="3a0e9-147">Требование</span><span class="sxs-lookup"><span data-stu-id="3a0e9-147">Requirement</span></span>                        | <span data-ttu-id="3a0e9-148">Значение</span><span class="sxs-lookup"><span data-stu-id="3a0e9-148">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="3a0e9-149">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3a0e9-149">Header</span></span>                   | <span data-ttu-id="3a0e9-150">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="3a0e9-150">d3d9caps.h</span></span> |
| <span data-ttu-id="3a0e9-151">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="3a0e9-151">Minimum operating system</span></span> | <span data-ttu-id="3a0e9-152">Windows 98</span><span class="sxs-lookup"><span data-stu-id="3a0e9-152">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3a0e9-153">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="3a0e9-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a0e9-154">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="3a0e9-154">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
