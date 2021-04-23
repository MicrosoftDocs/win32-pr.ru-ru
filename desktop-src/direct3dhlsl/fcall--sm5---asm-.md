---
title: фкалл (SM5-ASM)
description: Вызов функции интерфейса.
ms.assetid: C21784A0-D2F4-4DDE-9AC4-4F21351BCA6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57ea40fec51cf4155b0932f6ce4a7b80d3180dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412227"
---
# <a name="fcall-sm5---asm"></a><span data-ttu-id="fb19c-103">фкалл (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="fb19c-103">fcall (sm5 - asm)</span></span>

<span data-ttu-id="fb19c-104">Вызов функции интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fb19c-104">Interface function call.</span></span>



| <span data-ttu-id="fb19c-105">фкалл FP \# \[ arrayIndex \] \[ callSite\]</span><span class="sxs-lookup"><span data-stu-id="fb19c-105">fcall fp\#\[arrayIndex\]\[callSite\]</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="fb19c-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="fb19c-106">Item</span></span>                                                                                                           | <span data-ttu-id="fb19c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="fb19c-107">Description</span></span>                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb19c-108"><span id="fp_"></span><span id="FP_"></span>*FP\#*</span><span class="sxs-lookup"><span data-stu-id="fb19c-108"><span id="fp_"></span><span id="FP_"></span>*fp\#*</span></span><br/>                                                  | <span data-ttu-id="fb19c-109">\[в \] указателе функции.</span><span class="sxs-lookup"><span data-stu-id="fb19c-109">\[in\] The function pointer.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="fb19c-110"><span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*arrayIndex*</span><span class="sxs-lookup"><span data-stu-id="fb19c-110"><span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*arrayIndex*</span></span><br/> | <span data-ttu-id="fb19c-111">\[\]необязательно.</span><span class="sxs-lookup"><span data-stu-id="fb19c-111">\[in\] Optional.</span></span> <span data-ttu-id="fb19c-112">Задает смещение в массиве указателей функции.</span><span class="sxs-lookup"><span data-stu-id="fb19c-112">Specifies an offset into the function pointer array.</span></span> <span data-ttu-id="fb19c-113">Этот параметр должен быть целочисленным литералом без знака, если FP \# не объявлен как индексируемый.</span><span class="sxs-lookup"><span data-stu-id="fb19c-113">This parameter must be a literal unsigned integer if fp\# was not declared as indexable.</span></span> <span data-ttu-id="fb19c-114">В противном случае arrayIndex может иметь форму "базовый литерал + смещение" из регистра шейдера.</span><span class="sxs-lookup"><span data-stu-id="fb19c-114">Otherwise, arrayIndex may be of the form literal base + offset from a shader register.</span></span> <span data-ttu-id="fb19c-115">Например, фкалл FP1 \[ R1. w + 0 \] \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="fb19c-115">For example, fcall fp1\[r1.w + 0\]\[0\] .</span></span><br/> |
| <span data-ttu-id="fb19c-116"><span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span>*callSite*</span><span class="sxs-lookup"><span data-stu-id="fb19c-116"><span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span> *callSite*</span></span><br/>     | <span data-ttu-id="fb19c-117">\[\]необязательно.</span><span class="sxs-lookup"><span data-stu-id="fb19c-117">\[in\] Optional.</span></span> <span data-ttu-id="fb19c-118">Смещение целого числа без знака в выбранной таблице функции, выбор тела функции FB \# для выполнения.</span><span class="sxs-lookup"><span data-stu-id="fb19c-118">A literal unsigned integer offset into the selected function table, selecting a function body fb\# to execute.</span></span> <br/>                                                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="fb19c-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="fb19c-119">Remarks</span></span>

<span data-ttu-id="fb19c-120">*FP \#* \[  \] \[ arrayIndex \] разрешается в определенную таблицу функций, выбранную из API за пределами шейдера, из вариантов таблицы функций, перечисленных в объявлении *FP \#*.</span><span class="sxs-lookup"><span data-stu-id="fb19c-120">*fp\#*\[*arrayIndex*\]\[\] resolves to a particular function table, selected from the API outside the shader from the function table choices listed in the declaration of *fp\#*.</span></span>

<span data-ttu-id="fb19c-121">Сумма \# в *\# FP* и *arrayIndex* выберите таблицу функций.</span><span class="sxs-lookup"><span data-stu-id="fb19c-121">The sum of \# in *fp\#* and *arrayIndex* select the function table.</span></span> <span data-ttu-id="fb19c-122">Например, если интерфейс объявлен как fp4 \[ 4 \] \[ 3 \] (размер массива 4), следующие **фкаллs** эквивалентны: фкалл fp4 \[ 2 \] \[ 3 \] и FP5 \[ 1 \] \[ 3 \] , так как 4 + 2 = 5 + 1.</span><span class="sxs-lookup"><span data-stu-id="fb19c-122">For example, if an interface is declared as fp4\[4\]\[3\] (array size of 4), the following **fcall** s are equivalent: fcall fp4\[2\]\[3\] and fp5\[1\]\[3\], because 4+2 = 5+1.</span></span>

### <a name="restrictions"></a><span data-ttu-id="fb19c-123">Ограничения</span><span class="sxs-lookup"><span data-stu-id="fb19c-123">Restrictions</span></span>

