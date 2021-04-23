---
title: Функция Глунурбссурфаце (GLU. h)
description: Функция Глунурбссурфаце определяет форму неравномерного рационального постороннего прямоугольника B-сплайна (НУРБС).
ms.assetid: ee86376c-26ba-49a9-b0b0-4ca936b6614b
keywords:
- Функция Глунурбссурфаце OpenGL
topic_type:
- apiref
api_name:
- gluNurbsSurface
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c784741eded406a49bba90f67544a406ab024a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988169"
---
# <a name="glunurbssurface-function"></a><span data-ttu-id="4fe7b-104">Функция Глунурбссурфаце</span><span class="sxs-lookup"><span data-stu-id="4fe7b-104">gluNurbsSurface function</span></span>

<span data-ttu-id="4fe7b-105">Функция **глунурбссурфаце** определяет форму неравномерного рационального постороннего прямоугольника B-сплайна ([нурбс](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="4fe7b-105">The **gluNurbsSurface** function defines the shape of a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fe7b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fe7b-106">Syntax</span></span>


```C++
void WINAPI gluNurbsSurface(
   GLUnurbs *nobj,
   GLint    sknot_count,
   float    *sknot,
   GLint    tknot_count,
   GLfloat  *tknot,
   GLint    s_stride,
   GLint    t_stride,
   GLfloat  *ctlarray,
   GLint    sorder,
   GLint    torder,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="4fe7b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4fe7b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fe7b-108">*нобж*</span><span class="sxs-lookup"><span data-stu-id="4fe7b-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="4fe7b-109">Объект НУРБС (созданный с помощью [**глуневнурбсрендерер**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="4fe7b-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="4fe7b-110">*\_число скнот*</span><span class="sxs-lookup"><span data-stu-id="4fe7b-110">*sknot\_count*</span></span> 
</dt> <dd>

<span data-ttu-id="4fe7b-111">Число Кнотс в «параметрической» направлении *u* .</span><span class="sxs-lookup"><span data-stu-id="4fe7b-111">The number of knots in the parametric *u* direction.</span></span>

</dd> <dt>

<span data-ttu-id="4fe7b-112">*скнот*</span><span class="sxs-lookup"><span data-stu-id="4fe7b-112">*sknot*</span></span> 
</dt> <dd>

<span data-ttu-id="4fe7b-113">Массив *скнот \_ Count* нондекреасинг релевантной значений в непараметрической направлении *u* .</span><span class="sxs-lookup"><span data-stu-id="4fe7b-113">An array of *sknot\_count* nondecreasing knot values in the parametric *u* direction.</span></span>

</dd> <dt>

<span data-ttu-id="4fe7b-114">*\_число ткнот*</span><span class="sxs-lookup"><span data-stu-id="4fe7b-114">*tknot\_count*</span></span> 
</dt> <dd>

<span data-ttu-id="4fe7b-115">Число Кнотс в направлении параметрической *v* .</span><span class="sxs-lookup"><span data-stu-id="4fe7b-115">The number of knots in the parametric *v* direction.</span></span>

</dd> <dt>

<span data-ttu-id="4fe7b-116">*ткнот*</span><span class="sxs-lookup"><span data-stu-id="4fe7b-116">*tknot*</span></span> 
</dt> <dd>

<span data-ttu-id="4fe7b-117">Массив *ткнот \_ Count* нондекреасинг релевантной значений в направлении параметрической *v* .</span><span class="sxs-lookup"><span data-stu-id="4fe7b-117">An array of *tknot\_count* nondecreasing knot values in the parametric *v* direction.</span></span>

</dd> <dt>

<span data-ttu-id="4fe7b-118">*\_Шаг с шагом*</span><span class="sxs-lookup"><span data-stu-id="4fe7b-118">*s\_stride*</span></span> 
</dt> <dd>

<span data-ttu-id="4fe7b-119">Смещение (в виде числа отдельных значений преЦисионфлоатинг точек) между последовательными контрольными точками в параметре параметрической *u* в *ктларрай*.</span><span class="sxs-lookup"><span data-stu-id="4fe7b-119">The offset (as a number of single precisionfloating-point values) between successive control points in the parametric *u* direction in *ctlarray*.</span></span>

</dd> <dt>

<span data-ttu-id="4fe7b-120">*t \_ шаг*</span><span class="sxs-lookup"><span data-stu-id="4fe7b-120">*t\_stride*</span></span> 
</dt> <dd>

<span data-ttu-id="4fe7b-121">Смещение (в одиночных преЦисионфлоатинг значениях) между последовательными контрольными точками в направлении параметрической *v* в *ктларрай*.</span><span class="sxs-lookup"><span data-stu-id="4fe7b-121">The offset (in single precisionfloating-point values) between successive control points in the parametric *v* direction in *ctlarray*.</span></span>

</dd> <dt>

<span data-ttu-id="4fe7b-122">*ктларрай*</span><span class="sxs-lookup"><span data-stu-id="4fe7b-122">*ctlarray*</span></span> 
</dt> <dd>

<span data-ttu-id="4fe7b-123">Массив, содержащий контрольные точки для поверхности НУРБС.</span><span class="sxs-lookup"><span data-stu-id="4fe7b-123">An array containing control points for the NURBS surface.</span></span> <span data-ttu-id="4fe7b-124">Смещение между последовательными контрольными точками в направлениях *"параметрической"* и " *v* " определяется с помощью *s \_ stride* и *t \_ stride*.</span><span class="sxs-lookup"><span data-stu-id="4fe7b-124">The offsets between successive control points in the parametric *u* and *v* directions are given by *s\_stride* and *t\_stride*.</span></span>

</dd> <dt>

<span data-ttu-id="4fe7b-125">*сордер*</span><span class="sxs-lookup"><span data-stu-id="4fe7b-125">*sorder*</span></span> 
</dt> <dd>

<span data-ttu-id="4fe7b-126">Порядок поверхности НУРБС в направлении параметрической *u* .</span><span class="sxs-lookup"><span data-stu-id="4fe7b-126">The order of the NURBS surface in the parametric *u* direction.</span></span> <span data-ttu-id="4fe7b-127">Этот порядок больше, чем в степени, поэтому поверхность, которая является кубическим в *u* , имеет порядковый номер *u* 4.</span><span class="sxs-lookup"><span data-stu-id="4fe7b-127">The order is one more than the degree, hence a surface that is cubic in *u* has a *u* order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="4fe7b-128">*тордер*</span><span class="sxs-lookup"><span data-stu-id="4fe7b-128">*torder*</span></span> 
</dt> <dd>

<span data-ttu-id="4fe7b-129">Порядок поверхности НУРБС в направлении параметрической *v* .</span><span class="sxs-lookup"><span data-stu-id="4fe7b-129">The order of the NURBS surface in the parametric *v* direction.</span></span> <span data-ttu-id="4fe7b-130">Этот порядок больше, чем в степени, поэтому у поверхности, которая является кубическим  в версии v *, имеется порядковый* номер 4.</span><span class="sxs-lookup"><span data-stu-id="4fe7b-130">The order is one more than the degree, hence a surface that is cubic in *v* has a *v* order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="4fe7b-131">*type*</span><span class="sxs-lookup"><span data-stu-id="4fe7b-131">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="4fe7b-132">Тип поверхности.</span><span class="sxs-lookup"><span data-stu-id="4fe7b-132">The type of the surface.</span></span> <span data-ttu-id="4fe7b-133">Параметр *типа* может быть любым из допустимых двух типов оценщиков (например, GL \_ MAP2 \_ Vertex \_ 3 или GL \_ MAP2 \_ Color \_ 4).</span><span class="sxs-lookup"><span data-stu-id="4fe7b-133">The *type* parameter can be any of the valid two-dimensional evaluator types (such as GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_COLOR\_4).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fe7b-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4fe7b-134">Return value</span></span>

<span data-ttu-id="4fe7b-135">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4fe7b-135">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fe7b-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4fe7b-136">Remarks</span></span>

<span data-ttu-id="4fe7b-137">Используйте **глунурбссурфаце** в определении поверхности нурбс, чтобы описать форму поверхности нурбс (перед обрезками).</span><span class="sxs-lookup"><span data-stu-id="4fe7b-137">Use **gluNurbsSurface** within a NURBS surface definition to describe the shape of a NURBS surface (before any trimming).</span></span> <span data-ttu-id="4fe7b-138">Чтобы отметить начало определения поверхности НУРБС, используйте функцию [**глубегинсурфаце**](glubeginsurface.md) .</span><span class="sxs-lookup"><span data-stu-id="4fe7b-138">To mark the beginning of a NURBS surface definition, use the [**gluBeginSurface**](glubeginsurface.md) function.</span></span> <span data-ttu-id="4fe7b-139">Чтобы отметить конец определения поверхности НУРБС, используйте функцию [**глуендсурфаце**](gluendsurface.md) .</span><span class="sxs-lookup"><span data-stu-id="4fe7b-139">To mark the end of a NURBS surface definition, use the [**gluEndSurface**](gluendsurface.md) function.</span></span> <span data-ttu-id="4fe7b-140">Вызовите **глунурбссурфаце** только в определении поверхности нурбс.</span><span class="sxs-lookup"><span data-stu-id="4fe7b-140">Call **gluNurbsSurface** within a NURBS surface definition only.</span></span>

<span data-ttu-id="4fe7b-141">Вы связываете позиционированные, текстурные и цветные координаты с поверхностью, предоставляя каждую из них как отдельную **глунурбссурфаце** между парой **глубегинсурфаце** / **глуендсурфаце** .</span><span class="sxs-lookup"><span data-stu-id="4fe7b-141">You associate positional, texture, and color coordinates with a surface by presenting each as a separate **gluNurbsSurface** between a **gluBeginSurface**/**gluEndSurface** pair.</span></span> <span data-ttu-id="4fe7b-142">В одной паре **глубегинсурфаце** / **глуендсурфаце** можно установить только один вызов **глунурбссурфаце** для данных о цвете, положении и текстуре.</span><span class="sxs-lookup"><span data-stu-id="4fe7b-142">Within a single **gluBeginSurface**/**gluEndSurface** pair, you can make only one call to **gluNurbsSurface** for color, position, and texture data.</span></span> <span data-ttu-id="4fe7b-143">Сделайте ровно один вызов, чтобы описать расположение поверхности ( *тип* GL \_ MAP2 \_ Vertex \_ 3 или GL \_ MAP2 \_ Vertex \_ 4).</span><span class="sxs-lookup"><span data-stu-id="4fe7b-143">Make exactly one call to describe the position of the surface (a *type* of GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4).</span></span>

<span data-ttu-id="4fe7b-144">Можно обрезать НУРБС поверхность с помощью функций [**глунурбскурве**](glunurbscurve.md) и [**глупвлкурве**](glupwlcurve.md) между вызовами [**глубегинтрим**](glubegintrim.md) и [**глуендтрим**](gluendtrim.md).</span><span class="sxs-lookup"><span data-stu-id="4fe7b-144">You can trim a NURBS surface by using the [**gluNurbsCurve**](glunurbscurve.md) and [**gluPwlCurve**](glupwlcurve.md) functions between calls to [**gluBeginTrim**](glubegintrim.md) and [**gluEndTrim**](gluendtrim.md).</span></span>

<span data-ttu-id="4fe7b-145">**Глунурбссурфаце** с *скнот \_ Count* Кнотс в направлении *u* и *ткнот \_ Count* Кнотс в версии *v* с Orders *сордер* и *тордер* должны иметь контрольные точки (*скнот \_ Count*  - *сордер*) мултипиед by (*ткнот \_ Count*  - *тордер*).</span><span class="sxs-lookup"><span data-stu-id="4fe7b-145">A **gluNurbsSurface** with *sknot\_count* knots in the *u* direction and *tknot\_count* knots in the *v* direction with orders *sorder* and *torder* must have (*sknot\_count* -*sorder*) multipied by (*tknot\_count* -*torder*) control points.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fe7b-146">Требования</span><span class="sxs-lookup"><span data-stu-id="4fe7b-146">Requirements</span></span>



| <span data-ttu-id="4fe7b-147">Требование</span><span class="sxs-lookup"><span data-stu-id="4fe7b-147">Requirement</span></span> | <span data-ttu-id="4fe7b-148">Значение</span><span class="sxs-lookup"><span data-stu-id="4fe7b-148">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4fe7b-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fe7b-149">Minimum supported client</span></span><br/> | <span data-ttu-id="4fe7b-150">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4fe7b-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4fe7b-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fe7b-151">Minimum supported server</span></span><br/> | <span data-ttu-id="4fe7b-152">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4fe7b-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4fe7b-153">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4fe7b-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fe7b-154"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fe7b-154"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="4fe7b-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4fe7b-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="4fe7b-156"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fe7b-156"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4fe7b-157">DLL</span><span class="sxs-lookup"><span data-stu-id="4fe7b-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fe7b-158"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fe7b-158"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fe7b-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4fe7b-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fe7b-160">**глубегинсурфаце**</span><span class="sxs-lookup"><span data-stu-id="4fe7b-160">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="4fe7b-161">**глубегинтрим**</span><span class="sxs-lookup"><span data-stu-id="4fe7b-161">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="4fe7b-162">**глуендсурфаце**</span><span class="sxs-lookup"><span data-stu-id="4fe7b-162">**gluEndSurface**</span></span>](gluendsurface.md)
</dt> <dt>

[<span data-ttu-id="4fe7b-163">**глуендтрим**</span><span class="sxs-lookup"><span data-stu-id="4fe7b-163">**gluEndTrim**</span></span>](gluendtrim.md)
</dt> <dt>

[<span data-ttu-id="4fe7b-164">**глуневнурбсрендерер**</span><span class="sxs-lookup"><span data-stu-id="4fe7b-164">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="4fe7b-165">**глунурбскурве**</span><span class="sxs-lookup"><span data-stu-id="4fe7b-165">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="4fe7b-166">**глупвлкурве**</span><span class="sxs-lookup"><span data-stu-id="4fe7b-166">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





