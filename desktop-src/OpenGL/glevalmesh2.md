---
title: Функция glEvalMesh2 (GL. h)
description: Рассчитывает двухмерную сетку точек или линий.
ms.assetid: 21e94388-903e-4b9d-8e54-9c914d0ce372
keywords:
- Функция glEvalMesh2 OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 531e9f1f6288116d052c728654cd2cf03f38550a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801654"
---
# <a name="glevalmesh2-function"></a><span data-ttu-id="d4f08-104">Функция glEvalMesh2</span><span class="sxs-lookup"><span data-stu-id="d4f08-104">glEvalMesh2 function</span></span>

<span data-ttu-id="d4f08-105">Рассчитывает двухмерную сетку точек или линий.</span><span class="sxs-lookup"><span data-stu-id="d4f08-105">Computes a two-dimensional grid of points or lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4f08-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4f08-106">Syntax</span></span>


```C++
void WINAPI glEvalMesh2(
   GLenum mode,
   GLint  i1,
   GLint  i2,
   GLint  j1,
   GLint  j2
);
```



## <a name="parameters"></a><span data-ttu-id="d4f08-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4f08-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4f08-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="d4f08-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="d4f08-109">Значение, указывающее, следует ли вычислять двухмерную сетку точек, линий или многоугольников.</span><span class="sxs-lookup"><span data-stu-id="d4f08-109">A value that specifies whether to compute a two-dimensional mesh of points, lines, or polygons.</span></span> <span data-ttu-id="d4f08-110">Допустимы следующие символьные константы: \_ «точка GL», « \_ линия GL» и « \_ Заливка GL».</span><span class="sxs-lookup"><span data-stu-id="d4f08-110">The following symbolic constants are accepted: GL\_POINT, GL\_LINE, and GL\_FILL.</span></span>

</dd> <dt>

<span data-ttu-id="d4f08-111">*I1*</span><span class="sxs-lookup"><span data-stu-id="d4f08-111">*i1*</span></span> 
</dt> <dd>

<span data-ttu-id="d4f08-112">Первое целое значение для переменной домена сетки i.</span><span class="sxs-lookup"><span data-stu-id="d4f08-112">The first integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="d4f08-113">*I2*</span><span class="sxs-lookup"><span data-stu-id="d4f08-113">*i2*</span></span> 
</dt> <dd>

<span data-ttu-id="d4f08-114">Последнее целочисленное значение для переменной домена сетки i.</span><span class="sxs-lookup"><span data-stu-id="d4f08-114">The last integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="d4f08-115">*J1*</span><span class="sxs-lookup"><span data-stu-id="d4f08-115">*j1*</span></span> 
</dt> <dd>

<span data-ttu-id="d4f08-116">Первое целочисленное значение для переменной домена сетки j.</span><span class="sxs-lookup"><span data-stu-id="d4f08-116">The first integer value for grid domain variable j.</span></span>

</dd> <dt>

<span data-ttu-id="d4f08-117">*J2*</span><span class="sxs-lookup"><span data-stu-id="d4f08-117">*j2*</span></span> 
</dt> <dd>

<span data-ttu-id="d4f08-118">Последнее целочисленное значение для переменной домена сетки j.</span><span class="sxs-lookup"><span data-stu-id="d4f08-118">The last integer value for grid domain variable j.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4f08-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4f08-119">Return value</span></span>

<span data-ttu-id="d4f08-120">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d4f08-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d4f08-121">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d4f08-121">Error codes</span></span>

<span data-ttu-id="d4f08-122">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="d4f08-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d4f08-123">Имя</span><span class="sxs-lookup"><span data-stu-id="d4f08-123">Name</span></span>                                                                                                  | <span data-ttu-id="d4f08-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d4f08-124">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d4f08-125"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d4f08-125"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d4f08-126">Указывает, что *режим* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="d4f08-126">Indicates that *mode* is not an accepted value.</span></span> <br/>                                                                            |
| <dl> <span data-ttu-id="d4f08-127"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d4f08-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d4f08-128">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="d4f08-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="d4f08-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4f08-129">Remarks</span></span>

