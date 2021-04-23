---
title: Функция Глневлист (GL. h)
description: Функции Глневлист и Глендлист создают или заменяют список отображений. | Функция Глневлист (GL. h)
ms.assetid: 9c6556d4-855f-4cba-94cc-27b5f1e4607a
keywords:
- Функция Глневлист OpenGL
topic_type:
- apiref
api_name:
- glNewList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6135f67c07f69d24df67d4f1899404359efaa7aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664915"
---
# <a name="glnewlist-function"></a><span data-ttu-id="57f9e-105">Функция Глневлист</span><span class="sxs-lookup"><span data-stu-id="57f9e-105">glNewList function</span></span>

<span data-ttu-id="57f9e-106">Функции **глневлист** и [**глендлист**](glendlist.md) создают или заменяют список отображений.</span><span class="sxs-lookup"><span data-stu-id="57f9e-106">The **glNewList** and [**glEndList**](glendlist.md) functions create or replace a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="57f9e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57f9e-107">Syntax</span></span>


```C++
void WINAPI glNewList(
   GLuint list,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="57f9e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="57f9e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57f9e-109">*list*</span><span class="sxs-lookup"><span data-stu-id="57f9e-109">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="57f9e-110">Имя списка отображаемых имен.</span><span class="sxs-lookup"><span data-stu-id="57f9e-110">The display list name.</span></span>

</dd> <dt>

<span data-ttu-id="57f9e-111">*mode*</span><span class="sxs-lookup"><span data-stu-id="57f9e-111">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="57f9e-112">Режим компиляции.</span><span class="sxs-lookup"><span data-stu-id="57f9e-112">The compilation mode.</span></span> <span data-ttu-id="57f9e-113">Принимаются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="57f9e-113">The following values are accepted.</span></span>



| <span data-ttu-id="57f9e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="57f9e-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="57f9e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="57f9e-115">Meaning</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="GL_COMPILE"></span><span id="gl_compile"></span><dl> <span data-ttu-id="57f9e-116"><dt>**\_Компиляция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="57f9e-116"><dt>**GL\_COMPILE**</dt></span></span> </dl>                                       | <span data-ttu-id="57f9e-117">Команды компилируются просто.</span><span class="sxs-lookup"><span data-stu-id="57f9e-117">Commands are merely compiled.</span></span><br/>                                     |
| <span id="GL_COMPILE_AND_EXECUTE"></span><span id="gl_compile_and_execute"></span><dl> <span data-ttu-id="57f9e-118"><dt>**\_Компиляция \_ и \_ выполнение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="57f9e-118"><dt>**GL\_COMPILE\_AND\_EXECUTE**</dt></span></span> </dl> | <span data-ttu-id="57f9e-119">Команды выполняются по мере их компиляции в список отображение.</span><span class="sxs-lookup"><span data-stu-id="57f9e-119">Commands are executed as they are compiled into the display list.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57f9e-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="57f9e-120">Return value</span></span>

<span data-ttu-id="57f9e-121">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="57f9e-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="57f9e-122">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="57f9e-122">Error codes</span></span>

<span data-ttu-id="57f9e-123">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="57f9e-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="57f9e-124">Имя</span><span class="sxs-lookup"><span data-stu-id="57f9e-124">Name</span></span>                                                                                                  | <span data-ttu-id="57f9e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="57f9e-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="57f9e-126"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="57f9e-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="57f9e-127">*список* равен нулю.</span><span class="sxs-lookup"><span data-stu-id="57f9e-127">*list* was zero.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="57f9e-128"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="57f9e-128"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="57f9e-129">*режим* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="57f9e-129">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="57f9e-130"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="57f9e-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="57f9e-131">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="57f9e-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="57f9e-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="57f9e-132">Remarks</span></span>

<span data-ttu-id="57f9e-133">Списки отображений — это группы команд OpenGL, которые были сохранены для последующего выполнения.</span><span class="sxs-lookup"><span data-stu-id="57f9e-133">Display lists are groups of OpenGL commands that have been stored for subsequent execution.</span></span> <span data-ttu-id="57f9e-134">Списки отображений создаются с помощью **глневлист**.</span><span class="sxs-lookup"><span data-stu-id="57f9e-134">The display lists are created with **glNewList**.</span></span> <span data-ttu-id="57f9e-135">Все последующие команды помещаются в список просмотра в заданном порядке до вызова **глендлист** .</span><span class="sxs-lookup"><span data-stu-id="57f9e-135">All subsequent commands are placed in the display list, in the order issued, until **glEndList** is called.</span></span>

<span data-ttu-id="57f9e-136">Функция **глневлист** имеет два параметра.</span><span class="sxs-lookup"><span data-stu-id="57f9e-136">The **glNewList** function has two parameters.</span></span> <span data-ttu-id="57f9e-137">Первый параметр, *List*, представляет собой положительное целое число, которое становится уникальным именем для списка отображений.</span><span class="sxs-lookup"><span data-stu-id="57f9e-137">The first parameter, *list*, is a positive integer that becomes the unique name for the display list.</span></span> <span data-ttu-id="57f9e-138">Имена могут быть созданы и зарезервированы с помощью [**глженлистс**](glgenlists.md) и проверены на уникальность с помощью [**глислист**](glislist.md).</span><span class="sxs-lookup"><span data-stu-id="57f9e-138">Names can be created and reserved with [**glGenLists**](glgenlists.md) and tested for uniqueness with [**glIsList**](glislist.md).</span></span> <span data-ttu-id="57f9e-139">Второй параметр *mode*— это символьная константа, которая может принимать одно из двух приведенных выше значений.</span><span class="sxs-lookup"><span data-stu-id="57f9e-139">The second parameter, *mode*, is a symbolic constant that can assume one of the two preceding values.</span></span>

<span data-ttu-id="57f9e-140">Некоторые команды не компилируются в список просмотра, но выполняются немедленно, независимо от режима просмотра списка.</span><span class="sxs-lookup"><span data-stu-id="57f9e-140">Certain commands are not compiled into the display list, but are executed immediately, regardless of the display list mode.</span></span> <span data-ttu-id="57f9e-141">Эти команды являются [**глколорпоинтер**](glcolorpointer.md), [**глделетелистс**](gldeletelists.md), [**глдисаблеклиентстате**](gldisableclientstate.md), [**гледжефлагпоинтер**](gledgeflagpointer.md), [**гленаблеклиентстате**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList,**](glislist.md), [**glNormalPointer**](glpopclientattrib.md), [**glPopClientAttrib**](glpixelstore-functions.md), [**glPixelStore**](glpushclientattrib.md), [**glPushClientAttrib**](glreadpixels.md), [**glReadPixels**](glrendermode.md), [**glRenderMode**](glselectbuffer.md), [**glSelectBuffer**](gltexcoordpointer.md), [**glTexCoordPointer**](glvertexpointer.md)и все подпрограммы [**glVertexPointer**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) . [](glnormalpointer.md)</span><span class="sxs-lookup"><span data-stu-id="57f9e-141">These commands are [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md), and all of the [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) routines.</span></span>

<span data-ttu-id="57f9e-142">Аналогичным образом, [**glTexImage2D**](glteximage2d.md) и [**glTexImage1D**](glteximage1d.md) выполняются немедленно и не компилируются в список вывода, если их первый аргумент имеет \_ значение \_ 2D-текстура \_ двухмерной текстуры или плоская \_ текстура прокси-сервера GL \_ \_ , соответственно.</span><span class="sxs-lookup"><span data-stu-id="57f9e-142">Similarly, [**glTexImage2D**](glteximage2d.md) and [**glTexImage1D**](glteximage1d.md) are executed immediately and not compiled into the display list when their first argument is GL\_PROXY\_TEXTURE\_2D or GL\_PROXY\_TEXTURE\_1D, respectively.</span></span>

<span data-ttu-id="57f9e-143">При обнаружении функции **глендлист** определение списка отображается с помощью *сопоставления списка с уникальным именем (* указанным в команде **глневлист** ).</span><span class="sxs-lookup"><span data-stu-id="57f9e-143">When the **glEndList** function is encountered, the display list definition is completed by associating the list with the unique name *list* (specified in the **glNewList** command).</span></span> <span data-ttu-id="57f9e-144">Если *список просмотра с именем уже* существует, он заменяется только при вызове **глендлист** .</span><span class="sxs-lookup"><span data-stu-id="57f9e-144">If a display list with name *list* already exists, it is replaced only when **glEndList** is called.</span></span>

<span data-ttu-id="57f9e-145">Функции [**глкалллист**](glcalllist.md) и [**глкалллистс**](glcalllists.md) можно указать в списках вывода.</span><span class="sxs-lookup"><span data-stu-id="57f9e-145">The [**glCallList**](glcalllist.md) and [**glCallLists**](glcalllists.md) functions can be entered into display lists.</span></span> <span data-ttu-id="57f9e-146">Команды в списке отображаемых списков или списках, выполняемых **глкалллист** или **глкалллистс** , не включаются в создаваемый список просмотра, даже если в качестве режима создания списка используется значение GL \_ Compile \_ и \_ EXECUTE.</span><span class="sxs-lookup"><span data-stu-id="57f9e-146">The commands in the display list or lists executed by **glCallList** or **glCallLists** are not included in the display list being created, even if the list creation mode is GL\_COMPILE\_AND\_EXECUTE.</span></span>

<span data-ttu-id="57f9e-147">Следующая функция получает сведения, связанные с **глневлист**:</span><span class="sxs-lookup"><span data-stu-id="57f9e-147">The following function retrieves information related to **glNewList**:</span></span>

<span data-ttu-id="57f9e-148">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в \_ режиме матрицы GL \_</span><span class="sxs-lookup"><span data-stu-id="57f9e-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="57f9e-149">Требования</span><span class="sxs-lookup"><span data-stu-id="57f9e-149">Requirements</span></span>



| <span data-ttu-id="57f9e-150">Требование</span><span class="sxs-lookup"><span data-stu-id="57f9e-150">Requirement</span></span> | <span data-ttu-id="57f9e-151">Значение</span><span class="sxs-lookup"><span data-stu-id="57f9e-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57f9e-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57f9e-152">Minimum supported client</span></span><br/> | <span data-ttu-id="57f9e-153">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="57f9e-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="57f9e-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57f9e-154">Minimum supported server</span></span><br/> | <span data-ttu-id="57f9e-155">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="57f9e-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="57f9e-156">Заголовок</span><span class="sxs-lookup"><span data-stu-id="57f9e-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="57f9e-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="57f9e-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="57f9e-158">Библиотека</span><span class="sxs-lookup"><span data-stu-id="57f9e-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="57f9e-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57f9e-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="57f9e-160">DLL</span><span class="sxs-lookup"><span data-stu-id="57f9e-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57f9e-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57f9e-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57f9e-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57f9e-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57f9e-163">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="57f9e-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="57f9e-164">**глкалллист**</span><span class="sxs-lookup"><span data-stu-id="57f9e-164">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="57f9e-165">**глкалллистс**</span><span class="sxs-lookup"><span data-stu-id="57f9e-165">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="57f9e-166">**глделетелистс**</span><span class="sxs-lookup"><span data-stu-id="57f9e-166">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="57f9e-167">**гленд**</span><span class="sxs-lookup"><span data-stu-id="57f9e-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="57f9e-168">**глендлист**</span><span class="sxs-lookup"><span data-stu-id="57f9e-168">**glEndList**</span></span>](glendlist.md)
</dt> <dt>

[<span data-ttu-id="57f9e-169">**глженлистс**</span><span class="sxs-lookup"><span data-stu-id="57f9e-169">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="57f9e-170">**глислист**</span><span class="sxs-lookup"><span data-stu-id="57f9e-170">**glIsList**</span></span>](glislist.md)
</dt> </dl>

 

 





