---
title: Функция Гллогикоп (GL. h)
description: Функция Гллогикоп задает операцию логического пикселя для подготовки к просмотру цветового индекса.
ms.assetid: 29edf9bd-f3b8-4de7-9afb-07714f4efd92
keywords:
- Функция Гллогикоп OpenGL
topic_type:
- apiref
api_name:
- glLogicOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb29e8f845e99f6d3c988dfd0c0201de129bee69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535513"
---
# <a name="gllogicop-function"></a><span data-ttu-id="341fe-104">Функция Гллогикоп</span><span class="sxs-lookup"><span data-stu-id="341fe-104">glLogicOp function</span></span>

<span data-ttu-id="341fe-105">Функция **гллогикоп** задает операцию логического пикселя для подготовки к просмотру цветового индекса.</span><span class="sxs-lookup"><span data-stu-id="341fe-105">The **glLogicOp** function specifies a logical pixel operation for color index rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="341fe-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="341fe-106">Syntax</span></span>


```C++
void WINAPI glLogicOp(
   GLenum opcode
);
```



## <a name="parameters"></a><span data-ttu-id="341fe-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="341fe-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="341fe-108">*транслируют*</span><span class="sxs-lookup"><span data-stu-id="341fe-108">*opcode*</span></span> 
</dt> <dd>

<span data-ttu-id="341fe-109">Символьная константа, выбирающая логическую операцию.</span><span class="sxs-lookup"><span data-stu-id="341fe-109">A symbolic constant that selects a logical operation.</span></span> <span data-ttu-id="341fe-110">Следующие символы принимаются, где s равно значению исходного бита, а d — значение бита назначения.</span><span class="sxs-lookup"><span data-stu-id="341fe-110">The following symbols are accepted where s equals the value of the source bit and d is the value of the destination bit.</span></span>



