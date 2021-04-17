---
title: Функция Глскалед (GL. h)
description: Функции Глскалед и Глскалеф умножают текущую матрицу на общую матрицу масштабирования. | Функция Глскалед (GL. h)
ms.assetid: 3846289f-5c7b-4bb6-95a8-90a58dd8b9d9
keywords:
- Функция Глскалед OpenGL
topic_type:
- apiref
api_name:
- glScaled
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2655924f5716e142832882441066d4772d0e63
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104570549"
---
# <a name="glscaled-function"></a><span data-ttu-id="6d2bf-105">Функция Глскалед</span><span class="sxs-lookup"><span data-stu-id="6d2bf-105">glScaled function</span></span>

<span data-ttu-id="6d2bf-106">Функции **глскалед** и [**глскалеф**](glscalef.md) умножают текущую матрицу на общую матрицу масштабирования.</span><span class="sxs-lookup"><span data-stu-id="6d2bf-106">The **glScaled** and [**glScalef**](glscalef.md) functions multiply the current matrix by a general scaling matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d2bf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d2bf-107">Syntax</span></span>


```C++
void WINAPI glScaled(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="6d2bf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d2bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d2bf-109">*x*</span><span class="sxs-lookup"><span data-stu-id="6d2bf-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="6d2bf-110">Коэффициент масштабирования по оси *x* .</span><span class="sxs-lookup"><span data-stu-id="6d2bf-110">Scale factors along the *x* axis.</span></span>

</dd> <dt>

<span data-ttu-id="6d2bf-111">*y*</span><span class="sxs-lookup"><span data-stu-id="6d2bf-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="6d2bf-112">Коэффициент масштабирования по оси *y* .</span><span class="sxs-lookup"><span data-stu-id="6d2bf-112">Scale factors along the *y* axis.</span></span>

</dd> <dt>

<span data-ttu-id="6d2bf-113">*гармошкой*</span><span class="sxs-lookup"><span data-stu-id="6d2bf-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="6d2bf-114">Масштабирование факторов по оси *z* .</span><span class="sxs-lookup"><span data-stu-id="6d2bf-114">Scale factors along the *z* axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d2bf-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d2bf-115">Return value</span></span>

<span data-ttu-id="6d2bf-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6d2bf-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6d2bf-117">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="6d2bf-117">Error codes</span></span>

<span data-ttu-id="6d2bf-118">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="6d2bf-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6d2bf-119">Имя</span><span class="sxs-lookup"><span data-stu-id="6d2bf-119">Name</span></span>                                                                                                  | <span data-ttu-id="6d2bf-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6d2bf-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d2bf-121"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="6d2bf-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6d2bf-122">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6d2bf-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6d2bf-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d2bf-123">Remarks</span></span>

<span data-ttu-id="6d2bf-124">Функция **глскалед** создает общее масштабирование вдоль осей *x*, *y* и *z* .</span><span class="sxs-lookup"><span data-stu-id="6d2bf-124">The **glScaled** function produces a general scaling along the *x*, *y*, and *z* axes.</span></span> <span data-ttu-id="6d2bf-125">Три аргумента указывают требуемые коэффициенты масштабирования по каждой из трех осей.</span><span class="sxs-lookup"><span data-stu-id="6d2bf-125">The three arguments indicate the desired scale factors along each of the three axes.</span></span> <span data-ttu-id="6d2bf-126">Результирующая матрица —</span><span class="sxs-lookup"><span data-stu-id="6d2bf-126">The resulting matrix is</span></span>

![Схема, показывающая матрицу коэффициентов масштабирования вдоль осей x, y и z.](images/scale01.png)

<span data-ttu-id="6d2bf-128">Текущая матрица (см. [**глматриксмоде**](glmatrixmode.md)) умножается на эту матрицу масштабирования, при этом продукт заменяется текущей матрицей.</span><span class="sxs-lookup"><span data-stu-id="6d2bf-128">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this scale matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="6d2bf-129">То есть, если M — это текущая матрица, а S — матрица масштабирования, то M заменяется на M S.</span><span class="sxs-lookup"><span data-stu-id="6d2bf-129">That is, if M is the current matrix and S is the scale matrix, then M is replaced with M   S.</span></span>

<span data-ttu-id="6d2bf-130">Если режим матрицы — GL \_ моделвиев или GL \_ , то вызывается масштабирование всех объектов, нарисованных после **глскалед** .</span><span class="sxs-lookup"><span data-stu-id="6d2bf-130">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glScaled** is called are scaled.</span></span> <span data-ttu-id="6d2bf-131">Используйте [**глпушматрикс**](glpushmatrix.md) и [**глпопматрикс**](glpopmatrix.md) для сохранения и восстановления немасштабируемой системы координат.</span><span class="sxs-lookup"><span data-stu-id="6d2bf-131">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the unscaled coordinate system.</span></span>

<span data-ttu-id="6d2bf-132">Если для матрицы моделвиев применяются коэффициенты масштабирования, отличные от 1,0, и включено освещение, автоматическая нормализация нормалей, вероятно, также должна быть включена ([**гленабле**](glenable.md) и [**глдисабле**](gldisable.md) с аргументом GL \_ нормализация).</span><span class="sxs-lookup"><span data-stu-id="6d2bf-132">If scale factors other than 1.0 are applied to the modelview matrix and lighting is enabled, automatic normalization of normals should probably also be enabled ([**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_NORMALIZE).</span></span>

<span data-ttu-id="6d2bf-133">Следующие функции извлекают сведения, относящиеся к **глскалед**:</span><span class="sxs-lookup"><span data-stu-id="6d2bf-133">The following functions retrieve information related to **glScaled**:</span></span>

<span data-ttu-id="6d2bf-134">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в \_ режиме матрицы GL \_</span><span class="sxs-lookup"><span data-stu-id="6d2bf-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="6d2bf-135">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ МОДЕЛВИЕВ \_ Матрица GL</span><span class="sxs-lookup"><span data-stu-id="6d2bf-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="6d2bf-136">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ матрица проекции главной книги \_</span><span class="sxs-lookup"><span data-stu-id="6d2bf-136">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="6d2bf-137">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ \_ Матрица текстуры GL</span><span class="sxs-lookup"><span data-stu-id="6d2bf-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="6d2bf-138">Требования</span><span class="sxs-lookup"><span data-stu-id="6d2bf-138">Requirements</span></span>



| <span data-ttu-id="6d2bf-139">Требование</span><span class="sxs-lookup"><span data-stu-id="6d2bf-139">Requirement</span></span> | <span data-ttu-id="6d2bf-140">Значение</span><span class="sxs-lookup"><span data-stu-id="6d2bf-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d2bf-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d2bf-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6d2bf-142">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6d2bf-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6d2bf-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d2bf-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6d2bf-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6d2bf-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6d2bf-145">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6d2bf-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d2bf-146"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d2bf-146"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6d2bf-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6d2bf-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d2bf-148"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d2bf-148"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6d2bf-149">DLL</span><span class="sxs-lookup"><span data-stu-id="6d2bf-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d2bf-150"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d2bf-150"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d2bf-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d2bf-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d2bf-152">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="6d2bf-152">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6d2bf-153">**гленд**</span><span class="sxs-lookup"><span data-stu-id="6d2bf-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6d2bf-154">**глматриксмоде**</span><span class="sxs-lookup"><span data-stu-id="6d2bf-154">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="6d2bf-155">**глмултматрикс**</span><span class="sxs-lookup"><span data-stu-id="6d2bf-155">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="6d2bf-156">**глпопматрикс**</span><span class="sxs-lookup"><span data-stu-id="6d2bf-156">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="6d2bf-157">**глпушматрикс**</span><span class="sxs-lookup"><span data-stu-id="6d2bf-157">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="6d2bf-158">**глротатед**</span><span class="sxs-lookup"><span data-stu-id="6d2bf-158">**glRotated**</span></span>](glrotated.md)
</dt> <dt>

[<span data-ttu-id="6d2bf-159">**глротатеф**</span><span class="sxs-lookup"><span data-stu-id="6d2bf-159">**glRotatef**</span></span>](glrotatef.md)
</dt> <dt>

[<span data-ttu-id="6d2bf-160">**глтранслате**</span><span class="sxs-lookup"><span data-stu-id="6d2bf-160">**glTranslate**</span></span>](gltranslate.md)
</dt> </dl>

 

 





