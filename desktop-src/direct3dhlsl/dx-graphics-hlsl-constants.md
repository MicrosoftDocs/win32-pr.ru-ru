---
title: Константы шейдера (HLSL)
description: В Shader Model 4 константы шейдеров хранятся в одном или нескольких буферных ресурсах в памяти.
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- кбуффер
- тбуффер
- буфер констант
- буфер текстуры
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f314be4b8da98ff80bd7404c270479855e13fb6e
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129963"
---
# <a name="shader-constants-hlsl"></a><span data-ttu-id="c1f54-107">Константы шейдера (HLSL)</span><span class="sxs-lookup"><span data-stu-id="c1f54-107">Shader Constants (HLSL)</span></span>

<span data-ttu-id="c1f54-108">В Shader Model 4 константы шейдеров хранятся в одном или нескольких буферных ресурсах в памяти.</span><span class="sxs-lookup"><span data-stu-id="c1f54-108">In Shader Model 4, shader constants are stored in one or more buffer resources in memory.</span></span> <span data-ttu-id="c1f54-109">Они могут быть организованы в два типа буферов: постоянные буферы (cbuffer) и буферы текстур (tbuffer).</span><span class="sxs-lookup"><span data-stu-id="c1f54-109">They can be organized into two types of buffers: constant buffers (cbuffers) and texture buffers (tbuffers).</span></span> <span data-ttu-id="c1f54-110">Буферы констант оптимизированы для использования переменных с постоянными переменными, которые характеризуются доступом к меньшим задержкам и чаще обновляются из ЦП.</span><span class="sxs-lookup"><span data-stu-id="c1f54-110">Constant buffers are optimized for constant-variable usage, which is characterized by lower-latency access and more frequent update from the CPU.</span></span> <span data-ttu-id="c1f54-111">По этой причине к этим ресурсам применяются дополнительные ограничения на размер, макет и доступ.</span><span class="sxs-lookup"><span data-stu-id="c1f54-111">For this reason, additional size, layout, and access restrictions apply to these resources.</span></span> <span data-ttu-id="c1f54-112">Доступ к текстурным буферам осуществляется как к текстурам, что обеспечивает лучшую производительность при произвольном индексировании данных.</span><span class="sxs-lookup"><span data-stu-id="c1f54-112">Texture buffers are accessed like textures and perform better for arbitrarily indexed data.</span></span> <span data-ttu-id="c1f54-113">Независимо от того, какой тип ресурса вы используете, не существует ограничения на количество буферов констант или буферов текстуры, которые может создать приложение.</span><span class="sxs-lookup"><span data-stu-id="c1f54-113">Regardless of which type of resource you use, there is no limit to the number of constant buffers or texture buffers an application can create.</span></span>

<span data-ttu-id="c1f54-114">Объявление буфера константы или буфера текстуры во многом похоже на объявление структуры в языке C с добавлением ключевых слов **Register** и **паккоффсет** для назначения регистров или данных упаковки вручную.</span><span class="sxs-lookup"><span data-stu-id="c1f54-114">Declaring a constant buffer or a texture buffer looks very much like a structure declaration in C, with the addition of the **register** and **packoffset** keywords for manually assigning registers or packing data.</span></span>



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1f54-115">*Буффертипе* \[ *Имя* \] \[: **Register**(b \# ) \] { *вариабледекларатион* \[ : **паккоффсет**(c \# . ксизв) \] ;      ... };</span><span class="sxs-lookup"><span data-stu-id="c1f54-115">*BufferType* \[*Name*\] \[: **register**(b\#)\] {     *VariableDeclaration* \[: **packoffset**(c\#.xyzw)\];      ... };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="c1f54-116">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1f54-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1f54-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*буффертипе*</span><span class="sxs-lookup"><span data-stu-id="c1f54-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*</span></span>
</dt> <dd>

<span data-ttu-id="c1f54-118">\[в \] буфере типа.</span><span class="sxs-lookup"><span data-stu-id="c1f54-118">\[in\] The buffer type.</span></span>



| <span data-ttu-id="c1f54-119">буффертипе</span><span class="sxs-lookup"><span data-stu-id="c1f54-119">BufferType</span></span> | <span data-ttu-id="c1f54-120">Описание</span><span class="sxs-lookup"><span data-stu-id="c1f54-120">Description</span></span>     |
|------------|-----------------|
| <span data-ttu-id="c1f54-121">кбуффер</span><span class="sxs-lookup"><span data-stu-id="c1f54-121">cbuffer</span></span>    | <span data-ttu-id="c1f54-122">буфер констант</span><span class="sxs-lookup"><span data-stu-id="c1f54-122">constant buffer</span></span> |
| <span data-ttu-id="c1f54-123">тбуффер</span><span class="sxs-lookup"><span data-stu-id="c1f54-123">tbuffer</span></span>    | <span data-ttu-id="c1f54-124">буфер текстуры</span><span class="sxs-lookup"><span data-stu-id="c1f54-124">texture buffer</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c1f54-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Безымян*</span><span class="sxs-lookup"><span data-stu-id="c1f54-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="c1f54-126">\[в \] необязательной строке ASCII, содержащей уникальное имя буфера.</span><span class="sxs-lookup"><span data-stu-id="c1f54-126">\[in\] Optional, ASCII string containing a unique buffer name.</span></span>

