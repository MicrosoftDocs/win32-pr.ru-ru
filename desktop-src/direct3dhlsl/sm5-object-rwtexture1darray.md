---
title: RWTexture1DArray
description: Ресурс, доступный для чтения и записи. | RWTexture1DArray
ms.assetid: 214c7e7d-4e74-4f4f-bf78-98e9df0b3a0e
keywords:
- RWTexture1DArray HLSL
topic_type:
- apiref
api_name:
- RWTexture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7f6841cb1f15b12c9755da2a9fae50e42ed333
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000179"
---
# <a name="rwtexture1darray"></a><span data-ttu-id="26da0-105">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="26da0-105">RWTexture1DArray</span></span>

<span data-ttu-id="26da0-106">Ресурс, доступный для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="26da0-106">A read/write resource.</span></span>



| <span data-ttu-id="26da0-107">Метод</span><span class="sxs-lookup"><span data-stu-id="26da0-107">Method</span></span>                                                             | <span data-ttu-id="26da0-108">Описание</span><span class="sxs-lookup"><span data-stu-id="26da0-108">Description</span></span>                   |
|--------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="26da0-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="26da0-109">**GetDimensions**</span></span>](sm5-object-rwtexture1darray-getdimensions.md) | <span data-ttu-id="26da0-110">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="26da0-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="26da0-111">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="26da0-111">**Load**</span></span>](rwtexture1darray-load.md)                              | <span data-ttu-id="26da0-112">Считывает данные текстуры.</span><span class="sxs-lookup"><span data-stu-id="26da0-112">Reads texture data.</span></span>           |
| <span data-ttu-id="26da0-113">[**Оператор\[\]**](sm5-object-rwtexture1darray-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="26da0-113">[**Operator\[\]**](sm5-object-rwtexture1darray-operatorindex.md)</span></span>  | <span data-ttu-id="26da0-114">Возвращает переменную ресурса.</span><span class="sxs-lookup"><span data-stu-id="26da0-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="26da0-115">Можно добавить префикс для объектов **RWTexture1DArray** с классом хранения **глобалликохерент**.</span><span class="sxs-lookup"><span data-stu-id="26da0-115">You can prefix **RWTexture1DArray** objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="26da0-116">Этот класс хранения вызывает барьеры памяти и выполняет синхронизацию для очистки данных во всем GPU, так что другие группы могут видеть операции записи.</span><span class="sxs-lookup"><span data-stu-id="26da0-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="26da0-117">Без этого описателя барьер памяти или синхронизация будут сбрасывать UAV только в пределах текущей группы.</span><span class="sxs-lookup"><span data-stu-id="26da0-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="26da0-118">Для объекта **RWTexture1DArray** требуется тип элемента в операторе объявления для объекта.</span><span class="sxs-lookup"><span data-stu-id="26da0-118">A **RWTexture1DArray** object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="26da0-119">Например, следующее объявление верно:</span><span class="sxs-lookup"><span data-stu-id="26da0-119">For example, the following declaration is correct:</span></span>


```
RWTexture1DArray<float> tex;
```



<span data-ttu-id="26da0-120">Так как объект **RWTexture1DArray** является объектом UAV, его свойства отличаются от объекта типа представления ресурсов шейдера (SRV), такого как объект [**Texture1DArray**](sm5-object-texture1darray.md) .</span><span class="sxs-lookup"><span data-stu-id="26da0-120">Because a **RWTexture1DArray** object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [**Texture1DArray**](sm5-object-texture1darray.md) object.</span></span> <span data-ttu-id="26da0-121">Например, можно выполнять чтение из объекта **RWTexture1DArray** и запись в него, но можно только считывать объект **Texture1DArray** .</span><span class="sxs-lookup"><span data-stu-id="26da0-121">For example, you can read from and write to a **RWTexture1DArray** object, but you can only read from a **Texture1DArray** object.</span></span>

<span data-ttu-id="26da0-122">Объект **RWTexture1DArray** не может использовать методы из объекта [**Texture1DArray**](sm5-object-texture1darray.md) , например [Sample](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="26da0-122">A **RWTexture1DArray** object cannot use methods from a [**Texture1DArray**](sm5-object-texture1darray.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="26da0-123">Однако, поскольку можно создать несколько типов представлений для одного и того же ресурса, можно объявить несколько типов текстур как одну текстуру в нескольких шейдерах.</span><span class="sxs-lookup"><span data-stu-id="26da0-123">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="26da0-124">Например, можно объявить и использовать объект **RWTexture1DArray** как *Да* в шейдере вычислений, а затем объявить и использовать объект **Texture1DArray** как *Да* в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="26da0-124">For example, you can declare and use a **RWTexture1DArray** object as *tex* in a compute shader and then declare and use a **Texture1DArray** object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="26da0-125">Среда выполнения применяет определенные шаблоны использования при создании нескольких типов представлений для одного и того же ресурса.</span><span class="sxs-lookup"><span data-stu-id="26da0-125">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="26da0-126">Например, среда выполнения не позволяет одновременно использовать сопоставление UAV для ресурса и сопоставление SRV для одного и того же ресурса.</span><span class="sxs-lookup"><span data-stu-id="26da0-126">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="26da0-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="26da0-127">Minimum Shader Model</span></span>

<span data-ttu-id="26da0-128">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="26da0-128">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="26da0-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="26da0-129">Shader Model</span></span>                                                                | <span data-ttu-id="26da0-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="26da0-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="26da0-131">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="26da0-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="26da0-132">да</span><span class="sxs-lookup"><span data-stu-id="26da0-132">yes</span></span>       |



 

<span data-ttu-id="26da0-133">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="26da0-133">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="26da0-134">Вершина</span><span class="sxs-lookup"><span data-stu-id="26da0-134">Vertex</span></span> | <span data-ttu-id="26da0-135">Поверхности</span><span class="sxs-lookup"><span data-stu-id="26da0-135">Hull</span></span> | <span data-ttu-id="26da0-136">Домен</span><span class="sxs-lookup"><span data-stu-id="26da0-136">Domain</span></span> | <span data-ttu-id="26da0-137">Геометрия</span><span class="sxs-lookup"><span data-stu-id="26da0-137">Geometry</span></span> | <span data-ttu-id="26da0-138">Пиксель</span><span class="sxs-lookup"><span data-stu-id="26da0-138">Pixel</span></span> | <span data-ttu-id="26da0-139">Вычисления</span><span class="sxs-lookup"><span data-stu-id="26da0-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="26da0-140">x</span><span class="sxs-lookup"><span data-stu-id="26da0-140">x</span></span>     | <span data-ttu-id="26da0-141">x</span><span class="sxs-lookup"><span data-stu-id="26da0-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="26da0-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26da0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26da0-143">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="26da0-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




