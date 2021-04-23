---
title: Функция glCopyTexSubImage2D (GL. h)
description: Функция glCopyTexSubImage2D копирует подизображение двухмерного изображения текстуры из буфера кадров.
ms.assetid: cbb644d4-6a23-4d66-8599-5f8b48e9b91f
keywords:
- Функция glCopyTexSubImage2D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c966d031bb154b59cc54ae2e5d254347aa88d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415693"
---
# <a name="glcopytexsubimage2d-function"></a><span data-ttu-id="02eaf-104">Функция glCopyTexSubImage2D</span><span class="sxs-lookup"><span data-stu-id="02eaf-104">glCopyTexSubImage2D function</span></span>

<span data-ttu-id="02eaf-105">Функция **glCopyTexSubImage2D** копирует подизображение двухмерного изображения текстуры из буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="02eaf-105">The **glCopyTexSubImage2D** function copies a sub-image of a two-dimensional texture image from the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="02eaf-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02eaf-106">Syntax</span></span>


```C++
void WINAPI glCopyTexSubImage2D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   yoffset,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="02eaf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="02eaf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02eaf-108">*target*</span><span class="sxs-lookup"><span data-stu-id="02eaf-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="02eaf-109">Целевой объект, в который будут изменяться данные изображения.</span><span class="sxs-lookup"><span data-stu-id="02eaf-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="02eaf-110">Должно иметь значение \_ 2D текстуры GL \_ .</span><span class="sxs-lookup"><span data-stu-id="02eaf-110">Must have the value GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="02eaf-111">*level*</span><span class="sxs-lookup"><span data-stu-id="02eaf-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="02eaf-112">Номер уровня детализации.</span><span class="sxs-lookup"><span data-stu-id="02eaf-112">The level-of-detail number.</span></span> <span data-ttu-id="02eaf-113">Уровень 0 — базовый образ.</span><span class="sxs-lookup"><span data-stu-id="02eaf-113">Level 0 is the base image.</span></span> <span data-ttu-id="02eaf-114">Уровень *n* — это *n*-ое изображение для сокращения mipmap.</span><span class="sxs-lookup"><span data-stu-id="02eaf-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="02eaf-115">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="02eaf-115">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="02eaf-116">Смещение шаг текселя в направлении *x* в пределах массива текстуры.</span><span class="sxs-lookup"><span data-stu-id="02eaf-116">The texel offset in the *x* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="02eaf-117">*йоффсет*</span><span class="sxs-lookup"><span data-stu-id="02eaf-117">*yoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="02eaf-118">Смещение шаг текселя в направлении *оси y* в пределах массива текстуры.</span><span class="sxs-lookup"><span data-stu-id="02eaf-118">The texel offset in the *y* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="02eaf-119">*x*</span><span class="sxs-lookup"><span data-stu-id="02eaf-119">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="02eaf-120">Координата x окна координаты левого нижнего угла строки пикселей для копирования.</span><span class="sxs-lookup"><span data-stu-id="02eaf-120">The window x-plane coordinates of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="02eaf-121">*y*</span><span class="sxs-lookup"><span data-stu-id="02eaf-121">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="02eaf-122">Координата точки y окна нижнего левого угла копируемой строки пикселей.</span><span class="sxs-lookup"><span data-stu-id="02eaf-122">The window y-plane coordinates of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="02eaf-123">*width*</span><span class="sxs-lookup"><span data-stu-id="02eaf-123">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="02eaf-124">Ширина подобраза изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="02eaf-124">The width of the sub-image of the texture image.</span></span> <span data-ttu-id="02eaf-125">Указание подобраза текстуры с нулевой шириной не оказывает влияния.</span><span class="sxs-lookup"><span data-stu-id="02eaf-125">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="02eaf-126">*height*</span><span class="sxs-lookup"><span data-stu-id="02eaf-126">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="02eaf-127">Высота подизображения изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="02eaf-127">The height of the sub-image of the texture image.</span></span> <span data-ttu-id="02eaf-128">Указание подобраза текстуры с нулевой шириной не оказывает влияния.</span><span class="sxs-lookup"><span data-stu-id="02eaf-128">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02eaf-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02eaf-129">Return value</span></span>

<span data-ttu-id="02eaf-130">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="02eaf-130">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="02eaf-131">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="02eaf-131">Error codes</span></span>

<span data-ttu-id="02eaf-132">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="02eaf-132">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="02eaf-133">Имя</span><span class="sxs-lookup"><span data-stu-id="02eaf-133">Name</span></span>                                                                                                  | <span data-ttu-id="02eaf-134">Значение</span><span class="sxs-lookup"><span data-stu-id="02eaf-134">Meaning</span></span>                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="02eaf-135"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="02eaf-135"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="02eaf-136">значение *цели* не было принято.</span><span class="sxs-lookup"><span data-stu-id="02eaf-136">*target* was not an accepted value.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="02eaf-137"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="02eaf-137"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="02eaf-138">*уровень* был меньше нуля или больше, чем *log* 2 (*Max*), где *Max* — это возвращаемое значение для \_ максимального \_ размера текстуры GL \_ .</span><span class="sxs-lookup"><span data-stu-id="02eaf-138">*level* was less than zero or greater than *log* 2 (*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="02eaf-139"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="02eaf-139"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="02eaf-140">*ксоффсет* меньше *границы* или (  +  *Ширина* ксоффсет) больше (*w*  +  *border*), *йоффсет* была меньше *границы* или (*йоффсет*  +  *Высота*) больше (граница в *h*  +  ), где *w* — толщина текстуры GL, \_ \_ а *граница* — это \_ граница текстуры GL \_ .</span><span class="sxs-lookup"><span data-stu-id="02eaf-140">*xoffset* was less than *border* or (*xoffset* + *width*)was greater than (*w* + *border*), *yoffset* was less than *border*, or (*yoffset* + *height*) was greater than (*h* + *border*), where *w* is GL\_TEXTURE\_WIDTH and *border* is GL\_TEXTURE\_BORDER.</span></span> <span data-ttu-id="02eaf-141">Обратите внимание, что *w* включает в себя вдвое ширину *границы* .</span><span class="sxs-lookup"><span data-stu-id="02eaf-141">Note that *w* includes twice the *border* width.</span></span><br/> |
| <dl> <span data-ttu-id="02eaf-142"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="02eaf-142"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="02eaf-143">*Ширина* меньше *границы* или *y* меньше *границы*, где *border* является шириной границы для массива текстуры.</span><span class="sxs-lookup"><span data-stu-id="02eaf-143">*width* was less than *border* or *y* was less than *border*, where *border* is the border width of the texture array.</span></span><br/>                                                                                                                                                                                           |
| <dl> <span data-ttu-id="02eaf-144"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="02eaf-144"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="02eaf-145">Массив текстуры не был определен предыдущей операцией [**glTexImage1D**](glteximage1d.md) .</span><span class="sxs-lookup"><span data-stu-id="02eaf-145">The texture array was not defined by a previous [**glTexImage1D**](glteximage1d.md) operation.</span></span><br/>                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="02eaf-146"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="02eaf-146"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="02eaf-147">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="02eaf-147">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="02eaf-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02eaf-148">Remarks</span></span>

<span data-ttu-id="02eaf-149">Функция **glCopyTexSubImage2D** заменяет прямоугольную часть двухмерного изображения текстуры на пиксели из текущего буфера кадров, а не из основной памяти, как в случае с [**glTexSubImage2D**](gltexsubimage2d.md).</span><span class="sxs-lookup"><span data-stu-id="02eaf-149">The **glCopyTexSubImage2D** function replaces a rectangular portion of a two-dimensional texture image with pixels from the current framebuffer, rather than from main memory as is the case for [**glTexSubImage2D**](gltexsubimage2d.md).</span></span>

<span data-ttu-id="02eaf-150">Прямоугольник пикселей, начинающийся с координат окна *x* и *y* , а также с *шириной* и *высотой* измерений заменяет часть массива текстуры индексами, *ксоффсет* через *ксоффсет* + (*Width* -1), с индексами *йоффсет* через *йоффсет* + (*Width* -1) на уровне mipmap, заданном параметром *Level*.</span><span class="sxs-lookup"><span data-stu-id="02eaf-150">A rectangle of pixels beginning with the *x* and *y* window coordinates and with the dimensions *width* and *height* replaces the portion of the texture array with the indexes *xoffset* through *xoffset* + (*width* - 1), with the indexes *yoffset* through *yoffset* + (*width* - 1) at the mipmap level specified by *level*.</span></span> <span data-ttu-id="02eaf-151">Прямоугольник назначения в массиве текстур не может содержать пикселей текстуры за пределами изначально заданного массива текстуры.</span><span class="sxs-lookup"><span data-stu-id="02eaf-151">The destination rectangle in the texture array cannot include any texels outside the originally specified texture array.</span></span>

<span data-ttu-id="02eaf-152">Функция **glCopyTexSubImage2D** обрабатывает пикселы в строке таким же образом, как и [**глкопипикселс**](glcopypixels.md), за исключением того, что перед завершающим преобразованием пикселов все значения компонентов пикселов записываются в диапазон \[ 0, 1 \] и преобразуются в внутренний формат текстуры для хранения в массиве текстуры.</span><span class="sxs-lookup"><span data-stu-id="02eaf-152">The **glCopyTexSubImage2D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md), except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="02eaf-153">Порядок пикселей определяется с помощью более низких координат *x* , соответствующих более низким координатам текстуры.</span><span class="sxs-lookup"><span data-stu-id="02eaf-153">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="02eaf-154">Если любой из пикселов в заданной строке текущего буфера кадров находится за пределами окна, связанного с текущим контекстом отрисовки, то их значения не определены.</span><span class="sxs-lookup"><span data-stu-id="02eaf-154">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="02eaf-155">Если любой из пикселов в указанном прямоугольнике текущего буфера кадров находится вне окна чтения, связанного с текущим контекстом отрисовки, значения, полученные для этих пикселов, не определены.</span><span class="sxs-lookup"><span data-stu-id="02eaf-155">If any of the pixels within the specified rectangle of the current framebuffer are outside the read window associated with the current rendering context, then the values obtained for those pixels are undefined.</span></span> <span data-ttu-id="02eaf-156">В параметрах *интерналформат*, *Width*, *Height* или *border* указанного массива текстуры не вносятся изменения, либо значения шаг текселя за пределами указанного подизображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="02eaf-156">No change is made to the *internalFormat*, *width*, *height*, or *border* parameter of the specified texture array or to texel values outside the specified texture sub-image.</span></span>

<span data-ttu-id="02eaf-157">В списки вывода нельзя включать вызовы **glCopyTexSubImage2D** .</span><span class="sxs-lookup"><span data-stu-id="02eaf-157">You cannot include calls to **glCopyTexSubImage2D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="02eaf-158">Функция **glCopyTexSubImage2D** доступна только в OpenGL версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="02eaf-158">The **glCopyTexSubImage2D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="02eaf-159">Текстурирование не влияет на режим индексирования цветов.</span><span class="sxs-lookup"><span data-stu-id="02eaf-159">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="02eaf-160">Функции [**глпикселсторе**](glpixelstore-functions.md) и [**глпикселтрансфер**](glpixeltransfer.md) влияют на изображения текстур точно так же, как они влияют на способ прорисовки пикселов с помощью [**глдравпикселс**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="02eaf-160">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect the way pixels are drawn using [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="02eaf-161">Следующие функции извлекают сведения, относящиеся к **glCopyTexSubImage2D**:</span><span class="sxs-lookup"><span data-stu-id="02eaf-161">The following functions retrieve information related to **glCopyTexSubImage2D**:</span></span>

[<span data-ttu-id="02eaf-162">**глжеттексимаже**</span><span class="sxs-lookup"><span data-stu-id="02eaf-162">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="02eaf-163">[**глисенаблед**](glisenabled.md) с аргументом GL \_ текстуры \_ 2D</span><span class="sxs-lookup"><span data-stu-id="02eaf-163">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="02eaf-164">Требования</span><span class="sxs-lookup"><span data-stu-id="02eaf-164">Requirements</span></span>



| <span data-ttu-id="02eaf-165">Требование</span><span class="sxs-lookup"><span data-stu-id="02eaf-165">Requirement</span></span> | <span data-ttu-id="02eaf-166">Значение</span><span class="sxs-lookup"><span data-stu-id="02eaf-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02eaf-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02eaf-167">Minimum supported client</span></span><br/> | <span data-ttu-id="02eaf-168">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="02eaf-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="02eaf-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02eaf-169">Minimum supported server</span></span><br/> | <span data-ttu-id="02eaf-170">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="02eaf-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="02eaf-171">Заголовок</span><span class="sxs-lookup"><span data-stu-id="02eaf-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="02eaf-172"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="02eaf-172"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="02eaf-173">Библиотека</span><span class="sxs-lookup"><span data-stu-id="02eaf-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="02eaf-174"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02eaf-174"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="02eaf-175">DLL</span><span class="sxs-lookup"><span data-stu-id="02eaf-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02eaf-176"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02eaf-176"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02eaf-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02eaf-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02eaf-178">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="02eaf-178">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="02eaf-179">**глкопипикселс**</span><span class="sxs-lookup"><span data-stu-id="02eaf-179">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="02eaf-180">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="02eaf-180">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="02eaf-181">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="02eaf-181">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="02eaf-182">**гленд**</span><span class="sxs-lookup"><span data-stu-id="02eaf-182">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="02eaf-183">**глфог**</span><span class="sxs-lookup"><span data-stu-id="02eaf-183">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="02eaf-184">**глпикселсторе**</span><span class="sxs-lookup"><span data-stu-id="02eaf-184">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="02eaf-185">**глпикселтрансфер**</span><span class="sxs-lookup"><span data-stu-id="02eaf-185">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="02eaf-186">**глтексенв**</span><span class="sxs-lookup"><span data-stu-id="02eaf-186">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="02eaf-187">**глтексжен**</span><span class="sxs-lookup"><span data-stu-id="02eaf-187">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="02eaf-188">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="02eaf-188">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="02eaf-189">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="02eaf-189">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="02eaf-190">**глтекспараметер**</span><span class="sxs-lookup"><span data-stu-id="02eaf-190">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





