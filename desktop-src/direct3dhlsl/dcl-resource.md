---
title: dcl_resource (SM4-ASM)
description: '\_ресурс дкл (SM4-ASM)'
ms.assetid: 045610f0-f7db-4bf2-bfea-501bbee94601
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb65a8ea83feaf2fec80403fc9ac6c2ab38c1936
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103785007"
---
# <a name="dcl_resource-sm4---asm"></a><span data-ttu-id="e7f51-103">\_ресурс дкл (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="e7f51-103">dcl\_resource (sm4 - asm)</span></span>

<span data-ttu-id="e7f51-104">Объявляет многовыборочный источник данных шейдера.</span><span class="sxs-lookup"><span data-stu-id="e7f51-104">Declares a non-multisampled shader-input resource.</span></span>



| <span data-ttu-id="e7f51-105">дкл \_ Resource *тн*, *ResourceType*, *ReturnType (s)*</span><span class="sxs-lookup"><span data-stu-id="e7f51-105">dcl\_resource *tN*, *resourceType*, *returnType(s)*</span></span> |
|-----------------------------------------------------|



 

<span data-ttu-id="e7f51-106">Объявляет многовыборочный источник данных шейдера.</span><span class="sxs-lookup"><span data-stu-id="e7f51-106">Declares a multisampled shader-input resource.</span></span>



| <span data-ttu-id="e7f51-107">дкл \_ Resource *тн*, *ResourceType \[ size \] nn*, *ReturnType (s)*</span><span class="sxs-lookup"><span data-stu-id="e7f51-107">dcl\_resource *tN*, *resourceType\[size\]NN*, *returnType(s)*</span></span> |
|---------------------------------------------------------------|



 



| <span data-ttu-id="e7f51-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="e7f51-108">Item</span></span>                                                                                                                                                     | <span data-ttu-id="e7f51-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e7f51-109">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7f51-110"><span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*</span><span class="sxs-lookup"><span data-stu-id="e7f51-110"><span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*</span></span><br/>                                                                           | <span data-ttu-id="e7f51-111">\[в \] регистре текстуры, где *N* — это целое число, которое обозначает номер регистра.</span><span class="sxs-lookup"><span data-stu-id="e7f51-111">\[in\] The texture register, where *N* is an integer that denotes the register number.</span></span><br/>                                                                                                                                                                        |
| <span data-ttu-id="e7f51-112"><span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*resourceType*</span><span class="sxs-lookup"><span data-stu-id="e7f51-112"><span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*resourceType*</span></span><br/>                                   | <span data-ttu-id="e7f51-113">\[в \] любом типе объекта, перечисленном на странице « [текстура-объект](dx-graphics-hlsl-to-type.md) ».</span><span class="sxs-lookup"><span data-stu-id="e7f51-113">\[in\] Any object type listed in the [texture-object](dx-graphics-hlsl-to-type.md) page.</span></span><br/>                                                                                                                                                                     |
| <span data-ttu-id="e7f51-114"><span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*resourceType \[ size \] nn*</span><span class="sxs-lookup"><span data-stu-id="e7f51-114"><span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*resourceType\[size\]NN*</span></span><br/> | <span data-ttu-id="e7f51-115">\[в \] типе объекта Texture2D или Texture2DArray (см. страницу « [текстура-объект](dx-graphics-hlsl-to-type.md) »); *size* — это необязательное целое число, которое обозначает количество элементов в массиве; *Nn* — это целое число, которое обозначает количество нескольких выборок.</span><span class="sxs-lookup"><span data-stu-id="e7f51-115">\[in\] A Texture2D or a Texture2DArray object type (see the [texture-object](dx-graphics-hlsl-to-type.md) page); *size* is an optional integer that denotes the number of elements in the array; *NN* is an integer that denotes the number of multisamples.</span></span><br/> |
| <span data-ttu-id="e7f51-116"><span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType (s)*</span><span class="sxs-lookup"><span data-stu-id="e7f51-116"><span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType(s)*</span></span><br/>                               | <span data-ttu-id="e7f51-117">\[для \] каждого компонента возвращаемого типа, который является одним из следующих: UNORM, снорм, Синт, uint или float.</span><span class="sxs-lookup"><span data-stu-id="e7f51-117">\[in\] Per-component return type which is one of the following: UNORM, SNORM, SINT, UINT, or FLOAT.</span></span> <span data-ttu-id="e7f51-118">Число возвращаемых типов может быть равно 1 (если все компоненты имеют одинаковый тип), но может быть не меньше четырех.</span><span class="sxs-lookup"><span data-stu-id="e7f51-118">The number of return types can be as few as 1 (if all components are the same type), but can be as many as four.</span></span><br/>                                          |



 

