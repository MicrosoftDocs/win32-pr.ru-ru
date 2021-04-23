---
title: RWTexture2DArray
description: Ресурс, доступный для чтения и записи. | RWTexture2DArray
ms.assetid: 6a6f3655-f1c0-4d5b-91a2-d79da65858b8
keywords:
- RWTexture2DArray HLSL
topic_type:
- apiref
api_name:
- RWTexture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ada0fcaba729eff37f41f1ae7666841175689ff
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986421"
---
# <a name="rwtexture2darray"></a><span data-ttu-id="ec6b7-105">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="ec6b7-105">RWTexture2DArray</span></span>

<span data-ttu-id="ec6b7-106">Ресурс, доступный для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ec6b7-106">A read/write resource.</span></span>



| <span data-ttu-id="ec6b7-107">Метод</span><span class="sxs-lookup"><span data-stu-id="ec6b7-107">Method</span></span>                                                             | <span data-ttu-id="ec6b7-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ec6b7-108">Description</span></span>                   |
|--------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="ec6b7-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="ec6b7-109">**GetDimensions**</span></span>](sm5-object-rwtexture2darray-getdimensions.md) | <span data-ttu-id="ec6b7-110">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ec6b7-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="ec6b7-111">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="ec6b7-111">**Load**</span></span>](rwtexture2darray-load.md)                              | <span data-ttu-id="ec6b7-112">Считывает данные текстуры.</span><span class="sxs-lookup"><span data-stu-id="ec6b7-112">Reads texture data.</span></span>           |
| <span data-ttu-id="ec6b7-113">[**Оператор\[\]**](sm5-object-rwtexture2darray-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="ec6b7-113">[**Operator\[\]**](sm5-object-rwtexture2darray-operatorindex.md)</span></span>  | <span data-ttu-id="ec6b7-114">Возвращает переменную ресурса.</span><span class="sxs-lookup"><span data-stu-id="ec6b7-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="ec6b7-115">Можно добавить префикс для объектов **RWTexture2DArray** с классом хранения **глобалликохерент**.</span><span class="sxs-lookup"><span data-stu-id="ec6b7-115">You can prefix **RWTexture2DArray** objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="ec6b7-116">Этот класс хранения вызывает барьеры памяти и выполняет синхронизацию для очистки данных во всем GPU, так что другие группы могут видеть операции записи.</span><span class="sxs-lookup"><span data-stu-id="ec6b7-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="ec6b7-117">Без этого описателя барьер памяти или синхронизация будут сбрасывать UAV только в пределах текущей группы.</span><span class="sxs-lookup"><span data-stu-id="ec6b7-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="ec6b7-118">Для объекта **RWTexture2DArray** требуется тип элемента в операторе объявления для объекта.</span><span class="sxs-lookup"><span data-stu-id="ec6b7-118">A **RWTexture2DArray** object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="ec6b7-119">Например, следующее объявление верно:</span><span class="sxs-lookup"><span data-stu-id="ec6b7-119">For example, the following declaration is correct:</span></span>


```
RWTexture2DArray<float> tex;
```



<span data-ttu-id="ec6b7-120">Так как объект **RWTexture2DArray** является объектом UAV, его свойства отличаются от объекта типа представления ресурсов шейдера (SRV), такого как объект [**Texture2DArray**](sm5-object-texture2darray.md) .</span><span class="sxs-lookup"><span data-stu-id="ec6b7-120">Because a **RWTexture2DArray** object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [**Texture2DArray**](sm5-object-texture2darray.md) object.</span></span> <span data-ttu-id="ec6b7-121">Например, можно выполнять чтение из объекта **RWTexture2DArray** и запись в него, но можно только считывать объект **Texture2DArray** .</span><span class="sxs-lookup"><span data-stu-id="ec6b7-121">For example, you can read from and write to a **RWTexture2DArray** object, but you can only read from a **Texture2DArray** object.</span></span>

<span data-ttu-id="ec6b7-122">Объект **RWTexture2DArray** не может использовать методы из объекта [**Texture2DArray**](sm5-object-texture2darray.md) , например [Sample](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="ec6b7-122">A **RWTexture2DArray** object cannot use methods from a [**Texture2DArray**](sm5-object-texture2darray.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="ec6b7-123">Однако, поскольку можно создать несколько типов представлений для одного и того же ресурса, можно объявить несколько типов текстур как одну текстуру в нескольких шейдерах.</span><span class="sxs-lookup"><span data-stu-id="ec6b7-123">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="ec6b7-124">Например, можно объявить и использовать объект **RWTexture2DArray** как *Да* в шейдере вычислений, а затем объявить и использовать объект **Texture2DArray** как *Да* в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="ec6b7-124">For example, you can declare and use a **RWTexture2DArray** object as *tex* in a compute shader and then declare and use a **Texture2DArray** object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="ec6b7-125">Среда выполнения применяет определенные шаблоны использования при создании нескольких типов представлений для одного и того же ресурса.</span><span class="sxs-lookup"><span data-stu-id="ec6b7-125">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="ec6b7-126">Например, среда выполнения не позволяет одновременно использовать сопоставление UAV для ресурса и сопоставление SRV для одного и того же ресурса.</span><span class="sxs-lookup"><span data-stu-id="ec6b7-126">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="ec6b7-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ec6b7-127">Minimum Shader Model</span></span>

<span data-ttu-id="ec6b7-128">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="ec6b7-128">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="ec6b7-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ec6b7-129">Shader Model</span></span>                                                                | <span data-ttu-id="ec6b7-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ec6b7-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ec6b7-131">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="ec6b7-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="ec6b7-132">да</span><span class="sxs-lookup"><span data-stu-id="ec6b7-132">yes</span></span>       |



 

<span data-ttu-id="ec6b7-133">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ec6b7-133">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ec6b7-134">Вершина</span><span class="sxs-lookup"><span data-stu-id="ec6b7-134">Vertex</span></span> | <span data-ttu-id="ec6b7-135">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ec6b7-135">Hull</span></span> | <span data-ttu-id="ec6b7-136">Домен</span><span class="sxs-lookup"><span data-stu-id="ec6b7-136">Domain</span></span> | <span data-ttu-id="ec6b7-137">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ec6b7-137">Geometry</span></span> | <span data-ttu-id="ec6b7-138">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ec6b7-138">Pixel</span></span> | <span data-ttu-id="ec6b7-139">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ec6b7-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ec6b7-140">x</span><span class="sxs-lookup"><span data-stu-id="ec6b7-140">x</span></span>     | <span data-ttu-id="ec6b7-141">x</span><span class="sxs-lookup"><span data-stu-id="ec6b7-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ec6b7-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec6b7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec6b7-143">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="ec6b7-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




