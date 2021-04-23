---
title: Функция Глалфафунк (GL. h)
description: Функция Глалфафунк позволяет приложению задать функцию тестирования Alpha.
ms.assetid: 6c0c06b5-1bad-4590-a262-f134f63f0936
keywords:
- Функция Глалфафунк OpenGL
topic_type:
- apiref
api_name:
- glAlphaFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf96cfe2be0224c9c2e2409fc68805b530ae1f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681915"
---
# <a name="glalphafunc-function"></a><span data-ttu-id="dbba9-104">Функция Глалфафунк</span><span class="sxs-lookup"><span data-stu-id="dbba9-104">glAlphaFunc function</span></span>

<span data-ttu-id="dbba9-105">Функция **глалфафунк** позволяет приложению задать функцию тестирования Alpha.</span><span class="sxs-lookup"><span data-stu-id="dbba9-105">The **glAlphaFunc** function enables your application to set the alpha test function.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbba9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbba9-106">Syntax</span></span>


```C++
void WINAPI glAlphaFunc(
   GLenum   func,
   GLclampf ref
);
```



## <a name="parameters"></a><span data-ttu-id="dbba9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbba9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbba9-108">*func*</span><span class="sxs-lookup"><span data-stu-id="dbba9-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="dbba9-109">Функция сравнения альфа.</span><span class="sxs-lookup"><span data-stu-id="dbba9-109">The alpha comparison function.</span></span> <span data-ttu-id="dbba9-110">Ниже приведены допустимые символьные константы и их значения.</span><span class="sxs-lookup"><span data-stu-id="dbba9-110">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="dbba9-111">Значение</span><span class="sxs-lookup"><span data-stu-id="dbba9-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="dbba9-112">Значение</span><span class="sxs-lookup"><span data-stu-id="dbba9-112">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="dbba9-113"><dt>**ГК \_ никогда**</dt></span><span class="sxs-lookup"><span data-stu-id="dbba9-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="dbba9-114">Никогда не передает.</span><span class="sxs-lookup"><span data-stu-id="dbba9-114">Never passes.</span></span><br/>                                                                       |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="dbba9-115"><dt>**\_меньше ГК**</dt></span><span class="sxs-lookup"><span data-stu-id="dbba9-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="dbba9-116">Передает, если значение входящего альфа-канала меньше значения ссылки.</span><span class="sxs-lookup"><span data-stu-id="dbba9-116">Passes if the incoming alpha value is less than the reference value.</span></span><br/>                |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="dbba9-117"><dt>**значение GL \_ равно**</dt></span><span class="sxs-lookup"><span data-stu-id="dbba9-117"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="dbba9-118">Передает, если значение входящего альфа-канала равно значению ссылки.</span><span class="sxs-lookup"><span data-stu-id="dbba9-118">Passes if the incoming alpha value is equal to the reference value.</span></span><br/>                 |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="dbba9-119"><dt>**\_ЛЕКУАЛ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="dbba9-119"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="dbba9-120">Передает, если значение входящего альфа-канала меньше или равно значению ссылки.</span><span class="sxs-lookup"><span data-stu-id="dbba9-120">Passes if the incoming alpha value is less than or equal to the reference value.</span></span><br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="dbba9-121"><dt>**в \_ ГК**</dt></span><span class="sxs-lookup"><span data-stu-id="dbba9-121"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="dbba9-122">Передает, если значение входящего альфа-канала больше значения ссылки.</span><span class="sxs-lookup"><span data-stu-id="dbba9-122">Passes if the incoming alpha value is greater than the reference value.</span></span><br/>             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="dbba9-123"><dt>**\_NOTEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="dbba9-123"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="dbba9-124">Передает, если значение входящего альфа-канала не равно значению ссылки.</span><span class="sxs-lookup"><span data-stu-id="dbba9-124">Passes if the incoming alpha value is not equal to the reference value.</span></span><br/>             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="dbba9-125"><dt>**\_ЖЕКУАЛ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="dbba9-125"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="dbba9-126">Передает, если значение входящего альфа-канала больше или равно значению ссылки.</span><span class="sxs-lookup"><span data-stu-id="dbba9-126">Passes if the incoming alpha value is greater than or equal to the reference value.</span></span><br/> |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="dbba9-127"><dt>**GL \_ всегда**</dt></span><span class="sxs-lookup"><span data-stu-id="dbba9-127"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="dbba9-128">Всегда передает.</span><span class="sxs-lookup"><span data-stu-id="dbba9-128">Always passes.</span></span> <span data-ttu-id="dbba9-129">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dbba9-129">This is the default.</span></span><br/>                                                 |



 

