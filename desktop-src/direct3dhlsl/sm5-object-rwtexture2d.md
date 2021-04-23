---
title: RWTexture2D
description: Ресурс, доступный для чтения и записи. | RWTexture2D
ms.assetid: 19b383f1-c787-4c20-b77a-60ef9f212b9f
keywords:
- RWTexture2D HLSL
topic_type:
- apiref
api_name:
- RWTexture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccdeae4dd47d3ad4bf5d756c2ca362033eae6814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352972"
---
# <a name="rwtexture2d"></a><span data-ttu-id="8a7e2-105">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="8a7e2-105">RWTexture2D</span></span>

<span data-ttu-id="8a7e2-106">Ресурс, доступный для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="8a7e2-106">A read/write resource.</span></span>



| <span data-ttu-id="8a7e2-107">Метод</span><span class="sxs-lookup"><span data-stu-id="8a7e2-107">Method</span></span>                                                        | <span data-ttu-id="8a7e2-108">Описание</span><span class="sxs-lookup"><span data-stu-id="8a7e2-108">Description</span></span>                   |
|---------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="8a7e2-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="8a7e2-109">**GetDimensions**</span></span>](sm5-object-rwtexture2d-getdimensions.md) | <span data-ttu-id="8a7e2-110">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a7e2-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="8a7e2-111">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="8a7e2-111">**Load**</span></span>](rwtexture2d-load.md)                              | <span data-ttu-id="8a7e2-112">Считывает данные текстуры.</span><span class="sxs-lookup"><span data-stu-id="8a7e2-112">Reads texture data.</span></span>           |
| <span data-ttu-id="8a7e2-113">[**Оператор\[\]**](sm5-object-rwtexture2d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="8a7e2-113">[**Operator\[\]**](sm5-object-rwtexture2d-operatorindex.md)</span></span>  | <span data-ttu-id="8a7e2-114">Возвращает переменную ресурса.</span><span class="sxs-lookup"><span data-stu-id="8a7e2-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="8a7e2-115">Можно добавить префикс для объектов RWTexture2D с классом хранения **глобалликохерент**.</span><span class="sxs-lookup"><span data-stu-id="8a7e2-115">You can prefix RWTexture2D objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="8a7e2-116">Этот класс хранения вызывает барьеры памяти и выполняет синхронизацию для очистки данных во всем GPU, так что другие группы могут видеть операции записи.</span><span class="sxs-lookup"><span data-stu-id="8a7e2-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="8a7e2-117">Без этого описателя барьер памяти или синхронизация выполнит очистку только неупорядоченного представления доступа (UAV) в текущей группе.</span><span class="sxs-lookup"><span data-stu-id="8a7e2-117">Without this specifier, a memory barrier or sync will flush only an unordered access view (UAV) within the current group.</span></span>

<span data-ttu-id="8a7e2-118">Для объекта RWTexture2D требуется тип элемента в операторе объявления для объекта.</span><span class="sxs-lookup"><span data-stu-id="8a7e2-118">A RWTexture2D object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="8a7e2-119">Например, следующее объявление является неправильным:</span><span class="sxs-lookup"><span data-stu-id="8a7e2-119">For example, the following declaration is not correct:</span></span>


```
// The following declaration is incorrectly coded.
RWTexture2D myTexture;
```



<span data-ttu-id="8a7e2-120">Следующее объявление верно:</span><span class="sxs-lookup"><span data-stu-id="8a7e2-120">The following declaration is correct:</span></span>


```
// The following declaration is correctly coded.
RWTexture2D<float> tex;
```



<span data-ttu-id="8a7e2-121">Так как объект RWTexture2D является объектом UAV, его свойства отличаются от объекта типа представления ресурсов шейдера (SRV), такого как объект [Texture2D](sm5-object-texture2d.md) .</span><span class="sxs-lookup"><span data-stu-id="8a7e2-121">Because a RWTexture2D object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [Texture2D](sm5-object-texture2d.md) object.</span></span> <span data-ttu-id="8a7e2-122">Например, можно выполнять чтение из объекта RWTexture2D и запись в него, но можно только считывать объект Texture2D.</span><span class="sxs-lookup"><span data-stu-id="8a7e2-122">For example, you can read from and write to a RWTexture2D object, but you can only read from a Texture2D object.</span></span>

<span data-ttu-id="8a7e2-123">Объект RWTexture2D не может использовать методы из объекта [Texture2D](sm5-object-texture2d.md) , например [Sample](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="8a7e2-123">A RWTexture2D object cannot use methods from a [Texture2D](sm5-object-texture2d.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="8a7e2-124">Однако, поскольку можно создать несколько типов представлений для одного и того же ресурса, можно объявить несколько типов текстур как одну текстуру в нескольких шейдерах.</span><span class="sxs-lookup"><span data-stu-id="8a7e2-124">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="8a7e2-125">Например, в следующих фрагментах кода показано, как можно объявить и использовать объект RWTexture2D как *Да* в шейдере вычислений, а затем объявить и использовать объект Texture2D как *Да* в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="8a7e2-125">For example, the following code snippets show how you can declare and use a RWTexture2D object as *tex* in a compute shader and then declare and use a Texture2D object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="8a7e2-126">Среда выполнения применяет определенные шаблоны использования при создании нескольких типов представлений для одного и того же ресурса.</span><span class="sxs-lookup"><span data-stu-id="8a7e2-126">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="8a7e2-127">Например, среда выполнения не позволяет одновременно использовать сопоставление UAV для ресурса и сопоставление SRV для одного и того же ресурса.</span><span class="sxs-lookup"><span data-stu-id="8a7e2-127">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

<span data-ttu-id="8a7e2-128">Следующий код предназначен для вычислений с шейдером:</span><span class="sxs-lookup"><span data-stu-id="8a7e2-128">The following code is for the compute shader:</span></span>


```
RWTexture2D<float> tex;
[numthreads(groupDim_x, groupDim_y, 1)]
void main(
    uint3 groupId : SV_GroupID,
    uint3 groupThreadId : SV_GroupThreadID,
    uint3 dispatchThreadId : SV_DispatchThreadID,
    uint groupIndex : SV_GroupIndex)
{
    tex [dispatchThreadId.xy] = <something>;
}
```



<span data-ttu-id="8a7e2-129">Следующий код предназначен для построителя текстуры:</span><span class="sxs-lookup"><span data-stu-id="8a7e2-129">The following code is for the pixel shader:</span></span>


```
struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float2 tex : TEXTURE;
};

Texture2D<float> tex;
float4 main(PixelShaderInput input) : SV_TARGET
{
    return tex.Sample(TextureSampler, input.tex);
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="8a7e2-130">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8a7e2-130">Minimum Shader Model</span></span>

<span data-ttu-id="8a7e2-131">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="8a7e2-131">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="8a7e2-132">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8a7e2-132">Shader Model</span></span>                                                                | <span data-ttu-id="8a7e2-133">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8a7e2-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8a7e2-134">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="8a7e2-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="8a7e2-135">да</span><span class="sxs-lookup"><span data-stu-id="8a7e2-135">yes</span></span>       |



 

<span data-ttu-id="8a7e2-136">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="8a7e2-136">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8a7e2-137">Вершина</span><span class="sxs-lookup"><span data-stu-id="8a7e2-137">Vertex</span></span> | <span data-ttu-id="8a7e2-138">Поверхности</span><span class="sxs-lookup"><span data-stu-id="8a7e2-138">Hull</span></span> | <span data-ttu-id="8a7e2-139">Домен</span><span class="sxs-lookup"><span data-stu-id="8a7e2-139">Domain</span></span> | <span data-ttu-id="8a7e2-140">Геометрия</span><span class="sxs-lookup"><span data-stu-id="8a7e2-140">Geometry</span></span> | <span data-ttu-id="8a7e2-141">Пиксель</span><span class="sxs-lookup"><span data-stu-id="8a7e2-141">Pixel</span></span> | <span data-ttu-id="8a7e2-142">Вычисления</span><span class="sxs-lookup"><span data-stu-id="8a7e2-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8a7e2-143">x</span><span class="sxs-lookup"><span data-stu-id="8a7e2-143">x</span></span>     | <span data-ttu-id="8a7e2-144">x</span><span class="sxs-lookup"><span data-stu-id="8a7e2-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8a7e2-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a7e2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a7e2-146">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="8a7e2-146">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




