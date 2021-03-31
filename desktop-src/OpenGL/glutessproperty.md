---
title: Функция Глутесспроперти (GLU. h)
description: Функция Глутесспроперти задает свойство объекта тесселяции.
ms.assetid: 1306b9ef-4f1e-4684-99ea-464bae1d0a61
keywords:
- Функция Глутесспроперти OpenGL
topic_type:
- apiref
api_name:
- gluTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe21f2961cd4cb1df31a1fdb3f407a71d6e6d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137378"
---
# <a name="glutessproperty-function"></a><span data-ttu-id="d31d9-104">Функция Глутесспроперти</span><span class="sxs-lookup"><span data-stu-id="d31d9-104">gluTessProperty function</span></span>

<span data-ttu-id="d31d9-105">Функция **глутесспроперти** задает свойство объекта тесселяции.</span><span class="sxs-lookup"><span data-stu-id="d31d9-105">The **gluTessProperty** function sets the property of a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d31d9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d31d9-106">Syntax</span></span>


```C++
void WINAPI gluTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      value
);
```



## <a name="parameters"></a><span data-ttu-id="d31d9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d31d9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d31d9-108">*тесс*</span><span class="sxs-lookup"><span data-stu-id="d31d9-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="d31d9-109">Объект тесселяции (созданный с помощью [**глуневтесс**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="d31d9-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d31d9-110">*какую*</span><span class="sxs-lookup"><span data-stu-id="d31d9-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="d31d9-111">Задаваемое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="d31d9-111">The property value to set.</span></span> <span data-ttu-id="d31d9-112">Допустимы следующие значения: GLU \_ Тесс \_ обмотка \_ , Glu \_ Тесс \_ \_ only и Glu \_ Тесс \_ .</span><span class="sxs-lookup"><span data-stu-id="d31d9-112">The following values are valid: GLU\_TESS\_WINDING\_RULE, GLU\_TESS\_BOUNDARY\_ONLY, and GLU\_TESS\_TOLERANCE.</span></span>



