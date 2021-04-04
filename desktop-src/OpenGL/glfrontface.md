---
title: Функция Глфронтфаце (GL. h)
description: Функция Глфронтфаце определяет многоугольники с внешним и фоновым интерфейсом.
ms.assetid: 4087107c-99cd-4c26-92e3-8dc43633d51f
keywords:
- Функция Глфронтфаце OpenGL
topic_type:
- apiref
api_name:
- glFrontFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106fa40989f21e50eb738f1a218394e8e7e9b4bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989346"
---
# <a name="glfrontface-function"></a><span data-ttu-id="63a20-104">Функция Глфронтфаце</span><span class="sxs-lookup"><span data-stu-id="63a20-104">glFrontFace function</span></span>

<span data-ttu-id="63a20-105">Функция **глфронтфаце** определяет многоугольники с внешним и фоновым интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="63a20-105">The **glFrontFace** function defines front-facing and back-facing polygons.</span></span>

## <a name="syntax"></a><span data-ttu-id="63a20-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63a20-106">Syntax</span></span>


```C++
void WINAPI glFrontFace(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="63a20-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="63a20-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63a20-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="63a20-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="63a20-109">Ориентация внешних многоугольников.</span><span class="sxs-lookup"><span data-stu-id="63a20-109">The orientation of front-facing polygons.</span></span> <span data-ttu-id="63a20-110">\_Выводятся и \_ вызываемая оболочка CCW и GL.</span><span class="sxs-lookup"><span data-stu-id="63a20-110">GL\_CW and GL\_CCW are accepted.</span></span> <span data-ttu-id="63a20-111">Значение по умолчанию — GL \_ CCW.</span><span class="sxs-lookup"><span data-stu-id="63a20-111">The default value is GL\_CCW.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63a20-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63a20-112">Return value</span></span>

<span data-ttu-id="63a20-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="63a20-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="63a20-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="63a20-114">Error codes</span></span>

<span data-ttu-id="63a20-115">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="63a20-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="63a20-116">Имя</span><span class="sxs-lookup"><span data-stu-id="63a20-116">Name</span></span>                                                                                                  | <span data-ttu-id="63a20-117">Значение</span><span class="sxs-lookup"><span data-stu-id="63a20-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="63a20-118"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="63a20-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="63a20-119">*режим* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="63a20-119">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="63a20-120"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="63a20-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="63a20-121">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="63a20-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="63a20-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63a20-122">Remarks</span></span>

<span data-ttu-id="63a20-123">В сцене, полностью состоящей из непрозрачных замкнутых областей, фоновые многоугольники никогда не отображаются.</span><span class="sxs-lookup"><span data-stu-id="63a20-123">In a scene composed entirely of opaque closed surfaces, back-facing polygons are never visible.</span></span> <span data-ttu-id="63a20-124">Устранение этих невидимых многоугольников является очевидным преимуществом ускорения отрисовки изображения.</span><span class="sxs-lookup"><span data-stu-id="63a20-124">Eliminating these invisible polygons has the obvious benefit of speeding up the rendering of the image.</span></span> <span data-ttu-id="63a20-125">Вы включаете и отключаете возможность удаления многоугольников с обратным переходом с помощью [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md) , используя аргумент « \_ лицо для отбора GL \_ ».</span><span class="sxs-lookup"><span data-stu-id="63a20-125">You enable and disable elimination of back-facing polygons with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) using argument GL\_CULL\_FACE.</span></span>

<span data-ttu-id="63a20-126">Проекция многоугольника в координаты окна называется поворотом по часовой стрелке, если мнимый объект, следующий за путем от первой вершины, второй вершиной и т. д., в последнюю вершину, и, наконец, обратно в первую вершину, перемещается в направлении по часовой стрелке относительно внутренней части многоугольника.</span><span class="sxs-lookup"><span data-stu-id="63a20-126">The projection of a polygon to window coordinates is said to have clockwise winding if an imaginary object following the path from its first vertex, its second vertex, and so on, to its last vertex, and finally back to its first vertex, moves in a clockwise direction about the interior of the polygon.</span></span> <span data-ttu-id="63a20-127">Поворот многоугольника считается против часовой стрелки, если объект мнимой стороны, следующий за тем же путем, перемещается в направлении против часовой стрелки относительно внутренней части многоугольника.</span><span class="sxs-lookup"><span data-stu-id="63a20-127">The polygon's winding is said to be counterclockwise if the imaginary object following the same path moves in a counterclockwise direction about the interior of the polygon.</span></span> <span data-ttu-id="63a20-128">Функция **глфронтфаце** указывает, являются ли многоугольники с поворотом по часовой стрелке в координатах окна или при повороте против часовой стрелки в окнах.</span><span class="sxs-lookup"><span data-stu-id="63a20-128">The **glFrontFace** function specifies whether polygons with clockwise winding in window coordinates, or counterclockwise winding in window coordinates, are taken to be front-facing.</span></span> <span data-ttu-id="63a20-129">Передача GL \_ в *режим* с указанием модели "CCW" выбирает многоугольники в качестве внешнего взаимодействия. GL \_ по часовой стрелке выбирает многоугольники в качестве внешнего интерфейса.</span><span class="sxs-lookup"><span data-stu-id="63a20-129">Passing GL\_CCW to *mode* selects counterclockwise polygons as front-facing; GL\_CW selects clockwise polygons as front-facing.</span></span> <span data-ttu-id="63a20-130">По умолчанию многоугольники в противном случае переводятся в внешний вид.</span><span class="sxs-lookup"><span data-stu-id="63a20-130">By default, counterclockwise polygons are taken to be front-facing.</span></span>

<span data-ttu-id="63a20-131">Следующая функция получает сведения о **глфронтфаце**:</span><span class="sxs-lookup"><span data-stu-id="63a20-131">The following function retrieves information about **glFrontface**:</span></span>

<span data-ttu-id="63a20-132">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ Передняя \_ сторона GL</span><span class="sxs-lookup"><span data-stu-id="63a20-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FRONT\_FACE</span></span>

## <a name="requirements"></a><span data-ttu-id="63a20-133">Требования</span><span class="sxs-lookup"><span data-stu-id="63a20-133">Requirements</span></span>



| <span data-ttu-id="63a20-134">Требование</span><span class="sxs-lookup"><span data-stu-id="63a20-134">Requirement</span></span> | <span data-ttu-id="63a20-135">Значение</span><span class="sxs-lookup"><span data-stu-id="63a20-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63a20-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63a20-136">Minimum supported client</span></span><br/> | <span data-ttu-id="63a20-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="63a20-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="63a20-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63a20-138">Minimum supported server</span></span><br/> | <span data-ttu-id="63a20-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="63a20-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="63a20-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="63a20-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="63a20-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="63a20-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="63a20-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="63a20-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="63a20-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63a20-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="63a20-144">DLL</span><span class="sxs-lookup"><span data-stu-id="63a20-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63a20-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63a20-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63a20-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63a20-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63a20-147">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="63a20-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="63a20-148">**глкуллфаце**</span><span class="sxs-lookup"><span data-stu-id="63a20-148">**glCullFace**</span></span>](glcullface.md)
</dt> <dt>

[<span data-ttu-id="63a20-149">**глдисабле**</span><span class="sxs-lookup"><span data-stu-id="63a20-149">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="63a20-150">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="63a20-150">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="63a20-151">**гленд**</span><span class="sxs-lookup"><span data-stu-id="63a20-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="63a20-152">**глжет**</span><span class="sxs-lookup"><span data-stu-id="63a20-152">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="63a20-153">**гллигхтмодел**</span><span class="sxs-lookup"><span data-stu-id="63a20-153">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





