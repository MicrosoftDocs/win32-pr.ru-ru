---
title: dcl_function_body (SM5-ASM)
description: Объявите тело функции.
ms.assetid: 3A651107-BEA6-4D79-938F-8E0243C874C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f020748ecff270311fbbc89798d82b223b1f34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104133346"
---
# <a name="dcl_function_body-sm5---asm"></a><span data-ttu-id="ce56b-103">\_тело функции дкл \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ce56b-103">dcl\_function\_body (sm5 - asm)</span></span>

<span data-ttu-id="ce56b-104">Объявите тело функции.</span><span class="sxs-lookup"><span data-stu-id="ce56b-104">Declare a function body.</span></span>



| <span data-ttu-id="ce56b-105">\_тело функции дкл \_ FB\#</span><span class="sxs-lookup"><span data-stu-id="ce56b-105">dcl\_function\_body fb\#</span></span> |
|--------------------------|



 



| <span data-ttu-id="ce56b-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="ce56b-106">Item</span></span>                                                          | <span data-ttu-id="ce56b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ce56b-107">Description</span></span>                                                              |
|---------------------------------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="ce56b-108"><span id="fb_"></span><span id="FB_"></span>*FB\#*</span><span class="sxs-lookup"><span data-stu-id="ce56b-108"><span id="fb_"></span><span id="FB_"></span>*fb\#*</span></span><br/> | <span data-ttu-id="ce56b-109">\[в \] метке места, где будет отображаться функция.</span><span class="sxs-lookup"><span data-stu-id="ce56b-109">\[in\] The label of the place where the function will appear.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ce56b-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="ce56b-110">Remarks</span></span>

<span data-ttu-id="ce56b-111">Эта инструкция объявляет уникальный текст функции, код которого будет отображаться позже в программе в метке FB \# .</span><span class="sxs-lookup"><span data-stu-id="ce56b-111">This instruction declares a unique function body whose code will appear later in the program at label fb\#.</span></span>

<span data-ttu-id="ce56b-112">Тела функций используются в объявлениях таблиц функций.</span><span class="sxs-lookup"><span data-stu-id="ce56b-112">Function bodies are used in function table declarations.</span></span> <span data-ttu-id="ce56b-113">Дополнительные сведения см. в [разделе \_ \_ Таблица функций дкл](dcl-function-table---sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="ce56b-113">For more info, see [dcl\_function\_table](dcl-function-table---sm5---asm-.md).</span></span>

<span data-ttu-id="ce56b-114">В шейдере поверхности и шейдере доменов, где существует несколько этапов (этап контрольной точки, фаза ветвления и фаза соединения), все тела функций (метка FB \# ) отображаются после всех этапов, а не группируются по этапам.</span><span class="sxs-lookup"><span data-stu-id="ce56b-114">In the hull shader and domain shader, where there are multiple phases (control point phase, fork phase, and join phase), all function bodies (label fb\#) appear after all the phases, rather than being grouped by phase.</span></span>

<span data-ttu-id="ce56b-115">Не существует ограничения на количество существующих в теле функций.</span><span class="sxs-lookup"><span data-stu-id="ce56b-115">There is no limit to how many function bodies can be present.</span></span>

<span data-ttu-id="ce56b-116">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="ce56b-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ce56b-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="ce56b-117">Vertex</span></span> | <span data-ttu-id="ce56b-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ce56b-118">Hull</span></span> | <span data-ttu-id="ce56b-119">Домен</span><span class="sxs-lookup"><span data-stu-id="ce56b-119">Domain</span></span> | <span data-ttu-id="ce56b-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ce56b-120">Geometry</span></span> | <span data-ttu-id="ce56b-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ce56b-121">Pixel</span></span> | <span data-ttu-id="ce56b-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ce56b-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ce56b-123">X</span><span class="sxs-lookup"><span data-stu-id="ce56b-123">X</span></span>      | <span data-ttu-id="ce56b-124">X</span><span class="sxs-lookup"><span data-stu-id="ce56b-124">X</span></span>    | <span data-ttu-id="ce56b-125">X</span><span class="sxs-lookup"><span data-stu-id="ce56b-125">X</span></span>      | <span data-ttu-id="ce56b-126">X</span><span class="sxs-lookup"><span data-stu-id="ce56b-126">X</span></span>        | <span data-ttu-id="ce56b-127">X</span><span class="sxs-lookup"><span data-stu-id="ce56b-127">X</span></span>     | <span data-ttu-id="ce56b-128">X</span><span class="sxs-lookup"><span data-stu-id="ce56b-128">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ce56b-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ce56b-129">Minimum Shader Model</span></span>

<span data-ttu-id="ce56b-130">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ce56b-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ce56b-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ce56b-131">Shader Model</span></span>                                              | <span data-ttu-id="ce56b-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ce56b-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ce56b-133">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ce56b-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ce56b-134">да</span><span class="sxs-lookup"><span data-stu-id="ce56b-134">yes</span></span>       |
| [<span data-ttu-id="ce56b-135">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="ce56b-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ce56b-136">Нет</span><span class="sxs-lookup"><span data-stu-id="ce56b-136">no</span></span>        |
| [<span data-ttu-id="ce56b-137">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="ce56b-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ce56b-138">Нет</span><span class="sxs-lookup"><span data-stu-id="ce56b-138">no</span></span>        |
| [<span data-ttu-id="ce56b-139">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce56b-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ce56b-140">Нет</span><span class="sxs-lookup"><span data-stu-id="ce56b-140">no</span></span>        |
| [<span data-ttu-id="ce56b-141">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce56b-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ce56b-142">Нет</span><span class="sxs-lookup"><span data-stu-id="ce56b-142">no</span></span>        |
| [<span data-ttu-id="ce56b-143">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce56b-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ce56b-144">Нет</span><span class="sxs-lookup"><span data-stu-id="ce56b-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ce56b-145">См. также</span><span class="sxs-lookup"><span data-stu-id="ce56b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce56b-146">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce56b-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