| <span data-ttu-id="d31d9-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d31d9-113">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="d31d9-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d31d9-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_TESS_WINDING_RULE"></span><span id="glu_tess_winding_rule"></span><dl> <span data-ttu-id="d31d9-115"><dt>**\_правило Glu Тесс \_ обмотка \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d31d9-115"><dt>**GLU\_TESS\_WINDING\_RULE**</dt></span></span> </dl>    | <span data-ttu-id="d31d9-116">Определяет, какие части многоугольника находятся на внутреннем.</span><span class="sxs-lookup"><span data-stu-id="d31d9-116">Determines which parts of the polygon are on the interior.</span></span> <span data-ttu-id="d31d9-117">Параметру value может быть присвоено одно из следующих значений: GLU \_ Тесс \_ Ветер \_ , Glu \_ Тесс ветер, \_ \_ ненулевое значение, Glu \_ Тесс \_ обмотка \_ , Glu Тесс \_ \_ обмотка \_ или Glu \_ Тесс \_ обмотка а \_ ABS \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d31d9-117">The value parameter may be set to one of the following: GLU\_TESS\_WINDING\_ODD, GLU\_TESS\_WINDING\_NONZERO, GLU\_TESS\_WINDING\_POSITIVE, GLU\_TESS\_WINDING\_NEGATIVE, or GLU\_TESS\_WINDING\_ABS\_GEQ\_TWO.</span></span> <br/> <span data-ttu-id="d31d9-118">Чтобы понять, как работает правило поворота, сначала рассмотрите возможность того, чтобы в качестве входных данных секционировать плоскость на регионы.</span><span class="sxs-lookup"><span data-stu-id="d31d9-118">To understand how the winding rule works, first consider that the input contours partition the plane into regions.</span></span> <span data-ttu-id="d31d9-119">Правило поворота определяет, какие из этих регионов находятся внутри многоугольника.</span><span class="sxs-lookup"><span data-stu-id="d31d9-119">The winding rule determines which of these regions are inside the polygon.</span></span><br/> <span data-ttu-id="d31d9-120">Для одного профиля C номер обмотки точки x — это просто число революции, которое мы делаем по оси x, так как мы переносимся по пути в C (где против часовой стрелки).</span><span class="sxs-lookup"><span data-stu-id="d31d9-120">For a single-contour C, the winding number of a point x is simply the signed number of revolutions we make around x as we travel once around C (where counterclockwise is positive).</span></span> <span data-ttu-id="d31d9-121">Если существует несколько контуров, отдельные номера обмотки суммируются.</span><span class="sxs-lookup"><span data-stu-id="d31d9-121">When there are several contours, the individual winding numbers are summed.</span></span> <span data-ttu-id="d31d9-122">Эта процедура связывает целочисленное значение со знаком с каждой точкой x в плоскости.</span><span class="sxs-lookup"><span data-stu-id="d31d9-122">This procedure associates a signed integer value with each point x in the plane.</span></span> <span data-ttu-id="d31d9-123">Обратите внимание, что номер обмотки одинаков для всех точек в одном регионе.</span><span class="sxs-lookup"><span data-stu-id="d31d9-123">Note that the winding number is the same for all points in a single region.</span></span><br/> <span data-ttu-id="d31d9-124">Правило поворота классифицирует регион как "внутри", если его номер обмотки относится к выбранной категории (нечетное, ненулевое, положительное, отрицательное или абсолютное значение по крайней мере двух).</span><span class="sxs-lookup"><span data-stu-id="d31d9-124">The winding rule classifies a region as "inside" if its winding number belongs to the chosen category (odd, nonzero, positive, negative, or absolute value of at least two).</span></span> <span data-ttu-id="d31d9-125">Предыдущая GLU-тесселяция (до GLU 1,2) использовала правило "нечетное".</span><span class="sxs-lookup"><span data-stu-id="d31d9-125">The previous GLU tessellator (prior to GLU 1.2) used the "odd" rule.</span></span> <span data-ttu-id="d31d9-126">Ненулевое правило (GLU \_ Тесс \_ обмотка \_ ненулевой) — это еще один распространенный способ определения внутренней части.</span><span class="sxs-lookup"><span data-stu-id="d31d9-126">The "nonzero" rule (GLU\_TESS\_WINDING\_NONZERO) is another common way to define the interior.</span></span> <span data-ttu-id="d31d9-127">Другие три правила (GLU \_ Тесс \_ обмотка \_ , Glu \_ Тесс \_ обмотка с отрицательным числом, \_ Glu \_ Тесс \_ обмотка \_ ABS \_ жек \_ 2) полезны для многоугольных операций.</span><span class="sxs-lookup"><span data-stu-id="d31d9-127">The other three rules (GLU\_TESS\_WINDING\_POSITIVE, GLU\_TESS\_WINDING\_NEGATIVE, GLU\_TESS\_WINDING\_ABS\_GEQ\_TWO) are useful for polygon CSG operations.</span></span><br/> |
| <span id="GLU_TESS_BOUNDARY_ONLY"></span><span id="glu_tess_boundary_only"></span><dl> <span data-ttu-id="d31d9-128"><dt>**GLU \_ Тесс \_ \_ только граница**</dt></span><span class="sxs-lookup"><span data-stu-id="d31d9-128"><dt>**GLU\_TESS\_BOUNDARY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="d31d9-129">Задает логическое значение (значение GL \_ true или GL \_ false).</span><span class="sxs-lookup"><span data-stu-id="d31d9-129">Specifies a Boolean value (set value to GL\_TRUE or GL\_FALSE).</span></span> <span data-ttu-id="d31d9-130">Если для параметра value задано значение «GL \_ true», то вместо тесселяции возвращается набор замкнутых контуров, разделяющих внутреннюю и наружную части многоугольника.</span><span class="sxs-lookup"><span data-stu-id="d31d9-130">When you set value to GL\_TRUE, a set of closed contours separating the polygon interior and exterior is returned instead of a tessellation.</span></span> <span data-ttu-id="d31d9-131">Наружные контуры ориентированы против часовой стрелки относительно обычного. внутренние контуры ориентированы по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="d31d9-131">Exterior contours are oriented counterclockwise with respect to the normal; interior contours are oriented clockwise.</span></span> <span data-ttu-id="d31d9-132">\_ \_ Обратные вызовы данных Glu Тесс Begin и Glu \_ ТЕСС \_ \_ используют тип GL \_ Line \_ петля для каждого профиля.</span><span class="sxs-lookup"><span data-stu-id="d31d9-132">The GLU\_TESS\_BEGIN and GLU\_TESS\_BEGIN\_DATA callbacks use the type GL\_LINE\_LOOP for each contour.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GLU_TESS_TOLERANCE"></span><span id="glu_tess_tolerance"></span><dl> <span data-ttu-id="d31d9-133"><dt>**\_допуск Glu Тесс \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d31d9-133"><dt>**GLU\_TESS\_TOLERANCE**</dt></span></span> </dl>              | <span data-ttu-id="d31d9-134">Указывает допуск для слияния функций, чтобы уменьшить размер выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d31d9-134">Specifies a tolerance for merging features to reduce the size of the output.</span></span> <span data-ttu-id="d31d9-135">Например, две вершины, которые очень близки друг к другу, могут быть заменены одной вершиной.</span><span class="sxs-lookup"><span data-stu-id="d31d9-135">For example, two vertexes that are very close to each other might be replaced by a single vertex.</span></span> <span data-ttu-id="d31d9-136">Допуск умножается на максимальную координату любой входной вершины. Указывает максимальное расстояние, которое может быть перенесено любой функцией в результате одной операции слияния.</span><span class="sxs-lookup"><span data-stu-id="d31d9-136">The tolerance is multiplied by the largest coordinate magnitude of any input vertex; this specifies the maximum distance that any feature can move as the result of a single merge operation.</span></span> <span data-ttu-id="d31d9-137">Если один компонент принимает участие в нескольких операциях слияния, то общее расстояние перемещения может быть больше.</span><span class="sxs-lookup"><span data-stu-id="d31d9-137">If a single feature takes part in several merge operations, the total distance moved can be larger.</span></span> <br/> <span data-ttu-id="d31d9-138">Слияние функций является полностью необязательным; допуск — это только подсказка.</span><span class="sxs-lookup"><span data-stu-id="d31d9-138">Feature merging is completely optional; the tolerance is only a hint.</span></span> <span data-ttu-id="d31d9-139">Реализация может быть объединена в некоторых случаях, а не в других, или вообще не объединять функции.</span><span class="sxs-lookup"><span data-stu-id="d31d9-139">The implementation is free to merge in some cases and not in others, or to never merge features at all.</span></span> <span data-ttu-id="d31d9-140">Допуск по умолчанию равен нулю.</span><span class="sxs-lookup"><span data-stu-id="d31d9-140">The default tolerance is zero.</span></span><br/> <span data-ttu-id="d31d9-141">Текущая реализация выполняет слияние вершин только в том случае, если они точно коинЦидент, независимо от текущей допустимости.</span><span class="sxs-lookup"><span data-stu-id="d31d9-141">The current implementation merges vertexes only if they are exactly coincident, regardless of the current tolerance.</span></span> <span data-ttu-id="d31d9-142">Вершина присоединиться к границе, только если реализация не может определить, на какой стороне располагает вершина.</span><span class="sxs-lookup"><span data-stu-id="d31d9-142">A vertex is spliced into an edge only if the implementation is unable to distinguish which side of the edge the vertex lies on.</span></span> <span data-ttu-id="d31d9-143">Слияние двух ребер выполняется только в том случае, если обе конечные точки идентичны.</span><span class="sxs-lookup"><span data-stu-id="d31d9-143">Two edges are merged only when both endpoints are identical.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="d31d9-144">*value*</span><span class="sxs-lookup"><span data-stu-id="d31d9-144">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="d31d9-145">Значение указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="d31d9-145">The value of the indicated property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d31d9-146">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d31d9-146">Return value</span></span>

