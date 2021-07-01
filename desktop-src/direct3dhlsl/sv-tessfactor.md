---
title: SV_TessFactor
description: Определяет величину тесселяции для каждого края исправления.
ms.assetid: 970ff744-da5b-4933-866c-dd38b85fb48d
keywords:
- SV_TessFactor HLSL
topic_type:
- apiref
api_name:
- SV_TessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 308034fe607283ef9f1213cca1cabb4a7229765e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118899"
---
# <a name="sv_tessfactor"></a><span data-ttu-id="7006f-104">ОКП \_ тессфактор</span><span class="sxs-lookup"><span data-stu-id="7006f-104">SV\_TessFactor</span></span>

<span data-ttu-id="7006f-105">Определяет величину тесселяции для каждого края исправления.</span><span class="sxs-lookup"><span data-stu-id="7006f-105">Defines the tessellation amount on each edge of a patch.</span></span>

## <a name="type"></a><span data-ttu-id="7006f-106">Тип</span><span class="sxs-lookup"><span data-stu-id="7006f-106">Type</span></span>



|  <span data-ttu-id="7006f-107">Тип</span><span class="sxs-lookup"><span data-stu-id="7006f-107">Type</span></span>          |  <span data-ttu-id="7006f-108">Топология ввода</span><span class="sxs-lookup"><span data-stu-id="7006f-108">Input topology</span></span>              |
|------------|----------------|
| <span data-ttu-id="7006f-109">float \[ 4\]</span><span class="sxs-lookup"><span data-stu-id="7006f-109">float\[4\]</span></span> | <span data-ttu-id="7006f-110">четыре исправления</span><span class="sxs-lookup"><span data-stu-id="7006f-110">quad patch</span></span>     |
| <span data-ttu-id="7006f-111">float \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="7006f-111">float\[3\]</span></span> | <span data-ttu-id="7006f-112">три исправления</span><span class="sxs-lookup"><span data-stu-id="7006f-112">tri patch</span></span>      |
| <span data-ttu-id="7006f-113">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="7006f-113">float\[2\]</span></span> | <span data-ttu-id="7006f-114">исолине</span><span class="sxs-lookup"><span data-stu-id="7006f-114">isoline</span></span>        |



 

<span data-ttu-id="7006f-115">Факторы тесселяции должны быть объявлены как массив. они не могут быть упакованы в один вектор.</span><span class="sxs-lookup"><span data-stu-id="7006f-115">Tessellation factors must be declared as an array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="7006f-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="7006f-116">Remarks</span></span>

<span data-ttu-id="7006f-117">Значение фактора тесселяции должно быть определено во время функции Constant исправления шейдера поверхности.</span><span class="sxs-lookup"><span data-stu-id="7006f-117">The value for tessellation factor must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="7006f-118">Обязательное выходное значение для шейдера поверхности при использовании исправлений с четырьмя или тремя обновлениями.</span><span class="sxs-lookup"><span data-stu-id="7006f-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="7006f-119">Это значение также является обязательным входным значением для шейдера домена, чтобы соответствовать сигнатурам данных исправлений и констант между этапами тесселяции.</span><span class="sxs-lookup"><span data-stu-id="7006f-119">This value is also a required input value for the domain shader to match the patch-constant data signatures between the tessellation stages.</span></span>

<span data-ttu-id="7006f-120">Для исолине первое значение в SV \_ тессфактор — это фактор тесселяции линии, второе значение — это фактор тесселяции строкового типа данных.</span><span class="sxs-lookup"><span data-stu-id="7006f-120">For an isoline, the first value in SV\_TessFactor is the line-density tessellation factor, the second value is the line-detail tessellation factor.</span></span>

### <a name="tri-patch-tessellation-factors"></a><span data-ttu-id="7006f-121">Три фактора тесселяции исправлений</span><span class="sxs-lookup"><span data-stu-id="7006f-121">Tri Patch Tessellation Factors</span></span>

<span data-ttu-id="7006f-122">Первый компонент предоставляет тесселатион фактор для u = = 0 ребра обновления.</span><span class="sxs-lookup"><span data-stu-id="7006f-122">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="7006f-123">Второй компонент предоставляет тесселатион фактор для v = = 0 границы исправления.</span><span class="sxs-lookup"><span data-stu-id="7006f-123">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="7006f-124">Третий компонент предоставляет тесселатион фактор для w = = 0 ребра исправления.</span><span class="sxs-lookup"><span data-stu-id="7006f-124">The third component provides the tesselation factor for the w==0 edge of the patch.</span></span>

### <a name="quad-patch-tessellation-factors"></a><span data-ttu-id="7006f-125">Факторы тесселяции исправлений Quad</span><span class="sxs-lookup"><span data-stu-id="7006f-125">Quad Patch Tessellation Factors</span></span>

<span data-ttu-id="7006f-126">Первый компонент предоставляет тесселатион фактор для u = = 0 ребра обновления.</span><span class="sxs-lookup"><span data-stu-id="7006f-126">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="7006f-127">Второй компонент предоставляет тесселатион фактор для v = = 0 границы исправления.</span><span class="sxs-lookup"><span data-stu-id="7006f-127">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="7006f-128">Третий компонент предоставляет тесселатион фактор для u = = 1 края исправления.</span><span class="sxs-lookup"><span data-stu-id="7006f-128">The third component provides the tesselation factor for the u==1 edge of the patch.</span></span> <span data-ttu-id="7006f-129">Четвертый компонент предоставляет тесселатион фактор для v = = 1 границы исправления.</span><span class="sxs-lookup"><span data-stu-id="7006f-129">The fourth component provides the tesselation factor for the v==1 edge of the patch.</span></span> <span data-ttu-id="7006f-130">Упорядочивание краев происходит по часовой стрелке, начиная с границы u = = 0, которая является левой стороной исправления, и от v = = 0, которая является верхней частью исправления.</span><span class="sxs-lookup"><span data-stu-id="7006f-130">The ordering of the edges is clockwise, starting from the u==0 edge, which is the left side of the patch, and from the v==0 edge, which is the top of the patch.</span></span>

<span data-ttu-id="7006f-131">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="7006f-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="7006f-132">Вершина</span><span class="sxs-lookup"><span data-stu-id="7006f-132">Vertex</span></span> | <span data-ttu-id="7006f-133">Поверхности</span><span class="sxs-lookup"><span data-stu-id="7006f-133">Hull</span></span> | <span data-ttu-id="7006f-134">Домен</span><span class="sxs-lookup"><span data-stu-id="7006f-134">Domain</span></span> | <span data-ttu-id="7006f-135">Geometry</span><span class="sxs-lookup"><span data-stu-id="7006f-135">Geometry</span></span> | <span data-ttu-id="7006f-136">Пиксель</span><span class="sxs-lookup"><span data-stu-id="7006f-136">Pixel</span></span> | <span data-ttu-id="7006f-137">Службы вычислений</span><span class="sxs-lookup"><span data-stu-id="7006f-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="7006f-138">x</span><span class="sxs-lookup"><span data-stu-id="7006f-138">x</span></span>    | <span data-ttu-id="7006f-139">x</span><span class="sxs-lookup"><span data-stu-id="7006f-139">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="7006f-140">См. также</span><span class="sxs-lookup"><span data-stu-id="7006f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7006f-141">Семантика</span><span class="sxs-lookup"><span data-stu-id="7006f-141">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="7006f-142">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="7006f-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




