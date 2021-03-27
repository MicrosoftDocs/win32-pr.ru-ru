---
title: Mad (SM4-ASM)
description: Добавление на уровне компонентов.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d34823cdb3545f29426117b35903c97c08c5807
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069333"
---
# <a name="mad-sm4---asm"></a><span data-ttu-id="ecc49-103">Mad (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ecc49-103">mad (sm4 - asm)</span></span>

<span data-ttu-id="ecc49-104">& добавления на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="ecc49-104">Component-wise multiply & add.</span></span>



| <span data-ttu-id="ecc49-105">: Mad No \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src2 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="ecc49-105">:mad\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="ecc49-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="ecc49-106">Item</span></span>                                                            | <span data-ttu-id="ecc49-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ecc49-107">Description</span></span>                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc49-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ecc49-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ecc49-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="ecc49-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="ecc49-110">*конечный адрес*  =  *src0* \* *src1*  +  *src2*</span><span class="sxs-lookup"><span data-stu-id="ecc49-110">*dest* = *src0* \* *src1* + *src2*</span></span><br/> |
| <span data-ttu-id="ecc49-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ecc49-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ecc49-112">\[в \] множимое.</span><span class="sxs-lookup"><span data-stu-id="ecc49-112">\[in\] The multiplicand.</span></span><br/>                                                          |
| <span data-ttu-id="ecc49-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="ecc49-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="ecc49-114">\[в \] множители.</span><span class="sxs-lookup"><span data-stu-id="ecc49-114">\[in\] The multiplier.</span></span><br/>                                                            |
| <span data-ttu-id="ecc49-115"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="ecc49-115"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="ecc49-116">\[в \] слагаемое.</span><span class="sxs-lookup"><span data-stu-id="ecc49-116">\[in\] The addend.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="ecc49-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="ecc49-117">Remarks</span></span>

<span data-ttu-id="ecc49-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="ecc49-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ecc49-119">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="ecc49-119">Vertex Shader</span></span> | <span data-ttu-id="ecc49-120">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="ecc49-120">Geometry Shader</span></span> | <span data-ttu-id="ecc49-121">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="ecc49-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ecc49-122">x</span><span class="sxs-lookup"><span data-stu-id="ecc49-122">x</span></span>             | <span data-ttu-id="ecc49-123">x</span><span class="sxs-lookup"><span data-stu-id="ecc49-123">x</span></span>               | <span data-ttu-id="ecc49-124">x</span><span class="sxs-lookup"><span data-stu-id="ecc49-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ecc49-125">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ecc49-125">Minimum Shader Model</span></span>

<span data-ttu-id="ecc49-126">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="ecc49-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ecc49-127">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ecc49-127">Shader Model</span></span>                                              | <span data-ttu-id="ecc49-128">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ecc49-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ecc49-129">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ecc49-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ecc49-130">да</span><span class="sxs-lookup"><span data-stu-id="ecc49-130">yes</span></span>       |
| [<span data-ttu-id="ecc49-131">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="ecc49-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ecc49-132">да</span><span class="sxs-lookup"><span data-stu-id="ecc49-132">yes</span></span>       |
| [<span data-ttu-id="ecc49-133">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="ecc49-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ecc49-134">да</span><span class="sxs-lookup"><span data-stu-id="ecc49-134">yes</span></span>       |
| [<span data-ttu-id="ecc49-135">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecc49-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ecc49-136">Нет</span><span class="sxs-lookup"><span data-stu-id="ecc49-136">no</span></span>        |
| [<span data-ttu-id="ecc49-137">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecc49-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ecc49-138">Нет</span><span class="sxs-lookup"><span data-stu-id="ecc49-138">no</span></span>        |
| [<span data-ttu-id="ecc49-139">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecc49-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ecc49-140">Нет</span><span class="sxs-lookup"><span data-stu-id="ecc49-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ecc49-141">См. также</span><span class="sxs-lookup"><span data-stu-id="ecc49-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecc49-142">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecc49-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