<span data-ttu-id="e7f51-119">Доступ к ресурсу осуществляется в HLSL с помощью [Load](dx-graphics-hlsl-to-load.md); можно также получить доступ к многовыборочной текстуре, используя любой из образцов [объектов текстуры](dx-graphics-hlsl-to-type.md) HLSL.</span><span class="sxs-lookup"><span data-stu-id="e7f51-119">A resource is accessed in HLSL using [load](dx-graphics-hlsl-to-load.md); a non-multisampled texture can also be accessed using any of the HLSL [texture object](dx-graphics-hlsl-to-type.md) sample methods.</span></span>

<span data-ttu-id="e7f51-120">Если ресурс привязан к этапу шейдера, формат ресурса будет проверяться по типу возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="e7f51-120">If a resource is bound to a shader stage, the resource format will be validated against the return type.</span></span>

<span data-ttu-id="e7f51-121">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="e7f51-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e7f51-122">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="e7f51-122">Vertex Shader</span></span> | <span data-ttu-id="e7f51-123">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="e7f51-123">Geometry Shader</span></span> | <span data-ttu-id="e7f51-124">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="e7f51-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="e7f51-125">x</span><span class="sxs-lookup"><span data-stu-id="e7f51-125">x</span></span>             | <span data-ttu-id="e7f51-126">x</span><span class="sxs-lookup"><span data-stu-id="e7f51-126">x</span></span>               | <span data-ttu-id="e7f51-127">x</span><span class="sxs-lookup"><span data-stu-id="e7f51-127">x</span></span>            |



 

<span data-ttu-id="e7f51-128">Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.</span><span class="sxs-lookup"><span data-stu-id="e7f51-128">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="e7f51-129">Например, .</span><span class="sxs-lookup"><span data-stu-id="e7f51-129">Example</span></span>

<span data-ttu-id="e7f51-130">Ниже приведен пример.</span><span class="sxs-lookup"><span data-stu-id="e7f51-130">Here is an example.</span></span>


```
dcl_resource t3, buffer, UNORM
```



## <a name="minimum-shader-model"></a><span data-ttu-id="e7f51-131">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e7f51-131">Minimum Shader Model</span></span>

<span data-ttu-id="e7f51-132">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="e7f51-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e7f51-133">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e7f51-133">Shader Model</span></span>                                              | <span data-ttu-id="e7f51-134">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="e7f51-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e7f51-135">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="e7f51-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e7f51-136">да</span><span class="sxs-lookup"><span data-stu-id="e7f51-136">yes</span></span>       |
| [<span data-ttu-id="e7f51-137">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="e7f51-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e7f51-138">да</span><span class="sxs-lookup"><span data-stu-id="e7f51-138">yes</span></span>       |
| [<span data-ttu-id="e7f51-139">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="e7f51-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e7f51-140">да</span><span class="sxs-lookup"><span data-stu-id="e7f51-140">yes</span></span>       |
| [<span data-ttu-id="e7f51-141">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e7f51-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e7f51-142">Нет</span><span class="sxs-lookup"><span data-stu-id="e7f51-142">no</span></span>        |
| [<span data-ttu-id="e7f51-143">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e7f51-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e7f51-144">Нет</span><span class="sxs-lookup"><span data-stu-id="e7f51-144">no</span></span>        |
| [<span data-ttu-id="e7f51-145">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e7f51-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e7f51-146">Нет</span><span class="sxs-lookup"><span data-stu-id="e7f51-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e7f51-147">См. также</span><span class="sxs-lookup"><span data-stu-id="e7f51-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7f51-148">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e7f51-148">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





