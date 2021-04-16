---
title: Функция Глубегинтрим (GLU. h)
description: Функции Глубегинтрим и Глуендтрим разделяют определение цикла неравномерного рационального B-сплайна (НУРБС). | Функция Глубегинтрим (GLU. h)
ms.assetid: 636402d0-8f6d-4ad8-84c6-66364025d788
keywords:
- Функция Глубегинтрим OpenGL
topic_type:
- apiref
api_name:
- gluBeginTrim
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84cbe5c1cd0cc68ee892d42fc60db05b6ae2bea6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664871"
---
# <a name="glubegintrim-function"></a><span data-ttu-id="102c5-105">Функция Глубегинтрим</span><span class="sxs-lookup"><span data-stu-id="102c5-105">gluBeginTrim function</span></span>

<span data-ttu-id="102c5-106">Функции **глубегинтрим** и [**глуендтрим**](gluendtrim.md) разделяют определение цикла неравномерного рационального B-сплайна ([нурбс](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="102c5-106">The **gluBeginTrim** and [**gluEndTrim**](gluendtrim.md) functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) trimming loop definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="102c5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="102c5-107">Syntax</span></span>


```C++
void WINAPI gluBeginTrim(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="102c5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="102c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="102c5-109">*нобж*</span><span class="sxs-lookup"><span data-stu-id="102c5-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="102c5-110">Объект НУРБС (созданный с помощью [**глуневнурбсрендерер**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="102c5-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="102c5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="102c5-111">Return value</span></span>

<span data-ttu-id="102c5-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="102c5-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="102c5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="102c5-113">Remarks</span></span>

<span data-ttu-id="102c5-114">Используйте **глубегинтрим** , чтобы пометить начало цикла усечения, и **глуендтрим** , чтобы отметить конец цикла обрезки.</span><span class="sxs-lookup"><span data-stu-id="102c5-114">Use **gluBeginTrim** to mark the beginning of a trimming loop, and **gluEndTrim** to mark the end of a trimming loop.</span></span> <span data-ttu-id="102c5-115">Цикл обрезки — это набор ориентированных сегментов кривой (формирующих замкнутую кривую), определяющий границы НУРБС поверхности.</span><span class="sxs-lookup"><span data-stu-id="102c5-115">A trimming loop is a set of oriented curve segments (forming a closed curve) that define boundaries of a NURBS surface.</span></span> <span data-ttu-id="102c5-116">Эти циклы обрезки включаются в определение НУРБС поверхности между вызовами [**глубегинсурфаце**](glubeginsurface.md) и [**глуендсурфаце**](gluendsurface.md).</span><span class="sxs-lookup"><span data-stu-id="102c5-116">You include these trimming loops in the definition of a NURBS surface, between calls to [**gluBeginSurface**](glubeginsurface.md) and [**gluEndSurface**](gluendsurface.md).</span></span>

<span data-ttu-id="102c5-117">Определение поверхности НУРБС может содержать много циклов обрезки.</span><span class="sxs-lookup"><span data-stu-id="102c5-117">The definition for a NURBS surface can contain many trimming loops.</span></span> <span data-ttu-id="102c5-118">Например, при написании определения для НУРБС поверхности, напоминающей прямоугольник с перфорацией, определение будет содержать два цикла обрезки.</span><span class="sxs-lookup"><span data-stu-id="102c5-118">For example, if you write a definition for a NURBS surface that resembles a rectangle with a hole punched out, the definition would contain two trimming loops.</span></span> <span data-ttu-id="102c5-119">В одном цикле определяется внешнее ребро прямоугольника. во второй определяется Дырокол с перфорацией.</span><span class="sxs-lookup"><span data-stu-id="102c5-119">One loop would define the outer edge of the rectangle; the other would define the punched-out hole.</span></span> <span data-ttu-id="102c5-120">Определения каждого из этих циклов обрезки будут заключаться в скобки парой **глубегинтрим**  /  **глуендтрим** .</span><span class="sxs-lookup"><span data-stu-id="102c5-120">The definitions of each of these trimming loops would be bracketed by a **gluBeginTrim** / **gluEndTrim** pair.</span></span>

<span data-ttu-id="102c5-121">Определение одного замкнутого цикла обрезки может состоять из нескольких сегментов кривой, каждый из которых описан как ряд сегментов линии, образующих линейную кривую (см. [**глупвлкурве**](glupwlcurve.md)), в виде одной нурбс кривой (см. [**глунурбскурве**](glunurbscurve.md)) или как сочетание обоих в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="102c5-121">The definition of a single closed trimming loop can consist of multiple curve segments, each described as a series of line segments that form a linear curve (see [**gluPwlCurve**](glupwlcurve.md)), as a single NURBS curve (see [**gluNurbsCurve**](glunurbscurve.md)), or as a combination of both in any order.</span></span> <span data-ttu-id="102c5-122">Единственными вызовами библиотеки, которые могут присутствовать в определении цикла усечения (между вызовами **глубегинтрим** и **глуендтрим**), являются **глупвлкурве** и **глунурбскурве**.</span><span class="sxs-lookup"><span data-stu-id="102c5-122">The only library calls that can appear in a trimming-loop definition (between the calls to **gluBeginTrim** and **gluEndTrim**) are **gluPwlCurve** and **gluNurbsCurve**.</span></span>

<span data-ttu-id="102c5-123">Область, отображаемая на поверхности НУРБС, является областью в домене слева от кривой обрезки по мере увеличения параметра кривой.</span><span class="sxs-lookup"><span data-stu-id="102c5-123">The displayed area of the NURBS surface is the region in the domain to the left of the trimming curve as the curve parameter increases.</span></span> <span data-ttu-id="102c5-124">Таким же местом, где удерживается область НУРБС, находится внутри цикла обрезки против часовой стрелки и за пределами цикла обрезки по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="102c5-124">Thus, the retained region of the NURBS surface is inside a counterclockwise trimming loop and outside a clockwise trimming loop.</span></span> <span data-ttu-id="102c5-125">Для прямоугольника, упомянутого ранее, цикл обрезки внешнего края прямоугольника выполняется против часовой стрелки, а цикл обрезки для отверстия с перфорацией выполняется по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="102c5-125">For the rectangle mentioned earlier, the trimming loop for the outer edge of the rectangle runs counterclockwise, while the trimming loop for the punched-out hole runs clockwise.</span></span>

<span data-ttu-id="102c5-126">Если для определения одного цикла обрезки используется более одной кривой, сегменты кривой должны образовывать замкнутый цикл (то есть конечная точка каждой кривой должна быть начальной точкой следующей кривой, а конечная точка конечной кривой должна быть начальной точкой первой кривой).</span><span class="sxs-lookup"><span data-stu-id="102c5-126">If you use more than one curve to define a single trimming loop, the curve segments must form a closed loop (that is, the endpoint of each curve must be the starting point of the next curve, and the endpoint of the final curve must be the starting point of the first curve).</span></span> <span data-ttu-id="102c5-127">Если конечные точки кривой достаточно близки друг к другу, но не полностью коинЦидент, они будут принудительно согласованы.</span><span class="sxs-lookup"><span data-stu-id="102c5-127">If the endpoints of the curve are sufficiently close together but not exactly coincident, they will be forced to match.</span></span> <span data-ttu-id="102c5-128">Если конечные точки недостаточно близки, возникает ошибка (см. [*глунурбскаллбакк*](glunurbs.md)).</span><span class="sxs-lookup"><span data-stu-id="102c5-128">If the endpoints are not sufficiently close, an error results (see [*gluNurbsCallback*](glunurbs.md)).</span></span>

<span data-ttu-id="102c5-129">Если определение цикла усечения содержит несколько кривых, направление кривых должно быть согласованным (то есть внутри должно быть слева от всех кривых).</span><span class="sxs-lookup"><span data-stu-id="102c5-129">If a trimming-loop definition contains multiple curves, the direction of the curves must be consistent (that is, the inside must be to the left of all of the curves).</span></span> <span data-ttu-id="102c5-130">Вложенные циклы усечения можно использовать при условии, что ориентация кривой имеют правильный запас.</span><span class="sxs-lookup"><span data-stu-id="102c5-130">You can use nested trimming loops as long as the curve orientations alternate correctly.</span></span> <span data-ttu-id="102c5-131">Обрезанные кривые не могут быть самопересекающимися и не могут пересекать друг друга (или результаты ошибки).</span><span class="sxs-lookup"><span data-stu-id="102c5-131">Trimming curves cannot be self-intersecting, nor can they intersect one another (or an error results).</span></span>

<span data-ttu-id="102c5-132">Если для поверхности НУРБС не заданы сведения об обрезке, рисуется вся поверхность.</span><span class="sxs-lookup"><span data-stu-id="102c5-132">If no trimming information is given for a NURBS surface, the entire surface is drawn.</span></span>

## <a name="examples"></a><span data-ttu-id="102c5-133">Примеры</span><span class="sxs-lookup"><span data-stu-id="102c5-133">Examples</span></span>

<span data-ttu-id="102c5-134">Этот фрагмент кода определяет цикл обрезки, который состоит из одной линейной кривой кусочно-и двух НУРБС кривых:</span><span class="sxs-lookup"><span data-stu-id="102c5-134">This code fragment defines a trimming loop that consists of one piecewise linear curve and two NURBS curves:</span></span>

``` syntax
gluBeginTrim(nobj); 
    gluPwlCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_3);  
