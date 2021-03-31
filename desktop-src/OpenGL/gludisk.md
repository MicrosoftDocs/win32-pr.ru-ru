---
title: Функция Глудиск (GLU. h)
description: Функция Глудиск рисует диск.
ms.assetid: c9260621-930d-47dd-a046-30895779473b
keywords:
- Функция Глудиск OpenGL
topic_type:
- apiref
api_name:
- gluDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9a9e8b547790049c93360f060e944aafcea4511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071592"
---
# <a name="gludisk-function"></a><span data-ttu-id="4e615-104">Функция Глудиск</span><span class="sxs-lookup"><span data-stu-id="4e615-104">gluDisk function</span></span>

<span data-ttu-id="4e615-105">Функция **глудиск** рисует диск.</span><span class="sxs-lookup"><span data-stu-id="4e615-105">The **gluDisk** function draws a disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e615-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e615-106">Syntax</span></span>


```C++
void WINAPI gluDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops
);
```



## <a name="parameters"></a><span data-ttu-id="4e615-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e615-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e615-108">*кобж*</span><span class="sxs-lookup"><span data-stu-id="4e615-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="4e615-109">Объект куадрик (созданный с помощью [**глуневкуадрик**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="4e615-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="4e615-110">*иннеррадиус*</span><span class="sxs-lookup"><span data-stu-id="4e615-110">*innerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="4e615-111">Внутренний радиус диска (может равняться нулю).</span><span class="sxs-lookup"><span data-stu-id="4e615-111">The inner radius of the disk (may be zero).</span></span>

</dd> <dt>

<span data-ttu-id="4e615-112">*аутеррадиус*</span><span class="sxs-lookup"><span data-stu-id="4e615-112">*outerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="4e615-113">Внешний радиус диска.</span><span class="sxs-lookup"><span data-stu-id="4e615-113">The outer radius of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="4e615-114">*срезы*</span><span class="sxs-lookup"><span data-stu-id="4e615-114">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="4e615-115">Число подразделений вокруг оси z.</span><span class="sxs-lookup"><span data-stu-id="4e615-115">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="4e615-116">*бираются*</span><span class="sxs-lookup"><span data-stu-id="4e615-116">*loops*</span></span> 
</dt> <dd>

<span data-ttu-id="4e615-117">Количество концентрических колец относительно источника, в который делится диск.</span><span class="sxs-lookup"><span data-stu-id="4e615-117">The number of concentric rings about the origin into which the disk is subdivided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e615-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e615-118">Return value</span></span>

<span data-ttu-id="4e615-119">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4e615-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e615-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e615-120">Remarks</span></span>

<span data-ttu-id="4e615-121">Функция **глудиск** визуализирует диск на плоскости *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="4e615-121">The **gluDisk** function renders a disk on the *z* = 0 plane.</span></span> <span data-ttu-id="4e615-122">Диск имеет радиус *аутеррадиус* и содержит концентрические циклическое отверстие с радиусом *иннеррадиус*.</span><span class="sxs-lookup"><span data-stu-id="4e615-122">The disk has a radius of *outerRadius*, and contains a concentric circular hole with a radius of *innerRadius*.</span></span> <span data-ttu-id="4e615-123">Если *иннеррадиус* имеет значение 0, отверстие не создается.</span><span class="sxs-lookup"><span data-stu-id="4e615-123">If *innerRadius* is 0, then no hole is generated.</span></span> <span data-ttu-id="4e615-124">Диск разделяется вокруг оси z на срезы (например, срезы пиццы), а также о оси z в кольцах (как указано *срезами* и *циклами* соответственно).</span><span class="sxs-lookup"><span data-stu-id="4e615-124">The disk is subdivided around the z-axis into slices (like pizza slices) and also about the z-axis into rings (as specified by *slices* and *loops*, respectively).</span></span>

<span data-ttu-id="4e615-125">В отношении ориентации положительная *z*-сторона диска считается *внешней* (см. [**глукуадрикориентатион**](gluquadricorientation.md)).</span><span class="sxs-lookup"><span data-stu-id="4e615-125">With respect to orientation, the positive *z*-side of the disk is considered to be *outside* (see [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span> <span data-ttu-id="4e615-126">Это означает, что если для ориентации задано значение GLU \_ снаружи, то все создаваемые нормали указываются вдоль положительной оси z.</span><span class="sxs-lookup"><span data-stu-id="4e615-126">This means that if the orientation is set to GLU\_OUTSIDE, then any normals generated point along the positive z-axis.</span></span>

<span data-ttu-id="4e615-127">Если текстурирование включено (с [**глукуадриктекстуре**](gluquadrictexture.md)), координаты текстуры создаются линейно, так, где *r*  =  *аутеррадиус*, значение в (*r*, 0, 0) равно (1, 0,5); в (0, *r*, 0) оно равно (0,5, 1); в (-*r*, 0, 0) он равен (0, 0,5), а в (0,-*r*, 0) — (0,5, 0).</span><span class="sxs-lookup"><span data-stu-id="4e615-127">If texturing is turned on (with [**gluQuadricTexture**](gluquadrictexture.md)), texture coordinates are generated linearly such that where *r* = *outerRadius*, the value at (*r*, 0, 0) is (1, 0.5); at (0, *r*, 0) it is (0.5, 1); at (-*r*, 0, 0) it is (0, 0.5); and at (0, -*r*, 0) it is (0.5, 0).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e615-128">Требования</span><span class="sxs-lookup"><span data-stu-id="4e615-128">Requirements</span></span>



| <span data-ttu-id="4e615-129">Требование</span><span class="sxs-lookup"><span data-stu-id="4e615-129">Requirement</span></span> | <span data-ttu-id="4e615-130">Значение</span><span class="sxs-lookup"><span data-stu-id="4e615-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4e615-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e615-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4e615-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4e615-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4e615-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e615-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4e615-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4e615-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4e615-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4e615-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e615-136"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e615-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="4e615-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4e615-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="4e615-138"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e615-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4e615-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4e615-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e615-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e615-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e615-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e615-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e615-142">**глуцилиндер**</span><span class="sxs-lookup"><span data-stu-id="4e615-142">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="4e615-143">**глуневкуадрик**</span><span class="sxs-lookup"><span data-stu-id="4e615-143">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="4e615-144">**глупартиалдиск**</span><span class="sxs-lookup"><span data-stu-id="4e615-144">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="4e615-145">**глукуадрикориентатион**</span><span class="sxs-lookup"><span data-stu-id="4e615-145">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="4e615-146">**глукуадриктекстуре**</span><span class="sxs-lookup"><span data-stu-id="4e615-146">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="4e615-147">**глусфере**</span><span class="sxs-lookup"><span data-stu-id="4e615-147">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





