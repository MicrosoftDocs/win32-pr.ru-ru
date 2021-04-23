---
title: Функция Глутессендконтаур (GLU. h)
description: Функции Глутессбегинконтаур и Глутессендконтаур разделяют описание контура. | Функция Глутессендконтаур (GLU. h)
ms.assetid: 115db079-cbcb-48e1-8bab-0eb4814afb82
keywords:
- Функция Глутессендконтаур OpenGL
topic_type:
- apiref
api_name:
- gluTessEndContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac53f3920476489a1453bb6b5dc1e01d650d4fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352542"
---
# <a name="glutessendcontour-function"></a><span data-ttu-id="72081-105">Функция Глутессендконтаур</span><span class="sxs-lookup"><span data-stu-id="72081-105">gluTessEndContour function</span></span>

<span data-ttu-id="72081-106">Функции [**глутессбегинконтаур**](glutessbegincontour.md) и **глутессендконтаур** разделяют описание контура.</span><span class="sxs-lookup"><span data-stu-id="72081-106">The [**gluTessBeginContour**](glutessbegincontour.md) and **gluTessEndContour** functions delimit a contour description.</span></span>

## <a name="syntax"></a><span data-ttu-id="72081-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72081-107">Syntax</span></span>


```C++
void WINAPI gluTessEndContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="72081-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="72081-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72081-109">*тесс*</span><span class="sxs-lookup"><span data-stu-id="72081-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="72081-110">Объект тесселяции (созданный с помощью [**глуневтесс**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="72081-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72081-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="72081-111">Return value</span></span>

<span data-ttu-id="72081-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="72081-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="72081-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="72081-113">Remarks</span></span>

<span data-ttu-id="72081-114">Функции [**глутессбегинконтаур**](glutessbegincontour.md) и **глутессендконтаур** разделяют определение контура многоугольника.</span><span class="sxs-lookup"><span data-stu-id="72081-114">The [**gluTessBeginContour**](glutessbegincontour.md) and **gluTessEndContour** functions delimit the definition of a polygon contour.</span></span> <span data-ttu-id="72081-115">Внутри каждой пары **глутессбегинконтаур** / **глутессендконтаур** может быть несколько вызовов [**глутессвертекс**](glutessvertex.md).</span><span class="sxs-lookup"><span data-stu-id="72081-115">Within each **gluTessBeginContour**/**gluTessEndContour** pair, there can be zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="72081-116">Вершины задают замкнутый контур (последняя вершина каждого контура автоматически связывается с первым).</span><span class="sxs-lookup"><span data-stu-id="72081-116">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span> <span data-ttu-id="72081-117">**Глутессбегинконтаур** можно вызывать только между [**глутессбегинполигон**](glutessbeginpolygon.md) и [**глутессендполигон**](glutessendpolygon.md).</span><span class="sxs-lookup"><span data-stu-id="72081-117">You can call **gluTessBeginContour** only between [**gluTessBeginPolygon**](glutessbeginpolygon.md) and [**gluTessEndPolygon**](glutessendpolygon.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72081-118">Требования</span><span class="sxs-lookup"><span data-stu-id="72081-118">Requirements</span></span>



| <span data-ttu-id="72081-119">Требование</span><span class="sxs-lookup"><span data-stu-id="72081-119">Requirement</span></span> | <span data-ttu-id="72081-120">Значение</span><span class="sxs-lookup"><span data-stu-id="72081-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="72081-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="72081-121">Minimum supported client</span></span><br/> | <span data-ttu-id="72081-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="72081-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="72081-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="72081-123">Minimum supported server</span></span><br/> | <span data-ttu-id="72081-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="72081-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="72081-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="72081-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="72081-126"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="72081-126"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="72081-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="72081-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="72081-128"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72081-128"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="72081-129">DLL</span><span class="sxs-lookup"><span data-stu-id="72081-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72081-130"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72081-130"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72081-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72081-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72081-132">**глуневтесс**</span><span class="sxs-lookup"><span data-stu-id="72081-132">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="72081-133">**глутессбегинполигон**</span><span class="sxs-lookup"><span data-stu-id="72081-133">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="72081-134">*глутесскаллбакк*</span><span class="sxs-lookup"><span data-stu-id="72081-134">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="72081-135">**глутессендполигон**</span><span class="sxs-lookup"><span data-stu-id="72081-135">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> <dt>

[<span data-ttu-id="72081-136">**глутесснормал**</span><span class="sxs-lookup"><span data-stu-id="72081-136">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="72081-137">**глутесспроперти**</span><span class="sxs-lookup"><span data-stu-id="72081-137">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="72081-138">**глутессвертекс**</span><span class="sxs-lookup"><span data-stu-id="72081-138">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





