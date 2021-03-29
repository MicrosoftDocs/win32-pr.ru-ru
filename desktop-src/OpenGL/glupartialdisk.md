---
title: Функция Глупартиалдиск (GLU. h)
description: Функция Глупартиалдиск Рисует дугу диска.
ms.assetid: 46809c15-88c3-40fa-965a-7aeeedc1c598
keywords:
- Функция Глупартиалдиск OpenGL
topic_type:
- apiref
api_name:
- gluPartialDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36e35a6ea905f20e1cb30eddc5b270786614403b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661821"
---
# <a name="glupartialdisk-function"></a><span data-ttu-id="f5a71-104">Функция Глупартиалдиск</span><span class="sxs-lookup"><span data-stu-id="f5a71-104">gluPartialDisk function</span></span>

<span data-ttu-id="f5a71-105">Функция **глупартиалдиск** Рисует дугу диска.</span><span class="sxs-lookup"><span data-stu-id="f5a71-105">The **gluPartialDisk** function draws an arc of a disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5a71-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5a71-106">Syntax</span></span>


```C++
void WINAPI gluPartialDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops,
   GLdouble   startAngle,
   GLdouble   sweepAngle
);
```



## <a name="parameters"></a><span data-ttu-id="f5a71-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5a71-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5a71-108">*кобж*</span><span class="sxs-lookup"><span data-stu-id="f5a71-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="f5a71-109">Объект куадрик (созданный с помощью [**глуневкуадрик**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="f5a71-109">A quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="f5a71-110">*иннеррадиус*</span><span class="sxs-lookup"><span data-stu-id="f5a71-110">*innerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="f5a71-111">Внутренний радиус частичного диска (может быть равен нулю).</span><span class="sxs-lookup"><span data-stu-id="f5a71-111">The inner radius of the partial disk (can be zero).</span></span>

</dd> <dt>

<span data-ttu-id="f5a71-112">*аутеррадиус*</span><span class="sxs-lookup"><span data-stu-id="f5a71-112">*outerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="f5a71-113">Внешний радиус частичного диска.</span><span class="sxs-lookup"><span data-stu-id="f5a71-113">The outer radius of the partial disk.</span></span>

</dd> <dt>

<span data-ttu-id="f5a71-114">*срезы*</span><span class="sxs-lookup"><span data-stu-id="f5a71-114">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="f5a71-115">Число подразделений вокруг оси z.</span><span class="sxs-lookup"><span data-stu-id="f5a71-115">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="f5a71-116">*бираются*</span><span class="sxs-lookup"><span data-stu-id="f5a71-116">*loops*</span></span> 
</dt> <dd>

<span data-ttu-id="f5a71-117">Количество концентрических колец относительно источника, в который делится часть диска.</span><span class="sxs-lookup"><span data-stu-id="f5a71-117">The number of concentric rings about the origin into which the partial disk is subdivided.</span></span>

</dd> <dt>

<span data-ttu-id="f5a71-118">*startAngle и заканчивая*</span><span class="sxs-lookup"><span data-stu-id="f5a71-118">*startAngle*</span></span> 
</dt> <dd>

<span data-ttu-id="f5a71-119">Начальный угол (в градусах) части диска.</span><span class="sxs-lookup"><span data-stu-id="f5a71-119">The starting angle, in degrees, of the disk portion.</span></span>

</dd> <dt>

<span data-ttu-id="f5a71-120">*свипангле*</span><span class="sxs-lookup"><span data-stu-id="f5a71-120">*sweepAngle*</span></span> 
</dt> <dd>

<span data-ttu-id="f5a71-121">Угол поворота (в градусах) части диска.</span><span class="sxs-lookup"><span data-stu-id="f5a71-121">The sweep angle, in degrees, of the disk portion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5a71-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5a71-122">Return value</span></span>

<span data-ttu-id="f5a71-123">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f5a71-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5a71-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5a71-124">Remarks</span></span>

<span data-ttu-id="f5a71-125">Функция **глупартиалдиск** визуализирует частичный диск на плоскости *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="f5a71-125">The **gluPartialDisk** function renders a partial disk on the *z* = 0 plane.</span></span> <span data-ttu-id="f5a71-126">Частичный диск аналогичен полному диску, за исключением того, что включается только подмножество диска с *startAngle* по *startAngle*  +  *свипангле* (где 0 градусов — это положительная ось y, 90 градусов — вдоль положительной оси x, 180 270 градусов — вдоль отрицательной оси x).</span><span class="sxs-lookup"><span data-stu-id="f5a71-126">A partial disk is similar to a full disk, except that only the subset of the disk from *startAngle* through *startAngle* + *sweepAngle* is included (where 0 degrees is along the positive y-axis, 90 degrees is along the positive x-axis, 180 degrees is along the negative y-axis, and 270 degrees is along the negative x-axis).</span></span>

