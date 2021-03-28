---
title: hs_join_phase (SM5-ASM)
description: Запустите фазу соединения в шейдере поверхности.
ms.assetid: C53889BE-B65F-4F5F-8B87-7C5263FAC800
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54c45011209124d73fe866872772a3a787c538d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335576"
---
# <a name="hs_join_phase-sm5---asm"></a><span data-ttu-id="c6325-103">\_фаза присоединения к HS \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="c6325-103">hs\_join\_phase (sm5 - asm)</span></span>

<span data-ttu-id="c6325-104">Запустите фазу соединения в шейдере поверхности.</span><span class="sxs-lookup"><span data-stu-id="c6325-104">Start the join phase in a hull shader.</span></span>



| <span data-ttu-id="c6325-105">\_фаза присоединения к HS \_</span><span class="sxs-lookup"><span data-stu-id="c6325-105">hs\_join\_phase</span></span> |
|-----------------|



 

## <a name="remarks"></a><span data-ttu-id="c6325-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="c6325-106">Remarks</span></span>

<span data-ttu-id="c6325-107">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="c6325-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c6325-108">Вершина</span><span class="sxs-lookup"><span data-stu-id="c6325-108">Vertex</span></span> | <span data-ttu-id="c6325-109">Поверхности</span><span class="sxs-lookup"><span data-stu-id="c6325-109">Hull</span></span> | <span data-ttu-id="c6325-110">Домен</span><span class="sxs-lookup"><span data-stu-id="c6325-110">Domain</span></span> | <span data-ttu-id="c6325-111">Геометрия</span><span class="sxs-lookup"><span data-stu-id="c6325-111">Geometry</span></span> | <span data-ttu-id="c6325-112">Пиксель</span><span class="sxs-lookup"><span data-stu-id="c6325-112">Pixel</span></span> | <span data-ttu-id="c6325-113">Вычисления</span><span class="sxs-lookup"><span data-stu-id="c6325-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="c6325-114">X</span><span class="sxs-lookup"><span data-stu-id="c6325-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c6325-115">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c6325-115">Minimum Shader Model</span></span>

<span data-ttu-id="c6325-116">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="c6325-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c6325-117">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c6325-117">Shader Model</span></span>                                              | <span data-ttu-id="c6325-118">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="c6325-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c6325-119">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="c6325-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c6325-120">да</span><span class="sxs-lookup"><span data-stu-id="c6325-120">yes</span></span>       |
| [<span data-ttu-id="c6325-121">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="c6325-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c6325-122">Нет</span><span class="sxs-lookup"><span data-stu-id="c6325-122">no</span></span>        |
| [<span data-ttu-id="c6325-123">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="c6325-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c6325-124">Нет</span><span class="sxs-lookup"><span data-stu-id="c6325-124">no</span></span>        |
| [<span data-ttu-id="c6325-125">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6325-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c6325-126">Нет</span><span class="sxs-lookup"><span data-stu-id="c6325-126">no</span></span>        |
| [<span data-ttu-id="c6325-127">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6325-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c6325-128">Нет</span><span class="sxs-lookup"><span data-stu-id="c6325-128">no</span></span>        |
| [<span data-ttu-id="c6325-129">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6325-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c6325-130">Нет</span><span class="sxs-lookup"><span data-stu-id="c6325-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c6325-131">См. также</span><span class="sxs-lookup"><span data-stu-id="c6325-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6325-132">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6325-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




