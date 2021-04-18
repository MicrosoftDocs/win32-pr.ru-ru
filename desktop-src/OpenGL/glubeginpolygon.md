---
title: Функция Глубегинполигон (GLU. h)
description: Функции Глубегинполигон и Глуендполигон разделяют описание многоугольника. | Функция Глубегинполигон (GLU. h)
ms.assetid: e4da731c-2082-4dbc-ae3a-8d6b30d50253
keywords:
- Функция Глубегинполигон OpenGL
topic_type:
- apiref
api_name:
- gluBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60204e7d937b4686f3757b520c820886e168529e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664879"
---
# <a name="glubeginpolygon-function"></a><span data-ttu-id="96460-105">Функция Глубегинполигон</span><span class="sxs-lookup"><span data-stu-id="96460-105">gluBeginPolygon function</span></span>

<span data-ttu-id="96460-106">\[Функция **глубегинполигон** устарела и предоставляется только для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="96460-106">\[The **gluBeginPolygon** function is obsolete and is provided for backward compatibility only.</span></span> <span data-ttu-id="96460-107">Функция **глубегинполигон** сопоставляется с [**глутессбегинполигон**](glutessbeginpolygon.md) , за которым следует [**глутессбегинконтаур**](glutessbegincontour.md).\]</span><span class="sxs-lookup"><span data-stu-id="96460-107">The **gluBeginPolygon** function is mapped to [**gluTessBeginPolygon**](glutessbeginpolygon.md) followed by [**gluTessBeginContour**](glutessbegincontour.md).\]</span></span>

<span data-ttu-id="96460-108">Функции **глубегинполигон** и [**глуендполигон**](gluendpolygon.md) разделяют описание многоугольника.</span><span class="sxs-lookup"><span data-stu-id="96460-108">The **gluBeginPolygon** and [**gluEndPolygon**](gluendpolygon.md) functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="96460-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96460-109">Syntax</span></span>


```C++
void WINAPI gluBeginPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="96460-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="96460-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96460-111">*тесс*</span><span class="sxs-lookup"><span data-stu-id="96460-111">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="96460-112">Объект тесселяции (созданный с помощью [**глуневтесс**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="96460-112">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96460-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96460-113">Return value</span></span>

<span data-ttu-id="96460-114">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="96460-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="96460-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96460-115">Remarks</span></span>

<span data-ttu-id="96460-116">Используйте **глубегинполигон** и **глуендполигон** для разделения определения многоугольника нонконвекс.</span><span class="sxs-lookup"><span data-stu-id="96460-116">Use **gluBeginPolygon** and **gluEndPolygon** to delimit the definition of a nonconvex polygon.</span></span>

1.  <span data-ttu-id="96460-117">Вызовите **глубегинполигон**.</span><span class="sxs-lookup"><span data-stu-id="96460-117">Call **gluBeginPolygon**.</span></span>
2.  <span data-ttu-id="96460-118">Определите контуры многоугольника, вызвав [**глутессвертекс**](glutessvertex.md) для каждой вершины и [**глунекстконтаур**](glunextcontour.md) , чтобы начать каждый новый профиль.</span><span class="sxs-lookup"><span data-stu-id="96460-118">Define the contours of the polygon by calling [**gluTessVertex**](glutessvertex.md) for each vertex and [**gluNextContour**](glunextcontour.md) to start each new contour.</span></span>
3.  <span data-ttu-id="96460-119">Вызовите **глуендполигон** , чтобы сообщить об окончании определения.</span><span class="sxs-lookup"><span data-stu-id="96460-119">Call **gluEndPolygon** to signal the end of the definition.</span></span>

    <span data-ttu-id="96460-120">После вызова **глуендполигон** многоугольник размещается мозаикой, а итоговые треугольники — с помощью обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="96460-120">Once **gluEndPolygon** is called, the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="96460-121">Описание функций обратного вызова см. в разделе [*глутесскаллбакк*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="96460-121">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="96460-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="96460-122">Examples</span></span>

<span data-ttu-id="96460-123">В следующем примере описывается грани четырехсторонней с треугольным отверстием:</span><span class="sxs-lookup"><span data-stu-id="96460-123">The following example describes a quadrilateral with a triangular hole:</span></span>

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4); 
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7); 
gluEndPolygon(tess);
```

## <a name="requirements"></a><span data-ttu-id="96460-124">Требования</span><span class="sxs-lookup"><span data-stu-id="96460-124">Requirements</span></span>



| <span data-ttu-id="96460-125">Требование</span><span class="sxs-lookup"><span data-stu-id="96460-125">Requirement</span></span> | <span data-ttu-id="96460-126">Значение</span><span class="sxs-lookup"><span data-stu-id="96460-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="96460-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96460-127">Minimum supported client</span></span><br/> | <span data-ttu-id="96460-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="96460-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="96460-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96460-129">Minimum supported server</span></span><br/> | <span data-ttu-id="96460-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="96460-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="96460-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="96460-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="96460-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="96460-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="96460-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="96460-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="96460-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96460-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="96460-135">DLL</span><span class="sxs-lookup"><span data-stu-id="96460-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96460-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96460-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96460-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96460-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96460-138">**глуневтесс**</span><span class="sxs-lookup"><span data-stu-id="96460-138">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="96460-139">**глунекстконтаур**</span><span class="sxs-lookup"><span data-stu-id="96460-139">**gluNextContour**</span></span>](glunextcontour.md)
</dt> <dt>

[<span data-ttu-id="96460-140">**глутессбегинконтаур**</span><span class="sxs-lookup"><span data-stu-id="96460-140">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="96460-141">**глутессбегинполигон**</span><span class="sxs-lookup"><span data-stu-id="96460-141">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="96460-142">*глутесскаллбакк*</span><span class="sxs-lookup"><span data-stu-id="96460-142">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="96460-143">**глутессвертекс**</span><span class="sxs-lookup"><span data-stu-id="96460-143">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





