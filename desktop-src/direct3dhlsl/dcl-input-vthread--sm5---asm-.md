---
title: dcl_input Всреад (SM5-ASM)
description: Объявите идентификаторы входных данных шейдера вычислений.
ms.assetid: C041863A-32B0-4588-A1A9-E416AF9B723C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf6a7bb19feef95eae9cc153911407b206fde16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103785019"
---
# <a name="dcl_input-vthread-sm5---asm"></a><span data-ttu-id="450ee-103">дкл \_ input всреад (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="450ee-103">dcl\_input vThread (sm5 - asm)</span></span>

<span data-ttu-id="450ee-104">Объявите идентификаторы входных данных шейдера вычислений.</span><span class="sxs-lookup"><span data-stu-id="450ee-104">Declare compute shader input IDs.</span></span>



| <span data-ttu-id="450ee-105">дкл \_ Ввод {vThreadID.XYZ </span><span class="sxs-lookup"><span data-stu-id="450ee-105">dcl\_input {vThreadID.xyz</span></span>\|<span data-ttu-id="450ee-106">vThreadGroupID.xyz </span><span class="sxs-lookup"><span data-stu-id="450ee-106">vThreadGroupID.xyz</span></span>\| <span data-ttu-id="450ee-107">vThreadIDInGroup.xyz </span><span class="sxs-lookup"><span data-stu-id="450ee-107">vThreadIDInGroup.xyz</span></span>\|<span data-ttu-id="450ee-108">Всреадидинграупфлаттенед}</span><span class="sxs-lookup"><span data-stu-id="450ee-108">vThreadIDInGroupFlattened}</span></span> |
|--------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="450ee-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="450ee-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="450ee-110">Описание</span><span class="sxs-lookup"><span data-stu-id="450ee-110">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="450ee-111"><span id="vThreadID___vThreadGroupID___vThreadIDInGroup___vThreadIDInGroupFlattened"></span><span id="vthreadid___vthreadgroupid___vthreadidingroup___vthreadidingroupflattened"></span><span id="VTHREADID___VTHREADGROUPID___VTHREADIDINGROUP___VTHREADIDINGROUPFLATTENED"></span>*Всреадид \| всреадграупид \| всреадидинграуп \| всреадидинграупфлаттенед*</span><span class="sxs-lookup"><span data-stu-id="450ee-111"><span id="vThreadID___vThreadGroupID___vThreadIDInGroup___vThreadIDInGroupFlattened"></span><span id="vthreadid___vthreadgroupid___vthreadidingroup___vthreadidingroupflattened"></span><span id="VTHREADID___VTHREADGROUPID___VTHREADIDINGROUP___VTHREADIDINGROUPFLATTENED"></span>*vThreadID \| vThreadGroupID \| vThreadIDInGroup \| vThreadIDInGroupFlattened*</span></span><br/> | <span data-ttu-id="450ee-112">\[в \] 3-компонентном 32-разрядном целочисленном значении идентификатора.</span><span class="sxs-lookup"><span data-stu-id="450ee-112">\[in\] The 3-component unsigned 32-bit integer ID value.</span></span><br/> |



 

<span data-ttu-id="450ee-113">**\_ входные данные дкл** — это существующее объявление в других стадиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="450ee-113">**dcl\_input** is an existing declaration in other shader stages.</span></span> <span data-ttu-id="450ee-114">Он используется в шейдере вычислений для объявления различных значений 3-разрядного целочисленного идентификатора из трех 32 компонентов, уникальных для шейдера вычислений.</span><span class="sxs-lookup"><span data-stu-id="450ee-114">It is used in the compute shader to declare the various 3-component unsigned 32-bit integer ID values unique to the compute shader.</span></span> <span data-ttu-id="450ee-115">К ним относятся:</span><span class="sxs-lookup"><span data-stu-id="450ee-115">They are:</span></span>

-   <span data-ttu-id="450ee-116">vThreadID.xyz</span><span class="sxs-lookup"><span data-stu-id="450ee-116">vThreadID.xyz</span></span>
-   <span data-ttu-id="450ee-117">vGroupID.xyz</span><span class="sxs-lookup"><span data-stu-id="450ee-117">vGroupID.xyz</span></span>
-   <span data-ttu-id="450ee-118">vThreadIDInGroup.xyz</span><span class="sxs-lookup"><span data-stu-id="450ee-118">vThreadIDInGroup.xyz</span></span>
-   <span data-ttu-id="450ee-119">Всреадидинграупфлаттенед (один компонент)</span><span class="sxs-lookup"><span data-stu-id="450ee-119">vThreadIDInGroupFlattened (single component)</span></span>

<span data-ttu-id="450ee-120">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="450ee-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="450ee-121">Вершина</span><span class="sxs-lookup"><span data-stu-id="450ee-121">Vertex</span></span> | <span data-ttu-id="450ee-122">Поверхности</span><span class="sxs-lookup"><span data-stu-id="450ee-122">Hull</span></span> | <span data-ttu-id="450ee-123">Домен</span><span class="sxs-lookup"><span data-stu-id="450ee-123">Domain</span></span> | <span data-ttu-id="450ee-124">Геометрия</span><span class="sxs-lookup"><span data-stu-id="450ee-124">Geometry</span></span> | <span data-ttu-id="450ee-125">Пиксель</span><span class="sxs-lookup"><span data-stu-id="450ee-125">Pixel</span></span> | <span data-ttu-id="450ee-126">Вычисления</span><span class="sxs-lookup"><span data-stu-id="450ee-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="450ee-127">X</span><span class="sxs-lookup"><span data-stu-id="450ee-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="450ee-128">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="450ee-128">Minimum Shader Model</span></span>

<span data-ttu-id="450ee-129">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="450ee-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="450ee-130">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="450ee-130">Shader Model</span></span>                                              | <span data-ttu-id="450ee-131">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="450ee-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="450ee-132">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="450ee-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="450ee-133">да</span><span class="sxs-lookup"><span data-stu-id="450ee-133">yes</span></span>       |
| [<span data-ttu-id="450ee-134">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="450ee-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="450ee-135">Нет</span><span class="sxs-lookup"><span data-stu-id="450ee-135">no</span></span>        |
| [<span data-ttu-id="450ee-136">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="450ee-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="450ee-137">Нет</span><span class="sxs-lookup"><span data-stu-id="450ee-137">no</span></span>        |
| [<span data-ttu-id="450ee-138">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="450ee-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="450ee-139">Нет</span><span class="sxs-lookup"><span data-stu-id="450ee-139">no</span></span>        |
| [<span data-ttu-id="450ee-140">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="450ee-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="450ee-141">Нет</span><span class="sxs-lookup"><span data-stu-id="450ee-141">no</span></span>        |
| [<span data-ttu-id="450ee-142">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="450ee-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="450ee-143">Нет</span><span class="sxs-lookup"><span data-stu-id="450ee-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="450ee-144">См. также</span><span class="sxs-lookup"><span data-stu-id="450ee-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="450ee-145">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="450ee-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





