---
title: Функция Глколорсубтабликст (GL. h)
description: Функция Глколорсубтабликст указывает часть палитры целевой текстуры для замены.
ms.assetid: 21430245-f837-4c7a-944f-b44482254b12
keywords:
- Функция Глколорсубтабликст OpenGL
topic_type:
- apiref
api_name:
- glColorSubTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0386bda82bf08ae778d20b1be69858698ac7bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892098"
---
# <a name="glcolorsubtableext-function"></a><span data-ttu-id="26529-104">Функция Глколорсубтабликст</span><span class="sxs-lookup"><span data-stu-id="26529-104">glColorSubTableEXT function</span></span>

<span data-ttu-id="26529-105">Функция **глколорсубтабликст** указывает часть палитры целевой текстуры для замены.</span><span class="sxs-lookup"><span data-stu-id="26529-105">The **glColorSubTableEXT** function specifies a portion of the targeted texture's palette to be replaced.</span></span>

## <a name="syntax"></a><span data-ttu-id="26529-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26529-106">Syntax</span></span>


```C++
void WINAPI glColorSubTableEXT(
         GLenum  target,
         GLsizei start,
         GLsizei count,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a><span data-ttu-id="26529-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="26529-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26529-108">*target*</span><span class="sxs-lookup"><span data-stu-id="26529-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="26529-109">Целевая текстура с палитрой, для которой изменилась палитра.</span><span class="sxs-lookup"><span data-stu-id="26529-109">The target paletted texture that is to have its palette changed.</span></span> <span data-ttu-id="26529-110">Должен быть ТЕКСТУРой \_ 1d или 2D-текстурой \_ .</span><span class="sxs-lookup"><span data-stu-id="26529-110">Must be TEXTURE\_1D or TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="26529-111">*start*</span><span class="sxs-lookup"><span data-stu-id="26529-111">*start*</span></span> 
</dt> <dd>

<span data-ttu-id="26529-112">Начальная запись индекса палитры для изменяемой палитры.</span><span class="sxs-lookup"><span data-stu-id="26529-112">The starting palette index entry of the palette to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="26529-113">*count*</span><span class="sxs-lookup"><span data-stu-id="26529-113">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="26529-114">Число элементов индекса палитры для изменяемой палитры, начиная с *Start*.</span><span class="sxs-lookup"><span data-stu-id="26529-114">The number of palette index entries of the palette to be changed beginning at *start*.</span></span> <span data-ttu-id="26529-115">Параметр *Count* определяет диапазон изменяемых записей в индексе палитры.</span><span class="sxs-lookup"><span data-stu-id="26529-115">The *count* parameter determines the range of palette index entries that are changed.</span></span>

</dd> <dt>

<span data-ttu-id="26529-116">*format*</span><span class="sxs-lookup"><span data-stu-id="26529-116">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="26529-117">Формат точечных данных.</span><span class="sxs-lookup"><span data-stu-id="26529-117">The format of the pixel data.</span></span> <span data-ttu-id="26529-118">Допустимы следующие символьные константы.</span><span class="sxs-lookup"><span data-stu-id="26529-118">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26529-119">Значение</span><span class="sxs-lookup"><span data-stu-id="26529-119">Value</span></span></th>
<th><span data-ttu-id="26529-120">Значение</span><span class="sxs-lookup"><span data-stu-id="26529-120">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="26529-121"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="26529-121"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="26529-122">Каждый пиксель — это группа из четырех компонентов в следующем порядке: красный, зеленый, синий, альфа.</span><span class="sxs-lookup"><span data-stu-id="26529-122">Each pixel is a group of four components in the following order: red, green, blue, alpha.</span></span> <span data-ttu-id="26529-123">Формат RGBA определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="26529-123">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="26529-124">Функция <strong>глколорсубтабликст</strong> преобразует значения с плавающей запятой непосредственно во внутренний формат с неуказанной точностью.</span><span class="sxs-lookup"><span data-stu-id="26529-124">The <strong>glColorSubTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="26529-125">Целочисленные значения со знаком линейно сопоставляются с внутренним форматом таким образом, чтобы наиболее положительное значение целочисленного представления сопоставлялось с 1,0, а наиболее отрицательное значение — в-1,0.</span><span class="sxs-lookup"><span data-stu-id="26529-125">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="26529-126">Целочисленные данные без знака сопоставлены аналогичным образом: максимальное целочисленное значение сопоставляется с 1,0, а нулевое сопоставляется с 0,0.</span><span class="sxs-lookup"><span data-stu-id="26529-126">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="26529-127">Функция <strong>глколорсубтабликст</strong> умножает результирующие значения цвета на GL_c_SCALE и добавляет их в GL_c_BIAS, где <em>c</em> — красный, зеленый, синий и альфа-канал для соответствующих компонентов цвета.</span><span class="sxs-lookup"><span data-stu-id="26529-127">The <strong>glColorSubTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="26529-128">Результаты записываются в диапазон [0, 1].</span><span class="sxs-lookup"><span data-stu-id="26529-128">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="26529-129">Если GL_MAP_COLOR имеет <strong>значение true</strong>, <strong>глколорсубтабликст</strong> масштабирует каждый компонент цвета по размеру таблицы подстановки GL_PIXEL_MAP_c_TO_c, а затем заменяет компонент на значение, на которое он ссылается в этой таблице. <em>c</em> — R, G, B или A соответственно.</span><span class="sxs-lookup"><span data-stu-id="26529-129">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glColorSubTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="26529-130">Функция <strong>глколорсубтабликст</strong> преобразует итоговые цвета RGBA в фрагменты, присоединяя текущую координату <em>z</em>-координаты и координаты текстуры к каждому пикселю, а затем присвоив координаты <em>x</em> и <em>y</em> для <em>n</em>-го фрагмента, такого как<em>x</em>?</span><span class="sxs-lookup"><span data-stu-id="26529-130">The <strong>glColorSubTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment such that<em>x</em>?</span></span><span data-ttu-id="26529-131"> = <em>Ширина</em> <em>x</em><sub>r</sub> + <em>n</em></span><span class="sxs-lookup"><span data-stu-id="26529-131"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="26529-132"><em>Да</em>?</span><span class="sxs-lookup"><span data-stu-id="26529-132"><em>y</em>?</span></span><span data-ttu-id="26529-133"> = <em>y</em><sub></sub> +<em>n/Ширина</em></span><span class="sxs-lookup"><span data-stu-id="26529-133"> = <em>y</em><sub>r</sub> +<em>n / width</em></span></span><br/> <span data-ttu-id="26529-134">где (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) — Текущая разточечная координата.</span><span class="sxs-lookup"><span data-stu-id="26529-134">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="26529-135">Затем эти фрагменты пикселов обрабатываются так же, как фрагменты, созданные с помощью растровых точек, линий или многоугольников.</span><span class="sxs-lookup"><span data-stu-id="26529-135">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="26529-136">Функция <strong>глколорсубтабликст</strong> применяет сопоставление текстур, туман и все операции фрагментов перед записью фрагментов в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="26529-136">The <strong>glColorSubTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="26529-137"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="26529-137"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="26529-138">Каждый пиксель является одним красным компонентом.</span><span class="sxs-lookup"><span data-stu-id="26529-138">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="26529-139">Функция <strong>глколорсубтабликст</strong> преобразует этот компонент во внутренний формат точно так же, как красный компонент в пикселе RGBA, а затем преобразует его в пиксель RGBA с зеленым и синим значением 0,0, а альфа-канал — в значение 1,0.</span><span class="sxs-lookup"><span data-stu-id="26529-139">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="26529-140">После этого преобразования пиксел обрабатывается так же, как если бы он был считан как пиксель RGBA.</span><span class="sxs-lookup"><span data-stu-id="26529-140">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="26529-141"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="26529-141"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="26529-142">Каждый пиксель является одним зеленым компонентом.</span><span class="sxs-lookup"><span data-stu-id="26529-142">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="26529-143">Функция <strong>глколорсубтабликст</strong> преобразует этот компонент во внутренний формат таким же образом, как и зеленый компонент в пиксельном виде, а затем преобразует его в пиксель RGBA с красным и синим значением в 0,0, а альфа-канал — в значение 1,0.</span><span class="sxs-lookup"><span data-stu-id="26529-143">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="26529-144">После этого преобразования пиксел обрабатывается так же, как если бы он был считан как пиксель RGBA.</span><span class="sxs-lookup"><span data-stu-id="26529-144">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="26529-145"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="26529-145"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="26529-146">Каждый пиксель является одним синим компонентом.</span><span class="sxs-lookup"><span data-stu-id="26529-146">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="26529-147">Функция <strong>глколорсубтабликст</strong> преобразует этот компонент во внутренний формат точно таким же образом, как и синий компонент в пикселе RGBA, а затем преобразует его в пиксель RGBA с красным и зеленым значением, равным 0,0, а альфа-канал — 1,0.</span><span class="sxs-lookup"><span data-stu-id="26529-147">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="26529-148">После этого преобразования пиксел обрабатывается так же, как если бы он был считан как пиксель RGBA.</span><span class="sxs-lookup"><span data-stu-id="26529-148">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="26529-149"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="26529-149"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="26529-150">Каждый пиксель является одним компонентом альфа.</span><span class="sxs-lookup"><span data-stu-id="26529-150">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="26529-151">Функция <strong>глколорсубтабликст</strong> преобразует этот компонент во внутренний формат точно так же, как альфа-компонент в пиксельном пикселе RGBA, а затем преобразует его в пиксель RGBA с красным, зеленым и синим установленным значением 0,0.</span><span class="sxs-lookup"><span data-stu-id="26529-151">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="26529-152">После этого преобразования пиксел обрабатывается так же, как если бы он был считан как пиксель RGBA.</span><span class="sxs-lookup"><span data-stu-id="26529-152">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="26529-153"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="26529-153"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="26529-154">Каждый пиксель — это группа из трех компонентов в следующем порядке: красный, зеленый, синий.</span><span class="sxs-lookup"><span data-stu-id="26529-154">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="26529-155">Функция <strong>глколорсубтабликст</strong> преобразует каждый компонент во внутренний формат точно так же, как красный, зеленый и синий компоненты на пиксель RGBA.</span><span class="sxs-lookup"><span data-stu-id="26529-155">The <strong>glColorSubTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="26529-156">Тройной цвет преобразуется в пиксель RGBA с альфа-составляющей, равным 1,0.</span><span class="sxs-lookup"><span data-stu-id="26529-156">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="26529-157">После этого преобразования пиксел обрабатывается так же, как если бы он был считан как пиксель RGBA.</span><span class="sxs-lookup"><span data-stu-id="26529-157">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="26529-158"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="26529-158"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="26529-159">Каждый пиксель — это группа из трех компонентов в следующем порядке: синий, зеленый, красный.</span><span class="sxs-lookup"><span data-stu-id="26529-159">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="26529-160">GL_BGR_EXT предоставляет формат, соответствующий макету памяти, не зависящему от устройства Windows (DIB).</span><span class="sxs-lookup"><span data-stu-id="26529-160">GL_BGR_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="26529-161">Поэтому приложения могут использовать те же данные, что и вызовы функций Windows, и вызовы функций OpenGL Pixel.</span><span class="sxs-lookup"><span data-stu-id="26529-161">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="26529-162"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="26529-162"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="26529-163">Каждый пиксель — это группа из четырех компонентов в следующем порядке: синий, зеленый, красный, альфа.</span><span class="sxs-lookup"><span data-stu-id="26529-163">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="26529-164">GL_BGRA_EXT предоставляет формат, соответствующий макету памяти, не зависящему от устройства Windows (DIB).</span><span class="sxs-lookup"><span data-stu-id="26529-164">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="26529-165">Поэтому приложения могут использовать те же данные, что и вызовы функций Windows, и вызовы функций OpenGL Pixel.</span><span class="sxs-lookup"><span data-stu-id="26529-165">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="26529-166">*type*</span><span class="sxs-lookup"><span data-stu-id="26529-166">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="26529-167">Тип данных для *данных*.</span><span class="sxs-lookup"><span data-stu-id="26529-167">The data type for *data*.</span></span> <span data-ttu-id="26529-168">Следующие символьные константы принимаются: Byte без знака, формат GL, неподписанный байт, формат GL, Short, GL без знака, GL \_ \_ \_ \_ \_ \_ \_ \_ \_ int и GL с \_ плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="26529-168">The following symbolic constants are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

<span data-ttu-id="26529-169">В следующей таблице приведены значения допустимых констант для параметра *типа* .</span><span class="sxs-lookup"><span data-stu-id="26529-169">The following table summarizes the meaning of the valid constants for the *type* parameter.</span></span>



| <span data-ttu-id="26529-170">Значение</span><span class="sxs-lookup"><span data-stu-id="26529-170">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="26529-171">Значение</span><span class="sxs-lookup"><span data-stu-id="26529-171">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="26529-172"><dt>**\_байт без знака GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="26529-172"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="26529-173">8-разрядное целое число без знака</span><span class="sxs-lookup"><span data-stu-id="26529-173">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="26529-174"><dt>**\_байт GL**</dt></span><span class="sxs-lookup"><span data-stu-id="26529-174"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="26529-175">8-разрядное целое число со знаком</span><span class="sxs-lookup"><span data-stu-id="26529-175">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="26529-176"><dt>**\_ \_ сокращенный формат GL без знака**</dt></span><span class="sxs-lookup"><span data-stu-id="26529-176"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="26529-177">16-разрядное целое число без знака</span><span class="sxs-lookup"><span data-stu-id="26529-177">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="26529-178"><dt>**\_Краткая GL**</dt></span><span class="sxs-lookup"><span data-stu-id="26529-178"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="26529-179">16-разрядное целое число со знаком</span><span class="sxs-lookup"><span data-stu-id="26529-179">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="26529-180"><dt>**\_целое число без знака GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="26529-180"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="26529-181">32-разрядное целое число без знака</span><span class="sxs-lookup"><span data-stu-id="26529-181">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="26529-182"><dt>**тип в GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="26529-182"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="26529-183">32-разрядное целое число</span><span class="sxs-lookup"><span data-stu-id="26529-183">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="26529-184"><dt>**с \_ плавающей запятой**</dt></span><span class="sxs-lookup"><span data-stu-id="26529-184"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="26529-185">Число одинарной точности с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="26529-185">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="26529-186">*data*</span><span class="sxs-lookup"><span data-stu-id="26529-186">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="26529-187">Указатель на данные текстуры с палитрой.</span><span class="sxs-lookup"><span data-stu-id="26529-187">A pointer to the paletted texture data.</span></span> <span data-ttu-id="26529-188">Для записи палитры данные обрабатываются как отдельные пиксели в палитре одномерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="26529-188">The data is treated as single pixels of a 1-D texture palette entry for a palette entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26529-189">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26529-189">Return value</span></span>

<span data-ttu-id="26529-190">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="26529-190">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="26529-191">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="26529-191">Error codes</span></span>

<span data-ttu-id="26529-192">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="26529-192">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="26529-193">Имя</span><span class="sxs-lookup"><span data-stu-id="26529-193">Name</span></span>                                                                                              | <span data-ttu-id="26529-194">Значение</span><span class="sxs-lookup"><span data-stu-id="26529-194">Meaning</span></span>                                                                                                                               |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="26529-195"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="26529-195"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="26529-196">значение *Start* или *Count* было недопустимым целым числом.</span><span class="sxs-lookup"><span data-stu-id="26529-196">*start* or *count* was an invalid integer.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="26529-197"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="26529-197"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="26529-198">*целевой объект*, *Формат* или *тип* не являются допустимыми значениями.</span><span class="sxs-lookup"><span data-stu-id="26529-198">*target*, *format*,or *type* was not an accepted value.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="26529-199"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="26529-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="26529-200">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="26529-200">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="26529-201">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26529-201">Remarks</span></span>

<span data-ttu-id="26529-202">Функция **глколорсубтабликст** указывает части палитры текущей целевой текстуры для замены.</span><span class="sxs-lookup"><span data-stu-id="26529-202">The **glColorSubTableEXT** function specifies portions of the current targeted texture's palette to be replaced.</span></span> <span data-ttu-id="26529-203">В отличие от [**глколортабликст**](glcolortableext.md), нельзя указать *целевой* параметр в качестве палитры текстуры-посредника.</span><span class="sxs-lookup"><span data-stu-id="26529-203">Unlike [**glColorTableEXT**](glcolortableext.md), you cannot specify the *target* parameter to be a proxy texture palette.</span></span>

> [!Note]  
> <span data-ttu-id="26529-204">Функция **глколорсубтабликст** — это функция расширения, которая не является частью стандартной библиотеки OpenGL, но является частью расширения текстуры с помощью \_ палитры типа "Расш \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="26529-204">The **glColorSubTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="26529-205">Чтобы проверить, поддерживает ли ваша реализация OpenGL **глколорсубтабликст**, вызовите [**глжетстринг**](glgetstring.md)( \_ расширения GL).</span><span class="sxs-lookup"><span data-stu-id="26529-205">To check whether your implementation of OpenGL supports **glColorSubTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="26529-206">Если он возвращает \_ \_ текстуру с Многоцветовой палитрой GL \_ , поддерживается **глколорсубтабликст** .</span><span class="sxs-lookup"><span data-stu-id="26529-206">If it returns GL\_EXT\_paletted\_texture, **glColorSubTableEXT** is supported.</span></span> <span data-ttu-id="26529-207">Чтобы получить адрес функции расширения, вызовите [**вглжетпрокаддресс**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="26529-207">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="26529-208">Требования</span><span class="sxs-lookup"><span data-stu-id="26529-208">Requirements</span></span>



| <span data-ttu-id="26529-209">Требование</span><span class="sxs-lookup"><span data-stu-id="26529-209">Requirement</span></span> | <span data-ttu-id="26529-210">Значение</span><span class="sxs-lookup"><span data-stu-id="26529-210">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="26529-211">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26529-211">Minimum supported client</span></span><br/> | <span data-ttu-id="26529-212">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="26529-212">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="26529-213">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26529-213">Minimum supported server</span></span><br/> | <span data-ttu-id="26529-214">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="26529-214">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="26529-215">Заголовок</span><span class="sxs-lookup"><span data-stu-id="26529-215">Header</span></span><br/>                   | <dl> <span data-ttu-id="26529-216"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="26529-216"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26529-217">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26529-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26529-218">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="26529-218">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="26529-219">**глколортабликст**</span><span class="sxs-lookup"><span data-stu-id="26529-219">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="26529-220">**гленд**</span><span class="sxs-lookup"><span data-stu-id="26529-220">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="26529-221">**глжетколортабликст**</span><span class="sxs-lookup"><span data-stu-id="26529-221">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="26529-222">**глжетколортаблепараметерфвекст**</span><span class="sxs-lookup"><span data-stu-id="26529-222">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="26529-223">**глжетколортаблепараметеривекст**</span><span class="sxs-lookup"><span data-stu-id="26529-223">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="26529-224">**глжетстринг**</span><span class="sxs-lookup"><span data-stu-id="26529-224">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="26529-225">**вглжетпрокаддресс**</span><span class="sxs-lookup"><span data-stu-id="26529-225">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