</dd> <dt>

<span data-ttu-id="dbba9-130">*ref*</span><span class="sxs-lookup"><span data-stu-id="dbba9-130">*ref*</span></span> 
</dt> <dd>

<span data-ttu-id="dbba9-131">Ссылочное значение, на которое сравниваются входящие альфа-значения.</span><span class="sxs-lookup"><span data-stu-id="dbba9-131">The reference value to which incoming alpha values are compared.</span></span> <span data-ttu-id="dbba9-132">Это значение задается в диапазоне от 0 до 1, где 0 представляет наименьшее возможное альфа-значение и 1 наибольшее возможное значение.</span><span class="sxs-lookup"><span data-stu-id="dbba9-132">This value is clamped to the range 0 through 1, where 0 represents the lowest possible alpha value and 1 the highest possible value.</span></span> <span data-ttu-id="dbba9-133">Ссылка по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="dbba9-133">The default reference is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbba9-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbba9-134">Return value</span></span>

<span data-ttu-id="dbba9-135">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="dbba9-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dbba9-136">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="dbba9-136">Error codes</span></span>

<span data-ttu-id="dbba9-137">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="dbba9-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="dbba9-138">Имя</span><span class="sxs-lookup"><span data-stu-id="dbba9-138">Name</span></span>                                                                                                  | <span data-ttu-id="dbba9-139">Значение</span><span class="sxs-lookup"><span data-stu-id="dbba9-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dbba9-140"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="dbba9-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="dbba9-141">Функция *Func* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="dbba9-141">*func* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="dbba9-142"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="dbba9-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="dbba9-143">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="dbba9-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="dbba9-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbba9-144">Remarks</span></span>

<span data-ttu-id="dbba9-145">Альфа-тест отклоняет фрагменты в зависимости от результата сравнения альфа-значений входящих фрагментов и константного значения ссылки.</span><span class="sxs-lookup"><span data-stu-id="dbba9-145">The alpha test discards fragments depending on the outcome of a comparison between the incoming fragments' alpha values and a constant reference value.</span></span> <span data-ttu-id="dbba9-146">Функция **глалфафунк** задает ссылку и функцию сравнения.</span><span class="sxs-lookup"><span data-stu-id="dbba9-146">The **glAlphaFunc** function specifies the reference and comparison function.</span></span> <span data-ttu-id="dbba9-147">Сравнение выполняется только в том случае, если включено тестирование альфа-версии.</span><span class="sxs-lookup"><span data-stu-id="dbba9-147">The comparison is performed only if alpha testing is enabled.</span></span> <span data-ttu-id="dbba9-148">(Дополнительные сведения о GL \_ \_Тест Alpha см. в разделе [**гленабле**](glenable.md).)</span><span class="sxs-lookup"><span data-stu-id="dbba9-148">(For more information on GL\_ALPHA\_TEST, see [**glEnable**](glenable.md).)</span></span>

<span data-ttu-id="dbba9-149">Параметры *Func* и *ref* определяют условия, при которых рисуется пиксель.</span><span class="sxs-lookup"><span data-stu-id="dbba9-149">The *func* and *ref* parameters specify the conditions under which the pixel is drawn.</span></span> <span data-ttu-id="dbba9-150">Входящее альфа-значение сравнивается с *ref* с помощью функции, заданной функцией *Func*.</span><span class="sxs-lookup"><span data-stu-id="dbba9-150">The incoming alpha value is compared to *ref* using the function specified by *func*.</span></span> <span data-ttu-id="dbba9-151">Если сравнение прошло успешно, входящий фрагмент рисуется, условный на последующие тесты набора элементов и глубины буфера.</span><span class="sxs-lookup"><span data-stu-id="dbba9-151">If the comparison passes, the incoming fragment is drawn, conditional on subsequent stencil and depth-buffer tests.</span></span> <span data-ttu-id="dbba9-152">Если сравнение завершается неудачно, в буфера кадров в этом месте не вносится никаких изменений.</span><span class="sxs-lookup"><span data-stu-id="dbba9-152">If the comparison fails, no change is made to the framebuffer at that pixel location.</span></span>

