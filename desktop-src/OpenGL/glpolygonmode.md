---
title: Функция Глполигонмоде (GL. h)
description: Функция Глполигонмоде выбирает режим растрирования многоугольника.
ms.assetid: d8781bae-e78c-40fb-9f33-c742c70ebda1
keywords:
- Функция Глполигонмоде OpenGL
topic_type:
- apiref
api_name:
- glPolygonMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23d133243c1655432842a939b8da0f3a981fdffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661987"
---
# <a name="glpolygonmode-function"></a><span data-ttu-id="fe64c-104">Функция Глполигонмоде</span><span class="sxs-lookup"><span data-stu-id="fe64c-104">glPolygonMode function</span></span>

<span data-ttu-id="fe64c-105">Функция **глполигонмоде** выбирает режим растрирования многоугольника.</span><span class="sxs-lookup"><span data-stu-id="fe64c-105">The **glPolygonMode** function selects a polygon rasterization mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe64c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe64c-106">Syntax</span></span>


```C++
void WINAPI glPolygonMode(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="fe64c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe64c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe64c-108">*личным*</span><span class="sxs-lookup"><span data-stu-id="fe64c-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="fe64c-109">Многоугольники, к которым применяется *режим* .</span><span class="sxs-lookup"><span data-stu-id="fe64c-109">The polygons that *mode* applies to.</span></span> <span data-ttu-id="fe64c-110">Должен быть GL \_ спереди для внешних многоугольников, GL \_ для фоновых многоугольников или GL \_ спереди \_ и \_ обратно для внешних и задних многоугольников.</span><span class="sxs-lookup"><span data-stu-id="fe64c-110">Must be GL\_FRONT for front-facing polygons, GL\_BACK for back-facing polygons, or GL\_FRONT\_AND\_BACK for front- and back-facing polygons.</span></span>

</dd> <dt>

<span data-ttu-id="fe64c-111">*mode*</span><span class="sxs-lookup"><span data-stu-id="fe64c-111">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="fe64c-112">Способ растрирования многоугольников.</span><span class="sxs-lookup"><span data-stu-id="fe64c-112">The way polygons will be rasterized.</span></span> <span data-ttu-id="fe64c-113">Определены следующие режимы, которые можно указать в *режиме*.</span><span class="sxs-lookup"><span data-stu-id="fe64c-113">The following modes are defined and can be specified in *mode*.</span></span> <span data-ttu-id="fe64c-114">По умолчанию используется \_ Заливка GL для внешних и задних многоугольников.</span><span class="sxs-lookup"><span data-stu-id="fe64c-114">The default is GL\_FILL for both front- and back-facing polygons.</span></span>



| <span data-ttu-id="fe64c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="fe64c-115">Value</span></span>                                                                                                                                          | <span data-ttu-id="fe64c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fe64c-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINT"></span><span id="gl_point"></span><dl> <span data-ttu-id="fe64c-117"><dt>**\_точка GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fe64c-117"><dt>**GL\_POINT**</dt></span></span> </dl> | <span data-ttu-id="fe64c-118">Вершины многоугольников, помеченные как начало граничного края, рисуются как точки.</span><span class="sxs-lookup"><span data-stu-id="fe64c-118">Polygon vertices that are marked as the start of a boundary edge are drawn as points.</span></span> <span data-ttu-id="fe64c-119">Точечные атрибуты, такие как \_ Размер точки главной книги \_ и точка GL, \_ \_ гладко управляют растрирование точек.</span><span class="sxs-lookup"><span data-stu-id="fe64c-119">Point attributes such as GL\_POINT\_SIZE and GL\_POINT\_SMOOTH control the rasterization of the points.</span></span> <span data-ttu-id="fe64c-120">Атрибуты растрирования многоугольников, отличные от \_ режима "Многоугольник" \_ , не действуют.</span><span class="sxs-lookup"><span data-stu-id="fe64c-120">Polygon rasterization attributes other than GL\_POLYGON\_MODE have no effect.</span></span><br/>                                                                                                                                                    |
| <span id="GL_LINE"></span><span id="gl_line"></span><dl> <span data-ttu-id="fe64c-121"><dt>**\_строка GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fe64c-121"><dt>**GL\_LINE**</dt></span></span> </dl>    | <span data-ttu-id="fe64c-122">Границы границ многоугольника рисуются в виде линейных сегментов.</span><span class="sxs-lookup"><span data-stu-id="fe64c-122">Boundary edges of the polygon are drawn as line segments.</span></span> <span data-ttu-id="fe64c-123">Они рассматриваются как сегменты Соединенных линий для стипплинг строк. Счетчик и шаблон строки стиппле не сбрасываются между сегментами (см. [**гллинестиппле**](gllinestipple.md)).</span><span class="sxs-lookup"><span data-stu-id="fe64c-123">They are treated as connected line segments for line stippling; the line stipple counter and pattern are not reset between segments (see [**glLineStipple**](gllinestipple.md)).</span></span> <span data-ttu-id="fe64c-124">Такие атрибуты линии, как \_ « \_ толщина линии GL» и «линия GL» \_ \_ , контролируют растрирование линий.</span><span class="sxs-lookup"><span data-stu-id="fe64c-124">Line attributes such as GL\_LINE\_WIDTH and GL\_LINE\_SMOOTH control the rasterization of the lines.</span></span> <span data-ttu-id="fe64c-125">Атрибуты растрирования многоугольников, отличные от \_ режима "Многоугольник" \_ , не действуют.</span><span class="sxs-lookup"><span data-stu-id="fe64c-125">Polygon rasterization attributes other than GL\_POLYGON\_MODE have no effect.</span></span><br/> |
| <span id="GL_FILL"></span><span id="gl_fill"></span><dl> <span data-ttu-id="fe64c-126"><dt>**\_Заливка GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fe64c-126"><dt>**GL\_FILL**</dt></span></span> </dl>    | <span data-ttu-id="fe64c-127">Внутренняя часть многоугольника заполнена.</span><span class="sxs-lookup"><span data-stu-id="fe64c-127">The interior of the polygon is filled.</span></span> <span data-ttu-id="fe64c-128">Атрибуты многоугольников, такие как GL \_ Polygon \_ СТИППЛЕ и GL \_ Polygon, \_ гладко управляют растрирование многоугольника.</span><span class="sxs-lookup"><span data-stu-id="fe64c-128">Polygon attributes such as GL\_POLYGON\_STIPPLE and GL\_POLYGON\_SMOOTH control the rasterization of the polygon.</span></span><br/>                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe64c-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe64c-129">Return value</span></span>

<span data-ttu-id="fe64c-130">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="fe64c-130">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fe64c-131">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="fe64c-131">Error codes</span></span>

<span data-ttu-id="fe64c-132">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="fe64c-132">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fe64c-133">Имя</span><span class="sxs-lookup"><span data-stu-id="fe64c-133">Name</span></span>                                                                                                  | <span data-ttu-id="fe64c-134">Значение</span><span class="sxs-lookup"><span data-stu-id="fe64c-134">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fe64c-135"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fe64c-135"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="fe64c-136">Недопустимое значение для *лица* или *режима* .</span><span class="sxs-lookup"><span data-stu-id="fe64c-136">Either *face* or *mode* was not an accepted value.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="fe64c-137"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fe64c-137"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fe64c-138">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="fe64c-138">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fe64c-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe64c-139">Remarks</span></span>

<span data-ttu-id="fe64c-140">Функция **глполигонмоде** управляет интерпретацией многоугольников для растрирования.</span><span class="sxs-lookup"><span data-stu-id="fe64c-140">The **glPolygonMode** function controls the interpretation of polygons for rasterization.</span></span> <span data-ttu-id="fe64c-141">Параметр *Face* описывает *режим* многоугольников: внешние многоугольники ( \_ передний план GL), многоугольники с обратным переходом (GL \_ ) или оба ( \_ передний \_ и \_ задний план).</span><span class="sxs-lookup"><span data-stu-id="fe64c-141">The *face* parameter describes which polygons *mode* applies to: front-facing polygons (GL\_FRONT), back-facing polygons (GL\_BACK), or both (GL\_FRONT\_AND\_BACK).</span></span> <span data-ttu-id="fe64c-142">Режим многоугольника влияет только на финальную растрирование многоугольников.</span><span class="sxs-lookup"><span data-stu-id="fe64c-142">The polygon mode affects only the final rasterization of polygons.</span></span> <span data-ttu-id="fe64c-143">В частности, вершины многоугольника освещены, а многоугольник обрезается и, возможно, исключается перед применением этих режимов.</span><span class="sxs-lookup"><span data-stu-id="fe64c-143">In particular, a polygon's vertices are lit and the polygon is clipped and possibly culled before these modes are applied.</span></span>

<span data-ttu-id="fe64c-144">Чтобы нарисовать поверхность с заполненными многоугольниками и обрисованными внешними многоугольниками, вызовите метод</span><span class="sxs-lookup"><span data-stu-id="fe64c-144">To draw a surface with filled back-facing polygons and outlined front-facing polygons, call</span></span>

<span data-ttu-id="fe64c-145">**глполигонмоде**(GL \_ спереди, \_ строка GL);</span><span class="sxs-lookup"><span data-stu-id="fe64c-145">**glPolygonMode**(GL\_FRONT, GL\_LINE);</span></span>

<span data-ttu-id="fe64c-146">Вершины помечаются как границы или неграницы с флагом границы.</span><span class="sxs-lookup"><span data-stu-id="fe64c-146">Vertices are marked as boundary or nonboundary with an edge flag.</span></span> <span data-ttu-id="fe64c-147">Пограничные флаги создаются внутренне OpenGL при разметке многоугольников и могут быть заданы явно с помощью [**гледжефлаг**](gledgeflag-functions.md).</span><span class="sxs-lookup"><span data-stu-id="fe64c-147">Edge flags are generated internally by OpenGL when it decomposes polygons, and they can be set explicitly using [**glEdgeFlag**](gledgeflag-functions.md).</span></span>

<span data-ttu-id="fe64c-148">Следующая функция получает сведения, связанные с **глполигонмоде**:</span><span class="sxs-lookup"><span data-stu-id="fe64c-148">The following function retrieves information related to **glPolygonMode**:</span></span>

<span data-ttu-id="fe64c-149">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ режим многоугольника GL \_</span><span class="sxs-lookup"><span data-stu-id="fe64c-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="fe64c-150">Требования</span><span class="sxs-lookup"><span data-stu-id="fe64c-150">Requirements</span></span>



| <span data-ttu-id="fe64c-151">Требование</span><span class="sxs-lookup"><span data-stu-id="fe64c-151">Requirement</span></span> | <span data-ttu-id="fe64c-152">Значение</span><span class="sxs-lookup"><span data-stu-id="fe64c-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe64c-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe64c-153">Minimum supported client</span></span><br/> | <span data-ttu-id="fe64c-154">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fe64c-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fe64c-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe64c-155">Minimum supported server</span></span><br/> | <span data-ttu-id="fe64c-156">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fe64c-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fe64c-157">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fe64c-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe64c-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe64c-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fe64c-159">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fe64c-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="fe64c-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe64c-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fe64c-161">DLL</span><span class="sxs-lookup"><span data-stu-id="fe64c-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe64c-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe64c-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe64c-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe64c-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe64c-164">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="fe64c-164">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fe64c-165">**гледжефлаг**</span><span class="sxs-lookup"><span data-stu-id="fe64c-165">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="fe64c-166">**гленд**</span><span class="sxs-lookup"><span data-stu-id="fe64c-166">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fe64c-167">**гллинестиппле**</span><span class="sxs-lookup"><span data-stu-id="fe64c-167">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="fe64c-168">**гллиневидс**</span><span class="sxs-lookup"><span data-stu-id="fe64c-168">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="fe64c-169">**глпоинтсизе**</span><span class="sxs-lookup"><span data-stu-id="fe64c-169">**glPointSize**</span></span>](glpointsize.md)
</dt> <dt>

[<span data-ttu-id="fe64c-170">**глполигонстиппле**</span><span class="sxs-lookup"><span data-stu-id="fe64c-170">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> </dl>

 

 





