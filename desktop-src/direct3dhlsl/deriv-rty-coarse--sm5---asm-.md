---
title: deriv_rty_coarse (SM5-ASM)
description: Вычисление частоты изменения компонентов. | deriv_rty_coarse (SM5-ASM)
ms.assetid: 1EBCC0B9-BD3E-46DD-AC17-F7167F892195
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df7fd539adf8587118a6bdfdcb5959925e6a97f8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998170"
---
# <a name="deriv_rty_coarse-sm5---asm"></a><span data-ttu-id="1be53-104">производный \_ РТИ \_ грубый (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="1be53-104">deriv\_rty\_coarse (sm5 - asm)</span></span>

<span data-ttu-id="1be53-105">Вычисление частоты изменения компонентов.</span><span class="sxs-lookup"><span data-stu-id="1be53-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="1be53-106">наследование \_ РТИ \_ грубой \[ \_ \] \[ перекрытия \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] ,</span><span class="sxs-lookup"><span data-stu-id="1be53-106">deriv\_rty\_coarse\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------|



 



| <span data-ttu-id="1be53-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="1be53-107">Item</span></span>                                                            | <span data-ttu-id="1be53-108">Описание</span><span class="sxs-lookup"><span data-stu-id="1be53-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="1be53-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="1be53-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1be53-110">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="1be53-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="1be53-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1be53-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1be53-112">\[в \] компонентах операции.</span><span class="sxs-lookup"><span data-stu-id="1be53-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="1be53-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="1be53-113">Remarks</span></span>

<span data-ttu-id="1be53-114">Дополнительные сведения см. в разделе [наследование \_ RTX \_ грубой.](deriv-rtx-coarse--sm5---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="1be53-114">For more information, see [deriv\_rtx\_coarse.](deriv-rtx-coarse--sm5---asm-.md)</span></span>

<span data-ttu-id="1be53-115">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="1be53-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1be53-116">Вершина</span><span class="sxs-lookup"><span data-stu-id="1be53-116">Vertex</span></span> | <span data-ttu-id="1be53-117">Поверхности</span><span class="sxs-lookup"><span data-stu-id="1be53-117">Hull</span></span> | <span data-ttu-id="1be53-118">Домен</span><span class="sxs-lookup"><span data-stu-id="1be53-118">Domain</span></span> | <span data-ttu-id="1be53-119">Геометрия</span><span class="sxs-lookup"><span data-stu-id="1be53-119">Geometry</span></span> | <span data-ttu-id="1be53-120">Пиксель</span><span class="sxs-lookup"><span data-stu-id="1be53-120">Pixel</span></span> | <span data-ttu-id="1be53-121">Вычисления</span><span class="sxs-lookup"><span data-stu-id="1be53-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1be53-122">X</span><span class="sxs-lookup"><span data-stu-id="1be53-122">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1be53-123">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1be53-123">Minimum Shader Model</span></span>

<span data-ttu-id="1be53-124">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="1be53-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1be53-125">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1be53-125">Shader Model</span></span>                                              | <span data-ttu-id="1be53-126">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="1be53-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1be53-127">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="1be53-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1be53-128">да</span><span class="sxs-lookup"><span data-stu-id="1be53-128">yes</span></span>       |
| [<span data-ttu-id="1be53-129">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="1be53-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1be53-130">Нет</span><span class="sxs-lookup"><span data-stu-id="1be53-130">no</span></span>        |
| [<span data-ttu-id="1be53-131">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="1be53-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1be53-132">Нет</span><span class="sxs-lookup"><span data-stu-id="1be53-132">no</span></span>        |
| [<span data-ttu-id="1be53-133">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1be53-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1be53-134">Нет</span><span class="sxs-lookup"><span data-stu-id="1be53-134">no</span></span>        |
| [<span data-ttu-id="1be53-135">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1be53-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1be53-136">Нет</span><span class="sxs-lookup"><span data-stu-id="1be53-136">no</span></span>        |
| [<span data-ttu-id="1be53-137">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1be53-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1be53-138">Нет</span><span class="sxs-lookup"><span data-stu-id="1be53-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1be53-139">См. также</span><span class="sxs-lookup"><span data-stu-id="1be53-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1be53-140">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1be53-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