| <span data-ttu-id="341fe-111">Значение</span><span class="sxs-lookup"><span data-stu-id="341fe-111">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="341fe-112">Значение</span><span class="sxs-lookup"><span data-stu-id="341fe-112">Meaning</span></span>              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="GL_CLEAR"></span><span id="gl_clear"></span><dl> <span data-ttu-id="341fe-113"><dt>**\_Очистка GL**</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-113"><dt>**GL\_CLEAR**</dt></span></span> </dl>                          | <span data-ttu-id="341fe-114">0</span><span class="sxs-lookup"><span data-stu-id="341fe-114">0</span></span><br/>         |
| <span id="GL_SET"></span><span id="gl_set"></span><dl> <span data-ttu-id="341fe-115"><dt>**\_набор GL**</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-115"><dt>**GL\_SET**</dt></span></span> </dl>                                | <span data-ttu-id="341fe-116">1</span><span class="sxs-lookup"><span data-stu-id="341fe-116">1</span></span><br/>         |
| <span id="GL_COPY"></span><span id="gl_copy"></span><dl> <span data-ttu-id="341fe-117"><dt>**копирование в ГК \_**</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-117"><dt>**GL\_COPY**</dt></span></span> </dl>                             | <span data-ttu-id="341fe-118">s</span><span class="sxs-lookup"><span data-stu-id="341fe-118">s</span></span><br/>         |
| <span id="GL_COPY_INVERTED"></span><span id="gl_copy_inverted"></span><dl> <span data-ttu-id="341fe-119"><dt>**\_Инвертированное копирование в ГК \_**</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-119"><dt>**GL\_COPY\_INVERTED**</dt></span></span> </dl> | <span data-ttu-id="341fe-120">! s</span><span class="sxs-lookup"><span data-stu-id="341fe-120">!s</span></span><br/>        |
| <span id="GL_NOOP"></span><span id="gl_noop"></span><dl> <span data-ttu-id="341fe-121"><dt>**NOOP в ГК \_**</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-121"><dt>**GL\_NOOP**</dt></span></span> </dl>                             | <span data-ttu-id="341fe-122">d</span><span class="sxs-lookup"><span data-stu-id="341fe-122">d</span></span><br/>         |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <span data-ttu-id="341fe-123"><dt>**\_инверсия GL**</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-123"><dt>**GL\_INVERT**</dt></span></span> </dl>                       | <span data-ttu-id="341fe-124">! d</span><span class="sxs-lookup"><span data-stu-id="341fe-124">!d</span></span><br/>        |
| <span id="GL_AND"></span><span id="gl_and"></span><dl> <span data-ttu-id="341fe-125"><dt>**GL \_ и**</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-125"><dt>**GL\_AND**</dt></span></span> </dl>                                | <span data-ttu-id="341fe-126">s & d</span><span class="sxs-lookup"><span data-stu-id="341fe-126">s & d</span></span><br/>     |
| <span id="GL_NAND"></span><span id="gl_nand"></span><dl> <span data-ttu-id="341fe-127"><dt>**\_NИ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-127"><dt>**GL\_NAND**</dt></span></span> </dl>                             | <span data-ttu-id="341fe-128">! (s & d)</span><span class="sxs-lookup"><span data-stu-id="341fe-128">!(s & d)</span></span><br/>  |
| <span id="GL_OR"></span><span id="gl_or"></span><dl> <span data-ttu-id="341fe-129"><dt>**GL \_ или**</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-129"><dt>**GL\_OR**</dt></span></span> </dl>                                   | <span data-ttu-id="341fe-130">с \| d</span><span class="sxs-lookup"><span data-stu-id="341fe-130">s \| d</span></span><br/>    |
| <span id="GL_NOR"></span><span id="gl_nor"></span><dl> <span data-ttu-id="341fe-131"><dt>**GL \_ или**</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-131"><dt>**GL\_NOR**</dt></span></span> </dl>                                | <span data-ttu-id="341fe-132">! (s \| d)</span><span class="sxs-lookup"><span data-stu-id="341fe-132">!(s \| d)</span></span><br/> |
| <span id="GL_XOR"></span><span id="gl_xor"></span><dl> <span data-ttu-id="341fe-133"><dt>**GL ( \_ XOR)**</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-133"><dt>**GL\_XOR**</dt></span></span> </dl>                                | <span data-ttu-id="341fe-134">s ^ d</span><span class="sxs-lookup"><span data-stu-id="341fe-134">s ^ d</span></span><br/>     |
| <span id="GL_EQUIV"></span><span id="gl_equiv"></span><dl> <span data-ttu-id="341fe-135"><dt>**GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-135"><dt>**GL\_EQUIV**</dt></span></span> </dl>                          | <span data-ttu-id="341fe-136">! (s ^ d)</span><span class="sxs-lookup"><span data-stu-id="341fe-136">!(s ^ d)</span></span><br/>  |
| <span id="GL_AND_REVERSE"></span><span id="gl_and_reverse"></span><dl> <span data-ttu-id="341fe-137"><dt>**GL \_ и \_ Reverse**</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-137"><dt>**GL\_AND\_REVERSE**</dt></span></span> </dl>       | <span data-ttu-id="341fe-138">s &! d</span><span class="sxs-lookup"><span data-stu-id="341fe-138">s & !d</span></span><br/>    |
| <span id="GL_AND_INVERTED"></span><span id="gl_and_inverted"></span><dl> <span data-ttu-id="341fe-139"><dt>**GL \_ и \_ инверсия**</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-139"><dt>**GL\_AND\_INVERTED**</dt></span></span> </dl>    | <span data-ttu-id="341fe-140">! s & d</span><span class="sxs-lookup"><span data-stu-id="341fe-140">!s & d</span></span><br/>    |
| <span id="GL_OR_REVERSE"></span><span id="gl_or_reverse"></span><dl> <span data-ttu-id="341fe-141"><dt>**GL \_ или \_ Reverse**</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-141"><dt>**GL\_OR\_REVERSE**</dt></span></span> </dl>          | <span data-ttu-id="341fe-142">s \| ! d</span><span class="sxs-lookup"><span data-stu-id="341fe-142">s \| !d</span></span><br/>   |
| <span id="GL_OR_INVERTED"></span><span id="gl_or_inverted"></span><dl> <span data-ttu-id="341fe-143"><dt>**GL \_ или \_ инверсия**</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-143"><dt>**GL\_OR\_INVERTED**</dt></span></span> </dl>       | <span data-ttu-id="341fe-144">! s \| d</span><span class="sxs-lookup"><span data-stu-id="341fe-144">!s \| d</span></span><br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="341fe-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="341fe-145">Return value</span></span>

<span data-ttu-id="341fe-146">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="341fe-146">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="341fe-147">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="341fe-147">Error codes</span></span>

<span data-ttu-id="341fe-148">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="341fe-148">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="341fe-149">Имя</span><span class="sxs-lookup"><span data-stu-id="341fe-149">Name</span></span>                                                                                                  | <span data-ttu-id="341fe-150">Значение</span><span class="sxs-lookup"><span data-stu-id="341fe-150">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="341fe-151"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-151"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="341fe-152">*код операции* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="341fe-152">*opcode* was not an accepted value.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="341fe-153"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-153"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="341fe-154">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="341fe-154">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="341fe-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="341fe-155">Remarks</span></span>

<span data-ttu-id="341fe-156">Функция **гллогикоп** задает логическую операцию, которая, если она включена, применяется между входящим индексом цвета и индексом цвета в соответствующем расположении в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="341fe-156">The **glLogicOp** function specifies a logical operation that, when enabled, is applied between the incoming color index and the color index at the corresponding location in the framebuffer.</span></span> <span data-ttu-id="341fe-157">Логическая операция включена или отключена с помощью [**гленабле**](glenable.md) и **глдисабле** с использованием символьной константы главной операции GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="341fe-157">The logical operation is enabled or disabled with [**glEnable**](glenable.md) and **glDisable** using the symbolic constant GL\_LOGIC\_OP.</span></span>

