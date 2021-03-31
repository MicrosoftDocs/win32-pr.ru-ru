---
title: Функция Глбитмап (GL. h)
description: Функция Глбитмап рисует растровое изображение.
ms.assetid: 3cd8e41b-016b-4610-833a-048b5e50ae7c
keywords:
- Функция Глбитмап OpenGL
topic_type:
- apiref
api_name:
- glBitmap
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb97bb16a1e3c4c29d1dfb1a5320c02f44404d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071730"
---
# <a name="glbitmap-function"></a><span data-ttu-id="b9280-104">Функция Глбитмап</span><span class="sxs-lookup"><span data-stu-id="b9280-104">glBitmap function</span></span>

<span data-ttu-id="b9280-105">Функция **глбитмап** рисует растровое изображение.</span><span class="sxs-lookup"><span data-stu-id="b9280-105">The **glBitmap** function draws a bitmap.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9280-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9280-106">Syntax</span></span>


```C++
void WINAPI glBitmap(
         GLSizei width,
         GLSizei height,
         GLfloat xorig,
         GLfloat yorig,
         GLfloat xmove,
         GLfloat ymove,
   const GLubyte *bitmap
);
```



## <a name="parameters"></a><span data-ttu-id="b9280-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9280-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9280-108">*width*</span><span class="sxs-lookup"><span data-stu-id="b9280-108">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="b9280-109">Ширина точечного изображения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b9280-109">The pixel width of the bitmap image.</span></span>

</dd> <dt>

<span data-ttu-id="b9280-110">*height*</span><span class="sxs-lookup"><span data-stu-id="b9280-110">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="b9280-111">Высота точечного рисунка в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b9280-111">The pixel height of the bitmap image.</span></span>

</dd> <dt>

<span data-ttu-id="b9280-112">*ксориг*</span><span class="sxs-lookup"><span data-stu-id="b9280-112">*xorig*</span></span> 
</dt> <dd>

<span data-ttu-id="b9280-113">Расположение *x* источника в битовом изображении.</span><span class="sxs-lookup"><span data-stu-id="b9280-113">The *x* location of the origin in the bitmap image.</span></span> <span data-ttu-id="b9280-114">Источник измеряется от левого нижнего угла растрового изображения, а в направлениях справа и вверх — положительные оси.</span><span class="sxs-lookup"><span data-stu-id="b9280-114">The origin is measured from the lower-left corner of the bitmap, with right and up directions being the positive axes.</span></span>

</dd> <dt>

<span data-ttu-id="b9280-115">*йориг*</span><span class="sxs-lookup"><span data-stu-id="b9280-115">*yorig*</span></span> 
</dt> <dd>

<span data-ttu-id="b9280-116">Расположение *координаты y* источника в растровом изображении.</span><span class="sxs-lookup"><span data-stu-id="b9280-116">The *y* location of the origin in the bitmap image.</span></span> <span data-ttu-id="b9280-117">Источник измеряется от левого нижнего угла растрового изображения, а в направлениях справа и вверх — положительные оси.</span><span class="sxs-lookup"><span data-stu-id="b9280-117">The origin is measured from the lower-left corner of the bitmap, with right and up directions being the positive axes.</span></span>

</dd> <dt>

<span data-ttu-id="b9280-118">*ксмове*</span><span class="sxs-lookup"><span data-stu-id="b9280-118">*xmove*</span></span> 
</dt> <dd>

<span data-ttu-id="b9280-119">Смещение *x* , добавляемое в текущую растровую точку после прорисовки растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="b9280-119">The *x* offset to be added to the current raster position after the bitmap is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="b9280-120">*имове*</span><span class="sxs-lookup"><span data-stu-id="b9280-120">*ymove*</span></span> 
</dt> <dd>

<span data-ttu-id="b9280-121">Смещение *y* , добавляемое в текущую растровую точку после прорисовки растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="b9280-121">The *y* offset to be added to the current raster position after the bitmap is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="b9280-122">*bitmap*</span><span class="sxs-lookup"><span data-stu-id="b9280-122">*bitmap*</span></span> 
</dt> <dd>

<span data-ttu-id="b9280-123">Адрес растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="b9280-123">The address of the bitmap image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9280-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9280-124">Return value</span></span>

<span data-ttu-id="b9280-125">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b9280-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b9280-126">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b9280-126">Error codes</span></span>

