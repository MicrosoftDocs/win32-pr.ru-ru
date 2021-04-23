---
title: Функция Глубегинсурфаце (GLU. h)
description: Функции Глубегинсурфаце и Глуендсурфаце разделяют неоднородное рациональное определение поверхности B-сплайна (НУРБС). | Функция Глубегинсурфаце (GLU. h)
ms.assetid: 7189f05e-0c4d-4f82-8a82-a51fcc51b202
keywords:
- Функция Глубегинсурфаце OpenGL
topic_type:
- apiref
api_name:
- gluBeginSurface
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bbd09030290f78fac987a52cddd977a502dda06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684858"
---
# <a name="glubeginsurface-function"></a><span data-ttu-id="f28bd-105">Функция Глубегинсурфаце</span><span class="sxs-lookup"><span data-stu-id="f28bd-105">gluBeginSurface function</span></span>

<span data-ttu-id="f28bd-106">Функции **глубегинсурфаце** и [**глуендсурфаце**](gluendsurface.md) разделяют неоднородное рациональное определение поверхности B-сплайна ([нурбс](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="f28bd-106">The **gluBeginSurface** and [**gluEndSurface**](gluendsurface.md) functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) surface definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="f28bd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f28bd-107">Syntax</span></span>


```C++
void WINAPI gluBeginSurface(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="f28bd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f28bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f28bd-109">*нобж*</span><span class="sxs-lookup"><span data-stu-id="f28bd-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="f28bd-110">Объект НУРБС (созданный с помощью [**глуневнурбсрендерер**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="f28bd-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f28bd-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f28bd-111">Return value</span></span>

<span data-ttu-id="f28bd-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f28bd-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f28bd-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f28bd-113">Remarks</span></span>

<span data-ttu-id="f28bd-114">Функции **глубегинсурфаце** и **глуендсурфаце** отмечают начало и конец определений нурбс Surface, которые определяются вызовами **глунурбссурфаце**.</span><span class="sxs-lookup"><span data-stu-id="f28bd-114">The **gluBeginSurface** and **gluEndSurface** functions mark the beginning and end of NURBS surface definitions, which are defined with calls to **gluNurbsSurface**.</span></span>

1.  <span data-ttu-id="f28bd-115">Вызовите **глубегинсурфаце** , чтобы пометить начало определения поверхности нурбс.</span><span class="sxs-lookup"><span data-stu-id="f28bd-115">Call **gluBeginSurface** to mark the beginning of a NURBS surface definition.</span></span>
2.  <span data-ttu-id="f28bd-116">Выполните один или несколько вызовов **глунурбссурфаце** , чтобы определить атрибуты поверхности.</span><span class="sxs-lookup"><span data-stu-id="f28bd-116">Make one or more calls to **gluNurbsSurface** to define the attributes of the surface.</span></span>

    <span data-ttu-id="f28bd-117">Ровно один из этих вызовов **глунурбссурфаце** должен иметь тип поверхности GL \_ MAP2 \_ Vertex \_ 3 или GL \_ MAP2 \_ Vertex \_ 4.</span><span class="sxs-lookup"><span data-stu-id="f28bd-117">Exactly one of these calls to **gluNurbsSurface** must have a surface type of GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4.</span></span>

3.  <span data-ttu-id="f28bd-118">Чтобы отметить конец определения поверхности НУРБС, вызовите **глуендсурфаце**.</span><span class="sxs-lookup"><span data-stu-id="f28bd-118">To mark the end of the NURBS surface definition, call **gluEndSurface**.</span></span>

<span data-ttu-id="f28bd-119">Функции [**глубегинтрим**](glubegintrim.md), [**глупвлкурве**](glupwlcurve.md), [**глунурбскурве**](glunurbscurve.md)и [**глуендтрим**](gluendtrim.md) поддерживают усечение поверхностей нурбс.</span><span class="sxs-lookup"><span data-stu-id="f28bd-119">The [**gluBeginTrim**](glubegintrim.md), [**gluPwlCurve**](glupwlcurve.md), [**gluNurbsCurve**](glunurbscurve.md), and [**gluEndTrim**](gluendtrim.md) functions support trimming of NURBS surfaces.</span></span>

<span data-ttu-id="f28bd-120">Используйте оценщики OpenGL для отрисовки поверхности НУРБС в виде набора многоугольников.</span><span class="sxs-lookup"><span data-stu-id="f28bd-120">Use OpenGL evaluators to render the NURBS surface as a set of polygons.</span></span> <span data-ttu-id="f28bd-121">Сохраните состояние оценщика во время подготовки к просмотру с помощью [**глпушаттриб**](glpushattrib.md)( \_ бит главной оценки \_ ) и [**глпопаттриб**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="f28bd-121">Preserve the evaluator state during rendering with [**glPushAttrib**](glpushattrib.md)(GL\_EVAL\_BIT) and [**glPopAttrib**](glpopattrib.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f28bd-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="f28bd-122">Examples</span></span>

<span data-ttu-id="f28bd-123">Следующие функции отрисовывают текстурную поверхность НУРБС с нормальными, координаты текстуры и нормали также описаны как НУРБСные поверхности:</span><span class="sxs-lookup"><span data-stu-id="f28bd-123">The following functions render a textured NURBS surface with normals; the texture coordinates and normals are also described as NURBS surfaces:</span></span>

``` syntax
gluBeginSurface(nobj); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_TEXTURE_COORD_2); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_NORMAL); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_VERTEX_4); 
gluEndSurface(nobj);
```

## <a name="requirements"></a><span data-ttu-id="f28bd-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f28bd-124">Requirements</span></span>



| <span data-ttu-id="f28bd-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f28bd-125">Requirement</span></span> | <span data-ttu-id="f28bd-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f28bd-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f28bd-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f28bd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f28bd-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f28bd-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f28bd-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f28bd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f28bd-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f28bd-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f28bd-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f28bd-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f28bd-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="f28bd-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="f28bd-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f28bd-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="f28bd-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f28bd-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f28bd-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f28bd-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f28bd-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f28bd-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f28bd-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f28bd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f28bd-138">**глубегинкурве**</span><span class="sxs-lookup"><span data-stu-id="f28bd-138">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="f28bd-139">**глубегинтрим**</span><span class="sxs-lookup"><span data-stu-id="f28bd-139">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="f28bd-140">**глуневнурбсрендерер**</span><span class="sxs-lookup"><span data-stu-id="f28bd-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="f28bd-141">**глунурбскурве**</span><span class="sxs-lookup"><span data-stu-id="f28bd-141">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="f28bd-142">**глунурбссурфаце**</span><span class="sxs-lookup"><span data-stu-id="f28bd-142">**gluNurbsSurface**</span></span>](glunurbssurface.md)
</dt> <dt>

[<span data-ttu-id="f28bd-143">**глупвлкурве**</span><span class="sxs-lookup"><span data-stu-id="f28bd-143">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





