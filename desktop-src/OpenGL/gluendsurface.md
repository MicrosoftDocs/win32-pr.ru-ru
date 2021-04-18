---
title: Функция Глуендсурфаце (GLU. h)
description: Функции Глубегинсурфаце и Глуендсурфаце разделяют неоднородное рациональное определение поверхности B-сплайна (НУРБС). | Функция Глуендсурфаце (GLU. h)
ms.assetid: beaa0340-c67d-4376-bedd-7f73c5c6d742
keywords:
- Функция Глуендсурфаце OpenGL
topic_type:
- apiref
api_name:
- gluEndSurface
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54631d5c4ef752cffd989f8fa02f8cb512c67da3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547650"
---
# <a name="gluendsurface-function"></a><span data-ttu-id="a94b8-105">Функция Глуендсурфаце</span><span class="sxs-lookup"><span data-stu-id="a94b8-105">gluEndSurface function</span></span>

<span data-ttu-id="a94b8-106">Функции [**глубегинсурфаце**](glubeginsurface.md) и **глуендсурфаце** разделяют неоднородное рациональное определение поверхности B-сплайна ([нурбс](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="a94b8-106">The [**gluBeginSurface**](glubeginsurface.md) and **gluEndSurface** functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) surface definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="a94b8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a94b8-107">Syntax</span></span>


```C++
void WINAPI gluEndSurface(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="a94b8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a94b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a94b8-109">*нобж*</span><span class="sxs-lookup"><span data-stu-id="a94b8-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="a94b8-110">Объект НУРБС (созданный с помощью [**глуневнурбсрендерер**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="a94b8-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a94b8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a94b8-111">Return value</span></span>

<span data-ttu-id="a94b8-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a94b8-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a94b8-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a94b8-113">Remarks</span></span>

<span data-ttu-id="a94b8-114">Функции [**глубегинсурфаце**](glubeginsurface.md) и **глуендсурфаце** отмечают начало и конец определений нурбс Surface, которые определяются вызовами **глунурбссурфаце**.</span><span class="sxs-lookup"><span data-stu-id="a94b8-114">The [**gluBeginSurface**](glubeginsurface.md) and **gluEndSurface** functions mark the beginning and end of NURBS surface definitions, which are defined with calls to **gluNurbsSurface**.</span></span>

1.  <span data-ttu-id="a94b8-115">Вызовите **глубегинсурфаце** , чтобы пометить начало определения поверхности нурбс.</span><span class="sxs-lookup"><span data-stu-id="a94b8-115">Call **gluBeginSurface** to mark the beginning of a NURBS surface definition.</span></span>
2.  <span data-ttu-id="a94b8-116">Выполните один или несколько вызовов **глунурбссурфаце** , чтобы определить атрибуты поверхности.</span><span class="sxs-lookup"><span data-stu-id="a94b8-116">Make one or more calls to **gluNurbsSurface** to define the attributes of the surface.</span></span>

    <span data-ttu-id="a94b8-117">Ровно один из этих вызовов **глунурбссурфаце** должен иметь тип поверхности GL \_ MAP2 \_ Vertex \_ 3 или GL \_ MAP2 \_ Vertex \_ 4.</span><span class="sxs-lookup"><span data-stu-id="a94b8-117">Exactly one of these calls to **gluNurbsSurface** must have a surface type of GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4.</span></span>

3.  <span data-ttu-id="a94b8-118">Чтобы отметить конец определения поверхности НУРБС, вызовите **глуендсурфаце**.</span><span class="sxs-lookup"><span data-stu-id="a94b8-118">To mark the end of the NURBS surface definition, call **gluEndSurface**.</span></span>

<span data-ttu-id="a94b8-119">Функции [**глубегинтрим**](glubegintrim.md), [**глупвлкурве**](glupwlcurve.md), [**глунурбскурве**](glunurbscurve.md)и **глуендтрим** поддерживают усечение поверхностей нурбс.</span><span class="sxs-lookup"><span data-stu-id="a94b8-119">The [**gluBeginTrim**](glubegintrim.md), [**gluPwlCurve**](glupwlcurve.md), [**gluNurbsCurve**](glunurbscurve.md), and **gluEndTrim** functions support trimming of NURBS surfaces.</span></span>

<span data-ttu-id="a94b8-120">Используйте оценщики OpenGL для отрисовки поверхности НУРБС в виде набора многоугольников.</span><span class="sxs-lookup"><span data-stu-id="a94b8-120">Use OpenGL evaluators to render the NURBS surface as a set of polygons.</span></span> <span data-ttu-id="a94b8-121">Сохраните состояние оценщика во время подготовки к просмотру с помощью [**глпушаттриб**](glpushattrib.md) ( \_ бит главной оценки \_ ) и [**глпопаттриб**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="a94b8-121">Preserve the evaluator state during rendering with [**glPushAttrib**](glpushattrib.md) (GL\_EVAL\_BIT) and [**glPopAttrib**](glpopattrib.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a94b8-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="a94b8-122">Examples</span></span>

<span data-ttu-id="a94b8-123">Следующие функции отрисовывают текстурную поверхность НУРБС с нормальными, координаты текстуры и нормали также описаны как НУРБСные поверхности:</span><span class="sxs-lookup"><span data-stu-id="a94b8-123">The following functions render a textured NURBS surface with normals; the texture coordinates and normals are also described as NURBS surfaces:</span></span>

``` syntax
gluBeginSurface(nobj); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_TEXTURE_COORD_2); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_NORMAL); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_VERTEX_4); 
gluEndSurface(nobj);
```

## <a name="requirements"></a><span data-ttu-id="a94b8-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a94b8-124">Requirements</span></span>



| <span data-ttu-id="a94b8-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a94b8-125">Requirement</span></span> | <span data-ttu-id="a94b8-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a94b8-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a94b8-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a94b8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a94b8-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a94b8-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a94b8-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a94b8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a94b8-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a94b8-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a94b8-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a94b8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a94b8-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="a94b8-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="a94b8-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a94b8-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="a94b8-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a94b8-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a94b8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a94b8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a94b8-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a94b8-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a94b8-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a94b8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a94b8-138">**глубегинкурве**</span><span class="sxs-lookup"><span data-stu-id="a94b8-138">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="a94b8-139">**глубегинтрим**</span><span class="sxs-lookup"><span data-stu-id="a94b8-139">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="a94b8-140">**глуневнурбсрендерер**</span><span class="sxs-lookup"><span data-stu-id="a94b8-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="a94b8-141">**глунурбскурве**</span><span class="sxs-lookup"><span data-stu-id="a94b8-141">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="a94b8-142">**глунурбссурфаце**</span><span class="sxs-lookup"><span data-stu-id="a94b8-142">**gluNurbsSurface**</span></span>](glunurbssurface.md)
</dt> <dt>

[<span data-ttu-id="a94b8-143">**глупвлкурве**</span><span class="sxs-lookup"><span data-stu-id="a94b8-143">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





