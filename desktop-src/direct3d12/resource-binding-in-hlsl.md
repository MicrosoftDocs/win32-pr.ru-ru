---
title: Привязка ресурсов в HLSL
description: В этом разделе описываются некоторые особенности использования модели шейдера высокого уровня Shader (HLSL) 5,1 с Direct3D 12.
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 749fed319f9ffe840f2b06512e337efa28081e24
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548998"
---
# <a name="resource-binding-in-hlsl"></a><span data-ttu-id="f1983-103">Привязка ресурсов в HLSL</span><span class="sxs-lookup"><span data-stu-id="f1983-103">Resource binding in HLSL</span></span>

<span data-ttu-id="f1983-104">В этом разделе описываются некоторые особенности использования [модели шейдера](/windows/desktop/direct3dhlsl/shader-model-5-1) высокого уровня Shader (HLSL) 5,1 с Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="f1983-104">This topic describes some specific features of using High Level Shader Language (HLSL) [Shader Model 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) with Direct3D 12.</span></span> <span data-ttu-id="f1983-105">Все оборудование Direct3D 12 поддерживает модель шейдера 5,1, поэтому поддержка этой модели не зависит от уровня компонентов оборудования.</span><span class="sxs-lookup"><span data-stu-id="f1983-105">All Direct3D 12 hardware supports Shader Model 5.1, so support for this model does not depend on what the hardware feature level is.</span></span>

