---
title: Функция Глендлист (GL. h)
description: Функции Глневлист и Глендлист создают или заменяют список отображений. | Функция Глендлист (GL. h)
ms.assetid: dd749932-7b3c-47e5-8d91-90d272a7dc41
keywords:
- Функция Глендлист OpenGL
topic_type:
- apiref
api_name:
- glEndList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f8db8c2abea44d678268f804159b60fe695f96
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684920"
---
# <a name="glendlist-function"></a><span data-ttu-id="47598-105">Функция Глендлист</span><span class="sxs-lookup"><span data-stu-id="47598-105">glEndList function</span></span>

<span data-ttu-id="47598-106">Функции [**глневлист**](glnewlist.md) и **глендлист** создают или заменяют список отображений.</span><span class="sxs-lookup"><span data-stu-id="47598-106">The [**glNewList**](glnewlist.md) and **glEndList** functions create or replace a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="47598-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47598-107">Syntax</span></span>


```C++
void WINAPI glEndList(void);
```



## <a name="parameters"></a><span data-ttu-id="47598-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="47598-108">Parameters</span></span>

<span data-ttu-id="47598-109">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="47598-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="47598-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47598-110">Return value</span></span>

<span data-ttu-id="47598-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="47598-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="47598-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="47598-112">Error codes</span></span>

<span data-ttu-id="47598-113">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="47598-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="47598-114">Имя</span><span class="sxs-lookup"><span data-stu-id="47598-114">Name</span></span>                                                                                                  | <span data-ttu-id="47598-115">Значение</span><span class="sxs-lookup"><span data-stu-id="47598-115">Meaning</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="47598-116"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="47598-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="47598-117">**глендлист** был вызван без предшествующего **глневлист** или если **глневлист** был вызван во время определения списка отображений.</span><span class="sxs-lookup"><span data-stu-id="47598-117">**glEndList** was called without a preceding **glNewList**, or if **glnewlist** was called while a display list was being defined.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="47598-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47598-118">Remarks</span></span>

<span data-ttu-id="47598-119">Списки отображений — это группы команд OpenGL, которые были сохранены для последующего выполнения.</span><span class="sxs-lookup"><span data-stu-id="47598-119">Display lists are groups of OpenGL commands that have been stored for subsequent execution.</span></span> <span data-ttu-id="47598-120">Списки отображений создаются с помощью [**глневлист**](glnewlist.md).</span><span class="sxs-lookup"><span data-stu-id="47598-120">The display lists are created with [**glNewList**](glnewlist.md).</span></span> <span data-ttu-id="47598-121">Все последующие команды помещаются в список просмотра в заданном порядке до вызова **глендлист** .</span><span class="sxs-lookup"><span data-stu-id="47598-121">All subsequent commands are placed in the display list, in the order issued, until **glEndList** is called.</span></span>

<span data-ttu-id="47598-122">Функция [**глневлист**](glnewlist.md) имеет два параметра.</span><span class="sxs-lookup"><span data-stu-id="47598-122">The [**glNewList**](glnewlist.md) function has two parameters.</span></span> <span data-ttu-id="47598-123">Первый параметр, *List*, представляет собой положительное целое число, которое становится уникальным именем для списка отображений.</span><span class="sxs-lookup"><span data-stu-id="47598-123">The first parameter, *list*, is a positive integer that becomes the unique name for the display list.</span></span> <span data-ttu-id="47598-124">Имена могут быть созданы и зарезервированы с помощью [**глженлистс**](glgenlists.md) и проверены на уникальность с помощью [**глислист**](glislist.md).</span><span class="sxs-lookup"><span data-stu-id="47598-124">Names can be created and reserved with [**glGenLists**](glgenlists.md) and tested for uniqueness with [**glIsList**](glislist.md).</span></span> <span data-ttu-id="47598-125">Второй параметр *mode*— это символьная константа, которая может принимать одно из двух приведенных выше значений.</span><span class="sxs-lookup"><span data-stu-id="47598-125">The second parameter, *mode*, is a symbolic constant that can assume one of the two preceding values.</span></span>

<span data-ttu-id="47598-126">Некоторые команды не компилируются в список просмотра, но выполняются немедленно, независимо от режима просмотра списка.</span><span class="sxs-lookup"><span data-stu-id="47598-126">Certain commands are not compiled into the display list, but are executed immediately, regardless of the display list mode.</span></span> <span data-ttu-id="47598-127">Эти команды являются [**глколорпоинтер**](glcolorpointer.md), [**глделетелистс**](gldeletelists.md), [**глдисаблеклиентстате**](gldisableclientstate.md), [**гледжефлагпоинтер**](gledgeflagpointer.md), [**гленаблеклиентстате**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList,**](glislist.md), [**glNormalPointer**](glpopclientattrib.md), [**glPopClientAttrib**](glpixelstore-functions.md), [**glPixelStore**](glpushclientattrib.md), [**glPushClientAttrib**](glreadpixels.md), [**glReadPixels**](glrendermode.md), [**glRenderMode**](glselectbuffer.md), [**glSelectBuffer**](gltexcoordpointer.md), [**glTexCoordPointer**](glvertexpointer.md)и все подпрограммы [**glVertexPointer**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) . [](glnormalpointer.md)</span><span class="sxs-lookup"><span data-stu-id="47598-127">These commands are [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md), and all of the [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) routines.</span></span>

