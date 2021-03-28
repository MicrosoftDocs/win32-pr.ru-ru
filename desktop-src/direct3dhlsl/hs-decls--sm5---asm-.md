---
title: hs_decls (SM5-ASM)
description: Начните этап объявлений в шейдере поверхности.
ms.assetid: 1C8552B1-F649-4B73-A365-D449A9121DAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e57207e35aab507a1404efaf90131a9648918ae7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104133334"
---
# <a name="hs_decls-sm5---asm"></a><span data-ttu-id="d6987-103">HS \_ деклс (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="d6987-103">hs\_decls (sm5 - asm)</span></span>

<span data-ttu-id="d6987-104">Начните этап объявлений в шейдере поверхности.</span><span class="sxs-lookup"><span data-stu-id="d6987-104">Start the declarations phase in a hull shader.</span></span>



| <span data-ttu-id="d6987-105">\_деклс HS</span><span class="sxs-lookup"><span data-stu-id="d6987-105">hs\_decls</span></span> |
|-----------|



 

## <a name="remarks"></a><span data-ttu-id="d6987-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="d6987-106">Remarks</span></span>

<span data-ttu-id="d6987-107">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="d6987-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d6987-108">Вершина</span><span class="sxs-lookup"><span data-stu-id="d6987-108">Vertex</span></span> | <span data-ttu-id="d6987-109">Поверхности</span><span class="sxs-lookup"><span data-stu-id="d6987-109">Hull</span></span> | <span data-ttu-id="d6987-110">Домен</span><span class="sxs-lookup"><span data-stu-id="d6987-110">Domain</span></span> | <span data-ttu-id="d6987-111">Геометрия</span><span class="sxs-lookup"><span data-stu-id="d6987-111">Geometry</span></span> | <span data-ttu-id="d6987-112">Пиксель</span><span class="sxs-lookup"><span data-stu-id="d6987-112">Pixel</span></span> | <span data-ttu-id="d6987-113">Вычисления</span><span class="sxs-lookup"><span data-stu-id="d6987-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="d6987-114">X</span><span class="sxs-lookup"><span data-stu-id="d6987-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d6987-115">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d6987-115">Minimum Shader Model</span></span>

<span data-ttu-id="d6987-116">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="d6987-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d6987-117">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d6987-117">Shader Model</span></span>                                              | <span data-ttu-id="d6987-118">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="d6987-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d6987-119">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="d6987-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d6987-120">да</span><span class="sxs-lookup"><span data-stu-id="d6987-120">yes</span></span>       |
| [<span data-ttu-id="d6987-121">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="d6987-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d6987-122">Нет</span><span class="sxs-lookup"><span data-stu-id="d6987-122">no</span></span>        |
| [<span data-ttu-id="d6987-123">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="d6987-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d6987-124">Нет</span><span class="sxs-lookup"><span data-stu-id="d6987-124">no</span></span>        |
| [<span data-ttu-id="d6987-125">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6987-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d6987-126">Нет</span><span class="sxs-lookup"><span data-stu-id="d6987-126">no</span></span>        |
| [<span data-ttu-id="d6987-127">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6987-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d6987-128">Нет</span><span class="sxs-lookup"><span data-stu-id="d6987-128">no</span></span>        |
| [<span data-ttu-id="d6987-129">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6987-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d6987-130">Нет</span><span class="sxs-lookup"><span data-stu-id="d6987-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d6987-131">См. также</span><span class="sxs-lookup"><span data-stu-id="d6987-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6987-132">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6987-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




