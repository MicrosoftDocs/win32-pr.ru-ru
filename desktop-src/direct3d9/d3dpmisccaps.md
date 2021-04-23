---
description: Различные флаги примитивной возможности драйвера.
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76af50a1e7f78f6441af9e985f55e42ee2298b46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262717"
---
# <a name="d3dpmisccaps"></a><span data-ttu-id="41ed6-103">D3DPMISCCAPS</span><span class="sxs-lookup"><span data-stu-id="41ed6-103">D3DPMISCCAPS</span></span>

<span data-ttu-id="41ed6-104">Различные флаги примитивной возможности драйвера.</span><span class="sxs-lookup"><span data-stu-id="41ed6-104">Miscellaneous driver primitive capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41ed6-105">#определенно</span><span class="sxs-lookup"><span data-stu-id="41ed6-105">#define</span></span></td>
<td><span data-ttu-id="41ed6-106">Значение</span><span class="sxs-lookup"><span data-stu-id="41ed6-106">Value</span></span></td>
<td><span data-ttu-id="41ed6-107">Описание</span><span class="sxs-lookup"><span data-stu-id="41ed6-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41ed6-108">D3DPMISCCAPS_MASKZ</span><span class="sxs-lookup"><span data-stu-id="41ed6-108">D3DPMISCCAPS_MASKZ</span></span></td>
<td><span data-ttu-id="41ed6-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="41ed6-109">0x00000002L</span></span></td>
<td><span data-ttu-id="41ed6-110">Устройство может включать и отключать изменение буфера глубины в операциях с пикселами.</span><span class="sxs-lookup"><span data-stu-id="41ed6-110">Device can enable and disable modification of the depth buffer on pixel operations.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41ed6-111">D3DPMISCCAPS_CULLNONE</span><span class="sxs-lookup"><span data-stu-id="41ed6-111">D3DPMISCCAPS_CULLNONE</span></span></td>
<td><span data-ttu-id="41ed6-112">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="41ed6-112">0x00000010L</span></span></td>
<td><span data-ttu-id="41ed6-113">Драйвер не выполняет отбор треугольников.</span><span class="sxs-lookup"><span data-stu-id="41ed6-113">The driver does not perform triangle culling.</span></span> <span data-ttu-id="41ed6-114">Соответствует элементу D3DCULL_NONE перечислимого типа <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="41ed6-114">This corresponds to the D3DCULL_NONE member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41ed6-115">D3DPMISCCAPS_CULLCW</span><span class="sxs-lookup"><span data-stu-id="41ed6-115">D3DPMISCCAPS_CULLCW</span></span></td>
<td><span data-ttu-id="41ed6-116">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="41ed6-116">0x00000020L</span></span></td>
<td><span data-ttu-id="41ed6-117">Драйвер поддерживает истечение треугольника по часовой стрелке в состоянии D3DRS_CULLMODE.</span><span class="sxs-lookup"><span data-stu-id="41ed6-117">The driver supports clockwise triangle culling through the D3DRS_CULLMODE state.</span></span> <span data-ttu-id="41ed6-118">(Это относится только к примитивам треугольника.) Этот флаг соответствует элементу D3DCULL_CW перечисляемого типа <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="41ed6-118">(This applies only to triangle primitives.) This flag corresponds to the D3DCULL_CW member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41ed6-119">D3DPMISCCAPS_CULLCCW</span><span class="sxs-lookup"><span data-stu-id="41ed6-119">D3DPMISCCAPS_CULLCCW</span></span></td>
<td><span data-ttu-id="41ed6-120">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="41ed6-120">0x00000040L</span></span></td>
<td><span data-ttu-id="41ed6-121">Драйвер поддерживает истечение против часовой стрелки в состоянии D3DRS_CULLMODE.</span><span class="sxs-lookup"><span data-stu-id="41ed6-121">The driver supports counterclockwise culling through the D3DRS_CULLMODE state.</span></span> <span data-ttu-id="41ed6-122">(Это относится только к примитивам треугольника.) Этот флаг соответствует элементу D3DCULL_CCW перечисляемого типа <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="41ed6-122">(This applies only to triangle primitives.) This flag corresponds to the D3DCULL_CCW member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41ed6-123">D3DPMISCCAPS_COLORWRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="41ed6-123">D3DPMISCCAPS_COLORWRITEENABLE</span></span></td>
<td><span data-ttu-id="41ed6-124">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="41ed6-124">0x00000100L</span></span></td>
<td><span data-ttu-id="41ed6-125">Устройство поддерживает операции записи на канал для буфера цвета целевого объекта рендеринга с помощью состояния D3DRS_COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="41ed6-125">Device supports per-channel writes for the render-target color buffer through the D3DRS_COLORWRITEENABLE state.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41ed6-126">D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</span><span class="sxs-lookup"><span data-stu-id="41ed6-126">D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</span></span></td>
<td><span data-ttu-id="41ed6-127">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="41ed6-127">0x00000200L</span></span></td>
<td><span data-ttu-id="41ed6-128">Устройство правильно выводит масштабируемые точки размером больше 1,0 в определяемые пользователем отрезкиные плоскости.</span><span class="sxs-lookup"><span data-stu-id="41ed6-128">Device correctly clips scaled points of size greater than 1.0 to user-defined clipping planes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41ed6-129">D3DPMISCCAPS_CLIPTLVERTS</span><span class="sxs-lookup"><span data-stu-id="41ed6-129">D3DPMISCCAPS_CLIPTLVERTS</span></span></td>
<td><span data-ttu-id="41ed6-130">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="41ed6-130">0x00000200L</span></span></td>
<td><span data-ttu-id="41ed6-131">Зажимы устройств после преобразования-примитивы вершин.</span><span class="sxs-lookup"><span data-stu-id="41ed6-131">Device clips post-transformed vertex primitives.</span></span> <span data-ttu-id="41ed6-132">Укажите D3DUSAGE_DONOTCLIP, если конвейер не должен выполнять отсечение.</span><span class="sxs-lookup"><span data-stu-id="41ed6-132">Specify D3DUSAGE_DONOTCLIP when the pipeline should not do any clipping.</span></span> <span data-ttu-id="41ed6-133">В этом случае может потребоваться дополнительная обрезка программного обеспечения во время рисования, требующая, чтобы буфер вершин наводился в системной памяти.</span><span class="sxs-lookup"><span data-stu-id="41ed6-133">For this case, additional software clipping may need to be performed at draw time, requiring the vertex buffer to be in system memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41ed6-134">D3DPMISCCAPS_TSSARGTEMP</span><span class="sxs-lookup"><span data-stu-id="41ed6-134">D3DPMISCCAPS_TSSARGTEMP</span></span></td>
<td><span data-ttu-id="41ed6-135">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="41ed6-135">0x00000400L</span></span></td>
<td><span data-ttu-id="41ed6-136">Устройство поддерживает <a href="d3dta.md">D3DTA</a> для временного регистра.</span><span class="sxs-lookup"><span data-stu-id="41ed6-136">Device supports <a href="d3dta.md">D3DTA</a> for temporary register.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41ed6-137">D3DPMISCCAPS_BLENDOP</span><span class="sxs-lookup"><span data-stu-id="41ed6-137">D3DPMISCCAPS_BLENDOP</span></span></td>
<td><span data-ttu-id="41ed6-138">0x00000800L</span><span class="sxs-lookup"><span data-stu-id="41ed6-138">0x00000800L</span></span></td>
<td><span data-ttu-id="41ed6-139">Устройство поддерживает операции альфа-смешения, кроме D3DBLENDOP_ADD.</span><span class="sxs-lookup"><span data-stu-id="41ed6-139">Device supports alpha-blending operations other than D3DBLENDOP_ADD.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41ed6-140">D3DPMISCCAPS_NULLREFERENCE</span><span class="sxs-lookup"><span data-stu-id="41ed6-140">D3DPMISCCAPS_NULLREFERENCE</span></span></td>
<td><span data-ttu-id="41ed6-141">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="41ed6-141">0x00000100L</span></span></td>
<td><span data-ttu-id="41ed6-142">Эталонное устройство, которое не подготавливается к просмотру.</span><span class="sxs-lookup"><span data-stu-id="41ed6-142">A reference device that does not render.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41ed6-143">D3DPMISCCAPS_INDEPENDENTWRITEMASKS</span><span class="sxs-lookup"><span data-stu-id="41ed6-143">D3DPMISCCAPS_INDEPENDENTWRITEMASKS</span></span></td>
<td><span data-ttu-id="41ed6-144">0x00004000L</span><span class="sxs-lookup"><span data-stu-id="41ed6-144">0x00004000L</span></span></td>
<td><span data-ttu-id="41ed6-145">Устройство поддерживает независимые маски записи для нескольких текстур элементов или нескольких целевых объектов прорисовки.</span><span class="sxs-lookup"><span data-stu-id="41ed6-145">Device supports independent write masks for multiple element textures or multiple render targets.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41ed6-146">D3DPMISCCAPS_PERSTAGECONSTANT</span><span class="sxs-lookup"><span data-stu-id="41ed6-146">D3DPMISCCAPS_PERSTAGECONSTANT</span></span></td>
<td><span data-ttu-id="41ed6-147">0x00008000L</span><span class="sxs-lookup"><span data-stu-id="41ed6-147">0x00008000L</span></span></td>
<td><span data-ttu-id="41ed6-148">Устройство поддерживает константы для каждого этапа.</span><span class="sxs-lookup"><span data-stu-id="41ed6-148">Device supports per-stage constants.</span></span> <span data-ttu-id="41ed6-149">См. D3DTSS_CONSTANT в <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="41ed6-149">See D3DTSS_CONSTANT in <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41ed6-150">D3DPMISCCAPS_POSTBLENDSRGBCONVERT</span><span class="sxs-lookup"><span data-stu-id="41ed6-150">D3DPMISCCAPS_POSTBLENDSRGBCONVERT</span></span></td>
<td><span data-ttu-id="41ed6-151">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="41ed6-151">0x00200000L</span></span></td>
<td><span data-ttu-id="41ed6-152">Устройство поддерживает преобразование в sRGB после смешения.</span><span class="sxs-lookup"><span data-stu-id="41ed6-152">Device supports conversion to sRGB after blending.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41ed6-153">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="41ed6-153">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="41ed6-154">Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="41ed6-154">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41ed6-155">D3DPMISCCAPS_FOGANDSPECULARALPHA</span><span class="sxs-lookup"><span data-stu-id="41ed6-155">D3DPMISCCAPS_FOGANDSPECULARALPHA</span></span></td>
<td><span data-ttu-id="41ed6-156">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="41ed6-156">0x00010000L</span></span></td>
<td><span data-ttu-id="41ed6-157">Устройство поддерживает отдельные туманы и бликовые альфа-каналы.</span><span class="sxs-lookup"><span data-stu-id="41ed6-157">Device supports separate fog and specular alpha.</span></span> <span data-ttu-id="41ed6-158">Многие устройства используют отраженный альфа-канал для хранения коэффициента тумана.</span><span class="sxs-lookup"><span data-stu-id="41ed6-158">Many devices use the specular alpha channel to store the fog factor.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41ed6-159">D3DPMISCCAPS_SEPARATEALPHABLEND</span><span class="sxs-lookup"><span data-stu-id="41ed6-159">D3DPMISCCAPS_SEPARATEALPHABLEND</span></span></td>
<td><span data-ttu-id="41ed6-160">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="41ed6-160">0x00020000L</span></span></td>
<td><span data-ttu-id="41ed6-161">Устройство поддерживает отдельные параметры смешения для альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="41ed6-161">Device supports separate blend settings for the alpha channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41ed6-162">D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</span><span class="sxs-lookup"><span data-stu-id="41ed6-162">D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</span></span></td>
<td><span data-ttu-id="41ed6-163">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="41ed6-163">0x00040000L</span></span></td>
<td><span data-ttu-id="41ed6-164">Устройство поддерживает разные битовые глубины для нескольких целевых объектов рендеринга.</span><span class="sxs-lookup"><span data-stu-id="41ed6-164">Device supports different bit depths for multiple render targets.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41ed6-165">D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</span><span class="sxs-lookup"><span data-stu-id="41ed6-165">D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</span></span></td>
<td><span data-ttu-id="41ed6-166">0x00080000L</span><span class="sxs-lookup"><span data-stu-id="41ed6-166">0x00080000L</span></span></td>
<td><span data-ttu-id="41ed6-167">Устройство поддерживает операции шейдера после пикселей для нескольких целевых объектов рендеринга.</span><span class="sxs-lookup"><span data-stu-id="41ed6-167">Device supports post-pixel shader operations for multiple render targets.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41ed6-168">D3DPMISCCAPS_FOGVERTEXCLAMPED</span><span class="sxs-lookup"><span data-stu-id="41ed6-168">D3DPMISCCAPS_FOGVERTEXCLAMPED</span></span></td>
<td><span data-ttu-id="41ed6-169">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="41ed6-169">0x00100000L</span></span></td>
<td><span data-ttu-id="41ed6-170">Фактор для зажимов устройства — коэффициент смешения на вершину.</span><span class="sxs-lookup"><span data-stu-id="41ed6-170">Device clamps fog blend factor per vertex.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="41ed6-171">Эти константы используются членом Примитивемисккапс объекта [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="41ed6-171">These constants are used by the PrimitiveMiscCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="41ed6-172">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="41ed6-172">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="41ed6-173">Header</span><span class="sxs-lookup"><span data-stu-id="41ed6-173">Header</span></span>                   | <span data-ttu-id="41ed6-174">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="41ed6-174">d3d9caps.h</span></span> |
| <span data-ttu-id="41ed6-175">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="41ed6-175">Minimum operating system</span></span> | <span data-ttu-id="41ed6-176">Windows 98</span><span class="sxs-lookup"><span data-stu-id="41ed6-176">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="41ed6-177">См. также</span><span class="sxs-lookup"><span data-stu-id="41ed6-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41ed6-178">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="41ed6-178">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
