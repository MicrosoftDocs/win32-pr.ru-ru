---
title: Функция Глутессбегинполигон (GLU. h)
description: Функции Глутессбегинполигон и Глутессендполигон разделяют описание многоугольника. | Функция Глутессбегинполигон (GLU. h)
ms.assetid: 3a04363a-c492-4fa5-b312-f2fa2a805782
keywords:
- Функция Глутессбегинполигон OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34fad4c620890df109449b9a222d3355041ac77f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664925"
---
# <a name="glutessbeginpolygon-function"></a><span data-ttu-id="ef4ec-105">Функция Глутессбегинполигон</span><span class="sxs-lookup"><span data-stu-id="ef4ec-105">gluTessBeginPolygon function</span></span>

<span data-ttu-id="ef4ec-106">Функции **глутессбегинполигон** и [**глутессендполигон**](glutessendpolygon.md) разделяют описание многоугольника.</span><span class="sxs-lookup"><span data-stu-id="ef4ec-106">The **gluTessBeginPolygon** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef4ec-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef4ec-107">Syntax</span></span>


```C++
void WINAPI gluTessBeginPolygon(
   GLUtesselator *tess,
   void          *polygon_data
);
```



## <a name="parameters"></a><span data-ttu-id="ef4ec-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef4ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef4ec-109">*тесс*</span><span class="sxs-lookup"><span data-stu-id="ef4ec-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="ef4ec-110">Объект тесселяции (созданный с помощью [**глуневтесс**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="ef4ec-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="ef4ec-111">*данные многоугольника \_*</span><span class="sxs-lookup"><span data-stu-id="ef4ec-111">*polygon\_data*</span></span> 
</dt> <dd>

<span data-ttu-id="ef4ec-112">Указатель на структуру данных многоугольников, определяемую программистом.</span><span class="sxs-lookup"><span data-stu-id="ef4ec-112">A pointer to a programmer-defined polygon data structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef4ec-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef4ec-113">Return value</span></span>

<span data-ttu-id="ef4ec-114">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ef4ec-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef4ec-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef4ec-115">Remarks</span></span>

<span data-ttu-id="ef4ec-116">Функции **глутессбегинполигон** и [**глутессендполигон**](glutessendpolygon.md) разделяют определение многоугольника нонконвекс.</span><span class="sxs-lookup"><span data-stu-id="ef4ec-116">The **gluTessBeginPolygon** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit the definition of a nonconvex polygon.</span></span> <span data-ttu-id="ef4ec-117">В каждой паре **глутессбегинполигон**  /  **глутессендполигон** включите один или несколько вызовов [**глутессбегинконтаур**](glutessbegincontour.md).</span><span class="sxs-lookup"><span data-stu-id="ef4ec-117">Within each **gluTessBeginPolygon** / **gluTessEndPolygon** pair, include one or more calls to [**gluTessBeginContour**](glutessbegincontour.md).</span></span> <span data-ttu-id="ef4ec-118">В каждом контуре имеется ноль или более вызовов [**глутессвертекс**](glutessvertex.md).</span><span class="sxs-lookup"><span data-stu-id="ef4ec-118">Within each contour, there are zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="ef4ec-119">Вершины задают замкнутый контур (последняя вершина каждого контура автоматически связывается с первым).</span><span class="sxs-lookup"><span data-stu-id="ef4ec-119">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span>

<span data-ttu-id="ef4ec-120">Параметр *\_ данных Polygon* — это указатель на структуру данных, определяемую программистом.</span><span class="sxs-lookup"><span data-stu-id="ef4ec-120">The *polygon\_data* parameter is a pointer to a programmer-defined data structure.</span></span> <span data-ttu-id="ef4ec-121">Если указаны соответствующие обратные вызовы (см. [*глутесскаллбакк*](glutess.md)), этот указатель возвращается функции обратного вызова или функциям, что делает его удобным способом для хранения информации на многоугольнике.</span><span class="sxs-lookup"><span data-stu-id="ef4ec-121">If the appropriate callbacks are specified (see [*gluTessCallback*](glutess.md)), this pointer is returned to the callback function or functions, making it a convenient way to store per-polygon information.</span></span>

<span data-ttu-id="ef4ec-122">При вызове [**глутессендполигон**](glutessendpolygon.md)многоугольник размещается мозаикой, а итоговые треугольники — с помощью обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="ef4ec-122">When you call [**gluTessEndPolygon**](glutessendpolygon.md), the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="ef4ec-123">Описание функций обратного вызова см. в разделе [*глутесскаллбакк*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="ef4ec-123">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ef4ec-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="ef4ec-124">Examples</span></span>

<span data-ttu-id="ef4ec-125">Ниже описывается грани четырехсторонней с треугольным отверстием:</span><span class="sxs-lookup"><span data-stu-id="ef4ec-125">The following describes a quadrilateral with a triangular hole:</span></span>

``` syntax
gluTessBeginPolygon(tobj, NULL); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v1, v1); 
    gluTessVertex(tobj, v2, v2); 
    gluTessVertex(tobj, v3, v3); 
    gluTessVertex(tobj, v4, v4); 
  gluTessEndContour(tobj); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v5, v5); 
    gluTessVertex(tobj, v6, v6); 
    gluTessVertex(tobj, v7, v7); 
  gluTessEndContour(tobj); 
gluTessEndPolygon(tobj);
```

## <a name="requirements"></a><span data-ttu-id="ef4ec-126">Требования</span><span class="sxs-lookup"><span data-stu-id="ef4ec-126">Requirements</span></span>



| <span data-ttu-id="ef4ec-127">Требование</span><span class="sxs-lookup"><span data-stu-id="ef4ec-127">Requirement</span></span> | <span data-ttu-id="ef4ec-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ef4ec-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ef4ec-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef4ec-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ef4ec-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ef4ec-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ef4ec-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef4ec-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ef4ec-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ef4ec-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ef4ec-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ef4ec-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef4ec-134"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef4ec-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="ef4ec-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ef4ec-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef4ec-136"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef4ec-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ef4ec-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ef4ec-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef4ec-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef4ec-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef4ec-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef4ec-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef4ec-140">**глуневтесс**</span><span class="sxs-lookup"><span data-stu-id="ef4ec-140">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="ef4ec-141">**глутессбегинконтаур**</span><span class="sxs-lookup"><span data-stu-id="ef4ec-141">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="ef4ec-142">*глутесскаллбакк*</span><span class="sxs-lookup"><span data-stu-id="ef4ec-142">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="ef4ec-143">**глутессендконтаур**</span><span class="sxs-lookup"><span data-stu-id="ef4ec-143">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="ef4ec-144">**глутесснормал**</span><span class="sxs-lookup"><span data-stu-id="ef4ec-144">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="ef4ec-145">**глутесспроперти**</span><span class="sxs-lookup"><span data-stu-id="ef4ec-145">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="ef4ec-146">**глутессвертекс**</span><span class="sxs-lookup"><span data-stu-id="ef4ec-146">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





