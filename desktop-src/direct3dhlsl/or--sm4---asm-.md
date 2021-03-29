---
title: или (SM4-ASM)
description: Побитовое или.
ms.assetid: BBC06F8C-4C86-4077-A1F9-383D6A8FBED3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62064189725b246cc48bbde03a9c094d13f8b9a0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996943"
---
# <a name="or-sm4---asm"></a><span data-ttu-id="40b87-103">или (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="40b87-103">or (sm4 - asm)</span></span>

<span data-ttu-id="40b87-104">Побитовое или.</span><span class="sxs-lookup"><span data-stu-id="40b87-104">Bitwise or.</span></span>



| <span data-ttu-id="40b87-105">или DEST \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="40b87-105">or dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|------------------------------------------------------|



 



| <span data-ttu-id="40b87-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="40b87-106">Item</span></span>                                                            | <span data-ttu-id="40b87-107">Описание</span><span class="sxs-lookup"><span data-stu-id="40b87-107">Description</span></span>                                         |
|-----------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="40b87-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="40b87-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="40b87-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="40b87-109">\[in\] The result of the operation.</span></span><br/>      |
| <span data-ttu-id="40b87-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="40b87-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="40b87-111">\[в \] компонентах или с *src1*.</span><span class="sxs-lookup"><span data-stu-id="40b87-111">\[in\] The components to OR with *src1*.</span></span><br/> |
| <span data-ttu-id="40b87-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="40b87-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="40b87-113">\[в \] компонентах или с *src0*.</span><span class="sxs-lookup"><span data-stu-id="40b87-113">\[in\] The components to OR with *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="40b87-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="40b87-114">Remarks</span></span>

<span data-ttu-id="40b87-115">Эта инструкция выполняет покомпонентную логическую операцию или для каждой пары 32-разрядных значений из *src0* и *src1*.</span><span class="sxs-lookup"><span data-stu-id="40b87-115">This instruction performs a component-wise logical OR of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="40b87-116">32-разрядные результаты помещаются в *dest*.</span><span class="sxs-lookup"><span data-stu-id="40b87-116">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="40b87-117">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="40b87-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="40b87-118">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="40b87-118">Vertex Shader</span></span> | <span data-ttu-id="40b87-119">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="40b87-119">Geometry Shader</span></span> | <span data-ttu-id="40b87-120">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="40b87-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="40b87-121">x</span><span class="sxs-lookup"><span data-stu-id="40b87-121">x</span></span>             | <span data-ttu-id="40b87-122">x</span><span class="sxs-lookup"><span data-stu-id="40b87-122">x</span></span>               | <span data-ttu-id="40b87-123">x</span><span class="sxs-lookup"><span data-stu-id="40b87-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="40b87-124">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="40b87-124">Minimum Shader Model</span></span>

<span data-ttu-id="40b87-125">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="40b87-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="40b87-126">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="40b87-126">Shader Model</span></span>                                              | <span data-ttu-id="40b87-127">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="40b87-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="40b87-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="40b87-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="40b87-129">да</span><span class="sxs-lookup"><span data-stu-id="40b87-129">yes</span></span>       |
| [<span data-ttu-id="40b87-130">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="40b87-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="40b87-131">да</span><span class="sxs-lookup"><span data-stu-id="40b87-131">yes</span></span>       |
| [<span data-ttu-id="40b87-132">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="40b87-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="40b87-133">да</span><span class="sxs-lookup"><span data-stu-id="40b87-133">yes</span></span>       |
| [<span data-ttu-id="40b87-134">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="40b87-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="40b87-135">Нет</span><span class="sxs-lookup"><span data-stu-id="40b87-135">no</span></span>        |
| [<span data-ttu-id="40b87-136">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="40b87-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="40b87-137">Нет</span><span class="sxs-lookup"><span data-stu-id="40b87-137">no</span></span>        |
| [<span data-ttu-id="40b87-138">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="40b87-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="40b87-139">Нет</span><span class="sxs-lookup"><span data-stu-id="40b87-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="40b87-140">См. также</span><span class="sxs-lookup"><span data-stu-id="40b87-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40b87-141">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="40b87-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





