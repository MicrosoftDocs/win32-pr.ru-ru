---
title: не (SM4-ASM)
description: Побитовое не.
ms.assetid: AC7EBBC2-4B52-4793-812C-B25897FB8D05
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0bf224e6e5af7f2db6bcbaf7ae287ba2d399727
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983885"
---
# <a name="not-sm4---asm"></a><span data-ttu-id="271de-103">не (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="271de-103">not (sm4 - asm)</span></span>

<span data-ttu-id="271de-104">Побитовое не.</span><span class="sxs-lookup"><span data-stu-id="271de-104">Bitwise not.</span></span>



| <span data-ttu-id="271de-105">не dest \[ . Mask \] , src0 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="271de-105">not dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------|



 



| <span data-ttu-id="271de-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="271de-106">Item</span></span>                                                            | <span data-ttu-id="271de-107">Описание</span><span class="sxs-lookup"><span data-stu-id="271de-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="271de-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="271de-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="271de-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="271de-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="271de-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="271de-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="271de-111">\[в \] исходных компонентах.</span><span class="sxs-lookup"><span data-stu-id="271de-111">\[in\] The original components.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="271de-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="271de-112">Remarks</span></span>

<span data-ttu-id="271de-113">Эта инструкция выполняет дополнение одного компонента для каждого 32-битного значения в *src0*.</span><span class="sxs-lookup"><span data-stu-id="271de-113">This instruction performs a component-wise one's complement of each 32-bit value in *src0*.</span></span> <span data-ttu-id="271de-114">32-разрядные результаты хранятся в *dest*.</span><span class="sxs-lookup"><span data-stu-id="271de-114">The 32-bit results are stored in *dest*.</span></span>

<span data-ttu-id="271de-115">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="271de-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="271de-116">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="271de-116">Vertex Shader</span></span> | <span data-ttu-id="271de-117">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="271de-117">Geometry Shader</span></span> | <span data-ttu-id="271de-118">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="271de-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="271de-119">x</span><span class="sxs-lookup"><span data-stu-id="271de-119">x</span></span>             | <span data-ttu-id="271de-120">x</span><span class="sxs-lookup"><span data-stu-id="271de-120">x</span></span>               | <span data-ttu-id="271de-121">x</span><span class="sxs-lookup"><span data-stu-id="271de-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="271de-122">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="271de-122">Minimum Shader Model</span></span>

<span data-ttu-id="271de-123">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="271de-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="271de-124">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="271de-124">Shader Model</span></span>                                              | <span data-ttu-id="271de-125">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="271de-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="271de-126">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="271de-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="271de-127">да</span><span class="sxs-lookup"><span data-stu-id="271de-127">yes</span></span>       |
| [<span data-ttu-id="271de-128">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="271de-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="271de-129">да</span><span class="sxs-lookup"><span data-stu-id="271de-129">yes</span></span>       |
| [<span data-ttu-id="271de-130">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="271de-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="271de-131">да</span><span class="sxs-lookup"><span data-stu-id="271de-131">yes</span></span>       |
| [<span data-ttu-id="271de-132">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="271de-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="271de-133">Нет</span><span class="sxs-lookup"><span data-stu-id="271de-133">no</span></span>        |
| [<span data-ttu-id="271de-134">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="271de-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="271de-135">Нет</span><span class="sxs-lookup"><span data-stu-id="271de-135">no</span></span>        |
| [<span data-ttu-id="271de-136">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="271de-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="271de-137">Нет</span><span class="sxs-lookup"><span data-stu-id="271de-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="271de-138">См. также</span><span class="sxs-lookup"><span data-stu-id="271de-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="271de-139">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="271de-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





