---
title: фтау (SM4-ASM)
description: Преобразование с плавающей запятой в беззнаковое целое число.
ms.assetid: 0E3E090B-72C0-4CED-AFA5-2DDCF67D7263
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4a5e65e4bb9d4e71e4a2000f00861cf63e7c181
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335488"
---
# <a name="ftou-sm4---asm"></a><span data-ttu-id="8052d-103">фтау (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8052d-103">ftou (sm4 - asm)</span></span>

<span data-ttu-id="8052d-104">Преобразование с плавающей запятой в беззнаковое целое число.</span><span class="sxs-lookup"><span data-stu-id="8052d-104">Floating point to unsigned integer conversion.</span></span>



| <span data-ttu-id="8052d-105">фтау dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="8052d-105">ftou dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="8052d-106">фтои dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="8052d-106">ftoi dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="8052d-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="8052d-107">Item</span></span>                                                            | <span data-ttu-id="8052d-108">Описание</span><span class="sxs-lookup"><span data-stu-id="8052d-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="8052d-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="8052d-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="8052d-110">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="8052d-110">\[in\] The address of the result of the operation.</span></span> <br/> |
| <span data-ttu-id="8052d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="8052d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="8052d-112">\[\]преобразуемое значение.</span><span class="sxs-lookup"><span data-stu-id="8052d-112">\[in\] The value to convert.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="8052d-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="8052d-113">Remarks</span></span>

<span data-ttu-id="8052d-114">Преобразование выполняется для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="8052d-114">The conversion is performed per-component.</span></span> <span data-ttu-id="8052d-115">Округление всегда выполняется в сторону нуля, в соответствии с соглашением C для приведения типа float к типу int.</span><span class="sxs-lookup"><span data-stu-id="8052d-115">Rounding is always performed towards zero, following the C convention for casts from float to int.</span></span>

<span data-ttu-id="8052d-116">Приложения, для которых требуется другая семантика округления, могут вызывать **округленные** инструкции перед приведением к целому числу.</span><span class="sxs-lookup"><span data-stu-id="8052d-116">Applications that require different rounding semantics can invoke the **round** instructions before casting to integer.</span></span>

<span data-ttu-id="8052d-117">Входные данные записываются в диапазон \[ 0,0 f... 4294967295.999 f \] перед преобразованием, а входные значения NaN дают нулевой результат.</span><span class="sxs-lookup"><span data-stu-id="8052d-117">Inputs are clamped to the range \[0.0f ... 4294967295.999f\] prior to conversion, and input NaN values produce a zero result.</span></span>

<span data-ttu-id="8052d-118">Необязательные модификаторы отрицания и абсолютные значения применяются к исходным значениям перед преобразованием.</span><span class="sxs-lookup"><span data-stu-id="8052d-118">Optional negate and absolute value modifiers are applied to the source values before conversion.</span></span>

<span data-ttu-id="8052d-119">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="8052d-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8052d-120">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="8052d-120">Vertex Shader</span></span> | <span data-ttu-id="8052d-121">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="8052d-121">Geometry Shader</span></span> | <span data-ttu-id="8052d-122">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="8052d-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8052d-123">x</span><span class="sxs-lookup"><span data-stu-id="8052d-123">x</span></span>             | <span data-ttu-id="8052d-124">x</span><span class="sxs-lookup"><span data-stu-id="8052d-124">x</span></span>               | <span data-ttu-id="8052d-125">x</span><span class="sxs-lookup"><span data-stu-id="8052d-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8052d-126">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8052d-126">Minimum Shader Model</span></span>

<span data-ttu-id="8052d-127">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="8052d-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8052d-128">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8052d-128">Shader Model</span></span>                                              | <span data-ttu-id="8052d-129">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8052d-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8052d-130">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="8052d-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8052d-131">да</span><span class="sxs-lookup"><span data-stu-id="8052d-131">yes</span></span>       |
| [<span data-ttu-id="8052d-132">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="8052d-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8052d-133">да</span><span class="sxs-lookup"><span data-stu-id="8052d-133">yes</span></span>       |
| [<span data-ttu-id="8052d-134">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="8052d-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8052d-135">да</span><span class="sxs-lookup"><span data-stu-id="8052d-135">yes</span></span>       |
| [<span data-ttu-id="8052d-136">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8052d-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8052d-137">Нет</span><span class="sxs-lookup"><span data-stu-id="8052d-137">no</span></span>        |
| [<span data-ttu-id="8052d-138">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8052d-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8052d-139">Нет</span><span class="sxs-lookup"><span data-stu-id="8052d-139">no</span></span>        |
| [<span data-ttu-id="8052d-140">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8052d-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8052d-141">Нет</span><span class="sxs-lookup"><span data-stu-id="8052d-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8052d-142">См. также</span><span class="sxs-lookup"><span data-stu-id="8052d-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8052d-143">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8052d-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





