---
title: hs_control_point_phase (SM5-ASM)
description: Запустите этап контрольной точки в шейдере поверхности.
ms.assetid: 9CF26691-C04F-4728-8418-40F313ABBE4A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aba3f591fcd656e64609513dca7b9126496a86d6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069368"
---
# <a name="hs_control_point_phase-sm5---asm"></a><span data-ttu-id="60e2f-103">\_этап контрольной \_ точки HS \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="60e2f-103">hs\_control\_point\_phase (sm5 - asm)</span></span>

<span data-ttu-id="60e2f-104">Запустите этап контрольной точки в шейдере поверхности.</span><span class="sxs-lookup"><span data-stu-id="60e2f-104">Start the control point phase in a hull shader.</span></span>



| <span data-ttu-id="60e2f-105">\_фаза контрольной \_ точки HS \_</span><span class="sxs-lookup"><span data-stu-id="60e2f-105">hs\_control\_point\_phase</span></span> |
|---------------------------|



 

## <a name="remarks"></a><span data-ttu-id="60e2f-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="60e2f-106">Remarks</span></span>

<span data-ttu-id="60e2f-107">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="60e2f-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="60e2f-108">Вершина</span><span class="sxs-lookup"><span data-stu-id="60e2f-108">Vertex</span></span> | <span data-ttu-id="60e2f-109">Поверхности</span><span class="sxs-lookup"><span data-stu-id="60e2f-109">Hull</span></span> | <span data-ttu-id="60e2f-110">Домен</span><span class="sxs-lookup"><span data-stu-id="60e2f-110">Domain</span></span> | <span data-ttu-id="60e2f-111">Геометрия</span><span class="sxs-lookup"><span data-stu-id="60e2f-111">Geometry</span></span> | <span data-ttu-id="60e2f-112">Пиксель</span><span class="sxs-lookup"><span data-stu-id="60e2f-112">Pixel</span></span> | <span data-ttu-id="60e2f-113">Вычисления</span><span class="sxs-lookup"><span data-stu-id="60e2f-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="60e2f-114">X</span><span class="sxs-lookup"><span data-stu-id="60e2f-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="60e2f-115">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="60e2f-115">Minimum Shader Model</span></span>

<span data-ttu-id="60e2f-116">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="60e2f-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="60e2f-117">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="60e2f-117">Shader Model</span></span>                                              | <span data-ttu-id="60e2f-118">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="60e2f-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="60e2f-119">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="60e2f-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="60e2f-120">да</span><span class="sxs-lookup"><span data-stu-id="60e2f-120">yes</span></span>       |
| [<span data-ttu-id="60e2f-121">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="60e2f-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="60e2f-122">Нет</span><span class="sxs-lookup"><span data-stu-id="60e2f-122">no</span></span>        |
| [<span data-ttu-id="60e2f-123">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="60e2f-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="60e2f-124">Нет</span><span class="sxs-lookup"><span data-stu-id="60e2f-124">no</span></span>        |
| [<span data-ttu-id="60e2f-125">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="60e2f-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="60e2f-126">Нет</span><span class="sxs-lookup"><span data-stu-id="60e2f-126">no</span></span>        |
| [<span data-ttu-id="60e2f-127">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="60e2f-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="60e2f-128">Нет</span><span class="sxs-lookup"><span data-stu-id="60e2f-128">no</span></span>        |
| [<span data-ttu-id="60e2f-129">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="60e2f-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="60e2f-130">Нет</span><span class="sxs-lookup"><span data-stu-id="60e2f-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="60e2f-131">См. также</span><span class="sxs-lookup"><span data-stu-id="60e2f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60e2f-132">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="60e2f-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




