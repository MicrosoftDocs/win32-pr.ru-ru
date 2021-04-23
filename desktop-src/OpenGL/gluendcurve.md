---
title: Функция Глуендкурве (GLU. h)
description: Функции Глубегинкурве и Глуендкурве разделяют неоднородное рациональное определение кривой B-сплайна (НУРБС). | Функция Глуендкурве (GLU. h)
ms.assetid: b00ec687-6127-4585-b7b7-06e8dca78cfc
keywords:
- Функция Глуендкурве OpenGL
topic_type:
- apiref
api_name:
- gluEndCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49f6c0c08bf31135ca82e87d2093ef3b57197955
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674633"
---
# <a name="gluendcurve-function"></a><span data-ttu-id="9e3e1-105">Функция Глуендкурве</span><span class="sxs-lookup"><span data-stu-id="9e3e1-105">gluEndCurve function</span></span>

<span data-ttu-id="9e3e1-106">Функции [**глубегинкурве**](glubegincurve.md) и **глуендкурве** разделяют неоднородное рациональное определение кривой B-сплайна ([нурбс](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="9e3e1-106">The [**gluBeginCurve**](glubegincurve.md) and **gluEndCurve** functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) curve definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e3e1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e3e1-107">Syntax</span></span>


```C++
void WINAPI gluEndCurve(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="9e3e1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e3e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e3e1-109">*нобж*</span><span class="sxs-lookup"><span data-stu-id="9e3e1-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="9e3e1-110">Объект НУРБС (созданный с помощью [**глуневнурбсрендерер**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="9e3e1-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e3e1-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e3e1-111">Return value</span></span>

<span data-ttu-id="9e3e1-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9e3e1-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e3e1-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e3e1-113">Remarks</span></span>

<span data-ttu-id="9e3e1-114">Используйте [**глубегинкурве**](glubegincurve.md) , чтобы пометить начало определения кривой нурбс.</span><span class="sxs-lookup"><span data-stu-id="9e3e1-114">Use [**gluBeginCurve**](glubegincurve.md) to mark the beginning of a NURBS curve definition.</span></span> <span data-ttu-id="9e3e1-115">После вызова **глубегинкурве** выполните один или несколько вызовов [**глунурбскурве**](glunurbscurve.md) , чтобы определить атрибуты кривой.</span><span class="sxs-lookup"><span data-stu-id="9e3e1-115">After calling **gluBeginCurve**, make one or more calls to [**gluNurbsCurve**](glunurbscurve.md) to define the attributes of the curve.</span></span> <span data-ttu-id="9e3e1-116">Ровно один из вызовов **глунурбскурве** должен иметь тип кривой GL \_ «Карта1» \_ Vertex \_ 3 или GL \_ «Карта1» \_ вершиной \_ 4.</span><span class="sxs-lookup"><span data-stu-id="9e3e1-116">Exactly one of the calls to **gluNurbsCurve** must have a curve type of GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4.</span></span> <span data-ttu-id="9e3e1-117">Чтобы отметить конец определения кривой НУРБС, вызовите **глуендкурве**.</span><span class="sxs-lookup"><span data-stu-id="9e3e1-117">To mark the end of the NURBS curve definition, call **gluEndCurve**.</span></span>

<span data-ttu-id="9e3e1-118">Оценщики OpenGL используются для отрисовки кривой НУРБС в виде ряда сегментов линии.</span><span class="sxs-lookup"><span data-stu-id="9e3e1-118">OpenGL evaluators are used to render the NURBS curve as a series of line segments.</span></span> <span data-ttu-id="9e3e1-119">Состояние оценщика сохраняется во время подготовки к просмотру с помощью [**глпушаттриб**](glpushattrib.md) ( \_ бит оценки GL \_ ) и [**глпопаттриб**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="9e3e1-119">Evaluator state is preserved during rendering with [**glPushAttrib**](glpushattrib.md) (GL\_EVAL\_BIT ) and [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="9e3e1-120">Сведения о том, какое состояние эти вызовы сохраняют, см. в разделе **глпушаттриб**.</span><span class="sxs-lookup"><span data-stu-id="9e3e1-120">For information on exactly what state these calls preserve, see **glPushAttrib**.</span></span>

## <a name="examples"></a><span data-ttu-id="9e3e1-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="9e3e1-121">Examples</span></span>

<span data-ttu-id="9e3e1-122">Следующие функции визуализируются с помощью текстурной НУРБС кривой с нормальными. координаты текстуры и нормали также указываются в виде кривых НУРБС:</span><span class="sxs-lookup"><span data-stu-id="9e3e1-122">The following functions render a textured NURBS curve with normals; texture coordinates and normals are also specified as NURBS curves:</span></span>

``` syntax
gluBeginCurve(nobj); 
gluNurbsCurve(nobj, . . ., GL_MAP1_TEXTURE_COORD_2); 
gluNurbsCurve(nobj, . . ., GL_MAP1_NORMAL); 
gluNurbsCurve(nobj, . . ., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj);
```

## <a name="requirements"></a><span data-ttu-id="9e3e1-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9e3e1-123">Requirements</span></span>



| <span data-ttu-id="9e3e1-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9e3e1-124">Requirement</span></span> | <span data-ttu-id="9e3e1-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9e3e1-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9e3e1-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e3e1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9e3e1-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9e3e1-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9e3e1-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e3e1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9e3e1-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9e3e1-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9e3e1-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9e3e1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e3e1-131"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e3e1-131"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9e3e1-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9e3e1-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="9e3e1-133"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e3e1-133"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9e3e1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9e3e1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e3e1-135"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e3e1-135"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e3e1-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e3e1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e3e1-137">**глпушаттриб**</span><span class="sxs-lookup"><span data-stu-id="9e3e1-137">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="9e3e1-138">**глубегинсурфаце**</span><span class="sxs-lookup"><span data-stu-id="9e3e1-138">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="9e3e1-139">**глубегинтрим**</span><span class="sxs-lookup"><span data-stu-id="9e3e1-139">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="9e3e1-140">**глуневнурбсрендерер**</span><span class="sxs-lookup"><span data-stu-id="9e3e1-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="9e3e1-141">**глунурбскурве**</span><span class="sxs-lookup"><span data-stu-id="9e3e1-141">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> </dl>

 

 





