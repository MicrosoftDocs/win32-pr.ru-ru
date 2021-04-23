---
title: Функция Глжетколортабликст (GL. h)
description: Функция Глжетколортабликст получает данные цветовой таблицы для текущей целевой палитры текстуры.
ms.assetid: 9169c4e1-a22e-48fe-bd45-4549c1a10ff0
keywords:
- Функция Глжетколортабликст OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811dc53b32c937970fbef8d87fa9a2ef4eb8b978
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682156"
---
# <a name="glgetcolortableext-function"></a><span data-ttu-id="34c38-104">Функция Глжетколортабликст</span><span class="sxs-lookup"><span data-stu-id="34c38-104">glGetColorTableEXT function</span></span>

<span data-ttu-id="34c38-105">Функция **глжетколортабликст** получает данные цветовой таблицы для текущей целевой палитры текстуры.</span><span class="sxs-lookup"><span data-stu-id="34c38-105">The **glGetColorTableEXT** function gets the color table data of the current targeted texture palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="34c38-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34c38-106">Syntax</span></span>


```C++
void WINAPI glGetColorTableEXT(
         GLenum target,
         GLenum format,
         GLenum type,
   const GLvoid *data
);
```



## <a name="parameters"></a><span data-ttu-id="34c38-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="34c38-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34c38-108">*target*</span><span class="sxs-lookup"><span data-stu-id="34c38-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="34c38-109">Целевая текстура, для которой изменилась палитра.</span><span class="sxs-lookup"><span data-stu-id="34c38-109">The target texture that is to have its palette changed.</span></span> <span data-ttu-id="34c38-110">Должен быть ТЕКСТУРой \_ 1d или 2D-текстурой \_ .</span><span class="sxs-lookup"><span data-stu-id="34c38-110">Must be TEXTURE\_1D or TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="34c38-111">*format*</span><span class="sxs-lookup"><span data-stu-id="34c38-111">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="34c38-112">Формат точечных данных.</span><span class="sxs-lookup"><span data-stu-id="34c38-112">The format of the pixel data.</span></span> <span data-ttu-id="34c38-113">Допустимы следующие символьные константы.</span><span class="sxs-lookup"><span data-stu-id="34c38-113">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34c38-114">Значение</span><span class="sxs-lookup"><span data-stu-id="34c38-114">Value</span></span></th>
<th><span data-ttu-id="34c38-115">Значение</span><span class="sxs-lookup"><span data-stu-id="34c38-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="34c38-116"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="34c38-116"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="34c38-117">Каждый пиксель — это группа из четырех компонентов в следующем порядке: красный, зеленый, синий, альфа.</span><span class="sxs-lookup"><span data-stu-id="34c38-117">Each pixel is a group of four components in the following order: red, green, blue, alpha.</span></span> <span data-ttu-id="34c38-118">Формат RGBA определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="34c38-118">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="34c38-119">Функция <strong>глжетколортабликст</strong> преобразует значения с плавающей запятой непосредственно во внутренний формат с неуказанной точностью.</span><span class="sxs-lookup"><span data-stu-id="34c38-119">The <strong>glGetColorTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="34c38-120">Целочисленные значения со знаком сопоставляются по внутреннему формату, так что наиболее положительное целочисленное значение, которое можно отобразить, сопоставляется с 1,0, а наиболее отрицательное целочисленное значение — в-1,0.</span><span class="sxs-lookup"><span data-stu-id="34c38-120">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable integer value maps to -1.0.</span></span> <span data-ttu-id="34c38-121">Целочисленные данные без знака сопоставлены аналогичным образом: максимальное целочисленное значение сопоставляется с 1,0, а нулевое сопоставляется с 0,0.</span><span class="sxs-lookup"><span data-stu-id="34c38-121">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="34c38-122">Функция <strong>глжетколортабликст</strong> умножает результирующие значения цвета на GL_c_SCALE и добавляет их в GL_c_BIAS, где <em>c</em> — красный, зеленый, синий и альфа-канал для соответствующих компонентов цвета.</span><span class="sxs-lookup"><span data-stu-id="34c38-122">The <strong>glGetColorTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="34c38-123">Результаты записываются в диапазон [0, 1].</span><span class="sxs-lookup"><span data-stu-id="34c38-123">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="34c38-124">Если GL_MAP_COLOR имеет <strong>значение true</strong>, <strong>глжетколортабликст</strong> масштабирует каждый компонент цвета по размеру таблицы подстановки GL_PIXEL_MAP_c_TO_c, а затем заменяет компонент на значение, на которое он ссылается в этой таблице. <em>c</em> — R, G, B или A соответственно.</span><span class="sxs-lookup"><span data-stu-id="34c38-124">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glGetColorTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="34c38-125">Функция <strong>глжетколортабликст</strong> преобразует итоговые цвета RGBA в фрагменты, присоединяя текущую координату z-координаты и координаты текстуры к каждому пикселю, а затем присвоив координаты <em>x</em> и <em>y</em> для <em>n</em>-го фрагмента, такого как <em>x</em>?</span><span class="sxs-lookup"><span data-stu-id="34c38-125">The <strong>glGetColorTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position z-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment, such that <em>x</em>?</span></span><span data-ttu-id="34c38-126"> = <em>Ширина</em> <em>x</em><sub>r</sub> + <em>n</em></span><span class="sxs-lookup"><span data-stu-id="34c38-126"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="34c38-127"><em>Да</em>?</span><span class="sxs-lookup"><span data-stu-id="34c38-127"><em>y</em>?</span></span><span data-ttu-id="34c38-128"> = <em>y</em><sub></sub> + <em>n/Ширина</em></span><span class="sxs-lookup"><span data-stu-id="34c38-128"> = <em>y</em><sub>r</sub> + <em>n/width</em></span></span><br/> <span data-ttu-id="34c38-129">где (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) — Текущая разточечная координата.</span><span class="sxs-lookup"><span data-stu-id="34c38-129">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="34c38-130">Затем эти фрагменты пикселов обрабатываются так же, как фрагменты, созданные с помощью растровых точек, линий или многоугольников.</span><span class="sxs-lookup"><span data-stu-id="34c38-130">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="34c38-131">Функция <strong>глжетколортабликст</strong> применяет сопоставление текстур, туман и все операции фрагментов перед записью фрагментов в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="34c38-131">The <strong>glGetColorTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="34c38-132"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="34c38-132"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="34c38-133">Каждый пиксель является одним красным компонентом.</span><span class="sxs-lookup"><span data-stu-id="34c38-133">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="34c38-134">Функция <strong>глжетколортабликст</strong> преобразует этот компонент во внутренний формат точно так же, как красный компонент в пикселе RGBA, а затем преобразует его в пиксель RGBA с зеленым и синим значением 0,0, а альфа-канал — в значение 1,0.</span><span class="sxs-lookup"><span data-stu-id="34c38-134">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="34c38-135">После этого преобразования пиксел обрабатывается так же, как если бы он был считан как пиксель RGBA.</span><span class="sxs-lookup"><span data-stu-id="34c38-135">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="34c38-136"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="34c38-136"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="34c38-137">Каждый пиксель является одним зеленым компонентом.</span><span class="sxs-lookup"><span data-stu-id="34c38-137">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="34c38-138">Функция <strong>глжетколортабликст</strong> преобразует этот компонент во внутренний формат таким же образом, как и зеленый компонент в пиксельном виде, а затем преобразует его в пиксель RGBA с красным и синим значением в 0,0, а альфа-канал — в значение 1,0.</span><span class="sxs-lookup"><span data-stu-id="34c38-138">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="34c38-139">После этого преобразования пиксел обрабатывается так же, как если бы он был считан как пиксель RGBA.</span><span class="sxs-lookup"><span data-stu-id="34c38-139">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="34c38-140"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="34c38-140"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="34c38-141">Каждый пиксель является одним синим компонентом.</span><span class="sxs-lookup"><span data-stu-id="34c38-141">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="34c38-142">Функция <strong>глжетколортабликст</strong> преобразует этот компонент во внутренний формат точно таким же образом, как и синий компонент в пикселе RGBA, а затем преобразует его в пиксель RGBA с красным и зеленым значением, равным 0,0, а альфа-канал — 1,0.</span><span class="sxs-lookup"><span data-stu-id="34c38-142">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="34c38-143">После этого преобразования пиксел обрабатывается так же, как если бы он был считан как пиксель RGBA.</span><span class="sxs-lookup"><span data-stu-id="34c38-143">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="34c38-144"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="34c38-144"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="34c38-145">Каждый пиксель является одним компонентом альфа.</span><span class="sxs-lookup"><span data-stu-id="34c38-145">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="34c38-146">Функция <strong>глжетколортабликст</strong> преобразует этот компонент во внутренний формат точно так же, как альфа-компонент в пиксельном пикселе RGBA, а затем преобразует его в пиксель RGBA с красным, зеленым и синим установленным значением 0,0.</span><span class="sxs-lookup"><span data-stu-id="34c38-146">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="34c38-147">После этого преобразования пиксел обрабатывается так же, как если бы он был считан как пиксель RGBA.</span><span class="sxs-lookup"><span data-stu-id="34c38-147">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="34c38-148"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="34c38-148"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="34c38-149">Каждый пиксель — это группа из трех компонентов в следующем порядке: красный, зеленый, синий.</span><span class="sxs-lookup"><span data-stu-id="34c38-149">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="34c38-150">Функция <strong>глжетколортабликст</strong> преобразует каждый компонент во внутренний формат точно так же, как красный, зеленый и синий компоненты на пиксель RGBA.</span><span class="sxs-lookup"><span data-stu-id="34c38-150">The <strong>glGetColorTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="34c38-151">Тройной цвет преобразуется в пиксель RGBA с альфа-составляющей, равным 1,0.</span><span class="sxs-lookup"><span data-stu-id="34c38-151">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="34c38-152">После этого преобразования пиксел обрабатывается так же, как если бы он был считан как пиксель RGBA.</span><span class="sxs-lookup"><span data-stu-id="34c38-152">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="34c38-153"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="34c38-153"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="34c38-154">Каждый пиксель — это группа из трех компонентов в следующем порядке: синий, зеленый, красный.</span><span class="sxs-lookup"><span data-stu-id="34c38-154">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="34c38-155">GL_BGR_EXT предоставляет формат, соответствующий макету памяти для изображений, не зависящих от устройства Microsoft Windows (DIB).</span><span class="sxs-lookup"><span data-stu-id="34c38-155">GL_BGR_EXT provides a format that matches the memory layout of Microsoft Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="34c38-156">Таким же приложениям можно использовать те же данные, что и вызовы функций Windows, и вызовы функций OpenGL Pixel.</span><span class="sxs-lookup"><span data-stu-id="34c38-156">Thus, your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="34c38-157"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="34c38-157"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="34c38-158">Каждый пиксель — это группа из четырех компонентов в следующем порядке: синий, зеленый, красный, альфа.</span><span class="sxs-lookup"><span data-stu-id="34c38-158">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="34c38-159">GL_BGRA_EXT предоставляет формат, соответствующий макету памяти, не зависящему от устройства Windows (DIB).</span><span class="sxs-lookup"><span data-stu-id="34c38-159">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="34c38-160">Поэтому приложения могут использовать те же данные, что и вызовы функций Windows, и вызовы функций OpenGL Pixel.</span><span class="sxs-lookup"><span data-stu-id="34c38-160">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="34c38-161">*type*</span><span class="sxs-lookup"><span data-stu-id="34c38-161">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="34c38-162">Тип данных для *данных*.</span><span class="sxs-lookup"><span data-stu-id="34c38-162">The data type for *data*.</span></span> <span data-ttu-id="34c38-163">Ниже приведены допустимые символьные константы и их значения.</span><span class="sxs-lookup"><span data-stu-id="34c38-163">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="34c38-164">Значение</span><span class="sxs-lookup"><span data-stu-id="34c38-164">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="34c38-165">Значение</span><span class="sxs-lookup"><span data-stu-id="34c38-165">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="34c38-166"><dt>**\_байт без знака GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34c38-166"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="34c38-167">8-разрядное целое число без знака</span><span class="sxs-lookup"><span data-stu-id="34c38-167">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="34c38-168"><dt>**\_байт GL**</dt></span><span class="sxs-lookup"><span data-stu-id="34c38-168"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="34c38-169">8-разрядное целое число со знаком</span><span class="sxs-lookup"><span data-stu-id="34c38-169">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="34c38-170"><dt>**\_ \_ сокращенный формат GL без знака**</dt></span><span class="sxs-lookup"><span data-stu-id="34c38-170"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="34c38-171">16-разрядное целое число без знака</span><span class="sxs-lookup"><span data-stu-id="34c38-171">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="34c38-172"><dt>**\_Краткая GL**</dt></span><span class="sxs-lookup"><span data-stu-id="34c38-172"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="34c38-173">16-разрядное целое число со знаком</span><span class="sxs-lookup"><span data-stu-id="34c38-173">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="34c38-174"><dt>**\_целое число без знака GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34c38-174"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="34c38-175">32-разрядное целое число без знака</span><span class="sxs-lookup"><span data-stu-id="34c38-175">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="34c38-176"><dt>**тип в GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34c38-176"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="34c38-177">32-разрядное целое число</span><span class="sxs-lookup"><span data-stu-id="34c38-177">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="34c38-178"><dt>**с \_ плавающей запятой**</dt></span><span class="sxs-lookup"><span data-stu-id="34c38-178"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="34c38-179">Число одинарной точности с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="34c38-179">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="34c38-180">*data*</span><span class="sxs-lookup"><span data-stu-id="34c38-180">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="34c38-181">Указывает расположение, куда должны храниться данные таблицы цветов.</span><span class="sxs-lookup"><span data-stu-id="34c38-181">Points to the location where returned color table information is to be stored.</span></span> <span data-ttu-id="34c38-182">Каждая запись цветовой таблицы сохраняется так, как если бы она была единственной точкой одномерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="34c38-182">Each color table entry is stored as if it was a single pixel of a 1-D texture.</span></span> <span data-ttu-id="34c38-183">Так как все текстуры имеют палитру по умолчанию, **глжетколортабликст** всегда возвращает сведения о палитре, даже если данные текстуры не находятся в формате с палитрой.</span><span class="sxs-lookup"><span data-stu-id="34c38-183">Because all textures have a default palette, **glGetColorTableEXT** always returns palette information even if the texture data is not in a paletted format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34c38-184">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34c38-184">Return value</span></span>

