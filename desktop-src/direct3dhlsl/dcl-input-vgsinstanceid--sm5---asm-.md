---
title: dcl_input Вгсинстанцеид (SM5-ASM)
description: Включите создание экземпляров шейдера Geometry.
ms.assetid: 47B9BAD5-0FFF-4DB7-B34A-7811B8A4F792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3134a9d372f1fde5457f26235fe9a6a5439c58c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335643"
---
# <a name="dcl_input-vgsinstanceid-sm5---asm"></a><span data-ttu-id="1481d-103">дкл \_ input вгсинстанцеид (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="1481d-103">dcl\_input vGSInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="1481d-104">Включите создание экземпляров шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="1481d-104">Enable geometry shader instancing.</span></span>



| <span data-ttu-id="1481d-105">дкл \_ входные вгсинстанцеид, instanceCount</span><span class="sxs-lookup"><span data-stu-id="1481d-105">dcl\_input vGSInstanceID, instanceCount</span></span> |
|-----------------------------------------|



 



| <span data-ttu-id="1481d-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="1481d-106">Item</span></span>                                                                                                                       | <span data-ttu-id="1481d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1481d-107">Description</span></span>                           |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="1481d-108"><span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*вгсинстанцеид*</span><span class="sxs-lookup"><span data-stu-id="1481d-108"><span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vGSInstanceID*</span></span><br/> | <span data-ttu-id="1481d-109">\[в \] идентификаторе экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1481d-109">\[in\] The instance ID.</span></span><br/>    |
| <span data-ttu-id="1481d-110"><span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*</span><span class="sxs-lookup"><span data-stu-id="1481d-110"><span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*</span></span><br/> | <span data-ttu-id="1481d-111">\[в \] поле число экземпляров.</span><span class="sxs-lookup"><span data-stu-id="1481d-111">\[in\] The instance count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1481d-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="1481d-112">Remarks</span></span>

<span data-ttu-id="1481d-113">Параметр *instanceCount* объявления указывает, сколько экземпляров шейдер геометрии должен выполнять для каждого входного примитива.</span><span class="sxs-lookup"><span data-stu-id="1481d-113">The *instanceCount* parameter of the declaration specifies how many instances the geometry shader should execute for each input primitive.</span></span> <span data-ttu-id="1481d-114">Максимальное значение для *instanceCount* — 32.</span><span class="sxs-lookup"><span data-stu-id="1481d-114">The maximum value for *instanceCount* is 32.</span></span>

<span data-ttu-id="1481d-115">Максимальное число вершин, объявленных для выходных данных через [**дкл \_ максаутпутвертекскаунт**](dcl-maxoutputvertexcount.md), применяется по отдельности к каждому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="1481d-115">The maximum number of vertices declared for output, via [**dcl\_maxOutputVertexCount**](dcl-maxoutputvertexcount.md), applies individually to each instance.</span></span>

<span data-ttu-id="1481d-116">Число экземпляров в этом объявлении, умноженное на максимальное число вершин на экземпляр через [**дкл \_ максаутпутвертекскаунт**](dcl-maxoutputvertexcount.md), должно быть <= 1024.</span><span class="sxs-lookup"><span data-stu-id="1481d-116">The instance count in this declaration, multiplied by the maximum vertex count per instance via [**dcl\_maxOutputVertexCount**](dcl-maxoutputvertexcount.md), must be <= 1024.</span></span>

<span data-ttu-id="1481d-117">Объем данных, которые может порождать данный экземпляр шейдера Geometry, — это 1024 скаляров, проверенных с помощью подсчета всех скалярных значений, объявленных для входа и умножения на число объявленных выходных вершин.</span><span class="sxs-lookup"><span data-stu-id="1481d-117">The amount of data that a given geometry shader instance can emit is 1024 scalars maximum, validated by counting up all scalars declared for input and multiplying by the declared output vertex count.</span></span>

<span data-ttu-id="1481d-118">Использование создания экземпляров шейдера Geometry эффективно увеличивает общий объем данных, которые могут выдаваться для каждого примитива ввода.</span><span class="sxs-lookup"><span data-stu-id="1481d-118">Use of geometry shader instancing effectively increases the total amount of data that can be emitted per input primitive.</span></span> <span data-ttu-id="1481d-119">1024 скаляры для одного экземпляра дают до 1024 \* 32 скалярных выходных данных по всем экземплярам шейдера Geometry для одного примитива ввода.</span><span class="sxs-lookup"><span data-stu-id="1481d-119">1024 scalars for a single instance yields up to 1024\*32 scalars of output data across all geometry shader instances for a single input primitive.</span></span> <span data-ttu-id="1481d-120">Однако чем больше экземпляров, тем меньше вершин может порождать каждый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="1481d-120">However the more instances, the fewer vertices each instance can emit.</span></span> <span data-ttu-id="1481d-121">Один экземпляр (без создания экземпляра) может выдавать 1024 вершин.</span><span class="sxs-lookup"><span data-stu-id="1481d-121">A single instance (no instancing) can emit 1024 vertices.</span></span> <span data-ttu-id="1481d-122">Если объявить \* экземпляры 32, это означает, что каждый экземпляр может выводить только 1024/32 = 32 вершин.</span><span class="sxs-lookup"><span data-stu-id="1481d-122">If you declare \*32 instances it means each instance can only output 1024/32 = 32 vertices.</span></span>