<span data-ttu-id="b9280-127">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="b9280-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b9280-128">Имя</span><span class="sxs-lookup"><span data-stu-id="b9280-128">Name</span></span>                                                                                                  | <span data-ttu-id="b9280-129">Значение</span><span class="sxs-lookup"><span data-stu-id="b9280-129">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b9280-130"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b9280-130"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="b9280-131">*Ширина* или *Высота* отрицательны.</span><span class="sxs-lookup"><span data-stu-id="b9280-131">*width* or *height* is negative.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="b9280-132"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b9280-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b9280-133">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b9280-133">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b9280-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b9280-134">Remarks</span></span>

<span data-ttu-id="b9280-135">Точечный рисунок представляет собой двоичное изображение.</span><span class="sxs-lookup"><span data-stu-id="b9280-135">A bitmap is a binary image.</span></span> <span data-ttu-id="b9280-136">При рисовании точечный рисунок располагается относительно текущей позиции растрового изображения, а буфера кадров Пиксели, соответствующие 1 в точечном рисунке, записываются с использованием текущего растрового цвета или индекса.</span><span class="sxs-lookup"><span data-stu-id="b9280-136">When drawn, the bitmap is positioned relative to the current raster position, and framebuffer pixels corresponding to 1s in the bitmap are written using the current raster color or index.</span></span> <span data-ttu-id="b9280-137">Буферы кадров, соответствующие нулевым значениям в точечном рисунке, не изменяются.</span><span class="sxs-lookup"><span data-stu-id="b9280-137">Frame-buffer pixels corresponding to zeros in the bitmap are not modified.</span></span>

<span data-ttu-id="b9280-138">Растровое изображение интерпретируется как данные изображения для функции [**глдравпикселс**](gldrawpixels.md) с *шириной* и *высотой* , соответствующим аргументам Width и Height этой функции, а также с *типом* , для которого задано \_ битовое изображение и *Формат* GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b9280-138">The bitmap image is interpreted like image data for the [**glDrawPixels**](gldrawpixels.md) function, with *width* and *height* corresponding to the width and height arguments of that function, and with *type* set to GL\_BITMAP and *format* set to GL\_COLOR\_INDEX.</span></span> <span data-ttu-id="b9280-139">Режимы, заданные с помощью [**глпикселсторе**](glpixelstore-functions.md) , влияют на интерпретацию данных растрового изображения. режимы, указываемые с помощью [**глпикселтрансфер**](glpixeltransfer.md) , не имеют.</span><span class="sxs-lookup"><span data-stu-id="b9280-139">Modes you specify using [**glPixelStore**](glpixelstore-functions.md) affect the interpretation of bitmap image data; modes you specify using [**glPixelTransfer**](glpixeltransfer.md) do not.</span></span>

<span data-ttu-id="b9280-140">Если текущая растровая размещается в недопустимом положении, **глбитмап** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b9280-140">If the current raster position is invalid, **glBitmap** is ignored.</span></span> <span data-ttu-id="b9280-141">В противном случае нижний левый угол растрового изображения располагается в следующих координатах окна:</span><span class="sxs-lookup"><span data-stu-id="b9280-141">Otherwise, the lower-left corner of the bitmap image is positioned at the following window coordinates:</span></span>

<span data-ttu-id="b9280-142">*x*<sub>w</sub>  =  *x*<sub>r</sub> *x*?</span><span class="sxs-lookup"><span data-stu-id="b9280-142">*x*<sub>w</sub> = *x*<sub>r</sub> *x*?</span></span>

<span data-ttu-id="b9280-143">*y*<sub>ч</sub>  =  *y*<sub>r</sub> ?</span><span class="sxs-lookup"><span data-stu-id="b9280-143">*y*<sub>w</sub> = *y*<sub>r</sub> *y*?</span></span>

<span data-ttu-id="b9280-144">В этих координатах (*x*<sub>r</sub> , *y*<sub>r</sub> ) является точечной позицией и (*x*?</span><span class="sxs-lookup"><span data-stu-id="b9280-144">In these coordinates, (*x*<sub>r</sub> , *y*<sub>r</sub> ) is the raster position, and (*x*?</span></span> <span data-ttu-id="b9280-145">, *Да*?</span><span class="sxs-lookup"><span data-stu-id="b9280-145">, *y*?</span></span> <span data-ttu-id="b9280-146">) — это источник точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="b9280-146">) is the bitmap origin.</span></span> <span data-ttu-id="b9280-147">Затем создаются фрагменты для каждого пикселя, соответствующего 1 в растровом изображении.</span><span class="sxs-lookup"><span data-stu-id="b9280-147">Fragments are then generated for each pixel corresponding to a 1 in the bitmap image.</span></span> <span data-ttu-id="b9280-148">Эти фрагменты создаются с использованием текущей растровой координаты *z*, цвета или цвета, а также текущих координат текстурной текстуры.</span><span class="sxs-lookup"><span data-stu-id="b9280-148">These fragments are generated using the current raster *z*-coordinate, color or color index, and current raster texture coordinates.</span></span> <span data-ttu-id="b9280-149">Затем они обрабатываются так же, как если бы они были созданы точкой, линией или многоугольником, включая сопоставление текстур, фоггинг и все операции с фрагментами, например альфа-и глубинный тест.</span><span class="sxs-lookup"><span data-stu-id="b9280-149">They are then treated just as if they had been generated by a point, line, or polygon, including texture mapping, fogging, and all per-fragment operations such as alpha and depth testing.</span></span>

