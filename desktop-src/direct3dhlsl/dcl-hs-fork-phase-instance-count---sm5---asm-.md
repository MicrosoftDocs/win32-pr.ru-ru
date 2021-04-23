---
title: dcl_hs_fork_phase_instance_count (SM5-ASM)
description: Объявите число экземпляров фазы ветвления на фазе ветвления шейдера поверхности.
ms.assetid: E38C48BB-3439-4F63-8DF8-21CF562CF5E6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3459b43c22f60699445f3ef05e5323e268eeb71
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412246"
---
# <a name="dcl_hs_fork_phase_instance_count-sm5---asm"></a><span data-ttu-id="232e9-103">\_ \_ \_ число экземпляров фаз дкл \_ HS \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="232e9-103">dcl\_hs\_fork\_phase\_instance\_count (sm5 - asm)</span></span>

<span data-ttu-id="232e9-104">Объявите число экземпляров фазы ветвления на фазе ветвления шейдера поверхности.</span><span class="sxs-lookup"><span data-stu-id="232e9-104">Declare the fork phase instance count in a hull shader fork phase.</span></span>



| <span data-ttu-id="232e9-105">\_ \_ \_ число экземпляров этапа дкл \_ HS \_ {1... Max 32-bit uint}</span><span class="sxs-lookup"><span data-stu-id="232e9-105">dcl\_hs\_fork\_phase\_instance\_count {1...max 32-bit UINT}</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="232e9-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="232e9-106">Item</span></span>                                                   | <span data-ttu-id="232e9-107">Описание</span><span class="sxs-lookup"><span data-stu-id="232e9-107">Description</span></span>                           |
|--------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="232e9-108"><span id="N"></span><span id="n"></span>*\N*</span><span class="sxs-lookup"><span data-stu-id="232e9-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="232e9-109">\[в \] поле число экземпляров.</span><span class="sxs-lookup"><span data-stu-id="232e9-109">\[in\] The instance count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="232e9-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="232e9-110">Remarks</span></span>

<span data-ttu-id="232e9-111">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="232e9-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="232e9-112">Вершина</span><span class="sxs-lookup"><span data-stu-id="232e9-112">Vertex</span></span> | <span data-ttu-id="232e9-113">Поверхности</span><span class="sxs-lookup"><span data-stu-id="232e9-113">Hull</span></span> | <span data-ttu-id="232e9-114">Домен</span><span class="sxs-lookup"><span data-stu-id="232e9-114">Domain</span></span> | <span data-ttu-id="232e9-115">Геометрия</span><span class="sxs-lookup"><span data-stu-id="232e9-115">Geometry</span></span> | <span data-ttu-id="232e9-116">Пиксель</span><span class="sxs-lookup"><span data-stu-id="232e9-116">Pixel</span></span> | <span data-ttu-id="232e9-117">Вычисления</span><span class="sxs-lookup"><span data-stu-id="232e9-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="232e9-118">X</span><span class="sxs-lookup"><span data-stu-id="232e9-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="232e9-119">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="232e9-119">Minimum Shader Model</span></span>

<span data-ttu-id="232e9-120">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="232e9-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="232e9-121">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="232e9-121">Shader Model</span></span>                                              | <span data-ttu-id="232e9-122">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="232e9-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="232e9-123">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="232e9-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="232e9-124">да</span><span class="sxs-lookup"><span data-stu-id="232e9-124">yes</span></span>       |
| [<span data-ttu-id="232e9-125">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="232e9-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="232e9-126">Нет</span><span class="sxs-lookup"><span data-stu-id="232e9-126">no</span></span>        |
| [<span data-ttu-id="232e9-127">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="232e9-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="232e9-128">Нет</span><span class="sxs-lookup"><span data-stu-id="232e9-128">no</span></span>        |
| [<span data-ttu-id="232e9-129">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="232e9-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="232e9-130">Нет</span><span class="sxs-lookup"><span data-stu-id="232e9-130">no</span></span>        |
| [<span data-ttu-id="232e9-131">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="232e9-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="232e9-132">Нет</span><span class="sxs-lookup"><span data-stu-id="232e9-132">no</span></span>        |
| [<span data-ttu-id="232e9-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="232e9-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="232e9-134">Нет</span><span class="sxs-lookup"><span data-stu-id="232e9-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="232e9-135">См. также</span><span class="sxs-lookup"><span data-stu-id="232e9-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="232e9-136">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="232e9-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