<span data-ttu-id="34c38-185">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="34c38-185">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="34c38-186">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="34c38-186">Error codes</span></span>

<span data-ttu-id="34c38-187">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="34c38-187">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="34c38-188">Имя</span><span class="sxs-lookup"><span data-stu-id="34c38-188">Name</span></span>                                                                                                  | <span data-ttu-id="34c38-189">Значение</span><span class="sxs-lookup"><span data-stu-id="34c38-189">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="34c38-190"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="34c38-190"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="34c38-191">*целевой объект*, *Формат* или *тип* не являются допустимыми значениями.</span><span class="sxs-lookup"><span data-stu-id="34c38-191">*target*, *format*, or *type* was not an accepted value.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="34c38-192"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="34c38-192"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="34c38-193">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="34c38-193">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="34c38-194">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34c38-194">Remarks</span></span>

<span data-ttu-id="34c38-195">Функция **глжетколортабликст** возвращает фактические данные таблицы цветов, указанные в [**глколортабликст**](glcolortableext.md) и [**глколорсубтабликст**](glcolorsubtableext.md).</span><span class="sxs-lookup"><span data-stu-id="34c38-195">The **glGetColorTableEXT** function gets the actual color table data specified by [**glColorTableEXT**](glcolortableext.md) and [**glColorSubTableEXT**](glcolorsubtableext.md).</span></span>

