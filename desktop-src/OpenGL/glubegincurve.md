---
title: Функция Глубегинкурве (GLU. h)
description: Функции Глубегинкурве и Глуендкурве разделяют неоднородное рациональное определение кривой B-сплайна (НУРБС). | Функция Глубегинкурве (GLU. h)
ms.assetid: f7f2e765-1a07-4faa-940c-9cb957dd54d4
keywords:
- Функция Глубегинкурве OpenGL
topic_type:
- apiref
api_name:
- gluBeginCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4e17bd88cfcb49801450ead865c437843d179b5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684974"
---
# <a name="glubegincurve-function"></a><span data-ttu-id="d5f59-105">Функция Глубегинкурве</span><span class="sxs-lookup"><span data-stu-id="d5f59-105">gluBeginCurve function</span></span>

<span data-ttu-id="d5f59-106">Функции **глубегинкурве** и [**глуендкурве**](gluendcurve.md) разделяют неоднородное рациональное определение кривой B-сплайна ([нурбс](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="d5f59-106">The **gluBeginCurve** and [**gluEndCurve**](gluendcurve.md) functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) curve definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5f59-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5f59-107">Syntax</span></span>


```C++
void WINAPI gluBeginCurve(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="d5f59-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5f59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5f59-109">*нобж*</span><span class="sxs-lookup"><span data-stu-id="d5f59-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="d5f59-110">Объект НУРБС (созданный с помощью [**глуневнурбсрендерер**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="d5f59-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5f59-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5f59-111">Return value</span></span>

<span data-ttu-id="d5f59-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d5f59-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5f59-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5f59-113">Remarks</span></span>

<span data-ttu-id="d5f59-114">Используйте **глубегинкурве** , чтобы пометить начало определения кривой нурбс.</span><span class="sxs-lookup"><span data-stu-id="d5f59-114">Use **gluBeginCurve** to mark the beginning of a NURBS curve definition.</span></span> <span data-ttu-id="d5f59-115">После вызова **глубегинкурве** выполните один или несколько вызовов [**глунурбскурве**](glunurbscurve.md) , чтобы определить атрибуты кривой.</span><span class="sxs-lookup"><span data-stu-id="d5f59-115">After calling **gluBeginCurve**, make one or more calls to [**gluNurbsCurve**](glunurbscurve.md) to define the attributes of the curve.</span></span> <span data-ttu-id="d5f59-116">Ровно один из вызовов **глунурбскурве** должен иметь тип кривой GL \_ «Карта1» \_ Vertex \_ 3 или GL \_ «Карта1» \_ вершиной \_ 4.</span><span class="sxs-lookup"><span data-stu-id="d5f59-116">Exactly one of the calls to **gluNurbsCurve** must have a curve type of GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4.</span></span> <span data-ttu-id="d5f59-117">Чтобы отметить конец определения кривой НУРБС, вызовите [**глуендкурве**](gluendcurve.md).</span><span class="sxs-lookup"><span data-stu-id="d5f59-117">To mark the end of the NURBS curve definition, call [**gluEndCurve**](gluendcurve.md).</span></span>

<span data-ttu-id="d5f59-118">Оценщики OpenGL используются для отрисовки кривой НУРБС в виде ряда сегментов линии.</span><span class="sxs-lookup"><span data-stu-id="d5f59-118">OpenGL evaluators are used to render the NURBS curve as a series of line segments.</span></span> <span data-ttu-id="d5f59-119">Состояние оценщика сохраняется во время подготовки к просмотру с помощью [**глпушаттриб**](glpushattrib.md) ( \_ бит оценки GL \_ ) и [**глпопаттриб**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="d5f59-119">Evaluator state is preserved during rendering with [**glPushAttrib**](glpushattrib.md) (GL\_EVAL\_BIT) and [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="d5f59-120">Сведения о том, какое состояние эти вызовы сохраняют, см. в разделе **глпушаттриб**.</span><span class="sxs-lookup"><span data-stu-id="d5f59-120">For information on exactly what state these calls preserve, see **glPushAttrib**.</span></span>

## <a name="examples"></a><span data-ttu-id="d5f59-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="d5f59-121">Examples</span></span>

<span data-ttu-id="d5f59-122">Следующие функции визуализируются с помощью текстурной НУРБС кривой с нормальными. координаты текстуры и нормали также указываются в виде кривых НУРБС:</span><span class="sxs-lookup"><span data-stu-id="d5f59-122">The following functions render a textured NURBS curve with normals; texture coordinates and normals are also specified as NURBS curves:</span></span>

``` syntax
gluBeginCurve(nobj); 
gluNurbsCurve(nobj, . . ., GL_MAP1_TEXTURE_COORD_2); 
gluNurbsCurve(nobj, . . ., GL_MAP1_NORMAL); 
gluNurbsCurve(nobj, . . ., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj);
```

## <a name="requirements"></a><span data-ttu-id="d5f59-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d5f59-123">Requirements</span></span>



| <span data-ttu-id="d5f59-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d5f59-124">Requirement</span></span> | <span data-ttu-id="d5f59-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d5f59-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f59-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5f59-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d5f59-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d5f59-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d5f59-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5f59-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d5f59-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d5f59-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d5f59-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d5f59-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5f59-131"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5f59-131"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="d5f59-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d5f59-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5f59-133"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5f59-133"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d5f59-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d5f59-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5f59-135"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5f59-135"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5f59-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5f59-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5f59-137">**глпушаттриб**</span><span class="sxs-lookup"><span data-stu-id="d5f59-137">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="d5f59-138">**глубегинсурфаце**</span><span class="sxs-lookup"><span data-stu-id="d5f59-138">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="d5f59-139">**глубегинтрим**</span><span class="sxs-lookup"><span data-stu-id="d5f59-139">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="d5f59-140">**глуневнурбсрендерер**</span><span class="sxs-lookup"><span data-stu-id="d5f59-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="d5f59-141">**глунурбскурве**</span><span class="sxs-lookup"><span data-stu-id="d5f59-141">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> </dl>

 

 





