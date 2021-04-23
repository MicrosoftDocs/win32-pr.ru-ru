---
title: Функция ГлстенЦилоп (GL. h)
description: Функция ГлстенЦилоп задает действия теста набора элементов.
ms.assetid: 16809735-5624-49cf-bfa5-9908d008b234
keywords:
- Функция ГлстенЦилоп OpenGL
topic_type:
- apiref
api_name:
- glStencilOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b23162f8606ed68dc90a0cb6debdcc903e0ccd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672779"
---
# <a name="glstencilop-function"></a><span data-ttu-id="77b64-104">Функция ГлстенЦилоп</span><span class="sxs-lookup"><span data-stu-id="77b64-104">glStencilOp function</span></span>

<span data-ttu-id="77b64-105">Функция **глстенЦилоп** задает действия теста набора элементов.</span><span class="sxs-lookup"><span data-stu-id="77b64-105">The **glStencilOp** function sets the stencil test actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="77b64-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77b64-106">Syntax</span></span>


```C++
void WINAPI glStencilOp(
   GLenum fail,
   GLenum zfail,
   GLenum zpass
);
```



## <a name="parameters"></a><span data-ttu-id="77b64-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="77b64-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77b64-108">*Cчетчик*</span><span class="sxs-lookup"><span data-stu-id="77b64-108">*fail*</span></span> 
</dt> <dd>

<span data-ttu-id="77b64-109">Действие, выполняемое при сбое теста шаблона.</span><span class="sxs-lookup"><span data-stu-id="77b64-109">The action to take when the stencil test fails.</span></span> <span data-ttu-id="77b64-110">Принимаются следующие шесть символьных констант.</span><span class="sxs-lookup"><span data-stu-id="77b64-110">The following six symbolic constants are accepted.</span></span>



| <span data-ttu-id="77b64-111">Значение</span><span class="sxs-lookup"><span data-stu-id="77b64-111">Value</span></span>                                                                                                                                                | <span data-ttu-id="77b64-112">Значение</span><span class="sxs-lookup"><span data-stu-id="77b64-112">Meaning</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="GL_KEEP"></span><span id="gl_keep"></span><dl> <span data-ttu-id="77b64-113"><dt>**Держитесь в ГК \_**</dt></span><span class="sxs-lookup"><span data-stu-id="77b64-113"><dt>**GL\_KEEP**</dt></span></span> </dl>          | <span data-ttu-id="77b64-114">Сохраняет текущее значение.</span><span class="sxs-lookup"><span data-stu-id="77b64-114">Keeps the current value.</span></span><br/>                                                                         |
| <span id="GL_ZERO"></span><span id="gl_zero"></span><dl> <span data-ttu-id="77b64-115"><dt>**ноль в ГК \_**</dt></span><span class="sxs-lookup"><span data-stu-id="77b64-115"><dt>**GL\_ZERO**</dt></span></span> </dl>          | <span data-ttu-id="77b64-116">Устанавливает значение буфера набора элементов равным нулю.</span><span class="sxs-lookup"><span data-stu-id="77b64-116">Sets the stencil buffer value to zero.</span></span><br/>                                                           |
| <span id="GL_REPLACE"></span><span id="gl_replace"></span><dl> <span data-ttu-id="77b64-117"><dt>**\_Замена GL**</dt></span><span class="sxs-lookup"><span data-stu-id="77b64-117"><dt>**GL\_REPLACE**</dt></span></span> </dl> | <span data-ttu-id="77b64-118">Устанавливает значение параметра буфера набора элементов равным *ref*, как указано в **глстенЦилфунк**.</span><span class="sxs-lookup"><span data-stu-id="77b64-118">Sets the stencil buffer value to *ref*, as specified by **glStencilFunc**.</span></span><br/>                       |
| <span id="GL_INCR"></span><span id="gl_incr"></span><dl> <span data-ttu-id="77b64-119"><dt>**\_INCR GL**</dt></span><span class="sxs-lookup"><span data-stu-id="77b64-119"><dt>**GL\_INCR**</dt></span></span> </dl>          | <span data-ttu-id="77b64-120">Увеличивает значение текущего буфера набора элементов.</span><span class="sxs-lookup"><span data-stu-id="77b64-120">Increments the current stencil buffer value.</span></span> <span data-ttu-id="77b64-121">Фиксация максимального неподписанного значения без знака.</span><span class="sxs-lookup"><span data-stu-id="77b64-121">Clamps to the maximum representable unsigned value.</span></span><br/> |
| <span id="GL_DECR"></span><span id="gl_decr"></span><dl> <span data-ttu-id="77b64-122"><dt>**\_ДЕКР GL**</dt></span><span class="sxs-lookup"><span data-stu-id="77b64-122"><dt>**GL\_DECR**</dt></span></span> </dl>          | <span data-ttu-id="77b64-123">Уменьшает значение текущего буфера набора элементов.</span><span class="sxs-lookup"><span data-stu-id="77b64-123">Decrements the current stencil buffer value.</span></span> <span data-ttu-id="77b64-124">Фиксации до нуля.</span><span class="sxs-lookup"><span data-stu-id="77b64-124">Clamps to zero.</span></span><br/>                                     |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <span data-ttu-id="77b64-125"><dt>**\_инверсия GL**</dt></span><span class="sxs-lookup"><span data-stu-id="77b64-125"><dt>**GL\_INVERT**</dt></span></span> </dl>    | <span data-ttu-id="77b64-126">Побитовое инвертирует значение текущего буфера набора элементов.</span><span class="sxs-lookup"><span data-stu-id="77b64-126">Bitwise inverts the current stencil buffer value.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="77b64-127">*зфаил*</span><span class="sxs-lookup"><span data-stu-id="77b64-127">*zfail*</span></span> 
</dt> <dd>

