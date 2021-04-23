---
title: Функция Глфрустум (GL. h)
description: Функция Глфрустум Умножает текущую матрицу на матрицу перспективы.
ms.assetid: aa44c3fc-3bf6-4ef3-bb29-98e3056cdad3
keywords:
- Функция Глфрустум OpenGL
topic_type:
- apiref
api_name:
- glFrustum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce67879ca20819713e61a9392bf77be2f15211d5
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "104563506"
---
# <a name="glfrustum-function"></a><span data-ttu-id="6d99c-104">Функция Глфрустум</span><span class="sxs-lookup"><span data-stu-id="6d99c-104">glFrustum function</span></span>

<span data-ttu-id="6d99c-105">Функция **глфрустум** Умножает текущую матрицу на матрицу перспективы.</span><span class="sxs-lookup"><span data-stu-id="6d99c-105">The **glFrustum** function multiplies the current matrix by a perspective matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d99c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d99c-106">Syntax</span></span>


```C++
void WINAPI glFrustum(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a><span data-ttu-id="6d99c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d99c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d99c-108">*слева*</span><span class="sxs-lookup"><span data-stu-id="6d99c-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="6d99c-109">Координата вертикальной плоскости обрезки слева.</span><span class="sxs-lookup"><span data-stu-id="6d99c-109">The coordinate for the left-vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="6d99c-110">*Правильно*</span><span class="sxs-lookup"><span data-stu-id="6d99c-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="6d99c-111">Координата для правой вертикальной плоскости обрезки.</span><span class="sxs-lookup"><span data-stu-id="6d99c-111">The coordinate for the right-vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="6d99c-112">*Нижний*</span><span class="sxs-lookup"><span data-stu-id="6d99c-112">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="6d99c-113">Координата для нижней горизонтальной плоскости обрезки.</span><span class="sxs-lookup"><span data-stu-id="6d99c-113">The coordinate for the bottom-horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="6d99c-114">*В начало*</span><span class="sxs-lookup"><span data-stu-id="6d99c-114">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="6d99c-115">Координата для нижней горизонтальной плоскости обрезки.</span><span class="sxs-lookup"><span data-stu-id="6d99c-115">The coordinate for the bottom-horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="6d99c-116">*знеар*</span><span class="sxs-lookup"><span data-stu-id="6d99c-116">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="6d99c-117">Расстояния на плоскости обрезки близкой глубины.</span><span class="sxs-lookup"><span data-stu-id="6d99c-117">The distances to the near-depth clipping plane.</span></span> <span data-ttu-id="6d99c-118">Должно быть положительным.</span><span class="sxs-lookup"><span data-stu-id="6d99c-118">Must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="6d99c-119">*зфар*</span><span class="sxs-lookup"><span data-stu-id="6d99c-119">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="6d99c-120">Расстояния до дальней обрезанной плоскости.</span><span class="sxs-lookup"><span data-stu-id="6d99c-120">The distances to the far-depth clipping planes.</span></span> <span data-ttu-id="6d99c-121">Должно быть положительным.</span><span class="sxs-lookup"><span data-stu-id="6d99c-121">Must be positive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d99c-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d99c-122">Return value</span></span>

<span data-ttu-id="6d99c-123">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6d99c-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6d99c-124">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="6d99c-124">Error codes</span></span>

<span data-ttu-id="6d99c-125">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="6d99c-125">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6d99c-126">Имя</span><span class="sxs-lookup"><span data-stu-id="6d99c-126">Name</span></span>                                                                                                  | <span data-ttu-id="6d99c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6d99c-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d99c-128"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="6d99c-128"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="6d99c-129">*знеар* или *зфар* не поститиве.</span><span class="sxs-lookup"><span data-stu-id="6d99c-129">*zNear* or *zFar* was not postitive.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="6d99c-130"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="6d99c-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6d99c-131">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6d99c-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6d99c-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d99c-132">Remarks</span></span>

<span data-ttu-id="6d99c-133">Функция **глфрустум** описывает матрицу перспективы, которая создает перспективную проекцию.</span><span class="sxs-lookup"><span data-stu-id="6d99c-133">The **glFrustum** function describes a perspective matrix that produces a perspective projection.</span></span> <span data-ttu-id="6d99c-134">Параметры (*левый*, *Нижний*, *знеар*) и (*правый*, *верхний*, *знеар*) указывают точки на близкой плоскости, которые сопоставлены с нижним левым и верхним правым углами окна соответственно, предполагая, что глаз находится в (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="6d99c-134">The (*left*, *bottom*, *zNear*) and (*right*, *top*, *zNear*) parameters specify the points on the near clipping plane that are mapped to the lower-left and upper-right corners of the window, respectively, assuming that the eye is located at (0,0,0).</span></span> <span data-ttu-id="6d99c-135">Параметр *зфар* задает расположение дальней плоскости.</span><span class="sxs-lookup"><span data-stu-id="6d99c-135">The *zFar* parameter specifies the location of the far clipping plane.</span></span> <span data-ttu-id="6d99c-136">Оба *знеар* и *зфар* должны быть положительными.</span><span class="sxs-lookup"><span data-stu-id="6d99c-136">Both *zNear* and *zFar* must be positive.</span></span> <span data-ttu-id="6d99c-137">Соответствующая матрица показана на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="6d99c-137">The corresponding matrix is shown in the following image.</span></span>

![Диаграмма, показывающая матрицу перспективы, которая создает перспективную проекцию.](images/frust01.png)![Уравнения, отображающие функцию Глфрустум, описывающую матрицу перспективы.](images/frust02.png)

<span data-ttu-id="6d99c-140">Функция **глфрустум** Умножает текущую матрицу на эту матрицу с результатом замены текущей матрицы.</span><span class="sxs-lookup"><span data-stu-id="6d99c-140">The **glFrustum** function multiplies the current matrix by this matrix, with the result replacing the current matrix.</span></span> <span data-ttu-id="6d99c-141">То есть, если M — это текущая матрица, а F — матрица фрустум перспективы, **глфрустум** заменяет M на m F.</span><span class="sxs-lookup"><span data-stu-id="6d99c-141">That is, if M is the current matrix and F is the frustum perspective matrix, then **glFrustum** replaces M with M   F.</span></span>

<span data-ttu-id="6d99c-142">Используйте [**глпушматрикс**](glpushmatrix.md) и [**глпопматрикс**](glpopmatrix.md) для сохранения и восстановления текущего стека матриц.</span><span class="sxs-lookup"><span data-stu-id="6d99c-142">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the current matrix stack.</span></span>

<span data-ttu-id="6d99c-143">На точность буфера глубины влияют значения, указанные для *знеар* и *зфар*.</span><span class="sxs-lookup"><span data-stu-id="6d99c-143">Depth-buffer precision is affected by the values specified for *zNear* and *zFar*.</span></span> <span data-ttu-id="6d99c-144">Чем больше соотношение *зфар* к *знеар* , тем менее эффективный буфер глубины будет различен между поверхностями, расположенными рядом друг с другом.</span><span class="sxs-lookup"><span data-stu-id="6d99c-144">The greater the ratio of *zFar* to *zNear* is, the less effective the depth buffer will be at distinguishing between surfaces that are near each other.</span></span> <span data-ttu-id="6d99c-145">If</span><span class="sxs-lookup"><span data-stu-id="6d99c-145">If</span></span>

![Уравнение, показывающее отношение далеко к ближайшему.](images/frust03.png)

<span data-ttu-id="6d99c-147">примерно все биты *журнала* с точностью 2 (*r*) теряют точность буфера глубины.</span><span class="sxs-lookup"><span data-stu-id="6d99c-147">roughly *log* 2 (*r*) bits of depth buffer precision are lost.</span></span> <span data-ttu-id="6d99c-148">Так как *r* приближается к бесконечности, так как *знеар* приближается к нулю, никогда не следует устанавливать *знеар* в ноль.</span><span class="sxs-lookup"><span data-stu-id="6d99c-148">Because *r* approaches infinity as *zNear* approaches zero, you should never set *zNear* to zero.</span></span>

<span data-ttu-id="6d99c-149">Следующие функции извлекают сведения о **глфрустум**:</span><span class="sxs-lookup"><span data-stu-id="6d99c-149">The following functions retrieve information about **glFrustum**:</span></span>

<span data-ttu-id="6d99c-150">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в \_ режиме матрицы GL \_</span><span class="sxs-lookup"><span data-stu-id="6d99c-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="6d99c-151">**глжет** с аргументом \_ МОДЕЛВИЕВ \_ Матрица GL</span><span class="sxs-lookup"><span data-stu-id="6d99c-151">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="6d99c-152">**глжет** с аргументом \_ матрица проекции главной книги \_</span><span class="sxs-lookup"><span data-stu-id="6d99c-152">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="6d99c-153">**глжет** с аргументом \_ \_ Матрица текстуры GL</span><span class="sxs-lookup"><span data-stu-id="6d99c-153">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="6d99c-154">Требования</span><span class="sxs-lookup"><span data-stu-id="6d99c-154">Requirements</span></span>



| <span data-ttu-id="6d99c-155">Требование</span><span class="sxs-lookup"><span data-stu-id="6d99c-155">Requirement</span></span> | <span data-ttu-id="6d99c-156">Значение</span><span class="sxs-lookup"><span data-stu-id="6d99c-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d99c-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d99c-157">Minimum supported client</span></span><br/> | <span data-ttu-id="6d99c-158">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6d99c-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6d99c-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d99c-159">Minimum supported server</span></span><br/> | <span data-ttu-id="6d99c-160">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6d99c-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6d99c-161">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6d99c-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d99c-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d99c-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6d99c-163">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6d99c-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d99c-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d99c-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6d99c-165">DLL</span><span class="sxs-lookup"><span data-stu-id="6d99c-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d99c-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d99c-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d99c-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d99c-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d99c-168">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="6d99c-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6d99c-169">**гленд**</span><span class="sxs-lookup"><span data-stu-id="6d99c-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6d99c-170">**глжет**</span><span class="sxs-lookup"><span data-stu-id="6d99c-170">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="6d99c-171">**глматриксмоде**</span><span class="sxs-lookup"><span data-stu-id="6d99c-171">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="6d99c-172">**глмултматрикс**</span><span class="sxs-lookup"><span data-stu-id="6d99c-172">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="6d99c-173">**глорсо**</span><span class="sxs-lookup"><span data-stu-id="6d99c-173">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="6d99c-174">**глпопматрикс**</span><span class="sxs-lookup"><span data-stu-id="6d99c-174">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="6d99c-175">**глпушматрикс**</span><span class="sxs-lookup"><span data-stu-id="6d99c-175">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="6d99c-176">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="6d99c-176">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





