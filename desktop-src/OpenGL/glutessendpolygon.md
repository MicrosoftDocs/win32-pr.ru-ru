---
title: Функция Глутессендполигон (GLU. h)
description: Функции Глутессбегинполигон и Глутессендполигон разделяют описание многоугольника. | Функция Глутессендполигон (GLU. h)
ms.assetid: c9ae2075-59d7-4c1a-b720-0aa05954525c
keywords:
- Функция Глутессендполигон OpenGL
topic_type:
- apiref
api_name:
- gluTessEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f9176e5bdb64dc0e3cd21bd42735e57b541b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684873"
---
# <a name="glutessendpolygon-function"></a><span data-ttu-id="61daf-105">Функция Глутессендполигон</span><span class="sxs-lookup"><span data-stu-id="61daf-105">gluTessEndPolygon function</span></span>

<span data-ttu-id="61daf-106">Функции [**глутессбегинполигон**](glutessbeginpolygon.md) и **глутессендполигон** разделяют описание многоугольника.</span><span class="sxs-lookup"><span data-stu-id="61daf-106">The [**gluTessBeginPolygon**](glutessbeginpolygon.md) and **gluTessEndPolygon** functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="61daf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61daf-107">Syntax</span></span>


```C++
void WINAPI gluTessEndPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="61daf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="61daf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61daf-109">*тесс*</span><span class="sxs-lookup"><span data-stu-id="61daf-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="61daf-110">Объект тесселяции (созданный с помощью [**глуневтесс**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="61daf-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61daf-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="61daf-111">Return value</span></span>

<span data-ttu-id="61daf-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="61daf-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="61daf-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="61daf-113">Remarks</span></span>

<span data-ttu-id="61daf-114">Функции [**глутессбегинполигон**](glutessbeginpolygon.md) и **глутессендполигон** разделяют определение многоугольника нонконвекс.</span><span class="sxs-lookup"><span data-stu-id="61daf-114">The [**gluTessBeginPolygon**](glutessbeginpolygon.md) and **gluTessEndPolygon** functions delimit the definition of a nonconvex polygon.</span></span> <span data-ttu-id="61daf-115">В каждой паре **глутессбегинполигон**  /  **глутессендполигон** включите один или несколько вызовов [**глутессбегинконтаур**](glutessbegincontour.md).</span><span class="sxs-lookup"><span data-stu-id="61daf-115">Within each **gluTessBeginPolygon** / **gluTessEndPolygon** pair, include one or more calls to [**gluTessBeginContour**](glutessbegincontour.md).</span></span> <span data-ttu-id="61daf-116">В каждом контуре имеется ноль или более вызовов [**глутессвертекс**](glutessvertex.md).</span><span class="sxs-lookup"><span data-stu-id="61daf-116">Within each contour, there are zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="61daf-117">Вершины задают замкнутый контур (последняя вершина каждого контура автоматически связывается с первым).</span><span class="sxs-lookup"><span data-stu-id="61daf-117">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span>

<span data-ttu-id="61daf-118">Параметр *\_ данных Polygon* — это указатель на структуру данных, определяемую программистом.</span><span class="sxs-lookup"><span data-stu-id="61daf-118">The *polygon\_data* parameter is a pointer to a programmer-defined data structure.</span></span> <span data-ttu-id="61daf-119">Если указаны соответствующие обратные вызовы (см. [*глутесскаллбакк*](glutess.md)), этот указатель возвращается функции обратного вызова или функциям, что делает его удобным способом для хранения информации на многоугольнике.</span><span class="sxs-lookup"><span data-stu-id="61daf-119">If the appropriate callbacks are specified (see [*gluTessCallback*](glutess.md)), this pointer is returned to the callback function or functions, making it a convenient way to store per-polygon information.</span></span>

<span data-ttu-id="61daf-120">При вызове **глутессендполигон** многоугольник размещается мозаикой, а итоговые треугольники — с помощью обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="61daf-120">When you call **gluTessEndPolygon**, the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="61daf-121">Описание функций обратного вызова см. в разделе [*глутесскаллбакк*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="61daf-121">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="61daf-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="61daf-122">Examples</span></span>

<span data-ttu-id="61daf-123">Ниже описывается грани четырехсторонней с треугольным отверстием:</span><span class="sxs-lookup"><span data-stu-id="61daf-123">The following describes a quadrilateral with a triangular hole:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="61daf-124">Требования</span><span class="sxs-lookup"><span data-stu-id="61daf-124">Requirements</span></span>



| <span data-ttu-id="61daf-125">Требование</span><span class="sxs-lookup"><span data-stu-id="61daf-125">Requirement</span></span> | <span data-ttu-id="61daf-126">Значение</span><span class="sxs-lookup"><span data-stu-id="61daf-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="61daf-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61daf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="61daf-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61daf-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="61daf-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61daf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="61daf-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61daf-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="61daf-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="61daf-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="61daf-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="61daf-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="61daf-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="61daf-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="61daf-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61daf-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="61daf-135">DLL</span><span class="sxs-lookup"><span data-stu-id="61daf-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61daf-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61daf-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61daf-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61daf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61daf-138">**глуневтесс**</span><span class="sxs-lookup"><span data-stu-id="61daf-138">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="61daf-139">**глутессбегинконтаур**</span><span class="sxs-lookup"><span data-stu-id="61daf-139">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="61daf-140">*глутесскаллбакк*</span><span class="sxs-lookup"><span data-stu-id="61daf-140">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="61daf-141">**глутессендконтаур**</span><span class="sxs-lookup"><span data-stu-id="61daf-141">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="61daf-142">**глутесснормал**</span><span class="sxs-lookup"><span data-stu-id="61daf-142">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="61daf-143">**глутесспроперти**</span><span class="sxs-lookup"><span data-stu-id="61daf-143">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="61daf-144">**глутессвертекс**</span><span class="sxs-lookup"><span data-stu-id="61daf-144">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





