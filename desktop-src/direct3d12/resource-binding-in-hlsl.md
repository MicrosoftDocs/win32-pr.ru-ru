---
title: Привязка ресурсов в HLSL
description: В этом разделе описываются некоторые особенности использования модели шейдера высокого уровня Shader (HLSL) 5,1 с Direct3D 12.
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 01039550f07de57fb7b2f1e815bced02e549c741
ms.sourcegitcommit: 60120d10c957815d79af566c72e5f4bcfaca4025
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2021
ms.locfileid: "104837492"
---
# <a name="resource-binding-in-hlsl"></a><span data-ttu-id="33b1b-103">Привязка ресурсов в HLSL</span><span class="sxs-lookup"><span data-stu-id="33b1b-103">Resource binding in HLSL</span></span>

<span data-ttu-id="33b1b-104">В этом разделе описываются некоторые особенности использования [модели шейдера](/windows/desktop/direct3dhlsl/shader-model-5-1) высокого уровня Shader (HLSL) 5,1 с Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="33b1b-104">This topic describes some specific features of using High Level Shader Language (HLSL) [Shader Model 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) with Direct3D 12.</span></span> <span data-ttu-id="33b1b-105">Все оборудование Direct3D 12 поддерживает модель шейдера 5,1, поэтому поддержка этой модели не зависит от уровня компонентов оборудования.</span><span class="sxs-lookup"><span data-stu-id="33b1b-105">All Direct3D 12 hardware supports Shader Model 5.1, so support for this model does not depend on what the hardware feature level is.</span></span>

## <a name="resource-types-and-arrays"></a><span data-ttu-id="33b1b-106">Типы ресурсов и массивы</span><span class="sxs-lookup"><span data-stu-id="33b1b-106">Resource types and arrays</span></span>

<span data-ttu-id="33b1b-107">Синтаксис ресурсов Shader Model 5 (SM 5.0) использует `register` ключевое слово для ретрансляции важной информации о ресурсе в КОМПИЛЯТОР HLSL.</span><span class="sxs-lookup"><span data-stu-id="33b1b-107">Shader Model 5 (SM5.0) resource syntax uses the `register` keyword to relay important information about the resource to the HLSL compiler.</span></span> <span data-ttu-id="33b1b-108">Например, следующая инструкция объявляет массив из четырех текстур, привязанных к разъемам T3, T4, T5 и T6.</span><span class="sxs-lookup"><span data-stu-id="33b1b-108">For example, the following statement declares an array of four textures bound at slots t3, t4, t5, and t6.</span></span> <span data-ttu-id="33b1b-109">T3 — единственный слот регистров, отображаемый в операторе, просто первый в массиве из четырех.</span><span class="sxs-lookup"><span data-stu-id="33b1b-109">t3 is the only register slot appearing in the statement, simply being the first in the array of four.</span></span>

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

<span data-ttu-id="33b1b-110">Синтаксис ресурсов в модели шейдеров 5,1 (SM 5.1) в HLSL основан на существующем синтаксисе ресурсов регистров, что позволяет упростить перенос.</span><span class="sxs-lookup"><span data-stu-id="33b1b-110">Shader Model 5.1 (SM5.1) resource syntax in HLSL is based on existing register resource syntax, to allow easier porting.</span></span> <span data-ttu-id="33b1b-111">Ресурсы Direct3D 12 в HLSL привязаны к виртуальным регистрам в логических пространствах регистров:</span><span class="sxs-lookup"><span data-stu-id="33b1b-111">Direct3D 12 resources in HLSL are bound to virtual registers within logical register spaces:</span></span>

-   <span data-ttu-id="33b1b-112">t — для представлений ресурсов шейдера (SRV)</span><span class="sxs-lookup"><span data-stu-id="33b1b-112">t – for shader resource views (SRV)</span></span>
-   <span data-ttu-id="33b1b-113">s — для проб</span><span class="sxs-lookup"><span data-stu-id="33b1b-113">s – for samplers</span></span>
-   <span data-ttu-id="33b1b-114">u — для неупорядоченных представлений доступа (UAV)</span><span class="sxs-lookup"><span data-stu-id="33b1b-114">u – for unordered access views (UAV)</span></span>
-   <span data-ttu-id="33b1b-115">b — для представлений буфера констант (CBV)</span><span class="sxs-lookup"><span data-stu-id="33b1b-115">b – for constant buffer views (CBV)</span></span>

<span data-ttu-id="33b1b-116">Корневая подпись, ссылающаяся на шейдер, должна быть совместима с объявленными слотами регистров.</span><span class="sxs-lookup"><span data-stu-id="33b1b-116">The root signature referencing the shader must be compatible with the declared register slots.</span></span> <span data-ttu-id="33b1b-117">Например, следующая часть корневой сигнатуры будет совместима с использованием слотов текстур с T3 до T6, так как в нем описывается таблица дескрипторов с слотами, t0 через T98.</span><span class="sxs-lookup"><span data-stu-id="33b1b-117">For example, the following portion of a root signature would be compatible with the use of texture slots t3 through t6, as it describes a descriptor table with slots t0 through t98.</span></span>

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

<span data-ttu-id="33b1b-118">Объявление ресурса может быть скалярным, массивом 1D или многомерным массивом.</span><span class="sxs-lookup"><span data-stu-id="33b1b-118">A resource declaration may be a scalar, a 1D array, or a multidimensional array:</span></span>

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

