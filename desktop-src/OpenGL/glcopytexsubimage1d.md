---
title: Функция glCopyTexSubImage1D (GL. h)
description: Функция glCopyTexSubImage1D копирует подизображение одномерного изображения текстуры из буфера кадров.
ms.assetid: 718aee8a-6dce-49e1-a441-19beccd89f8d
keywords:
- Функция glCopyTexSubImage1D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64006f9cec7e5fd2f3ca6f860249e579b16dbf10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988887"
---
# <a name="glcopytexsubimage1d-function"></a><span data-ttu-id="edae0-104">Функция glCopyTexSubImage1D</span><span class="sxs-lookup"><span data-stu-id="edae0-104">glCopyTexSubImage1D function</span></span>

<span data-ttu-id="edae0-105">Функция **glCopyTexSubImage1D** копирует подизображение одномерного изображения текстуры из буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="edae0-105">The **glCopyTexSubImage1D** function copies a sub-image of a one-dimensional texture image from the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="edae0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="edae0-106">Syntax</span></span>


```C++
void WINAPI glCopyTexSubImage1D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   x,
   GLint   y,
   GLsizei width
);
```



## <a name="parameters"></a><span data-ttu-id="edae0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="edae0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edae0-108">*target*</span><span class="sxs-lookup"><span data-stu-id="edae0-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="edae0-109">Целевой объект, в который будут изменяться данные изображения.</span><span class="sxs-lookup"><span data-stu-id="edae0-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="edae0-110">Должно иметь значение GL \_ текстура \_ 1d.</span><span class="sxs-lookup"><span data-stu-id="edae0-110">Must have the value GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="edae0-111">*level*</span><span class="sxs-lookup"><span data-stu-id="edae0-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="edae0-112">Номер уровня детализации.</span><span class="sxs-lookup"><span data-stu-id="edae0-112">The level-of-detail number.</span></span> <span data-ttu-id="edae0-113">Уровень 0 — базовый образ.</span><span class="sxs-lookup"><span data-stu-id="edae0-113">Level 0 is the base image.</span></span> <span data-ttu-id="edae0-114">Уровень *n* — это *n*-ое изображение для сокращения mipmap.</span><span class="sxs-lookup"><span data-stu-id="edae0-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="edae0-115">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="edae0-115">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="edae0-116">Смещение шаг текселя в пределах массива текстуры.</span><span class="sxs-lookup"><span data-stu-id="edae0-116">The texel offset within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="edae0-117">*x*</span><span class="sxs-lookup"><span data-stu-id="edae0-117">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="edae0-118">Координата x окна в левом нижнем углу строки пикселей для копирования.</span><span class="sxs-lookup"><span data-stu-id="edae0-118">The window x-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="edae0-119">*y*</span><span class="sxs-lookup"><span data-stu-id="edae0-119">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="edae0-120">Координата точки y окна для копирования левого нижнего угла строки пикселей.</span><span class="sxs-lookup"><span data-stu-id="edae0-120">The window y-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="edae0-121">*width*</span><span class="sxs-lookup"><span data-stu-id="edae0-121">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="edae0-122">Ширина подобраза изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="edae0-122">The width of the sub-image of the texture image.</span></span> <span data-ttu-id="edae0-123">Указание подобраза текстуры с нулевой шириной не оказывает влияния.</span><span class="sxs-lookup"><span data-stu-id="edae0-123">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edae0-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="edae0-124">Return value</span></span>

<span data-ttu-id="edae0-125">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="edae0-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="edae0-126">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="edae0-126">Error codes</span></span>

