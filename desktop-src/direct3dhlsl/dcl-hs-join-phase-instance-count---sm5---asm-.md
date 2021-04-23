---
title: dcl_hs_join_phase_instance_count (SM5-ASM)
description: Объявите число экземпляров фазы соединения на фазе присоединения шейдера поверхности.
ms.assetid: 9951B849-0537-4D08-9ADE-8CF6FF51A193
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34c3acc7074170ab4561a54e67668698d58b7ac1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412247"
---
# <a name="dcl_hs_join_phase_instance_count-sm5---asm"></a><span data-ttu-id="2c024-103">\_ \_ \_ число экземпляров фазы соединения дкл HS \_ \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2c024-103">dcl\_hs\_join\_phase\_instance\_count (sm5 - asm)</span></span>

<span data-ttu-id="2c024-104">Объявите число экземпляров фазы соединения на фазе присоединения шейдера поверхности.</span><span class="sxs-lookup"><span data-stu-id="2c024-104">Declare the join phase instance count in a hull shader join phase.</span></span>



| <span data-ttu-id="2c024-105">\_ \_ \_ число экземпляров фазы соединения дкл HS \_ \_ {1... Max 32-bit uint}</span><span class="sxs-lookup"><span data-stu-id="2c024-105">dcl\_hs\_join\_phase\_instance\_count {1... max 32-bit UINT}</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="2c024-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="2c024-106">Item</span></span>                                                   | <span data-ttu-id="2c024-107">Описание</span><span class="sxs-lookup"><span data-stu-id="2c024-107">Description</span></span>                           |
|--------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="2c024-108"><span id="N"></span><span id="n"></span>*\N*</span><span class="sxs-lookup"><span data-stu-id="2c024-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="2c024-109">\[в \] поле число экземпляров.</span><span class="sxs-lookup"><span data-stu-id="2c024-109">\[in\] The instance count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2c024-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="2c024-110">Remarks</span></span>

<span data-ttu-id="2c024-111">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="2c024-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2c024-112">Вершина</span><span class="sxs-lookup"><span data-stu-id="2c024-112">Vertex</span></span> | <span data-ttu-id="2c024-113">Поверхности</span><span class="sxs-lookup"><span data-stu-id="2c024-113">Hull</span></span> | <span data-ttu-id="2c024-114">Домен</span><span class="sxs-lookup"><span data-stu-id="2c024-114">Domain</span></span> | <span data-ttu-id="2c024-115">Геометрия</span><span class="sxs-lookup"><span data-stu-id="2c024-115">Geometry</span></span> | <span data-ttu-id="2c024-116">Пиксель</span><span class="sxs-lookup"><span data-stu-id="2c024-116">Pixel</span></span> | <span data-ttu-id="2c024-117">Вычисления</span><span class="sxs-lookup"><span data-stu-id="2c024-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="2c024-118">X</span><span class="sxs-lookup"><span data-stu-id="2c024-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2c024-119">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2c024-119">Minimum Shader Model</span></span>

<span data-ttu-id="2c024-120">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="2c024-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2c024-121">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2c024-121">Shader Model</span></span>                                              | <span data-ttu-id="2c024-122">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="2c024-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2c024-123">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="2c024-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2c024-124">да</span><span class="sxs-lookup"><span data-stu-id="2c024-124">yes</span></span>       |
| [<span data-ttu-id="2c024-125">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="2c024-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2c024-126">Нет</span><span class="sxs-lookup"><span data-stu-id="2c024-126">no</span></span>        |
| [<span data-ttu-id="2c024-127">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="2c024-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2c024-128">Нет</span><span class="sxs-lookup"><span data-stu-id="2c024-128">no</span></span>        |
| [<span data-ttu-id="2c024-129">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c024-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2c024-130">Нет</span><span class="sxs-lookup"><span data-stu-id="2c024-130">no</span></span>        |
| [<span data-ttu-id="2c024-131">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c024-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2c024-132">Нет</span><span class="sxs-lookup"><span data-stu-id="2c024-132">no</span></span>        |
| [<span data-ttu-id="2c024-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c024-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2c024-134">Нет</span><span class="sxs-lookup"><span data-stu-id="2c024-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2c024-135">См. также</span><span class="sxs-lookup"><span data-stu-id="2c024-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c024-136">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c024-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





