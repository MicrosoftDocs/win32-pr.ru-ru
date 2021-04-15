---
title: Функция Глупвлкурве (GLU. h)
description: Функция Глупвлкурве описывает кусочно-линейную кривую неоднородной кривой B-сплайна (НУРБС).
ms.assetid: 3d08e7e8-dfdf-447c-9795-bd73299412b5
keywords:
- Функция Глупвлкурве OpenGL
topic_type:
- apiref
api_name:
- gluPwlCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15c532659811c7e499369e7798c4b1ceaf842bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661947"
---
# <a name="glupwlcurve-function"></a><span data-ttu-id="c7297-104">Функция Глупвлкурве</span><span class="sxs-lookup"><span data-stu-id="c7297-104">gluPwlCurve function</span></span>

<span data-ttu-id="c7297-105">Функция **глупвлкурве** описывает кусочно-линейную кривую неоднородной кривой B-сплайна ([нурбс](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="c7297-105">The **gluPwlCurve** function describes a piecewise linear Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) trimming curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7297-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7297-106">Syntax</span></span>


```C++
void WINAPI gluPwlCurve(
   GLUnurbs *nobj,
   GLint    count,
   GLfloat  *array,
   GLint    stride,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="c7297-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7297-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7297-108">*нобж*</span><span class="sxs-lookup"><span data-stu-id="c7297-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="c7297-109">Объект НУРБС (созданный с помощью [**глуневнурбсрендерер**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="c7297-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="c7297-110">*count*</span><span class="sxs-lookup"><span data-stu-id="c7297-110">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="c7297-111">Число точек на кривой.</span><span class="sxs-lookup"><span data-stu-id="c7297-111">The number of points on the curve.</span></span>

</dd> <dt>

<span data-ttu-id="c7297-112">*array*</span><span class="sxs-lookup"><span data-stu-id="c7297-112">*array*</span></span> 
</dt> <dd>

<span data-ttu-id="c7297-113">Массив, содержащий точки кривой.</span><span class="sxs-lookup"><span data-stu-id="c7297-113">An array containing the curve points.</span></span>

</dd> <dt>

<span data-ttu-id="c7297-114">*шага*</span><span class="sxs-lookup"><span data-stu-id="c7297-114">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="c7297-115">Смещение (число значений с плавающей запятой одиночной точности) между точками кривой.</span><span class="sxs-lookup"><span data-stu-id="c7297-115">The offset (a number of single-precision floating-point values) between points on the curve.</span></span>

</dd> <dt>

<span data-ttu-id="c7297-116">*type*</span><span class="sxs-lookup"><span data-stu-id="c7297-116">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="c7297-117">Тип кривой.</span><span class="sxs-lookup"><span data-stu-id="c7297-117">The type of curve.</span></span> <span data-ttu-id="c7297-118">Должен быть либо GLU \_ «Карта1» \_ Trim \_ 2, либо \_ Glu «Карта1» \_ Trim \_ 3.</span><span class="sxs-lookup"><span data-stu-id="c7297-118">Must be either GLU\_MAP1\_TRIM\_2 or GLU\_MAP1\_TRIM\_3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7297-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7297-119">Return value</span></span>

<span data-ttu-id="c7297-120">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c7297-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7297-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7297-121">Remarks</span></span>

<span data-ttu-id="c7297-122">Функция **глупвлкурве** описывает кривую линейной обрезки кусочно-для поверхности нурбс.</span><span class="sxs-lookup"><span data-stu-id="c7297-122">The **gluPwlCurve** function describes a piecewise linear trimming curve for a NURBS surface.</span></span> <span data-ttu-id="c7297-123">Линейная кривая кусочно-состоит из списка координат точек в области параметров для усечения поверхности НУРБС.</span><span class="sxs-lookup"><span data-stu-id="c7297-123">A piecewise linear curve consists of a list of coordinates of points in the parameter space for the NURBS surface to be trimmed.</span></span> <span data-ttu-id="c7297-124">Эти точки связаны с сегментами линии для формирования кривой.</span><span class="sxs-lookup"><span data-stu-id="c7297-124">These points are connected with line segments to form a curve.</span></span> <span data-ttu-id="c7297-125">Если кривая приближена к реальной кривой, точки должны быть близки, чтобы результирующий контур был изогнут в разрешении, используемом в приложении.</span><span class="sxs-lookup"><span data-stu-id="c7297-125">If the curve is an approximation to a real curve, the points should be close enough that the resulting path appears curved at the resolution used in the application.</span></span>

<span data-ttu-id="c7297-126">Если *тип* — Glu \_ «Карта1» \_ Trim \_ 2, он описывает кривую в двухмерном пространстве параметров (*u* и *v*).</span><span class="sxs-lookup"><span data-stu-id="c7297-126">If *type* is GLU\_MAP1\_TRIM\_2, it describes a curve in two-dimensional (*u* and *v*) parameter space.</span></span> <span data-ttu-id="c7297-127">Если это GLU \_ «Карта1» \_ Trim \_ 3, то он описывает кривую в двухмерном одномерном пространстве параметров (*u*, *v* и *w*).</span><span class="sxs-lookup"><span data-stu-id="c7297-127">If it is GLU\_MAP1\_TRIM\_3, then it describes a curve in two-dimensional homogeneous (*u*, *v*, and *w*) parameter space.</span></span> <span data-ttu-id="c7297-128">Дополнительные сведения об усечении кривых см. в разделе [**глубегинтрим**](glubegintrim.md).</span><span class="sxs-lookup"><span data-stu-id="c7297-128">For more information about trimming curves, see [**gluBeginTrim**](glubegintrim.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7297-129">Требования</span><span class="sxs-lookup"><span data-stu-id="c7297-129">Requirements</span></span>



| <span data-ttu-id="c7297-130">Требование</span><span class="sxs-lookup"><span data-stu-id="c7297-130">Requirement</span></span> | <span data-ttu-id="c7297-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c7297-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c7297-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7297-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c7297-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c7297-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c7297-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7297-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c7297-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c7297-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c7297-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c7297-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7297-137"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7297-137"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="c7297-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c7297-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7297-139"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7297-139"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c7297-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c7297-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7297-141"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7297-141"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7297-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7297-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7297-143">**глубегинкурве**</span><span class="sxs-lookup"><span data-stu-id="c7297-143">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="c7297-144">**глубегинтрим**</span><span class="sxs-lookup"><span data-stu-id="c7297-144">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="c7297-145">**глуневнурбсрендерер**</span><span class="sxs-lookup"><span data-stu-id="c7297-145">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="c7297-146">**глунурбскурве**</span><span class="sxs-lookup"><span data-stu-id="c7297-146">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> </dl>

 

 





