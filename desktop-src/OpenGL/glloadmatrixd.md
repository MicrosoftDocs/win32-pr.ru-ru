---
title: Функция Гллоадматриксд (GL. h)
description: Функция Гллоадматриксд заменяет текущую матрицу произвольной матрицей. | Функция Гллоадматриксд (GL. h)
ms.assetid: 66c499f7-3f55-4de2-b67b-5b775b5854e0
keywords:
- Функция Гллоадматриксд OpenGL
topic_type:
- apiref
api_name:
- glLoadMatrixd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4715da159dff60024adb3c7331cbf03c7c3759ce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684835"
---
# <a name="glloadmatrixd-function"></a><span data-ttu-id="50988-105">Функция Гллоадматриксд</span><span class="sxs-lookup"><span data-stu-id="50988-105">glLoadMatrixd function</span></span>

<span data-ttu-id="50988-106">Функции **гллоадматриксд** и [**гллоадматриксф**](glloadmatrixf.md) заменяют текущую матрицу произвольной матрицей.</span><span class="sxs-lookup"><span data-stu-id="50988-106">The **glLoadMatrixd** and [**glLoadMatrixf**](glloadmatrixf.md) functions replace the current matrix with an arbitrary matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="50988-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50988-107">Syntax</span></span>


```C++
void WINAPI glLoadMatrixd(
   const GLdouble *m
);
```



## <a name="parameters"></a><span data-ttu-id="50988-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="50988-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50988-109">*m*</span><span class="sxs-lookup"><span data-stu-id="50988-109">*m*</span></span> 
</dt> <dd>

<span data-ttu-id="50988-110">Указатель на матрицу 4x4, хранящийся в основном порядке столбцов, как 16 последовательных значений.</span><span class="sxs-lookup"><span data-stu-id="50988-110">A pointer to a 4x4 matrix stored in column-major order as 16 consecutive values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50988-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50988-111">Return value</span></span>

<span data-ttu-id="50988-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="50988-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="50988-113">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="50988-113">Error codes</span></span>

<span data-ttu-id="50988-114">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="50988-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="50988-115">Имя</span><span class="sxs-lookup"><span data-stu-id="50988-115">Name</span></span>                                                                                                  | <span data-ttu-id="50988-116">Значение</span><span class="sxs-lookup"><span data-stu-id="50988-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="50988-117"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="50988-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="50988-118">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="50988-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="50988-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50988-119">Remarks</span></span>

<span data-ttu-id="50988-120">Функция **гллоадматрикс** заменяет текущую матрицу на ту, которая указана в *m*.</span><span class="sxs-lookup"><span data-stu-id="50988-120">The **glLoadMatrix** function replaces the current matrix with the one specified in *m*.</span></span> <span data-ttu-id="50988-121">Текущая матрица — матрица проекции, моделвиев матрица или Текстурная матрица, определяемая текущим режимом матрицы (см. [**глматриксмоде**](glmatrixmode.md)).</span><span class="sxs-lookup"><span data-stu-id="50988-121">The current matrix is the projection matrix, modelview matrix, or texture matrix, determined by the current matrix mode (see [**glMatrixMode**](glmatrixmode.md)).</span></span>

<span data-ttu-id="50988-122">Параметр *m* указывает на матрицу 4x4 значений с плавающей запятой одиночной точности или двойной точности, хранящихся в основном порядке столбцов.</span><span class="sxs-lookup"><span data-stu-id="50988-122">The *m* parameter points to a 4x4 matrix of single-precision or double-precision floating-point values stored in column-major order.</span></span> <span data-ttu-id="50988-123">То есть Матрица сохраняется, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="50988-123">That is, the matrix is stored as shown in the following image.</span></span>

![Схема, на которой показана матрица 4x4, на которую указывает параметр m.](images/load02.png)

<span data-ttu-id="50988-125">Следующие функции извлекают сведения, относящиеся к **гллоадматрикс**:</span><span class="sxs-lookup"><span data-stu-id="50988-125">The following functions retrieve information related to **glLoadMatrix**:</span></span>

<span data-ttu-id="50988-126">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в \_ режиме матрицы GL \_</span><span class="sxs-lookup"><span data-stu-id="50988-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="50988-127">**глжет** с аргументом \_ МОДЕЛВИЕВ \_ Матрица GL</span><span class="sxs-lookup"><span data-stu-id="50988-127">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="50988-128">**глжет** с аргументом \_ матрица проекции главной книги \_</span><span class="sxs-lookup"><span data-stu-id="50988-128">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="50988-129">**глжет** с аргументом \_ \_ Матрица текстуры GL</span><span class="sxs-lookup"><span data-stu-id="50988-129">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="50988-130">Требования</span><span class="sxs-lookup"><span data-stu-id="50988-130">Requirements</span></span>



| <span data-ttu-id="50988-131">Требование</span><span class="sxs-lookup"><span data-stu-id="50988-131">Requirement</span></span> | <span data-ttu-id="50988-132">Значение</span><span class="sxs-lookup"><span data-stu-id="50988-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50988-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50988-133">Minimum supported client</span></span><br/> | <span data-ttu-id="50988-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50988-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="50988-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50988-135">Minimum supported server</span></span><br/> | <span data-ttu-id="50988-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50988-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="50988-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="50988-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="50988-138"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="50988-138"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="50988-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="50988-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="50988-140"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50988-140"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="50988-141">DLL</span><span class="sxs-lookup"><span data-stu-id="50988-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50988-142"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50988-142"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50988-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50988-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50988-144">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="50988-144">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="50988-145">**гленд**</span><span class="sxs-lookup"><span data-stu-id="50988-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="50988-146">**гллоадидентити**</span><span class="sxs-lookup"><span data-stu-id="50988-146">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="50988-147">**глматриксмоде**</span><span class="sxs-lookup"><span data-stu-id="50988-147">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="50988-148">**глмултматрикс**</span><span class="sxs-lookup"><span data-stu-id="50988-148">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="50988-149">**глпушматрикс**</span><span class="sxs-lookup"><span data-stu-id="50988-149">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