<span data-ttu-id="47598-128">Аналогичным образом, [**glTexImage2D**](glteximage2d.md) и [**glTexImage1D**](glteximage1d.md) выполняются немедленно и не компилируются в список вывода, если их первый аргумент имеет \_ значение \_ 2D-текстура \_ двухмерной текстуры или плоская \_ текстура прокси-сервера GL \_ \_ , соответственно.</span><span class="sxs-lookup"><span data-stu-id="47598-128">Similarly, [**glTexImage2D**](glteximage2d.md) and [**glTexImage1D**](glteximage1d.md) are executed immediately and not compiled into the display list when their first argument is GL\_PROXY\_TEXTURE\_2D or GL\_PROXY\_TEXTURE\_1D, respectively.</span></span>

<span data-ttu-id="47598-129">При обнаружении функции **глендлист** определение списка отображается с помощью *сопоставления списка с уникальным именем (* указанным в команде [**глневлист**](glnewlist.md) ).</span><span class="sxs-lookup"><span data-stu-id="47598-129">When the **glEndList** function is encountered, the display list definition is completed by associating the list with the unique name *list* (specified in the [**glNewList**](glnewlist.md) command).</span></span> <span data-ttu-id="47598-130">Если *список просмотра с именем уже* существует, он заменяется только при вызове **глендлист** .</span><span class="sxs-lookup"><span data-stu-id="47598-130">If a display list with name *list* already exists, it is replaced only when **glEndList** is called.</span></span>

<span data-ttu-id="47598-131">Функции [**глкалллист**](glcalllist.md) и [**глкалллистс**](glcalllists.md) можно указать в списках вывода.</span><span class="sxs-lookup"><span data-stu-id="47598-131">The [**glCallList**](glcalllist.md) and [**glCallLists**](glcalllists.md) functions can be entered into display lists.</span></span> <span data-ttu-id="47598-132">Команды в списке отображаемых списков или списках, выполняемых **глкалллист** или **глкалллистс** , не включаются в создаваемый список просмотра, даже если в качестве режима создания списка используется значение GL \_ Compile \_ и \_ EXECUTE.</span><span class="sxs-lookup"><span data-stu-id="47598-132">The commands in the display list or lists executed by **glCallList** or **glCallLists** are not included in the display list being created, even if the list creation mode is GL\_COMPILE\_AND\_EXECUTE.</span></span>

<span data-ttu-id="47598-133">Следующая функция получает сведения, связанные с [**глневлист**](glnewlist.md):</span><span class="sxs-lookup"><span data-stu-id="47598-133">The following function retrieves information related to [**glNewList**](glnewlist.md):</span></span>

<span data-ttu-id="47598-134">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в \_ режиме матрицы GL \_</span><span class="sxs-lookup"><span data-stu-id="47598-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="47598-135">Требования</span><span class="sxs-lookup"><span data-stu-id="47598-135">Requirements</span></span>



| <span data-ttu-id="47598-136">Требование</span><span class="sxs-lookup"><span data-stu-id="47598-136">Requirement</span></span> | <span data-ttu-id="47598-137">Значение</span><span class="sxs-lookup"><span data-stu-id="47598-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47598-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47598-138">Minimum supported client</span></span><br/> | <span data-ttu-id="47598-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="47598-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="47598-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47598-140">Minimum supported server</span></span><br/> | <span data-ttu-id="47598-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="47598-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="47598-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="47598-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="47598-143"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="47598-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="47598-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="47598-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="47598-145"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47598-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="47598-146">DLL</span><span class="sxs-lookup"><span data-stu-id="47598-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47598-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47598-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47598-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47598-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47598-149">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="47598-149">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="47598-150">**глкалллист**</span><span class="sxs-lookup"><span data-stu-id="47598-150">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="47598-151">**глкалллистс**</span><span class="sxs-lookup"><span data-stu-id="47598-151">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="47598-152">**глделетелистс**</span><span class="sxs-lookup"><span data-stu-id="47598-152">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="47598-153">**гленд**</span><span class="sxs-lookup"><span data-stu-id="47598-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="47598-154">**глженлистс**</span><span class="sxs-lookup"><span data-stu-id="47598-154">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="47598-155">**глислист**</span><span class="sxs-lookup"><span data-stu-id="47598-155">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="47598-156">**глневлист**</span><span class="sxs-lookup"><span data-stu-id="47598-156">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





