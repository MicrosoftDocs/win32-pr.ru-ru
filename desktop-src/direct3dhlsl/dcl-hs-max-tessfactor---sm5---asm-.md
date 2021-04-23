---
title: dcl_hs_max_tessfactor (SM5-ASM)
description: Объявите Макстессфактор для исправления.
ms.assetid: 7EF0FD81-69FE-49F6-95DF-0C452A90A713
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69bd20fc8f4a3687988e8b100975f74016a45ae6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996990"
---
# <a name="dcl_hs_max_tessfactor-sm5---asm"></a><span data-ttu-id="0f7e4-103">дкл \_ HS \_ Max \_ тессфактор (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="0f7e4-103">dcl\_hs\_max\_tessfactor (sm5 - asm)</span></span>

<span data-ttu-id="0f7e4-104">Объявите Макстессфактор для исправления.</span><span class="sxs-lookup"><span data-stu-id="0f7e4-104">Declare the maxTessFactor for the patch.</span></span>



| <span data-ttu-id="0f7e4-105">дкл \_ HS \_ Max \_ тессфактор n</span><span class="sxs-lookup"><span data-stu-id="0f7e4-105">dcl\_hs\_max\_tessfactor n</span></span> |
|----------------------------|



 



| <span data-ttu-id="0f7e4-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="0f7e4-106">Item</span></span>                                                   | <span data-ttu-id="0f7e4-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0f7e4-107">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="0f7e4-108"><span id="n"></span><span id="N"></span>*\n*</span><span class="sxs-lookup"><span data-stu-id="0f7e4-108"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="0f7e4-109">\[в \] макстессфактор.</span><span class="sxs-lookup"><span data-stu-id="0f7e4-109">\[in\] The maxTessFactor.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0f7e4-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="0f7e4-110">Remarks</span></span>

<span data-ttu-id="0f7e4-111">Макстессфактор — это значение float32 в диапазоне {1,0... 64,0}.</span><span class="sxs-lookup"><span data-stu-id="0f7e4-111">The maxTessFactor is a float32 value in the range {1.0 ... 64.0}.</span></span>

<span data-ttu-id="0f7e4-112">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="0f7e4-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0f7e4-113">Вершина</span><span class="sxs-lookup"><span data-stu-id="0f7e4-113">Vertex</span></span> | <span data-ttu-id="0f7e4-114">Поверхности</span><span class="sxs-lookup"><span data-stu-id="0f7e4-114">Hull</span></span> | <span data-ttu-id="0f7e4-115">Домен</span><span class="sxs-lookup"><span data-stu-id="0f7e4-115">Domain</span></span> | <span data-ttu-id="0f7e4-116">Геометрия</span><span class="sxs-lookup"><span data-stu-id="0f7e4-116">Geometry</span></span> | <span data-ttu-id="0f7e4-117">Пиксель</span><span class="sxs-lookup"><span data-stu-id="0f7e4-117">Pixel</span></span> | <span data-ttu-id="0f7e4-118">Вычисления</span><span class="sxs-lookup"><span data-stu-id="0f7e4-118">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="0f7e4-119">X</span><span class="sxs-lookup"><span data-stu-id="0f7e4-119">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0f7e4-120">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0f7e4-120">Minimum Shader Model</span></span>

<span data-ttu-id="0f7e4-121">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="0f7e4-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0f7e4-122">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0f7e4-122">Shader Model</span></span>                                              | <span data-ttu-id="0f7e4-123">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="0f7e4-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0f7e4-124">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="0f7e4-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0f7e4-125">да</span><span class="sxs-lookup"><span data-stu-id="0f7e4-125">yes</span></span>       |
| [<span data-ttu-id="0f7e4-126">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="0f7e4-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0f7e4-127">Нет</span><span class="sxs-lookup"><span data-stu-id="0f7e4-127">no</span></span>        |
| [<span data-ttu-id="0f7e4-128">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="0f7e4-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0f7e4-129">Нет</span><span class="sxs-lookup"><span data-stu-id="0f7e4-129">no</span></span>        |
| [<span data-ttu-id="0f7e4-130">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f7e4-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0f7e4-131">Нет</span><span class="sxs-lookup"><span data-stu-id="0f7e4-131">no</span></span>        |
| [<span data-ttu-id="0f7e4-132">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f7e4-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0f7e4-133">Нет</span><span class="sxs-lookup"><span data-stu-id="0f7e4-133">no</span></span>        |
| [<span data-ttu-id="0f7e4-134">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f7e4-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0f7e4-135">Нет</span><span class="sxs-lookup"><span data-stu-id="0f7e4-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0f7e4-136">См. также</span><span class="sxs-lookup"><span data-stu-id="0f7e4-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f7e4-137">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f7e4-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





