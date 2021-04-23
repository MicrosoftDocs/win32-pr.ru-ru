---
title: Функция Глпопматрикс (GL. h)
description: Функции Глпушматрикс и Глпопматрикс принудительно отправляют и отправляют текущий стек матриц. | Функция Глпопматрикс (GL. h)
ms.assetid: 7b4fc26e-36c8-4252-aba7-2e8ec6b34f91
keywords:
- Функция Глпопматрикс OpenGL
topic_type:
- apiref
api_name:
- glPopMatrix
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41424a8af3ca6599edc7a66f9e498632640022c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664881"
---
# <a name="glpopmatrix-function"></a><span data-ttu-id="7adf4-105">Функция Глпопматрикс</span><span class="sxs-lookup"><span data-stu-id="7adf4-105">glPopMatrix function</span></span>

<span data-ttu-id="7adf4-106">Функции [**глпушматрикс**](glpushmatrix.md) и **глпопматрикс** принудительно отправляют и отправляют текущий стек матриц.</span><span class="sxs-lookup"><span data-stu-id="7adf4-106">The [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** functions push and pop the current matrix stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="7adf4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7adf4-107">Syntax</span></span>


```C++
void WINAPI glPopMatrix(void);
```



## <a name="parameters"></a><span data-ttu-id="7adf4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7adf4-108">Parameters</span></span>

<span data-ttu-id="7adf4-109">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="7adf4-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7adf4-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7adf4-110">Return value</span></span>

<span data-ttu-id="7adf4-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7adf4-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7adf4-112">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="7adf4-112">Error codes</span></span>

<span data-ttu-id="7adf4-113">Отправка полного стека матрицы или открытие стека матриц, содержащего только одну матрицу, является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="7adf4-113">It is an error to push a full matrix stack, or to pop a matrix stack that contains only a single matrix.</span></span> <span data-ttu-id="7adf4-114">В любом случае устанавливается флаг ошибки, а в состояние OpenGL другие изменения не вносятся.</span><span class="sxs-lookup"><span data-stu-id="7adf4-114">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="7adf4-115">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="7adf4-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7adf4-116">Имя</span><span class="sxs-lookup"><span data-stu-id="7adf4-116">Name</span></span>                                                                                                  | <span data-ttu-id="7adf4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7adf4-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7adf4-118"><dt>**\_ \_ потеря значимости СТЕКа GL**</dt></span><span class="sxs-lookup"><span data-stu-id="7adf4-118"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="7adf4-119">Функция была вызвана, пока текущий стек матриц содержал только одну матрицу.</span><span class="sxs-lookup"><span data-stu-id="7adf4-119">The function was called while the current matrix stack contained only a single matrix.</span></span><br/>                                     |
| <dl> <span data-ttu-id="7adf4-120"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="7adf4-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7adf4-121">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="7adf4-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7adf4-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7adf4-122">Remarks</span></span>

<span data-ttu-id="7adf4-123">Существует стек матриц для каждого режима матрицы.</span><span class="sxs-lookup"><span data-stu-id="7adf4-123">There is a stack of matrices for each of the matrix modes.</span></span> <span data-ttu-id="7adf4-124">В \_ моделвиев режиме GL глубина стека составляет не менее 32.</span><span class="sxs-lookup"><span data-stu-id="7adf4-124">In GL\_MODELVIEW mode, the stack depth is at least 32.</span></span> <span data-ttu-id="7adf4-125">В двух других режимах — \_ проекция и \_ текстура GL, глубина — не менее 2.</span><span class="sxs-lookup"><span data-stu-id="7adf4-125">In the other two modes, GL\_PROJECTION and GL\_TEXTURE, the depth is at least 2.</span></span> <span data-ttu-id="7adf4-126">Текущая матрица в любом режиме — это матрица, расположенная в верхней части стека для этого режима.</span><span class="sxs-lookup"><span data-stu-id="7adf4-126">The current matrix in any mode is the matrix on the top of the stack for that mode.</span></span>

<span data-ttu-id="7adf4-127">Функция [**глпушматрикс**](glpushmatrix.md) помещает текущий стек матриц вниз на единицу, что дублирует текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="7adf4-127">The [**glPushMatrix**](glpushmatrix.md) function pushes the current matrix stack down by one, duplicating the current matrix.</span></span> <span data-ttu-id="7adf4-128">То есть после вызова **глпушматрикс** матрица, расположенная вверху стека, идентична расположенной ниже.</span><span class="sxs-lookup"><span data-stu-id="7adf4-128">That is, after a **glPushMatrix** call, the matrix on the top of the stack is identical to the one below it.</span></span> <span data-ttu-id="7adf4-129">Функция **глпопматрикс** выводит текущий стек матриц, заменяя текущую матрицу на одну под ней в стеке.</span><span class="sxs-lookup"><span data-stu-id="7adf4-129">The **glPopMatrix** function pops the current matrix stack, replacing the current matrix with the one below it on the stack.</span></span> <span data-ttu-id="7adf4-130">Изначально каждый из стеков содержит одну матрицу, матрицу идентификации.</span><span class="sxs-lookup"><span data-stu-id="7adf4-130">Initially, each of the stacks contains one matrix, an identity matrix.</span></span>

<span data-ttu-id="7adf4-131">Следующие функции извлекают сведения, относящиеся к [**глпушматрикс**](glpushmatrix.md) и **глпопматрикс**:</span><span class="sxs-lookup"><span data-stu-id="7adf4-131">The following functions retrieve information related to [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix**:</span></span>

<span data-ttu-id="7adf4-132">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в \_ режиме матрицы GL \_</span><span class="sxs-lookup"><span data-stu-id="7adf4-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="7adf4-133">**глжет** с аргументом \_ МОДЕЛВИЕВ \_ Матрица GL</span><span class="sxs-lookup"><span data-stu-id="7adf4-133">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="7adf4-134">**глжет** с аргументом \_ матрица проекции главной книги \_</span><span class="sxs-lookup"><span data-stu-id="7adf4-134">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="7adf4-135">**глжет** с аргументом \_ \_ Матрица текстуры GL</span><span class="sxs-lookup"><span data-stu-id="7adf4-135">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

<span data-ttu-id="7adf4-136">**глжет** с аргументом GL \_ моделвиев \_ Stack \_</span><span class="sxs-lookup"><span data-stu-id="7adf4-136">**glGet** with argument GL\_MODELVIEW\_STACK\_DEPTH</span></span>

<span data-ttu-id="7adf4-137">**глжет** с аргументом \_ " \_ глубина стека главной книги GL" \_</span><span class="sxs-lookup"><span data-stu-id="7adf4-137">**glGet** with argument GL\_PROJECTION\_STACK\_DEPTH</span></span>

<span data-ttu-id="7adf4-138">**глжет** с аргументом \_ \_ глубина текстуры стека GL \_</span><span class="sxs-lookup"><span data-stu-id="7adf4-138">**glGet** with argument GL\_TEXTURE\_STACK\_DEPTH</span></span>

<span data-ttu-id="7adf4-139">**глжет** с аргументом \_ GL \_ Максимальная \_ глубина моделвиев стека \_</span><span class="sxs-lookup"><span data-stu-id="7adf4-139">**glGet** with argument GL\_MAX\_MODELVIEW\_STACK\_DEPTH</span></span>

<span data-ttu-id="7adf4-140">**глжет** с аргументом \_ Максимальная \_ \_ глубина стека проекции \_</span><span class="sxs-lookup"><span data-stu-id="7adf4-140">**glGet** with argument GL\_MAX\_PROJECTION\_STACK\_DEPTH</span></span>

<span data-ttu-id="7adf4-141">**глжет** с аргументом \_ " \_ Максимальная \_ глубина текстуры стека \_ "</span><span class="sxs-lookup"><span data-stu-id="7adf4-141">**glGet** with argument GL\_MAX\_TEXTURE\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="7adf4-142">Требования</span><span class="sxs-lookup"><span data-stu-id="7adf4-142">Requirements</span></span>



| <span data-ttu-id="7adf4-143">Требование</span><span class="sxs-lookup"><span data-stu-id="7adf4-143">Requirement</span></span> | <span data-ttu-id="7adf4-144">Значение</span><span class="sxs-lookup"><span data-stu-id="7adf4-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7adf4-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7adf4-145">Minimum supported client</span></span><br/> | <span data-ttu-id="7adf4-146">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7adf4-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7adf4-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7adf4-147">Minimum supported server</span></span><br/> | <span data-ttu-id="7adf4-148">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7adf4-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7adf4-149">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7adf4-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="7adf4-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7adf4-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7adf4-151">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7adf4-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="7adf4-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7adf4-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7adf4-153">DLL</span><span class="sxs-lookup"><span data-stu-id="7adf4-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7adf4-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7adf4-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7adf4-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7adf4-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7adf4-156">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="7adf4-156">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7adf4-157">**гленд**</span><span class="sxs-lookup"><span data-stu-id="7adf4-157">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7adf4-158">**глфрустум**</span><span class="sxs-lookup"><span data-stu-id="7adf4-158">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="7adf4-159">**гллоадидентити**</span><span class="sxs-lookup"><span data-stu-id="7adf4-159">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="7adf4-160">**гллоадматрикс**</span><span class="sxs-lookup"><span data-stu-id="7adf4-160">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="7adf4-161">**глматриксмоде**</span><span class="sxs-lookup"><span data-stu-id="7adf4-161">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="7adf4-162">**глмултматрикс**</span><span class="sxs-lookup"><span data-stu-id="7adf4-162">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="7adf4-163">**глорсо**</span><span class="sxs-lookup"><span data-stu-id="7adf4-163">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="7adf4-164">**глпушматрикс**</span><span class="sxs-lookup"><span data-stu-id="7adf4-164">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="7adf4-165">**глротате**</span><span class="sxs-lookup"><span data-stu-id="7adf4-165">**glRotate**</span></span>](glrotate.md)
</dt> <dt>

[<span data-ttu-id="7adf4-166">**глскале**</span><span class="sxs-lookup"><span data-stu-id="7adf4-166">**glScale**</span></span>](glscale.md)
</dt> <dt>

[<span data-ttu-id="7adf4-167">**глтранслате**</span><span class="sxs-lookup"><span data-stu-id="7adf4-167">**glTranslate**</span></span>](gltranslate.md)
</dt> <dt>

[<span data-ttu-id="7adf4-168">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="7adf4-168">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