<span data-ttu-id="77b64-128">Действие трафарета при прохождении теста шаблона, но проверка глубины не удалась.</span><span class="sxs-lookup"><span data-stu-id="77b64-128">Stencil action when the stencil test passes, but the depth test fails.</span></span> <span data-ttu-id="77b64-129">Принимает те же символьные константы, что и *Fail.*</span><span class="sxs-lookup"><span data-stu-id="77b64-129">Accepts the same symbolic constants as *fail.*</span></span>

</dd> <dt>

<span data-ttu-id="77b64-130">*зпасс*</span><span class="sxs-lookup"><span data-stu-id="77b64-130">*zpass*</span></span> 
</dt> <dd>

<span data-ttu-id="77b64-131">Действие трафарета при прохождении как теста трафарета, так и тестового прохода, а также если отсутствует буфер глубины или не включено тестов глубины.</span><span class="sxs-lookup"><span data-stu-id="77b64-131">Stencil action when both the stencil test and the depth test pass, or when the stencil test passes and either there is no depth buffer or depth testing is not enabled.</span></span> <span data-ttu-id="77b64-132">Принимает те же символьные константы, что и *Fail*.</span><span class="sxs-lookup"><span data-stu-id="77b64-132">Accepts the same symbolic constants as *fail*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77b64-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77b64-133">Return value</span></span>

<span data-ttu-id="77b64-134">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="77b64-134">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="77b64-135">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="77b64-135">Error codes</span></span>

<span data-ttu-id="77b64-136">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="77b64-136">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="77b64-137">Имя</span><span class="sxs-lookup"><span data-stu-id="77b64-137">Name</span></span>                                                                                                  | <span data-ttu-id="77b64-138">Значение</span><span class="sxs-lookup"><span data-stu-id="77b64-138">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="77b64-139"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="77b64-139"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="77b64-140">*Fail*, *зфаил* или *зпасс* было любым значением, отличным от шести определенных значений констант.</span><span class="sxs-lookup"><span data-stu-id="77b64-140">*fail*, *zfail*, or *zpass* was any value other than the six defined constant values.</span></span><br/>                                      |
| <dl> <span data-ttu-id="77b64-141"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="77b64-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="77b64-142">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="77b64-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="77b64-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77b64-143">Remarks</span></span>