<span data-ttu-id="341fe-158">Параметр *кода операции* — это символьная константа, выбранная из списка ниже.</span><span class="sxs-lookup"><span data-stu-id="341fe-158">The *opcode* parameter is a symbolic constant chosen from the list below.</span></span> <span data-ttu-id="341fe-159">В объяснении логических операций *s* представляет индекс входящего цвета, а *d* — индекс в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="341fe-159">In the explanation of the logical operations, *s* represents the incoming color index and *d* represents the index in the framebuffer.</span></span> <span data-ttu-id="341fe-160">Используются стандартные операторы языка C.</span><span class="sxs-lookup"><span data-stu-id="341fe-160">Standard C-language operators are used.</span></span> <span data-ttu-id="341fe-161">Как и в этих побитовых операторах, логическая операция применяется независимо к каждой паре битов исходного и конечного индексов.</span><span class="sxs-lookup"><span data-stu-id="341fe-161">As these bitwise operators suggest, the logical operation is applied independently to each bit pair of the source and destination indexes.</span></span>

<span data-ttu-id="341fe-162">Операции логического пикселя не применяются к буферам цветов RGBA.</span><span class="sxs-lookup"><span data-stu-id="341fe-162">Logical pixel operations are not applied to RGBA color buffers.</span></span>

<span data-ttu-id="341fe-163">Если для рисования включено более одного буфера цветового индекса, логические операции выполняются отдельно для каждого включенного буфера с использованием содержимого этого буфера для индекса назначения (см. [**глдравбуффер**](gldrawbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="341fe-163">When more than one color-index buffer is enabled for drawing, logical operations are done separately for each enabled buffer, using the contents of that buffer for the destination index (see [**glDrawBuffer**](gldrawbuffer.md)).</span></span>

<span data-ttu-id="341fe-164">Параметр *кода операции* должен быть одним из 16 допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="341fe-164">The *opcode* parameter must be one of the 16 accepted values.</span></span> <span data-ttu-id="341fe-165">Другие значения приводят к ошибке.</span><span class="sxs-lookup"><span data-stu-id="341fe-165">Other values result in an error.</span></span>

<span data-ttu-id="341fe-166">Следующие функции извлекают сведения, относящиеся к **гллогикоп**:</span><span class="sxs-lookup"><span data-stu-id="341fe-166">The following functions retrieve information related to **glLogicOp**:</span></span>

<span data-ttu-id="341fe-167">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ режим ЛОГИКи операций GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="341fe-167">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LOGIC\_OP\_MODE</span></span>

<span data-ttu-id="341fe-168">[**глисенаблед**](glisenabled.md) с аргументом \_ ЛОГИКа операции GL \_</span><span class="sxs-lookup"><span data-stu-id="341fe-168">[**glIsEnabled**](glisenabled.md) with argument GL\_LOGIC\_OP</span></span>

## <a name="requirements"></a><span data-ttu-id="341fe-169">Требования</span><span class="sxs-lookup"><span data-stu-id="341fe-169">Requirements</span></span>



| <span data-ttu-id="341fe-170">Требование</span><span class="sxs-lookup"><span data-stu-id="341fe-170">Requirement</span></span> | <span data-ttu-id="341fe-171">Значение</span><span class="sxs-lookup"><span data-stu-id="341fe-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="341fe-172">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="341fe-172">Minimum supported client</span></span><br/> | <span data-ttu-id="341fe-173">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="341fe-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="341fe-174">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="341fe-174">Minimum supported server</span></span><br/> | <span data-ttu-id="341fe-175">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="341fe-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="341fe-176">Заголовок</span><span class="sxs-lookup"><span data-stu-id="341fe-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="341fe-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="341fe-178">Библиотека</span><span class="sxs-lookup"><span data-stu-id="341fe-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="341fe-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="341fe-180">DLL</span><span class="sxs-lookup"><span data-stu-id="341fe-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="341fe-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="341fe-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="341fe-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="341fe-183">**глалфафунк**</span><span class="sxs-lookup"><span data-stu-id="341fe-183">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="341fe-184">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="341fe-184">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="341fe-185">**глблендфунк**</span><span class="sxs-lookup"><span data-stu-id="341fe-185">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="341fe-186">**глдравбуффер**</span><span class="sxs-lookup"><span data-stu-id="341fe-186">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="341fe-187">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="341fe-187">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="341fe-188">**гленд**</span><span class="sxs-lookup"><span data-stu-id="341fe-188">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="341fe-189">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="341fe-189">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="341fe-190">**глстенЦилоп**</span><span class="sxs-lookup"><span data-stu-id="341fe-190">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





