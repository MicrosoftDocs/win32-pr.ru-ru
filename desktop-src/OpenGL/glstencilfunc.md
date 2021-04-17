---
title: Функция ГлстенЦилфунк (GL. h)
description: Функция ГлстенЦилфунк задает функцию и ссылочное значение для тестирования набора элементов.
ms.assetid: 6c84415b-4d22-494b-90f2-6243d1406725
keywords:
- Функция ГлстенЦилфунк OpenGL
topic_type:
- apiref
api_name:
- glStencilFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4f9c0a5ec905ecb061ddb54984bf35ff8edc3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672911"
---
# <a name="glstencilfunc-function"></a><span data-ttu-id="14cd5-104">Функция ГлстенЦилфунк</span><span class="sxs-lookup"><span data-stu-id="14cd5-104">glStencilFunc function</span></span>

<span data-ttu-id="14cd5-105">Функция **глстенЦилфунк** задает функцию и ссылочное значение для тестирования набора элементов.</span><span class="sxs-lookup"><span data-stu-id="14cd5-105">The **glStencilFunc** function sets the function and reference value for stencil testing.</span></span>

## <a name="syntax"></a><span data-ttu-id="14cd5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14cd5-106">Syntax</span></span>


```C++
void WINAPI glStencilFunc(
   GLenum func,
   GLint  ref,
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="14cd5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="14cd5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14cd5-108">*func*</span><span class="sxs-lookup"><span data-stu-id="14cd5-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="14cd5-109">Тестовая функция.</span><span class="sxs-lookup"><span data-stu-id="14cd5-109">The test function.</span></span> <span data-ttu-id="14cd5-110">Допустимы следующие восемь токенов.</span><span class="sxs-lookup"><span data-stu-id="14cd5-110">The following eight tokens are valid.</span></span>



| <span data-ttu-id="14cd5-111">Значение</span><span class="sxs-lookup"><span data-stu-id="14cd5-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="14cd5-112">Значение</span><span class="sxs-lookup"><span data-stu-id="14cd5-112">Meaning</span></span>                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="14cd5-113"><dt>**ГК \_ никогда**</dt></span><span class="sxs-lookup"><span data-stu-id="14cd5-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="14cd5-114">Всегда завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="14cd5-114">Always fails.</span></span><br/>                                         |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="14cd5-115"><dt>**\_меньше ГК**</dt></span><span class="sxs-lookup"><span data-stu-id="14cd5-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="14cd5-116">Передает, если (*ref*  &  *Mask*) < (маска *набора элементов*  &  ).</span><span class="sxs-lookup"><span data-stu-id="14cd5-116">Passes if (*ref* & *mask*) < (*stencil* & *mask*).</span></span><br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="14cd5-117"><dt>**\_ЛЕКУАЛ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="14cd5-117"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="14cd5-118">Передает, если (*ref*  &  *Mask*) = (маска *набора элементов*  &  ).</span><span class="sxs-lookup"><span data-stu-id="14cd5-118">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="14cd5-119"><dt>**в \_ ГК**</dt></span><span class="sxs-lookup"><span data-stu-id="14cd5-119"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="14cd5-120">Передает, если (*ref*  &  *Mask*) > (маска *набора элементов*  &  ).</span><span class="sxs-lookup"><span data-stu-id="14cd5-120">Passes if (*ref* & *mask*) > (*stencil* & *mask*).</span></span><br/> |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="14cd5-121"><dt>**\_ЖЕКУАЛ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="14cd5-121"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="14cd5-122">Передает, если (*ref*  &  *Mask*) = (маска *набора элементов*  &  ).</span><span class="sxs-lookup"><span data-stu-id="14cd5-122">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="14cd5-123"><dt>**значение GL \_ равно**</dt></span><span class="sxs-lookup"><span data-stu-id="14cd5-123"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="14cd5-124">Передает, если (*ref*  &  *Mask*) = (маска *набора элементов*  &  ).</span><span class="sxs-lookup"><span data-stu-id="14cd5-124">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="14cd5-125"><dt>**\_NOTEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="14cd5-125"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="14cd5-126">Передать, если (*ref*  &  *Mask*)?</span><span class="sxs-lookup"><span data-stu-id="14cd5-126">Passes if (*ref* & *mask*) ?</span></span> <span data-ttu-id="14cd5-127">(*набор элементов*  &  *Маска*).</span><span class="sxs-lookup"><span data-stu-id="14cd5-127">(*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="14cd5-128"><dt>**GL \_ всегда**</dt></span><span class="sxs-lookup"><span data-stu-id="14cd5-128"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="14cd5-129">Всегда передает.</span><span class="sxs-lookup"><span data-stu-id="14cd5-129">Always passes.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="14cd5-130">*ref*</span><span class="sxs-lookup"><span data-stu-id="14cd5-130">*ref*</span></span> 
</dt> <dd>

<span data-ttu-id="14cd5-131">Эталонное значение для теста набора элементов.</span><span class="sxs-lookup"><span data-stu-id="14cd5-131">The reference value for the stencil test.</span></span> <span data-ttu-id="14cd5-132">Параметр *ref* передается в диапазон \[ 0, 2 *n* 1 \] , где *n* — число битпланес в буфере шаблона.</span><span class="sxs-lookup"><span data-stu-id="14cd5-132">The *ref* parameter is clamped to the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span>

</dd> <dt>

<span data-ttu-id="14cd5-133">*виде*</span><span class="sxs-lookup"><span data-stu-id="14cd5-133">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="14cd5-134">Маска, которая является **и** ED со значением ссылки и сохраненным значением трафарета после завершения теста.</span><span class="sxs-lookup"><span data-stu-id="14cd5-134">A mask that is **AND** ed with both the reference value and the stored stencil value when the test is done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14cd5-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14cd5-135">Return value</span></span>

<span data-ttu-id="14cd5-136">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="14cd5-136">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="14cd5-137">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="14cd5-137">Error codes</span></span>

<span data-ttu-id="14cd5-138">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="14cd5-138">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="14cd5-139">Имя</span><span class="sxs-lookup"><span data-stu-id="14cd5-139">Name</span></span>                                                                                                  | <span data-ttu-id="14cd5-140">Значение</span><span class="sxs-lookup"><span data-stu-id="14cd5-140">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="14cd5-141"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="14cd5-141"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="14cd5-142">Функция *Func* не является одним из восьми допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="14cd5-142">*func* was not one of the eight accepted values.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="14cd5-143"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="14cd5-143"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="14cd5-144">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="14cd5-144">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="14cd5-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14cd5-145">Remarks</span></span>

<span data-ttu-id="14cd5-146">Набор элементов, например *z*-буферизация, включает и отключает рисование на уровне отдельных пикселов.</span><span class="sxs-lookup"><span data-stu-id="14cd5-146">Stenciling, like *z*-buffering, enables and disables drawing on a per-pixel basis.</span></span> <span data-ttu-id="14cd5-147">Вы рисуете на плоскости трафаретов с помощью примитивов рисования OpenGL, затем визуализируете геометрию и изображения, используя плоскости трафаретов для маскирования частей экрана.</span><span class="sxs-lookup"><span data-stu-id="14cd5-147">You draw into the stencil planes using OpenGL drawing primitives, then render geometry and images, using the stencil planes to mask out portions of the screen.</span></span> <span data-ttu-id="14cd5-148">Набор элементов обычно используется в алгоритмах многопроходной отрисовки для достижения специальных эффектов, таких как декалс, структурирование и конструктивностьная визуализация геометрических объектов.</span><span class="sxs-lookup"><span data-stu-id="14cd5-148">Stenciling is typically used in multipass rendering algorithms to achieve special effects, such as decals, outlining, and constructive solid geometry rendering.</span></span>

<span data-ttu-id="14cd5-149">Условие теста трафарета позволяет исключить пиксель на основе результатов сравнения между ссылочным значением и значением в буфере шаблона.</span><span class="sxs-lookup"><span data-stu-id="14cd5-149">The stencil test conditionally eliminates a pixel based on the outcome of a comparison between the reference value and the value in the stencil buffer.</span></span> <span data-ttu-id="14cd5-150">Тест включается с помощью [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md) с аргументом \_ Test трафарета GL \_ .</span><span class="sxs-lookup"><span data-stu-id="14cd5-150">The test is enabled by [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_STENCIL\_TEST.</span></span> <span data-ttu-id="14cd5-151">Действия, выполненные на основе результата теста набора элементов, указываются с помощью [**глстенЦилоп**](glstencilop.md).</span><span class="sxs-lookup"><span data-stu-id="14cd5-151">Actions taken based on the outcome of the stencil test are specified with [**glStencilOp**](glstencilop.md).</span></span>

<span data-ttu-id="14cd5-152">Параметр *Func* является символьной константой, определяющей функцию сравнения наборов элементов.</span><span class="sxs-lookup"><span data-stu-id="14cd5-152">The *func* parameter is a symbolic constant that determines the stencil comparison function.</span></span> <span data-ttu-id="14cd5-153">Он принимает одно из восьми значений, показанных выше.</span><span class="sxs-lookup"><span data-stu-id="14cd5-153">It accepts one of the eight values shown above.</span></span> <span data-ttu-id="14cd5-154">Параметр *ref* — это целочисленное значение ссылки, используемое в сравнении наборов элементов.</span><span class="sxs-lookup"><span data-stu-id="14cd5-154">The *ref* parameter is an integer reference value that is used in the stencil comparison.</span></span> <span data-ttu-id="14cd5-155">Он перемещается в диапазон \[ 0, 2 *n* 1 \] , где *n* — число битпланес в буфере шаблона.</span><span class="sxs-lookup"><span data-stu-id="14cd5-155">It is clamped to the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span> <span data-ttu-id="14cd5-156">Параметр *Mask* является побитовым **и** ED как ссылочным значением, так и сохраненным значением трафарета со значениями **и** ED, участвующими в сравнении.</span><span class="sxs-lookup"><span data-stu-id="14cd5-156">The *mask* parameter is bitwise **AND** ed with both the reference value and the stored stencil value, with the **AND** ed values participating in the comparison.</span></span>

<span data-ttu-id="14cd5-157">Если *набор элементов* представляет значение, хранящееся в соответствующем расположении буфера набора элементов, в приведенном выше списке показан результат каждой функции сравнения, которая может быть указана функцией *Func*.</span><span class="sxs-lookup"><span data-stu-id="14cd5-157">If *stencil* represents the value stored in the corresponding stencil buffer location, the preceding list shows the effect of each comparison function that can be specified by *func*.</span></span> <span data-ttu-id="14cd5-158">Только если сравнение выполнено успешно, точка передается на следующий этап процесса растрирования (см. [**глстенЦилоп**](glstencilop.md)).</span><span class="sxs-lookup"><span data-stu-id="14cd5-158">Only if the comparison succeeds is the pixel passed through to the next stage in the rasterization process (see [**glStencilOp**](glstencilop.md)).</span></span> <span data-ttu-id="14cd5-159">Все тесты рассматривают значения *набора элементов* как целые числа без знака в диапазоне \[ 0, 2 *n* 1 \] , где *n* — число битпланес в буфере шаблона.</span><span class="sxs-lookup"><span data-stu-id="14cd5-159">All tests treat *stencil* values as unsigned integers in the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span>

<span data-ttu-id="14cd5-160">Изначально тест шаблона отключен.</span><span class="sxs-lookup"><span data-stu-id="14cd5-160">Initially, the stencil test is disabled.</span></span> <span data-ttu-id="14cd5-161">Если буфер трафарета отсутствует, изменение трафарета не может быть выполнено, так как тест шаблона всегда проходит.</span><span class="sxs-lookup"><span data-stu-id="14cd5-161">If there is no stencil buffer, no stencil modification can occur and it is as if the stencil test always passes.</span></span>

<span data-ttu-id="14cd5-162">Следующие функции извлекают сведения, относящиеся к **глстенЦилфунк**:</span><span class="sxs-lookup"><span data-stu-id="14cd5-162">The following functions retrieve information related to **glStencilFunc**:</span></span>

<span data-ttu-id="14cd5-163">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом " \_ набор элементов GL" \_ Func</span><span class="sxs-lookup"><span data-stu-id="14cd5-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_FUNC</span></span>

<span data-ttu-id="14cd5-164">**глжет** с аргументом \_ \_ Маска значения трафарета GL \_</span><span class="sxs-lookup"><span data-stu-id="14cd5-164">**glGet** with argument GL\_STENCIL\_VALUE\_MASK</span></span>

<span data-ttu-id="14cd5-165">**глжет** с аргументом " \_ ссылка на трафарет шаблона GL" \_</span><span class="sxs-lookup"><span data-stu-id="14cd5-165">**glGet** with argument GL\_STENCIL\_REF</span></span>

<span data-ttu-id="14cd5-166">**глжет** с аргументом \_ биты шаблона GL \_</span><span class="sxs-lookup"><span data-stu-id="14cd5-166">**glGet** with argument GL\_STENCIL\_BITS</span></span>

<span data-ttu-id="14cd5-167">[**глисенаблед**](glisenabled.md) с аргументом \_ Test трафарета GL \_</span><span class="sxs-lookup"><span data-stu-id="14cd5-167">[**glIsEnabled**](glisenabled.md) with argument GL\_STENCIL\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="14cd5-168">Требования</span><span class="sxs-lookup"><span data-stu-id="14cd5-168">Requirements</span></span>



| <span data-ttu-id="14cd5-169">Требование</span><span class="sxs-lookup"><span data-stu-id="14cd5-169">Requirement</span></span> | <span data-ttu-id="14cd5-170">Значение</span><span class="sxs-lookup"><span data-stu-id="14cd5-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14cd5-171">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14cd5-171">Minimum supported client</span></span><br/> | <span data-ttu-id="14cd5-172">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="14cd5-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="14cd5-173">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14cd5-173">Minimum supported server</span></span><br/> | <span data-ttu-id="14cd5-174">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="14cd5-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="14cd5-175">Заголовок</span><span class="sxs-lookup"><span data-stu-id="14cd5-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="14cd5-176"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="14cd5-176"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="14cd5-177">Библиотека</span><span class="sxs-lookup"><span data-stu-id="14cd5-177">Library</span></span><br/>                  | <dl> <span data-ttu-id="14cd5-178"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14cd5-178"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="14cd5-179">DLL</span><span class="sxs-lookup"><span data-stu-id="14cd5-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14cd5-180"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14cd5-180"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14cd5-181">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14cd5-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14cd5-182">**глалфафунк**</span><span class="sxs-lookup"><span data-stu-id="14cd5-182">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="14cd5-183">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="14cd5-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="14cd5-184">**глблендфунк**</span><span class="sxs-lookup"><span data-stu-id="14cd5-184">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="14cd5-185">**глдепсфунк**</span><span class="sxs-lookup"><span data-stu-id="14cd5-185">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="14cd5-186">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="14cd5-186">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="14cd5-187">**гленд**</span><span class="sxs-lookup"><span data-stu-id="14cd5-187">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="14cd5-188">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="14cd5-188">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="14cd5-189">**гллогикоп**</span><span class="sxs-lookup"><span data-stu-id="14cd5-189">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="14cd5-190">**глстенЦилоп**</span><span class="sxs-lookup"><span data-stu-id="14cd5-190">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