<span data-ttu-id="33b1b-119">В SM 5.1 используются те же типы ресурсов и типы элементов, что и в SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="33b1b-119">SM5.1 uses the same resource types and element types as SM5.0 does.</span></span> <span data-ttu-id="33b1b-120">Ограничения объявления SM 5.1 более гибкие и ограничены только ограничениями среды выполнения и оборудования.</span><span class="sxs-lookup"><span data-stu-id="33b1b-120">SM5.1 declaration limits are more flexible, and constrained only by the runtime/hardware limits.</span></span> <span data-ttu-id="33b1b-121">`space`Ключевое слово указывает, к какому пространству логических регистров привязана объявленная переменная.</span><span class="sxs-lookup"><span data-stu-id="33b1b-121">The `space` keyword specifies to which logical register space the declared variable is bound.</span></span> <span data-ttu-id="33b1b-122">Если `space` ключевое слово опущено, то индекс пространства по умолчанию, равный 0, неявно присваивается диапазону (так что `tex2` диапазон выше находится в `space0` ).</span><span class="sxs-lookup"><span data-stu-id="33b1b-122">If the `space` keyword is omitted, then the default space index of 0 is implicitly assigned to the range (so the `tex2` range above resides in `space0`).</span></span> <span data-ttu-id="33b1b-123">`register(t3,  space0)` никогда не будет конфликтовать с `register(t3,  space1)` или с любым массивом в другом пространстве, который может включать T3.</span><span class="sxs-lookup"><span data-stu-id="33b1b-123">`register(t3,  space0)` will never conflict with `register(t3,  space1)`, nor with any array in another space that might include t3.</span></span>

<span data-ttu-id="33b1b-124">Ресурс массива может иметь неограниченный размер, который объявляется с помощью указания первого измерения, который должен быть пустым, или 0:</span><span class="sxs-lookup"><span data-stu-id="33b1b-124">An array resource may have an unbounded size, which is declared by specifying the very first dimension to be empty, or 0:</span></span>

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

<span data-ttu-id="33b1b-125">Соответствующая таблица дескрипторов может быть:</span><span class="sxs-lookup"><span data-stu-id="33b1b-125">The matching descriptor table could be:</span></span>

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

<span data-ttu-id="33b1b-126">Неограниченный массив в HLSL соответствует фиксированному числу, заданному `numDescriptors` в таблице дескрипторов, и фиксированный размер в HLSL соответствует неограниченному объявлению в таблице дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="33b1b-126">An unbounded array in HLSL does match a fixed number set with `numDescriptors` in the descriptor table, and a fixed size in the HLSL does match an unbounded declaration in the descriptor table.</span></span>

<span data-ttu-id="33b1b-127">Многомерные массивы допускаются, включая неограниченный размер.</span><span class="sxs-lookup"><span data-stu-id="33b1b-127">Multi-dimensional arrays are allowed, including of an unbounded size.</span></span> <span data-ttu-id="33b1b-128">Эти многомерные массивы выравниваются из пространства регистров.</span><span class="sxs-lookup"><span data-stu-id="33b1b-128">These multidimensional arrays are flattened out in register space.</span></span>

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

<span data-ttu-id="33b1b-129">Использование псевдонимов диапазонов ресурсов не допускается.</span><span class="sxs-lookup"><span data-stu-id="33b1b-129">Aliasing of resource ranges is not allowed.</span></span> <span data-ttu-id="33b1b-130">Иными словами, для каждого типа ресурса (t, s, u, b) объявленные диапазоны регистров не должны перекрываются.</span><span class="sxs-lookup"><span data-stu-id="33b1b-130">In other words, for each resource type (t, s, u, b), declared register ranges mustn't overlap.</span></span> <span data-ttu-id="33b1b-131">Это также относится и к неограниченным диапазонам.</span><span class="sxs-lookup"><span data-stu-id="33b1b-131">That includes unbounded ranges, too.</span></span> <span data-ttu-id="33b1b-132">Диапазоны, объявленные в разных пространствах регистра, никогда не перекрываются.</span><span class="sxs-lookup"><span data-stu-id="33b1b-132">Ranges declared in different register spaces never overlap.</span></span> <span data-ttu-id="33b1b-133">Обратите внимание, что неограниченное `tex2` (выше) размещается в `space0` , а непривязанных `tex3` — в `space1` , так что они не перекрываются.</span><span class="sxs-lookup"><span data-stu-id="33b1b-133">Note that unbounded `tex2` (above) resides in `space0`, while unbounded `tex3` resides in `space1`, such that they don't overlap.</span></span>

<span data-ttu-id="33b1b-134">Для доступа к ресурсам, объявленным как массивы, достаточно просто индексировать их.</span><span class="sxs-lookup"><span data-stu-id="33b1b-134">Accessing resources that have been declared as arrays is as simple as indexing them.</span></span>

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

