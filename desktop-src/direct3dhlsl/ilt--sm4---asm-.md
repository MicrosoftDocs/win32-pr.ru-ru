---
title: илт (SM4-ASM)
description: Компонентно-ориентированное векторное число меньше, чем сравнение.
ms.assetid: 5F06E568-6234-4778-8169-D8352FAB5297
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c2e5e47272412bb483e4782e9a6c35e971293c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335472"
---
# <a name="ilt-sm4---asm"></a><span data-ttu-id="6e03d-103">илт (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="6e03d-103">ilt (sm4 - asm)</span></span>

<span data-ttu-id="6e03d-104">Компонентно-ориентированное векторное число меньше, чем сравнение.</span><span class="sxs-lookup"><span data-stu-id="6e03d-104">Component-wise vector integer less-than comparison.</span></span>



| <span data-ttu-id="6e03d-105">илт dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="6e03d-105">ilt dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="6e03d-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="6e03d-106">Item</span></span>                                                            | <span data-ttu-id="6e03d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="6e03d-107">Description</span></span>                                       |
|-----------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="6e03d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="6e03d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="6e03d-109">Результат операции.</span><span class="sxs-lookup"><span data-stu-id="6e03d-109">The result of the operation.</span></span><br/>           |
| <span data-ttu-id="6e03d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6e03d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6e03d-111">\[в \] значении, сравниваемом с *src1*.</span><span class="sxs-lookup"><span data-stu-id="6e03d-111">\[in\] The value to compare to *src1*.</span></span><br/> |
| <span data-ttu-id="6e03d-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="6e03d-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="6e03d-113">\[в \] значении, сравниваемом с *src0*.</span><span class="sxs-lookup"><span data-stu-id="6e03d-113">\[in\] The value to compare to *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6e03d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6e03d-114">Remarks</span></span>

<span data-ttu-id="6e03d-115">Выполняет сравнение целых чисел *(src0*  <  *src1*) для каждого компонента и записывает результат в *dest*.</span><span class="sxs-lookup"><span data-stu-id="6e03d-115">Performs the integer comparison *(src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="6e03d-116">Если сравнение истинно, то для этого компонента возвращается значение 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="6e03d-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="6e03d-117">В противном случае возвращается 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="6e03d-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="6e03d-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="6e03d-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6e03d-119">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="6e03d-119">Vertex Shader</span></span> | <span data-ttu-id="6e03d-120">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="6e03d-120">Geometry Shader</span></span> | <span data-ttu-id="6e03d-121">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="6e03d-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="6e03d-122">x</span><span class="sxs-lookup"><span data-stu-id="6e03d-122">x</span></span>             | <span data-ttu-id="6e03d-123">x</span><span class="sxs-lookup"><span data-stu-id="6e03d-123">x</span></span>               | <span data-ttu-id="6e03d-124">x</span><span class="sxs-lookup"><span data-stu-id="6e03d-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6e03d-125">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="6e03d-125">Minimum Shader Model</span></span>



| <span data-ttu-id="6e03d-126">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="6e03d-126">Shader Model</span></span>                                              | <span data-ttu-id="6e03d-127">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="6e03d-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6e03d-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="6e03d-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6e03d-129">да</span><span class="sxs-lookup"><span data-stu-id="6e03d-129">yes</span></span>       |
| [<span data-ttu-id="6e03d-130">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="6e03d-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6e03d-131">да</span><span class="sxs-lookup"><span data-stu-id="6e03d-131">yes</span></span>       |
| [<span data-ttu-id="6e03d-132">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="6e03d-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6e03d-133">да</span><span class="sxs-lookup"><span data-stu-id="6e03d-133">yes</span></span>       |
| [<span data-ttu-id="6e03d-134">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e03d-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6e03d-135">Нет</span><span class="sxs-lookup"><span data-stu-id="6e03d-135">no</span></span>        |
| [<span data-ttu-id="6e03d-136">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e03d-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6e03d-137">Нет</span><span class="sxs-lookup"><span data-stu-id="6e03d-137">no</span></span>        |
| [<span data-ttu-id="6e03d-138">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e03d-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6e03d-139">Нет</span><span class="sxs-lookup"><span data-stu-id="6e03d-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6e03d-140">См. также</span><span class="sxs-lookup"><span data-stu-id="6e03d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e03d-141">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e03d-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





