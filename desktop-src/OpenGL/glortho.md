---
title: Функция Глорсо (GL. h)
description: Функция Глорсо Умножает текущую матрицу на ортогональную матрицу.
ms.assetid: 5c70819f-e9b6-49e2-add5-9f6e6aba26ee
keywords:
- Функция Глорсо OpenGL
topic_type:
- apiref
api_name:
- glOrtho
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46abbb0edd2dfc7fc51aaf7fa6519dc5367b109c
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "104568615"
---
# <a name="glortho-function"></a><span data-ttu-id="e5874-104">Функция Глорсо</span><span class="sxs-lookup"><span data-stu-id="e5874-104">glOrtho function</span></span>

<span data-ttu-id="e5874-105">Функция **глорсо** Умножает текущую матрицу на ортогональную матрицу.</span><span class="sxs-lookup"><span data-stu-id="e5874-105">The **glOrtho** function multiplies the current matrix by an orthographic matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5874-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5874-106">Syntax</span></span>


```C++
void WINAPI glOrtho(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a><span data-ttu-id="e5874-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5874-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5874-108">*слева*</span><span class="sxs-lookup"><span data-stu-id="e5874-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="e5874-109">Координаты левой вертикальной плоскости обрезки.</span><span class="sxs-lookup"><span data-stu-id="e5874-109">The coordinates for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="e5874-110">*Правильно*</span><span class="sxs-lookup"><span data-stu-id="e5874-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="e5874-111">Координаты вертикальной плоскости обрезки серигхт.</span><span class="sxs-lookup"><span data-stu-id="e5874-111">The coordinates for theright vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="e5874-112">*Нижний*</span><span class="sxs-lookup"><span data-stu-id="e5874-112">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="e5874-113">Координаты нижней горизонтальной плоскости отсечения.</span><span class="sxs-lookup"><span data-stu-id="e5874-113">The coordinates for the bottom horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="e5874-114">*В начало*</span><span class="sxs-lookup"><span data-stu-id="e5874-114">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="e5874-115">Координаты верхних горизонтальных планов отсечения.</span><span class="sxs-lookup"><span data-stu-id="e5874-115">The coordinates for the top horizontal clipping plans.</span></span>

</dd> <dt>

<span data-ttu-id="e5874-116">*знеар*</span><span class="sxs-lookup"><span data-stu-id="e5874-116">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="e5874-117">Расстояния до плоскости усечения глубины.</span><span class="sxs-lookup"><span data-stu-id="e5874-117">The distances to the nearer depth clipping plane.</span></span> <span data-ttu-id="e5874-118">Это расстояние является отрицательным, если плоскость находится за пределами средства просмотра.</span><span class="sxs-lookup"><span data-stu-id="e5874-118">This distance is negative if the plane is to be behind the viewer.</span></span>

</dd> <dt>

<span data-ttu-id="e5874-119">*зфар*</span><span class="sxs-lookup"><span data-stu-id="e5874-119">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="e5874-120">Расстояния на плоскости усечения глубины.</span><span class="sxs-lookup"><span data-stu-id="e5874-120">The distances to the farther depth clipping plane.</span></span> <span data-ttu-id="e5874-121">Это расстояние является отрицательным, если плоскость находится за пределами средства просмотра.</span><span class="sxs-lookup"><span data-stu-id="e5874-121">This distance is negative if the plane is to be behind the viewer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5874-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5874-122">Return value</span></span>

<span data-ttu-id="e5874-123">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e5874-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e5874-124">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="e5874-124">Error codes</span></span>

<span data-ttu-id="e5874-125">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="e5874-125">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e5874-126">Имя</span><span class="sxs-lookup"><span data-stu-id="e5874-126">Name</span></span>                                                                                                  | <span data-ttu-id="e5874-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e5874-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e5874-128"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e5874-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e5874-129">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e5874-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e5874-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5874-130">Remarks</span></span>

<span data-ttu-id="e5874-131">Функция **глорсо** описывает матрицу перспективы, которая создает параллельную проекцию.</span><span class="sxs-lookup"><span data-stu-id="e5874-131">The **glOrtho** function describes a perspective matrix that produces a parallel projection.</span></span> <span data-ttu-id="e5874-132">Параметры (*слева*, *снизу*, *вблизи*) и (*справа*, *сверху*, *вблизи*) указывают точки на близкой плоскости, которые сопоставлены с нижним левым и верхним правым углами окна соответственно, предполагая, что глаз находится в (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="e5874-132">The (*left*, *bottom*, *near*) and (*right*, *top*, *near*) parameters specify the points on the near clipping plane that are mapped to the lower-left and upper-right corners of the window, respectively, assuming that the eye is located at (0, 0, 0).</span></span> <span data-ttu-id="e5874-133">Параметр *FAR* задает расположение дальней плоскости.</span><span class="sxs-lookup"><span data-stu-id="e5874-133">The *far* parameter specifies the location of the far clipping plane.</span></span> <span data-ttu-id="e5874-134">Оба *знеар* и *зфар* могут быть либо положительными, либо отрицательными.</span><span class="sxs-lookup"><span data-stu-id="e5874-134">Both *zNear* and *zFar* can be either positive or negative.</span></span> <span data-ttu-id="e5874-135">Соответствующая матрица показана на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="e5874-135">The corresponding matrix is shown in the following image.</span></span>

![Схема, показывающая матрицу перспективы, которую описывает функция Глорсо.](images/ortho1.png)

<span data-ttu-id="e5874-137">where</span><span class="sxs-lookup"><span data-stu-id="e5874-137">where</span></span>

![Уравнения, описывающие матрицу перспективы.](images/ortho2.png)

<span data-ttu-id="e5874-139">Текущая матрица умножается на эту матрицу с результатом замены текущей матрицы.</span><span class="sxs-lookup"><span data-stu-id="e5874-139">The current matrix is multiplied by this matrix with the result replacing the current matrix.</span></span> <span data-ttu-id="e5874-140">То есть, если M — это текущая матрица, а O — матрица Орсо, то M заменяется на M O.</span><span class="sxs-lookup"><span data-stu-id="e5874-140">That is, if M is the current matrix and O is the ortho matrix, then M is replaced with M   O.</span></span>

<span data-ttu-id="e5874-141">Используйте [**глпушматрикс**](glpushmatrix.md) и **глпопматрикс** для сохранения и восстановления текущего стека матриц.</span><span class="sxs-lookup"><span data-stu-id="e5874-141">Use [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** to save and restore the current matrix stack.</span></span> <span data-ttu-id="e5874-142">Чтобы задать текущую матрицу, используйте [**глматриксмоде**](glmatrixmode.md) .</span><span class="sxs-lookup"><span data-stu-id="e5874-142">Use [**glMatrixMode**](glmatrixmode.md) to set the current matrix.</span></span>

<span data-ttu-id="e5874-143">Следующие функции извлекают сведения, относящиеся к **глорсо**:</span><span class="sxs-lookup"><span data-stu-id="e5874-143">The following functions retrieve information related to **glOrtho**:</span></span>

<span data-ttu-id="e5874-144">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в \_ режиме матрицы GL \_</span><span class="sxs-lookup"><span data-stu-id="e5874-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="e5874-145">**глжет** с аргументом \_ МОДЕЛВИЕВ \_ Матрица GL</span><span class="sxs-lookup"><span data-stu-id="e5874-145">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="e5874-146">**глжет** с аргументом \_ матрица проекции главной книги \_</span><span class="sxs-lookup"><span data-stu-id="e5874-146">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="e5874-147">**глжет** с аргументом \_ \_ Матрица текстуры GL</span><span class="sxs-lookup"><span data-stu-id="e5874-147">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="e5874-148">Требования</span><span class="sxs-lookup"><span data-stu-id="e5874-148">Requirements</span></span>



| <span data-ttu-id="e5874-149">Требование</span><span class="sxs-lookup"><span data-stu-id="e5874-149">Requirement</span></span> | <span data-ttu-id="e5874-150">Значение</span><span class="sxs-lookup"><span data-stu-id="e5874-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5874-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5874-151">Minimum supported client</span></span><br/> | <span data-ttu-id="e5874-152">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e5874-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e5874-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5874-153">Minimum supported server</span></span><br/> | <span data-ttu-id="e5874-154">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e5874-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e5874-155">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e5874-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5874-156"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5874-156"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e5874-157">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e5874-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="e5874-158"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5874-158"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e5874-159">DLL</span><span class="sxs-lookup"><span data-stu-id="e5874-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5874-160"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5874-160"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5874-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5874-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5874-162">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="e5874-162">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e5874-163">**гленд**</span><span class="sxs-lookup"><span data-stu-id="e5874-163">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e5874-164">**глфрустум**</span><span class="sxs-lookup"><span data-stu-id="e5874-164">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="e5874-165">**глматриксмоде**</span><span class="sxs-lookup"><span data-stu-id="e5874-165">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="e5874-166">**глмултматрикс**</span><span class="sxs-lookup"><span data-stu-id="e5874-166">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="e5874-167">**глпушматрикс**</span><span class="sxs-lookup"><span data-stu-id="e5874-167">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="e5874-168">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="e5874-168">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