<span data-ttu-id="d31d9-147">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d31d9-147">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d31d9-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d31d9-148">Remarks</span></span>

<span data-ttu-id="d31d9-149">Функция **глутесспроперти** управляет свойствами, хранящимися в объекте тесселяции.</span><span class="sxs-lookup"><span data-stu-id="d31d9-149">The **gluTessProperty** function controls properties stored in a tessellation object.</span></span> <span data-ttu-id="d31d9-150">Эти свойства влияют на способ интерпретации и отрисовки многоугольников.</span><span class="sxs-lookup"><span data-stu-id="d31d9-150">These properties affect the way the polygons are interpreted and rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="d31d9-151">Требования</span><span class="sxs-lookup"><span data-stu-id="d31d9-151">Requirements</span></span>



| <span data-ttu-id="d31d9-152">Требование</span><span class="sxs-lookup"><span data-stu-id="d31d9-152">Requirement</span></span> | <span data-ttu-id="d31d9-153">Значение</span><span class="sxs-lookup"><span data-stu-id="d31d9-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d31d9-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d31d9-154">Minimum supported client</span></span><br/> | <span data-ttu-id="d31d9-155">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d31d9-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d31d9-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d31d9-156">Minimum supported server</span></span><br/> | <span data-ttu-id="d31d9-157">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d31d9-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d31d9-158">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d31d9-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="d31d9-159"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="d31d9-159"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="d31d9-160">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d31d9-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="d31d9-161"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d31d9-161"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d31d9-162">DLL</span><span class="sxs-lookup"><span data-stu-id="d31d9-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d31d9-163"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d31d9-163"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d31d9-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d31d9-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d31d9-165">**глужеттесспроперти**</span><span class="sxs-lookup"><span data-stu-id="d31d9-165">**gluGetTessProperty**</span></span>](glugettessproperty.md)
</dt> <dt>

[<span data-ttu-id="d31d9-166">**глуневтесс**</span><span class="sxs-lookup"><span data-stu-id="d31d9-166">**gluNewTess**</span></span>](glunewtess.md)
</dt> </dl>

 

 