<span data-ttu-id="edae0-127">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="edae0-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="edae0-128">Имя</span><span class="sxs-lookup"><span data-stu-id="edae0-128">Name</span></span>                                                                                                  | <span data-ttu-id="edae0-129">Значение</span><span class="sxs-lookup"><span data-stu-id="edae0-129">Meaning</span></span>                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="edae0-130"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="edae0-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="edae0-131">значение *цели* не было принято.</span><span class="sxs-lookup"><span data-stu-id="edae0-131">*target* was not an accepted value.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="edae0-132"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="edae0-132"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="edae0-133">*уровень* меньше нуля или *уровня* больше, чем *log* 2 (*Max*), где *Max* — это возвращаемое значение для \_ максимального \_ размера текстуры GL \_ .</span><span class="sxs-lookup"><span data-stu-id="edae0-133">*level* was less than zero or *level* is greater than *log* 2(*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="edae0-134"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="edae0-134"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="edae0-135">*ксоффсет* меньше *границы* или (  +  *Ширина* ксоффсет) больше (*w*  +  *border*), где *w* — толщина текстуры GL, \_ \_ а *граница* — это \_ граница текстуры GL \_ .</span><span class="sxs-lookup"><span data-stu-id="edae0-135">*xoffset* was less than *border* or (*xoffset* + *width*)was greater than (*w* + *border*), where *w* is GL\_TEXTURE\_WIDTH and *border* is GL\_TEXTURE\_BORDER.</span></span> <span data-ttu-id="edae0-136">Обратите внимание, что *w* включает в себя вдвое ширину *границы* .</span><span class="sxs-lookup"><span data-stu-id="edae0-136">Note that *w* includes twice the *border* width.</span></span><br/> |
| <dl> <span data-ttu-id="edae0-137"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="edae0-137"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="edae0-138">*Ширина* меньше *границы* или *y* меньше *границы*, где *border* является шириной границы для массива текстуры.</span><span class="sxs-lookup"><span data-stu-id="edae0-138">*width* was less than *border* or *y* was less than *border*, where *border* is the border width of the texture array.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="edae0-139"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="edae0-139"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="edae0-140">Массив текстуры не был определен предыдущей операцией [**glTexImage1D**](glteximage1d.md) .</span><span class="sxs-lookup"><span data-stu-id="edae0-140">The texture array was not defined by a previous [**glTexImage1D**](glteximage1d.md) operation.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="edae0-141"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="edae0-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="edae0-142">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="edae0-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                        |



## <a name="remarks"></a><span data-ttu-id="edae0-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="edae0-143">Remarks</span></span>

<span data-ttu-id="edae0-144">Функция **glCopyTexSubImage1D** заменяет часть одномерного изображения текстуры, используя Пиксели из текущего буфера кадров, а не из основной памяти, как в случае с [**glTexSubImage1D**](gltexsubimage1d.md).</span><span class="sxs-lookup"><span data-stu-id="edae0-144">The **glCopyTexSubImage1D** function replaces a portion of a one-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexSubImage1D**](gltexsubimage1d.md).</span></span>

<span data-ttu-id="edae0-145">Строка пикселей, начиная с координат окна, заданных *x* и *y* и с *шириной* , заменяет часть массива текстуры индексами, *ксоффсет* через *ксоффсет* + (*Width* -1).</span><span class="sxs-lookup"><span data-stu-id="edae0-145">A row of pixels beginning with the window coordinates specified by *x* and *y* and with the length *width* replaces the portion of the texture array with the indexes *xoffset* through *xoffset* + (*width* - 1).</span></span> <span data-ttu-id="edae0-146">Назначение в массиве текстуры не может включать пикселей текстуры за пределами изначально заданного массива текстуры.</span><span class="sxs-lookup"><span data-stu-id="edae0-146">The destination in the texture array cannot include any texels outside the originally specified texture array.</span></span>

<span data-ttu-id="edae0-147">Функция **glCopyTexSubImage1D** обрабатывает Пиксели в строке таким же образом, как и [**глкопипикселс**](glcopypixels.md) , за исключением того, что перед завершающим преобразованием пикселов все значения компонентов пикселов записываются в диапазон \[ 0, 1 \] и преобразуются в внутренний формат текстуры для хранения в массиве текстуры.</span><span class="sxs-lookup"><span data-stu-id="edae0-147">The **glCopyTexSubImage1D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md) except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="edae0-148">Порядок пикселей определяется с помощью более низких координат *x* , соответствующих более низким координатам текстуры.</span><span class="sxs-lookup"><span data-stu-id="edae0-148">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="edae0-149">Если любой из пикселов в заданной строке текущего буфера кадров находится за пределами окна, связанного с текущим контекстом отрисовки, то их значения не определены.</span><span class="sxs-lookup"><span data-stu-id="edae0-149">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="edae0-150">В параметре *интерналформат*, *Width* или *border* указанного массива текстуры не вносятся изменения или значения шаг текселя за пределами указанного подизображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="edae0-150">No change is made to the *internalFormat*, *width*, or *border* parameter of the specified texture array or to texel values outside the specified texture sub-image.</span></span>

