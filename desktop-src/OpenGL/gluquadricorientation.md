---
title: Функция Глукуадрикориентатион (GLU. h)
description: Функция Глукуадрикориентатион Указывает ориентацию внутри или снаружи для куадрикс.
ms.assetid: 4e3fc6d3-5a39-455b-bd24-8eb497333096
keywords:
- Функция Глукуадрикориентатион OpenGL
topic_type:
- apiref
api_name:
- gluQuadricOrientation
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05ffb1eeff199297943e678783731a26a38092a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800994"
---
# <a name="gluquadricorientation-function"></a><span data-ttu-id="fb967-104">Функция Глукуадрикориентатион</span><span class="sxs-lookup"><span data-stu-id="fb967-104">gluQuadricOrientation function</span></span>

<span data-ttu-id="fb967-105">Функция **глукуадрикориентатион** Указывает ориентацию внутри или снаружи для куадрикс.</span><span class="sxs-lookup"><span data-stu-id="fb967-105">The **gluQuadricOrientation** function specifies inside or outside orientation for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb967-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb967-106">Syntax</span></span>


```C++
void WINAPI gluQuadricOrientation(
   GLUquadric *quadObject,
   GLenum     orientation
);
```



## <a name="parameters"></a><span data-ttu-id="fb967-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb967-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb967-108">*куадобжект*</span><span class="sxs-lookup"><span data-stu-id="fb967-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="fb967-109">Объект куадрик (созданный с помощью [**глуневкуадрик**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="fb967-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="fb967-110">*orientation*</span><span class="sxs-lookup"><span data-stu-id="fb967-110">*orientation*</span></span> 
</dt> <dd>

<span data-ttu-id="fb967-111">Желаемая ориентация.</span><span class="sxs-lookup"><span data-stu-id="fb967-111">The desired orientation.</span></span> <span data-ttu-id="fb967-112">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="fb967-112">The following values are valid.</span></span>



| <span data-ttu-id="fb967-113">Значение</span><span class="sxs-lookup"><span data-stu-id="fb967-113">Value</span></span>                                                                                                                                                   | <span data-ttu-id="fb967-114">Значение</span><span class="sxs-lookup"><span data-stu-id="fb967-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="GLU_OUTSIDE"></span><span id="glu_outside"></span><dl> <span data-ttu-id="fb967-115"><dt>**GLU \_ снаружи**</dt></span><span class="sxs-lookup"><span data-stu-id="fb967-115"><dt>**GLU\_OUTSIDE**</dt></span></span> </dl> | <span data-ttu-id="fb967-116">Нарисуйте куадрикс с обычными, указывающими наружу.</span><span class="sxs-lookup"><span data-stu-id="fb967-116">Draw quadrics with normals pointing outward.</span></span> <span data-ttu-id="fb967-117">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fb967-117">This is the default value.</span></span><br/> |
| <span id="GLU_INSIDE"></span><span id="glu_inside"></span><dl> <span data-ttu-id="fb967-118"><dt>**GLU \_ внутри**</dt></span><span class="sxs-lookup"><span data-stu-id="fb967-118"><dt>**GLU\_INSIDE**</dt></span></span> </dl>    | <span data-ttu-id="fb967-119">Нарисуйте куадрикс с обычными, указывающими.</span><span class="sxs-lookup"><span data-stu-id="fb967-119">Draw quadrics with normals pointing inward.</span></span><br/>                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb967-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb967-120">Return value</span></span>

<span data-ttu-id="fb967-121">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="fb967-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb967-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb967-122">Remarks</span></span>

<span data-ttu-id="fb967-123">Функция **глукуадрикориентатион** указывает, какой вид ориентации требуется для куадрикс, отображаемого с помощью **куадобжект**.</span><span class="sxs-lookup"><span data-stu-id="fb967-123">The **gluQuadricOrientation** function specifies what kind of orientation is desired for quadrics rendered with **quadObject**.</span></span> <span data-ttu-id="fb967-124">Интерпретация наружной и обратной части зависит от прорисовки куадрик.</span><span class="sxs-lookup"><span data-stu-id="fb967-124">The interpretation of outward and inward depends on the quadric being drawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb967-125">Требования</span><span class="sxs-lookup"><span data-stu-id="fb967-125">Requirements</span></span>



| <span data-ttu-id="fb967-126">Требование</span><span class="sxs-lookup"><span data-stu-id="fb967-126">Requirement</span></span> | <span data-ttu-id="fb967-127">Значение</span><span class="sxs-lookup"><span data-stu-id="fb967-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fb967-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb967-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fb967-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fb967-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="fb967-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb967-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fb967-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fb967-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fb967-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fb967-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb967-133"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb967-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="fb967-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fb967-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb967-135"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb967-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fb967-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fb967-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb967-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb967-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb967-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb967-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb967-139">**глуневкуадрик**</span><span class="sxs-lookup"><span data-stu-id="fb967-139">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="fb967-140">**глукуадрикдравстиле**</span><span class="sxs-lookup"><span data-stu-id="fb967-140">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="fb967-141">**глукуадрикнормалс**</span><span class="sxs-lookup"><span data-stu-id="fb967-141">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="fb967-142">**глукуадриктекстуре**</span><span class="sxs-lookup"><span data-stu-id="fb967-142">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





