---
title: dcl_input Вфоркинстанцеид (SM5-ASM)
description: Объявите идентификатор экземпляра на фазе ветвления шейдера поверхности.
ms.assetid: AA73E8B6-C6D7-4483-B46E-C733341F552C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ce5fcf111a59abb0c9a6ccb36de63d94dcb11e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069387"
---
# <a name="dcl_input-vforkinstanceid-sm5---asm"></a><span data-ttu-id="1f1c1-103">дкл \_ input вфоркинстанцеид (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="1f1c1-103">dcl\_input vForkInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="1f1c1-104">Объявите идентификатор экземпляра на фазе ветвления шейдера поверхности.</span><span class="sxs-lookup"><span data-stu-id="1f1c1-104">Declare the instance ID in a hull shader fork phase.</span></span>



| <span data-ttu-id="1f1c1-105">дкл \_ входные вфоркинстанцеид</span><span class="sxs-lookup"><span data-stu-id="1f1c1-105">dcl\_input vForkInstanceID</span></span> |
|----------------------------|



 



| <span data-ttu-id="1f1c1-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="1f1c1-106">Item</span></span>                                                                                                                               | <span data-ttu-id="1f1c1-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1f1c1-107">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="1f1c1-108"><span id="vForkInstanceID"></span><span id="vforkinstanceid"></span><span id="VFORKINSTANCEID"></span>*вфоркинстанцеид*</span><span class="sxs-lookup"><span data-stu-id="1f1c1-108"><span id="vForkInstanceID"></span><span id="vforkinstanceid"></span><span id="VFORKINSTANCEID"></span>*vForkInstanceID*</span></span><br/> | <span data-ttu-id="1f1c1-109">\[в \] идентификаторе экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1f1c1-109">\[in\] The instance ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1f1c1-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="1f1c1-110">Remarks</span></span>

<span data-ttu-id="1f1c1-111">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="1f1c1-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1f1c1-112">Вершина</span><span class="sxs-lookup"><span data-stu-id="1f1c1-112">Vertex</span></span> | <span data-ttu-id="1f1c1-113">Поверхности</span><span class="sxs-lookup"><span data-stu-id="1f1c1-113">Hull</span></span> | <span data-ttu-id="1f1c1-114">Домен</span><span class="sxs-lookup"><span data-stu-id="1f1c1-114">Domain</span></span> | <span data-ttu-id="1f1c1-115">Геометрия</span><span class="sxs-lookup"><span data-stu-id="1f1c1-115">Geometry</span></span> | <span data-ttu-id="1f1c1-116">Пиксель</span><span class="sxs-lookup"><span data-stu-id="1f1c1-116">Pixel</span></span> | <span data-ttu-id="1f1c1-117">Вычисления</span><span class="sxs-lookup"><span data-stu-id="1f1c1-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="1f1c1-118">X</span><span class="sxs-lookup"><span data-stu-id="1f1c1-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1f1c1-119">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1f1c1-119">Minimum Shader Model</span></span>

<span data-ttu-id="1f1c1-120">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="1f1c1-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1f1c1-121">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1f1c1-121">Shader Model</span></span>                                              | <span data-ttu-id="1f1c1-122">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="1f1c1-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1f1c1-123">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="1f1c1-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1f1c1-124">да</span><span class="sxs-lookup"><span data-stu-id="1f1c1-124">yes</span></span>       |
| [<span data-ttu-id="1f1c1-125">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="1f1c1-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1f1c1-126">Нет</span><span class="sxs-lookup"><span data-stu-id="1f1c1-126">no</span></span>        |
| [<span data-ttu-id="1f1c1-127">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="1f1c1-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1f1c1-128">Нет</span><span class="sxs-lookup"><span data-stu-id="1f1c1-128">no</span></span>        |
| [<span data-ttu-id="1f1c1-129">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f1c1-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1f1c1-130">Нет</span><span class="sxs-lookup"><span data-stu-id="1f1c1-130">no</span></span>        |
| [<span data-ttu-id="1f1c1-131">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f1c1-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1f1c1-132">Нет</span><span class="sxs-lookup"><span data-stu-id="1f1c1-132">no</span></span>        |
| [<span data-ttu-id="1f1c1-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f1c1-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1f1c1-134">Нет</span><span class="sxs-lookup"><span data-stu-id="1f1c1-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1f1c1-135">См. также</span><span class="sxs-lookup"><span data-stu-id="1f1c1-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f1c1-136">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f1c1-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





