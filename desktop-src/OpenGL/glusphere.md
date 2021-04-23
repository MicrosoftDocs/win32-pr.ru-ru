---
title: Функция Глусфере (GLU. h)
description: Функция Глусфере рисует сферу.
ms.assetid: 0f1919c6-0551-4d50-b782-767dacc088cb
keywords:
- Функция Глусфере OpenGL
topic_type:
- apiref
api_name:
- gluSphere
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899ff4833c705aae34fdb7830c264fee91414116
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491907"
---
# <a name="glusphere-function"></a><span data-ttu-id="41f38-104">Функция Глусфере</span><span class="sxs-lookup"><span data-stu-id="41f38-104">gluSphere function</span></span>

<span data-ttu-id="41f38-105">Функция **глусфере** рисует сферу.</span><span class="sxs-lookup"><span data-stu-id="41f38-105">The **gluSphere** function draws a sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="41f38-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41f38-106">Syntax</span></span>


```C++
void WINAPI gluSphere(
   GLUquadric *qobj,
   GLdouble   radius,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a><span data-ttu-id="41f38-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="41f38-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41f38-108">*кобж*</span><span class="sxs-lookup"><span data-stu-id="41f38-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="41f38-109">Объект куадрик (созданный с помощью [**глуневкуадрик**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="41f38-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="41f38-110">*RADIUS*</span><span class="sxs-lookup"><span data-stu-id="41f38-110">*radius*</span></span> 
</dt> <dd>

<span data-ttu-id="41f38-111">Радиус сферы.</span><span class="sxs-lookup"><span data-stu-id="41f38-111">The radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="41f38-112">*срезы*</span><span class="sxs-lookup"><span data-stu-id="41f38-112">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="41f38-113">Число подразделений вокруг оси z (как и линии долготы).</span><span class="sxs-lookup"><span data-stu-id="41f38-113">The number of subdivisions around the z-axis (similar to lines of longitude).</span></span>

</dd> <dt>

<span data-ttu-id="41f38-114">*стеки*</span><span class="sxs-lookup"><span data-stu-id="41f38-114">*stacks*</span></span> 
</dt> <dd>

<span data-ttu-id="41f38-115">Число подразделений вдоль оси z (аналогично линиям широты).</span><span class="sxs-lookup"><span data-stu-id="41f38-115">The number of subdivisions along the z-axis (similar to lines of latitude).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41f38-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41f38-116">Return value</span></span>

<span data-ttu-id="41f38-117">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="41f38-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41f38-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41f38-118">Remarks</span></span>

<span data-ttu-id="41f38-119">Функция **глусфере** рисует сферу заданного радиуса по центру от начала координат.</span><span class="sxs-lookup"><span data-stu-id="41f38-119">The **gluSphere** function draws a sphere of the given radius centered around the origin.</span></span> <span data-ttu-id="41f38-120">Сфера разделяется вокруг оси z на срезы и вдоль оси z в стеки (аналогично линиям долготы и широты).</span><span class="sxs-lookup"><span data-stu-id="41f38-120">The sphere is subdivided around the z-axis into slices and along the z-axis into stacks (similar to lines of longitude and latitude).</span></span>

<span data-ttu-id="41f38-121">Если для ориентации задано значение GLU \_ снаружи (с **глукуадрикориентатион**), все обычные нормализованные значения выходят за пределы центра сферы.</span><span class="sxs-lookup"><span data-stu-id="41f38-121">If the orientation is set to GLU\_OUTSIDE (with **gluQuadricOrientation**), any normals generated point away from the center of the sphere.</span></span> <span data-ttu-id="41f38-122">В противном случае они указывают на центр сферы.</span><span class="sxs-lookup"><span data-stu-id="41f38-122">Otherwise, they point toward the center of the sphere.</span></span>

<span data-ttu-id="41f38-123">Если текстурирование включено (с **глукуадриктекстуре**), то координаты текстуры формируются таким образом, чтобы *диапазоны* в диапазоне от 0,0 по *z* =-*радиусу* 1,0 по *z*  =  *радиусу* (*t* — линейно по долготу линиям  ). и находятся в диапазоне от 0,0 на положительной оси y, до 0,25 на позитивной оси x, до 0,5 на отрицательной оси y, в 0,75 по отрицательной оси x и обратно в 1,0 на положительной оси y.</span><span class="sxs-lookup"><span data-stu-id="41f38-123">If texturing is turned on (with **gluQuadricTexture**): texture coordinates are generated so that *t* ranges from 0.0 at *z* = -*radius* to 1.0 at *z* = *radius* (*t* increases linearly along longitudinal lines); and *s* ranges from 0.0 at the positive y-axis, to 0.25 at the positive x-axis, to 0.5 at the negative y-axis, to 0.75 at the negative x-axis, and back to 1.0 at the positive y-axis.</span></span>

## <a name="requirements"></a><span data-ttu-id="41f38-124">Требования</span><span class="sxs-lookup"><span data-stu-id="41f38-124">Requirements</span></span>



| <span data-ttu-id="41f38-125">Требование</span><span class="sxs-lookup"><span data-stu-id="41f38-125">Requirement</span></span> | <span data-ttu-id="41f38-126">Значение</span><span class="sxs-lookup"><span data-stu-id="41f38-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="41f38-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41f38-127">Minimum supported client</span></span><br/> | <span data-ttu-id="41f38-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="41f38-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="41f38-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41f38-129">Minimum supported server</span></span><br/> | <span data-ttu-id="41f38-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="41f38-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="41f38-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="41f38-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="41f38-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="41f38-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="41f38-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="41f38-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="41f38-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41f38-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="41f38-135">DLL</span><span class="sxs-lookup"><span data-stu-id="41f38-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41f38-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41f38-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41f38-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41f38-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41f38-138">**глуцилиндер**</span><span class="sxs-lookup"><span data-stu-id="41f38-138">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="41f38-139">**глудиск**</span><span class="sxs-lookup"><span data-stu-id="41f38-139">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="41f38-140">**глуневкуадрик**</span><span class="sxs-lookup"><span data-stu-id="41f38-140">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="41f38-141">**глупартиалдиск**</span><span class="sxs-lookup"><span data-stu-id="41f38-141">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="41f38-142">**глукуадрикориентатион**</span><span class="sxs-lookup"><span data-stu-id="41f38-142">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="41f38-143">**глукуадриктекстуре**</span><span class="sxs-lookup"><span data-stu-id="41f38-143">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