-   <span data-ttu-id="fb19c-124">Если *arrayIndex* использует динамическое индексирование, поведение не определено, если *arrayIndex* расходят на смежных вызовах шейдера, которые могут выполняться в локкстеп.</span><span class="sxs-lookup"><span data-stu-id="fb19c-124">If *arrayIndex* uses dynamic indexing, behavior is undefined if *arrayIndex* diverges on adjacent shader invocations, which could be executing in lockstep.</span></span> <span data-ttu-id="fb19c-125">Компилятор HLSL будет пытаться запретить этот случай.</span><span class="sxs-lookup"><span data-stu-id="fb19c-125">The HLSL compiler will attempt to disallow this case.</span></span>

    <span data-ttu-id="fb19c-126">Смежные вызовы могут быть неактивными из-за управления потоком, так как они не прерывать выполнение локкстеп.</span><span class="sxs-lookup"><span data-stu-id="fb19c-126">Adjacent invocations can be inactive due to flow control, because it doesn t break lockstep execution.</span></span>

-   <span data-ttu-id="fb19c-127">Если *FP \#*  +  *arrayIndex* указывает индекс вне допустимого диапазона, поведение не определено.</span><span class="sxs-lookup"><span data-stu-id="fb19c-127">If *fp\#* + *arrayIndex* specifies an out of bounds index, behavior is undefined.</span></span>
-   <span data-ttu-id="fb19c-128">В неопределенных случаях, описанных здесь, это означает, что поведение текущего устройства D3D станет неопределенным, включая возможность потери устройства.</span><span class="sxs-lookup"><span data-stu-id="fb19c-128">For the undefined cases described here, it means the behavior of the current D3D device becomes undefined, including the possibility of Device Lost.</span></span> <span data-ttu-id="fb19c-129">Однако доступ к памяти за пределами текущего устройства D3D будет невозможен или выполнен в виде кода.</span><span class="sxs-lookup"><span data-stu-id="fb19c-129">However no memory outside the current D3D device will be accessed or executed as code.</span></span>

<span data-ttu-id="fb19c-130">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="fb19c-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fb19c-131">Вершина</span><span class="sxs-lookup"><span data-stu-id="fb19c-131">Vertex</span></span> | <span data-ttu-id="fb19c-132">Поверхности</span><span class="sxs-lookup"><span data-stu-id="fb19c-132">Hull</span></span> | <span data-ttu-id="fb19c-133">Домен</span><span class="sxs-lookup"><span data-stu-id="fb19c-133">Domain</span></span> | <span data-ttu-id="fb19c-134">Геометрия</span><span class="sxs-lookup"><span data-stu-id="fb19c-134">Geometry</span></span> | <span data-ttu-id="fb19c-135">Пиксель</span><span class="sxs-lookup"><span data-stu-id="fb19c-135">Pixel</span></span> | <span data-ttu-id="fb19c-136">Вычисления</span><span class="sxs-lookup"><span data-stu-id="fb19c-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="fb19c-137">X</span><span class="sxs-lookup"><span data-stu-id="fb19c-137">X</span></span>      | <span data-ttu-id="fb19c-138">X</span><span class="sxs-lookup"><span data-stu-id="fb19c-138">X</span></span>    | <span data-ttu-id="fb19c-139">X</span><span class="sxs-lookup"><span data-stu-id="fb19c-139">X</span></span>      | <span data-ttu-id="fb19c-140">X</span><span class="sxs-lookup"><span data-stu-id="fb19c-140">X</span></span>        | <span data-ttu-id="fb19c-141">X</span><span class="sxs-lookup"><span data-stu-id="fb19c-141">X</span></span>     | <span data-ttu-id="fb19c-142">X</span><span class="sxs-lookup"><span data-stu-id="fb19c-142">X</span></span>       |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="fb19c-143">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fb19c-143">Minimum Shader Model</span></span>

<span data-ttu-id="fb19c-144">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="fb19c-144">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="fb19c-145">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fb19c-145">Shader Model</span></span>                                              | <span data-ttu-id="fb19c-146">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="fb19c-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fb19c-147">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="fb19c-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fb19c-148">да</span><span class="sxs-lookup"><span data-stu-id="fb19c-148">yes</span></span>       |
| [<span data-ttu-id="fb19c-149">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="fb19c-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fb19c-150">Нет</span><span class="sxs-lookup"><span data-stu-id="fb19c-150">no</span></span>        |
| [<span data-ttu-id="fb19c-151">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="fb19c-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fb19c-152">Нет</span><span class="sxs-lookup"><span data-stu-id="fb19c-152">no</span></span>        |
| [<span data-ttu-id="fb19c-153">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fb19c-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fb19c-154">Нет</span><span class="sxs-lookup"><span data-stu-id="fb19c-154">no</span></span>        |
| [<span data-ttu-id="fb19c-155">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fb19c-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fb19c-156">Нет</span><span class="sxs-lookup"><span data-stu-id="fb19c-156">no</span></span>        |
| [<span data-ttu-id="fb19c-157">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fb19c-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fb19c-158">Нет</span><span class="sxs-lookup"><span data-stu-id="fb19c-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fb19c-159">См. также</span><span class="sxs-lookup"><span data-stu-id="fb19c-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb19c-160">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fb19c-160">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





