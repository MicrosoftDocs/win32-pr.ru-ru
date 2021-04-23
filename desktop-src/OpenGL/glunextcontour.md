---
title: Функция Глунекстконтаур (GLU. h)
description: Функция Глунекстконтаур отмечает начало другого контура.
ms.assetid: 622cd631-3426-4206-9e23-af2a74343da5
keywords:
- Функция Глунекстконтаур OpenGL
topic_type:
- apiref
api_name:
- gluNextContour
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b798eba50205053c019e3e8d1708c9ed834e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415125"
---
# <a name="glunextcontour-function"></a><span data-ttu-id="171f8-104">Функция Глунекстконтаур</span><span class="sxs-lookup"><span data-stu-id="171f8-104">gluNextContour function</span></span>

<span data-ttu-id="171f8-105">\[Функция **глунекстконтаур** устарела и предоставляется только для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="171f8-105">\[The **gluNextContour** function is obsolete and is provided for backward compatibility only.</span></span> <span data-ttu-id="171f8-106">Функция **глунекстконтаур** сопоставляется с [**глутессендконтаур**](glutessendcontour.md) , за которым следует [**глутессбегинконтаур**](glutessbegincontour.md).\]</span><span class="sxs-lookup"><span data-stu-id="171f8-106">The **gluNextContour** function is mapped to [**gluTessEndContour**](glutessendcontour.md) followed by [**gluTessBeginContour**](glutessbegincontour.md).\]</span></span>

<span data-ttu-id="171f8-107">Функция **глунекстконтаур** отмечает начало другого контура.</span><span class="sxs-lookup"><span data-stu-id="171f8-107">The **gluNextContour** function marks the beginning of another contour.</span></span>

## <a name="syntax"></a><span data-ttu-id="171f8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="171f8-108">Syntax</span></span>


```C++
void WINAPI gluNextContour(
   GLUtesselator *tess,
   GLenum        type
);
```



## <a name="parameters"></a><span data-ttu-id="171f8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="171f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="171f8-110">*тесс*</span><span class="sxs-lookup"><span data-stu-id="171f8-110">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="171f8-111">Объект тесселяции (созданный с помощью [**глуневтесс**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="171f8-111">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="171f8-112">*type*</span><span class="sxs-lookup"><span data-stu-id="171f8-112">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="171f8-113">Тип определяемого контура.</span><span class="sxs-lookup"><span data-stu-id="171f8-113">The type of the contour being defined.</span></span> <span data-ttu-id="171f8-114">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="171f8-114">The following values are valid.</span></span>



| <span data-ttu-id="171f8-115">Значение</span><span class="sxs-lookup"><span data-stu-id="171f8-115">Value</span></span>                                                                                                                                                                | <span data-ttu-id="171f8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="171f8-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_EXTERIOR"></span><span id="glu_exterior"></span><dl> <span data-ttu-id="171f8-117"><dt>**\_наружный Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="171f8-117"><dt>**GLU\_EXTERIOR**</dt></span></span> </dl>           | <span data-ttu-id="171f8-118">Наружный контур определяет наружную границу многоугольника.</span><span class="sxs-lookup"><span data-stu-id="171f8-118">An exterior contour defines an exterior boundary of the polygon.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GLU_INTERIOR"></span><span id="glu_interior"></span><dl> <span data-ttu-id="171f8-119"><dt>**\_Внутренняя Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="171f8-119"><dt>**GLU\_INTERIOR**</dt></span></span> </dl>           | <span data-ttu-id="171f8-120">Внутренний контур определяет внутреннюю границу многоугольника (например, отверстие).</span><span class="sxs-lookup"><span data-stu-id="171f8-120">An interior contour defines an interior boundary of the polygon (such as a hole).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GLU_UNKNOWN"></span><span id="glu_unknown"></span><dl> <span data-ttu-id="171f8-121"><dt>**GLU \_ неизвестный**</dt></span><span class="sxs-lookup"><span data-stu-id="171f8-121"><dt>**GLU\_UNKNOWN**</dt></span></span> </dl>              | <span data-ttu-id="171f8-122">Библиотека анализирует неизвестный профиль, чтобы определить, является ли он внутренним или внешним.</span><span class="sxs-lookup"><span data-stu-id="171f8-122">An unknown contour is analyzed by the library to determine whether it is interior or exterior.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CCW__GLU_CW"></span><span id="glu_ccw__glu_cw"></span><dl> <span data-ttu-id="171f8-123"><dt>**GLU \_ CCW, Glu \_ во вт.**</dt></span><span class="sxs-lookup"><span data-stu-id="171f8-123"><dt>**GLU\_CCW, GLU\_CW**</dt></span></span> </dl> | <span data-ttu-id="171f8-124">Первый GLU, \_ определенный контуром CCW или Glu, \_ считается наружным.</span><span class="sxs-lookup"><span data-stu-id="171f8-124">The first GLU\_CCW or GLU\_CW contour defined is considered to be exterior.</span></span> <span data-ttu-id="171f8-125">Все остальные контуры считаются внешними, если они ориентированы в одном направлении (по часовой стрелке или против часовой стрелки) в качестве первого профиля, а также для внутренних, если они нет.</span><span class="sxs-lookup"><span data-stu-id="171f8-125">All other contours are considered to be exterior if they are oriented in the same direction (clockwise or counterclockwise) as the first contour, and interior if they are not.</span></span><br/> <span data-ttu-id="171f8-126">Если один профиль имеет тип GLU \_ CCW или Glu \_ во вт., то все эти профили должны иметь один и тот же тип (если они не равны, то все ы \_ CCW и Glu \_ во Вт будут изменены на GLU \_ Unknown).</span><span class="sxs-lookup"><span data-stu-id="171f8-126">If one contour is of type GLU\_CCW or GLU\_CW, then all contours must be of the same type (if they are not, then all GLU\_CCW and GLU\_CW contours will be changed to GLU\_UNKNOWN).</span></span> <span data-ttu-id="171f8-127">Обратите внимание, что между \_ типами профилей Glu CCW и Glu \_ во вт.</span><span class="sxs-lookup"><span data-stu-id="171f8-127">Note that there is no real difference between the GLU\_CCW and GLU\_CW contour types.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="171f8-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="171f8-128">Return value</span></span>

