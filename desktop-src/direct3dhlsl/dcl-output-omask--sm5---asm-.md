---
title: dcl_output Омаск (SM5-ASM)
description: Объявите выходной регистр, записываемый шейдером.
ms.assetid: 23FC5FA3-F550-4CD1-9AA9-86738818686F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1831a47680a06eba085f61badfe56529eed4ba32
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412238"
---
# <a name="dcl_output-omask-sm5---asm"></a><span data-ttu-id="d9589-103">дкл \_ Output омаск (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="d9589-103">dcl\_output oMask (sm5 - asm)</span></span>

<span data-ttu-id="d9589-104">Объявите выходной регистр, записываемый шейдером.</span><span class="sxs-lookup"><span data-stu-id="d9589-104">Declare an output register to be written by the shader.</span></span>



| <span data-ttu-id="d9589-105">дкл \_ выход o \# \[ . Mask\]</span><span class="sxs-lookup"><span data-stu-id="d9589-105">dcl\_output o\#\[.mask\]</span></span> |
|--------------------------|



 



| <span data-ttu-id="d9589-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="d9589-106">Item</span></span>                                                   | <span data-ttu-id="d9589-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d9589-107">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="d9589-108"><span id="o"></span><span id="O"></span>*вывода*</span><span class="sxs-lookup"><span data-stu-id="d9589-108"><span id="o"></span><span id="O"></span>*o*</span></span><br/> | <span data-ttu-id="d9589-109">\[в \] реестре выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d9589-109">\[in\] The output register.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d9589-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="d9589-110">Remarks</span></span>


```
Example:
                dcl_output o[3].xyz
```



### <a name="restrictions"></a><span data-ttu-id="d9589-111">Ограничения</span><span class="sxs-lookup"><span data-stu-id="d9589-111">Restrictions</span></span>

-   <span data-ttu-id="d9589-112">Маска компонента может быть любым подмножеством \[ ксизв \] .</span><span class="sxs-lookup"><span data-stu-id="d9589-112">The component mask can be any subset of \[xyzw\].</span></span> <span data-ttu-id="d9589-113">Однако разрывы между компонентами не занимают место.</span><span class="sxs-lookup"><span data-stu-id="d9589-113">However, leaving gaps between components wastes space.</span></span>
-   <span data-ttu-id="d9589-114">Допустимо объявлять надмножество маски компонента, объявленной для входных данных на следующем этапе.</span><span class="sxs-lookup"><span data-stu-id="d9589-114">It is legal to declare a superset of the component mask declared for input by the next stage.</span></span> <span data-ttu-id="d9589-115">Однако взаимно исключающие маски не допускаются.</span><span class="sxs-lookup"><span data-stu-id="d9589-115">However mutually exclusive masks are not allowed.</span></span> <span data-ttu-id="d9589-116">Выводится O3. XY шейдера вершин, означающее, что построитель построителя текстуры помещает значение v3. z недопустимый, но вывод значений v3. x или v3. y или v3. XY является допустимым.</span><span class="sxs-lookup"><span data-stu-id="d9589-116">The vertex shader outputting o3.xy, means the pixel shader inputting v3.z is invalid, but inputting v3.x or v3.y or v3.xy is valid.</span></span>

<span data-ttu-id="d9589-117">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="d9589-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d9589-118">Вершина</span><span class="sxs-lookup"><span data-stu-id="d9589-118">Vertex</span></span> | <span data-ttu-id="d9589-119">Поверхности</span><span class="sxs-lookup"><span data-stu-id="d9589-119">Hull</span></span> | <span data-ttu-id="d9589-120">Домен</span><span class="sxs-lookup"><span data-stu-id="d9589-120">Domain</span></span> | <span data-ttu-id="d9589-121">Геометрия</span><span class="sxs-lookup"><span data-stu-id="d9589-121">Geometry</span></span> | <span data-ttu-id="d9589-122">Пиксель</span><span class="sxs-lookup"><span data-stu-id="d9589-122">Pixel</span></span> | <span data-ttu-id="d9589-123">Вычисления</span><span class="sxs-lookup"><span data-stu-id="d9589-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d9589-124">X</span><span class="sxs-lookup"><span data-stu-id="d9589-124">X</span></span>      | <span data-ttu-id="d9589-125">X</span><span class="sxs-lookup"><span data-stu-id="d9589-125">X</span></span>    | <span data-ttu-id="d9589-126">X</span><span class="sxs-lookup"><span data-stu-id="d9589-126">X</span></span>      | <span data-ttu-id="d9589-127">X</span><span class="sxs-lookup"><span data-stu-id="d9589-127">X</span></span>        | <span data-ttu-id="d9589-128">X</span><span class="sxs-lookup"><span data-stu-id="d9589-128">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d9589-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d9589-129">Minimum Shader Model</span></span>

<span data-ttu-id="d9589-130">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="d9589-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d9589-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d9589-131">Shader Model</span></span>                                              | <span data-ttu-id="d9589-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="d9589-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d9589-133">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="d9589-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d9589-134">да</span><span class="sxs-lookup"><span data-stu-id="d9589-134">yes</span></span>       |
| [<span data-ttu-id="d9589-135">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="d9589-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d9589-136">Нет</span><span class="sxs-lookup"><span data-stu-id="d9589-136">no</span></span>        |
| [<span data-ttu-id="d9589-137">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="d9589-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d9589-138">Нет</span><span class="sxs-lookup"><span data-stu-id="d9589-138">no</span></span>        |
| [<span data-ttu-id="d9589-139">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9589-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d9589-140">Нет</span><span class="sxs-lookup"><span data-stu-id="d9589-140">no</span></span>        |
| [<span data-ttu-id="d9589-141">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9589-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d9589-142">Нет</span><span class="sxs-lookup"><span data-stu-id="d9589-142">no</span></span>        |
| [<span data-ttu-id="d9589-143">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9589-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d9589-144">Нет</span><span class="sxs-lookup"><span data-stu-id="d9589-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d9589-145">См. также</span><span class="sxs-lookup"><span data-stu-id="d9589-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9589-146">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9589-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





