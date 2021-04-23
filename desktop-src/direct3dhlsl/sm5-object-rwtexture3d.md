---
title: RWTexture3D
description: Ресурс, доступный для чтения и записи. | RWTexture3D
ms.assetid: 4d02810e-4f3c-4b20-b057-0ff27d6732b5
keywords:
- RWTexture3D HLSL
topic_type:
- apiref
api_name:
- RWTexture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b89ed7ff724eabef9fc2b2757c6ac0e5272c69e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352672"
---
# <a name="rwtexture3d"></a><span data-ttu-id="08a82-105">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="08a82-105">RWTexture3D</span></span>

<span data-ttu-id="08a82-106">Ресурс, доступный для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="08a82-106">A read/write resource.</span></span>



| <span data-ttu-id="08a82-107">Метод</span><span class="sxs-lookup"><span data-stu-id="08a82-107">Method</span></span>                                                        | <span data-ttu-id="08a82-108">Описание</span><span class="sxs-lookup"><span data-stu-id="08a82-108">Description</span></span>                   |
|---------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="08a82-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="08a82-109">**GetDimensions**</span></span>](sm5-object-rwtexture3d-getdimensions.md) | <span data-ttu-id="08a82-110">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="08a82-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="08a82-111">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="08a82-111">**Load**</span></span>](rwtexture3d-load.md)                              | <span data-ttu-id="08a82-112">Считывает данные текстуры.</span><span class="sxs-lookup"><span data-stu-id="08a82-112">Reads texture data.</span></span>           |
| <span data-ttu-id="08a82-113">[**Оператор\[\]**](sm5-object-rwtexture3d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="08a82-113">[**Operator\[\]**](sm5-object-rwtexture3d-operatorindex.md)</span></span>  | <span data-ttu-id="08a82-114">Возвращает переменную ресурса.</span><span class="sxs-lookup"><span data-stu-id="08a82-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="08a82-115">Можно добавить префикс для объектов **RWTexture3D** с классом хранения **глобалликохерент**.</span><span class="sxs-lookup"><span data-stu-id="08a82-115">You can prefix **RWTexture3D** objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="08a82-116">Этот класс хранения вызывает барьеры памяти и выполняет синхронизацию для очистки данных во всем GPU, так что другие группы могут видеть операции записи.</span><span class="sxs-lookup"><span data-stu-id="08a82-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="08a82-117">Без этого описателя барьер памяти или синхронизация будут сбрасывать UAV только в пределах текущей группы.</span><span class="sxs-lookup"><span data-stu-id="08a82-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="08a82-118">Для объекта **RWTexture3D** требуется тип элемента в операторе объявления для объекта.</span><span class="sxs-lookup"><span data-stu-id="08a82-118">A **RWTexture3D** object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="08a82-119">Например, следующее объявление верно:</span><span class="sxs-lookup"><span data-stu-id="08a82-119">For example, the following declaration is correct:</span></span>


```
RWTexture3D<float> tex;
```



<span data-ttu-id="08a82-120">Так как объект **RWTexture3D** является объектом UAV, его свойства отличаются от объекта типа представления ресурсов шейдера (SRV), такого как объект [**Texture3D**](sm5-object-texture3d.md) .</span><span class="sxs-lookup"><span data-stu-id="08a82-120">Because a **RWTexture3D** object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [**Texture3D**](sm5-object-texture3d.md) object.</span></span> <span data-ttu-id="08a82-121">Например, можно выполнять чтение из объекта **RWTexture3D** и запись в него, но можно только считывать объект **Texture3D** .</span><span class="sxs-lookup"><span data-stu-id="08a82-121">For example, you can read from and write to a **RWTexture3D** object, but you can only read from a **Texture3D** object.</span></span>

<span data-ttu-id="08a82-122">Объект **RWTexture3D** не может использовать методы из объекта [**Texture3D**](sm5-object-texture3d.md) , например [Sample](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="08a82-122">A **RWTexture3D** object cannot use methods from a [**Texture3D**](sm5-object-texture3d.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="08a82-123">Однако, поскольку можно создать несколько типов представлений для одного и того же ресурса, можно объявить несколько типов текстур как одну текстуру в нескольких шейдерах.</span><span class="sxs-lookup"><span data-stu-id="08a82-123">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="08a82-124">Например, можно объявить и использовать объект **RWTexture3D** как *Да* в шейдере вычислений, а затем объявить и использовать объект **Texture3D** как *Да* в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="08a82-124">For example, you can declare and use a **RWTexture3D** object as *tex* in a compute shader and then declare and use a **Texture3D** object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="08a82-125">Среда выполнения применяет определенные шаблоны использования при создании нескольких типов представлений для одного и того же ресурса.</span><span class="sxs-lookup"><span data-stu-id="08a82-125">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="08a82-126">Например, среда выполнения не позволяет одновременно использовать сопоставление UAV для ресурса и сопоставление SRV для одного и того же ресурса.</span><span class="sxs-lookup"><span data-stu-id="08a82-126">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="08a82-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="08a82-127">Minimum Shader Model</span></span>

<span data-ttu-id="08a82-128">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="08a82-128">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="08a82-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="08a82-129">Shader Model</span></span>                                                                | <span data-ttu-id="08a82-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="08a82-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="08a82-131">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="08a82-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="08a82-132">да</span><span class="sxs-lookup"><span data-stu-id="08a82-132">yes</span></span>       |



 

<span data-ttu-id="08a82-133">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="08a82-133">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="08a82-134">Вершина</span><span class="sxs-lookup"><span data-stu-id="08a82-134">Vertex</span></span> | <span data-ttu-id="08a82-135">Поверхности</span><span class="sxs-lookup"><span data-stu-id="08a82-135">Hull</span></span> | <span data-ttu-id="08a82-136">Домен</span><span class="sxs-lookup"><span data-stu-id="08a82-136">Domain</span></span> | <span data-ttu-id="08a82-137">Геометрия</span><span class="sxs-lookup"><span data-stu-id="08a82-137">Geometry</span></span> | <span data-ttu-id="08a82-138">Пиксель</span><span class="sxs-lookup"><span data-stu-id="08a82-138">Pixel</span></span> | <span data-ttu-id="08a82-139">Вычисления</span><span class="sxs-lookup"><span data-stu-id="08a82-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="08a82-140">x</span><span class="sxs-lookup"><span data-stu-id="08a82-140">x</span></span>     | <span data-ttu-id="08a82-141">x</span><span class="sxs-lookup"><span data-stu-id="08a82-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="08a82-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08a82-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a82-143">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="08a82-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