<span data-ttu-id="f5a71-127">Частичный диск имеет радиус *аутеррадиус* и содержит концентрические циклическое отверстие с радиусом *иннеррадиус*.</span><span class="sxs-lookup"><span data-stu-id="f5a71-127">The partial disk has a radius of *outerRadius* and contains a concentric circular hole with a radius of *innerRadius*.</span></span> <span data-ttu-id="f5a71-128">Если *иннеррадиус* равен нулю, отверстие не создается.</span><span class="sxs-lookup"><span data-stu-id="f5a71-128">If *innerRadius* is zero, then no hole is generated.</span></span> <span data-ttu-id="f5a71-129">Частичный диск делится вокруг оси z на срезы (например, срезы пиццы), а также о оси z в кольцах (как указано *срезами* и *циклами* соответственно).</span><span class="sxs-lookup"><span data-stu-id="f5a71-129">The partial disk is subdivided around the z-axis into slices (like pizza slices), and also about the z-axis into rings (as specified by *slices* and *loops*, respectively).</span></span>

<span data-ttu-id="f5a71-130">С точки зрения ориентации, положительная z-сторона частичного диска считается внешней (см. [**глукуадрикориентатион**](gluquadricorientation.md)).</span><span class="sxs-lookup"><span data-stu-id="f5a71-130">With respect to orientation, the positive z-side of the partial disk is considered to be outside (see [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span> <span data-ttu-id="f5a71-131">Это означает, что если для ориентации задано значение GLU \_ снаружи, то все создаваемые нормали указываются вдоль положительной оси z.</span><span class="sxs-lookup"><span data-stu-id="f5a71-131">This means that if the orientation is set to GLU\_OUTSIDE, then any normals generated point along the positive z-axis.</span></span>

<span data-ttu-id="f5a71-132">Если вы включили текстурирование (с [**глукуадриктекстуре**](gluquadrictexture.md)), **глупартиалдиск** создает координаты текстуры линейно, например, где *r*  =  *аутеррадиус*, значение в (*r*, 0, 0) равно (1, 0,5); в (0, *r*, 0) это (0,5, 1); в (*r*, 0, 0) это (0, 0,5), а в (0, *r*, 0) — (0,5, 0).</span><span class="sxs-lookup"><span data-stu-id="f5a71-132">If you have turned on texturing (with [**gluQuadricTexture**](gluquadrictexture.md)), **gluPartialDisk** generates texture coordinates linearly such that where *r* = *outerRadius*, the value at (*r*, 0, 0) is (1, 0.5); at (0, *r*, 0) it is (0.5, 1); at (*r*, 0, 0) it is (0, 0.5); and at (0, *r*, 0) it is (0.5, 0).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5a71-133">Требования</span><span class="sxs-lookup"><span data-stu-id="f5a71-133">Requirements</span></span>



| <span data-ttu-id="f5a71-134">Требование</span><span class="sxs-lookup"><span data-stu-id="f5a71-134">Requirement</span></span> | <span data-ttu-id="f5a71-135">Значение</span><span class="sxs-lookup"><span data-stu-id="f5a71-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a71-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5a71-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f5a71-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f5a71-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f5a71-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5a71-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f5a71-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f5a71-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f5a71-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f5a71-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5a71-141"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5a71-141"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="f5a71-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f5a71-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="f5a71-143"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5a71-143"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f5a71-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f5a71-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5a71-145"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5a71-145"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5a71-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5a71-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a71-147">**глуцилиндер**</span><span class="sxs-lookup"><span data-stu-id="f5a71-147">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="f5a71-148">**глудиск**</span><span class="sxs-lookup"><span data-stu-id="f5a71-148">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="f5a71-149">**глуневкуадрик**</span><span class="sxs-lookup"><span data-stu-id="f5a71-149">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="f5a71-150">**глукуадрикориентатион**</span><span class="sxs-lookup"><span data-stu-id="f5a71-150">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="f5a71-151">**глукуадриктекстуре**</span><span class="sxs-lookup"><span data-stu-id="f5a71-151">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="f5a71-152">**глусфере**</span><span class="sxs-lookup"><span data-stu-id="f5a71-152">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