<span data-ttu-id="77b64-144">Набор элементов, например *z*-буферизация, включает и отключает рисование на уровне отдельных пикселов.</span><span class="sxs-lookup"><span data-stu-id="77b64-144">Stenciling, like *z*-buffering, enables and disables drawing on a per-pixel basis.</span></span> <span data-ttu-id="77b64-145">Вы рисуете на плоскости трафаретов с помощью примитивов рисования OpenGL, затем визуализируете геометрию и изображения, используя плоскости трафаретов для маскирования частей экрана.</span><span class="sxs-lookup"><span data-stu-id="77b64-145">You draw into the stencil planes using OpenGL drawing primitives, then render geometry and images, using the stencil planes to mask out portions of the screen.</span></span> <span data-ttu-id="77b64-146">Набор элементов обычно используется в алгоритмах многопроходной отрисовки для достижения специальных эффектов, таких как декалс, структурирование и конструктивностьная визуализация геометрических объектов.</span><span class="sxs-lookup"><span data-stu-id="77b64-146">Stenciling is typically used in multipass rendering algorithms to achieve special effects, such as decals, outlining, and constructive solid geometry rendering.</span></span>

<span data-ttu-id="77b64-147">Условие теста трафарета позволяет исключить пиксель на основе результата сравнения значения в буфере шаблона и ссылочного значения.</span><span class="sxs-lookup"><span data-stu-id="77b64-147">The stencil test conditionally eliminates a pixel based on the outcome of a comparison between the value in the stencil buffer and a reference value.</span></span> <span data-ttu-id="77b64-148">Тест включается с вызовами [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md) с аргументом \_ Test трафарета GL \_ и управляется с помощью [**глстенЦилфунк**](glstencilfunc.md).</span><span class="sxs-lookup"><span data-stu-id="77b64-148">The test is enabled with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) calls with argument GL\_STENCIL\_TEST, and controlled with [**glStencilFunc**](glstencilfunc.md).</span></span>

<span data-ttu-id="77b64-149">Функция **глстенЦилоп** принимает три аргумента, которые указывают, что происходит с сохраненным значением набора элементов при включенном наборе элементов.</span><span class="sxs-lookup"><span data-stu-id="77b64-149">The **glStencilOp** function takes three arguments that indicate what happens to the stored stencil value while stenciling is enabled.</span></span> <span data-ttu-id="77b64-150">Если проверка набора элементов завершается неудачно, в буферы цветов или глубины пикселя не вносятся изменения, а при *сбое* указывается, что происходит с содержимым буфера трафарета.</span><span class="sxs-lookup"><span data-stu-id="77b64-150">If the stencil test fails, no change is made to the pixel's color or depth buffers, and *fail* specifies what happens to the stencil buffer contents.</span></span>

<span data-ttu-id="77b64-151">Значения буфера наборов элементов рассматриваются как целые числа без знака.</span><span class="sxs-lookup"><span data-stu-id="77b64-151">Stencil buffer values are treated as unsigned integers.</span></span> <span data-ttu-id="77b64-152">При увеличении и уменьшении значения записываются в 0 и 2 *n* 1, где *n* — значение, возвращаемое запросом \_ битов трафарета GL \_ .</span><span class="sxs-lookup"><span data-stu-id="77b64-152">When incremented and decremented, values are clamped to 0 and 2 *n* 1, where *n* is the value returned by querying GL\_STENCIL\_BITS.</span></span>

<span data-ttu-id="77b64-153">Два других аргумента для **глстенЦилоп** указывают действия буфера набора элементов, если последующие тесты в буфере глубины выполнены успешно (*зпасс*) или Fail (*зфаил*).</span><span class="sxs-lookup"><span data-stu-id="77b64-153">The other two arguments to **glStencilOp** specify stencil buffer actions should subsequent depth buffer tests succeed (*zpass*) or fail (*zfail*).</span></span> <span data-ttu-id="77b64-154">(См. [**глдепсфунк**](gldepthfunc.md).) Они указываются с использованием тех же шести символьных констант, что и *Fail*.</span><span class="sxs-lookup"><span data-stu-id="77b64-154">(See [**glDepthFunc**](gldepthfunc.md).) They are specified using the same six symbolic constants as *fail*.</span></span> <span data-ttu-id="77b64-155">Обратите внимание, что *зфаил* игнорируется, если буфер глубины отсутствует или если буфер глубины не включен.</span><span class="sxs-lookup"><span data-stu-id="77b64-155">Note that *zfail* is ignored when there is no depth buffer, or when the depth buffer is not enabled.</span></span> <span data-ttu-id="77b64-156">В таких случаях команда *Fail* и *зпасс* Указание действия трафарета при сбое и прохождении теста трафарета соответственно.</span><span class="sxs-lookup"><span data-stu-id="77b64-156">In these cases, *fail* and *zpass* specify stencil action when the stencil test fails and passes, respectively.</span></span>

