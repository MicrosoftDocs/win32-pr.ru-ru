---
title: Функция Глпикселзум (GL. h)
description: Функция Глпикселзум задает коэффициенты масштабирования пикселя.
ms.assetid: 57ead7d8-0502-46b4-9f66-dbb3cb75b0f9
keywords:
- Функция Глпикселзум OpenGL
topic_type:
- apiref
api_name:
- glPixelZoom
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 065e1735ca0228046cfb08e2fb441d3cdc02af74
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105664791"
---
# <a name="glpixelzoom-function"></a><span data-ttu-id="b4b7b-104">Функция Глпикселзум</span><span class="sxs-lookup"><span data-stu-id="b4b7b-104">glPixelZoom function</span></span>

<span data-ttu-id="b4b7b-105">Функция **глпикселзум** задает коэффициенты масштабирования пикселя.</span><span class="sxs-lookup"><span data-stu-id="b4b7b-105">The **glPixelZoom** function specifies the pixel zoom factors.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4b7b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4b7b-106">Syntax</span></span>


```C++
void WINAPI glPixelZoom(
   GLfloat xfactor,
   GLfloat yfactor
);
```



## <a name="parameters"></a><span data-ttu-id="b4b7b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4b7b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4b7b-108">*ксфактор*</span><span class="sxs-lookup"><span data-stu-id="b4b7b-108">*xfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="b4b7b-109">Коэффициент масштабирования по *оси x* для операций записи в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b4b7b-109">The *x* zoom factor for pixel write operations.</span></span>

</dd> <dt>

<span data-ttu-id="b4b7b-110">*ифактор*</span><span class="sxs-lookup"><span data-stu-id="b4b7b-110">*yfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="b4b7b-111">Коэффициент масштабирования *y* для операций записи в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b4b7b-111">The *y* zoom factor for pixel write operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4b7b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4b7b-112">Return value</span></span>

<span data-ttu-id="b4b7b-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b4b7b-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b4b7b-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b4b7b-114">Error codes</span></span>

<span data-ttu-id="b4b7b-115">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="b4b7b-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b4b7b-116">Имя</span><span class="sxs-lookup"><span data-stu-id="b4b7b-116">Name</span></span>                                                                                                  | <span data-ttu-id="b4b7b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b4b7b-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b4b7b-118"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b4b7b-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b4b7b-119">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b4b7b-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b4b7b-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4b7b-120">Remarks</span></span>

<span data-ttu-id="b4b7b-121">Функция **глпикселзум** задает значения для коэффициентов масштабирования *x* и *y* .</span><span class="sxs-lookup"><span data-stu-id="b4b7b-121">The **glPixelZoom** function specifies values for the *x* and *y* zoom factors.</span></span> <span data-ttu-id="b4b7b-122">При выполнении [**глдравпикселс**](gldrawpixels.md) или [**глкопипикселс**](glcopypixels.md), если (*x*<sub>r</sub> ,*y*<sub>r</sub> ) является текущей позицией в виде растрового изображения, а заданный элемент находится в *n*-ой строке и *м* ом столбце пиксельного прямоугольника, то пиксели, центры которых находятся в прямоугольнике с углами в</span><span class="sxs-lookup"><span data-stu-id="b4b7b-122">During the execution of [**glDrawPixels**](gldrawpixels.md) or [**glCopyPixels**](glcopypixels.md), if (*x*<sub>r</sub> ,*y*<sub>r</sub> ) is the current raster position, and a given element is in the *n* th row and *m* th column of the pixel rectangle, then pixels whose centers are in the rectangle with corners at</span></span>

![Уравнение, показывающее места, где Пиксели являются кандидатами на замену.](images/pix05.png)

<span data-ttu-id="b4b7b-124">являются кандидатами на замену.</span><span class="sxs-lookup"><span data-stu-id="b4b7b-124">are candidates for replacement.</span></span> <span data-ttu-id="b4b7b-125">Все пиксели, центр которых находится на нижнем или левом краю этой прямоугольной области, также изменяются.</span><span class="sxs-lookup"><span data-stu-id="b4b7b-125">Any pixel whose center lies on the bottom or left edge of this rectangular region is also modified.</span></span>

<span data-ttu-id="b4b7b-126">Коэффициенты масштабирования пикселей не ограничиваются положительными значениями.</span><span class="sxs-lookup"><span data-stu-id="b4b7b-126">Pixel zoom factors are not limited to positive values.</span></span> <span data-ttu-id="b4b7b-127">Отрицательные коэффициенты масштабирования соответствуют полученному изображению относительно текущей координаты.</span><span class="sxs-lookup"><span data-stu-id="b4b7b-127">Negative zoom factors reflect the resulting image about the current raster position.</span></span>

<span data-ttu-id="b4b7b-128">Следующие функции извлекают сведения, относящиеся к **глпикселзум**:</span><span class="sxs-lookup"><span data-stu-id="b4b7b-128">The following functions retrieve information related to **glPixelZoom**:</span></span>

<span data-ttu-id="b4b7b-129">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ Zoom \_ X</span><span class="sxs-lookup"><span data-stu-id="b4b7b-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ZOOM\_X</span></span>

<span data-ttu-id="b4b7b-130">**глжет** с аргументом GL \_ Zoom \_ Y</span><span class="sxs-lookup"><span data-stu-id="b4b7b-130">**glGet** with argument GL\_ZOOM\_Y</span></span>

## <a name="requirements"></a><span data-ttu-id="b4b7b-131">Требования</span><span class="sxs-lookup"><span data-stu-id="b4b7b-131">Requirements</span></span>



| <span data-ttu-id="b4b7b-132">Требование</span><span class="sxs-lookup"><span data-stu-id="b4b7b-132">Requirement</span></span> | <span data-ttu-id="b4b7b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="b4b7b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b7b-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4b7b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b4b7b-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b4b7b-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b4b7b-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4b7b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b4b7b-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b4b7b-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b4b7b-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b4b7b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4b7b-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4b7b-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b4b7b-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b4b7b-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="b4b7b-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4b7b-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b4b7b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b4b7b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4b7b-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4b7b-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4b7b-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4b7b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4b7b-145">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="b4b7b-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b4b7b-146">**глкопипикселс**</span><span class="sxs-lookup"><span data-stu-id="b4b7b-146">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="b4b7b-147">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="b4b7b-147">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="b4b7b-148">**гленд**</span><span class="sxs-lookup"><span data-stu-id="b4b7b-148">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





