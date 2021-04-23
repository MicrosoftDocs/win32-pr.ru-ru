---
title: Указание целевых объектов компилятора
description: Здесь перечислены целевые объекты для различных профилей, которые поддерживаются D3DCompile \ функции и компилятор HLSL.
ms.assetid: 594E1C14-C1D4-4207-91A1-28892CE6D821
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68fc6c5a202ad537b02a20846d36526533240f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413605"
---
# <a name="specifying-compiler-targets"></a><span data-ttu-id="620be-103">Указание целевых объектов компилятора</span><span class="sxs-lookup"><span data-stu-id="620be-103">Specifying Compiler Targets</span></span>

<span data-ttu-id="620be-104">Необходимо указать целевой объект шейдера — набор функций шейдера — для компиляции при вызове функции [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2)или [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) .</span><span class="sxs-lookup"><span data-stu-id="620be-104">You need to specify the shader target — set of shader features — to compile against when you call the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2), or [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) function.</span></span> <span data-ttu-id="620be-105">Здесь перечислены целевые объекты для различных профилей, которые поддерживаются функциями **D3DCompile \*** и компилятором HLSL.</span><span class="sxs-lookup"><span data-stu-id="620be-105">Here we list the targets for various profiles that the **D3DCompile\*** functions and the HLSL compiler support.</span></span>