<span data-ttu-id="d4f08-130">Используйте [**глмапгрид**](glmapgrid-functions.md) и [**глевалмеш**](glevalmesh-functions.md) в сочетании для эффективного создания и вычисления ряда значений домена сопоставлений с равными пробелами.</span><span class="sxs-lookup"><span data-stu-id="d4f08-130">Use [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="d4f08-131">Функция **глевалмеш** выполняет шаг с целым доменом одномерной или двухмерной сетки, диапазон которого представляет собой домен карт оценки, заданных в [**glMap1**](glmap1.md) и [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="d4f08-131">The **glEvalMesh** function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="d4f08-132">Параметр mode определяет, соединяются ли результирующие вершины как точки, линии или закрашенные многоугольники.</span><span class="sxs-lookup"><span data-stu-id="d4f08-132">The mode parameter determines whether the resulting vertices are connected as points, lines, or filled polygons.</span></span>

<span data-ttu-id="d4f08-133">В двухмерном регистре **glEvalMesh2**, Let</span><span class="sxs-lookup"><span data-stu-id="d4f08-133">In the two-dimensional case, **glEvalMesh2**, let</span></span>

<span data-ttu-id="d4f08-134">?</span><span class="sxs-lookup"><span data-stu-id="d4f08-134">?</span></span> <span data-ttu-id="d4f08-135">u = (U2 U1)/n</span><span class="sxs-lookup"><span data-stu-id="d4f08-135">u = (u2 u1)/n</span></span>

<span data-ttu-id="d4f08-136">?</span><span class="sxs-lookup"><span data-stu-id="d4f08-136">?</span></span> <span data-ttu-id="d4f08-137">v = (V2 v1)/m,</span><span class="sxs-lookup"><span data-stu-id="d4f08-137">v = (v2 v1)/m,</span></span>

<span data-ttu-id="d4f08-138">где n, U1, U2, m, v1 и v2 являются аргументами самой последней функции [**glMapGrid2**](glmapgrid-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="d4f08-138">where n, u1, u2, m, v1, and v2 are the arguments to the most recent [**glMapGrid2**](glmapgrid-functions.md) function.</span></span> <span data-ttu-id="d4f08-139">Затем, если *mode* имеет значение GL \_ Fill, **glEvalMesh2** эквивалентно следующему:</span><span class="sxs-lookup"><span data-stu-id="d4f08-139">Then, if *mode* is GL\_FILL, **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="d4f08-140">для (j = J1; j < J2; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="d4f08-140">for (j = j1; j < j2; j += 1)</span></span>

<span data-ttu-id="d4f08-141">{</span><span class="sxs-lookup"><span data-stu-id="d4f08-141">{</span></span>

<span data-ttu-id="d4f08-142">[**глбегин**](glbegin.md)( \_ четыре \_ ленты GL);</span><span class="sxs-lookup"><span data-stu-id="d4f08-142">[**glBegin**](glbegin.md)(GL\_QUAD\_STRIP);</span></span>

<span data-ttu-id="d4f08-143">для (i = I1; я <= I2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="d4f08-143">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="d4f08-144">{</span><span class="sxs-lookup"><span data-stu-id="d4f08-144">{</span></span>

<span data-ttu-id="d4f08-145">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1 (), j?</span><span class="sxs-lookup"><span data-stu-id="d4f08-145">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , j ?</span></span> <span data-ttu-id="d4f08-146">v + v1);</span><span class="sxs-lookup"><span data-stu-id="d4f08-146">v + v1);</span></span>

<span data-ttu-id="d4f08-147">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1 (), (j + 1)?</span><span class="sxs-lookup"><span data-stu-id="d4f08-147">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , (j+1) ?</span></span> <span data-ttu-id="d4f08-148">v + v1);</span><span class="sxs-lookup"><span data-stu-id="d4f08-148">v + v1);</span></span>

<span data-ttu-id="d4f08-149">}</span><span class="sxs-lookup"><span data-stu-id="d4f08-149">}</span></span>

<span data-ttu-id="d4f08-150">[**гленд**](glend.md)(); }</span><span class="sxs-lookup"><span data-stu-id="d4f08-150">[**glEnd**](glend.md)( ); }</span></span>

<span data-ttu-id="d4f08-151">Если *режим* является \_ строкой GL, вызов **glEvalMesh2** эквивалентен следующему:</span><span class="sxs-lookup"><span data-stu-id="d4f08-151">If *mode* is GL\_LINE, then a call to **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="d4f08-152">для (j = J1; j <= J2; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="d4f08-152">for (j = j1; j <= j2; j += 1)</span></span>

<span data-ttu-id="d4f08-153">{</span><span class="sxs-lookup"><span data-stu-id="d4f08-153">{</span></span>

<span data-ttu-id="d4f08-154">[**глбегин**](glbegin.md)( \_ \_ полоса строк GL);</span><span class="sxs-lookup"><span data-stu-id="d4f08-154">[**glBegin**](glbegin.md)(GL\_LINE\_STRIP);</span></span>

<span data-ttu-id="d4f08-155">для (i = I1; я <= I2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="d4f08-155">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="d4f08-156">{</span><span class="sxs-lookup"><span data-stu-id="d4f08-156">{</span></span>

<span data-ttu-id="d4f08-157">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);</span><span class="sxs-lookup"><span data-stu-id="d4f08-157">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="d4f08-158">}</span><span class="sxs-lookup"><span data-stu-id="d4f08-158">}</span></span>

<span data-ttu-id="d4f08-159">[**гленд**](glend.md)();</span><span class="sxs-lookup"><span data-stu-id="d4f08-159">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="d4f08-160">}</span><span class="sxs-lookup"><span data-stu-id="d4f08-160">}</span></span>

<span data-ttu-id="d4f08-161">для (i = I1; я <= I2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="d4f08-161">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="d4f08-162">{</span><span class="sxs-lookup"><span data-stu-id="d4f08-162">{</span></span>

<span data-ttu-id="d4f08-163">[**глбегин**](glbegin.md)( \_ \_ полоса строк GL);</span><span class="sxs-lookup"><span data-stu-id="d4f08-163">[**glBegin**](glbegin.md)(GL\_LINE\_STRIP);</span></span>

<span data-ttu-id="d4f08-164">для (j = J1; j <= J1; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="d4f08-164">for (j = j1; j <= j1; j += 1)</span></span>

<span data-ttu-id="d4f08-165">{</span><span class="sxs-lookup"><span data-stu-id="d4f08-165">{</span></span>

<span data-ttu-id="d4f08-166">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);</span><span class="sxs-lookup"><span data-stu-id="d4f08-166">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="d4f08-167">}</span><span class="sxs-lookup"><span data-stu-id="d4f08-167">}</span></span>

<span data-ttu-id="d4f08-168">Гленд ();</span><span class="sxs-lookup"><span data-stu-id="d4f08-168">glEnd( );</span></span>

<span data-ttu-id="d4f08-169">}</span><span class="sxs-lookup"><span data-stu-id="d4f08-169">}</span></span>

<span data-ttu-id="d4f08-170">И, наконец, если *mode* является \_ точкой GL, вызов **glEvalMesh2** эквивалентен следующему:</span><span class="sxs-lookup"><span data-stu-id="d4f08-170">And finally, if *mode* is GL\_POINT, then a call to **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="d4f08-171">[**глбегин**](glbegin.md)( \_ пункты GL);</span><span class="sxs-lookup"><span data-stu-id="d4f08-171">[**glBegin**](glbegin.md)(GL\_POINTS);</span></span>

<span data-ttu-id="d4f08-172">для (j = J1; j <= J2; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="d4f08-172">for (j = j1; j <= j2; j += 1)</span></span>

<span data-ttu-id="d4f08-173">{</span><span class="sxs-lookup"><span data-stu-id="d4f08-173">{</span></span>

<span data-ttu-id="d4f08-174">для (i = I1; я <= I2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="d4f08-174">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="d4f08-175">{</span><span class="sxs-lookup"><span data-stu-id="d4f08-175">{</span></span>

<span data-ttu-id="d4f08-176">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);</span><span class="sxs-lookup"><span data-stu-id="d4f08-176">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="d4f08-177">}</span><span class="sxs-lookup"><span data-stu-id="d4f08-177">}</span></span>

<span data-ttu-id="d4f08-178">}</span><span class="sxs-lookup"><span data-stu-id="d4f08-178">}</span></span>

<span data-ttu-id="d4f08-179">[**гленд**](glend.md)();</span><span class="sxs-lookup"><span data-stu-id="d4f08-179">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="d4f08-180">Во всех трех случаях единственными абсолютными числовыми требованиями является то, что если i = n, то значение, вычисленное из i? u + U1 — это ровно U2, а если j = m, то значение, вычисленное из j? v + v1 — ровно 2.</span><span class="sxs-lookup"><span data-stu-id="d4f08-180">In all three cases, the only absolute numeric requirements are that if i = n, then the value computed from i? u + u1 is exactly u2, and if j = m, then the value computed from j? v + v1 is exactly v2.</span></span> <span data-ttu-id="d4f08-181">Следующие функции извлекают сведения, относящиеся к **глевалмеш**:</span><span class="sxs-lookup"><span data-stu-id="d4f08-181">The following functions retrieve information relating to **glEvalMesh**:</span></span>

<span data-ttu-id="d4f08-182">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ GL \_ «Карта1» \_ домен Grid</span><span class="sxs-lookup"><span data-stu-id="d4f08-182">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>

<span data-ttu-id="d4f08-183">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ GL \_ MAP2 \_ домен Grid</span><span class="sxs-lookup"><span data-stu-id="d4f08-183">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>

<span data-ttu-id="d4f08-184">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументами \_ \_ сегментами сетки GL «Карта1» \_</span><span class="sxs-lookup"><span data-stu-id="d4f08-184">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>

<span data-ttu-id="d4f08-185">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументами \_ \_ сегментами сетки GL MAP2 \_</span><span class="sxs-lookup"><span data-stu-id="d4f08-185">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="d4f08-186">Требования</span><span class="sxs-lookup"><span data-stu-id="d4f08-186">Requirements</span></span>



| <span data-ttu-id="d4f08-187">Требование</span><span class="sxs-lookup"><span data-stu-id="d4f08-187">Requirement</span></span> | <span data-ttu-id="d4f08-188">Значение</span><span class="sxs-lookup"><span data-stu-id="d4f08-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f08-189">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4f08-189">Minimum supported client</span></span><br/> | <span data-ttu-id="d4f08-190">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d4f08-190">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d4f08-191">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4f08-191">Minimum supported server</span></span><br/> | <span data-ttu-id="d4f08-192">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d4f08-192">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d4f08-193">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d4f08-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4f08-194"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4f08-194"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d4f08-195">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d4f08-195">Library</span></span><br/>                  | <dl> <span data-ttu-id="d4f08-196"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4f08-196"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d4f08-197">DLL</span><span class="sxs-lookup"><span data-stu-id="d4f08-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4f08-198"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4f08-198"><dt>Opengl32.dll</dt></span></span> </dl> |



 

 





