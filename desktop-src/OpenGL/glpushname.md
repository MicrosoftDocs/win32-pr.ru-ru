---
title: Функция Глпушнаме (GL. h)
description: Функции Глпушнаме и Глпопнаме отправляют и выводят на экран стека имен. | Функция Глпушнаме (GL. h)
ms.assetid: e4319018-42c0-4567-b67f-31dbdbee9b13
keywords:
- Функция Глпушнаме OpenGL
topic_type:
- apiref
api_name:
- glPushName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff783a108f5cb1ac34141c6c57f47b16e23531a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684893"
---
# <a name="glpushname-function"></a><span data-ttu-id="36d0f-105">Функция Глпушнаме</span><span class="sxs-lookup"><span data-stu-id="36d0f-105">glPushName function</span></span>

<span data-ttu-id="36d0f-106">Функции **глпушнаме** и [**глпопнаме**](glpopname.md) отправляют и выводят на экран стека имен.</span><span class="sxs-lookup"><span data-stu-id="36d0f-106">The **glPushName** and [**glPopName**](glpopname.md) functions push and pop the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="36d0f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36d0f-107">Syntax</span></span>


```C++
void WINAPI glPushName(
   GLuint name
);
```



## <a name="parameters"></a><span data-ttu-id="36d0f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="36d0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36d0f-109">*name*</span><span class="sxs-lookup"><span data-stu-id="36d0f-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="36d0f-110">Имя, которое будет отправлено в стек имен.</span><span class="sxs-lookup"><span data-stu-id="36d0f-110">A name that will be pushed onto the name stack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36d0f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36d0f-111">Return value</span></span>

<span data-ttu-id="36d0f-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="36d0f-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="36d0f-113">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="36d0f-113">Error codes</span></span>

<span data-ttu-id="36d0f-114">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="36d0f-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="36d0f-115">Имя</span><span class="sxs-lookup"><span data-stu-id="36d0f-115">Name</span></span>                                                                                                  | <span data-ttu-id="36d0f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="36d0f-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="36d0f-117"><dt>**\_переполнение стека GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="36d0f-117"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="36d0f-118">Функция была вызвана, пока текущий стек матриц заполнен.</span><span class="sxs-lookup"><span data-stu-id="36d0f-118">The function was called while the current matrix stack was full.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="36d0f-119"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="36d0f-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="36d0f-120">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="36d0f-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="36d0f-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36d0f-121">Remarks</span></span>

<span data-ttu-id="36d0f-122">Функция **глпушнаме** приводит к тому, что имя помещается в стек имен, который изначально пуст.</span><span class="sxs-lookup"><span data-stu-id="36d0f-122">The **glPushName** function causes name to be pushed onto the name stack, which is initially empty.</span></span> <span data-ttu-id="36d0f-123">Функция [**глпопнаме**](glpopname.md) выводит одно имя из верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="36d0f-123">The [**glPopName**](glpopname.md) function pops one name off the top of the stack.</span></span> <span data-ttu-id="36d0f-124">В режиме выбора используется стек имен, чтобы обеспечить уникальную идентификацию наборов команд отрисовки.</span><span class="sxs-lookup"><span data-stu-id="36d0f-124">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="36d0f-125">Он состоит из упорядоченного набора целых чисел без знака.</span><span class="sxs-lookup"><span data-stu-id="36d0f-125">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="36d0f-126">Стек имен всегда пуст, пока режим рендеринга не является GL \_ SELECT.</span><span class="sxs-lookup"><span data-stu-id="36d0f-126">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="36d0f-127">Вызовы **глпушнаме** или [**глпопнаме**](glpopname.md) , когда режим рендеринга не является GL \_ SELECT, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="36d0f-127">Calls to **glPushName** or [**glPopName**](glpopname.md) while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="36d0f-128">Следующие функции извлекают сведения, относящиеся к **глпушнаме** и [**глпопнаме**](glpopname.md):</span><span class="sxs-lookup"><span data-stu-id="36d0f-128">The following functions retrieve information related to **glPushName** and [**glPopName**](glpopname.md):</span></span>

<span data-ttu-id="36d0f-129">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ \_ Длина стека имен GL \_</span><span class="sxs-lookup"><span data-stu-id="36d0f-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="36d0f-130">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ , \_ \_ глубина стека максимальных имен \_</span><span class="sxs-lookup"><span data-stu-id="36d0f-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="36d0f-131">Требования</span><span class="sxs-lookup"><span data-stu-id="36d0f-131">Requirements</span></span>



| <span data-ttu-id="36d0f-132">Требование</span><span class="sxs-lookup"><span data-stu-id="36d0f-132">Requirement</span></span> | <span data-ttu-id="36d0f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="36d0f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36d0f-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36d0f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="36d0f-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="36d0f-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="36d0f-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36d0f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="36d0f-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="36d0f-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="36d0f-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="36d0f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="36d0f-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="36d0f-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="36d0f-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="36d0f-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="36d0f-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36d0f-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="36d0f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="36d0f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36d0f-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36d0f-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36d0f-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36d0f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36d0f-145">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="36d0f-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="36d0f-146">**гленд**</span><span class="sxs-lookup"><span data-stu-id="36d0f-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="36d0f-147">**глинитнамес**</span><span class="sxs-lookup"><span data-stu-id="36d0f-147">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="36d0f-148">**гллоаднаме**</span><span class="sxs-lookup"><span data-stu-id="36d0f-148">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="36d0f-149">**глрендермоде**</span><span class="sxs-lookup"><span data-stu-id="36d0f-149">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="36d0f-150">**глселектбуффер**</span><span class="sxs-lookup"><span data-stu-id="36d0f-150">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





