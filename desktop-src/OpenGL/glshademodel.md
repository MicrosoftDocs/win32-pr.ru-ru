---
title: Функция Глшадемодел (GL. h)
description: Функция Глшадемодел выбирает плоскую или плавную заливку.
ms.assetid: 52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e
keywords:
- Функция Глшадемодел OpenGL
topic_type:
- apiref
api_name:
- glShadeModel
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142ac518c91c6378f1606235e25502be8c06dd6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672621"
---
# <a name="glshademodel-function"></a><span data-ttu-id="34a52-104">Функция Глшадемодел</span><span class="sxs-lookup"><span data-stu-id="34a52-104">glShadeModel function</span></span>

<span data-ttu-id="34a52-105">Функция **глшадемодел** выбирает плоскую или плавную заливку.</span><span class="sxs-lookup"><span data-stu-id="34a52-105">The **glShadeModel** function selects flat or smooth shading.</span></span>

## <a name="syntax"></a><span data-ttu-id="34a52-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34a52-106">Syntax</span></span>


```C++
void WINAPI glShadeModel(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="34a52-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="34a52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34a52-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="34a52-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="34a52-109">Символьное значение, представляющее метод заливки.</span><span class="sxs-lookup"><span data-stu-id="34a52-109">A symbolic value representing a shading technique.</span></span> <span data-ttu-id="34a52-110">Допустимые значения: GL \_ Flat и GL \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="34a52-110">Accepted values are GL\_FLAT and GL\_SMOOTH.</span></span> <span data-ttu-id="34a52-111">По умолчанию используется параметр GL \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="34a52-111">The default is GL\_SMOOTH.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34a52-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34a52-112">Return value</span></span>

<span data-ttu-id="34a52-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="34a52-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="34a52-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="34a52-114">Error codes</span></span>

<span data-ttu-id="34a52-115">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="34a52-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="34a52-116">Имя</span><span class="sxs-lookup"><span data-stu-id="34a52-116">Name</span></span>                                                                                                  | <span data-ttu-id="34a52-117">Значение</span><span class="sxs-lookup"><span data-stu-id="34a52-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="34a52-118"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="34a52-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="34a52-119">*режим* имел значение, отличное от GL \_ глат или GL \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="34a52-119">*mode* was a value other than GL\_GLAT or GL\_SMOOTH.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="34a52-120"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="34a52-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="34a52-121">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="34a52-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="34a52-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34a52-122">Remarks</span></span>

<span data-ttu-id="34a52-123">Примитивы OpenGL могут иметь плоскую или плавную заливку.</span><span class="sxs-lookup"><span data-stu-id="34a52-123">OpenGL primitives can have either flat or smooth shading.</span></span> <span data-ttu-id="34a52-124">Плавное затенение, используемое по умолчанию, приводит к интерполяции вычисленных цветов вершин по мере растрирования примитива, обычно присваивая каждому фрагменту пиксела разные цвета.</span><span class="sxs-lookup"><span data-stu-id="34a52-124">Smooth shading, the default, causes the computed colors of vertices to be interpolated as the primitive is rasterized, typically assigning different colors to each resulting pixel fragment.</span></span> <span data-ttu-id="34a52-125">Плоская заливка выбирает вычисленный цвет только для одной вершины и назначает ее всем фрагментам пикселов, созданным с помощью растрирования одного примитива.</span><span class="sxs-lookup"><span data-stu-id="34a52-125">Flat shading selects the computed color of just one vertex and assigns it to all the pixel fragments generated by rasterizing a single primitive.</span></span> <span data-ttu-id="34a52-126">В любом случае вычисленный цвет вершины является результатом освещения, если освещение включено, или текущим цветом на момент указания вершины, если освещение отключено.</span><span class="sxs-lookup"><span data-stu-id="34a52-126">In either case, the computed color of a vertex is the result of lighting, if lighting is enabled, or it is the current color at the time the vertex was specified, if lighting is disabled.</span></span>

<span data-ttu-id="34a52-127">Плоские и плавные заливки неразличимы для точек.</span><span class="sxs-lookup"><span data-stu-id="34a52-127">Flat and smooth shading are indistinguishable for points.</span></span> <span data-ttu-id="34a52-128">Подсчет вершин и примитивов из одного, начиная с [**глбегин**](glbegin.md) , *каждый сегмент сплошной линии получает* вычисленный цвет вершины *i* + 1, второй вершиной.</span><span class="sxs-lookup"><span data-stu-id="34a52-128">Counting vertices and primitives from one, starting when [**glBegin**](glbegin.md) is issued, each flat-shaded line segment *i* is given the computed color of vertex *i* + 1, its second vertex.</span></span> <span data-ttu-id="34a52-129">Аналогичным образом, каждому плоскому многоугольнику присваивается вычисленный цвет вершин, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="34a52-129">Counting similarly from one, each flat-shaded polygon is given the computed color of the vertex listed in the following table.</span></span> <span data-ttu-id="34a52-130">Это последняя вершина для указания многоугольника во всех случаях, кроме единичных многоугольников, где первая вершина задает цвет с плоским затенением.</span><span class="sxs-lookup"><span data-stu-id="34a52-130">This is the last vertex to specify the polygon in all cases except single polygons, where the first vertex specifies the flat-shaded color.</span></span>



| <span data-ttu-id="34a52-131">Примитивный тип многоугольника i</span><span class="sxs-lookup"><span data-stu-id="34a52-131">Primitive type of polygon i</span></span> | <span data-ttu-id="34a52-132">Вершина</span><span class="sxs-lookup"><span data-stu-id="34a52-132">Vertex</span></span>   |
|-----------------------------|----------|
| <span data-ttu-id="34a52-133">Один многоугольник (*I*= 1)</span><span class="sxs-lookup"><span data-stu-id="34a52-133">Single polygon (*I*=1)</span></span>      | <span data-ttu-id="34a52-134">1</span><span class="sxs-lookup"><span data-stu-id="34a52-134">1</span></span>        |
| <span data-ttu-id="34a52-135">Лента треугольника</span><span class="sxs-lookup"><span data-stu-id="34a52-135">Triangle strip</span></span>              | <span data-ttu-id="34a52-136">*i* + 2</span><span class="sxs-lookup"><span data-stu-id="34a52-136">*i* + 2</span></span>  |
| <span data-ttu-id="34a52-137">Вентилятор треугольника</span><span class="sxs-lookup"><span data-stu-id="34a52-137">Triangle fan</span></span>                | <span data-ttu-id="34a52-138">*i* + 2</span><span class="sxs-lookup"><span data-stu-id="34a52-138">*i* + 2</span></span>  |
| <span data-ttu-id="34a52-139">Независимый треугольник</span><span class="sxs-lookup"><span data-stu-id="34a52-139">Independent triangle</span></span>        | <span data-ttu-id="34a52-140">3 *I*</span><span class="sxs-lookup"><span data-stu-id="34a52-140">3 *I*</span></span>     |
| <span data-ttu-id="34a52-141">Четыре полосы</span><span class="sxs-lookup"><span data-stu-id="34a52-141">Quad strip</span></span>                  | <span data-ttu-id="34a52-142">2 *i* + 2</span><span class="sxs-lookup"><span data-stu-id="34a52-142">2 *i* + 2</span></span> |
| <span data-ttu-id="34a52-143">Независимый четырехъядерный</span><span class="sxs-lookup"><span data-stu-id="34a52-143">Independent quad</span></span>            | <span data-ttu-id="34a52-144">4</span><span class="sxs-lookup"><span data-stu-id="34a52-144">4 *I*</span></span>     |



 

<span data-ttu-id="34a52-145">Плоская и гладкая заливка задаются параметром **глшадемодел** с *режимом* GL \_ Flat и GL \_ Smooth соответственно.</span><span class="sxs-lookup"><span data-stu-id="34a52-145">Flat and smooth shading are specified by **glShadeModel** with *mode* set to GL\_FLAT and GL\_SMOOTH, respectively.</span></span>

<span data-ttu-id="34a52-146">Следующая функция получает сведения, связанные с **глшадемодел**:</span><span class="sxs-lookup"><span data-stu-id="34a52-146">The following function retrieves information related to **glShadeModel**:</span></span>

<span data-ttu-id="34a52-147">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ модели шейдера GL \_</span><span class="sxs-lookup"><span data-stu-id="34a52-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_SHADE\_MODEL</span></span>

## <a name="requirements"></a><span data-ttu-id="34a52-148">Требования</span><span class="sxs-lookup"><span data-stu-id="34a52-148">Requirements</span></span>



| <span data-ttu-id="34a52-149">Требование</span><span class="sxs-lookup"><span data-stu-id="34a52-149">Requirement</span></span> | <span data-ttu-id="34a52-150">Значение</span><span class="sxs-lookup"><span data-stu-id="34a52-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34a52-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34a52-151">Minimum supported client</span></span><br/> | <span data-ttu-id="34a52-152">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="34a52-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="34a52-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34a52-153">Minimum supported server</span></span><br/> | <span data-ttu-id="34a52-154">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="34a52-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="34a52-155">Заголовок</span><span class="sxs-lookup"><span data-stu-id="34a52-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="34a52-156"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="34a52-156"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="34a52-157">Библиотека</span><span class="sxs-lookup"><span data-stu-id="34a52-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="34a52-158"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34a52-158"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="34a52-159">DLL</span><span class="sxs-lookup"><span data-stu-id="34a52-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34a52-160"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34a52-160"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34a52-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34a52-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34a52-162">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="34a52-162">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="34a52-163">**глколор**</span><span class="sxs-lookup"><span data-stu-id="34a52-163">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="34a52-164">**гленд**</span><span class="sxs-lookup"><span data-stu-id="34a52-164">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="34a52-165">**гллигхт**</span><span class="sxs-lookup"><span data-stu-id="34a52-165">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="34a52-166">**гллигхтмодел**</span><span class="sxs-lookup"><span data-stu-id="34a52-166">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





