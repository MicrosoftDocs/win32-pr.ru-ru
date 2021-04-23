---
title: dcl_tessellator_output_primitive (SM5-ASM)
description: Объявите тип выходных примитивов тесселяции в разделе объявления шейдера поверхности.
ms.assetid: 95F074C5-6012-4160-B78E-440C33C1ECC3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 390f22cdafe3b0d078bf8a502623a1c741e34e34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069380"
---
# <a name="dcl_tessellator_output_primitive-sm5---asm"></a><span data-ttu-id="cc816-103">\_выходной примитив дкл тесселяции \_ \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="cc816-103">dcl\_tessellator\_output\_primitive (sm5 - asm)</span></span>

<span data-ttu-id="cc816-104">Объявите тип выходных примитивов тесселяции в разделе объявления шейдера поверхности.</span><span class="sxs-lookup"><span data-stu-id="cc816-104">Declare the tessellator output primitive type in a hull shader declaration section.</span></span>



| <span data-ttu-id="cc816-105">\_выходной примитив дкл тесселяции \_ \_ { \_ точка вывода </span><span class="sxs-lookup"><span data-stu-id="cc816-105">dcl\_tessellator\_output\_primitive {output\_point </span></span>\| <span data-ttu-id="cc816-106">\_строка вывода </span><span class="sxs-lookup"><span data-stu-id="cc816-106">output\_line </span></span>\| <span data-ttu-id="cc816-107">трианглаутпут по \_ Вт. д. \_</span><span class="sxs-lookup"><span data-stu-id="cc816-107">triangloutput\_e\_cw \</span></span>| <span data-ttu-id="cc816-108">выходной \_ треугольник \_ CCW}</span><span class="sxs-lookup"><span data-stu-id="cc816-108">output\_triangle\_ccw}</span></span> |
|----------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="cc816-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="cc816-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="cc816-110">Описание</span><span class="sxs-lookup"><span data-stu-id="cc816-110">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="cc816-111"><span id="output_point___output_line_____________________________________triangloutput_e_cw___output_triangle_ccw"></span><span id="OUTPUT_POINT___OUTPUT_LINE_____________________________________TRIANGLOUTPUT_E_CW___OUTPUT_TRIANGLE_CCW"></span>*Выходная строка выходного \_ пункта \| \_ \| трианглаутпут \_ e \_ во \| выходной \_ треугольник \_ CCW*</span><span class="sxs-lookup"><span data-stu-id="cc816-111"><span id="output_point___output_line_____________________________________triangloutput_e_cw___output_triangle_ccw"></span><span id="OUTPUT_POINT___OUTPUT_LINE_____________________________________TRIANGLOUTPUT_E_CW___OUTPUT_TRIANGLE_CCW"></span>*output\_point \| output\_line \| triangloutput\_e\_cw \| output\_triangle\_ccw*</span></span><br/> | <span data-ttu-id="cc816-112">\[в \] выходном типе-примитиве.</span><span class="sxs-lookup"><span data-stu-id="cc816-112">\[in\] The output primitive type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cc816-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="cc816-113">Remarks</span></span>

<span data-ttu-id="cc816-114">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="cc816-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="cc816-115">Вершина</span><span class="sxs-lookup"><span data-stu-id="cc816-115">Vertex</span></span> | <span data-ttu-id="cc816-116">Поверхности</span><span class="sxs-lookup"><span data-stu-id="cc816-116">Hull</span></span>                 | <span data-ttu-id="cc816-117">Домен</span><span class="sxs-lookup"><span data-stu-id="cc816-117">Domain</span></span> | <span data-ttu-id="cc816-118">Геометрия</span><span class="sxs-lookup"><span data-stu-id="cc816-118">Geometry</span></span> | <span data-ttu-id="cc816-119">Пиксель</span><span class="sxs-lookup"><span data-stu-id="cc816-119">Pixel</span></span> | <span data-ttu-id="cc816-120">Вычисления</span><span class="sxs-lookup"><span data-stu-id="cc816-120">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="cc816-121">Раздел объявлений</span><span class="sxs-lookup"><span data-stu-id="cc816-121">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cc816-122">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="cc816-122">Minimum Shader Model</span></span>

<span data-ttu-id="cc816-123">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="cc816-123">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="cc816-124">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="cc816-124">Shader Model</span></span>                                              | <span data-ttu-id="cc816-125">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="cc816-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cc816-126">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="cc816-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cc816-127">да</span><span class="sxs-lookup"><span data-stu-id="cc816-127">yes</span></span>       |
| [<span data-ttu-id="cc816-128">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="cc816-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cc816-129">Нет</span><span class="sxs-lookup"><span data-stu-id="cc816-129">no</span></span>        |
| [<span data-ttu-id="cc816-130">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="cc816-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cc816-131">Нет</span><span class="sxs-lookup"><span data-stu-id="cc816-131">no</span></span>        |
| [<span data-ttu-id="cc816-132">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc816-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cc816-133">Нет</span><span class="sxs-lookup"><span data-stu-id="cc816-133">no</span></span>        |
| [<span data-ttu-id="cc816-134">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc816-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cc816-135">Нет</span><span class="sxs-lookup"><span data-stu-id="cc816-135">no</span></span>        |
| [<span data-ttu-id="cc816-136">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc816-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cc816-137">Нет</span><span class="sxs-lookup"><span data-stu-id="cc816-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cc816-138">См. также</span><span class="sxs-lookup"><span data-stu-id="cc816-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc816-139">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc816-139">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