-   [<span data-ttu-id="f1983-106">Типы ресурсов и массивы</span><span class="sxs-lookup"><span data-stu-id="f1983-106">Resource types and arrays</span></span>](#resource-types-and-arrays)
-   [<span data-ttu-id="f1983-107">Массивы дескрипторов и массивы текстур</span><span class="sxs-lookup"><span data-stu-id="f1983-107">Descriptor arrays and texture arrays</span></span>](#descriptor-arrays-and-texture-arrays)
-   [<span data-ttu-id="f1983-108">Присвоение псевдонимов ресурсам</span><span class="sxs-lookup"><span data-stu-id="f1983-108">Resource aliasing</span></span>](#resource-aliasing)
-   [<span data-ttu-id="f1983-109">Расхождение и производные</span><span class="sxs-lookup"><span data-stu-id="f1983-109">Divergence and derivatives</span></span>](#divergence-and-derivatives)
-   [<span data-ttu-id="f1983-110">Уавс в шейдере пикселей</span><span class="sxs-lookup"><span data-stu-id="f1983-110">UAVs in pixel shaders</span></span>](#uavs-in-pixel-shaders)
-   [<span data-ttu-id="f1983-111">Буферы констант</span><span class="sxs-lookup"><span data-stu-id="f1983-111">Constant Buffers</span></span>](#constant-buffers)
-   [<span data-ttu-id="f1983-112">Изменения байтового кода в SM 5.1</span><span class="sxs-lookup"><span data-stu-id="f1983-112">Bytecode changes in SM5.1</span></span>](#bytecode-changes-in-sm51)
-   [<span data-ttu-id="f1983-113">Примеры объявлений HLSL</span><span class="sxs-lookup"><span data-stu-id="f1983-113">Example HLSL Declarations</span></span>](#example-hlsl-declarations)
-   [<span data-ttu-id="f1983-114">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="f1983-114">Related topics</span></span>](#related-topics)

## <a name="resource-types-and-arrays"></a><span data-ttu-id="f1983-115">Типы ресурсов и массивы</span><span class="sxs-lookup"><span data-stu-id="f1983-115">Resource types and arrays</span></span>

<span data-ttu-id="f1983-116">Синтаксис ресурсов Shader Model 5 (SM 5.0) использует `register` ключевое слово для ретрансляции важной информации о ресурсе в КОМПИЛЯТОР HLSL.</span><span class="sxs-lookup"><span data-stu-id="f1983-116">Shader Model 5 (SM5.0) resource syntax uses the `register` keyword to relay important information about the resource to the HLSL compiler.</span></span> <span data-ttu-id="f1983-117">Например, следующая инструкция объявляет массив из четырех текстур, привязанных к разъемам T3, T4, T5 и T6.</span><span class="sxs-lookup"><span data-stu-id="f1983-117">For example, the following statement declares an array of four textures bound at slots t3, t4, t5, and t6.</span></span> <span data-ttu-id="f1983-118">T3 — единственный слот регистров, отображаемый в операторе, просто первый в массиве из четырех.</span><span class="sxs-lookup"><span data-stu-id="f1983-118">t3 is the only register slot appearing in the statement, simply being the first in the array of four.</span></span>

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

<span data-ttu-id="f1983-119">Синтаксис ресурсов в модели шейдеров 5,1 (SM 5.1) в HLSL основан на существующем синтаксисе ресурсов регистров, что позволяет упростить перенос.</span><span class="sxs-lookup"><span data-stu-id="f1983-119">Shader Model 5.1 (SM5.1) resource syntax in HLSL is based on existing register resource syntax, to allow easier porting.</span></span> <span data-ttu-id="f1983-120">Ресурсы Direct3D 12 в HLSL привязаны к виртуальным регистрам в логических пространствах регистров:</span><span class="sxs-lookup"><span data-stu-id="f1983-120">Direct3D 12 resources in HLSL are bound to virtual registers within logical register spaces:</span></span>

-   <span data-ttu-id="f1983-121">t — для представлений ресурсов шейдера (SRV)</span><span class="sxs-lookup"><span data-stu-id="f1983-121">t – for shader resource views (SRV)</span></span>
-   <span data-ttu-id="f1983-122">s — для проб</span><span class="sxs-lookup"><span data-stu-id="f1983-122">s – for samplers</span></span>
-   <span data-ttu-id="f1983-123">u — для неупорядоченных представлений доступа (UAV)</span><span class="sxs-lookup"><span data-stu-id="f1983-123">u – for unordered access views (UAV)</span></span>
-   <span data-ttu-id="f1983-124">b — для представлений буфера констант (CBV)</span><span class="sxs-lookup"><span data-stu-id="f1983-124">b – for constant buffer views (CBV)</span></span>

<span data-ttu-id="f1983-125">Корневая подпись, ссылающаяся на шейдер, должна быть совместима с объявленными слотами регистров.</span><span class="sxs-lookup"><span data-stu-id="f1983-125">The root signature referencing the shader must be compatible with the declared register slots.</span></span> <span data-ttu-id="f1983-126">Например, следующая часть корневой сигнатуры будет совместима с использованием слотов текстур с T3 до T6, так как в нем описывается таблица дескрипторов с слотами, t0 через T98.</span><span class="sxs-lookup"><span data-stu-id="f1983-126">For example, the following portion of a root signature would be compatible with the use of texture slots t3 through t6, as it describes a descriptor table with slots t0 through t98.</span></span>

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

<span data-ttu-id="f1983-127">Объявление ресурса может быть скалярным, массивом 1D или многомерным массивом.</span><span class="sxs-lookup"><span data-stu-id="f1983-127">A resource declaration may be a scalar, a 1D array, or a multidimensional array:</span></span>

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

<span data-ttu-id="f1983-128">В SM 5.1 используются те же типы ресурсов и типы элементов, что и в SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="f1983-128">SM5.1 uses the same resource types and element types as SM5.0 does.</span></span> <span data-ttu-id="f1983-129">Ограничения объявления SM 5.1 более гибкие и ограничены только ограничениями среды выполнения и оборудования.</span><span class="sxs-lookup"><span data-stu-id="f1983-129">SM5.1 declaration limits are more flexible, and constrained only by the runtime/hardware limits.</span></span> <span data-ttu-id="f1983-130">`space`Ключевое слово указывает, к какому пространству логических регистров привязана объявленная переменная.</span><span class="sxs-lookup"><span data-stu-id="f1983-130">The `space` keyword specifies to which logical register space the declared variable is bound.</span></span> <span data-ttu-id="f1983-131">Если `space` ключевое слово опущено, то индекс пространства по умолчанию, равный 0, неявно присваивается диапазону (так что `tex2` диапазон выше находится в `space0` ).</span><span class="sxs-lookup"><span data-stu-id="f1983-131">If the `space` keyword is omitted, then the default space index of 0 is implicitly assigned to the range (so the `tex2` range above resides in `space0`).</span></span> <span data-ttu-id="f1983-132">`register(t3,  space0)` никогда не будет конфликтовать с `register(t3,  space1)` или с любым массивом в другом пространстве, который может включать T3.</span><span class="sxs-lookup"><span data-stu-id="f1983-132">`register(t3,  space0)` will never conflict with `register(t3,  space1)`, nor with any array in another space that might include t3.</span></span>

<span data-ttu-id="f1983-133">Ресурс массива может иметь неограниченный размер, который объявляется с помощью указания первого измерения, который должен быть пустым, или 0:</span><span class="sxs-lookup"><span data-stu-id="f1983-133">An array resource may have an unbounded size, which is declared by specifying the very first dimension to be empty, or 0:</span></span>

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

<span data-ttu-id="f1983-134">Соответствующая таблица дескрипторов может быть:</span><span class="sxs-lookup"><span data-stu-id="f1983-134">The matching descriptor table could be:</span></span>

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

<span data-ttu-id="f1983-135">Неограниченный массив в HLSL соответствует фиксированному числу, заданному `numDescriptors` в таблице дескрипторов, и фиксированный размер в HLSL соответствует неограниченному объявлению в таблице дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="f1983-135">An unbounded array in HLSL does match a fixed number set with `numDescriptors` in the descriptor table, and a fixed size in the HLSL does match an unbounded declaration in the descriptor table.</span></span>

<span data-ttu-id="f1983-136">Многомерные массивы допускаются, включая неограниченный размер.</span><span class="sxs-lookup"><span data-stu-id="f1983-136">Multi-dimensional arrays are allowed, including of an unbounded size.</span></span> <span data-ttu-id="f1983-137">Эти многомерные массивы выравниваются из пространства регистров.</span><span class="sxs-lookup"><span data-stu-id="f1983-137">These multidimensional arrays are flattened out in register space.</span></span>

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

<span data-ttu-id="f1983-138">Использование псевдонимов диапазонов ресурсов не допускается.</span><span class="sxs-lookup"><span data-stu-id="f1983-138">Aliasing of resource ranges is not allowed.</span></span> <span data-ttu-id="f1983-139">Иными словами, для каждого типа ресурса (t, s, u, b) объявленные диапазоны регистров не должны перекрываются.</span><span class="sxs-lookup"><span data-stu-id="f1983-139">In other words, for each resource type (t, s, u, b), declared register ranges mustn't overlap.</span></span> <span data-ttu-id="f1983-140">Это также относится и к неограниченным диапазонам.</span><span class="sxs-lookup"><span data-stu-id="f1983-140">That includes unbounded ranges, too.</span></span> <span data-ttu-id="f1983-141">Диапазоны, объявленные в разных пространствах регистра, никогда не перекрываются.</span><span class="sxs-lookup"><span data-stu-id="f1983-141">Ranges declared in different register spaces never overlap.</span></span> <span data-ttu-id="f1983-142">Обратите внимание, что неограниченное `tex2` (выше) размещается в `space0` , а непривязанных `tex3` — в `space1` , так что они не перекрываются.</span><span class="sxs-lookup"><span data-stu-id="f1983-142">Note that unbounded `tex2` (above) resides in `space0`, while unbounded `tex3` resides in `space1`, such that they don't overlap.</span></span>

<span data-ttu-id="f1983-143">Для доступа к ресурсам, объявленным как массивы, достаточно просто индексировать их.</span><span class="sxs-lookup"><span data-stu-id="f1983-143">Accessing resources that have been declared as arrays is as simple as indexing them.</span></span>

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

<span data-ttu-id="f1983-144">Существует важное ограничение по умолчанию для использования индексов ( `myMaterialID` и `samplerID` в приведенном выше коде) тем, что они не могут быть разными в [волне](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span><span class="sxs-lookup"><span data-stu-id="f1983-144">There's an important default restriction on the use of the indices (`myMaterialID` and `samplerID` in the code above) in that they're not allowed to vary within a [wave](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span></span> <span data-ttu-id="f1983-145">Даже изменение индекса на основе количества экземпляров.</span><span class="sxs-lookup"><span data-stu-id="f1983-145">Even changing the index based on instancing counts as varying.</span></span>

<span data-ttu-id="f1983-146">Если требуется изменение индекса, укажите в `NonUniformResourceIndex` индексе квалификатор, например:</span><span class="sxs-lookup"><span data-stu-id="f1983-146">If varying the index is required then specify the `NonUniformResourceIndex` qualifier on the index, for example:</span></span>

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

<span data-ttu-id="f1983-147">На некоторых устройствах использование этого квалификатора создает дополнительный код для обеспечения правильности (включая потоки), но при незначительной стоимости производительности.</span><span class="sxs-lookup"><span data-stu-id="f1983-147">On some hardware the use of this qualifier generates additional code to enforce correctness (including across threads) but at a minor performance cost.</span></span> <span data-ttu-id="f1983-148">Если индекс изменяется без квалификатора и в процессе рисования/отправки результаты не определены.</span><span class="sxs-lookup"><span data-stu-id="f1983-148">If an index is changed without this qualifier and within a draw/dispatch the results are undefined.</span></span>

## <a name="descriptor-arrays-and-texture-arrays"></a><span data-ttu-id="f1983-149">Массивы дескрипторов и массивы текстур</span><span class="sxs-lookup"><span data-stu-id="f1983-149">Descriptor arrays and texture arrays</span></span>

<span data-ttu-id="f1983-150">С момента выпуска DirectX 10 были доступны массивы текстур.</span><span class="sxs-lookup"><span data-stu-id="f1983-150">Texture arrays have been available since DirectX 10.</span></span> <span data-ttu-id="f1983-151">Для массивов текстуры требуется один дескриптор, однако все срезы массива должны иметь одинаковый формат, ширину, высоту и число MIP.</span><span class="sxs-lookup"><span data-stu-id="f1983-151">Texture arrays require one descriptor, however all the array slices must share the same format, width, height and mip count.</span></span> <span data-ttu-id="f1983-152">Кроме того, массив должен занимать непрерывный диапазон в виртуальном адресном пространстве.</span><span class="sxs-lookup"><span data-stu-id="f1983-152">Also, the array must occupy a contiguous range in virtual address space.</span></span> <span data-ttu-id="f1983-153">В следующем коде показан пример доступа к массиву текстуры из шейдера.</span><span class="sxs-lookup"><span data-stu-id="f1983-153">The following code shows an example of accessing a texture array from a shader.</span></span>

``` syntax
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

<span data-ttu-id="f1983-154">В массиве текстур индекс может свободно изменяться без каких-либо необходимых квалификаторов, таких как `NonUniformResourceIndex` .</span><span class="sxs-lookup"><span data-stu-id="f1983-154">In a texture array, the index can be varied freely, without any need for qualifiers such as `NonUniformResourceIndex`.</span></span>

<span data-ttu-id="f1983-155">Эквивалентный массив дескрипторов будет следующим:</span><span class="sxs-lookup"><span data-stu-id="f1983-155">The equivalent descriptor array would be:</span></span>

``` syntax
Texture2D<float4> myTex2DArray[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

<span data-ttu-id="f1983-156">Обратите внимание, что неудобное использование float для индекса массива заменяется на `myTex2D[2]` .</span><span class="sxs-lookup"><span data-stu-id="f1983-156">Note the awkward use of a float for the array index is replaced with `myTex2D[2]`.</span></span> <span data-ttu-id="f1983-157">Кроме того, массивы дескрипторов обеспечивают большую гибкость при использовании измерений.</span><span class="sxs-lookup"><span data-stu-id="f1983-157">Also descriptor arrays offer more flexibility with the dimensions.</span></span> <span data-ttu-id="f1983-158">Тип `Texture2D` — это пример, который не может быть разным, но формат, ширина, высота и число MIP могут различаться в зависимости от каждого дескриптора.</span><span class="sxs-lookup"><span data-stu-id="f1983-158">The type, `Texture2D` is this example, cannot vary, but the format, width, height, and mip count can all vary with each descriptor.</span></span>

<span data-ttu-id="f1983-159">В качестве дескриптора можно использовать массив массивов текстур:</span><span class="sxs-lookup"><span data-stu-id="f1983-159">It is legitimate to have a descriptor array of texture arrays:</span></span>

``` syntax
Texture2DArray<float4> myTex2DArrayOfArrays[2] : register(t0);
```

<span data-ttu-id="f1983-160">Незаконно объявлять массив структур, каждая структура, содержащая дескрипторы, например следующий код, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f1983-160">It is not legitimate to declare an array of structures, each structure containing descriptors, for example the following code is not supported.</span></span>

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

<span data-ttu-id="f1983-161">Это позволило бы abcabcabc макет памяти **....**, но является ограничением языка и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f1983-161">This would have allowed the memory layout **abcabcabc....**, but is a language limitation and is not supported.</span></span> <span data-ttu-id="f1983-162">Ниже приведен один из поддерживаемых методов выполнения этой операции, хотя в этом случае в качестве структуры памяти используется **AAA... BBB... CCC**....</span><span class="sxs-lookup"><span data-stu-id="f1983-162">One supported method of doing this would be as follows, though the memory layout in this case is **aaa...bbb...ccc...**.</span></span>

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

<span data-ttu-id="f1983-163">Чтобы получить макет памяти **abcabcabc....** , используйте таблицу дескрипторов без использования `myStruct` структуры.</span><span class="sxs-lookup"><span data-stu-id="f1983-163">To achieve the **abcabcabc....** memory layout, use a descriptor table without use of the `myStruct` structure.</span></span>

## <a name="resource-aliasing"></a><span data-ttu-id="f1983-164">Присвоение псевдонимов ресурсам</span><span class="sxs-lookup"><span data-stu-id="f1983-164">Resource aliasing</span></span>

<span data-ttu-id="f1983-165">Диапазоны ресурсов, указанные в шейдерах HLSL, являются логическими диапазонами.</span><span class="sxs-lookup"><span data-stu-id="f1983-165">The resource ranges specified in the HLSL shaders are logical ranges.</span></span> <span data-ttu-id="f1983-166">Они привязаны к конкретным диапазонам кучи во время выполнения через механизм корневой подписи.</span><span class="sxs-lookup"><span data-stu-id="f1983-166">They are be bound to concrete heap ranges at runtime via the root signature mechanism.</span></span> <span data-ttu-id="f1983-167">Как правило, логический диапазон сопоставляется с диапазоном кучи, который не перекрывается с другими диапазонами кучи.</span><span class="sxs-lookup"><span data-stu-id="f1983-167">Normally, a logical range maps to a heap range that does not overlap with other heap ranges.</span></span> <span data-ttu-id="f1983-168">Однако механизм корневой подписи делает возможным псевдонимы диапазонов кучи совместимых типов.</span><span class="sxs-lookup"><span data-stu-id="f1983-168">However, the root signature mechanism makes it possible to alias (overlap) heap ranges of compatible types.</span></span> <span data-ttu-id="f1983-169">Например, `tex2` и `tex3` диапазоны из приведенного выше примера могут быть сопоставлены с одним (или перекрывающим) диапазоном кучи, в котором действует псевдоним текстур в программе HLSL.</span><span class="sxs-lookup"><span data-stu-id="f1983-169">For example, `tex2` and `tex3` ranges from the above example may be mapped to the same (or overlapping) heap range, which has the effect of aliasing textures in the HLSL program.</span></span> <span data-ttu-id="f1983-170">Если требуется такое присвоение псевдонимов, шейдер должен быть скомпилирован с использованием \_ ресурсов шейдера \_ D3D10 \_ \_ , которые задаются с помощью параметра */RES может быть \_ \_ псевдонимом* для [средства компилятора Effect](/windows/desktop/direct3dtools/fxc) (FXC).</span><span class="sxs-lookup"><span data-stu-id="f1983-170">If such aliasing is desired, the shader must be compiled with D3D10\_SHADER\_RESOURCES\_MAY\_ALIAS option, which is set by using the */res\_may\_alias* option for the [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC).</span></span> <span data-ttu-id="f1983-171">Параметр позволяет компилятору создавать правильный код, предотвращая определенные оптимизации нагрузки и хранения в соответствии с предположением, что ресурсы могут быть псевдонимами.</span><span class="sxs-lookup"><span data-stu-id="f1983-171">The option makes the compiler produce correct code by preventing certain load/store optimizations under the assumption that resources may alias.</span></span>

## <a name="divergence-and-derivatives"></a><span data-ttu-id="f1983-172">Расхождение и производные</span><span class="sxs-lookup"><span data-stu-id="f1983-172">Divergence and derivatives</span></span>

<span data-ttu-id="f1983-173">SM 5.1 не накладывает ограничений на индекс ресурсов; т. е. ` tex2[idx].Sample(…)` индекс idx может быть литеральной константой, константой кбуффер или интерполяцией значения.</span><span class="sxs-lookup"><span data-stu-id="f1983-173">SM5.1 does not impose limitations on the resource index; i.e.,` tex2[idx].Sample(…)` – the index idx can be a literal constant, a cbuffer constant, or an interpolated value.</span></span> <span data-ttu-id="f1983-174">Хотя модель программирования обеспечивает такую высокую гибкость, существуют проблемы, которые следует учитывать:</span><span class="sxs-lookup"><span data-stu-id="f1983-174">While the programming model provides such great flexibility, there are issues to be aware of:</span></span>

-   <span data-ttu-id="f1983-175">Если индекс рассходится по четырем, то вычисленное оборудованием производные и производные количества, например Лод, могут быть неопределенными.</span><span class="sxs-lookup"><span data-stu-id="f1983-175">If index diverges across a quad, the hardware-computed derivative and derived quantities such as LOD may be undefined.</span></span> <span data-ttu-id="f1983-176">Компилятор HLSL делает лучшие усилия для выдачи предупреждения в этом случае, но не помешает компиляции шейдера.</span><span class="sxs-lookup"><span data-stu-id="f1983-176">The HLSL compiler makes the best effort to issue a warning in this case, but will not prevent a shader from compiling.</span></span> <span data-ttu-id="f1983-177">Такое поведение аналогично вычислению производных элементов в последовательном потоке управления.</span><span class="sxs-lookup"><span data-stu-id="f1983-177">This behavior is similar to computing derivatives in divergent control flow.</span></span>
-   <span data-ttu-id="f1983-178">Если индекс ресурсов отличается, производительность уменьшается по сравнению с вариантом универсального индекса, так как оборудование должно выполнять операции с несколькими ресурсами.</span><span class="sxs-lookup"><span data-stu-id="f1983-178">If the resource index is divergent, the performance is diminished compared to the case of a uniform index, because the hardware needs to perform operations on several resources.</span></span> <span data-ttu-id="f1983-179">Индексы ресурсов, которые могут быть иными, должны быть помечены `NonUniformResourceIndex` функцией в коде HLSL.</span><span class="sxs-lookup"><span data-stu-id="f1983-179">Resource indexes that may be divergent must be marked with the `NonUniformResourceIndex` function in HLSL code.</span></span> <span data-ttu-id="f1983-180">В противном случае результаты не определены.</span><span class="sxs-lookup"><span data-stu-id="f1983-180">Otherwise results are undefined.</span></span>

## <a name="uavs-in-pixel-shaders"></a><span data-ttu-id="f1983-181">Уавс в шейдере пикселей</span><span class="sxs-lookup"><span data-stu-id="f1983-181">UAVs in pixel shaders</span></span>

<span data-ttu-id="f1983-182">SM 5.1 не накладывает ограничений на диапазоны UAV в шейдерах пикселей, как это было в случае SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="f1983-182">SM5.1 does not impose constraints on UAV ranges in pixel shaders as was the case for SM5.0.</span></span>

## <a name="constant-buffers"></a><span data-ttu-id="f1983-183">Буферы констант</span><span class="sxs-lookup"><span data-stu-id="f1983-183">Constant Buffers</span></span>

<span data-ttu-id="f1983-184">Синтаксис для константных буферов SM 5.1 (кбуффер) изменился с SM 5.0, чтобы позволить разработчикам индексировать буферы констант.</span><span class="sxs-lookup"><span data-stu-id="f1983-184">SM5.1 constant buffers (cbuffer) syntax has changed from SM5.0 to enable developers to index constant buffers.</span></span> <span data-ttu-id="f1983-185">Чтобы включить индексируемые буферы констант, SM 5.1 вводит `ConstantBuffer` конструкцию "Template":</span><span class="sxs-lookup"><span data-stu-id="f1983-185">To enable indexable constant buffers, SM5.1 introduces the `ConstantBuffer` “template” construct:</span></span>

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

<span data-ttu-id="f1983-186">Приведенный выше код объявляет переменную буфера константы `myCB1` типа `Foo` и размера 6, а также скалярную переменную буфера `myCB2` .</span><span class="sxs-lookup"><span data-stu-id="f1983-186">The preceding code declares constant buffer variable `myCB1` of type `Foo` and size 6, and a scalar, constant buffer variable `myCB2`.</span></span> <span data-ttu-id="f1983-187">Переменная буфера константы теперь может индексироваться в шейдере следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f1983-187">A constant buffer variable can now be indexed in the shader as:</span></span>

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

<span data-ttu-id="f1983-188">Поля "a" и "b" не становятся глобальными переменными, а должны рассматриваться как поля.</span><span class="sxs-lookup"><span data-stu-id="f1983-188">Fields ‘a’ and ‘b’ do not become global variables, but rather must be treated as fields.</span></span> <span data-ttu-id="f1983-189">Для обеспечения обратной совместимости SM 5.1 поддерживает старую концепцию кбуффер для скалярного cbuffer.</span><span class="sxs-lookup"><span data-stu-id="f1983-189">For backward compatibility, SM5.1 supports the old cbuffer concept for scalar cbuffers.</span></span> <span data-ttu-id="f1983-190">Следующая инструкция делает глобальные переменные «a» и «b» только для чтения, как в SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="f1983-190">The following statement makes ‘a’ and ‘b’ global, read-only variables as in SM5.0.</span></span> <span data-ttu-id="f1983-191">Однако такие кбуффер не могут индексироваться.</span><span class="sxs-lookup"><span data-stu-id="f1983-191">However, such an old-style cbuffer cannot be indexable.</span></span>

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

<span data-ttu-id="f1983-192">В настоящее время компилятор шейдеров поддерживает `ConstantBuffer` шаблон только для определяемых пользователем структур.</span><span class="sxs-lookup"><span data-stu-id="f1983-192">Currently, the shader compiler supports the `ConstantBuffer` template for user-defined structures only.</span></span>

<span data-ttu-id="f1983-193">В целях совместимости компилятор HLSL может автоматически назначать регистры ресурсов для диапазонов, объявленных в `space0` .</span><span class="sxs-lookup"><span data-stu-id="f1983-193">For compatibility reasons, the HLSL compiler may automatically assign resource registers for ranges declared in `space0`.</span></span> <span data-ttu-id="f1983-194">Если в предложении Register не указан пробел, используется значение по умолчанию `space0` .</span><span class="sxs-lookup"><span data-stu-id="f1983-194">If ‘space’ is omitted in the register clause, the default `space0` is used.</span></span> <span data-ttu-id="f1983-195">Для назначения регистров компилятор использует эвристический метод "первый-дыра".</span><span class="sxs-lookup"><span data-stu-id="f1983-195">The compiler uses the first-hole-fits heuristic to assign the registers.</span></span> <span data-ttu-id="f1983-196">Назначение можно получить с помощью API отражения, который был расширен для добавления поля *пробела* , а поле *биндпоинт* — нижнюю границу диапазона регистров ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f1983-196">The assignment can be retrieved via the reflection API, which has been extended to add the *Space* field for space, while the *BindPoint* field indicates the lower bound of the resource register range.</span></span>

## <a name="bytecode-changes-in-sm51"></a><span data-ttu-id="f1983-197">Изменения байтового кода в SM 5.1</span><span class="sxs-lookup"><span data-stu-id="f1983-197">Bytecode changes in SM5.1</span></span>

<span data-ttu-id="f1983-198">SM 5.1 изменяет объявление регистров ресурсов и ссылки в инструкциях.</span><span class="sxs-lookup"><span data-stu-id="f1983-198">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span> <span data-ttu-id="f1983-199">Синтаксис включает объявление переменной Register, аналогично тому, как это делается для групповых регистров общей памяти:</span><span class="sxs-lookup"><span data-stu-id="f1983-199">The syntax involves declaring a register “variable”, similar to how it is done for group shared memory registers:</span></span>

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

<span data-ttu-id="f1983-200">Будет разбираться в:</span><span class="sxs-lookup"><span data-stu-id="f1983-200">This will disassemble to:</span></span>

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

<span data-ttu-id="f1983-201">Каждый диапазон ресурсов шейдера теперь имеет идентификатор (имя), уникальный для байт-кода шейдера.</span><span class="sxs-lookup"><span data-stu-id="f1983-201">Each shader resource range now has an ID (a name) that is unique to the shader bytecode.</span></span> <span data-ttu-id="f1983-202">Например, массив текстуры Tex1 (T10) превращается в "1" в байт-код шейдера.</span><span class="sxs-lookup"><span data-stu-id="f1983-202">For example, tex1 (t10) texture array becomes ‘T1’ in the shader bytecode.</span></span> <span data-ttu-id="f1983-203">Присвоение уникальных идентификаторов каждому диапазону ресурсов позволяет выполнить два действия:</span><span class="sxs-lookup"><span data-stu-id="f1983-203">Giving unique IDs to each resource range allows two things:</span></span>

-   <span data-ttu-id="f1983-204">Однозначно определяет, какой диапазон ресурсов (см. дкл \_ Resource \_ Texture2D) индексируется в инструкции (см. пример инструкции).</span><span class="sxs-lookup"><span data-stu-id="f1983-204">Unambiguously identify which resource range (see dcl\_resource\_texture2d) is being indexed in an instruction (see sample instruction).</span></span>
-   <span data-ttu-id="f1983-205">Присоединение набора атрибутов к объявлению, например, тип элемента, размер шага, режим растровой операции и т. д.</span><span class="sxs-lookup"><span data-stu-id="f1983-205">Attaching a set of attributes to the declaration, e.g., element type, stride size, raster operation mode, etc.</span></span>

<span data-ttu-id="f1983-206">Обратите внимание, что идентификатор диапазона не связан с объявлением HLSL нижней границы.</span><span class="sxs-lookup"><span data-stu-id="f1983-206">Note that the ID of the range is not related to the HLSL lower bound declaration.</span></span>

<span data-ttu-id="f1983-207">Порядок привязок ресурсов отражения (сверху) и инструкций объявлений шейдера (дкл \_ \* ) аналогичен, чтобы помочь в определении соответствия между переменными HLSL и идентификаторами байт-кода.</span><span class="sxs-lookup"><span data-stu-id="f1983-207">The order of reflection resource bindings (listing at the top) and shader declaration instructions (dcl\_\*) is the same to aid in identifying the correspondence between HLSL variables and bytecode IDs.</span></span>

<span data-ttu-id="f1983-208">Каждая инструкция объявления в SM 5.1 использует трехмерный операнд для определения: идентификатор диапазона, Нижняя и верхняя границы.</span><span class="sxs-lookup"><span data-stu-id="f1983-208">Each declaration instruction in SM5.1 uses a 3D operand to define: range ID, lower and upper bounds.</span></span> <span data-ttu-id="f1983-209">Для указания пространства регистра создается дополнительный токен.</span><span class="sxs-lookup"><span data-stu-id="f1983-209">An additional token is emitted to specify the register space.</span></span> <span data-ttu-id="f1983-210">Также могут выдаваться другие токены для передачи дополнительных свойств диапазона, например кбуффер или инструкция объявления буфера, выдает размер кбуффер или структуры.</span><span class="sxs-lookup"><span data-stu-id="f1983-210">Other tokens may be emitted as well to convey additional properties of the range, e.g., cbuffer or structured buffer declaration instruction emits the size of the cbuffer or structure.</span></span> <span data-ttu-id="f1983-211">Точные сведения о кодировке можно найти в d3d12TokenizedProgramFormat. h и **D3D10ShaderBinary:: кшадеркодепарсер**.</span><span class="sxs-lookup"><span data-stu-id="f1983-211">The exact details of encoding can be found in d3d12TokenizedProgramFormat.h and **D3D10ShaderBinary::CShaderCodeParser**.</span></span>

<span data-ttu-id="f1983-212">Инструкции SM 5.1 не будут выдавать дополнительные сведения о операндах ресурсов в рамках инструкции (как в SM 5.0).</span><span class="sxs-lookup"><span data-stu-id="f1983-212">SM5.1 instructions will not emit additional resource operand information as part of the instruction (as in SM5.0).</span></span> <span data-ttu-id="f1983-213">Эти сведения теперь приведены в инструкциях по объявлению.</span><span class="sxs-lookup"><span data-stu-id="f1983-213">This information is now in the declaration instructions.</span></span> <span data-ttu-id="f1983-214">В SM 5.0 приведены инструкции по индексированию ресурсов, необходимых атрибутам ресурсов, которые должны быть описаны в маркерах расширенного кода операции, поскольку индексирование замаскировано к объявлению.</span><span class="sxs-lookup"><span data-stu-id="f1983-214">In SM5.0, instructions indexing resources required resource attributes to be described in extended opcode tokens, since indexing obfuscated the association to the declaration.</span></span> <span data-ttu-id="f1983-215">В SM 5.1 Каждый идентификатор (например, "'t 1") однозначно связан с одним объявлением, описывающим необходимые сведения о ресурсах.</span><span class="sxs-lookup"><span data-stu-id="f1983-215">In SM5.1, each ID (such as ‘t1’) is unambiguously associated with a single declaration that describes the required resource information.</span></span> <span data-ttu-id="f1983-216">Поэтому маркеры расширенного кода операций, используемые в инструкциях для описания сведений о ресурсах, больше не создаются.</span><span class="sxs-lookup"><span data-stu-id="f1983-216">Therefore, the extended opcode tokens used on instructions to describe resource information are no longer emitted.</span></span>

<span data-ttu-id="f1983-217">В инструкциях без объявления операнд ресурса для образцов, СРВС и Уавс является 2D-операндом.</span><span class="sxs-lookup"><span data-stu-id="f1983-217">In non-declaration instructions, a resource operand for samplers, SRVs, and UAVs is a 2D operand.</span></span> <span data-ttu-id="f1983-218">Первый индекс представляет собой литеральную константу, указывающую идентификатор диапазона.</span><span class="sxs-lookup"><span data-stu-id="f1983-218">The first index is a literal constant that specifies the range ID.</span></span> <span data-ttu-id="f1983-219">Второй индекс представляет линейное значение индекса.</span><span class="sxs-lookup"><span data-stu-id="f1983-219">The second index represents the linearized value of the index.</span></span> <span data-ttu-id="f1983-220">Значение высчитывается относительно начала соответствующего пространства регистра (не относительно начала логического диапазона) для лучшего сопоставления с корневой подписью и для уменьшения количества погрузок компилятора драйвера на настройку индекса.</span><span class="sxs-lookup"><span data-stu-id="f1983-220">The value is computed relative to the beginning of the corresponding register space (not relative to the beginning of the logical range) to better correlate with the root signature and to reduce the driver compiler burden of adjusting the index.</span></span>

<span data-ttu-id="f1983-221">Операнд ресурса для КБВС является трехмерным операндом, содержащим: литеральный идентификатор диапазона, индекс буфера константы и смещение в определенном экземпляре буфера констант.</span><span class="sxs-lookup"><span data-stu-id="f1983-221">A resource operand for CBVs is a 3D operand, containing: literal ID of the range, index of the constant buffer, offset into the particular instance of constant buffer.</span></span>

## <a name="example-hlsl-declarations"></a><span data-ttu-id="f1983-222">Примеры объявлений HLSL</span><span class="sxs-lookup"><span data-stu-id="f1983-222">Example HLSL Declarations</span></span>

<span data-ttu-id="f1983-223">Программам HLSL не нужно ничего знать о корневых сигнатурах.</span><span class="sxs-lookup"><span data-stu-id="f1983-223">HLSL programs do not need to know anything about root signatures.</span></span> <span data-ttu-id="f1983-224">Они могут назначать привязки к виртуальному пространству привязки "Register", t \# для СРВС, u \# для уавс, b \# для КБВС, s для \# проб или использовать компилятор для выбора назначений (и запрашивать полученные сопоставления с помощью отражения шейдера).</span><span class="sxs-lookup"><span data-stu-id="f1983-224">They can assign bindings to the virtual “register” binding space, t\# for SRVs, u\# for UAVs, b\# for CBVs, s\# for samplers, or rely on the compiler to pick assignments (and query the resulting mappings using shader reflection afterwards).</span></span> <span data-ttu-id="f1983-225">Корневой узел подписи сопоставляет таблицы дескрипторов, корневые дескрипторы и корневые константы с этим виртуальным пространством регистра.</span><span class="sxs-lookup"><span data-stu-id="f1983-225">The root signature maps descriptor tables, root descriptors, and root constants to this virtual register space.</span></span>

<span data-ttu-id="f1983-226">Ниже приведены примеры объявлений, которые может иметь Шейдер HLSL.</span><span class="sxs-lookup"><span data-stu-id="f1983-226">The following are some example declarations an HLSL shader might have.</span></span> <span data-ttu-id="f1983-227">Обратите внимание, что отсутствуют ссылки на корневые сигнатуры или таблицы дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="f1983-227">Note that there are no references to root signatures or descriptor tables.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="f1983-228">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="f1983-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1983-229">Динамическое индексирование с помощью HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="f1983-229">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[<span data-ttu-id="f1983-230">Effect — средство компилятора</span><span class="sxs-lookup"><span data-stu-id="f1983-230">Effect-Compiler Tool</span></span>](/windows/desktop/direct3dtools/fxc)
</dt> <dt>

[<span data-ttu-id="f1983-231">Функции HLSL Shader Model 5,1 для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="f1983-231">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[<span data-ttu-id="f1983-232">Упорядоченные представления средства прорисовки</span><span class="sxs-lookup"><span data-stu-id="f1983-232">Rasterizer Ordered Views</span></span>](rasterizer-order-views.md)
</dt> <dt>

[<span data-ttu-id="f1983-233">Привязка ресурсов</span><span class="sxs-lookup"><span data-stu-id="f1983-233">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="f1983-234">Корневые подписи</span><span class="sxs-lookup"><span data-stu-id="f1983-234">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="f1983-235">Модель шейдера 5,1</span><span class="sxs-lookup"><span data-stu-id="f1983-235">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="f1983-236">Заданное значение ссылки на набор элементов в шейдере</span><span class="sxs-lookup"><span data-stu-id="f1983-236">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
</dt> <dt>

[<span data-ttu-id="f1983-237">Указание корневых подписей в HLSL</span><span class="sxs-lookup"><span data-stu-id="f1983-237">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 