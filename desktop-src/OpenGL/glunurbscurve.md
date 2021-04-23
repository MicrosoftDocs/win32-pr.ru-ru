---
title: Функция Глунурбскурве (GLU. h)
description: Функция Глунурбскурве определяет форму неоднородной кривой B-сплайна (НУРБС).
ms.assetid: d03064a5-26f5-487f-877f-3748646bcb2f
keywords:
- Функция Глунурбскурве OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e3d5fe35e994afa4b5d8b91c4244573132c5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672595"
---
# <a name="glunurbscurve-function"></a><span data-ttu-id="89f24-104">Функция Глунурбскурве</span><span class="sxs-lookup"><span data-stu-id="89f24-104">gluNurbsCurve function</span></span>

<span data-ttu-id="89f24-105">Функция **глунурбскурве** определяет форму неоднородной кривой B-сплайна ([нурбс](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="89f24-105">The **gluNurbsCurve** function defines the shape of a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="89f24-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89f24-106">Syntax</span></span>


```C++
void WINAPI gluNurbsCurve(
   GLUnurbs *nobj,
   GLint    nknots,
   GLfloat  *knot,
   GLint    stride,
   GLfloat  *ctlarray,
   GLint    order,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="89f24-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="89f24-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89f24-108">*нобж*</span><span class="sxs-lookup"><span data-stu-id="89f24-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="89f24-109">Объект НУРБС (созданный с помощью [**глуневнурбсрендерер**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="89f24-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="89f24-110">*нкнотс*</span><span class="sxs-lookup"><span data-stu-id="89f24-110">*nknots*</span></span> 
</dt> <dd>

<span data-ttu-id="89f24-111">Число Кнотс в *релевантной*.</span><span class="sxs-lookup"><span data-stu-id="89f24-111">The number of knots in *knot*.</span></span> <span data-ttu-id="89f24-112">Параметр *нкнотс* равен числу контрольных точек и порядку.</span><span class="sxs-lookup"><span data-stu-id="89f24-112">The *nknots* parameter equals the number of control points plus the order.</span></span>

</dd> <dt>

<span data-ttu-id="89f24-113">*релевантной*</span><span class="sxs-lookup"><span data-stu-id="89f24-113">*knot*</span></span> 
</dt> <dd>

<span data-ttu-id="89f24-114">Массив значений релевантной нондекреасинг *нкнотс* .</span><span class="sxs-lookup"><span data-stu-id="89f24-114">An array of *nknots* nondecreasing knot values.</span></span>

</dd> <dt>

<span data-ttu-id="89f24-115">*шага*</span><span class="sxs-lookup"><span data-stu-id="89f24-115">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="89f24-116">Смещение (в виде количества значений с плавающей запятой одиночной точности) между последовательными контрольными точками кривой.</span><span class="sxs-lookup"><span data-stu-id="89f24-116">The offset (as a number of single-precision floating-point values) between successive curve control points.</span></span>

</dd> <dt>

<span data-ttu-id="89f24-117">*ктларрай*</span><span class="sxs-lookup"><span data-stu-id="89f24-117">*ctlarray*</span></span> 
</dt> <dd>

<span data-ttu-id="89f24-118">Указатель на массив контрольных точек.</span><span class="sxs-lookup"><span data-stu-id="89f24-118">A pointer to an array of control points.</span></span> <span data-ttu-id="89f24-119">Координаты должны быть согласованы с *типом*.</span><span class="sxs-lookup"><span data-stu-id="89f24-119">The coordinates must agree with *type*.</span></span>

</dd> <dt>

<span data-ttu-id="89f24-120">*order*</span><span class="sxs-lookup"><span data-stu-id="89f24-120">*order*</span></span> 
</dt> <dd>

<span data-ttu-id="89f24-121">Порядок кривой НУРБС.</span><span class="sxs-lookup"><span data-stu-id="89f24-121">The order of the NURBS curve.</span></span> <span data-ttu-id="89f24-122">Параметр *порядка* равен degree + 1; Таким образом, кривая третьего порядка имеет порядковый номер 4.</span><span class="sxs-lookup"><span data-stu-id="89f24-122">The *order* parameter equals degree + 1; hence a cubic curve has an order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="89f24-123">*type*</span><span class="sxs-lookup"><span data-stu-id="89f24-123">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="89f24-124">Тип кривой.</span><span class="sxs-lookup"><span data-stu-id="89f24-124">The type of the curve.</span></span> <span data-ttu-id="89f24-125">Если эта кривая определена в паре [**глубегинкурве**](glubegincurve.md) / [**глуендкурве**](gluendcurve.md) , то тип может быть любым допустимым типом одномерного оценщика (например, GL \_ «Карта1» \_ вершиной \_ 3 или GL \_ «Карта1» \_ Color \_ 4).</span><span class="sxs-lookup"><span data-stu-id="89f24-125">If this curve is defined within a [**gluBeginCurve**](glubegincurve.md)/[**gluEndCurve**](gluendcurve.md) pair, then the type can be any of the valid one-dimensional evaluator types (such as GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_COLOR\_4).</span></span> <span data-ttu-id="89f24-126">Между парой [**глубегинтрим**](glubegintrim.md) / [**глуендтрим**](gluendtrim.md) единственными допустимыми типами являются Glu \_ «Карта1» \_ Trim \_ 2 и Glu \_ «Карта1» \_ Trim \_ 3.</span><span class="sxs-lookup"><span data-stu-id="89f24-126">Between a [**gluBeginTrim**](glubegintrim.md)/[**gluEndTrim**](gluendtrim.md) pair, the only valid types are GLU\_MAP1\_TRIM\_2 and GLU\_MAP1\_TRIM\_3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89f24-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89f24-127">Return value</span></span>

<span data-ttu-id="89f24-128">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="89f24-128">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="89f24-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89f24-129">Remarks</span></span>

<span data-ttu-id="89f24-130">Когда **глунурбскурве** появляется между парой **глубегинкурве** / **глуендкурве** , она описывает кривую для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="89f24-130">When **gluNurbsCurve** appears between a **gluBeginCurve**/**gluEndCurve** pair, it describes a curve to be rendered.</span></span> <span data-ttu-id="89f24-131">Вы связываете позиционированные, текстурные и цветовые координаты, предоставляя каждый как отдельный **глунурбскурве** между парой **глубегинкурве** / **глуендкурве** .</span><span class="sxs-lookup"><span data-stu-id="89f24-131">You associate positional, texture, and color coordinates by presenting each as a separate **gluNurbsCurve** between a **gluBeginCurve**/**gluEndCurve** pair.</span></span> <span data-ttu-id="89f24-132">Не делайте более одного вызова **глунурбскурве** для данных о цвете, положении и текстуре в одной паре **глубегинкурве** / **глуендкурве** .</span><span class="sxs-lookup"><span data-stu-id="89f24-132">Do not make more than one call to **gluNurbsCurve** for color, position, and texture data within a single **gluBeginCurve**/**gluEndCurve** pair.</span></span> <span data-ttu-id="89f24-133">Сделайте ровно один вызов, чтобы описать расположение кривой ( *тип* GL \_ «Карта1» \_ вершиной \_ 3 или GL \_ «Карта1» \_ Vertex \_ 4).</span><span class="sxs-lookup"><span data-stu-id="89f24-133">Make exactly one call to describe the position of the curve (a *type* of GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4).</span></span>

<span data-ttu-id="89f24-134">Когда **глунурбскурве** появляется между парой [**глубегинтрим**](glubegintrim.md) / [**глуендтрим**](gluendtrim.md) , она описывает кривую обрезки на поверхности нурбс.</span><span class="sxs-lookup"><span data-stu-id="89f24-134">When **gluNurbsCurve** appears between a [**gluBeginTrim**](glubegintrim.md)/[**gluEndTrim**](gluendtrim.md) pair, it describes a trimming curve on a NURBS surface.</span></span> <span data-ttu-id="89f24-135">Если *тип* — Glu \_ «Карта1» \_ Trim \_ 2, он описывает кривую в двухмерном пространстве параметров (*u* и *v*).</span><span class="sxs-lookup"><span data-stu-id="89f24-135">If *type* is GLU\_MAP1\_TRIM\_2, it describes a curve in two-dimensional (*u* and *v*) parameter space.</span></span> <span data-ttu-id="89f24-136">Если это GLU \_ «Карта1» \_ Trim \_ 3, он описывает кривую в двухмерном одномерном пространстве параметров (*u*, *v* и *w*).</span><span class="sxs-lookup"><span data-stu-id="89f24-136">If it is GLU\_MAP1\_TRIM\_3, it describes a curve in two-dimensional homogeneous (*u*, *v*, and *w*) parameter space.</span></span> <span data-ttu-id="89f24-137">Дополнительные сведения об усечении кривых см. в статье **глубегинтрим**.</span><span class="sxs-lookup"><span data-stu-id="89f24-137">For more discussion about trimming curves, see **gluBeginTrim**.</span></span>

## <a name="examples"></a><span data-ttu-id="89f24-138">Примеры</span><span class="sxs-lookup"><span data-stu-id="89f24-138">Examples</span></span>

<span data-ttu-id="89f24-139">Следующие функции визуализируются с помощью текстурной НУРБС кривой с нормальными функциями:</span><span class="sxs-lookup"><span data-stu-id="89f24-139">The following functions render a textured NURBS curve with normals:</span></span>

``` syntax
gluBeginCurve(nobj); 
    gluNurbsCurve(nobj, ..., GL_MAP1_TEXTURE_COORD_2); 
    gluNurbsCurve(nobj, ..., GL_MAP1_NORMAL); 
    gluNurbsCurve(nobj, ..., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj); 
```

## <a name="requirements"></a><span data-ttu-id="89f24-140">Требования</span><span class="sxs-lookup"><span data-stu-id="89f24-140">Requirements</span></span>



| <span data-ttu-id="89f24-141">Требование</span><span class="sxs-lookup"><span data-stu-id="89f24-141">Requirement</span></span> | <span data-ttu-id="89f24-142">Значение</span><span class="sxs-lookup"><span data-stu-id="89f24-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="89f24-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89f24-143">Minimum supported client</span></span><br/> | <span data-ttu-id="89f24-144">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="89f24-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="89f24-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89f24-145">Minimum supported server</span></span><br/> | <span data-ttu-id="89f24-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="89f24-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="89f24-147">Заголовок</span><span class="sxs-lookup"><span data-stu-id="89f24-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="89f24-148"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="89f24-148"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="89f24-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="89f24-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="89f24-150"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89f24-150"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="89f24-151">DLL</span><span class="sxs-lookup"><span data-stu-id="89f24-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89f24-152"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89f24-152"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89f24-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89f24-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89f24-154">**глубегинкурве**</span><span class="sxs-lookup"><span data-stu-id="89f24-154">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="89f24-155">**глубегинтрим**</span><span class="sxs-lookup"><span data-stu-id="89f24-155">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="89f24-156">**глуендкурве**</span><span class="sxs-lookup"><span data-stu-id="89f24-156">**gluEndCurve**</span></span>](gluendcurve.md)
</dt> <dt>

[<span data-ttu-id="89f24-157">**глуендтрим**</span><span class="sxs-lookup"><span data-stu-id="89f24-157">**gluEndTrim**</span></span>](gluendtrim.md)
</dt> <dt>

[<span data-ttu-id="89f24-158">**глуневнурбсрендерер**</span><span class="sxs-lookup"><span data-stu-id="89f24-158">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="89f24-159">**глупвлкурве**</span><span class="sxs-lookup"><span data-stu-id="89f24-159">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





