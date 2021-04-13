---
title: Функция Глмултматриксд (GL. h)
description: Функция Глмултматриксд Умножает текущую матрицу на произвольную матрицу. | Функция Глмултматриксд (GL. h)
ms.assetid: 1f6cf4e4-e7bd-470c-b1f4-b9ccc1fb756e
keywords:
- Функция Глмултматриксд OpenGL
topic_type:
- apiref
api_name:
- glMultMatrixd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e24993fe5873be0af8713e3d127b86a7c593cd82
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353785"
---
# <a name="glmultmatrixd-function"></a><span data-ttu-id="1e03c-105">Функция Глмултматриксд</span><span class="sxs-lookup"><span data-stu-id="1e03c-105">glMultMatrixd function</span></span>

<span data-ttu-id="1e03c-106">Функции **глмултматриксд** и [**глмултматриксф**](glmultmatrixf.md) умножают текущую матрицу на произвольную матрицу.</span><span class="sxs-lookup"><span data-stu-id="1e03c-106">The **glMultMatrixd** and [**glMultMatrixf**](glmultmatrixf.md) functions multiply the current matrix by an arbitrary matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e03c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e03c-107">Syntax</span></span>


```C++
void WINAPI glMultMatrixd(
   const GLdouble *m
);
```



## <a name="parameters"></a><span data-ttu-id="1e03c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e03c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e03c-109">*m*</span><span class="sxs-lookup"><span data-stu-id="1e03c-109">*m*</span></span> 
</dt> <dd>

<span data-ttu-id="1e03c-110">Указатель на матрицу 4x4, хранящийся в основном порядке столбцов, как 16 последовательных значений.</span><span class="sxs-lookup"><span data-stu-id="1e03c-110">A pointer to a 4x4 matrix stored in column-major order as 16 consecutive values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e03c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e03c-111">Return value</span></span>

<span data-ttu-id="1e03c-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1e03c-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1e03c-113">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="1e03c-113">Error codes</span></span>

<span data-ttu-id="1e03c-114">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="1e03c-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1e03c-115">Имя</span><span class="sxs-lookup"><span data-stu-id="1e03c-115">Name</span></span>                                                                                                  | <span data-ttu-id="1e03c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1e03c-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1e03c-117"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="1e03c-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1e03c-118">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="1e03c-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1e03c-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e03c-119">Remarks</span></span>

<span data-ttu-id="1e03c-120">Функция **глмултматрикс** Умножает текущую матрицу на единицу, указанную в *m*.</span><span class="sxs-lookup"><span data-stu-id="1e03c-120">The **glMultMatrix** function multiplies the current matrix by the one specified in *m*.</span></span> <span data-ttu-id="1e03c-121">То есть, если M — это текущая матрица, а T — матрица, передаваемая в **глмултматрикс**, то m заменяется на m T.</span><span class="sxs-lookup"><span data-stu-id="1e03c-121">That is, if M is the current matrix and T is the matrix passed to **glMultMatrix**, then M is replaced with M   T.</span></span>

<span data-ttu-id="1e03c-122">Текущая матрица — матрица проекции, моделвиев матрица или Текстурная матрица, определяемая текущим режимом матрицы (см. [**глматриксмоде**](glmatrixmode.md)).</span><span class="sxs-lookup"><span data-stu-id="1e03c-122">The current matrix is the projection matrix, modelview matrix, or texture matrix, determined by the current matrix mode (see [**glMatrixMode**](glmatrixmode.md)).</span></span>

<span data-ttu-id="1e03c-123">Параметр *m* указывает на матрицу 4x4 значений с плавающей запятой одиночной точности или двойной точности, хранящихся в основном порядке столбцов.</span><span class="sxs-lookup"><span data-stu-id="1e03c-123">The *m* parameter points to a 4x4 matrix of single-precision or double-precision floating-point values stored in column-major order.</span></span> <span data-ttu-id="1e03c-124">То есть Матрица сохраняется, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="1e03c-124">That is, the matrix is stored as shown in the following image.</span></span>

![! [Диаграмма, показывающая матрицу 4x4, на которую указывает параметр m.]](images/multi01.png)

<span data-ttu-id="1e03c-126">Следующие функции извлекают сведения, относящиеся к **глмултматрикс**:</span><span class="sxs-lookup"><span data-stu-id="1e03c-126">The following functions retrieve information related to **glMultMatrix**:</span></span>

<span data-ttu-id="1e03c-127">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в \_ режиме матрицы GL \_</span><span class="sxs-lookup"><span data-stu-id="1e03c-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="1e03c-128">**глжет** с аргументом \_ МОДЕЛВИЕВ \_ Матрица GL</span><span class="sxs-lookup"><span data-stu-id="1e03c-128">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="1e03c-129">**глжет** с аргументом \_ матрица проекции главной книги \_</span><span class="sxs-lookup"><span data-stu-id="1e03c-129">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="1e03c-130">**глжет** с аргументом \_ \_ Матрица текстуры GL</span><span class="sxs-lookup"><span data-stu-id="1e03c-130">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="1e03c-131">Требования</span><span class="sxs-lookup"><span data-stu-id="1e03c-131">Requirements</span></span>



| <span data-ttu-id="1e03c-132">Требование</span><span class="sxs-lookup"><span data-stu-id="1e03c-132">Requirement</span></span> | <span data-ttu-id="1e03c-133">Значение</span><span class="sxs-lookup"><span data-stu-id="1e03c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e03c-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e03c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1e03c-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1e03c-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1e03c-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e03c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1e03c-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1e03c-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1e03c-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1e03c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e03c-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e03c-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1e03c-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1e03c-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="1e03c-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e03c-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1e03c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1e03c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e03c-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e03c-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e03c-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e03c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e03c-145">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="1e03c-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1e03c-146">**гленд**</span><span class="sxs-lookup"><span data-stu-id="1e03c-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1e03c-147">**гллоадидентити**</span><span class="sxs-lookup"><span data-stu-id="1e03c-147">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="1e03c-148">**гллоадматрикс**</span><span class="sxs-lookup"><span data-stu-id="1e03c-148">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="1e03c-149">**глматриксмоде**</span><span class="sxs-lookup"><span data-stu-id="1e03c-149">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="1e03c-150">**глпушматрикс**</span><span class="sxs-lookup"><span data-stu-id="1e03c-150">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





