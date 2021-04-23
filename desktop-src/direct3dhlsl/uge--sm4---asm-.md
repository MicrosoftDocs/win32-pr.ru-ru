---
title: уже (SM4-ASM)
description: Покомпонентное векторное целое число без знака "больше или равно" для сравнения.
ms.assetid: CA8E19EC-619F-4C19-B6FD-91650B5DAF9F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4aecd9e39aa94c69acefff0f6a0fdf843cec5d8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103890000"
---
# <a name="uge-sm4---asm"></a><span data-ttu-id="1c6b3-103">уже (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="1c6b3-103">uge (sm4 - asm)</span></span>

<span data-ttu-id="1c6b3-104">Покомпонентное векторное целое число без знака "больше или равно" для сравнения.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-104">Component-wise vector unsigned integer greater-than-or-equal comparison.</span></span>



| <span data-ttu-id="1c6b3-105">уже dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="1c6b3-105">uge dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="1c6b3-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="1c6b3-106">Item</span></span>                                                            | <span data-ttu-id="1c6b3-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1c6b3-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="1c6b3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="1c6b3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1c6b3-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="1c6b3-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1c6b3-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1c6b3-111">\[в \] компонентах, сравниваемых с *src1*.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-111">\[in\] The components to compare to *src1*.</span></span><br/>        |
| <span data-ttu-id="1c6b3-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="1c6b3-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="1c6b3-113">\[в \] компонентах, сравниваемых с *src0*.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-113">\[in\] The components to compare to *src0*.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="1c6b3-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="1c6b3-114">Remarks</span></span>

<span data-ttu-id="1c6b3-115">Эта инструкция выполняет сравнение целых чисел без знака (*src0*  >=  *src1*) для каждого компонента и записывает результат в *dest*.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-115">This instruction performs the unsigned integer comparison (*src0* >= *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="1c6b3-116">Если сравнение истинно, то для этого компонента возвращается значение 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="1c6b3-117">В противном случае возвращается 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="1c6b3-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="1c6b3-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1c6b3-119">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="1c6b3-119">Vertex Shader</span></span> | <span data-ttu-id="1c6b3-120">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="1c6b3-120">Geometry Shader</span></span> | <span data-ttu-id="1c6b3-121">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="1c6b3-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1c6b3-122">x</span><span class="sxs-lookup"><span data-stu-id="1c6b3-122">x</span></span>             | <span data-ttu-id="1c6b3-123">x</span><span class="sxs-lookup"><span data-stu-id="1c6b3-123">x</span></span>               | <span data-ttu-id="1c6b3-124">x</span><span class="sxs-lookup"><span data-stu-id="1c6b3-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1c6b3-125">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1c6b3-125">Minimum Shader Model</span></span>

<span data-ttu-id="1c6b3-126">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1c6b3-127">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1c6b3-127">Shader Model</span></span>                                              | <span data-ttu-id="1c6b3-128">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="1c6b3-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1c6b3-129">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="1c6b3-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1c6b3-130">да</span><span class="sxs-lookup"><span data-stu-id="1c6b3-130">yes</span></span>       |
| [<span data-ttu-id="1c6b3-131">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="1c6b3-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1c6b3-132">да</span><span class="sxs-lookup"><span data-stu-id="1c6b3-132">yes</span></span>       |
| [<span data-ttu-id="1c6b3-133">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="1c6b3-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1c6b3-134">да</span><span class="sxs-lookup"><span data-stu-id="1c6b3-134">yes</span></span>       |
| [<span data-ttu-id="1c6b3-135">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c6b3-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1c6b3-136">Нет</span><span class="sxs-lookup"><span data-stu-id="1c6b3-136">no</span></span>        |
| [<span data-ttu-id="1c6b3-137">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c6b3-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1c6b3-138">Нет</span><span class="sxs-lookup"><span data-stu-id="1c6b3-138">no</span></span>        |
| [<span data-ttu-id="1c6b3-139">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c6b3-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1c6b3-140">Нет</span><span class="sxs-lookup"><span data-stu-id="1c6b3-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1c6b3-141">См. также</span><span class="sxs-lookup"><span data-stu-id="1c6b3-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c6b3-142">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c6b3-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





