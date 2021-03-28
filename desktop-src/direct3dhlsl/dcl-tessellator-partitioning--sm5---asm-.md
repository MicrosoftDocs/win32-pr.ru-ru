---
title: dcl_tessellator_partitioning (SM5-ASM)
description: Объявите секционирование тесселяции в разделе объявления шейдера поверхности.
ms.assetid: 6EA00C6B-A0DE-4CE4-8B52-1337CA92CA5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6f6091301f95dd2364debec2bf54c0966c0e64
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412231"
---
# <a name="dcl_tessellator_partitioning-sm5---asm"></a><span data-ttu-id="1e04e-103">\_секционирование тесселяции дкл \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="1e04e-103">dcl\_tessellator\_partitioning (sm5 - asm)</span></span>

<span data-ttu-id="1e04e-104">Объявите секционирование тесселяции в разделе объявления шейдера поверхности.</span><span class="sxs-lookup"><span data-stu-id="1e04e-104">Declare the tessellator partitioning in a hull shader declaration section.</span></span>



| <span data-ttu-id="1e04e-105">\_секционирование тесселяции дкл \_ { \_ целое число секционирования </span><span class="sxs-lookup"><span data-stu-id="1e04e-105">dcl\_tessellator\_partitioning {partitioning\_integer</span></span>\| <span data-ttu-id="1e04e-106">секционирование \_ pow2 </span><span class="sxs-lookup"><span data-stu-id="1e04e-106">partitioning\_pow2</span></span>\|<span data-ttu-id="1e04e-107">нечетные секционирование в \_ долях секунды \_</span><span class="sxs-lookup"><span data-stu-id="1e04e-107">partitioning\_fractional\_odd\</span></span>| <span data-ttu-id="1e04e-108">секционирование \_ дробной части \_ даже}</span><span class="sxs-lookup"><span data-stu-id="1e04e-108">partitioning\_fractional\_even}</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="1e04e-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="1e04e-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="1e04e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1e04e-110">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="1e04e-111"><span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*секционирование \_ целых чисел \| \_ pow2 \| секционирование с \_ \_ четной дробной \| секцией с \_ \_ четностью*</span><span class="sxs-lookup"><span data-stu-id="1e04e-111"><span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*partitioning\_integer\| partitioning\_pow2\|partitioning\_fractional\_odd\| partitioning\_fractional\_even*</span></span><br/> | <span data-ttu-id="1e04e-112">\[в \] секционировании тесселяции.</span><span class="sxs-lookup"><span data-stu-id="1e04e-112">\[in\] The tessellator partitioning.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1e04e-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="1e04e-113">Remarks</span></span>

<span data-ttu-id="1e04e-114">С точки зрения оборудования \_ pow2 ведет себя так же, как и \_ целое число.</span><span class="sxs-lookup"><span data-stu-id="1e04e-114">From the hardware point of view, \_pow2 behaves just like \_integer.</span></span> <span data-ttu-id="1e04e-115">Это HLSL шейдера и (или) компилеркоде для округления Тессфакторс к степени 2.</span><span class="sxs-lookup"><span data-stu-id="1e04e-115">It is up to the HLSL shader author and/or compilercode to round TessFactors to powers of 2.</span></span>

<span data-ttu-id="1e04e-116">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="1e04e-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1e04e-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="1e04e-117">Vertex</span></span> | <span data-ttu-id="1e04e-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="1e04e-118">Hull</span></span>                 | <span data-ttu-id="1e04e-119">Домен</span><span class="sxs-lookup"><span data-stu-id="1e04e-119">Domain</span></span> | <span data-ttu-id="1e04e-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="1e04e-120">Geometry</span></span> | <span data-ttu-id="1e04e-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="1e04e-121">Pixel</span></span> | <span data-ttu-id="1e04e-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="1e04e-122">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="1e04e-123">Раздел объявлений</span><span class="sxs-lookup"><span data-stu-id="1e04e-123">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1e04e-124">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1e04e-124">Minimum Shader Model</span></span>

<span data-ttu-id="1e04e-125">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="1e04e-125">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1e04e-126">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1e04e-126">Shader Model</span></span>                                              | <span data-ttu-id="1e04e-127">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="1e04e-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1e04e-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="1e04e-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1e04e-129">да</span><span class="sxs-lookup"><span data-stu-id="1e04e-129">yes</span></span>       |
| [<span data-ttu-id="1e04e-130">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="1e04e-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1e04e-131">Нет</span><span class="sxs-lookup"><span data-stu-id="1e04e-131">no</span></span>        |
| [<span data-ttu-id="1e04e-132">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="1e04e-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1e04e-133">Нет</span><span class="sxs-lookup"><span data-stu-id="1e04e-133">no</span></span>        |
| [<span data-ttu-id="1e04e-134">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1e04e-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1e04e-135">Нет</span><span class="sxs-lookup"><span data-stu-id="1e04e-135">no</span></span>        |
| [<span data-ttu-id="1e04e-136">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1e04e-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1e04e-137">Нет</span><span class="sxs-lookup"><span data-stu-id="1e04e-137">no</span></span>        |
| [<span data-ttu-id="1e04e-138">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1e04e-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1e04e-139">Нет</span><span class="sxs-lookup"><span data-stu-id="1e04e-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1e04e-140">См. также</span><span class="sxs-lookup"><span data-stu-id="1e04e-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e04e-141">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1e04e-141">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