<span data-ttu-id="edae0-151">В списки вывода нельзя включать вызовы **glCopyTexSubImage1D** .</span><span class="sxs-lookup"><span data-stu-id="edae0-151">You cannot include calls to **glCopyTexSubImage1D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="edae0-152">Функция **glCopyTexSubImage1D** доступна только в OpenGL версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="edae0-152">The **glCopyTexSubImage1D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="edae0-153">Текстурирование не влияет на режим индексирования цветов.</span><span class="sxs-lookup"><span data-stu-id="edae0-153">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="edae0-154">Функции [**глпикселсторе**](glpixelstore-functions.md) и [**глпикселтрансфер**](glpixeltransfer.md) влияют на изображения текстур точно так же, как они влияют на способ прорисовки пикселов с помощью [**глдравпикселс**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="edae0-154">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect the way pixels are drawn using [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="edae0-155">Следующие функции извлекают сведения, относящиеся к **glCopyTexSubImage1D**:</span><span class="sxs-lookup"><span data-stu-id="edae0-155">The following functions retrieve information related to **glCopyTexSubImage1D**:</span></span>

[<span data-ttu-id="edae0-156">**глжеттексимаже**</span><span class="sxs-lookup"><span data-stu-id="edae0-156">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="edae0-157">[**глисенаблед**](glisenabled.md) с аргументом GL \_ текстура \_ 1d</span><span class="sxs-lookup"><span data-stu-id="edae0-157">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="edae0-158">Требования</span><span class="sxs-lookup"><span data-stu-id="edae0-158">Requirements</span></span>



| <span data-ttu-id="edae0-159">Требование</span><span class="sxs-lookup"><span data-stu-id="edae0-159">Requirement</span></span> | <span data-ttu-id="edae0-160">Значение</span><span class="sxs-lookup"><span data-stu-id="edae0-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="edae0-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="edae0-161">Minimum supported client</span></span><br/> | <span data-ttu-id="edae0-162">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="edae0-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="edae0-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="edae0-163">Minimum supported server</span></span><br/> | <span data-ttu-id="edae0-164">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="edae0-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="edae0-165">Заголовок</span><span class="sxs-lookup"><span data-stu-id="edae0-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="edae0-166"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="edae0-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="edae0-167">Библиотека</span><span class="sxs-lookup"><span data-stu-id="edae0-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="edae0-168"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="edae0-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="edae0-169">DLL</span><span class="sxs-lookup"><span data-stu-id="edae0-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edae0-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edae0-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edae0-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="edae0-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edae0-172">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="edae0-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="edae0-173">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="edae0-173">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="edae0-174">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="edae0-174">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="edae0-175">**гленд**</span><span class="sxs-lookup"><span data-stu-id="edae0-175">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="edae0-176">**глфог**</span><span class="sxs-lookup"><span data-stu-id="edae0-176">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="edae0-177">**глпикселсторе**</span><span class="sxs-lookup"><span data-stu-id="edae0-177">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="edae0-178">**глпикселтрансфер**</span><span class="sxs-lookup"><span data-stu-id="edae0-178">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="edae0-179">**глтексенв**</span><span class="sxs-lookup"><span data-stu-id="edae0-179">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="edae0-180">**глтексжен**</span><span class="sxs-lookup"><span data-stu-id="edae0-180">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="edae0-181">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="edae0-181">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="edae0-182">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="edae0-182">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="edae0-183">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="edae0-183">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="edae0-184">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="edae0-184">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="edae0-185">**глтекспараметер**</span><span class="sxs-lookup"><span data-stu-id="edae0-185">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