</dd> <dt>

<span data-ttu-id="c1f54-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**Регистрация**(b \# )</span><span class="sxs-lookup"><span data-stu-id="c1f54-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**register**(b\#)</span></span>
</dt> <dd>

<span data-ttu-id="c1f54-128">\[\]ключевое слово Optional используется для упаковки постоянных данных вручную.</span><span class="sxs-lookup"><span data-stu-id="c1f54-128">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="c1f54-129">Константы можно упаковывать в регистр только в буфере констант, где начальная регистр задается номером регистра ( *\#* ).</span><span class="sxs-lookup"><span data-stu-id="c1f54-129">Constants can be packed in a register only in a constant buffer, where the starting register is given by the register number (*\#*).</span></span>

</dd> <dt>

<span data-ttu-id="c1f54-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*вариабледекларатион*</span><span class="sxs-lookup"><span data-stu-id="c1f54-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*</span></span>
</dt> <dd>

<span data-ttu-id="c1f54-131">\[в \] объявлении переменной аналогично объявлению члена структуры.</span><span class="sxs-lookup"><span data-stu-id="c1f54-131">\[in\] Variable declaration, similar to a structure member declaration.</span></span> <span data-ttu-id="c1f54-132">Это может быть любой тип HLSL или объект Effect (за исключением текстуры или объекта образца).</span><span class="sxs-lookup"><span data-stu-id="c1f54-132">This can be any HLSL type or effect object (except a texture or a sampler object).</span></span>

</dd> <dt>

<span data-ttu-id="c1f54-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**паккоффсет**(c \# . ксизв)</span><span class="sxs-lookup"><span data-stu-id="c1f54-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c\#.xyzw)</span></span>
</dt> <dd>

<span data-ttu-id="c1f54-134">\[\]ключевое слово Optional используется для упаковки постоянных данных вручную.</span><span class="sxs-lookup"><span data-stu-id="c1f54-134">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="c1f54-135">Константы можно упаковывать в любой буфер констант, где номер регистра предоставляется ( *\#* ).</span><span class="sxs-lookup"><span data-stu-id="c1f54-135">Constants can be packed in any constant buffer, where the register number is given by (*\#*).</span></span> <span data-ttu-id="c1f54-136">Упаковка вложенных компонентов (с помощью ксизв группирующие) доступна для констант, размер которых умещается в пределах одного регистра (не пересекают границу регистра).</span><span class="sxs-lookup"><span data-stu-id="c1f54-136">Sub-component packing (using xyzw swizzling) is available for constants whose size fit within a single register (do not cross a register boundary).</span></span> <span data-ttu-id="c1f54-137">Например, float4 не может быть упакован в один регистр, начиная с компонента y, так как он не умещается в регистре из четырех компонентов.</span><span class="sxs-lookup"><span data-stu-id="c1f54-137">For instance, a float4 could not be packed in a single register starting with the y-component because it would not fit in a four-component register.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1f54-138">Remarks</span><span class="sxs-lookup"><span data-stu-id="c1f54-138">Remarks</span></span>

<span data-ttu-id="c1f54-139">Буферы констант уменьшают пропускную способность, необходимую для обновления констант шейдера, позволяя сгруппировать и обработать их одновременно, без отдельных вызовов для обработки каждой константы.</span><span class="sxs-lookup"><span data-stu-id="c1f54-139">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="c1f54-140">Постоянный буфер — это специализированный буферный ресурс, доступ к которому осуществляется как к буферу.</span><span class="sxs-lookup"><span data-stu-id="c1f54-140">A constant buffer is a specialized buffer resource that is accessed like a buffer.</span></span> <span data-ttu-id="c1f54-141">Каждый буфер константы может содержать до 4096 [векторов](dx-graphics-hlsl-vector.md); Каждый вектор содержит до 4 32-битных значений.</span><span class="sxs-lookup"><span data-stu-id="c1f54-141">Each constant buffer can hold up to 4096 [vectors](dx-graphics-hlsl-vector.md); each vector contains up to four 32-bit values.</span></span> <span data-ttu-id="c1f54-142">Можно выполнить привязку до 14 буферов констант на стадию конвейера (2 дополнительных слотов зарезервированы для внутреннего использования).</span><span class="sxs-lookup"><span data-stu-id="c1f54-142">You can bind up to 14 constant buffers per pipeline stage (2 additional slots are reserved for internal use).</span></span>

<span data-ttu-id="c1f54-143">Буфер текстуры — это специализированный буферный ресурс, доступ к которому осуществляется как к текстуре.</span><span class="sxs-lookup"><span data-stu-id="c1f54-143">A texture buffer is a specialized buffer resource that is accessed like a texture.</span></span> <span data-ttu-id="c1f54-144">Доступ к текстуре (по сравнению с доступом к буферу) может повысить производительность для произвольно индексированных данных.</span><span class="sxs-lookup"><span data-stu-id="c1f54-144">Texture access (as compared with buffer access) can have better performance for arbitrarily indexed data.</span></span> <span data-ttu-id="c1f54-145">Для каждого этапа конвейера можно привязать до 128 буферов текстуры.</span><span class="sxs-lookup"><span data-stu-id="c1f54-145">You can bind up to 128 texture buffers per pipeline stage.</span></span>

<span data-ttu-id="c1f54-146">Ресурс буфера предназначен для снижения издержек на установку констант шейдера.</span><span class="sxs-lookup"><span data-stu-id="c1f54-146">A buffer resource is designed to minimize the overhead of setting shader constants.</span></span> <span data-ttu-id="c1f54-147">Платформа эффектов (см. [**интерфейс ID3D10Effect**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) будет управлять обновлением буферов констант и текстур, а также использовать API Direct3D для обновления буферов (см. Дополнительные сведения о [копировании и доступе к данным ресурсов (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) ).</span><span class="sxs-lookup"><span data-stu-id="c1f54-147">The effect framework (see [**ID3D10Effect Interface**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) will manage updating constant and texture buffers, or you can use the Direct3D API to update buffers (see [Copying and Accessing Resource Data (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) for information).</span></span> <span data-ttu-id="c1f54-148">Приложение также может копировать данные из другого буфера (например, целевого объекта прорисовки или целевого объекта вывода потока) в буфер констант.</span><span class="sxs-lookup"><span data-stu-id="c1f54-148">An application can also copy data from another buffer (such as a render target or a stream-output target) into a constant buffer.</span></span>

<span data-ttu-id="c1f54-149">Дополнительные сведения об использовании буферов констант в приложении D3D10 см. в разделе [типы ресурсов (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) и [Создание ресурсов буфера (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span><span class="sxs-lookup"><span data-stu-id="c1f54-149">For more info on using constant buffers in a D3D10 application, see [Resource Types (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) and [Creating Buffer Resources (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span></span>

<span data-ttu-id="c1f54-150">Сведения о том, как использовать буферы констант в приложении D3D11, см. в статьях [Введение в буферы в Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) и [инструкции: Создание буфера констант](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span><span class="sxs-lookup"><span data-stu-id="c1f54-150">For morel info on using constant buffers in a D3D11 application, see [Introduction to Buffers in Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) and [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="c1f54-151">Для буфера констант не требуется, чтобы [представление](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) было привязано к конвейеру.</span><span class="sxs-lookup"><span data-stu-id="c1f54-151">A constant buffer does not require a [view](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) to be bound to the pipeline.</span></span> <span data-ttu-id="c1f54-152">Буфер текстуры, однако, требует представления и должен быть привязан к слоту текстуры (или должен быть связан с [**сеттекстуребуффер**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) при использовании этого действия).</span><span class="sxs-lookup"><span data-stu-id="c1f54-152">A texture buffer, however, requires a view and must be bound to a texture slot (or must be bound with [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) when using an effect).</span></span>

<span data-ttu-id="c1f54-153">Существует два способа упаковки данных с константами: с помощью ключевых слов [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) и [ПАККОФФСЕТ (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .</span><span class="sxs-lookup"><span data-stu-id="c1f54-153">There are two ways to pack constants data: using the [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) and [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) keywords.</span></span>

<span data-ttu-id="c1f54-154">Различия между Direct3D 9 и Direct3D 10 и 11:</span><span class="sxs-lookup"><span data-stu-id="c1f54-154">Differences between Direct3D 9 and Direct3D 10 and 11:</span></span>

- <span data-ttu-id="c1f54-155">В отличие от автоматического выделения констант в Direct3D 9, которые не выполняли упаковку и назначают каждую переменную набору регистров float4, переменные константы HLSL следуют правилам упаковки в Direct3D 10 и 11.</span><span class="sxs-lookup"><span data-stu-id="c1f54-155">Unlike the auto-allocation of constants in Direct3D 9, which did not perform packing and instead assigned each variable to a set of float4 registers, HLSL constant variables follow packing rules in Direct3D 10 and 11.</span></span>



 

### <a name="organizing-constant-buffers"></a><span data-ttu-id="c1f54-156">Организация постоянных буферов</span><span class="sxs-lookup"><span data-stu-id="c1f54-156">Organizing constant buffers</span></span>

<span data-ttu-id="c1f54-157">Буферы констант уменьшают пропускную способность, необходимую для обновления констант шейдера, позволяя сгруппировать и обработать их одновременно, без отдельных вызовов для обработки каждой константы.</span><span class="sxs-lookup"><span data-stu-id="c1f54-157">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="c1f54-158">Лучшим способом эффективного использования буферов констант является упорядочение переменных шейдера в буферах констант согласно частоте их обновления.</span><span class="sxs-lookup"><span data-stu-id="c1f54-158">The best way to efficiently use constant buffers is to organize shader variables into constant buffers based on their frequency of update.</span></span> <span data-ttu-id="c1f54-159">Это позволяет приложению максимально снизить пропускную способность, необходимую для обновления констант шейдера.</span><span class="sxs-lookup"><span data-stu-id="c1f54-159">This allows an application to minimize the bandwidth required for updating shader constants.</span></span> <span data-ttu-id="c1f54-160">Например, шейдер может объявлять два буфера констант и упорядочивать данные по частоте обновления: данные, которые необходимо обновить для каждого объекта (например, матрица мира), группируются в буфер констант, который может быть обновлен для каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="c1f54-160">For example, a shader might declare two constant buffers and organize the data in each based on their frequency of update: data that needs to be updated on a per-object basis (like a world matrix) is grouped into a constant buffer which could be updated for each object.</span></span> <span data-ttu-id="c1f54-161">Это отдельно от данных, которые характеризуют сцену и, следовательно, часто обновляются гораздо реже (при изменении сцены).</span><span class="sxs-lookup"><span data-stu-id="c1f54-161">This is separate from data that characterizes a scene and is therefore likely to be updated much less often (when the scene changes).</span></span>


```
cbuffer myObject
{       
    float4x4 matWorld;
    float3   vObjectPosition;
    int      arrayIndex;
}
 
cbuffer myScene
{
    float3   vSunPosition;
    float4x4 matView;
}
        
```



### <a name="default-constant-buffers"></a><span data-ttu-id="c1f54-162">Буферы констант по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c1f54-162">Default constant buffers</span></span>

<span data-ttu-id="c1f54-163">Доступны два буфера констант по умолчанию: $Global и $Param.</span><span class="sxs-lookup"><span data-stu-id="c1f54-163">There are two default constant buffers available, $Global and $Param.</span></span> <span data-ttu-id="c1f54-164">Переменные, помещаемые в глобальную область, добавляются неявно в $Global кбуффер с использованием того же метода упаковки, который используется для cbuffer.</span><span class="sxs-lookup"><span data-stu-id="c1f54-164">Variables that are placed in the global scope are added implicitly to the $Global cbuffer, using the same packing method that is used for cbuffers.</span></span> <span data-ttu-id="c1f54-165">Универсальные параметры в списке параметров функции отображаются в буфере констант $Param, когда шейдер компилируется за пределами платформы Effects.</span><span class="sxs-lookup"><span data-stu-id="c1f54-165">Uniform parameters in the parameter list of a function appear in the $Param constant buffer when a shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="c1f54-166">При компиляции внутри платформы Effects все универсальные значения должны разрешаться в переменные, определенные в глобальной области.</span><span class="sxs-lookup"><span data-stu-id="c1f54-166">When compiled inside the effects framework, all uniforms must resolve to variables defined in the global scope.</span></span>

## <a name="examples"></a><span data-ttu-id="c1f54-167">Примеры</span><span class="sxs-lookup"><span data-stu-id="c1f54-167">Examples</span></span>

<span data-ttu-id="c1f54-168">Ниже приведен пример из [примера Skinning10](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) , который представляет собой буфер текстуры, состоящие из массива матриц.</span><span class="sxs-lookup"><span data-stu-id="c1f54-168">Here is an example from [Skinning10 Sample](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) that is a texture buffer made up of an array of matrices.</span></span>


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



<span data-ttu-id="c1f54-169">В этом примере объявление вручную назначает буфер константы для запуска с определенным регистром, а также упаковывает определенные элементы по подкомпонентам.</span><span class="sxs-lookup"><span data-stu-id="c1f54-169">This example declaration manually assigns a constant buffer to start at a particular register, and also packs particular elements by subcomponents.</span></span>


```
cbuffer MyBuffer : register(b3)
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
      
```



## <a name="related-topics"></a><span data-ttu-id="c1f54-170">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="c1f54-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1f54-171">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="c1f54-171">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

