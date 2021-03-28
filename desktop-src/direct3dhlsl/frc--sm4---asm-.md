---
title: ФРК (SM4-ASM)
description: Компонентно-ориентированное извлечение дробного компонента.
ms.assetid: 17C88BCE-7F2F-446C-9BB4-860098B5E42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4abcfd56e7d6051e9c476097b3e5eef4d97563e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983876"
---
# <a name="frc-sm4---asm"></a><span data-ttu-id="fcb41-103">ФРК (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="fcb41-103">frc (sm4 - asm)</span></span>

<span data-ttu-id="fcb41-104">Компонентно-ориентированное извлечение дробного компонента.</span><span class="sxs-lookup"><span data-stu-id="fcb41-104">Component-wise, extract fractional component.</span></span>



| <span data-ttu-id="fcb41-105">ФРК \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="fcb41-105">frc\[\_sat\] dest\[.mask\], \[-\] src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="fcb41-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="fcb41-106">Item</span></span>                                                            | <span data-ttu-id="fcb41-107">Описание</span><span class="sxs-lookup"><span data-stu-id="fcb41-107">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcb41-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="fcb41-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="fcb41-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="fcb41-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="fcb41-110">*конечный адрес*  =  *src0*  -  [Round \_ Ni](round-ni--sm4---asm-.md)(*src0*)</span><span class="sxs-lookup"><span data-stu-id="fcb41-110">*dest* = *src0* - [round\_ni](round-ni--sm4---asm-.md)(*src0*)</span></span><br/> |
| <span data-ttu-id="fcb41-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="fcb41-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="fcb41-112">\[в \] компоненте операции.</span><span class="sxs-lookup"><span data-stu-id="fcb41-112">\[in\] The component in the operation.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="fcb41-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="fcb41-113">Remarks</span></span>

<span data-ttu-id="fcb41-114">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел.</span><span class="sxs-lookup"><span data-stu-id="fcb41-114">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



|          |          |            |             |        |        |             |            |          |         |
|----------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="fcb41-115">**src**</span><span class="sxs-lookup"><span data-stu-id="fcb41-115">**src**</span></span>  | <span data-ttu-id="fcb41-116">**-INF**</span><span class="sxs-lookup"><span data-stu-id="fcb41-116">**-inf**</span></span> | <span data-ttu-id="fcb41-117">**-F**</span><span class="sxs-lookup"><span data-stu-id="fcb41-117">**-F**</span></span>     | <span data-ttu-id="fcb41-118">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="fcb41-118">**-denorm**</span></span> | <span data-ttu-id="fcb41-119">**-0**</span><span class="sxs-lookup"><span data-stu-id="fcb41-119">**-0**</span></span> | <span data-ttu-id="fcb41-120">**+0**</span><span class="sxs-lookup"><span data-stu-id="fcb41-120">**+0**</span></span> | <span data-ttu-id="fcb41-121">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="fcb41-121">**+denorm**</span></span> | <span data-ttu-id="fcb41-122">**+ F**</span><span class="sxs-lookup"><span data-stu-id="fcb41-122">**+F**</span></span>     | <span data-ttu-id="fcb41-123">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="fcb41-123">**+inf**</span></span> | <span data-ttu-id="fcb41-124">**Не число**</span><span class="sxs-lookup"><span data-stu-id="fcb41-124">**NaN**</span></span> |
| <span data-ttu-id="fcb41-125">**dest**</span><span class="sxs-lookup"><span data-stu-id="fcb41-125">**dest**</span></span> | <span data-ttu-id="fcb41-126">не число</span><span class="sxs-lookup"><span data-stu-id="fcb41-126">NaN</span></span>      | <span data-ttu-id="fcb41-127">\[+ 0 – 1)</span><span class="sxs-lookup"><span data-stu-id="fcb41-127">\[+0 to 1)</span></span> | <span data-ttu-id="fcb41-128">+0</span><span class="sxs-lookup"><span data-stu-id="fcb41-128">+0</span></span>          | <span data-ttu-id="fcb41-129">+0</span><span class="sxs-lookup"><span data-stu-id="fcb41-129">+0</span></span>     | <span data-ttu-id="fcb41-130">+0</span><span class="sxs-lookup"><span data-stu-id="fcb41-130">+0</span></span>     | <span data-ttu-id="fcb41-131">+0</span><span class="sxs-lookup"><span data-stu-id="fcb41-131">+0</span></span>          | <span data-ttu-id="fcb41-132">\[+ 0 – 1)</span><span class="sxs-lookup"><span data-stu-id="fcb41-132">\[+0 to 1)</span></span> | <span data-ttu-id="fcb41-133">Не число</span><span class="sxs-lookup"><span data-stu-id="fcb41-133">NaN</span></span>      | <span data-ttu-id="fcb41-134">Не число</span><span class="sxs-lookup"><span data-stu-id="fcb41-134">NaN</span></span>     |



 

<span data-ttu-id="fcb41-135">F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="fcb41-135">F means finite-real number.</span></span>

<span data-ttu-id="fcb41-136">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="fcb41-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fcb41-137">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="fcb41-137">Vertex Shader</span></span> | <span data-ttu-id="fcb41-138">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="fcb41-138">Geometry Shader</span></span> | <span data-ttu-id="fcb41-139">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="fcb41-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="fcb41-140">x</span><span class="sxs-lookup"><span data-stu-id="fcb41-140">x</span></span>             | <span data-ttu-id="fcb41-141">x</span><span class="sxs-lookup"><span data-stu-id="fcb41-141">x</span></span>               | <span data-ttu-id="fcb41-142">x</span><span class="sxs-lookup"><span data-stu-id="fcb41-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fcb41-143">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fcb41-143">Minimum Shader Model</span></span>

<span data-ttu-id="fcb41-144">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="fcb41-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fcb41-145">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fcb41-145">Shader Model</span></span>                                              | <span data-ttu-id="fcb41-146">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="fcb41-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fcb41-147">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="fcb41-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fcb41-148">да</span><span class="sxs-lookup"><span data-stu-id="fcb41-148">yes</span></span>       |
| [<span data-ttu-id="fcb41-149">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="fcb41-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fcb41-150">да</span><span class="sxs-lookup"><span data-stu-id="fcb41-150">yes</span></span>       |
| [<span data-ttu-id="fcb41-151">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="fcb41-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fcb41-152">да</span><span class="sxs-lookup"><span data-stu-id="fcb41-152">yes</span></span>       |
| [<span data-ttu-id="fcb41-153">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fcb41-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fcb41-154">Нет</span><span class="sxs-lookup"><span data-stu-id="fcb41-154">no</span></span>        |
| [<span data-ttu-id="fcb41-155">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fcb41-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fcb41-156">Нет</span><span class="sxs-lookup"><span data-stu-id="fcb41-156">no</span></span>        |
| [<span data-ttu-id="fcb41-157">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fcb41-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fcb41-158">Нет</span><span class="sxs-lookup"><span data-stu-id="fcb41-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fcb41-159">См. также</span><span class="sxs-lookup"><span data-stu-id="fcb41-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcb41-160">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fcb41-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





