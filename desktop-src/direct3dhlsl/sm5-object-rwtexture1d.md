---
title: RWTexture1D
description: Ресурс, доступный для чтения и записи. | RWTexture1D
ms.assetid: 47866e5a-b26b-4264-9291-c8940882d662
keywords:
- RWTexture1D HLSL
topic_type:
- apiref
api_name:
- RWTexture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 695b73cc14541505ee1b2d4391aac2d145eec8d7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986236"
---
# <a name="rwtexture1d"></a><span data-ttu-id="1ce2e-105">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="1ce2e-105">RWTexture1D</span></span>

<span data-ttu-id="1ce2e-106">Ресурс, доступный для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1ce2e-106">A read/write resource.</span></span>



| <span data-ttu-id="1ce2e-107">Метод</span><span class="sxs-lookup"><span data-stu-id="1ce2e-107">Method</span></span>                                                        | <span data-ttu-id="1ce2e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="1ce2e-108">Description</span></span>                   |
|---------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="1ce2e-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="1ce2e-109">**GetDimensions**</span></span>](sm5-object-rwtexture1d-getdimensions.md) | <span data-ttu-id="1ce2e-110">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1ce2e-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="1ce2e-111">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="1ce2e-111">**Load**</span></span>](rwtexture1d-load.md)                              | <span data-ttu-id="1ce2e-112">Считывает данные текстуры.</span><span class="sxs-lookup"><span data-stu-id="1ce2e-112">Reads texture data.</span></span>           |
| <span data-ttu-id="1ce2e-113">[**Оператор\[\]**](sm5-object-rwtexture1d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="1ce2e-113">[**Operator\[\]**](sm5-object-rwtexture1d-operatorindex.md)</span></span>  | <span data-ttu-id="1ce2e-114">Возвращает переменную ресурса.</span><span class="sxs-lookup"><span data-stu-id="1ce2e-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="1ce2e-115">Можно добавить префикс для объектов **RWTexture1D** с классом хранения **глобалликохерент**.</span><span class="sxs-lookup"><span data-stu-id="1ce2e-115">You can prefix **RWTexture1D** objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="1ce2e-116">Этот класс хранения вызывает барьеры памяти и выполняет синхронизацию для очистки данных во всем GPU, так что другие группы могут видеть операции записи.</span><span class="sxs-lookup"><span data-stu-id="1ce2e-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="1ce2e-117">Без этого описателя барьер памяти или синхронизация будут сбрасывать UAV только в пределах текущей группы.</span><span class="sxs-lookup"><span data-stu-id="1ce2e-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="1ce2e-118">Для объекта **RWTexture1D** требуется тип элемента в операторе объявления для объекта.</span><span class="sxs-lookup"><span data-stu-id="1ce2e-118">A **RWTexture1D** object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="1ce2e-119">Например, следующее объявление верно:</span><span class="sxs-lookup"><span data-stu-id="1ce2e-119">For example, the following declaration is correct:</span></span>


```
RWTexture1D<float> tex;
```



<span data-ttu-id="1ce2e-120">Так как объект **RWTexture1D** является объектом UAV, его свойства отличаются от объекта типа представления ресурсов шейдера (SRV), такого как объект [**Texture1D**](sm5-object-texture1d.md) .</span><span class="sxs-lookup"><span data-stu-id="1ce2e-120">Because a **RWTexture1D** object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [**Texture1D**](sm5-object-texture1d.md) object.</span></span> <span data-ttu-id="1ce2e-121">Например, можно выполнять чтение из объекта **RWTexture1D** и запись в него, но можно только считывать объект **Texture1D** .</span><span class="sxs-lookup"><span data-stu-id="1ce2e-121">For example, you can read from and write to a **RWTexture1D** object, but you can only read from a **Texture1D** object.</span></span>

<span data-ttu-id="1ce2e-122">Объект **RWTexture1D** не может использовать методы из объекта [**Texture1D**](sm5-object-texture1d.md) , например [Sample](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="1ce2e-122">A **RWTexture1D** object cannot use methods from a [**Texture1D**](sm5-object-texture1d.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="1ce2e-123">Однако, поскольку можно создать несколько типов представлений для одного и того же ресурса, можно объявить несколько типов текстур как одну текстуру в нескольких шейдерах.</span><span class="sxs-lookup"><span data-stu-id="1ce2e-123">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="1ce2e-124">Например, можно объявить и использовать объект **RWTexture1D** как *Да* в шейдере вычислений, а затем объявить и использовать объект **Texture1D** как *Да* в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="1ce2e-124">For example, you can declare and use a **RWTexture1D** object as *tex* in a compute shader and then declare and use a **Texture1D** object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="1ce2e-125">Среда выполнения применяет определенные шаблоны использования при создании нескольких типов представлений для одного и того же ресурса.</span><span class="sxs-lookup"><span data-stu-id="1ce2e-125">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="1ce2e-126">Например, среда выполнения не позволяет одновременно использовать сопоставление UAV для ресурса и сопоставление SRV для одного и того же ресурса.</span><span class="sxs-lookup"><span data-stu-id="1ce2e-126">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="1ce2e-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1ce2e-127">Minimum Shader Model</span></span>

<span data-ttu-id="1ce2e-128">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="1ce2e-128">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="1ce2e-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1ce2e-129">Shader Model</span></span>                                                                | <span data-ttu-id="1ce2e-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="1ce2e-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="1ce2e-131">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="1ce2e-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="1ce2e-132">да</span><span class="sxs-lookup"><span data-stu-id="1ce2e-132">yes</span></span>       |



 

<span data-ttu-id="1ce2e-133">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="1ce2e-133">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1ce2e-134">Вершина</span><span class="sxs-lookup"><span data-stu-id="1ce2e-134">Vertex</span></span> | <span data-ttu-id="1ce2e-135">Поверхности</span><span class="sxs-lookup"><span data-stu-id="1ce2e-135">Hull</span></span> | <span data-ttu-id="1ce2e-136">Домен</span><span class="sxs-lookup"><span data-stu-id="1ce2e-136">Domain</span></span> | <span data-ttu-id="1ce2e-137">Геометрия</span><span class="sxs-lookup"><span data-stu-id="1ce2e-137">Geometry</span></span> | <span data-ttu-id="1ce2e-138">Пиксель</span><span class="sxs-lookup"><span data-stu-id="1ce2e-138">Pixel</span></span> | <span data-ttu-id="1ce2e-139">Вычисления</span><span class="sxs-lookup"><span data-stu-id="1ce2e-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1ce2e-140">x</span><span class="sxs-lookup"><span data-stu-id="1ce2e-140">x</span></span>     | <span data-ttu-id="1ce2e-141">x</span><span class="sxs-lookup"><span data-stu-id="1ce2e-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1ce2e-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ce2e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ce2e-143">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="1ce2e-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




