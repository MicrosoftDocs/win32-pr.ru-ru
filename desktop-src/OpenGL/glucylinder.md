---
title: Функция Глуцилиндер (GLU. h)
description: Функция Глуцилиндер рисует цилиндр.
ms.assetid: 43329d2f-50bb-46ea-85cb-22956d0df375
keywords:
- Функция Глуцилиндер OpenGL
topic_type:
- apiref
api_name:
- gluCylinder
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fd201d1ddd720501715d1ead08d94bab72f7b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661937"
---
# <a name="glucylinder-function"></a><span data-ttu-id="16aed-104">Функция Глуцилиндер</span><span class="sxs-lookup"><span data-stu-id="16aed-104">gluCylinder function</span></span>

<span data-ttu-id="16aed-105">Функция **глуцилиндер** рисует цилиндр.</span><span class="sxs-lookup"><span data-stu-id="16aed-105">The **gluCylinder** function draws a cylinder.</span></span>

## <a name="syntax"></a><span data-ttu-id="16aed-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16aed-106">Syntax</span></span>


```C++
void WINAPI gluCylinder(
   GLUquadric *qobj,
   GLdouble   baseRadius,
   GLdouble   topRadius,
   GLdouble   height,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a><span data-ttu-id="16aed-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="16aed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16aed-108">*кобж*</span><span class="sxs-lookup"><span data-stu-id="16aed-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="16aed-109">Объект куадрик (созданный с помощью [**глуневкуадрик**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="16aed-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="16aed-110">*басерадиус*</span><span class="sxs-lookup"><span data-stu-id="16aed-110">*baseRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="16aed-111">Радиус цилиндра по *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="16aed-111">The radius of the cylinder at *z* = 0.</span></span>

</dd> <dt>

<span data-ttu-id="16aed-112">*топрадиус*</span><span class="sxs-lookup"><span data-stu-id="16aed-112">*topRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="16aed-113">Радиус цилиндра по высоте от *z*  =  .</span><span class="sxs-lookup"><span data-stu-id="16aed-113">The radius of the cylinder at *z* = *height*.</span></span>

</dd> <dt>

<span data-ttu-id="16aed-114">*height*</span><span class="sxs-lookup"><span data-stu-id="16aed-114">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="16aed-115">Высота цилиндра.</span><span class="sxs-lookup"><span data-stu-id="16aed-115">The height of the cylinder.</span></span>

</dd> <dt>

<span data-ttu-id="16aed-116">*срезы*</span><span class="sxs-lookup"><span data-stu-id="16aed-116">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="16aed-117">Число подразделений вокруг оси z.</span><span class="sxs-lookup"><span data-stu-id="16aed-117">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="16aed-118">*стеки*</span><span class="sxs-lookup"><span data-stu-id="16aed-118">*stacks*</span></span> 
</dt> <dd>

<span data-ttu-id="16aed-119">Число подразделений вдоль оси z.</span><span class="sxs-lookup"><span data-stu-id="16aed-119">The number of subdivisions along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16aed-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16aed-120">Return value</span></span>

<span data-ttu-id="16aed-121">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="16aed-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16aed-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16aed-122">Remarks</span></span>

<span data-ttu-id="16aed-123">Функция **глуцилиндер** рисует цилиндр, ориентированный вдоль оси z.</span><span class="sxs-lookup"><span data-stu-id="16aed-123">The **gluCylinder** function draws a cylinder oriented along the z-axis.</span></span> <span data-ttu-id="16aed-124">Основание цилиндра помещается в *z* = 0, а верхняя *— по*  =  *высоте*.</span><span class="sxs-lookup"><span data-stu-id="16aed-124">The base of the cylinder is placed at *z* = 0, and the top at *z* = *height*.</span></span> <span data-ttu-id="16aed-125">Как и в сфере, цилиндр разбивается вокруг оси z на срезы, а вдоль оси z в стеки.</span><span class="sxs-lookup"><span data-stu-id="16aed-125">Like a sphere, a cylinder is subdivided around the z-axis into slices, and along the z-axis into stacks.</span></span>

<span data-ttu-id="16aed-126">Обратите внимание, что если *топрадиус* имеет значение 0, то эта подпрограммы создаст конус.</span><span class="sxs-lookup"><span data-stu-id="16aed-126">Note that if *topRadius* is set to zero, then this routine will generate a cone.</span></span>

<span data-ttu-id="16aed-127">Если для ориентации задано значение GLU \_ снаружи (с [**глукуадрикориентатион**](gluquadricorientation.md)), то все созданные нормали указываются на расстоянии от оси z.</span><span class="sxs-lookup"><span data-stu-id="16aed-127">If the orientation is set to GLU\_OUTSIDE (with [**gluQuadricOrientation**](gluquadricorientation.md)), then any generated normals point away from the z-axis.</span></span> <span data-ttu-id="16aed-128">В противном случае они указывают на ось z.</span><span class="sxs-lookup"><span data-stu-id="16aed-128">Otherwise, they point toward the z-axis.</span></span>

<span data-ttu-id="16aed-129">Если текстурирование включено (с [**глукуадриктекстуре**](gluquadrictexture.md)): координаты текстуры генерируются таким образом, что *t* перечисляются в диапазоне от 0,0 по *z* = 0 до 1,0 по *z*  =  -*высоте*;, а диапазоны — от 0,0 по положительной оси x, по 0,25 с положительной осью х, по 0,5 на отрицательной оси y, в 0,75 на отрицательной оси x и обратно в 1,0 по положительной оси y. </span><span class="sxs-lookup"><span data-stu-id="16aed-129">If texturing is turned on (with [**gluQuadricTexture**](gluquadrictexture.md)): texture coordinates are generated so that *t* ranges linearly from 0.0 at *z* = 0 to 1.0 at *z* = *height*; and *s* ranges from 0.0 at the positive y-axis, to 0.25 at the positive x-axis, to 0.5 at the negative y-axis, to 0.75 at the negative x-axis, and back to 1.0 at the positive y-axis.</span></span>

## <a name="requirements"></a><span data-ttu-id="16aed-130">Требования</span><span class="sxs-lookup"><span data-stu-id="16aed-130">Requirements</span></span>



| <span data-ttu-id="16aed-131">Требование</span><span class="sxs-lookup"><span data-stu-id="16aed-131">Requirement</span></span> | <span data-ttu-id="16aed-132">Значение</span><span class="sxs-lookup"><span data-stu-id="16aed-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="16aed-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="16aed-133">Minimum supported client</span></span><br/> | <span data-ttu-id="16aed-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="16aed-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="16aed-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="16aed-135">Minimum supported server</span></span><br/> | <span data-ttu-id="16aed-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="16aed-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="16aed-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="16aed-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="16aed-138"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="16aed-138"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="16aed-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="16aed-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="16aed-140"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16aed-140"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="16aed-141">DLL</span><span class="sxs-lookup"><span data-stu-id="16aed-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16aed-142"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16aed-142"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16aed-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16aed-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16aed-144">**глудиск**</span><span class="sxs-lookup"><span data-stu-id="16aed-144">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="16aed-145">**глуневкуадрик**</span><span class="sxs-lookup"><span data-stu-id="16aed-145">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="16aed-146">**глупартиалдиск**</span><span class="sxs-lookup"><span data-stu-id="16aed-146">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="16aed-147">**глукуадрикориентатион**</span><span class="sxs-lookup"><span data-stu-id="16aed-147">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="16aed-148">**глукуадриктекстуре**</span><span class="sxs-lookup"><span data-stu-id="16aed-148">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="16aed-149">**глусфере**</span><span class="sxs-lookup"><span data-stu-id="16aed-149">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





