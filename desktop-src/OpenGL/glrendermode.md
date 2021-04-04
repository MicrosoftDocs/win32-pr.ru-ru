---
title: Функция Глрендермоде (GL. h)
description: Функция Глрендермоде устанавливает режим растрирования.
ms.assetid: bcbc3bba-c552-425b-8284-6cadff0c9f56
keywords:
- Функция Глрендермоде OpenGL
topic_type:
- apiref
api_name:
- glRenderMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af07d2492d70f9c0a3a764d767b52b2f71204939
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137578"
---
# <a name="glrendermode-function"></a><span data-ttu-id="d1b9c-104">Функция Глрендермоде</span><span class="sxs-lookup"><span data-stu-id="d1b9c-104">glRenderMode function</span></span>

<span data-ttu-id="d1b9c-105">Функция **глрендермоде** устанавливает режим растрирования.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-105">The **glRenderMode** function sets the rasterization mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1b9c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1b9c-106">Syntax</span></span>


```C++
GLint WINAPI glRenderMode(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="d1b9c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1b9c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1b9c-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="d1b9c-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="d1b9c-109">Режим растрирования.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-109">The rasterization mode.</span></span> <span data-ttu-id="d1b9c-110">Принимаются следующие три значения.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-110">The following three values are accepted.</span></span> <span data-ttu-id="d1b9c-111">Значение по умолчанию — « \_ рендеринг GL».</span><span class="sxs-lookup"><span data-stu-id="d1b9c-111">The default value is GL\_RENDER.</span></span>



| <span data-ttu-id="d1b9c-112">Значение</span><span class="sxs-lookup"><span data-stu-id="d1b9c-112">Value</span></span>                                                                                                                                                   | <span data-ttu-id="d1b9c-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d1b9c-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_RENDER"></span><span id="gl_render"></span><dl> <span data-ttu-id="d1b9c-114"><dt>**\_рендеринг GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d1b9c-114"><dt>**GL\_RENDER**</dt></span></span> </dl>       | <span data-ttu-id="d1b9c-115">Режим рендеринга.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-115">Render mode.</span></span> <span data-ttu-id="d1b9c-116">Примитивы растрируются, создавая фрагменты пикселей, которые записываются в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-116">Primitives are rasterized, producing pixel fragments, which are written into the framebuffer.</span></span> <span data-ttu-id="d1b9c-117">Это нормальный режим, а также режим по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-117">This is the normal mode and also the default mode.</span></span><br/>                                                                                                                                                                                                      |
| <span id="GL_SELECT"></span><span id="gl_select"></span><dl> <span data-ttu-id="d1b9c-118"><dt>**\_Выбор GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d1b9c-118"><dt>**GL\_SELECT**</dt></span></span> </dl>       | <span data-ttu-id="d1b9c-119">Режим выбора.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-119">Selection mode.</span></span> <span data-ttu-id="d1b9c-120">Фрагменты пикселей не создаются и не вносятся изменения в содержимое буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-120">No pixel fragments are produced, and no change to the framebuffer contents is made.</span></span> <span data-ttu-id="d1b9c-121">Вместо этого в буфере SELECT возвращается запись с именами примитивов, которые были бы вырисованы, если был возвращен режим рендеринга GL \_ , который должен быть создан (см. [**глселектбуффер**](glselectbuffer.md)) перед входом в режим выбора.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-121">Instead, a record of the names of primitives that would have been drawn if the render mode was GL\_RENDER is returned in a select buffer, which must be created (see [**glSelectBuffer**](glselectbuffer.md)) before selection mode is entered.</span></span><br/>               |
| <span id="GL_FEEDBACK"></span><span id="gl_feedback"></span><dl> <span data-ttu-id="d1b9c-122"><dt>**\_обратная связь ГК**</dt></span><span class="sxs-lookup"><span data-stu-id="d1b9c-122"><dt>**GL\_FEEDBACK**</dt></span></span> </dl> | <span data-ttu-id="d1b9c-123">Режим обратной связи.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-123">Feedback mode.</span></span> <span data-ttu-id="d1b9c-124">Фрагменты пикселей не создаются и не вносятся изменения в содержимое буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-124">No pixel fragments are produced, and no change to the framebuffer contents is made.</span></span> <span data-ttu-id="d1b9c-125">Вместо этого координаты и атрибуты вершин, которые были бы прорисованы, были \_ возвращены в буфер обратной связи, который должен быть создан (см. [**глфидбаккбуффер**](glfeedbackbuffer.md)) перед входом в режим обратной связи.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-125">Instead, the coordinates and attributes of vertices that would have been drawn had the render mode been GL\_RENDER are returned in a feedback buffer, which must be created (see [**glFeedbackBuffer**](glfeedbackbuffer.md)) before feedback mode is entered.</span></span><br/> |



 

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="d1b9c-126">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d1b9c-126">Error codes</span></span>

<span data-ttu-id="d1b9c-127">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d1b9c-128">Имя</span><span class="sxs-lookup"><span data-stu-id="d1b9c-128">Name</span></span>                                                                                                  | <span data-ttu-id="d1b9c-129">Значение</span><span class="sxs-lookup"><span data-stu-id="d1b9c-129">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d1b9c-130"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d1b9c-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d1b9c-131">*режим* не является одним из трех допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-131">*mode* was not one of three accepted values.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="d1b9c-132"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d1b9c-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d1b9c-133">Функция была вызвана с аргументом GL \_ SELECT перед вызовом [**глселектбуффер**](glselectbuffer.md) по крайней мере один раз.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-133">The function was called with argument GL\_SELECT before [**glSelectBuffer**](glselectbuffer.md) was called at least once.</span></span><br/>       |
| <dl> <span data-ttu-id="d1b9c-134"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d1b9c-134"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d1b9c-135">Функция была вызвана с аргументом \_ Feedback GL до того, как [**глбидбаккбуффер**](glfeedbackbuffer.md) был вызван хотя бы один раз.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-135">The function was called with argument GL\_FEEDBACK before [**glBeedbackBuffer**](glfeedbackbuffer.md) was called at least once.</span></span><br/> |
| <dl> <span data-ttu-id="d1b9c-136"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d1b9c-136"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d1b9c-137">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="d1b9c-137">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="d1b9c-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1b9c-138">Remarks</span></span>

<span data-ttu-id="d1b9c-139">Функция **глрендермоде** принимает один аргумент *mode*, который может принимать одно из трех предварительно определенных значений.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-139">The **glRenderMode** function takes one argument, *mode*, which can assume one of three predefined values above.</span></span>

<span data-ttu-id="d1b9c-140">Возвращаемое значение функции **глрендермоде** определяется режимом рендеринга во время вызова **глрендермоде** , а не в *режиме*.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-140">The return value of the **glRenderMode** function is determined by the render mode at the time **glRenderMode** is called, rather than by *mode*.</span></span> <span data-ttu-id="d1b9c-141">Ниже приведены значения, возвращаемые для трех режимов рендеринга.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-141">The values returned for the three render modes are as follows.</span></span>



| <span data-ttu-id="d1b9c-142">Значение</span><span class="sxs-lookup"><span data-stu-id="d1b9c-142">Value</span></span>        | <span data-ttu-id="d1b9c-143">Значение</span><span class="sxs-lookup"><span data-stu-id="d1b9c-143">Meaning</span></span>                                                                 |
|--------------|-------------------------------------------------------------------------|
| <span data-ttu-id="d1b9c-144">\_рендеринг GL</span><span class="sxs-lookup"><span data-stu-id="d1b9c-144">GL\_RENDER</span></span>   | <span data-ttu-id="d1b9c-145">Ноль.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-145">Zero.</span></span>                                                                   |
| <span data-ttu-id="d1b9c-146">\_Выбор GL</span><span class="sxs-lookup"><span data-stu-id="d1b9c-146">GL\_SELECT</span></span>   | <span data-ttu-id="d1b9c-147">Число записей об попадании, передаваемых в буфер SELECT.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-147">The number of hit records transferred to the select buffer.</span></span>             |
| <span data-ttu-id="d1b9c-148">\_обратная связь ГК</span><span class="sxs-lookup"><span data-stu-id="d1b9c-148">GL\_FEEDBACK</span></span> | <span data-ttu-id="d1b9c-149">Количество значений (не вершин), передаваемых в буфер обратной связи.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-149">The number of values (not vertices) transferred to the feedback buffer.</span></span> |



 

<span data-ttu-id="d1b9c-150">Дополнительные сведения о выборе и операциях обратной связи см. в разделе [**глселектбуффер**](glselectbuffer.md) и [**глфидбаккбуффер**](glfeedbackbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="d1b9c-150">Refer to [**glSelectBuffer**](glselectbuffer.md) and [**glFeedbackBuffer**](glfeedbackbuffer.md) for more details concerning selection and feedback operation.</span></span>

<span data-ttu-id="d1b9c-151">Если возникает ошибка, **глрендермоде** возвращает ноль независимо от текущего режима рендеринга.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-151">If an error is generated, **glRenderMode** returns zero regardless of the current render mode.</span></span>

<span data-ttu-id="d1b9c-152">Следующая функция получает сведения, связанные с **глрендермоде**:</span><span class="sxs-lookup"><span data-stu-id="d1b9c-152">The following function retrieves information related to **glRenderMode**:</span></span>

<span data-ttu-id="d1b9c-153">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ режим рендеринга GL \_</span><span class="sxs-lookup"><span data-stu-id="d1b9c-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="d1b9c-154">Требования</span><span class="sxs-lookup"><span data-stu-id="d1b9c-154">Requirements</span></span>



| <span data-ttu-id="d1b9c-155">Требование</span><span class="sxs-lookup"><span data-stu-id="d1b9c-155">Requirement</span></span> | <span data-ttu-id="d1b9c-156">Значение</span><span class="sxs-lookup"><span data-stu-id="d1b9c-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b9c-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1b9c-157">Minimum supported client</span></span><br/> | <span data-ttu-id="d1b9c-158">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d1b9c-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d1b9c-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1b9c-159">Minimum supported server</span></span><br/> | <span data-ttu-id="d1b9c-160">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d1b9c-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d1b9c-161">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d1b9c-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1b9c-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1b9c-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d1b9c-163">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d1b9c-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="d1b9c-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1b9c-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d1b9c-165">DLL</span><span class="sxs-lookup"><span data-stu-id="d1b9c-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1b9c-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1b9c-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1b9c-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1b9c-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1b9c-168">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="d1b9c-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d1b9c-169">**гленд**</span><span class="sxs-lookup"><span data-stu-id="d1b9c-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d1b9c-170">**глфидбаккбуффер**</span><span class="sxs-lookup"><span data-stu-id="d1b9c-170">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="d1b9c-171">**глинитнамес**</span><span class="sxs-lookup"><span data-stu-id="d1b9c-171">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="d1b9c-172">**гллоаднаме**</span><span class="sxs-lookup"><span data-stu-id="d1b9c-172">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="d1b9c-173">**глпасссраугх**</span><span class="sxs-lookup"><span data-stu-id="d1b9c-173">**glPassThrough**</span></span>](glpassthrough.md)
</dt> <dt>

[<span data-ttu-id="d1b9c-174">**глпушнаме**</span><span class="sxs-lookup"><span data-stu-id="d1b9c-174">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="d1b9c-175">**глселектбуффер**</span><span class="sxs-lookup"><span data-stu-id="d1b9c-175">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