<span data-ttu-id="b9280-150">После прорисовки растрового изображения координаты *x* и *y* текущей позиции в виде смещения смещаются на *ксмове* и *имове*.</span><span class="sxs-lookup"><span data-stu-id="b9280-150">After the bitmap has been drawn, the *x* and *y* coordinates of the current raster position are offset by *xmove* and *ymove*.</span></span> <span data-ttu-id="b9280-151">В *z*-координате текущей позиции оттенок не вносится никаких изменений, а также для текущего растрового цвета, индекса или координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="b9280-151">No change is made to the *z*-coordinate of the current raster position, or to the current raster color, index, or texture coordinates.</span></span>

<span data-ttu-id="b9280-152">Следующие функции извлекают сведения, относящиеся к функции **глбитмап** :</span><span class="sxs-lookup"><span data-stu-id="b9280-152">The following functions retrieve information related to the **glBitmap** function:</span></span>

<span data-ttu-id="b9280-153">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ текущей \_ точечной \_ позицией GL</span><span class="sxs-lookup"><span data-stu-id="b9280-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>

 

<span data-ttu-id="b9280-154">**глжет** с аргументом \_ текущий \_ растровый \_ Цвет GL</span><span class="sxs-lookup"><span data-stu-id="b9280-154">**glGet** with argument GL\_CURRENT\_RASTER\_COLOR</span></span>

 

<span data-ttu-id="b9280-155">**глжет** с аргументом GL \_ текущий \_ растровый \_ индекс</span><span class="sxs-lookup"><span data-stu-id="b9280-155">**glGet** with argument GL\_CURRENT\_RASTER\_INDEX</span></span>

 

<span data-ttu-id="b9280-156">**глжет** с аргументом GL \_ Текущая \_ растровая \_ текстура \_</span><span class="sxs-lookup"><span data-stu-id="b9280-156">**glGet** with argument GL\_CURRENT\_RASTER\_TEXTURE\_COORDS</span></span>

 

<span data-ttu-id="b9280-157">**глжет** с аргументом \_ текущей \_ точечной \_ позицией GL \_ допустимо</span><span class="sxs-lookup"><span data-stu-id="b9280-157">**glGet** with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>

## <a name="requirements"></a><span data-ttu-id="b9280-158">Требования</span><span class="sxs-lookup"><span data-stu-id="b9280-158">Requirements</span></span>



| <span data-ttu-id="b9280-159">Требование</span><span class="sxs-lookup"><span data-stu-id="b9280-159">Requirement</span></span> | <span data-ttu-id="b9280-160">Значение</span><span class="sxs-lookup"><span data-stu-id="b9280-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9280-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b9280-161">Minimum supported client</span></span><br/> | <span data-ttu-id="b9280-162">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b9280-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b9280-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b9280-163">Minimum supported server</span></span><br/> | <span data-ttu-id="b9280-164">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b9280-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b9280-165">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b9280-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9280-166"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9280-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b9280-167">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b9280-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9280-168"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9280-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b9280-169">DLL</span><span class="sxs-lookup"><span data-stu-id="b9280-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9280-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9280-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9280-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9280-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9280-172">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="b9280-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b9280-173">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="b9280-173">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="b9280-174">**гленд**</span><span class="sxs-lookup"><span data-stu-id="b9280-174">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b9280-175">**глпикселсторе**</span><span class="sxs-lookup"><span data-stu-id="b9280-175">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="b9280-176">**глпикселтрансфер**</span><span class="sxs-lookup"><span data-stu-id="b9280-176">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="b9280-177">**глрастерпос**</span><span class="sxs-lookup"><span data-stu-id="b9280-177">**glRasterPos**</span></span>](glrasterpos-functions.md)
</dt> </dl>

 

 





