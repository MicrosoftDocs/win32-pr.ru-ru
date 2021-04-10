---
title: Функция Глуендтрим (GLU. h)
description: Функции Глубегинтрим и Глуендтрим разделяют определение цикла неравномерного рационального B-сплайна (НУРБС). | Функция Глуендтрим (GLU. h)
ms.assetid: e85cc60b-4492-441d-b778-31a3d52b398a
keywords:
- Функция Глуендтрим OpenGL
topic_type:
- apiref
api_name:
- gluEndTrim
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4105cc911105f0444ba17c6b57a3deb048bc96d2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104081782"
---
# <a name="gluendtrim-function"></a><span data-ttu-id="ef21d-105">Функция Глуендтрим</span><span class="sxs-lookup"><span data-stu-id="ef21d-105">gluEndTrim function</span></span>

<span data-ttu-id="ef21d-106">Функции [**глубегинтрим**](glubegintrim.md) и **глуендтрим** разделяют определение цикла неравномерного рационального B-сплайна ([нурбс](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="ef21d-106">The [**gluBeginTrim**](glubegintrim.md) and **gluEndTrim** functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) trimming loop definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef21d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef21d-107">Syntax</span></span>


```C++
void WINAPI gluEndTrim(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="ef21d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef21d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef21d-109">*нобж*</span><span class="sxs-lookup"><span data-stu-id="ef21d-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="ef21d-110">Объект НУРБС (созданный с помощью [**глуневнурбсрендерер**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="ef21d-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef21d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef21d-111">Return value</span></span>

<span data-ttu-id="ef21d-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ef21d-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef21d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef21d-113">Remarks</span></span>

<span data-ttu-id="ef21d-114">Используйте [**глубегинтрим**](glubegintrim.md) , чтобы пометить начало цикла усечения, и **глуендтрим** , чтобы отметить конец цикла обрезки.</span><span class="sxs-lookup"><span data-stu-id="ef21d-114">Use [**gluBeginTrim**](glubegintrim.md) to mark the beginning of a trimming loop, and **gluEndTrim** to mark the end of a trimming loop.</span></span> <span data-ttu-id="ef21d-115">Цикл обрезки — это набор ориентированных сегментов кривой (формирующих замкнутую кривую), определяющий границы НУРБС поверхности.</span><span class="sxs-lookup"><span data-stu-id="ef21d-115">A trimming loop is a set of oriented curve segments (forming a closed curve) that define boundaries of a NURBS surface.</span></span> <span data-ttu-id="ef21d-116">Эти циклы обрезки включаются в определение НУРБС поверхности между вызовами [**глубегинсурфаце**](glubeginsurface.md) и [**глуендсурфаце**](gluendsurface.md).</span><span class="sxs-lookup"><span data-stu-id="ef21d-116">You include these trimming loops in the definition of a NURBS surface, between calls to [**gluBeginSurface**](glubeginsurface.md) and [**gluEndSurface**](gluendsurface.md).</span></span>

<span data-ttu-id="ef21d-117">Определение поверхности НУРБС может содержать много циклов обрезки.</span><span class="sxs-lookup"><span data-stu-id="ef21d-117">The definition for a NURBS surface can contain many trimming loops.</span></span> <span data-ttu-id="ef21d-118">Например, при написании определения для НУРБС поверхности, напоминающей прямоугольник с перфорацией, определение будет содержать два цикла обрезки.</span><span class="sxs-lookup"><span data-stu-id="ef21d-118">For example, if you write a definition for a NURBS surface that resembles a rectangle with a hole punched out, the definition would contain two trimming loops.</span></span> <span data-ttu-id="ef21d-119">В одном цикле определяется внешнее ребро прямоугольника. во второй определяется Дырокол с перфорацией.</span><span class="sxs-lookup"><span data-stu-id="ef21d-119">One loop would define the outer edge of the rectangle; the other would define the punched-out hole.</span></span> <span data-ttu-id="ef21d-120">Определения каждого из этих циклов обрезки будут заключаться в скобки парой [**глубегинтрим**](glubegintrim.md)  /  **глуендтрим** .</span><span class="sxs-lookup"><span data-stu-id="ef21d-120">The definitions of each of these trimming loops would be bracketed by a [**gluBeginTrim**](glubegintrim.md) / **gluEndTrim** pair.</span></span>

<span data-ttu-id="ef21d-121">Определение одного замкнутого цикла обрезки может состоять из нескольких сегментов кривой, каждый из которых описан как ряд сегментов линии, образующих линейную кривую (см. [**глупвлкурве**](glupwlcurve.md)), в виде одной нурбс кривой (см. [**глунурбскурве**](glunurbscurve.md)) или как сочетание обоих в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="ef21d-121">The definition of a single closed trimming loop can consist of multiple curve segments, each described as a series of line segments that form a linear curve (see [**gluPwlCurve**](glupwlcurve.md)), as a single NURBS curve (see [**gluNurbsCurve**](glunurbscurve.md)), or as a combination of both in any order.</span></span> <span data-ttu-id="ef21d-122">Единственными вызовами библиотеки, которые могут присутствовать в определении цикла усечения (между вызовами [**глубегинтрим**](glubegintrim.md) и **глуендтрим**), являются **глупвлкурве** и **глунурбскурве**.</span><span class="sxs-lookup"><span data-stu-id="ef21d-122">The only library calls that can appear in a trimming-loop definition (between the calls to [**gluBeginTrim**](glubegintrim.md) and **gluEndTrim**) are **gluPwlCurve** and **gluNurbsCurve**.</span></span>

<span data-ttu-id="ef21d-123">Область, отображаемая на поверхности НУРБС, является областью в домене слева от кривой обрезки по мере увеличения параметра кривой.</span><span class="sxs-lookup"><span data-stu-id="ef21d-123">The displayed area of the NURBS surface is the region in the domain to the left of the trimming curve as the curve parameter increases.</span></span> <span data-ttu-id="ef21d-124">Таким же местом, где удерживается область НУРБС, находится внутри цикла обрезки против часовой стрелки и за пределами цикла обрезки по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="ef21d-124">Thus, the retained region of the NURBS surface is inside a counterclockwise trimming loop and outside a clockwise trimming loop.</span></span> <span data-ttu-id="ef21d-125">Для прямоугольника, упомянутого ранее, цикл обрезки внешнего края прямоугольника выполняется против часовой стрелки, а цикл обрезки для отверстия с перфорацией выполняется по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="ef21d-125">For the rectangle mentioned earlier, the trimming loop for the outer edge of the rectangle runs counterclockwise, while the trimming loop for the punched-out hole runs clockwise.</span></span>

<span data-ttu-id="ef21d-126">Если для определения одного цикла обрезки используется более одной кривой, сегменты кривой должны образовывать замкнутый цикл (то есть конечная точка каждой кривой должна быть начальной точкой следующей кривой, а конечная точка конечной кривой должна быть начальной точкой первой кривой).</span><span class="sxs-lookup"><span data-stu-id="ef21d-126">If you use more than one curve to define a single trimming loop, the curve segments must form a closed loop (that is, the endpoint of each curve must be the starting point of the next curve, and the endpoint of the final curve must be the starting point of the first curve).</span></span> <span data-ttu-id="ef21d-127">Если конечные точки кривой достаточно близки друг к другу, но не полностью коинЦидент, они будут принудительно согласованы.</span><span class="sxs-lookup"><span data-stu-id="ef21d-127">If the endpoints of the curve are sufficiently close together but not exactly coincident, they will be forced to match.</span></span> <span data-ttu-id="ef21d-128">Если конечные точки недостаточно близки, возникает ошибка (см. [*глунурбскаллбакк*](glunurbs.md)).</span><span class="sxs-lookup"><span data-stu-id="ef21d-128">If the endpoints are not sufficiently close, an error results (see [*gluNurbsCallback*](glunurbs.md)).</span></span>

<span data-ttu-id="ef21d-129">Если определение цикла усечения содержит несколько кривых, направление кривых должно быть согласованным (то есть внутри должно быть слева от всех кривых).</span><span class="sxs-lookup"><span data-stu-id="ef21d-129">If a trimming-loop definition contains multiple curves, the direction of the curves must be consistent (that is, the inside must be to the left of all of the curves).</span></span> <span data-ttu-id="ef21d-130">Вложенные циклы усечения можно использовать при условии, что ориентация кривой имеют правильный запас.</span><span class="sxs-lookup"><span data-stu-id="ef21d-130">You can use nested trimming loops as long as the curve orientations alternate correctly.</span></span> <span data-ttu-id="ef21d-131">Обрезанные кривые не могут быть самопересекающимися и не могут пересекать друг друга (или результаты ошибки).</span><span class="sxs-lookup"><span data-stu-id="ef21d-131">Trimming curves cannot be self-intersecting, nor can they intersect one another (or an error results).</span></span>

<span data-ttu-id="ef21d-132">Если для поверхности НУРБС не заданы сведения об обрезке, рисуется вся поверхность.</span><span class="sxs-lookup"><span data-stu-id="ef21d-132">If no trimming information is given for a NURBS surface, the entire surface is drawn.</span></span>

## <a name="examples"></a><span data-ttu-id="ef21d-133">Примеры</span><span class="sxs-lookup"><span data-stu-id="ef21d-133">Examples</span></span>

<span data-ttu-id="ef21d-134">Этот фрагмент кода определяет цикл обрезки, который состоит из одной линейной кривой кусочно-и двух НУРБС кривых:</span><span class="sxs-lookup"><span data-stu-id="ef21d-134">This code fragment defines a trimming loop that consists of one piecewise linear curve and two NURBS curves:</span></span>

``` syntax
gluBeginTrim(nobj); 
    gluPwlCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_3);  
