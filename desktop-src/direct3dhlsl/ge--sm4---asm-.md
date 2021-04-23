---
title: GE (SM4-ASM)
description: Сравнение на уровне компонентов с плавающей точкой "больше или равно".
ms.assetid: 658AF249-4935-41AF-972A-D8CDEABA76AA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93d21d9ac044e2ad4d63e954a4732a15794b123
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412161"
---
# <a name="ge-sm4---asm"></a><span data-ttu-id="1800c-103">GE (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="1800c-103">ge (sm4 - asm)</span></span>

<span data-ttu-id="1800c-104">Сравнение на уровне компонентов с плавающей точкой "больше или равно".</span><span class="sxs-lookup"><span data-stu-id="1800c-104">Component-wise vector floating point greater-than-or-equal comparison.</span></span>



| <span data-ttu-id="1800c-105">GE dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS. \] \[ свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="1800c-105">ge dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="1800c-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="1800c-106">Item</span></span>                                                            | <span data-ttu-id="1800c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1800c-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="1800c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="1800c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1800c-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="1800c-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="1800c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1800c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1800c-111">\[в \] компоненте для сравнения с *src1*.</span><span class="sxs-lookup"><span data-stu-id="1800c-111">\[in\] The component to compare to *src1*.</span></span><br/>         |
| <span data-ttu-id="1800c-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="1800c-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="1800c-113">\[в \] компоненте для сравнения с *src0*.</span><span class="sxs-lookup"><span data-stu-id="1800c-113">\[in\] The component to compare to *src0*.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="1800c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="1800c-114">Remarks</span></span>

<span data-ttu-id="1800c-115">Выполняет сравнение с плавающей запятой (*src0*  >=  *src1*) для каждого компонента и записывает результат в *dest*.</span><span class="sxs-lookup"><span data-stu-id="1800c-115">Performs the float comparison (*src0* >= *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="1800c-116">Если сравнение истинно, то для этого компонента возвращается значение 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="1800c-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="1800c-117">В противном случае возвращается 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="1800c-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="1800c-118">Перед сравнением выполняется очистка, а исходные регистры исходного кода не затрагиваются.</span><span class="sxs-lookup"><span data-stu-id="1800c-118">Denorms are flushed before comparison, and original source registers are untouched.</span></span> <span data-ttu-id="1800c-119">+ 0 равно-0.</span><span class="sxs-lookup"><span data-stu-id="1800c-119">+0 equals -0.</span></span> <span data-ttu-id="1800c-120">Сравнение с NaN возвращает false.</span><span class="sxs-lookup"><span data-stu-id="1800c-120">Comparison with NaN returns false.</span></span>

<span data-ttu-id="1800c-121">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="1800c-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1800c-122">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="1800c-122">Vertex Shader</span></span> | <span data-ttu-id="1800c-123">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="1800c-123">Geometry Shader</span></span> | <span data-ttu-id="1800c-124">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="1800c-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1800c-125">x</span><span class="sxs-lookup"><span data-stu-id="1800c-125">x</span></span>             | <span data-ttu-id="1800c-126">x</span><span class="sxs-lookup"><span data-stu-id="1800c-126">x</span></span>               | <span data-ttu-id="1800c-127">x</span><span class="sxs-lookup"><span data-stu-id="1800c-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1800c-128">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1800c-128">Minimum Shader Model</span></span>

<span data-ttu-id="1800c-129">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="1800c-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1800c-130">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1800c-130">Shader Model</span></span>                                              | <span data-ttu-id="1800c-131">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="1800c-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1800c-132">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="1800c-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1800c-133">да</span><span class="sxs-lookup"><span data-stu-id="1800c-133">yes</span></span>       |
| [<span data-ttu-id="1800c-134">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="1800c-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1800c-135">да</span><span class="sxs-lookup"><span data-stu-id="1800c-135">yes</span></span>       |
| [<span data-ttu-id="1800c-136">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="1800c-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1800c-137">да</span><span class="sxs-lookup"><span data-stu-id="1800c-137">yes</span></span>       |
| [<span data-ttu-id="1800c-138">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1800c-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1800c-139">Нет</span><span class="sxs-lookup"><span data-stu-id="1800c-139">no</span></span>        |
| [<span data-ttu-id="1800c-140">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1800c-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1800c-141">Нет</span><span class="sxs-lookup"><span data-stu-id="1800c-141">no</span></span>        |
| [<span data-ttu-id="1800c-142">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1800c-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1800c-143">Нет</span><span class="sxs-lookup"><span data-stu-id="1800c-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1800c-144">См. также</span><span class="sxs-lookup"><span data-stu-id="1800c-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1800c-145">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1800c-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





