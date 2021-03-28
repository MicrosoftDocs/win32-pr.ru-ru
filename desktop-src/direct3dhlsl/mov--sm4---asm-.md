---
title: MOV (SM4-ASM)
description: Перемещение на уровне компонентов. | MOV (SM4-ASM)
ms.assetid: A8865237-59D3-4332-9F09-157E10C4FFC6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f029cd8a31a9348e729681878773c225b87b9fbb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273401"
---
# <a name="mov-sm4---asm"></a><span data-ttu-id="33647-104">MOV (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="33647-104">mov (sm4 - asm)</span></span>

<span data-ttu-id="33647-105">Перемещение на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="33647-105">Component-wise move.</span></span>



| <span data-ttu-id="33647-106">Инструкция: MOV \[ \_ Кот \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="33647-106">Instruction: mov\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------|



 



| <span data-ttu-id="33647-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="33647-107">Item</span></span>                                                            | <span data-ttu-id="33647-108">Описание</span><span class="sxs-lookup"><span data-stu-id="33647-108">Description</span></span>                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="33647-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="33647-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="33647-110">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="33647-110">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="33647-111">*конечный адрес*  =  *src0*</span><span class="sxs-lookup"><span data-stu-id="33647-111">*dest* = *src0*</span></span><br/> |
| <span data-ttu-id="33647-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="33647-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="33647-113">\[в \] перемещаемых компонентах.</span><span class="sxs-lookup"><span data-stu-id="33647-113">\[in\] The components to move.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="33647-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="33647-114">Remarks</span></span>

<span data-ttu-id="33647-115">Модификаторы, отличные от свиззле, предполагают, что данные являются плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="33647-115">The modifiers, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="33647-116">Отсутствие модификаторов просто перемещает данные без изменения битов.</span><span class="sxs-lookup"><span data-stu-id="33647-116">The absence of modifiers just moves data without altering bits.</span></span>

<span data-ttu-id="33647-117">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="33647-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="33647-118">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="33647-118">Vertex Shader</span></span> | <span data-ttu-id="33647-119">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="33647-119">Geometry Shader</span></span> | <span data-ttu-id="33647-120">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="33647-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="33647-121">x</span><span class="sxs-lookup"><span data-stu-id="33647-121">x</span></span>             | <span data-ttu-id="33647-122">x</span><span class="sxs-lookup"><span data-stu-id="33647-122">x</span></span>               | <span data-ttu-id="33647-123">x</span><span class="sxs-lookup"><span data-stu-id="33647-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="33647-124">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="33647-124">Minimum Shader Model</span></span>

<span data-ttu-id="33647-125">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="33647-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="33647-126">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="33647-126">Shader Model</span></span>                                              | <span data-ttu-id="33647-127">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="33647-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="33647-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="33647-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="33647-129">да</span><span class="sxs-lookup"><span data-stu-id="33647-129">yes</span></span>       |
| [<span data-ttu-id="33647-130">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="33647-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="33647-131">да</span><span class="sxs-lookup"><span data-stu-id="33647-131">yes</span></span>       |
| [<span data-ttu-id="33647-132">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="33647-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="33647-133">да</span><span class="sxs-lookup"><span data-stu-id="33647-133">yes</span></span>       |
| [<span data-ttu-id="33647-134">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33647-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="33647-135">Нет</span><span class="sxs-lookup"><span data-stu-id="33647-135">no</span></span>        |
| [<span data-ttu-id="33647-136">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33647-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="33647-137">Нет</span><span class="sxs-lookup"><span data-stu-id="33647-137">no</span></span>        |
| [<span data-ttu-id="33647-138">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33647-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="33647-139">Нет</span><span class="sxs-lookup"><span data-stu-id="33647-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="33647-140">См. также</span><span class="sxs-lookup"><span data-stu-id="33647-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33647-141">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33647-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





