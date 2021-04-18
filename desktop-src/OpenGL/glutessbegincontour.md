---
title: Функция Глутессбегинконтаур (GLU. h)
description: Функции Глутессбегинконтаур и Глутессендконтаур разделяют описание контура. | Функция Глутессбегинконтаур (GLU. h)
ms.assetid: 4008ce9c-86e7-4b24-9bda-5915f469596a
keywords:
- Функция Глутессбегинконтаур OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd28efc96c977e5e0483b4f3d87e9ce840b985cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684904"
---
# <a name="glutessbegincontour-function"></a><span data-ttu-id="11794-105">Функция Глутессбегинконтаур</span><span class="sxs-lookup"><span data-stu-id="11794-105">gluTessBeginContour function</span></span>

<span data-ttu-id="11794-106">Функции **глутессбегинконтаур** и [**глутессендконтаур**](glutessendcontour.md) разделяют описание контура.</span><span class="sxs-lookup"><span data-stu-id="11794-106">The **gluTessBeginContour** and [**gluTessEndContour**](glutessendcontour.md) functions delimit a contour description.</span></span>

## <a name="syntax"></a><span data-ttu-id="11794-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11794-107">Syntax</span></span>


```C++
void WINAPI gluTessBeginContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="11794-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="11794-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11794-109">*тесс*</span><span class="sxs-lookup"><span data-stu-id="11794-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="11794-110">Объект тесселяции (созданный с помощью [**глуневтесс**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="11794-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11794-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11794-111">Return value</span></span>

<span data-ttu-id="11794-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="11794-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="11794-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11794-113">Remarks</span></span>

<span data-ttu-id="11794-114">Функции **глутессбегинконтаур** и [**глутессендполигон**](glutessendpolygon.md) разделяют определение контура многоугольника.</span><span class="sxs-lookup"><span data-stu-id="11794-114">The **gluTessBeginContour** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit the definition of a polygon contour.</span></span> <span data-ttu-id="11794-115">Внутри каждой пары **глутессбегинконтаур** / **глутессендполигон** может быть несколько вызовов [**глутессвертекс**](glutessvertex.md).</span><span class="sxs-lookup"><span data-stu-id="11794-115">Within each **gluTessBeginContour**/**gluTessEndPolygon** pair, there can be zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="11794-116">Вершины задают замкнутый контур (последняя вершина каждого контура автоматически связывается с первым).</span><span class="sxs-lookup"><span data-stu-id="11794-116">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span> <span data-ttu-id="11794-117">**Глутессбегинконтаур** можно вызывать только между [**глутессбегинполигон**](glutessbeginpolygon.md) и **глутессендполигон**.</span><span class="sxs-lookup"><span data-stu-id="11794-117">You can call **gluTessBeginContour** only between [**gluTessBeginPolygon**](glutessbeginpolygon.md) and **gluTessEndPolygon**.</span></span>

## <a name="requirements"></a><span data-ttu-id="11794-118">Требования</span><span class="sxs-lookup"><span data-stu-id="11794-118">Requirements</span></span>



| <span data-ttu-id="11794-119">Требование</span><span class="sxs-lookup"><span data-stu-id="11794-119">Requirement</span></span> | <span data-ttu-id="11794-120">Значение</span><span class="sxs-lookup"><span data-stu-id="11794-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="11794-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11794-121">Minimum supported client</span></span><br/> | <span data-ttu-id="11794-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="11794-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="11794-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11794-123">Minimum supported server</span></span><br/> | <span data-ttu-id="11794-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="11794-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="11794-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="11794-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="11794-126"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="11794-126"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="11794-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="11794-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="11794-128"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11794-128"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="11794-129">DLL</span><span class="sxs-lookup"><span data-stu-id="11794-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11794-130"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11794-130"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11794-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11794-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11794-132">**глуневтесс**</span><span class="sxs-lookup"><span data-stu-id="11794-132">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="11794-133">**глутессбегинполигон**</span><span class="sxs-lookup"><span data-stu-id="11794-133">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="11794-134">*глутесскаллбакк*</span><span class="sxs-lookup"><span data-stu-id="11794-134">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="11794-135">**глутессендполигон**</span><span class="sxs-lookup"><span data-stu-id="11794-135">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> <dt>

[<span data-ttu-id="11794-136">**глутесснормал**</span><span class="sxs-lookup"><span data-stu-id="11794-136">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="11794-137">**глутесспроперти**</span><span class="sxs-lookup"><span data-stu-id="11794-137">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="11794-138">**глутессвертекс**</span><span class="sxs-lookup"><span data-stu-id="11794-138">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





