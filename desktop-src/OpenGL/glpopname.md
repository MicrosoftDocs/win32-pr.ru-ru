---
title: Функция Глпопнаме (GL. h)
description: Функции Глпушнаме и Глпопнаме отправляют и выводят на экран стека имен. | Функция Глпопнаме (GL. h)
ms.assetid: ee741188-b275-4839-a89d-4d988c547d07
keywords:
- Функция Глпопнаме OpenGL
topic_type:
- apiref
api_name:
- glPopName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 830c4937b30cca64de3063b42ad16dd3adc87c89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684926"
---
# <a name="glpopname-function"></a><span data-ttu-id="dcd29-105">Функция Глпопнаме</span><span class="sxs-lookup"><span data-stu-id="dcd29-105">glPopName function</span></span>

<span data-ttu-id="dcd29-106">Функции [**глпушнаме**](glpushname.md) и **глпопнаме** отправляют и выводят на экран стека имен.</span><span class="sxs-lookup"><span data-stu-id="dcd29-106">The [**glPushName**](glpushname.md) and **glPopName** functions push and pop the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcd29-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dcd29-107">Syntax</span></span>


```C++
void WINAPI glPopName(void);
```



## <a name="parameters"></a><span data-ttu-id="dcd29-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dcd29-108">Parameters</span></span>

<span data-ttu-id="dcd29-109">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="dcd29-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dcd29-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dcd29-110">Return value</span></span>

<span data-ttu-id="dcd29-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="dcd29-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dcd29-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="dcd29-112">Error codes</span></span>

<span data-ttu-id="dcd29-113">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="dcd29-113">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="dcd29-114">Имя</span><span class="sxs-lookup"><span data-stu-id="dcd29-114">Name</span></span>                                                                                                  | <span data-ttu-id="dcd29-115">Значение</span><span class="sxs-lookup"><span data-stu-id="dcd29-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dcd29-116"><dt>**\_ \_ потеря значимости СТЕКа GL**</dt></span><span class="sxs-lookup"><span data-stu-id="dcd29-116"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="dcd29-117">Функция была вызвана, пока текущий стек матриц содержал только одну матрицу.</span><span class="sxs-lookup"><span data-stu-id="dcd29-117">The function was called while the current matrix stack contained only a single matrix.</span></span><br/>                                     |
| <dl> <span data-ttu-id="dcd29-118"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="dcd29-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="dcd29-119">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="dcd29-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="dcd29-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dcd29-120">Remarks</span></span>

<span data-ttu-id="dcd29-121">Функция [**глпушнаме**](glpushname.md) приводит к тому, что имя помещается в стек имен, который изначально пуст.</span><span class="sxs-lookup"><span data-stu-id="dcd29-121">The [**glPushName**](glpushname.md) function causes name to be pushed onto the name stack, which is initially empty.</span></span> <span data-ttu-id="dcd29-122">Функция **глпопнаме** выводит одно имя из верхней части стека.</span><span class="sxs-lookup"><span data-stu-id="dcd29-122">The **glPopName** function pops one name off the top of the stack.</span></span> <span data-ttu-id="dcd29-123">В режиме выбора используется стек имен, чтобы обеспечить уникальную идентификацию наборов команд отрисовки.</span><span class="sxs-lookup"><span data-stu-id="dcd29-123">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="dcd29-124">Он состоит из упорядоченного набора целых чисел без знака.</span><span class="sxs-lookup"><span data-stu-id="dcd29-124">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="dcd29-125">Стек имен всегда пуст, пока режим рендеринга не является GL \_ SELECT.</span><span class="sxs-lookup"><span data-stu-id="dcd29-125">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="dcd29-126">Вызовы [**глпушнаме**](glpushname.md) или **глпопнаме** , когда режим рендеринга не является GL \_ SELECT, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="dcd29-126">Calls to [**glPushName**](glpushname.md) or **glPopName** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="dcd29-127">Следующие функции извлекают сведения, относящиеся к [**глпушнаме**](glpushname.md) и **глпопнаме**:</span><span class="sxs-lookup"><span data-stu-id="dcd29-127">The following functions retrieve information related to [**glPushName**](glpushname.md) and **glPopName**:</span></span>

<span data-ttu-id="dcd29-128">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ \_ Длина стека имен GL \_</span><span class="sxs-lookup"><span data-stu-id="dcd29-128">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="dcd29-129">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ , \_ \_ глубина стека максимальных имен \_</span><span class="sxs-lookup"><span data-stu-id="dcd29-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="dcd29-130">Требования</span><span class="sxs-lookup"><span data-stu-id="dcd29-130">Requirements</span></span>



| <span data-ttu-id="dcd29-131">Требование</span><span class="sxs-lookup"><span data-stu-id="dcd29-131">Requirement</span></span> | <span data-ttu-id="dcd29-132">Значение</span><span class="sxs-lookup"><span data-stu-id="dcd29-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcd29-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dcd29-133">Minimum supported client</span></span><br/> | <span data-ttu-id="dcd29-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dcd29-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="dcd29-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dcd29-135">Minimum supported server</span></span><br/> | <span data-ttu-id="dcd29-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dcd29-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dcd29-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="dcd29-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcd29-138"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcd29-138"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="dcd29-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dcd29-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="dcd29-140"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcd29-140"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="dcd29-141">DLL</span><span class="sxs-lookup"><span data-stu-id="dcd29-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcd29-142"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcd29-142"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcd29-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dcd29-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcd29-144">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="dcd29-144">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="dcd29-145">**гленд**</span><span class="sxs-lookup"><span data-stu-id="dcd29-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="dcd29-146">**глинитнамес**</span><span class="sxs-lookup"><span data-stu-id="dcd29-146">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="dcd29-147">**гллоаднаме**</span><span class="sxs-lookup"><span data-stu-id="dcd29-147">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="dcd29-148">**глрендермоде**</span><span class="sxs-lookup"><span data-stu-id="dcd29-148">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="dcd29-149">**глселектбуффер**</span><span class="sxs-lookup"><span data-stu-id="dcd29-149">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