<span data-ttu-id="171f8-129">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="171f8-129">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="171f8-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="171f8-130">Remarks</span></span>

<span data-ttu-id="171f8-131">Используйте функцию **глунекстконтаур** для описания многоугольников с несколькими контурами.</span><span class="sxs-lookup"><span data-stu-id="171f8-131">Use the **gluNextContour** function to describe polygons with multiple contours.</span></span> <span data-ttu-id="171f8-132">После описания первого контура с помощью ряда вызовов [**глутессвертекс**](glutessvertex.md) вызов **глунекстконтаур** указывает, что предыдущий профиль завершен и что начинается следующий профиль.</span><span class="sxs-lookup"><span data-stu-id="171f8-132">After you describe the first contour through a series of [**gluTessVertex**](glutessvertex.md) calls, a **gluNextContour** call indicates that the previous contour is complete and that the next contour is about to begin.</span></span> <span data-ttu-id="171f8-133">Выполните еще одну серию вызовов **глутессвертекс** , чтобы описать новый профиль.</span><span class="sxs-lookup"><span data-stu-id="171f8-133">Perform another series of **gluTessVertex** calls to describe the new contour.</span></span> <span data-ttu-id="171f8-134">Повторите эту процедуру, пока не будут описаны все контуры.</span><span class="sxs-lookup"><span data-stu-id="171f8-134">Repeat this process until all contours have been described.</span></span>

<span data-ttu-id="171f8-135">Параметр *типа* определяет, какой тип контура следует за.</span><span class="sxs-lookup"><span data-stu-id="171f8-135">The *type* parameter defines what type of contour follows.</span></span>

<span data-ttu-id="171f8-136">Чтобы определить тип первого профиля, можно вызвать **глунекстконтаур** , прежде чем описать первый профиль.</span><span class="sxs-lookup"><span data-stu-id="171f8-136">To define the type of the first contour, you can call **gluNextContour** before describing the first contour.</span></span> <span data-ttu-id="171f8-137">Если не вызвать **глунекстконтаур** перед первым контуром, первый контур помечается как Glu \_ наружный.</span><span class="sxs-lookup"><span data-stu-id="171f8-137">If you do not call **gluNextContour** before the first contour, the first contour is marked GLU\_EXTERIOR.</span></span>

## <a name="examples"></a><span data-ttu-id="171f8-138">Примеры</span><span class="sxs-lookup"><span data-stu-id="171f8-138">Examples</span></span>

<span data-ttu-id="171f8-139">Вы можете описать грани четырехсторонней с треугольным отверстием в нем следующим образом:</span><span class="sxs-lookup"><span data-stu-id="171f8-139">You can describe a quadrilateral with a triangular hole in it as follows:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="171f8-140">Требования</span><span class="sxs-lookup"><span data-stu-id="171f8-140">Requirements</span></span>



| <span data-ttu-id="171f8-141">Требование</span><span class="sxs-lookup"><span data-stu-id="171f8-141">Requirement</span></span> | <span data-ttu-id="171f8-142">Значение</span><span class="sxs-lookup"><span data-stu-id="171f8-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="171f8-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="171f8-143">Minimum supported client</span></span><br/> | <span data-ttu-id="171f8-144">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="171f8-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="171f8-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="171f8-145">Minimum supported server</span></span><br/> | <span data-ttu-id="171f8-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="171f8-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="171f8-147">Заголовок</span><span class="sxs-lookup"><span data-stu-id="171f8-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="171f8-148"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="171f8-148"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="171f8-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="171f8-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="171f8-150"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="171f8-150"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="171f8-151">DLL</span><span class="sxs-lookup"><span data-stu-id="171f8-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="171f8-152"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="171f8-152"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="171f8-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="171f8-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="171f8-154">**глуневтесс**</span><span class="sxs-lookup"><span data-stu-id="171f8-154">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="171f8-155">**глутессбегинконтаур**</span><span class="sxs-lookup"><span data-stu-id="171f8-155">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="171f8-156">**глутессбегинполигон**</span><span class="sxs-lookup"><span data-stu-id="171f8-156">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="171f8-157">*глутесскаллбакк*</span><span class="sxs-lookup"><span data-stu-id="171f8-157">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="171f8-158">**глутессендконтаур**</span><span class="sxs-lookup"><span data-stu-id="171f8-158">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="171f8-159">**глутессвертекс**</span><span class="sxs-lookup"><span data-stu-id="171f8-159">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