<span data-ttu-id="34c38-196">Функция **глжетколортабликст** — это функция расширения, которая не является частью стандартной библиотеки OpenGL, но является частью расширения текстуры с помощью \_ палитры типа "Расш \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="34c38-196">The **glGetColorTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="34c38-197">Чтобы проверить, поддерживает ли ваша реализация OpenGL **глжетколортабликст**, вызовите [**глжетстринг**](glgetstring.md)( \_ расширения GL).</span><span class="sxs-lookup"><span data-stu-id="34c38-197">To check whether your implementation of OpenGL supports **glGetColorTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="34c38-198">Если он возвращает \_ \_ текстуру с Многоцветовой палитрой GL \_ , поддерживается **глжетколортабликст** .</span><span class="sxs-lookup"><span data-stu-id="34c38-198">If it returns GL\_EXT\_paletted\_texture, **glGetColorTableEXT** is supported.</span></span> <span data-ttu-id="34c38-199">Чтобы получить адрес функции расширения, вызовите [**вглжетпрокаддресс**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="34c38-199">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

## <a name="requirements"></a><span data-ttu-id="34c38-200">Требования</span><span class="sxs-lookup"><span data-stu-id="34c38-200">Requirements</span></span>



| <span data-ttu-id="34c38-201">Требование</span><span class="sxs-lookup"><span data-stu-id="34c38-201">Requirement</span></span> | <span data-ttu-id="34c38-202">Значение</span><span class="sxs-lookup"><span data-stu-id="34c38-202">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="34c38-203">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34c38-203">Minimum supported client</span></span><br/> | <span data-ttu-id="34c38-204">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="34c38-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="34c38-205">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34c38-205">Minimum supported server</span></span><br/> | <span data-ttu-id="34c38-206">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="34c38-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="34c38-207">Заголовок</span><span class="sxs-lookup"><span data-stu-id="34c38-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="34c38-208"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="34c38-208"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34c38-209">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34c38-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34c38-210">**глколорсубтабликст**</span><span class="sxs-lookup"><span data-stu-id="34c38-210">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="34c38-211">**глколортабликст**</span><span class="sxs-lookup"><span data-stu-id="34c38-211">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="34c38-212">**глжетколортаблепараметерфвекст**</span><span class="sxs-lookup"><span data-stu-id="34c38-212">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="34c38-213">**глжетколортаблепараметеривекст**</span><span class="sxs-lookup"><span data-stu-id="34c38-213">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="34c38-214">**вглжетпрокаддресс**</span><span class="sxs-lookup"><span data-stu-id="34c38-214">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





