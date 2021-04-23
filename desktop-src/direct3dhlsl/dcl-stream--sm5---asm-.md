---
title: dcl_stream (SM5-ASM)
description: Объявите выходной поток шейдера Geometry.
ms.assetid: 0A8B8AB5-B7B0-46BB-91E8-B2E8E3D64B74
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f46903c3257c280788e91c25700743a23c146fe
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412234"
---
# <a name="dcl_stream-sm5---asm"></a><span data-ttu-id="3fae5-103">\_поток дкл (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="3fae5-103">dcl\_stream (sm5 - asm)</span></span>

<span data-ttu-id="3fae5-104">Объявите выходной поток шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="3fae5-104">Declare a geometry shader output stream.</span></span>



| <span data-ttu-id="3fae5-105">\_поток дкл m\#</span><span class="sxs-lookup"><span data-stu-id="3fae5-105">dcl\_stream m\#</span></span> |
|-----------------|



 



| <span data-ttu-id="3fae5-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="3fae5-106">Item</span></span>                                                       | <span data-ttu-id="3fae5-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3fae5-107">Description</span></span>                             |
|------------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="3fae5-108"><span id="m_"></span><span id="M_"></span>*Пн\#*</span><span class="sxs-lookup"><span data-stu-id="3fae5-108"><span id="m_"></span><span id="M_"></span>*m\#*</span></span><br/> | <span data-ttu-id="3fae5-109">\[в \] потоке 0.. 3 (M0.. M3).</span><span class="sxs-lookup"><span data-stu-id="3fae5-109">\[in\] Stream 0..3 (m0..m3).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3fae5-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="3fae5-110">Remarks</span></span>

<span data-ttu-id="3fae5-111">Данный поток может быть объявлен только один раз.</span><span class="sxs-lookup"><span data-stu-id="3fae5-111">A given stream can only be declared once.</span></span>

<span data-ttu-id="3fae5-112">Если ни один поток не объявлен, объявления топологии OUTPUT и Output считаются для потока 0.</span><span class="sxs-lookup"><span data-stu-id="3fae5-112">If no streams are declared, output and output topology declarations are assumed to be for stream 0.</span></span>

<span data-ttu-id="3fae5-113">Первый **\_ поток дкл** не может располагаться после любых инструкций **\_ Output дкл** или **дкл \_ аутпуттопологи** .</span><span class="sxs-lookup"><span data-stu-id="3fae5-113">The first **dcl\_stream** cannot appear after any **dcl\_output** or **dcl\_outputTopology** statements.</span></span>

<span data-ttu-id="3fae5-114">Любые **дкл \_ Output** или **дкл \_ аутпуттоплоги** инструкции после любой инструкции **дкл \_ Stream** m \# определяют выходные данные для Stream m \# .</span><span class="sxs-lookup"><span data-stu-id="3fae5-114">Any **dcl\_output** or **dcl\_outputToplogy** statements after any **dcl\_stream** m\# statement define the outputs for stream m\#.</span></span>

<span data-ttu-id="3fae5-115">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="3fae5-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3fae5-116">Вершина</span><span class="sxs-lookup"><span data-stu-id="3fae5-116">Vertex</span></span> | <span data-ttu-id="3fae5-117">Поверхности</span><span class="sxs-lookup"><span data-stu-id="3fae5-117">Hull</span></span> | <span data-ttu-id="3fae5-118">Домен</span><span class="sxs-lookup"><span data-stu-id="3fae5-118">Domain</span></span> | <span data-ttu-id="3fae5-119">Геометрия</span><span class="sxs-lookup"><span data-stu-id="3fae5-119">Geometry</span></span> | <span data-ttu-id="3fae5-120">Пиксель</span><span class="sxs-lookup"><span data-stu-id="3fae5-120">Pixel</span></span> | <span data-ttu-id="3fae5-121">Вычисления</span><span class="sxs-lookup"><span data-stu-id="3fae5-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="3fae5-122">X</span><span class="sxs-lookup"><span data-stu-id="3fae5-122">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3fae5-123">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="3fae5-123">Minimum Shader Model</span></span>

<span data-ttu-id="3fae5-124">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="3fae5-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="3fae5-125">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="3fae5-125">Shader Model</span></span>                                              | <span data-ttu-id="3fae5-126">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="3fae5-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3fae5-127">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="3fae5-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3fae5-128">да</span><span class="sxs-lookup"><span data-stu-id="3fae5-128">yes</span></span>       |
| [<span data-ttu-id="3fae5-129">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="3fae5-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3fae5-130">Нет</span><span class="sxs-lookup"><span data-stu-id="3fae5-130">no</span></span>        |
| [<span data-ttu-id="3fae5-131">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="3fae5-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3fae5-132">Нет</span><span class="sxs-lookup"><span data-stu-id="3fae5-132">no</span></span>        |
| [<span data-ttu-id="3fae5-133">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3fae5-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3fae5-134">Нет</span><span class="sxs-lookup"><span data-stu-id="3fae5-134">no</span></span>        |
| [<span data-ttu-id="3fae5-135">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3fae5-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3fae5-136">Нет</span><span class="sxs-lookup"><span data-stu-id="3fae5-136">no</span></span>        |
| [<span data-ttu-id="3fae5-137">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3fae5-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3fae5-138">Нет</span><span class="sxs-lookup"><span data-stu-id="3fae5-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3fae5-139">См. также</span><span class="sxs-lookup"><span data-stu-id="3fae5-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fae5-140">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3fae5-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