<span data-ttu-id="dbba9-153">Функция **глалфафунк** работает со всеми операциями записи в пикселях, включая те, что были результатом сканирования при преобразовании точек, линий, многоугольников и точечных рисунков, а также из операций рисования и копирования пикселей.</span><span class="sxs-lookup"><span data-stu-id="dbba9-153">The **glAlphaFunc** function operates on all pixel writes, including those resulting from the scan conversion of points, lines, polygons, and bitmaps, and from pixel draw and copy operations.</span></span> <span data-ttu-id="dbba9-154">Функция **глалфафунк** не влияет на операции очистки экрана.</span><span class="sxs-lookup"><span data-stu-id="dbba9-154">The **glAlphaFunc** function does not affect screen clear operations.</span></span>

<span data-ttu-id="dbba9-155">Альфа-тестирование выполняется только в режиме RGBA.</span><span class="sxs-lookup"><span data-stu-id="dbba9-155">Alpha testing is done only in RGBA mode.</span></span>

<span data-ttu-id="dbba9-156">Следующие функции извлекают сведения, относящиеся к функции **глалфафунк** :</span><span class="sxs-lookup"><span data-stu-id="dbba9-156">The following functions retrieve information related to the **glAlphaFunc** function:</span></span>

<span data-ttu-id="dbba9-157">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ альфа \_ Test \_ Func</span><span class="sxs-lookup"><span data-stu-id="dbba9-157">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ALPHA\_TEST\_FUNC</span></span>

<span data-ttu-id="dbba9-158">**глжет** с аргументом " \_ альфа- \_ \_ ссылка теста GL"</span><span class="sxs-lookup"><span data-stu-id="dbba9-158">**glGet** with argument GL\_ALPHA\_TEST\_REF</span></span>

<span data-ttu-id="dbba9-159">[**глисенаблед**](glisenabled.md) с аргументом " \_ альфа- \_ Тест"</span><span class="sxs-lookup"><span data-stu-id="dbba9-159">[**glIsEnabled**](glisenabled.md) with argument GL\_ALPHA\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="dbba9-160">Требования</span><span class="sxs-lookup"><span data-stu-id="dbba9-160">Requirements</span></span>



| <span data-ttu-id="dbba9-161">Требование</span><span class="sxs-lookup"><span data-stu-id="dbba9-161">Requirement</span></span> | <span data-ttu-id="dbba9-162">Значение</span><span class="sxs-lookup"><span data-stu-id="dbba9-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbba9-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dbba9-163">Minimum supported client</span></span><br/> | <span data-ttu-id="dbba9-164">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dbba9-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="dbba9-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dbba9-165">Minimum supported server</span></span><br/> | <span data-ttu-id="dbba9-166">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dbba9-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dbba9-167">Заголовок</span><span class="sxs-lookup"><span data-stu-id="dbba9-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbba9-168"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbba9-168"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="dbba9-169">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dbba9-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="dbba9-170"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbba9-170"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="dbba9-171">DLL</span><span class="sxs-lookup"><span data-stu-id="dbba9-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbba9-172"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbba9-172"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbba9-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbba9-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbba9-174">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="dbba9-174">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="dbba9-175">**глблендфунк**</span><span class="sxs-lookup"><span data-stu-id="dbba9-175">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="dbba9-176">**глклеар**</span><span class="sxs-lookup"><span data-stu-id="dbba9-176">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="dbba9-177">**глдепсфунк**</span><span class="sxs-lookup"><span data-stu-id="dbba9-177">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="dbba9-178">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="dbba9-178">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="dbba9-179">**гленд**</span><span class="sxs-lookup"><span data-stu-id="dbba9-179">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="dbba9-180">**глжет**</span><span class="sxs-lookup"><span data-stu-id="dbba9-180">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="dbba9-181">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="dbba9-181">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="dbba9-182">**глстенЦилфунк**</span><span class="sxs-lookup"><span data-stu-id="dbba9-182">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





