---
title: Функция Глхинт (GL. h)
description: Функция Глхинт задает указания, относящиеся к реализации.
ms.assetid: 6d03e107-321a-45ee-9ce7-25fa9cab32d9
keywords:
- Функция Глхинт OpenGL
topic_type:
- apiref
api_name:
- glHint
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2772c76868c741660486184e5ab51bd193d3667a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135431"
---
# <a name="glhint-function"></a><span data-ttu-id="78b66-104">Функция Глхинт</span><span class="sxs-lookup"><span data-stu-id="78b66-104">glHint function</span></span>

<span data-ttu-id="78b66-105">Функция **глхинт** задает указания, относящиеся к реализации.</span><span class="sxs-lookup"><span data-stu-id="78b66-105">The **glHint** function specifies implementation-specific hints.</span></span>

## <a name="syntax"></a><span data-ttu-id="78b66-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78b66-106">Syntax</span></span>


```C++
void WINAPI glHint(
   GLenum target,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="78b66-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="78b66-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78b66-108">*target*</span><span class="sxs-lookup"><span data-stu-id="78b66-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="78b66-109">Символьная константа, указывающая поведение для управления.</span><span class="sxs-lookup"><span data-stu-id="78b66-109">A symbolic constant indicating the behavior to be controlled.</span></span> <span data-ttu-id="78b66-110">Принимаются следующие символьные константы, а также предлагаемая семантика.</span><span class="sxs-lookup"><span data-stu-id="78b66-110">The following symbolic constants, along with suggested semantics, are accepted.</span></span>



| <span data-ttu-id="78b66-111">Значение</span><span class="sxs-lookup"><span data-stu-id="78b66-111">Value</span></span>                                                                                                                                                                                                              | <span data-ttu-id="78b66-112">Значение</span><span class="sxs-lookup"><span data-stu-id="78b66-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_HINT"></span><span id="gl_fog_hint"></span><dl> <span data-ttu-id="78b66-113"><dt>**\_Указание тумана GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="78b66-113"><dt>**GL\_FOG\_HINT**</dt></span></span> </dl>                                                           | <span data-ttu-id="78b66-114">Указывает точность вычисления тумана.</span><span class="sxs-lookup"><span data-stu-id="78b66-114">Indicates the accuracy of fog calculation.</span></span> <span data-ttu-id="78b66-115">Если при вычислении тумана на пиксельных координатах не поддерживается эффективное использование в реализации OpenGL, подсказка GL \_ не \_ или \_ самая быстрая в ГК может привести к вычислению эффектов тумана на основе вершин.</span><span class="sxs-lookup"><span data-stu-id="78b66-115">If per-pixel fog calculation is not efficiently supported by the OpenGL implementation, hinting GL\_DONT\_CARE or GL\_FASTEST can result in per-vertex calculation of fog effects.</span></span><br/>                                                                          |
| <span id="GL_LINE_SMOOTH_HINT"></span><span id="gl_line_smooth_hint"></span><dl> <span data-ttu-id="78b66-116"><dt>**\_ \_ Указание СГЛАЖИВАНИЯ строки \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="78b66-116"><dt>**GL\_LINE\_SMOOTH\_HINT**</dt></span></span> </dl>                                  | <span data-ttu-id="78b66-117">Указывает качество выборки сглаженных линий.</span><span class="sxs-lookup"><span data-stu-id="78b66-117">Indicates the sampling quality of antialiased lines.</span></span> <span data-ttu-id="78b66-118">Указание GL \_ ницест может привести к созданию большего количества фрагментов пикселей во время растрирования, если применяется более крупная функция фильтра.</span><span class="sxs-lookup"><span data-stu-id="78b66-118">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                               |
| <span id="GL_PERSPECTIVE_CORRECTION_HINT"></span><span id="gl_perspective_correction_hint"></span><dl> <span data-ttu-id="78b66-119"><dt>**\_ \_ Указание корректировки главной точки \_**</dt></span><span class="sxs-lookup"><span data-stu-id="78b66-119"><dt>**GL\_PERSPECTIVE\_CORRECTION\_HINT**</dt></span></span> </dl> | <span data-ttu-id="78b66-120">Указывает качество интерполяции цвета и координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="78b66-120">Indicates the quality of color and texture coordinate interpolation.</span></span> <span data-ttu-id="78b66-121">Если в реализации OpenGL неэффективно поддерживается интерполяция параметров с исправленной перспективой, то указание главной \_ неной \_ осторожности или \_ самой быстрой ГК может привести к простой линейной интерполяции цветов и/или координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="78b66-121">If perspective-corrected parameter interpolation is not efficiently supported by the OpenGL implementation, hinting GL\_DONT\_CARE or GL\_FASTEST can result in simple linear interpolation of colors and/or texture coordinates.</span></span><br/> |
| <span id="GL_POINT_SMOOTH_HINT"></span><span id="gl_point_smooth_hint"></span><dl> <span data-ttu-id="78b66-122"><dt>**\_ \_ гладкая \_ Подсказка для точки GL**</dt></span><span class="sxs-lookup"><span data-stu-id="78b66-122"><dt>**GL\_POINT\_SMOOTH\_HINT**</dt></span></span> </dl>                               | <span data-ttu-id="78b66-123">Указывает качество выборки точек сглаживания.</span><span class="sxs-lookup"><span data-stu-id="78b66-123">Indicates the sampling quality of antialiased points.</span></span> <span data-ttu-id="78b66-124">Указание GL \_ ницест может привести к созданию большего количества фрагментов пикселей во время растрирования, если применяется более крупная функция фильтра.</span><span class="sxs-lookup"><span data-stu-id="78b66-124">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                              |
| <span id="GL_POLYGON_SMOOTH_HINT"></span><span id="gl_polygon_smooth_hint"></span><dl> <span data-ttu-id="78b66-125"><dt>**\_ \_ Указание гладкого МНОГОУГОЛЬНИКа GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="78b66-125"><dt>**GL\_POLYGON\_SMOOTH\_HINT**</dt></span></span> </dl>                         | <span data-ttu-id="78b66-126">Указывает качество выборки для многоугольников с сглаживанием.</span><span class="sxs-lookup"><span data-stu-id="78b66-126">Indicates the sampling quality of antialiased polygons.</span></span> <span data-ttu-id="78b66-127">Указание GL \_ ницест может привести к созданию большего количества фрагментов пикселей во время растрирования, если применяется более крупная функция фильтра.</span><span class="sxs-lookup"><span data-stu-id="78b66-127">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="78b66-128">*mode*</span><span class="sxs-lookup"><span data-stu-id="78b66-128">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="78b66-129">Символьная константа, указывающая требуемое поведение.</span><span class="sxs-lookup"><span data-stu-id="78b66-129">A symbolic constant indicating the desired behavior.</span></span> <span data-ttu-id="78b66-130">Допустимы следующие символьные константы.</span><span class="sxs-lookup"><span data-stu-id="78b66-130">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="78b66-131">Значение</span><span class="sxs-lookup"><span data-stu-id="78b66-131">Value</span></span>                                                                                                                                                       | <span data-ttu-id="78b66-132">Значение</span><span class="sxs-lookup"><span data-stu-id="78b66-132">Meaning</span></span>                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="GL_FASTEST"></span><span id="gl_fastest"></span><dl> <span data-ttu-id="78b66-133"><dt>**Быстрая по ГК \_**</dt></span><span class="sxs-lookup"><span data-stu-id="78b66-133"><dt>**GL\_FASTEST**</dt></span></span> </dl>        | <span data-ttu-id="78b66-134">Следует выбрать наиболее эффективный вариант.</span><span class="sxs-lookup"><span data-stu-id="78b66-134">The most efficient option should be chosen.</span></span><br/>                    |
| <span id="GL_NICEST"></span><span id="gl_nicest"></span><dl> <span data-ttu-id="78b66-135"><dt>**\_НИЦЕСТ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="78b66-135"><dt>**GL\_NICEST**</dt></span></span> </dl>           | <span data-ttu-id="78b66-136">Необходимо выбрать наиболее правильное или наивысшее качество.</span><span class="sxs-lookup"><span data-stu-id="78b66-136">The most correct, or highest quality, option should be chosen.</span></span><br/> |
| <span id="GL_DONT_CARE"></span><span id="gl_dont_care"></span><dl> <span data-ttu-id="78b66-137"><dt>**\_Неа \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="78b66-137"><dt>**GL\_DONT\_CARE**</dt></span></span> </dl> | <span data-ttu-id="78b66-138">У клиента нет предпочтений.</span><span class="sxs-lookup"><span data-stu-id="78b66-138">The client doesn't have a preference.</span></span><br/>                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78b66-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78b66-139">Return value</span></span>

<span data-ttu-id="78b66-140">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="78b66-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="78b66-141">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="78b66-141">Error codes</span></span>

<span data-ttu-id="78b66-142">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="78b66-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="78b66-143">Имя</span><span class="sxs-lookup"><span data-stu-id="78b66-143">Name</span></span>                                                                                                  | <span data-ttu-id="78b66-144">Значение</span><span class="sxs-lookup"><span data-stu-id="78b66-144">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="78b66-145"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="78b66-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="78b66-146">*целевой объект* или *режим* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="78b66-146">*target* or *mode* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="78b66-147"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="78b66-147"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="78b66-148">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="78b66-148">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="78b66-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78b66-149">Remarks</span></span>

<span data-ttu-id="78b66-150">При наличии места для интерпретации можно управлять определенными аспектами поведения OpenGL с помощью подсказок.</span><span class="sxs-lookup"><span data-stu-id="78b66-150">When there is room for interpretation, you can control certain aspects of OpenGL behavior with hints.</span></span> <span data-ttu-id="78b66-151">Укажите указание с двумя аргументами.</span><span class="sxs-lookup"><span data-stu-id="78b66-151">You specify a hint with two arguments.</span></span> <span data-ttu-id="78b66-152">Параметр *Target* представляет собой символьную константу, указывающую поведение, которое необходимо контролировать, а *режим* — еще одна символьная константа, указывающая требуемое поведение.</span><span class="sxs-lookup"><span data-stu-id="78b66-152">The *target* parameter is a symbolic constant indicating the behavior to be controlled, and *mode* is another symbolic constant indicating the desired behavior.</span></span>

<span data-ttu-id="78b66-153">Хотя аспекты реализации, которые можно указывать, хорошо определены, интерпретация подсказок зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="78b66-153">Though the implementation aspects that can be hinted are well defined, the interpretation of the hints depends on the implementation.</span></span>

<span data-ttu-id="78b66-154">Функцию **глхинт** можно игнорировать.</span><span class="sxs-lookup"><span data-stu-id="78b66-154">The **glHint** function can be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="78b66-155">Требования</span><span class="sxs-lookup"><span data-stu-id="78b66-155">Requirements</span></span>



| <span data-ttu-id="78b66-156">Требование</span><span class="sxs-lookup"><span data-stu-id="78b66-156">Requirement</span></span> | <span data-ttu-id="78b66-157">Значение</span><span class="sxs-lookup"><span data-stu-id="78b66-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78b66-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78b66-158">Minimum supported client</span></span><br/> | <span data-ttu-id="78b66-159">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="78b66-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="78b66-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78b66-160">Minimum supported server</span></span><br/> | <span data-ttu-id="78b66-161">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="78b66-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="78b66-162">Заголовок</span><span class="sxs-lookup"><span data-stu-id="78b66-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="78b66-163"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="78b66-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="78b66-164">Библиотека</span><span class="sxs-lookup"><span data-stu-id="78b66-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="78b66-165"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78b66-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="78b66-166">DLL</span><span class="sxs-lookup"><span data-stu-id="78b66-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78b66-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78b66-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78b66-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78b66-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78b66-169">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="78b66-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="78b66-170">**гленд**</span><span class="sxs-lookup"><span data-stu-id="78b66-170">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