-   [<span data-ttu-id="620be-106">Уровни компонентов Direct3D 11,0 и 11,1</span><span class="sxs-lookup"><span data-stu-id="620be-106">Direct3D 11.0 and 11.1 feature levels</span></span>](#direct3d-110-and-111-feature-levels)
-   [<span data-ttu-id="620be-107">Уровень компонентов Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="620be-107">Direct3D 10.1 feature level</span></span>](#direct3d-101-feature-level)
-   [<span data-ttu-id="620be-108">Уровень компонентов Direct3D 10,0</span><span class="sxs-lookup"><span data-stu-id="620be-108">Direct3D 10.0 feature level</span></span>](#direct3d-100-feature-level)
-   [<span data-ttu-id="620be-109">Уровни компонентов Direct3D 9,1, 9,2 и 9,3</span><span class="sxs-lookup"><span data-stu-id="620be-109">Direct3D 9.1, 9.2, and 9.3 feature levels</span></span>](#direct3d-91-92-and-93-feature-levels)
-   [<span data-ttu-id="620be-110">Устаревшая модель шейдера Direct3D 9 3,0</span><span class="sxs-lookup"><span data-stu-id="620be-110">Legacy Direct3D 9 Shader Model 3.0</span></span>](#legacy-direct3d-9-shader-model-30)
-   [<span data-ttu-id="620be-111">Устаревшая модель шейдера Direct3D 9 2,0</span><span class="sxs-lookup"><span data-stu-id="620be-111">Legacy Direct3D 9 Shader Model 2.0</span></span>](#legacy-direct3d-9-shader-model-20)
-   [<span data-ttu-id="620be-112">Устаревшая модель шейдера Direct3D 9 с 1. x</span><span class="sxs-lookup"><span data-stu-id="620be-112">Legacy Direct3D 9 Shader Model 1.x</span></span>](#legacy-direct3d-9-shader-model-1x)
-   [<span data-ttu-id="620be-113">Устаревшие эффекты</span><span class="sxs-lookup"><span data-stu-id="620be-113">Legacy Effects</span></span>](#legacy-effects)
-   [<span data-ttu-id="620be-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="620be-114">Notes</span></span>](#notes)
-   [<span data-ttu-id="620be-115">См. также</span><span class="sxs-lookup"><span data-stu-id="620be-115">Related topics</span></span>](#related-topics)

## <a name="direct3d-110-and-111-feature-levels"></a><span data-ttu-id="620be-116">Уровни компонентов Direct3D 11,0 и 11,1</span><span class="sxs-lookup"><span data-stu-id="620be-116">Direct3D 11.0 and 11.1 feature levels</span></span>

<span data-ttu-id="620be-117">Ниже приведены цели шейдера, поддерживаемые [уровнями компонентов](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 11,0 и 11,1.</span><span class="sxs-lookup"><span data-stu-id="620be-117">Here are the shader targets that Direct3D 11.0 and 11.1 [feature levels](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) support.</span></span>



| <span data-ttu-id="620be-118">целевого объекта</span><span class="sxs-lookup"><span data-stu-id="620be-118">Target</span></span>   | <span data-ttu-id="620be-119">Описание</span><span class="sxs-lookup"><span data-stu-id="620be-119">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="620be-120">CS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="620be-120">cs\_5\_0</span></span> | <span data-ttu-id="620be-121">DirectCompute 5,0 ([COMPUTE Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))</span><span class="sxs-lookup"><span data-stu-id="620be-121">DirectCompute 5.0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))</span></span>                              |
| <span data-ttu-id="620be-122">DS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="620be-122">ds\_5\_0</span></span> | [<span data-ttu-id="620be-123">Шейдер доменов</span><span class="sxs-lookup"><span data-stu-id="620be-123">Domain shader</span></span>](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)             |
| <span data-ttu-id="620be-124">GS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="620be-124">gs\_5\_0</span></span> | <span data-ttu-id="620be-125">[Шейдер геометрии](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="620be-125">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="620be-126">HS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="620be-126">hs\_5\_0</span></span> | [<span data-ttu-id="620be-127">Шейдер поверхности</span><span class="sxs-lookup"><span data-stu-id="620be-127">Hull shader</span></span>](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                   |
| <span data-ttu-id="620be-128">PS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="620be-128">ps\_5\_0</span></span> | <span data-ttu-id="620be-129">[Построитель текстуры](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="620be-129">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="620be-130">VS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="620be-130">vs\_5\_0</span></span> | <span data-ttu-id="620be-131">[Вершинный построитель текстуры](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="620be-131">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-101-feature-level"></a><span data-ttu-id="620be-132">Уровень компонентов Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="620be-132">Direct3D 10.1 feature level</span></span>

<span data-ttu-id="620be-133">Ниже приведены целевые шейдеры, поддерживаемые [уровнем компонентов](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="620be-133">Here are the shader targets that the Direct3D 10.1 [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) supports.</span></span>



| <span data-ttu-id="620be-134">целевого объекта</span><span class="sxs-lookup"><span data-stu-id="620be-134">Target</span></span>   | <span data-ttu-id="620be-135">Описание</span><span class="sxs-lookup"><span data-stu-id="620be-135">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="620be-136">CS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="620be-136">cs\_4\_1</span></span> | <span data-ttu-id="620be-137">DirectCompute 4,1 ([COMPUTE Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹</span><span class="sxs-lookup"><span data-stu-id="620be-137">DirectCompute 4.1 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹</span></span>                             |
| <span data-ttu-id="620be-138">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="620be-138">gs\_4\_1</span></span> | <span data-ttu-id="620be-139">[Шейдер геометрии](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="620be-139">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="620be-140">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="620be-140">ps\_4\_1</span></span> | <span data-ttu-id="620be-141">[Построитель текстуры](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="620be-141">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="620be-142">VS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="620be-142">vs\_4\_1</span></span> | <span data-ttu-id="620be-143">[Вершинный построитель текстуры](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="620be-143">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-100-feature-level"></a><span data-ttu-id="620be-144">Уровень компонентов Direct3D 10,0</span><span class="sxs-lookup"><span data-stu-id="620be-144">Direct3D 10.0 feature level</span></span>

<span data-ttu-id="620be-145">Ниже приведены целевые шейдеры, поддерживаемые [уровнем компонентов](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="620be-145">Here are the shader targets that the Direct3D 10.0 [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) supports.</span></span>



| <span data-ttu-id="620be-146">целевого объекта</span><span class="sxs-lookup"><span data-stu-id="620be-146">Target</span></span>   | <span data-ttu-id="620be-147">Описание</span><span class="sxs-lookup"><span data-stu-id="620be-147">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="620be-148">CS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="620be-148">cs\_4\_0</span></span> | <span data-ttu-id="620be-149">DirectCompute 4,0 ([COMPUTE Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹</span><span class="sxs-lookup"><span data-stu-id="620be-149">DirectCompute 4.0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹</span></span>                             |
| <span data-ttu-id="620be-150">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="620be-150">gs\_4\_0</span></span> | <span data-ttu-id="620be-151">[Шейдер геометрии](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="620be-151">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="620be-152">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="620be-152">ps\_4\_0</span></span> | <span data-ttu-id="620be-153">[Построитель текстуры](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="620be-153">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="620be-154">VS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="620be-154">vs\_4\_0</span></span> | <span data-ttu-id="620be-155">[Вершинный построитель текстуры](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="620be-155">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-91-92-and-93-feature-levels"></a><span data-ttu-id="620be-156">Уровни компонентов Direct3D 9,1, 9,2 и 9,3</span><span class="sxs-lookup"><span data-stu-id="620be-156">Direct3D 9.1, 9.2, and 9.3 feature levels</span></span>

<span data-ttu-id="620be-157">Ниже приведены цели шейдера, поддерживаемые [уровнями функций](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 9,1, 9,2 и 9,3.</span><span class="sxs-lookup"><span data-stu-id="620be-157">Here are the shader targets that Direct3D 9.1, 9.2 and 9.3 [feature levels](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) support.</span></span>

> [!Note]  
> <span data-ttu-id="620be-158">При использовании \* \_ \_ \_ профилей шейдера с 4 уровнями \_ 9 \_ x HLSL вы неявно используете профили [шейдера 2. x](dx-graphics-hlsl-sm2.md) для поддержки аппаратного обеспечения с поддержкой Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="620be-158">When you use the \*\_4\_0\_level\_9\_x HLSL shader profiles, you implicitly use of the [Shader Model 2.x](dx-graphics-hlsl-sm2.md) profiles to support Direct3D 9 capable hardware.</span></span> <span data-ttu-id="620be-159">Профили Shader модели 2. x поддерживают более ограниченное поведение управления потоком, чем профили [шейдера 4. x](dx-graphics-hlsl-sm4.md) и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="620be-159">Shader Model 2.x profiles support more limited flow control behavior than the [Shader Model 4.x](dx-graphics-hlsl-sm4.md) and later profiles.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="620be-160">целевого объекта</span><span class="sxs-lookup"><span data-stu-id="620be-160">Target</span></span></th>
<th><span data-ttu-id="620be-161">Описание</span><span class="sxs-lookup"><span data-stu-id="620be-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="620be-162">ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="620be-162">ps_4_0_level_9_1</span></span></td>
<td><span data-ttu-id="620be-163">[Построитель текстуры](/previous-versions//bb205146(v=vs.85)) для 9,1 и 9,2 (аналогичные ограничения ps_2_0)</span><span class="sxs-lookup"><span data-stu-id="620be-163">[Pixel shader](/previous-versions//bb205146(v=vs.85)) for 9.1 and 9.2 (similar limits to ps_2_0)</span></span>
<ul>
<li><span data-ttu-id="620be-164">64 арифметические и 32 текстурных инструкций</span><span class="sxs-lookup"><span data-stu-id="620be-164">64 arithmetic and 32 texture instructions</span></span></li>
<li><span data-ttu-id="620be-165">12 временных регистров</span><span class="sxs-lookup"><span data-stu-id="620be-165">12 temporary registers</span></span></li>
<li><span data-ttu-id="620be-166">4 уровня зависимых операций чтения</span><span class="sxs-lookup"><span data-stu-id="620be-166">4 levels of dependent reads</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="620be-167">ps_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="620be-167">ps_4_0_level_9_3</span></span></td>
<td><span data-ttu-id="620be-168"><a href="/previous-versions//bb205146(v=vs.85)">Построитель текстуры</a> для 9,3 (аналогичные ограничения ps_2_x ² с дополнительными функциями шейдеров)</span><span class="sxs-lookup"><span data-stu-id="620be-168"><a href="/previous-versions//bb205146(v=vs.85)">Pixel shader</a> for 9.3 (similar limits to ps_2_x² with additional shader features)</span></span>
<ul>
<li><span data-ttu-id="620be-169">512 инструкции</span><span class="sxs-lookup"><span data-stu-id="620be-169">512 instructions</span></span></li>
<li><span data-ttu-id="620be-170">32. временные регистры</span><span class="sxs-lookup"><span data-stu-id="620be-170">32 temporary registers</span></span></li>
<li><span data-ttu-id="620be-171">Статическое управление потоком (максимальная глубина 4)</span><span class="sxs-lookup"><span data-stu-id="620be-171">Static flow control (max depth of 4)</span></span></li>
<li><span data-ttu-id="620be-172">Динамическое управление потоком (максимальная глубина 24)</span><span class="sxs-lookup"><span data-stu-id="620be-172">Dynamic flow control (max depth of 24)</span></span></li>
<li><span data-ttu-id="620be-173">D3DPS20CAPS_ARBITRARYSWIZZLE</span><span class="sxs-lookup"><span data-stu-id="620be-173">D3DPS20CAPS_ARBITRARYSWIZZLE</span></span></li>
<li><span data-ttu-id="620be-174">D3DPS20CAPS_GRADIENTINSTRUCTIONS</span><span class="sxs-lookup"><span data-stu-id="620be-174">D3DPS20CAPS_GRADIENTINSTRUCTIONS</span></span></li>
<li><span data-ttu-id="620be-175">D3DPS20CAPS_PREDICATION</span><span class="sxs-lookup"><span data-stu-id="620be-175">D3DPS20CAPS_PREDICATION</span></span></li>
<li><span data-ttu-id="620be-176">D3DPS20CAPS_NODEPENDENTREADLIMIT</span><span class="sxs-lookup"><span data-stu-id="620be-176">D3DPS20CAPS_NODEPENDENTREADLIMIT</span></span></li>
<li><span data-ttu-id="620be-177">D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</span><span class="sxs-lookup"><span data-stu-id="620be-177">D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="620be-178">vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="620be-178">vs_4_0_level_9_1</span></span></td>
<td><span data-ttu-id="620be-179"><a href="/previous-versions//bb205146(v=vs.85)">Шейдер вершин</a> для 9,1 и 9,2 (аналогично VS_2_0)</span><span class="sxs-lookup"><span data-stu-id="620be-179"><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> for 9.1 and 9.2 (similar to vs_2_0)</span></span>
<ul>
<li><span data-ttu-id="620be-180">256 инструкции</span><span class="sxs-lookup"><span data-stu-id="620be-180">256 instructions</span></span></li>
<li><span data-ttu-id="620be-181">12 временных регистров</span><span class="sxs-lookup"><span data-stu-id="620be-181">12 temporary registers</span></span></li>
<li><span data-ttu-id="620be-182">Статическое управление потоком (максимальная глубина 1)</span><span class="sxs-lookup"><span data-stu-id="620be-182">Static flow control (max depth of 1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="620be-183">vs_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="620be-183">vs_4_0_level_9_3</span></span></td>
<td><span data-ttu-id="620be-184"><a href="/previous-versions//bb205146(v=vs.85)">Шейдер вершин</a> для 9,3 (аналогично vs_2_a ² с дополнительными функциями шейдера и созданием экземпляров)</span><span class="sxs-lookup"><span data-stu-id="620be-184"><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> for 9.3 (similar to vs_2_a² with additional shader features and instancing)</span></span>
<ul>
<li><span data-ttu-id="620be-185">256 инструкции</span><span class="sxs-lookup"><span data-stu-id="620be-185">256 instructions</span></span></li>
<li><span data-ttu-id="620be-186">32. временные регистры</span><span class="sxs-lookup"><span data-stu-id="620be-186">32 temporary registers</span></span></li>
<li><span data-ttu-id="620be-187">Статическое управление потоком (максимальная глубина 4)</span><span class="sxs-lookup"><span data-stu-id="620be-187">Static flow control (max depth of 4)</span></span></li>
<li><span data-ttu-id="620be-188">D3DVS20CAPS_PREDICATION</span><span class="sxs-lookup"><span data-stu-id="620be-188">D3DVS20CAPS_PREDICATION</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="legacy-direct3d-9-shader-model-30"></a><span data-ttu-id="620be-189">Устаревшая модель шейдера Direct3D 9 3,0</span><span class="sxs-lookup"><span data-stu-id="620be-189">Legacy Direct3D 9 Shader Model 3.0</span></span>

<span data-ttu-id="620be-190">Ниже приведены цели шейдера для устаревшей модели шейдера Direct3D 9 3,0 ³.</span><span class="sxs-lookup"><span data-stu-id="620be-190">Here are the shader targets for legacy Direct3D 9 shader model 3.0³.</span></span>



| <span data-ttu-id="620be-191">целевого объекта</span><span class="sxs-lookup"><span data-stu-id="620be-191">Target</span></span>    | <span data-ttu-id="620be-192">Описание</span><span class="sxs-lookup"><span data-stu-id="620be-192">Description</span></span>                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="620be-193">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="620be-193">ps\_3\_0</span></span>  | <span data-ttu-id="620be-194">[Построитель текстуры](/previous-versions//bb205146(v=vs.85)) 3,0</span><span class="sxs-lookup"><span data-stu-id="620be-194">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 3.0</span></span>               |
| <span data-ttu-id="620be-195">PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="620be-195">ps\_3\_sw</span></span> | <span data-ttu-id="620be-196">[Шейдер пикселей](/previous-versions//bb205146(v=vs.85)) 3,0 (программное обеспечение)</span><span class="sxs-lookup"><span data-stu-id="620be-196">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 3.0 (software)</span></span>    |
| <span data-ttu-id="620be-197">VS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="620be-197">vs\_3\_0</span></span>  | <span data-ttu-id="620be-198">[Шейдер вершин](/previous-versions//bb205146(v=vs.85)) 3,0</span><span class="sxs-lookup"><span data-stu-id="620be-198">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 3.0</span></span>            |
| <span data-ttu-id="620be-199">VS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="620be-199">vs\_3\_sw</span></span> | <span data-ttu-id="620be-200">[Шейдер вершин](/previous-versions//bb205146(v=vs.85)) 3,0 (программное обеспечение)</span><span class="sxs-lookup"><span data-stu-id="620be-200">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 3.0 (software)</span></span> |



 

## <a name="legacy-direct3d-9-shader-model-20"></a><span data-ttu-id="620be-201">Устаревшая модель шейдера Direct3D 9 2,0</span><span class="sxs-lookup"><span data-stu-id="620be-201">Legacy Direct3D 9 Shader Model 2.0</span></span>

<span data-ttu-id="620be-202">Ниже приведены цели шейдера для устаревшей модели шейдера Direct3D 9 2,0 ³.</span><span class="sxs-lookup"><span data-stu-id="620be-202">Here are the shader targets for legacy Direct3D 9 shader model 2.0³.</span></span>



| <span data-ttu-id="620be-203">целевого объекта</span><span class="sxs-lookup"><span data-stu-id="620be-203">Target</span></span>    | <span data-ttu-id="620be-204">Описание</span><span class="sxs-lookup"><span data-stu-id="620be-204">Description</span></span>                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="620be-205">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="620be-205">ps\_2\_0</span></span>  | <span data-ttu-id="620be-206">[Построитель текстуры](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="620be-206">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2.0</span></span>             |
| <span data-ttu-id="620be-207">PS \_ 2 \_ a</span><span class="sxs-lookup"><span data-stu-id="620be-207">ps\_2\_a</span></span>  | <span data-ttu-id="620be-208">[Шейдер пикселей](/previous-versions//bb205146(v=vs.85)) 2A</span><span class="sxs-lookup"><span data-stu-id="620be-208">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2a</span></span>              |
| <span data-ttu-id="620be-209">PS \_ 2 \_ b</span><span class="sxs-lookup"><span data-stu-id="620be-209">ps\_2\_b</span></span>  | <span data-ttu-id="620be-210">[Шейдер пикселей](/previous-versions//bb205146(v=vs.85)) 2b</span><span class="sxs-lookup"><span data-stu-id="620be-210">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2b</span></span>              |
| <span data-ttu-id="620be-211">PS \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="620be-211">ps\_2\_sw</span></span> | <span data-ttu-id="620be-212">Программное обеспечение [построителя текстуры](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="620be-212">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2.0 software</span></span>    |
| <span data-ttu-id="620be-213">VS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="620be-213">vs\_2\_0</span></span>  | <span data-ttu-id="620be-214">[Шейдер вершин](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="620be-214">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2.0</span></span>          |
| <span data-ttu-id="620be-215">VS \_ 2 \_ a</span><span class="sxs-lookup"><span data-stu-id="620be-215">vs\_2\_a</span></span>  | <span data-ttu-id="620be-216">[Шейдер вершин](/previous-versions//bb205146(v=vs.85)) 2A</span><span class="sxs-lookup"><span data-stu-id="620be-216">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2a</span></span>           |
| <span data-ttu-id="620be-217">VS \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="620be-217">vs\_2\_sw</span></span> | <span data-ttu-id="620be-218">Программное обеспечение [вершинного шейдера](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="620be-218">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2.0 software</span></span> |



 

## <a name="legacy-direct3d-9-shader-model-1x"></a><span data-ttu-id="620be-219">Устаревшая модель шейдера Direct3D 9 с 1. x</span><span class="sxs-lookup"><span data-stu-id="620be-219">Legacy Direct3D 9 Shader Model 1.x</span></span>

<span data-ttu-id="620be-220">Ниже приведены цели шейдера для устаревшей версии Direct3D 9 Shader Model 1. x ⁴.</span><span class="sxs-lookup"><span data-stu-id="620be-220">Here are the shader targets for legacy Direct3D 9 shader model 1.x⁴.</span></span>



| <span data-ttu-id="620be-221">целевого объекта</span><span class="sxs-lookup"><span data-stu-id="620be-221">Target</span></span>   | <span data-ttu-id="620be-222">Описание</span><span class="sxs-lookup"><span data-stu-id="620be-222">Description</span></span>                                                                                                                                                                       |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="620be-223">TX \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="620be-223">tx\_1\_0</span></span> | <span data-ttu-id="620be-224">Профиль шейдера текстуры, который использует устаревшие функции D3DX9 ⁵ [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) и [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx)</span><span class="sxs-lookup"><span data-stu-id="620be-224">Texture shader profile that legacy D3DX9⁵ functions [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) and [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) use</span></span> |
| <span data-ttu-id="620be-225">VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="620be-225">vs\_1\_1</span></span> | <span data-ttu-id="620be-226">[Шейдер вершин](/previous-versions//bb205146(v=vs.85)) 1,1</span><span class="sxs-lookup"><span data-stu-id="620be-226">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 1.1</span></span>                                                            |



 

## <a name="legacy-effects"></a><span data-ttu-id="620be-227">Устаревшие эффекты</span><span class="sxs-lookup"><span data-stu-id="620be-227">Legacy Effects</span></span>

<span data-ttu-id="620be-228">Ниже приведены целевые эффекты для устаревших эффектов.</span><span class="sxs-lookup"><span data-stu-id="620be-228">Here are the effect targets for legacy effects.</span></span>



| <span data-ttu-id="620be-229">целевого объекта</span><span class="sxs-lookup"><span data-stu-id="620be-229">Target</span></span>   | <span data-ttu-id="620be-230">Описание</span><span class="sxs-lookup"><span data-stu-id="620be-230">Description</span></span>                               |
|----------|-------------------------------------------|
| <span data-ttu-id="620be-231">FX \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="620be-231">fx\_2\_0</span></span> | <span data-ttu-id="620be-232">Эффекты (FX) для Direct3D 9 в D3DX9 ⁵</span><span class="sxs-lookup"><span data-stu-id="620be-232">Effects (FX) for Direct3D 9 in D3DX9⁵</span></span>     |
| <span data-ttu-id="620be-233">FX \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="620be-233">fx\_4\_0</span></span> | <span data-ttu-id="620be-234">Эффекты (FX) для Direct3D 10,0 в D3DX10 ⁵</span><span class="sxs-lookup"><span data-stu-id="620be-234">Effects (FX) for Direct3D 10.0 in D3DX10⁵</span></span> |
| <span data-ttu-id="620be-235">FX \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="620be-235">fx\_4\_1</span></span> | <span data-ttu-id="620be-236">Эффекты (FX) для Direct3D 10,1 в D3DX10 ⁵</span><span class="sxs-lookup"><span data-stu-id="620be-236">Effects (FX) for Direct3D 10.1 in D3DX10⁵</span></span> |
| <span data-ttu-id="620be-237">FX \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="620be-237">fx\_5\_0</span></span> | <span data-ttu-id="620be-238">Эффекты (FX) для Direct3D 11 ⁵</span><span class="sxs-lookup"><span data-stu-id="620be-238">Effects (FX) for Direct3D 11⁵</span></span>             |



 

## <a name="notes"></a><span data-ttu-id="620be-239">Примечания</span><span class="sxs-lookup"><span data-stu-id="620be-239">Notes</span></span>

<span data-ttu-id="620be-240">Ниже приведены некоторые замечания, на которые ссылаются предыдущие разделы.</span><span class="sxs-lookup"><span data-stu-id="620be-240">Here are some notes that the preceding sections refer to:</span></span>

1.  <span data-ttu-id="620be-241">устройства [уровня](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0 и 10,1 могут дополнительно поддерживать DirectCompute.</span><span class="sxs-lookup"><span data-stu-id="620be-241">[feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 and 10.1 devices can optionally support DirectCompute.</span></span> <span data-ttu-id="620be-242">Чтобы проверить поддержку, используйте [**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) с [**\_ \_ \_ \_ \_ параметрами оборудования D3D11 Feature D3D10 X**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).</span><span class="sxs-lookup"><span data-stu-id="620be-242">To verify support, use [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) with [**D3D11\_FEATURE\_D3D10\_X\_HARDWARE\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).</span></span>
2.  <span data-ttu-id="620be-243">на [уровне компонентов](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9,3 эффективно требуется оборудование, которое соответствует требованиям для [устаревшей модели шейдера Direct3D 9 (3,0](#legacy-direct3d-9-shader-model-30)), но этот уровень функций не использует \_ \_ целевые объекты VS 3 0 или PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="620be-243">[feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9.3 effectively requires hardware that complies with the requirements for [legacy Direct3D 9 shader model 3.0](#legacy-direct3d-9-shader-model-30), but this feature level does not make use of vs\_3\_0 or ps\_3\_0 targets.</span></span>
3.  <span data-ttu-id="620be-244">Используйте только устаревшие модели шейдеров Direct3D 9 с API Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="620be-244">Only use legacy Direct3D 9 shader models with the Direct3D 9 API.</span></span> <span data-ttu-id="620be-245">Вместо этого используйте профили 9. x с API Direct3D 10. x и 11. x.</span><span class="sxs-lookup"><span data-stu-id="620be-245">Instead, use the 9.x profiles with the Direct3D 10.x and 11.x API.</span></span>
4.  <span data-ttu-id="620be-246">Текущие функции **D3DCompile \*** шейдера HLSL не поддерживают устаревшие шейдеры 1. x пикселей.</span><span class="sxs-lookup"><span data-stu-id="620be-246">The current HLSL shader **D3DCompile\*** functions don't support legacy 1.x pixel shaders.</span></span> <span data-ttu-id="620be-247">Последняя версия HLSL для поддержки этих целей была D3DX9а в выпуске DirectX SDK, выпущенной в октябре 2006.</span><span class="sxs-lookup"><span data-stu-id="620be-247">The last version of HLSL to support these targets was D3DX9 in the October 2006 release of the DirectX SDK.</span></span>
5.  <span data-ttu-id="620be-248">Все версии D3DX и DirectX SDK являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="620be-248">All versions of D3DX and the DirectX SDK are deprecated.</span></span> <span data-ttu-id="620be-249">Дополнительные сведения см. [в разделе где находится пакет DirectX SDK?](/windows/desktop/directx-sdk--august-2009-).</span><span class="sxs-lookup"><span data-stu-id="620be-249">For more info, see [Where is the DirectX SDK?](/windows/desktop/directx-sdk--august-2009-).</span></span>

## <a name="related-topics"></a><span data-ttu-id="620be-250">См. также</span><span class="sxs-lookup"><span data-stu-id="620be-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="620be-251">Руководство по программированию для HLSL</span><span class="sxs-lookup"><span data-stu-id="620be-251">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 