---
title: dcl_input Ваутпутконтролпоинтид (SM5-ASM)
description: Объявите идентификатор контрольной точки вывода на этапе контрольной точки шейдера поверхности.
ms.assetid: 376ECA4F-DD71-4466-8A9D-E92A536832BC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cee49a8a825f25b0fbbccff027d5ad1b9ade514
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069386"
---
# <a name="dcl_input-voutputcontrolpointid-sm5---asm"></a><span data-ttu-id="28b37-103">дкл \_ input ваутпутконтролпоинтид (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="28b37-103">dcl\_input vOutputControlPointID (sm5 - asm)</span></span>

<span data-ttu-id="28b37-104">Объявите идентификатор контрольной точки вывода на этапе контрольной точки шейдера поверхности.</span><span class="sxs-lookup"><span data-stu-id="28b37-104">Declare the output control point ID in a hull shader control point phase.</span></span>



| <span data-ttu-id="28b37-105">дкл \_ входные ваутпутконтролпоинтид</span><span class="sxs-lookup"><span data-stu-id="28b37-105">dcl\_input vOutputControlPointID</span></span> |
|----------------------------------|



 



| <span data-ttu-id="28b37-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="28b37-106">Item</span></span>                                                                                                                                                       | <span data-ttu-id="28b37-107">Описание</span><span class="sxs-lookup"><span data-stu-id="28b37-107">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="28b37-108"><span id="vOutputControlPointID"></span><span id="voutputcontrolpointid"></span><span id="VOUTPUTCONTROLPOINTID"></span>*ваутпутконтролпоинтид*</span><span class="sxs-lookup"><span data-stu-id="28b37-108"><span id="vOutputControlPointID"></span><span id="voutputcontrolpointid"></span><span id="VOUTPUTCONTROLPOINTID"></span>*vOutputControlPointID*</span></span><br/> | <span data-ttu-id="28b37-109">\[в \] поле идентификатор точки управления выходом.</span><span class="sxs-lookup"><span data-stu-id="28b37-109">\[in\] The output control point ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="28b37-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="28b37-110">Remarks</span></span>

<span data-ttu-id="28b37-111">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="28b37-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="28b37-112">Вершина</span><span class="sxs-lookup"><span data-stu-id="28b37-112">Vertex</span></span> | <span data-ttu-id="28b37-113">Поверхности</span><span class="sxs-lookup"><span data-stu-id="28b37-113">Hull</span></span> | <span data-ttu-id="28b37-114">Домен</span><span class="sxs-lookup"><span data-stu-id="28b37-114">Domain</span></span> | <span data-ttu-id="28b37-115">Геометрия</span><span class="sxs-lookup"><span data-stu-id="28b37-115">Geometry</span></span> | <span data-ttu-id="28b37-116">Пиксель</span><span class="sxs-lookup"><span data-stu-id="28b37-116">Pixel</span></span> | <span data-ttu-id="28b37-117">Вычисления</span><span class="sxs-lookup"><span data-stu-id="28b37-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="28b37-118">X</span><span class="sxs-lookup"><span data-stu-id="28b37-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="28b37-119">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="28b37-119">Minimum Shader Model</span></span>

<span data-ttu-id="28b37-120">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="28b37-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="28b37-121">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="28b37-121">Shader Model</span></span>                                              | <span data-ttu-id="28b37-122">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="28b37-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="28b37-123">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="28b37-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="28b37-124">да</span><span class="sxs-lookup"><span data-stu-id="28b37-124">yes</span></span>       |
| [<span data-ttu-id="28b37-125">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="28b37-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="28b37-126">Нет</span><span class="sxs-lookup"><span data-stu-id="28b37-126">no</span></span>        |
| [<span data-ttu-id="28b37-127">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="28b37-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="28b37-128">Нет</span><span class="sxs-lookup"><span data-stu-id="28b37-128">no</span></span>        |
| [<span data-ttu-id="28b37-129">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="28b37-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="28b37-130">Нет</span><span class="sxs-lookup"><span data-stu-id="28b37-130">no</span></span>        |
| [<span data-ttu-id="28b37-131">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="28b37-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="28b37-132">Нет</span><span class="sxs-lookup"><span data-stu-id="28b37-132">no</span></span>        |
| [<span data-ttu-id="28b37-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="28b37-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="28b37-134">Нет</span><span class="sxs-lookup"><span data-stu-id="28b37-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="28b37-135">См. также</span><span class="sxs-lookup"><span data-stu-id="28b37-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28b37-136">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="28b37-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