<span data-ttu-id="77b64-157">Изначально Проверка набора элементов отключена.</span><span class="sxs-lookup"><span data-stu-id="77b64-157">Initially the stencil test is disabled.</span></span> <span data-ttu-id="77b64-158">Если буфер трафарета отсутствует, изменение трафарета не может быть выполнено и так, как если бы набор элементов всегда прошел проверку, независимо от любого вызова **глстенЦилоп**.</span><span class="sxs-lookup"><span data-stu-id="77b64-158">If there is no stencil buffer, no stencil modification can occur and it is as if the stencil tests always pass, regardless of any call to **glStencilOp**.</span></span>

<span data-ttu-id="77b64-159">Следующие функции извлекают сведения, относящиеся к **глстенЦилоп**:</span><span class="sxs-lookup"><span data-stu-id="77b64-159">The following functions retrieve information related to **glStencilOp**:</span></span>

<span data-ttu-id="77b64-160">[**сбой глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ трафарета GL \_</span><span class="sxs-lookup"><span data-stu-id="77b64-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_FAIL</span></span>

<span data-ttu-id="77b64-161">**глжет** с аргументом \_ \_ \_ этап глубины прохода в трафарете \_</span><span class="sxs-lookup"><span data-stu-id="77b64-161">**glGet** with argument GL\_STENCIL\_PASS\_DEPTH\_PASS</span></span>

<span data-ttu-id="77b64-162">**сбой глжет** с аргументом \_ \_ \_ глубины этапа для шаблона GL \_</span><span class="sxs-lookup"><span data-stu-id="77b64-162">**glGet** with argument GL\_STENCIL\_PASS\_DEPTH\_FAIL</span></span>

<span data-ttu-id="77b64-163">**глжет** с аргументом \_ биты шаблона GL \_</span><span class="sxs-lookup"><span data-stu-id="77b64-163">**glGet** with argument GL\_STENCIL\_BITS</span></span>

<span data-ttu-id="77b64-164">[**глисенаблед**](glisenabled.md) с аргументом \_ Test трафарета GL \_</span><span class="sxs-lookup"><span data-stu-id="77b64-164">[**glIsEnabled**](glisenabled.md) with argument GL\_STENCIL\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="77b64-165">Требования</span><span class="sxs-lookup"><span data-stu-id="77b64-165">Requirements</span></span>



| <span data-ttu-id="77b64-166">Требование</span><span class="sxs-lookup"><span data-stu-id="77b64-166">Requirement</span></span> | <span data-ttu-id="77b64-167">Значение</span><span class="sxs-lookup"><span data-stu-id="77b64-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77b64-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77b64-168">Minimum supported client</span></span><br/> | <span data-ttu-id="77b64-169">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="77b64-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="77b64-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77b64-170">Minimum supported server</span></span><br/> | <span data-ttu-id="77b64-171">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="77b64-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77b64-172">Заголовок</span><span class="sxs-lookup"><span data-stu-id="77b64-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="77b64-173"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="77b64-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="77b64-174">Библиотека</span><span class="sxs-lookup"><span data-stu-id="77b64-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="77b64-175"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77b64-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="77b64-176">DLL</span><span class="sxs-lookup"><span data-stu-id="77b64-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77b64-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77b64-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77b64-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77b64-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77b64-179">**глалфафунк**</span><span class="sxs-lookup"><span data-stu-id="77b64-179">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="77b64-180">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="77b64-180">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="77b64-181">**глблендфунк**</span><span class="sxs-lookup"><span data-stu-id="77b64-181">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="77b64-182">**глдепсфунк**</span><span class="sxs-lookup"><span data-stu-id="77b64-182">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="77b64-183">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="77b64-183">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="77b64-184">**гленд**</span><span class="sxs-lookup"><span data-stu-id="77b64-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="77b64-185">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="77b64-185">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="77b64-186">**гллогикоп**</span><span class="sxs-lookup"><span data-stu-id="77b64-186">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="77b64-187">**глстенЦилфунк**</span><span class="sxs-lookup"><span data-stu-id="77b64-187">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