gluEndTrim(nobj);
```

## <a name="requirements"></a><span data-ttu-id="ef21d-135">Требования</span><span class="sxs-lookup"><span data-stu-id="ef21d-135">Requirements</span></span>



| <span data-ttu-id="ef21d-136">Требование</span><span class="sxs-lookup"><span data-stu-id="ef21d-136">Requirement</span></span> | <span data-ttu-id="ef21d-137">Значение</span><span class="sxs-lookup"><span data-stu-id="ef21d-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ef21d-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef21d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ef21d-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ef21d-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ef21d-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef21d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ef21d-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ef21d-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ef21d-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ef21d-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef21d-143"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef21d-143"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="ef21d-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ef21d-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef21d-145"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef21d-145"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ef21d-146">DLL</span><span class="sxs-lookup"><span data-stu-id="ef21d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef21d-147"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef21d-147"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef21d-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef21d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef21d-149">**глубегинсурфаце**</span><span class="sxs-lookup"><span data-stu-id="ef21d-149">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="ef21d-150">**глуендсурфаце**</span><span class="sxs-lookup"><span data-stu-id="ef21d-150">**gluEndSurface**</span></span>](gluendsurface.md)
</dt> <dt>

[<span data-ttu-id="ef21d-151">**глуневнурбсрендерер**</span><span class="sxs-lookup"><span data-stu-id="ef21d-151">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="ef21d-152">*глунурбскаллбакк*</span><span class="sxs-lookup"><span data-stu-id="ef21d-152">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="ef21d-153">**глунурбскурве**</span><span class="sxs-lookup"><span data-stu-id="ef21d-153">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="ef21d-154">**глупвлкурве**</span><span class="sxs-lookup"><span data-stu-id="ef21d-154">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





