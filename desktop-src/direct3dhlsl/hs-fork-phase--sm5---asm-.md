---
title: hs_fork_phase (SM5-ASM)
description: Начните этап ветвления в шейдере поверхности.
ms.assetid: 13D6A06C-F001-45BE-8AB4-D7ACA73BF535
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9316cc92c1bf5683afa620927b3c6f38432c3c4e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412217"
---
# <a name="hs_fork_phase-sm5---asm"></a><span data-ttu-id="76a0b-103">\_фаза вилки HS \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="76a0b-103">hs\_fork\_phase (sm5 - asm)</span></span>

<span data-ttu-id="76a0b-104">Начните этап ветвления в шейдере поверхности.</span><span class="sxs-lookup"><span data-stu-id="76a0b-104">Start the fork phase in a hull shader.</span></span>



| <span data-ttu-id="76a0b-105">\_фаза вилки HS \_</span><span class="sxs-lookup"><span data-stu-id="76a0b-105">hs\_fork\_phase</span></span> |
|-----------------|



 

## <a name="remarks"></a><span data-ttu-id="76a0b-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="76a0b-106">Remarks</span></span>

<span data-ttu-id="76a0b-107">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="76a0b-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="76a0b-108">Вершина</span><span class="sxs-lookup"><span data-stu-id="76a0b-108">Vertex</span></span> | <span data-ttu-id="76a0b-109">Поверхности</span><span class="sxs-lookup"><span data-stu-id="76a0b-109">Hull</span></span> | <span data-ttu-id="76a0b-110">Домен</span><span class="sxs-lookup"><span data-stu-id="76a0b-110">Domain</span></span> | <span data-ttu-id="76a0b-111">Геометрия</span><span class="sxs-lookup"><span data-stu-id="76a0b-111">Geometry</span></span> | <span data-ttu-id="76a0b-112">Пиксель</span><span class="sxs-lookup"><span data-stu-id="76a0b-112">Pixel</span></span> | <span data-ttu-id="76a0b-113">Вычисления</span><span class="sxs-lookup"><span data-stu-id="76a0b-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="76a0b-114">X</span><span class="sxs-lookup"><span data-stu-id="76a0b-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="76a0b-115">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="76a0b-115">Minimum Shader Model</span></span>

<span data-ttu-id="76a0b-116">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="76a0b-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="76a0b-117">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="76a0b-117">Shader Model</span></span>                                              | <span data-ttu-id="76a0b-118">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="76a0b-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="76a0b-119">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="76a0b-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="76a0b-120">да</span><span class="sxs-lookup"><span data-stu-id="76a0b-120">yes</span></span>       |
| [<span data-ttu-id="76a0b-121">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="76a0b-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="76a0b-122">Нет</span><span class="sxs-lookup"><span data-stu-id="76a0b-122">no</span></span>        |
| [<span data-ttu-id="76a0b-123">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="76a0b-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="76a0b-124">Нет</span><span class="sxs-lookup"><span data-stu-id="76a0b-124">no</span></span>        |
| [<span data-ttu-id="76a0b-125">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76a0b-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="76a0b-126">Нет</span><span class="sxs-lookup"><span data-stu-id="76a0b-126">no</span></span>        |
| [<span data-ttu-id="76a0b-127">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76a0b-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="76a0b-128">Нет</span><span class="sxs-lookup"><span data-stu-id="76a0b-128">no</span></span>        |
| [<span data-ttu-id="76a0b-129">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76a0b-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="76a0b-130">Нет</span><span class="sxs-lookup"><span data-stu-id="76a0b-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="76a0b-131">См. также</span><span class="sxs-lookup"><span data-stu-id="76a0b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76a0b-132">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76a0b-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




