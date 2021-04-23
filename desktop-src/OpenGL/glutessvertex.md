---
title: Функция Глутессвертекс (GLU. h)
description: Функция Глутессвертекс указывает вершину многоугольника.
ms.assetid: 9c555b32-5257-4eeb-9323-ccad59591097
keywords:
- Функция Глутессвертекс OpenGL
topic_type:
- apiref
api_name:
- gluTessVertex
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546bbad2be1205f62c7889fbb18f23d5b0e38b8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535243"
---
# <a name="glutessvertex-function"></a><span data-ttu-id="45f7a-104">Функция Глутессвертекс</span><span class="sxs-lookup"><span data-stu-id="45f7a-104">gluTessVertex function</span></span>

<span data-ttu-id="45f7a-105">Функция **глутессвертекс** указывает вершину многоугольника.</span><span class="sxs-lookup"><span data-stu-id="45f7a-105">The **gluTessVertex** function specifies a vertex on a polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="45f7a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45f7a-106">Syntax</span></span>


```C++
void WINAPI gluTessVertex(
   GLUtesselator *tess,
   GLdouble      coords[3],
   void          *data
);
```



## <a name="parameters"></a><span data-ttu-id="45f7a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="45f7a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45f7a-108">*тесс*</span><span class="sxs-lookup"><span data-stu-id="45f7a-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="45f7a-109">Объект тесселяции (созданный с помощью [**глуневтесс**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="45f7a-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="45f7a-110">*coords*</span><span class="sxs-lookup"><span data-stu-id="45f7a-110">*coords*</span></span> 
</dt> <dd>

<span data-ttu-id="45f7a-111">Расположение вершины.</span><span class="sxs-lookup"><span data-stu-id="45f7a-111">The location of the vertex.</span></span>

</dd> <dt>

<span data-ttu-id="45f7a-112">*data*</span><span class="sxs-lookup"><span data-stu-id="45f7a-112">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="45f7a-113">Указатель, передаваемый обратно в программу с обратным вызовом вершины (как указано в [*глутесскаллбакк*](glutess.md)).</span><span class="sxs-lookup"><span data-stu-id="45f7a-113">An pointer passed back to the program with the vertex callback (as specified by [*gluTessCallback*](glutess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45f7a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45f7a-114">Return value</span></span>

<span data-ttu-id="45f7a-115">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="45f7a-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="45f7a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45f7a-116">Remarks</span></span>

<span data-ttu-id="45f7a-117">Функция **глутессвертекс** описывает вершину многоугольника, определяемого пользователем.</span><span class="sxs-lookup"><span data-stu-id="45f7a-117">The **gluTessVertex** function describes a vertex on a polygon that the user is defining.</span></span> <span data-ttu-id="45f7a-118">Последовательные вызовы **глутессвертекс** описывают закрытый профиль.</span><span class="sxs-lookup"><span data-stu-id="45f7a-118">Successive **gluTessVertex** calls describe a closed contour.</span></span> <span data-ttu-id="45f7a-119">Например, чтобы описать грани четырехсторонней, вызовите **глутессвертекс** четыре раза.</span><span class="sxs-lookup"><span data-stu-id="45f7a-119">For example, to describe a quadrilateral, call **gluTessVertex** four times.</span></span> <span data-ttu-id="45f7a-120">**Глутессвертекс** можно вызывать только между [**глутессбегинконтаур**](glutessbegincontour.md) и [**глутессендконтаур**](glutessendcontour.md).</span><span class="sxs-lookup"><span data-stu-id="45f7a-120">You can only call **gluTessVertex** between [**gluTessBeginContour**](glutessbegincontour.md) and [**gluTessEndContour**](glutessendcontour.md).</span></span>

<span data-ttu-id="45f7a-121">Параметр *данных* обычно указывает на структуру, содержащую расположение вершины, а также на другие атрибуты для каждой вершины, такие как цвет и обычный.</span><span class="sxs-lookup"><span data-stu-id="45f7a-121">The *data* parameter normally points to a structure containing the vertex location, as well as other per-vertex attributes such as color and normal.</span></span> <span data-ttu-id="45f7a-122">Этот указатель передается обратно в программу через \_ обратный вызов вершины Glu после тесселяции (см. [*глутесскаллбакк*](glutess.md)).</span><span class="sxs-lookup"><span data-stu-id="45f7a-122">This pointer is passed back to the program through the GLU\_VERTEX callback after tessellation (see [*gluTessCallback*](glutess.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="45f7a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="45f7a-123">Requirements</span></span>



| <span data-ttu-id="45f7a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="45f7a-124">Requirement</span></span> | <span data-ttu-id="45f7a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="45f7a-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="45f7a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45f7a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="45f7a-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="45f7a-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="45f7a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45f7a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="45f7a-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="45f7a-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="45f7a-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="45f7a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="45f7a-131"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="45f7a-131"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="45f7a-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="45f7a-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="45f7a-133"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45f7a-133"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="45f7a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="45f7a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45f7a-135"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45f7a-135"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45f7a-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45f7a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45f7a-137">**глуневтесс**</span><span class="sxs-lookup"><span data-stu-id="45f7a-137">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="45f7a-138">**глутессбегинконтаур**</span><span class="sxs-lookup"><span data-stu-id="45f7a-138">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="45f7a-139">**глутессбегинполигон**</span><span class="sxs-lookup"><span data-stu-id="45f7a-139">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="45f7a-140">*глутесскаллбакк*</span><span class="sxs-lookup"><span data-stu-id="45f7a-140">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="45f7a-141">**глутессендконтаур**</span><span class="sxs-lookup"><span data-stu-id="45f7a-141">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="45f7a-142">**глутесснормал**</span><span class="sxs-lookup"><span data-stu-id="45f7a-142">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="45f7a-143">**глутесспроперти**</span><span class="sxs-lookup"><span data-stu-id="45f7a-143">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> </dl>

 

 





