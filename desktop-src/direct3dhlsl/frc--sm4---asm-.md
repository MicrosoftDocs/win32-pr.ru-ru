---
title: ФРК (SM4-ASM)
description: Компонентно-ориентированное извлечение дробного компонента.
ms.assetid: 17C88BCE-7F2F-446C-9BB4-860098B5E42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f59b747f38fb970b92b5e48610873efe781d63d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993921"
---
# <a name="frc-sm4---asm"></a><span data-ttu-id="53d35-103">ФРК (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="53d35-103">frc (sm4 - asm)</span></span>

<span data-ttu-id="53d35-104">Компонентно-ориентированное извлечение дробного компонента.</span><span class="sxs-lookup"><span data-stu-id="53d35-104">Component-wise, extract fractional component.</span></span>



| <span data-ttu-id="53d35-105">ФРК \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="53d35-105">frc\[\_sat\] dest\[.mask\], \[-\] src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="53d35-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="53d35-106">Item</span></span>                                                            | <span data-ttu-id="53d35-107">Описание</span><span class="sxs-lookup"><span data-stu-id="53d35-107">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53d35-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="53d35-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="53d35-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="53d35-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="53d35-110">*конечный адрес*  =  *src0*  -  [Round \_ Ni](round-ni--sm4---asm-.md)(*src0*)</span><span class="sxs-lookup"><span data-stu-id="53d35-110">*dest* = *src0* - [round\_ni](round-ni--sm4---asm-.md)(*src0*)</span></span><br/> |
| <span data-ttu-id="53d35-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="53d35-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="53d35-112">\[в \] компоненте операции.</span><span class="sxs-lookup"><span data-stu-id="53d35-112">\[in\] The component in the operation.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="53d35-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="53d35-113">Remarks</span></span>

<span data-ttu-id="53d35-114">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел.</span><span class="sxs-lookup"><span data-stu-id="53d35-114">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



| <span data-ttu-id="53d35-115">**src**</span><span class="sxs-lookup"><span data-stu-id="53d35-115">**src**</span></span>  | <span data-ttu-id="53d35-116">**-INF**</span><span class="sxs-lookup"><span data-stu-id="53d35-116">**-inf**</span></span> | <span data-ttu-id="53d35-117">**-F**</span><span class="sxs-lookup"><span data-stu-id="53d35-117">**-F**</span></span>     | <span data-ttu-id="53d35-118">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="53d35-118">**-denorm**</span></span> | <span data-ttu-id="53d35-119">**-0**</span><span class="sxs-lookup"><span data-stu-id="53d35-119">**-0**</span></span> | <span data-ttu-id="53d35-120">**+0**</span><span class="sxs-lookup"><span data-stu-id="53d35-120">**+0**</span></span> | <span data-ttu-id="53d35-121">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="53d35-121">**+denorm**</span></span> | <span data-ttu-id="53d35-122">**+ F**</span><span class="sxs-lookup"><span data-stu-id="53d35-122">**+F**</span></span>     | <span data-ttu-id="53d35-123">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="53d35-123">**+inf**</span></span> | <span data-ttu-id="53d35-124">**Не число**</span><span class="sxs-lookup"><span data-stu-id="53d35-124">**NaN**</span></span> |
|----------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="53d35-125">**dest**</span><span class="sxs-lookup"><span data-stu-id="53d35-125">**dest**</span></span> | <span data-ttu-id="53d35-126">не число</span><span class="sxs-lookup"><span data-stu-id="53d35-126">NaN</span></span>      | <span data-ttu-id="53d35-127">\[+ 0 – 1)</span><span class="sxs-lookup"><span data-stu-id="53d35-127">\[+0 to 1)</span></span> | <span data-ttu-id="53d35-128">+0</span><span class="sxs-lookup"><span data-stu-id="53d35-128">+0</span></span>          | <span data-ttu-id="53d35-129">+0</span><span class="sxs-lookup"><span data-stu-id="53d35-129">+0</span></span>     | <span data-ttu-id="53d35-130">+0</span><span class="sxs-lookup"><span data-stu-id="53d35-130">+0</span></span>     | <span data-ttu-id="53d35-131">+0</span><span class="sxs-lookup"><span data-stu-id="53d35-131">+0</span></span>          | <span data-ttu-id="53d35-132">\[+ 0 – 1)</span><span class="sxs-lookup"><span data-stu-id="53d35-132">\[+0 to 1)</span></span> | <span data-ttu-id="53d35-133">Не число</span><span class="sxs-lookup"><span data-stu-id="53d35-133">NaN</span></span>      | <span data-ttu-id="53d35-134">Не число</span><span class="sxs-lookup"><span data-stu-id="53d35-134">NaN</span></span>     |



 

<span data-ttu-id="53d35-135">F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="53d35-135">F means finite-real number.</span></span>

<span data-ttu-id="53d35-136">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="53d35-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="53d35-137">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="53d35-137">Vertex Shader</span></span> | <span data-ttu-id="53d35-138">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="53d35-138">Geometry Shader</span></span> | <span data-ttu-id="53d35-139">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="53d35-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="53d35-140">x</span><span class="sxs-lookup"><span data-stu-id="53d35-140">x</span></span>             | <span data-ttu-id="53d35-141">x</span><span class="sxs-lookup"><span data-stu-id="53d35-141">x</span></span>               | <span data-ttu-id="53d35-142">x</span><span class="sxs-lookup"><span data-stu-id="53d35-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="53d35-143">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="53d35-143">Minimum Shader Model</span></span>

<span data-ttu-id="53d35-144">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="53d35-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="53d35-145">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="53d35-145">Shader Model</span></span>                                              | <span data-ttu-id="53d35-146">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="53d35-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="53d35-147">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="53d35-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="53d35-148">да</span><span class="sxs-lookup"><span data-stu-id="53d35-148">yes</span></span>       |
| [<span data-ttu-id="53d35-149">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="53d35-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="53d35-150">да</span><span class="sxs-lookup"><span data-stu-id="53d35-150">yes</span></span>       |
| [<span data-ttu-id="53d35-151">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="53d35-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="53d35-152">да</span><span class="sxs-lookup"><span data-stu-id="53d35-152">yes</span></span>       |
| [<span data-ttu-id="53d35-153">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53d35-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="53d35-154">Нет</span><span class="sxs-lookup"><span data-stu-id="53d35-154">no</span></span>        |
| [<span data-ttu-id="53d35-155">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53d35-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="53d35-156">Нет</span><span class="sxs-lookup"><span data-stu-id="53d35-156">no</span></span>        |
| [<span data-ttu-id="53d35-157">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53d35-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="53d35-158">Нет</span><span class="sxs-lookup"><span data-stu-id="53d35-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="53d35-159">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="53d35-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53d35-160">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53d35-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