<span data-ttu-id="1481d-123">Объявление создания экземпляров шейдера Geometry делает доступной для программы автономный 32-разрядный целочисленный входной регистр *вгсинстанцеид*.</span><span class="sxs-lookup"><span data-stu-id="1481d-123">The geometry shader instancing declaration makes available to the program a standalone 32-bit integer input register, *vGSInstanceID*.</span></span> <span data-ttu-id="1481d-124">Каждый экземпляр шейдера Geometry определяется значением, содержащимся в *вгсинстанцеид* \[ 0, 1, 2.. \] .</span><span class="sxs-lookup"><span data-stu-id="1481d-124">Each geometry shader instance is identified by the value contained in *vGSInstanceID* \[0,1,2...\].</span></span>

<span data-ttu-id="1481d-125">*вгсинстанцеид* не является частью входного массива вершин шейдера Geometry (например, 3 вершины при вводе треугольника).</span><span class="sxs-lookup"><span data-stu-id="1481d-125">*vGSInstanceID* is not part of the geometry shader input vertex array (e.g. 3 vertices when inputting a triangle).</span></span> <span data-ttu-id="1481d-126">Регистр *вгсинстанцеид* по своей собственной, например впримитивеид.</span><span class="sxs-lookup"><span data-stu-id="1481d-126">The *vGSInstanceID* register stands on its own, like vPrimitiveID.</span></span>

<span data-ttu-id="1481d-127">После завершения каждого экземпляра шейдера Geometry в выходной топологии возникает неявная вырезание, поэтому последовательные экземпляры не зависят друг от друга.</span><span class="sxs-lookup"><span data-stu-id="1481d-127">When each geometry shader instance ends, there is an implicit cut in the output topology, so consecutive instances do not depend on each other.</span></span>

<span data-ttu-id="1481d-128">Несмотря на то что оборудование может выполнять каждый экземпляр шейдера Geometry в параллельном режиме, выходные данные всех экземпляров в конце сериализуются, как если бы все экземпляры вызовов шейдера Geometry выполнялись последовательно в цикле, *вгсинстанцеид* от 0 до *instanceCount*-1, с неявной выходной топологией в конце каждого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1481d-128">Although hardware may execute each geometry shader instance in parallel, the output of all instances at the end is serialized as if all the instanced geometry shader invocations ran sequentially in a loop iterating *vGSInstanceID* from 0 to *instanceCount*-1, with implicit output topology cuts at the end of each instance.</span></span>

<span data-ttu-id="1481d-129">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="1481d-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1481d-130">Вершина</span><span class="sxs-lookup"><span data-stu-id="1481d-130">Vertex</span></span> | <span data-ttu-id="1481d-131">Поверхности</span><span class="sxs-lookup"><span data-stu-id="1481d-131">Hull</span></span> | <span data-ttu-id="1481d-132">Домен</span><span class="sxs-lookup"><span data-stu-id="1481d-132">Domain</span></span> | <span data-ttu-id="1481d-133">Геометрия</span><span class="sxs-lookup"><span data-stu-id="1481d-133">Geometry</span></span> | <span data-ttu-id="1481d-134">Пиксель</span><span class="sxs-lookup"><span data-stu-id="1481d-134">Pixel</span></span> | <span data-ttu-id="1481d-135">Вычисления</span><span class="sxs-lookup"><span data-stu-id="1481d-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="1481d-136">X</span><span class="sxs-lookup"><span data-stu-id="1481d-136">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1481d-137">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1481d-137">Minimum Shader Model</span></span>

<span data-ttu-id="1481d-138">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="1481d-138">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1481d-139">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1481d-139">Shader Model</span></span>                                              | <span data-ttu-id="1481d-140">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="1481d-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1481d-141">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="1481d-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1481d-142">да</span><span class="sxs-lookup"><span data-stu-id="1481d-142">yes</span></span>       |
| [<span data-ttu-id="1481d-143">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="1481d-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1481d-144">Нет</span><span class="sxs-lookup"><span data-stu-id="1481d-144">no</span></span>        |
| [<span data-ttu-id="1481d-145">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="1481d-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1481d-146">Нет</span><span class="sxs-lookup"><span data-stu-id="1481d-146">no</span></span>        |
| [<span data-ttu-id="1481d-147">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1481d-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1481d-148">Нет</span><span class="sxs-lookup"><span data-stu-id="1481d-148">no</span></span>        |
| [<span data-ttu-id="1481d-149">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1481d-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1481d-150">Нет</span><span class="sxs-lookup"><span data-stu-id="1481d-150">no</span></span>        |
| [<span data-ttu-id="1481d-151">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1481d-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1481d-152">Нет</span><span class="sxs-lookup"><span data-stu-id="1481d-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1481d-153">См. также</span><span class="sxs-lookup"><span data-stu-id="1481d-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1481d-154">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1481d-154">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