gluEndTrim(nobj);
```

## <a name="requirements"></a><span data-ttu-id="102c5-135">Требования</span><span class="sxs-lookup"><span data-stu-id="102c5-135">Requirements</span></span>



| <span data-ttu-id="102c5-136">Требование</span><span class="sxs-lookup"><span data-stu-id="102c5-136">Requirement</span></span> | <span data-ttu-id="102c5-137">Значение</span><span class="sxs-lookup"><span data-stu-id="102c5-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="102c5-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="102c5-138">Minimum supported client</span></span><br/> | <span data-ttu-id="102c5-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="102c5-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="102c5-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="102c5-140">Minimum supported server</span></span><br/> | <span data-ttu-id="102c5-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="102c5-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="102c5-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="102c5-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="102c5-143"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="102c5-143"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="102c5-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="102c5-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="102c5-145"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="102c5-145"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="102c5-146">DLL</span><span class="sxs-lookup"><span data-stu-id="102c5-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="102c5-147"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="102c5-147"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="102c5-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="102c5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="102c5-149">**глубегинсурфаце**</span><span class="sxs-lookup"><span data-stu-id="102c5-149">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="102c5-150">**глуендсурфаце**</span><span class="sxs-lookup"><span data-stu-id="102c5-150">**gluEndSurface**</span></span>](gluendsurface.md)
</dt> <dt>

[<span data-ttu-id="102c5-151">**глуневнурбсрендерер**</span><span class="sxs-lookup"><span data-stu-id="102c5-151">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="102c5-152">*глунурбскаллбакк*</span><span class="sxs-lookup"><span data-stu-id="102c5-152">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="102c5-153">**глунурбскурве**</span><span class="sxs-lookup"><span data-stu-id="102c5-153">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="102c5-154">**глупвлкурве**</span><span class="sxs-lookup"><span data-stu-id="102c5-154">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