<span data-ttu-id="33b1b-135">Существует важное ограничение по умолчанию для использования индексов ( `myMaterialID` и `samplerID` в приведенном выше коде) тем, что они не могут быть разными в [волне](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span><span class="sxs-lookup"><span data-stu-id="33b1b-135">There's an important default restriction on the use of the indices (`myMaterialID` and `samplerID` in the code above) in that they're not allowed to vary within a [wave](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span></span> <span data-ttu-id="33b1b-136">Даже изменение индекса на основе количества экземпляров.</span><span class="sxs-lookup"><span data-stu-id="33b1b-136">Even changing the index based on instancing counts as varying.</span></span>

<span data-ttu-id="33b1b-137">Если требуется изменение индекса, укажите в `NonUniformResourceIndex` индексе квалификатор, например:</span><span class="sxs-lookup"><span data-stu-id="33b1b-137">If varying the index is required then specify the `NonUniformResourceIndex` qualifier on the index, for example:</span></span>

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

<span data-ttu-id="33b1b-138">На некоторых устройствах использование этого квалификатора создает дополнительный код для обеспечения правильности (включая потоки), но при незначительной стоимости производительности.</span><span class="sxs-lookup"><span data-stu-id="33b1b-138">On some hardware the use of this qualifier generates additional code to enforce correctness (including across threads) but at a minor performance cost.</span></span> <span data-ttu-id="33b1b-139">Если индекс изменяется без квалификатора и в процессе рисования/отправки результаты не определены.</span><span class="sxs-lookup"><span data-stu-id="33b1b-139">If an index is changed without this qualifier and within a draw/dispatch the results are undefined.</span></span>

## <a name="descriptor-arrays-and-texture-arrays"></a><span data-ttu-id="33b1b-140">Массивы дескрипторов и массивы текстур</span><span class="sxs-lookup"><span data-stu-id="33b1b-140">Descriptor arrays and texture arrays</span></span>

<span data-ttu-id="33b1b-141">С момента выпуска DirectX 10 были доступны массивы текстур.</span><span class="sxs-lookup"><span data-stu-id="33b1b-141">Texture arrays have been available since DirectX 10.</span></span> <span data-ttu-id="33b1b-142">Для массивов текстуры требуется один дескриптор, однако все срезы массива должны иметь одинаковый формат, ширину, высоту и число MIP.</span><span class="sxs-lookup"><span data-stu-id="33b1b-142">Texture arrays require one descriptor, however all the array slices must share the same format, width, height and mip count.</span></span> <span data-ttu-id="33b1b-143">Кроме того, массив должен занимать непрерывный диапазон в виртуальном адресном пространстве.</span><span class="sxs-lookup"><span data-stu-id="33b1b-143">Also, the array must occupy a contiguous range in virtual address space.</span></span> <span data-ttu-id="33b1b-144">В следующем коде показан пример доступа к массиву текстуры из шейдера.</span><span class="sxs-lookup"><span data-stu-id="33b1b-144">The following code shows an example of accessing a texture array from a shader.</span></span>

``` syntax
Texture2DArray<float4> myTex2DArray : register(t0); // t0
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

<span data-ttu-id="33b1b-145">В массиве текстур индекс может свободно изменяться без каких-либо необходимых квалификаторов, таких как `NonUniformResourceIndex` .</span><span class="sxs-lookup"><span data-stu-id="33b1b-145">In a texture array, the index can be varied freely, without any need for qualifiers such as `NonUniformResourceIndex`.</span></span>

<span data-ttu-id="33b1b-146">Эквивалентный массив дескрипторов будет следующим:</span><span class="sxs-lookup"><span data-stu-id="33b1b-146">The equivalent descriptor array would be:</span></span>

``` syntax
Texture2D<float4> myArrayOfTex2D[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myArrayOfTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

<span data-ttu-id="33b1b-147">Обратите внимание, что неудобное использование float для индекса массива заменяется на `myArrayOfTex2D[2]` .</span><span class="sxs-lookup"><span data-stu-id="33b1b-147">Note the awkward use of a float for the array index is replaced with `myArrayOfTex2D[2]`.</span></span> <span data-ttu-id="33b1b-148">Кроме того, массивы дескрипторов обеспечивают большую гибкость при использовании измерений.</span><span class="sxs-lookup"><span data-stu-id="33b1b-148">Also descriptor arrays offer more flexibility with the dimensions.</span></span> <span data-ttu-id="33b1b-149">Тип `Texture2D` — это пример, который не может быть разным, но формат, ширина, высота и число MIP могут различаться в зависимости от каждого дескриптора.</span><span class="sxs-lookup"><span data-stu-id="33b1b-149">The type, `Texture2D` is this example, cannot vary, but the format, width, height, and mip count can all vary with each descriptor.</span></span>

<span data-ttu-id="33b1b-150">В качестве дескриптора можно использовать массив массивов текстур:</span><span class="sxs-lookup"><span data-stu-id="33b1b-150">It is legitimate to have a descriptor array of texture arrays:</span></span>

``` syntax
Texture2DArray<float4> myArrayOfTex2DArrays[2] : register(t0);
```

<span data-ttu-id="33b1b-151">Незаконно объявлять массив структур, каждая структура, содержащая дескрипторы, например следующий код, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="33b1b-151">It is not legitimate to declare an array of structures, each structure containing descriptors, for example the following code is not supported.</span></span>

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

<span data-ttu-id="33b1b-152">Это позволило бы abcabcabc макет памяти **....**, но является ограничением языка и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="33b1b-152">This would have allowed the memory layout **abcabcabc....**, but is a language limitation and is not supported.</span></span> <span data-ttu-id="33b1b-153">Ниже приведен один из поддерживаемых методов выполнения этой операции, хотя в этом случае в качестве структуры памяти используется **AAA... BBB... CCC**....</span><span class="sxs-lookup"><span data-stu-id="33b1b-153">One supported method of doing this would be as follows, though the memory layout in this case is **aaa...bbb...ccc...**.</span></span>

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

<span data-ttu-id="33b1b-154">Чтобы получить макет памяти **abcabcabc....** , используйте таблицу дескрипторов без использования `myStruct` структуры.</span><span class="sxs-lookup"><span data-stu-id="33b1b-154">To achieve the **abcabcabc....** memory layout, use a descriptor table without use of the `myStruct` structure.</span></span>

## <a name="resource-aliasing"></a><span data-ttu-id="33b1b-155">Присвоение псевдонимов ресурсам</span><span class="sxs-lookup"><span data-stu-id="33b1b-155">Resource aliasing</span></span>

<span data-ttu-id="33b1b-156">Диапазоны ресурсов, указанные в шейдерах HLSL, являются логическими диапазонами.</span><span class="sxs-lookup"><span data-stu-id="33b1b-156">The resource ranges specified in the HLSL shaders are logical ranges.</span></span> <span data-ttu-id="33b1b-157">Они привязаны к конкретным диапазонам кучи во время выполнения через механизм корневой подписи.</span><span class="sxs-lookup"><span data-stu-id="33b1b-157">They are be bound to concrete heap ranges at runtime via the root signature mechanism.</span></span> <span data-ttu-id="33b1b-158">Как правило, логический диапазон сопоставляется с диапазоном кучи, который не перекрывается с другими диапазонами кучи.</span><span class="sxs-lookup"><span data-stu-id="33b1b-158">Normally, a logical range maps to a heap range that does not overlap with other heap ranges.</span></span> <span data-ttu-id="33b1b-159">Однако механизм корневой подписи делает возможным псевдонимы диапазонов кучи совместимых типов.</span><span class="sxs-lookup"><span data-stu-id="33b1b-159">However, the root signature mechanism makes it possible to alias (overlap) heap ranges of compatible types.</span></span> <span data-ttu-id="33b1b-160">Например, `tex2` и `tex3` диапазоны из приведенного выше примера могут быть сопоставлены с одним (или перекрывающим) диапазоном кучи, в котором действует псевдоним текстур в программе HLSL.</span><span class="sxs-lookup"><span data-stu-id="33b1b-160">For example, `tex2` and `tex3` ranges from the above example may be mapped to the same (or overlapping) heap range, which has the effect of aliasing textures in the HLSL program.</span></span> <span data-ttu-id="33b1b-161">Если требуется такое присвоение псевдонимов, шейдер должен быть скомпилирован с использованием \_ ресурсов шейдера \_ D3D10 \_ \_ , которые задаются с помощью параметра */RES может быть \_ \_ псевдонимом* для [средства компилятора Effect](/windows/win32/direct3dtools/fxc) (FXC).</span><span class="sxs-lookup"><span data-stu-id="33b1b-161">If such aliasing is desired, the shader must be compiled with D3D10\_SHADER\_RESOURCES\_MAY\_ALIAS option, which is set by using the */res\_may\_alias* option for the [Effect-Compiler Tool](/windows/win32/direct3dtools/fxc) (FXC).</span></span> <span data-ttu-id="33b1b-162">Параметр позволяет компилятору создавать правильный код, предотвращая определенные оптимизации нагрузки и хранения в соответствии с предположением, что ресурсы могут быть псевдонимами.</span><span class="sxs-lookup"><span data-stu-id="33b1b-162">The option makes the compiler produce correct code by preventing certain load/store optimizations under the assumption that resources may alias.</span></span>

## <a name="divergence-and-derivatives"></a><span data-ttu-id="33b1b-163">Расхождение и производные</span><span class="sxs-lookup"><span data-stu-id="33b1b-163">Divergence and derivatives</span></span>

<span data-ttu-id="33b1b-164">SM 5.1 не накладывает ограничений на индекс ресурсов; т. е. ` tex2[idx].Sample(…)` индекс idx может быть литеральной константой, константой кбуффер или интерполяцией значения.</span><span class="sxs-lookup"><span data-stu-id="33b1b-164">SM5.1 does not impose limitations on the resource index; i.e.,` tex2[idx].Sample(…)` – the index idx can be a literal constant, a cbuffer constant, or an interpolated value.</span></span> <span data-ttu-id="33b1b-165">Хотя модель программирования обеспечивает такую высокую гибкость, существуют проблемы, которые следует учитывать:</span><span class="sxs-lookup"><span data-stu-id="33b1b-165">While the programming model provides such great flexibility, there are issues to be aware of:</span></span>

-   <span data-ttu-id="33b1b-166">Если индекс рассходится по четырем, то вычисленное оборудованием производные и производные количества, например Лод, могут быть неопределенными.</span><span class="sxs-lookup"><span data-stu-id="33b1b-166">If index diverges across a quad, the hardware-computed derivative and derived quantities such as LOD may be undefined.</span></span> <span data-ttu-id="33b1b-167">Компилятор HLSL делает лучшие усилия для выдачи предупреждения в этом случае, но не помешает компиляции шейдера.</span><span class="sxs-lookup"><span data-stu-id="33b1b-167">The HLSL compiler makes the best effort to issue a warning in this case, but will not prevent a shader from compiling.</span></span> <span data-ttu-id="33b1b-168">Такое поведение аналогично вычислению производных элементов в последовательном потоке управления.</span><span class="sxs-lookup"><span data-stu-id="33b1b-168">This behavior is similar to computing derivatives in divergent control flow.</span></span>
-   <span data-ttu-id="33b1b-169">Если индекс ресурсов отличается, производительность уменьшается по сравнению с вариантом универсального индекса, так как оборудование должно выполнять операции с несколькими ресурсами.</span><span class="sxs-lookup"><span data-stu-id="33b1b-169">If the resource index is divergent, the performance is diminished compared to the case of a uniform index, because the hardware needs to perform operations on several resources.</span></span> <span data-ttu-id="33b1b-170">Индексы ресурсов, которые могут быть иными, должны быть помечены `NonUniformResourceIndex` функцией в коде HLSL.</span><span class="sxs-lookup"><span data-stu-id="33b1b-170">Resource indexes that may be divergent must be marked with the `NonUniformResourceIndex` function in HLSL code.</span></span> <span data-ttu-id="33b1b-171">В противном случае результаты не определены.</span><span class="sxs-lookup"><span data-stu-id="33b1b-171">Otherwise results are undefined.</span></span>

## <a name="uavs-in-pixel-shaders"></a><span data-ttu-id="33b1b-172">Уавс в шейдере пикселей</span><span class="sxs-lookup"><span data-stu-id="33b1b-172">UAVs in pixel shaders</span></span>

<span data-ttu-id="33b1b-173">SM 5.1 не накладывает ограничений на диапазоны UAV в шейдерах пикселей, как это было в случае SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="33b1b-173">SM5.1 does not impose constraints on UAV ranges in pixel shaders as was the case for SM5.0.</span></span>

## <a name="constant-buffers"></a><span data-ttu-id="33b1b-174">Буферы констант</span><span class="sxs-lookup"><span data-stu-id="33b1b-174">Constant Buffers</span></span>

<span data-ttu-id="33b1b-175">Синтаксис для константных буферов SM 5.1 (кбуффер) изменился с SM 5.0, чтобы позволить разработчикам индексировать буферы констант.</span><span class="sxs-lookup"><span data-stu-id="33b1b-175">SM5.1 constant buffers (cbuffer) syntax has changed from SM5.0 to enable developers to index constant buffers.</span></span> <span data-ttu-id="33b1b-176">Чтобы включить индексируемые буферы констант, SM 5.1 вводит `ConstantBuffer` конструкцию "Template":</span><span class="sxs-lookup"><span data-stu-id="33b1b-176">To enable indexable constant buffers, SM5.1 introduces the `ConstantBuffer` “template” construct:</span></span>

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

<span data-ttu-id="33b1b-177">Приведенный выше код объявляет переменную буфера константы `myCB1` типа `Foo` и размера 6, а также скалярную переменную буфера `myCB2` .</span><span class="sxs-lookup"><span data-stu-id="33b1b-177">The preceding code declares constant buffer variable `myCB1` of type `Foo` and size 6, and a scalar, constant buffer variable `myCB2`.</span></span> <span data-ttu-id="33b1b-178">Переменная буфера константы теперь может индексироваться в шейдере следующим образом:</span><span class="sxs-lookup"><span data-stu-id="33b1b-178">A constant buffer variable can now be indexed in the shader as:</span></span>

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

<span data-ttu-id="33b1b-179">Поля "a" и "b" не становятся глобальными переменными, а должны рассматриваться как поля.</span><span class="sxs-lookup"><span data-stu-id="33b1b-179">Fields ‘a’ and ‘b’ do not become global variables, but rather must be treated as fields.</span></span> <span data-ttu-id="33b1b-180">Для обеспечения обратной совместимости SM 5.1 поддерживает старую концепцию кбуффер для скалярного cbuffer.</span><span class="sxs-lookup"><span data-stu-id="33b1b-180">For backward compatibility, SM5.1 supports the old cbuffer concept for scalar cbuffers.</span></span> <span data-ttu-id="33b1b-181">Следующая инструкция делает глобальные переменные «a» и «b» только для чтения, как в SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="33b1b-181">The following statement makes ‘a’ and ‘b’ global, read-only variables as in SM5.0.</span></span> <span data-ttu-id="33b1b-182">Однако такие кбуффер не могут индексироваться.</span><span class="sxs-lookup"><span data-stu-id="33b1b-182">However, such an old-style cbuffer cannot be indexable.</span></span>

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

<span data-ttu-id="33b1b-183">В настоящее время компилятор шейдеров поддерживает `ConstantBuffer` шаблон только для определяемых пользователем структур.</span><span class="sxs-lookup"><span data-stu-id="33b1b-183">Currently, the shader compiler supports the `ConstantBuffer` template for user-defined structures only.</span></span>

<span data-ttu-id="33b1b-184">В целях совместимости компилятор HLSL может автоматически назначать регистры ресурсов для диапазонов, объявленных в `space0` .</span><span class="sxs-lookup"><span data-stu-id="33b1b-184">For compatibility reasons, the HLSL compiler may automatically assign resource registers for ranges declared in `space0`.</span></span> <span data-ttu-id="33b1b-185">Если в предложении Register не указан пробел, используется значение по умолчанию `space0` .</span><span class="sxs-lookup"><span data-stu-id="33b1b-185">If ‘space’ is omitted in the register clause, the default `space0` is used.</span></span> <span data-ttu-id="33b1b-186">Для назначения регистров компилятор использует эвристический метод "первый-дыра".</span><span class="sxs-lookup"><span data-stu-id="33b1b-186">The compiler uses the first-hole-fits heuristic to assign the registers.</span></span> <span data-ttu-id="33b1b-187">Назначение можно получить с помощью API отражения, который был расширен для добавления поля *пробела* , а поле *биндпоинт* — нижнюю границу диапазона регистров ресурсов.</span><span class="sxs-lookup"><span data-stu-id="33b1b-187">The assignment can be retrieved via the reflection API, which has been extended to add the *Space* field for space, while the *BindPoint* field indicates the lower bound of the resource register range.</span></span>

## <a name="bytecode-changes-in-sm51"></a><span data-ttu-id="33b1b-188">Изменения байтового кода в SM 5.1</span><span class="sxs-lookup"><span data-stu-id="33b1b-188">Bytecode changes in SM5.1</span></span>

<span data-ttu-id="33b1b-189">SM 5.1 изменяет объявление регистров ресурсов и ссылки в инструкциях.</span><span class="sxs-lookup"><span data-stu-id="33b1b-189">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span> <span data-ttu-id="33b1b-190">Синтаксис включает объявление переменной Register, аналогично тому, как это делается для групповых регистров общей памяти:</span><span class="sxs-lookup"><span data-stu-id="33b1b-190">The syntax involves declaring a register “variable”, similar to how it is done for group shared memory registers:</span></span>

``` syntax
Texture2D<float4> tex0          : register(t5,  space0);
Texture2D<float4> tex1[][5][3]  : register(t10, space0);
Texture2D<float4> tex2[8]       : register(t0,  space1);
SamplerState samp0              : register(s5, space0);

float4 main(float4 coord : COORD) : SV_TARGET
{
    float4 r = coord;
    r += tex0.Sample(samp0, r.xy);
    r += tex2[r.x].Sample(samp0, r.xy);
    r += tex1[r.x][r.y][r.z].Sample(samp0, r.xy);
    return r;
}
```

<span data-ttu-id="33b1b-191">Будет разбираться в:</span><span class="sxs-lookup"><span data-stu-id="33b1b-191">This will disassemble to:</span></span>

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim    ID   HLSL Bind     Count
// ------------------------------ ---------- ------- ----------- -----   --------- ---------
// samp0                             sampler      NA          NA     S0    a5            1
// tex0                              texture  float4          2d     T0    t5            1
// tex1[0][5][3]                     texture  float4          2d     T1   t10        unbounded
// tex2[8]                           texture  float4          2d     T2    t0.space1     8
//
//
//
// Input signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// COORD                    0   xyzw        0     NONE   float   xyzw
//
//
// Output signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// SV_TARGET                0   xyzw        0   TARGET   float   xyzw
//
ps_5_1
dcl_globalFlags refactoringAllowed
dcl_sampler s0[5:5], mode_default, space=0
dcl_resource_texture2d (float,float,float,float) t0[5:5], space=0
dcl_resource_texture2d (float,float,float,float) t1[10:*], space=0
dcl_resource_texture2d (float,float,float,float) t2[0:7], space=1
dcl_input_ps linear v0.xyzw
dcl_output o0.xyzw
dcl_temps 2
sample r0.xyzw, v0.xyxx, t0[0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, v0.xyzw
ftou r1.x, r0.x
sample r1.xyzw, r0.xyxx, t2[r1.x + 0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, r1.xyzw
ftou r1.xyz, r0.zyxz
imul null, r1.yz, r1.zzyz, l(0, 15, 3, 0)
iadd r1.y, r1.z, r1.y
iadd r1.x, r1.x, r1.y
sample r1.xyzw, r0.xyxx, t1[r1.x + 10].xyzw, s0[5]
add o0.xyzw, r0.xyzw, r1.xyzw
ret
// Approximately 12 instruction slots are used.
```

<span data-ttu-id="33b1b-192">Каждый диапазон ресурсов шейдера теперь имеет идентификатор (имя), уникальный для байт-кода шейдера.</span><span class="sxs-lookup"><span data-stu-id="33b1b-192">Each shader resource range now has an ID (a name) that is unique to the shader bytecode.</span></span> <span data-ttu-id="33b1b-193">Например, массив текстуры Tex1 (T10) превращается в "1" в байт-код шейдера.</span><span class="sxs-lookup"><span data-stu-id="33b1b-193">For example, tex1 (t10) texture array becomes ‘T1’ in the shader bytecode.</span></span> <span data-ttu-id="33b1b-194">Присвоение уникальных идентификаторов каждому диапазону ресурсов позволяет выполнить два действия:</span><span class="sxs-lookup"><span data-stu-id="33b1b-194">Giving unique IDs to each resource range allows two things:</span></span>

-   <span data-ttu-id="33b1b-195">Однозначно определяет, какой диапазон ресурсов (см. дкл \_ Resource \_ Texture2D) индексируется в инструкции (см. пример инструкции).</span><span class="sxs-lookup"><span data-stu-id="33b1b-195">Unambiguously identify which resource range (see dcl\_resource\_texture2d) is being indexed in an instruction (see sample instruction).</span></span>
-   <span data-ttu-id="33b1b-196">Присоединение набора атрибутов к объявлению, например, тип элемента, размер шага, режим растровой операции и т. д.</span><span class="sxs-lookup"><span data-stu-id="33b1b-196">Attaching a set of attributes to the declaration, e.g., element type, stride size, raster operation mode, etc.</span></span>

<span data-ttu-id="33b1b-197">Обратите внимание, что идентификатор диапазона не связан с объявлением HLSL нижней границы.</span><span class="sxs-lookup"><span data-stu-id="33b1b-197">Note that the ID of the range is not related to the HLSL lower bound declaration.</span></span>

<span data-ttu-id="33b1b-198">Порядок привязок ресурсов отражения (сверху) и инструкций объявлений шейдера (дкл \_ \* ) аналогичен, чтобы помочь в определении соответствия между переменными HLSL и идентификаторами байт-кода.</span><span class="sxs-lookup"><span data-stu-id="33b1b-198">The order of reflection resource bindings (listing at the top) and shader declaration instructions (dcl\_\*) is the same to aid in identifying the correspondence between HLSL variables and bytecode IDs.</span></span>

<span data-ttu-id="33b1b-199">Каждая инструкция объявления в SM 5.1 использует трехмерный операнд для определения: идентификатор диапазона, Нижняя и верхняя границы.</span><span class="sxs-lookup"><span data-stu-id="33b1b-199">Each declaration instruction in SM5.1 uses a 3D operand to define: range ID, lower and upper bounds.</span></span> <span data-ttu-id="33b1b-200">Для указания пространства регистра создается дополнительный токен.</span><span class="sxs-lookup"><span data-stu-id="33b1b-200">An additional token is emitted to specify the register space.</span></span> <span data-ttu-id="33b1b-201">Также могут выдаваться другие токены для передачи дополнительных свойств диапазона, например кбуффер или инструкция объявления буфера, выдает размер кбуффер или структуры.</span><span class="sxs-lookup"><span data-stu-id="33b1b-201">Other tokens may be emitted as well to convey additional properties of the range, e.g., cbuffer or structured buffer declaration instruction emits the size of the cbuffer or structure.</span></span> <span data-ttu-id="33b1b-202">Точные сведения о кодировке можно найти в d3d12TokenizedProgramFormat. h и **D3D10ShaderBinary:: кшадеркодепарсер**.</span><span class="sxs-lookup"><span data-stu-id="33b1b-202">The exact details of encoding can be found in d3d12TokenizedProgramFormat.h and **D3D10ShaderBinary::CShaderCodeParser**.</span></span>

<span data-ttu-id="33b1b-203">Инструкции SM 5.1 не будут выдавать дополнительные сведения о операндах ресурсов в рамках инструкции (как в SM 5.0).</span><span class="sxs-lookup"><span data-stu-id="33b1b-203">SM5.1 instructions will not emit additional resource operand information as part of the instruction (as in SM5.0).</span></span> <span data-ttu-id="33b1b-204">Эти сведения теперь приведены в инструкциях по объявлению.</span><span class="sxs-lookup"><span data-stu-id="33b1b-204">This information is now in the declaration instructions.</span></span> <span data-ttu-id="33b1b-205">В SM 5.0 приведены инструкции по индексированию ресурсов, необходимых атрибутам ресурсов, которые должны быть описаны в маркерах расширенного кода операции, поскольку индексирование замаскировано к объявлению.</span><span class="sxs-lookup"><span data-stu-id="33b1b-205">In SM5.0, instructions indexing resources required resource attributes to be described in extended opcode tokens, since indexing obfuscated the association to the declaration.</span></span> <span data-ttu-id="33b1b-206">В SM 5.1 Каждый идентификатор (например, "'t 1") однозначно связан с одним объявлением, описывающим необходимые сведения о ресурсах.</span><span class="sxs-lookup"><span data-stu-id="33b1b-206">In SM5.1, each ID (such as ‘t1’) is unambiguously associated with a single declaration that describes the required resource information.</span></span> <span data-ttu-id="33b1b-207">Поэтому маркеры расширенного кода операций, используемые в инструкциях для описания сведений о ресурсах, больше не создаются.</span><span class="sxs-lookup"><span data-stu-id="33b1b-207">Therefore, the extended opcode tokens used on instructions to describe resource information are no longer emitted.</span></span>

<span data-ttu-id="33b1b-208">В инструкциях без объявления операнд ресурса для образцов, СРВС и Уавс является 2D-операндом.</span><span class="sxs-lookup"><span data-stu-id="33b1b-208">In non-declaration instructions, a resource operand for samplers, SRVs, and UAVs is a 2D operand.</span></span> <span data-ttu-id="33b1b-209">Первый индекс представляет собой литеральную константу, указывающую идентификатор диапазона.</span><span class="sxs-lookup"><span data-stu-id="33b1b-209">The first index is a literal constant that specifies the range ID.</span></span> <span data-ttu-id="33b1b-210">Второй индекс представляет линейное значение индекса.</span><span class="sxs-lookup"><span data-stu-id="33b1b-210">The second index represents the linearized value of the index.</span></span> <span data-ttu-id="33b1b-211">Значение высчитывается относительно начала соответствующего пространства регистра (не относительно начала логического диапазона) для лучшего сопоставления с корневой подписью и для уменьшения количества погрузок компилятора драйвера на настройку индекса.</span><span class="sxs-lookup"><span data-stu-id="33b1b-211">The value is computed relative to the beginning of the corresponding register space (not relative to the beginning of the logical range) to better correlate with the root signature and to reduce the driver compiler burden of adjusting the index.</span></span>

<span data-ttu-id="33b1b-212">Операнд ресурса для КБВС является трехмерным операндом, содержащим: литеральный идентификатор диапазона, индекс буфера константы и смещение в определенном экземпляре буфера констант.</span><span class="sxs-lookup"><span data-stu-id="33b1b-212">A resource operand for CBVs is a 3D operand, containing: literal ID of the range, index of the constant buffer, offset into the particular instance of constant buffer.</span></span>

## <a name="example-hlsl-declarations"></a><span data-ttu-id="33b1b-213">Примеры объявлений HLSL</span><span class="sxs-lookup"><span data-stu-id="33b1b-213">Example HLSL Declarations</span></span>

<span data-ttu-id="33b1b-214">Программам HLSL не нужно ничего знать о корневых сигнатурах.</span><span class="sxs-lookup"><span data-stu-id="33b1b-214">HLSL programs do not need to know anything about root signatures.</span></span> <span data-ttu-id="33b1b-215">Они могут назначать привязки к виртуальному пространству привязки "Register", t \# для СРВС, u \# для уавс, b \# для КБВС, s для \# проб или использовать компилятор для выбора назначений (и запрашивать полученные сопоставления с помощью отражения шейдера).</span><span class="sxs-lookup"><span data-stu-id="33b1b-215">They can assign bindings to the virtual “register” binding space, t\# for SRVs, u\# for UAVs, b\# for CBVs, s\# for samplers, or rely on the compiler to pick assignments (and query the resulting mappings using shader reflection afterwards).</span></span> <span data-ttu-id="33b1b-216">Корневой узел подписи сопоставляет таблицы дескрипторов, корневые дескрипторы и корневые константы с этим виртуальным пространством регистра.</span><span class="sxs-lookup"><span data-stu-id="33b1b-216">The root signature maps descriptor tables, root descriptors, and root constants to this virtual register space.</span></span>

<span data-ttu-id="33b1b-217">Ниже приведены примеры объявлений, которые может иметь Шейдер HLSL.</span><span class="sxs-lookup"><span data-stu-id="33b1b-217">The following are some example declarations an HLSL shader might have.</span></span> <span data-ttu-id="33b1b-218">Обратите внимание, что отсутствуют ссылки на корневые сигнатуры или таблицы дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="33b1b-218">Note that there are no references to root signatures or descriptor tables.</span></span>

``` syntax
Texture2D foo[5] : register(t2);
Buffer bar : register(t7);
RWBuffer dataLog : register(u1);

Sampler samp : register(s0);

struct Data
{
    UINT index;
    float4 color;
};
ConstantBuffer<Data> myData : register(b0);

Texture2D terrain[] : register(t8); // Unbounded array
Texture2D misc[] : register(t0,space1); // Another unbounded array 
                                        // space1 avoids overlap with above t#

struct MoreData
{
    float4x4 xform;
};
ConstantBuffer<MoreData> myMoreData : register(b1);

struct Stuff
{
    float2 factor;
    UINT drawID;
};
ConstantBuffer<Stuff> myStuff[][3][8]  : register(b2, space3)
```

## <a name="related-topics"></a><span data-ttu-id="33b1b-219">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="33b1b-219">Related topics</span></span>

* [<span data-ttu-id="33b1b-220">Динамическое индексирование с помощью HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="33b1b-220">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
* [<span data-ttu-id="33b1b-221">Effect — средство компилятора</span><span class="sxs-lookup"><span data-stu-id="33b1b-221">Effect-Compiler Tool</span></span>](/windows/win32/direct3dtools/fxc)
* [<span data-ttu-id="33b1b-222">Функции HLSL Shader Model 5,1 для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="33b1b-222">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/win32/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
* [<span data-ttu-id="33b1b-223">Упорядоченные представления средства прорисовки</span><span class="sxs-lookup"><span data-stu-id="33b1b-223">Rasterizer Ordered Views</span></span>](rasterizer-order-views.md)
* [<span data-ttu-id="33b1b-224">Привязка ресурсов</span><span class="sxs-lookup"><span data-stu-id="33b1b-224">Resource Binding</span></span>](resource-binding.md)
* [<span data-ttu-id="33b1b-225">Корневые подписи</span><span class="sxs-lookup"><span data-stu-id="33b1b-225">Root Signatures</span></span>](root-signatures.md)
* [<span data-ttu-id="33b1b-226">Модель шейдера 5,1</span><span class="sxs-lookup"><span data-stu-id="33b1b-226">Shader Model 5.1</span></span>](/windows/win32/direct3dhlsl/shader-model-5-1)
* [<span data-ttu-id="33b1b-227">Заданное значение ссылки на набор элементов в шейдере</span><span class="sxs-lookup"><span data-stu-id="33b1b-227">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
* [<span data-ttu-id="33b1b-228">Указание корневых подписей в HLSL</span><span class="sxs-lookup"><span data-stu-id="33b1b-228">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
