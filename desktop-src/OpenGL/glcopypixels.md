---
title: Функция Глкопипикселс (GL. h)
description: Функция Глкопипикселс копирует Пиксели в буфера кадров.
ms.assetid: c4055928-7b8b-4d0f-94f3-e3b9c0503308
keywords:
- Функция Глкопипикселс OpenGL
topic_type:
- apiref
api_name:
- glCopyPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7ba0833534d21e48c251da6491fee2996c3ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988789"
---
# <a name="glcopypixels-function"></a><span data-ttu-id="d9b1e-104">Функция Глкопипикселс</span><span class="sxs-lookup"><span data-stu-id="d9b1e-104">glCopyPixels function</span></span>

<span data-ttu-id="d9b1e-105">Функция **глкопипикселс** копирует Пиксели в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-105">The **glCopyPixels** function copies pixels in the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9b1e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9b1e-106">Syntax</span></span>


```C++
void WINAPI glCopyPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  type
);
```



## <a name="parameters"></a><span data-ttu-id="d9b1e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9b1e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9b1e-108">*x*</span><span class="sxs-lookup"><span data-stu-id="d9b1e-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="d9b1e-109">Координата x окна в левом нижнем углу прямоугольной области пикселей для копирования.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-109">The window x-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="d9b1e-110">*y*</span><span class="sxs-lookup"><span data-stu-id="d9b1e-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="d9b1e-111">Координата точки y окна для копирования левого нижнего угла прямоугольной области пикселей.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-111">The window y-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="d9b1e-112">*width*</span><span class="sxs-lookup"><span data-stu-id="d9b1e-112">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="d9b1e-113">Измерение ширины прямоугольной области пикселей для копирования.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-113">The width dimension of the rectangular region of pixels to be copied.</span></span> <span data-ttu-id="d9b1e-114">Должно быть неотрицательным значением.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-114">Must be nonnegative.</span></span>

</dd> <dt>

<span data-ttu-id="d9b1e-115">*height*</span><span class="sxs-lookup"><span data-stu-id="d9b1e-115">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="d9b1e-116">Измерение высоты прямоугольной области пикселей для копирования.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-116">The height dimension of the rectangular region of pixels to be copied.</span></span> <span data-ttu-id="d9b1e-117">Должно быть неотрицательным значением.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-117">Must be nonnegative.</span></span>

</dd> <dt>

<span data-ttu-id="d9b1e-118">*type*</span><span class="sxs-lookup"><span data-stu-id="d9b1e-118">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="d9b1e-119">Указывает, следует ли **глкопипикселс** копировать значения цветов, значения глубины или значения трафарета.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-119">Specifies whether **glCopyPixels** is to copy color values, depth values, or stencil values.</span></span> <span data-ttu-id="d9b1e-120">Допустимые символьные константы:.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-120">The acceptable symbolic constants are.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9b1e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d9b1e-121">Value</span></span></th>
<th><span data-ttu-id="d9b1e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d9b1e-122">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_COLOR"></span><span id="gl_color"></span><dl> <span data-ttu-id="d9b1e-123"><dt><strong>GL_COLOR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d9b1e-123"><dt><strong>GL_COLOR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d9b1e-124">Функция <strong>глкопипикселс</strong> считывает индексы или цвета RGBA из буфера, указанного в качестве исходного буфера чтения (см. <a href="glreadbuffer.md"><strong>глреадбуффер</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="d9b1e-124">The <strong>glCopyPixels</strong> function reads indexes or RGBA colors from the buffer currently specified as the read source buffer (see <a href="glreadbuffer.md"><strong>glReadBuffer</strong></a>).</span></span> <br/> <span data-ttu-id="d9b1e-125">Если OpenGL находится в режиме индексов цветов:</span><span class="sxs-lookup"><span data-stu-id="d9b1e-125">If OpenGL is in color-index mode:</span></span><br/>
<ol>
<li><span data-ttu-id="d9b1e-126">Каждый индекс, считанный из этого буфера, преобразуется в формат с фиксированной запятой с неопределенным числом битов справа от двоичной точки.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-126">Each index that is read from this buffer is converted to a fixed-point format with an unspecified number of bits to the right of the binary point.</span></span></li>
<li><span data-ttu-id="d9b1e-127">Каждый индекс смещается влево на GL_INDEX_SHIFT бит и добавляется в GL_INDEX_OFFSET. Если GL_INDEX_SHIFT является отрицательным, сдвиг вправо.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-127">Each index is shifted left by GL_INDEX_SHIFT bits, and added to GL_INDEX_OFFSET.If GL_INDEX_SHIFT is negative, the shift is to the right.</span></span> <span data-ttu-id="d9b1e-128">В любом случае нулевые биты заполняются в результате неопределенных битовых точек в результатах.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-128">In either case, zero bits fill otherwise unspecified bit locations in the result.</span></span><br/></li>
<li><span data-ttu-id="d9b1e-129">Если GL_MAP_COLOR имеет значение true, индекс заменяется на значение, на которое он ссылается в таблице подстановки GL_PIXEL_MAP_I_TO_I.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-129">If GL_MAP_COLOR is true, the index is replaced with the value that it references in lookup table GL_PIXEL_MAP_I_TO_I.</span></span></li>
<li><span data-ttu-id="d9b1e-130">Независимо от того, выполняется ли замена уточняющего запроса индекса, целочисленная часть индекса затем <strong>и</strong>ED с 2<em><sup>b</sup></em> 1, где <em>b</em> — число битов в буфере цветового индекса.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-130">Whether the lookup replacement of the index is done or not, the integer part of the index is then <strong>AND</strong>ed with 2<em><sup>b</sup></em> 1, where <em>b</em> is the number of bits in a color-index buffer.</span></span></li>
</ol>
<span data-ttu-id="d9b1e-131">Если OpenGL находится в режиме RGBA:</span><span class="sxs-lookup"><span data-stu-id="d9b1e-131">If OpenGL is in RGBA mode:</span></span><br/>
<ol>
<li><span data-ttu-id="d9b1e-132">Красный, зеленый, синий и альфа-компоненты каждого считанного пиксела преобразуются во внутренний формат с плавающей запятой с неопределенной точностью.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-132">The red, green, blue, and alpha components of each pixel that is read are converted to an internal floating-point format with unspecified precision.</span></span></li>
<li><span data-ttu-id="d9b1e-133">Преобразование сопоставляет значение самого крупного возможного компонента с 1,0, а значение компонента — нуль — 0,0.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-133">The conversion maps the largest representable component value to 1.0, and component value zero to 0.0.</span></span></li>
<li><span data-ttu-id="d9b1e-134">Результирующие значения цвета с плавающей запятой затем умножаются на GL_c_SCALE и добавляются в GL_c_BIAS, где <em>c</em> — красный, зеленый, синий и альфа-канал для соответствующих компонентов цвета.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-134">The resulting floating-point color values are then multiplied by GL_c_SCALE and added to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span></li>
<li><span data-ttu-id="d9b1e-135">Результаты записываются в диапазон [0, 1].</span><span class="sxs-lookup"><span data-stu-id="d9b1e-135">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="d9b1e-136">Если GL_MAP_COLOR имеет значение true, каждый компонент цвета масштабируется по размеру таблицы подстановки GL_PIXEL_MAP_c_TO_c, а затем заменяется на значение, на которое она ссылается в этой таблице. <em>c</em> — R, G, B или A соответственно.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-136">If GL_MAP_COLOR is true, each color component is scaled by the size of lookup table GL_PIXEL_MAP_c_TO_c, and then replaced by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span> <span data-ttu-id="d9b1e-137">Полученные в результате индексы или RGBA цвета преобразуются в фрагменты путем присоединения текущей растровой координаты <em>z</em>и координат текстуры к каждому пикселю, а затем присваиваются координаты окна (<em>x</em><sub>r</sub> + , <em>y r</em><sub></sub> + <em>j</em>), где (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) — текущее положение относительной точки, а пиксель — пиксель в положении <em>i</em> в строке <em>j</em> .</span><span class="sxs-lookup"><span data-stu-id="d9b1e-137">The resulting indexes or RGBA colors are then converted to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, and then assigning window coordinates (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position, and the pixel was the pixel in the <em>i</em> position in the <em>j</em> row.</span></span> <span data-ttu-id="d9b1e-138">Затем эти фрагменты пикселов обрабатываются так же, как фрагменты, созданные с помощью растровых точек, линий или многоугольников.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-138">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="d9b1e-139">Сопоставление текстур, туман и все операции фрагмента применяются до того, как фрагменты записываются в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-139">Texture mapping, fog, and all the fragment operations are applied before the fragments are written to the framebuffer.</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_DEPTH"></span><span id="gl_depth"></span><dl> <span data-ttu-id="d9b1e-140"><dt><strong>GL_DEPTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d9b1e-140"><dt><strong>GL_DEPTH</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d9b1e-141">Значения глубины считываются из буфера глубины и преобразуются непосредственно во внутренний формат с плавающей запятой с неуказанной точностью.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-141">Depth values are read from the depth buffer and converted directly to an internal floating-point format with unspecified precision.</span></span> <span data-ttu-id="d9b1e-142">Полученное значение глубины с плавающей запятой затем умножается на GL_DEPTH_SCALE и добавляется в GL_DEPTH_BIAS.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-142">The resulting floating-point depth value is then multiplied by GL_DEPTH_SCALE and added to GL_DEPTH_BIAS.</span></span> <span data-ttu-id="d9b1e-143">Результат задается в виде фиксации в диапазоне [0, 1].</span><span class="sxs-lookup"><span data-stu-id="d9b1e-143">The result is clamped to the range [0,1].</span></span> <br/> <span data-ttu-id="d9b1e-144">Результирующие компоненты глубины затем преобразуются в фрагменты путем присоединения текущего цветового индекса или цветового указателя и координат текстуры к каждому пикселю, а затем присваиваются координаты окна (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), где (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) — Текущая растровая позиция, а пиксель — пиксель в позиции <em>i</em> в строке <em>j</em> .</span><span class="sxs-lookup"><span data-stu-id="d9b1e-144">The resulting depth components are then converted to fragments by attaching the current raster position color or color index and texture coordinates to each pixel, then assigning window coordinates (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position, and the pixel was the pixel in the <em>i</em> position in the <em>j</em> row.</span></span> <span data-ttu-id="d9b1e-145">Затем эти фрагменты пикселов обрабатываются так же, как фрагменты, созданные с помощью растровых точек, линий или многоугольников.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-145">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="d9b1e-146">Сопоставление текстур, туман и все операции фрагмента применяются до того, как фрагменты записываются в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-146">Texture mapping, fog, and all the fragment operations are applied before the fragments are written to the framebuffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_STENCIL"></span><span id="gl_stencil"></span><dl> <span data-ttu-id="d9b1e-147"><dt><strong>GL_STENCIL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d9b1e-147"><dt><strong>GL_STENCIL</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d9b1e-148">Индексы наборов элементов считываются из буфера шаблона и преобразуются во внутренний формат с фиксированной запятой с неопределенным числом битов справа от двоичной точки.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-148">Stencil indexes are read from the stencil buffer and converted to an internal fixed-point format with an unspecified number of bits to the right of the binary point.</span></span> <span data-ttu-id="d9b1e-149">Затем каждый индекс с фиксированной точкой смещается на GL_INDEX_SHIFT бит и добавляется в GL_INDEX_OFFSET.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-149">Each fixed-point index is then shifted left by GL_INDEX_SHIFT bits, and added to GL_INDEX_OFFSET.</span></span> <span data-ttu-id="d9b1e-150">Если GL_INDEX_SHIFT является отрицательным, сдвиг вправо.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-150">If GL_INDEX_SHIFT is negative, the shift is to the right.</span></span> <span data-ttu-id="d9b1e-151">В любом случае нулевые биты заполняются в результате неопределенных битовых точек в результатах.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-151">In either case, zero bits fill otherwise unspecified bit locations in the result.</span></span> <span data-ttu-id="d9b1e-152">Если GL_MAP_STENCIL имеет значение true, индекс заменяется на значение, на которое он ссылается в таблице подстановки GL_PIXEL_MAP_S_TO_S.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-152">If GL_MAP_STENCIL is true, the index is replaced with the value that it references in lookup table GL_PIXEL_MAP_S_TO_S.</span></span> <span data-ttu-id="d9b1e-153">Независимо от того, выполняется ли замена уточняющего запроса индекса, целочисленная часть индекса затем <strong>и</strong>ED с 2<sup>b</sup> - 1, где <em>b</em> — число битов в буфере шаблона.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-153">Whether the lookup replacement of the index is done or not, the integer part of the index is then <strong>AND</strong>ed with 2<sup>b</sup> - 1, where <em>b</em> is the number of bits in the stencil buffer.</span></span> <span data-ttu-id="d9b1e-154">Итоговые индексы набора элементов затем записываются в буфер трафарета таким, что индекс, считанный из <em>i</em> -е строки <em>j</em> , записывается в расположение (<em>x</em><sub>r</sub> + <em>i</em>, <em>y</em><sub>r</sub> + <em>j</em>), где (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) — текущее положение в виде растровой позиции.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-154">The resulting stencil indexes are then written to the stencil buffer such that the index read from the <em>i</em> location of the <em>j</em> row is written to location (<em>x</em><sub>r</sub> + <em>i</em>, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span> <span data-ttu-id="d9b1e-155">На эти операции записи влияют только тест «точка-владение», «прямоугольный тест» и вритемаск трафарета.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-155">Only the pixel-ownership test, the scissor test, and the stencil writemask affect these writes.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9b1e-156">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9b1e-156">Return value</span></span>

<span data-ttu-id="d9b1e-157">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-157">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d9b1e-158">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d9b1e-158">Error codes</span></span>

<span data-ttu-id="d9b1e-159">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-159">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d9b1e-160">Имя</span><span class="sxs-lookup"><span data-stu-id="d9b1e-160">Name</span></span>                                                                                                  | <span data-ttu-id="d9b1e-161">Значение</span><span class="sxs-lookup"><span data-stu-id="d9b1e-161">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d9b1e-162"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d9b1e-162"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d9b1e-163">*тип* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-163">*type* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="d9b1e-164"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d9b1e-164"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="d9b1e-165">Либо *Ширина* , либо высота были отрицательными.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-165">Either *width* or height was negative.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="d9b1e-166"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d9b1e-166"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d9b1e-167">*тип* имел \_ глубину GL, а буфер глубины отсутствует.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-167">*type* was GL\_DEPTH and there was no depth buffer.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="d9b1e-168"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d9b1e-168"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d9b1e-169">*тип* был \_ трафаретом GL, но буфер трафарета не существует.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-169">*type* was GL\_STENCIL and there was no stencil buffer.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="d9b1e-170"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d9b1e-170"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d9b1e-171">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="d9b1e-171">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d9b1e-172">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9b1e-172">Remarks</span></span>

<span data-ttu-id="d9b1e-173">Функция **глкопипикселс** копирует прямоугольник пикселей с выставкой по экрану из указанного расположения буфера кадров в регион относительно текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-173">The **glCopyPixels** function copies a screen-aligned rectangle of pixels from the specified framebuffer location to a region relative to the current raster position.</span></span> <span data-ttu-id="d9b1e-174">Его операция хорошо определена только в том случае, если область источника пикселя находится внутри видимой части окна.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-174">Its operation is well defined only if the entire pixel source region is within the exposed portion of the window.</span></span> <span data-ttu-id="d9b1e-175">Результаты копирования извне окна или из областей окна, которые не являются видимыми, являются аппаратно зависимыми и неопределенными.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-175">Results of copies from outside the window, or from regions of the window that are not exposed, are hardware dependent and undefined.</span></span>

<span data-ttu-id="d9b1e-176">Параметры *x* и *y* задают координаты окна левого нижнего угла прямоугольной области для копирования.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-176">The *x* and *y* parameters specify the window coordinates of the lower-left corner of the rectangular region to be copied.</span></span> <span data-ttu-id="d9b1e-177">Параметры *Width* и *Height* определяют размеры прямоугольной области для копирования.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-177">The *width* and *height* parameters specify the dimensions of the rectangular region to be copied.</span></span> <span data-ttu-id="d9b1e-178">*Ширина* и *Высота* должны быть неотрицательными.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-178">Both *width* and *height* must be nonnegative.</span></span>

<span data-ttu-id="d9b1e-179">Несколько параметров управляют обработкой данных пикселей во время их копирования.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-179">Several parameters control the processing of the pixel data while it is being copied.</span></span> <span data-ttu-id="d9b1e-180">Эти параметры задаются тремя функциями: [**глпикселтрансфер**](glpixeltransfer.md), [**глпикселмап**](glpixelmap.md)и [**глпикселзум**](glpixelzoom.md).</span><span class="sxs-lookup"><span data-stu-id="d9b1e-180">These parameters are set with three functions: [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md), and [**glPixelZoom**](glpixelzoom.md).</span></span> <span data-ttu-id="d9b1e-181">В этом разделе описывается влияние на **глкопипикселс** большинства (но не всех) параметров, заданных этими тремя функциями.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-181">This topic describes the effects on **glCopyPixels** of most, but not all, of the parameters specified by these three functions.</span></span>

<span data-ttu-id="d9b1e-182">Функция **глкопипикселс** копирует значения из каждого пикселя в левом нижнем углу в (*x*  +  *i*, *y*  +  *j*) для 0 =   <  *Ширина* i и 0 = *j*  <  *Height*.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-182">The **glCopyPixels** function copies values from each pixel with the lower-left corner at (*x* + *i*, *y* + *j*) for 0 = *i* < *width* and 0 = *j* < *height*.</span></span> <span data-ttu-id="d9b1e-183">Этот пиксель считается точкой *i* в строке *j* .</span><span class="sxs-lookup"><span data-stu-id="d9b1e-183">This pixel is said to be the *i* pixel in the *j* row.</span></span> <span data-ttu-id="d9b1e-184">Пиксели копируются в порядке строк от нижнего к верхнему, слева направо в каждой строке.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-184">Pixels are copied in row order from the lowest to the highest row, left to right in each row.</span></span>

<span data-ttu-id="d9b1e-185">Параметр *типа* указывает, следует ли копировать данные цвета, глубины или трафарета.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-185">The *type* parameter specifies whether color, depth, or stencil data is to be copied.</span></span>

<span data-ttu-id="d9b1e-186">Приведенная выше растрирования предполагает, что коэффициенты масштабирования пикселя в 1,0.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-186">The rasterization described thus far assumes pixel zoom factors of 1.0.</span></span> <span data-ttu-id="d9b1e-187">При использовании [**глпикселзум**](glpixelzoom.md) для изменения коэффициентов масштабирования *x* и *y* Пиксели преобразуются в фрагменты следующим образом.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-187">If you use [**glPixelZoom**](glpixelzoom.md) to change the *x* and *y* pixel zoom factors, pixels are converted to fragments as follows.</span></span> <span data-ttu-id="d9b1e-188">Если (*x*<sub>r</sub> , *y*<sub>r</sub> ) является текущей позицией разряда, а заданный пиксель находится в позиции *i* в строке *j* исходного пиксельного прямоугольника, то фрагменты создаются для пикселов, центры которых находятся в прямоугольнике с углами в</span><span class="sxs-lookup"><span data-stu-id="d9b1e-188">If (*x*<sub>r</sub> , *y*<sub>r</sub> ) is the current raster position, and a given pixel is in the *i* location in the *j* row of the source pixel rectangle, then fragments are generated for pixels whose centers are in the rectangle with corners at</span></span>

<span data-ttu-id="d9b1e-189">(*x*<sub>r</sub>  +  *увеличить масштаб* я, y <sub>r</sub>  +  *Zoom*<sub>y</sub> *j*)</span><span class="sxs-lookup"><span data-stu-id="d9b1e-189">(*x*<sub>r</sub> + *zoom*? i, y <sub>r</sub> + *zoom*<sub>y</sub> *j*)</span></span>

<span data-ttu-id="d9b1e-190">и</span><span class="sxs-lookup"><span data-stu-id="d9b1e-190">and</span></span>

<span data-ttu-id="d9b1e-191">(*x*<sub>r</sub>  +  *увеличить масштаб*</span><span class="sxs-lookup"><span data-stu-id="d9b1e-191">(*x*<sub>r</sub> + *zoom*?</span></span> <span data-ttu-id="d9b1e-192">(*i* + 1), *y*<sub>r</sub>  +  *Zoom*<sub>y</sub> (*j* + 1))</span><span class="sxs-lookup"><span data-stu-id="d9b1e-192">(*i* + 1), *y*<sub>r</sub> + *zoom*<sub>y</sub> (*j* + 1))</span></span>

<span data-ttu-id="d9b1e-193">где *увеличить*? — значение параметра «масштаб в GL» \_ \_ X, а « *масштаб*<sub>y</sub> » — значение « \_ Масштаб по \_ оси y».</span><span class="sxs-lookup"><span data-stu-id="d9b1e-193">where *zoom*? is the value of GL\_ZOOM\_X and *zoom*<sub>y</sub> is the value of GL\_ZOOM\_Y.</span></span>

<span data-ttu-id="d9b1e-194">Режимы, заданные параметром [**глпикселсторе**](glpixelstore-functions.md) , не влияют на работу **глкопипикселс**.</span><span class="sxs-lookup"><span data-stu-id="d9b1e-194">Modes specified by [**glPixelStore**](glpixelstore-functions.md) have no effect on the operation of **glCopyPixels**.</span></span>

<span data-ttu-id="d9b1e-195">Следующие функции извлекают сведения, относящиеся к **глкопипикселс**:</span><span class="sxs-lookup"><span data-stu-id="d9b1e-195">The following functions retrieve information related to **glCopyPixels**:</span></span>

<span data-ttu-id="d9b1e-196">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ текущей \_ точечной \_ позицией GL</span><span class="sxs-lookup"><span data-stu-id="d9b1e-196">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>

<span data-ttu-id="d9b1e-197">**глжет** с аргументом \_ текущей \_ точечной \_ позицией GL \_ допустимо</span><span class="sxs-lookup"><span data-stu-id="d9b1e-197">**glGet** with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>

<span data-ttu-id="d9b1e-198">Чтобы скопировать цветовую точку в левом нижнем углу окна в текущую координату, используйте</span><span class="sxs-lookup"><span data-stu-id="d9b1e-198">To copy the color pixel in the lower-left corner of the window to the current raster position, use</span></span>

<span data-ttu-id="d9b1e-199">**глкопипикселс**(0, 0, 1, 1, GL \_ );</span><span class="sxs-lookup"><span data-stu-id="d9b1e-199">**glCopyPixels**( 0, 0, 1, 1, GL\_COLOR );</span></span>

## <a name="requirements"></a><span data-ttu-id="d9b1e-200">Требования</span><span class="sxs-lookup"><span data-stu-id="d9b1e-200">Requirements</span></span>



| <span data-ttu-id="d9b1e-201">Требование</span><span class="sxs-lookup"><span data-stu-id="d9b1e-201">Requirement</span></span> | <span data-ttu-id="d9b1e-202">Значение</span><span class="sxs-lookup"><span data-stu-id="d9b1e-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9b1e-203">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9b1e-203">Minimum supported client</span></span><br/> | <span data-ttu-id="d9b1e-204">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d9b1e-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d9b1e-205">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9b1e-205">Minimum supported server</span></span><br/> | <span data-ttu-id="d9b1e-206">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d9b1e-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d9b1e-207">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d9b1e-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9b1e-208"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9b1e-208"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d9b1e-209">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d9b1e-209">Library</span></span><br/>                  | <dl> <span data-ttu-id="d9b1e-210"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9b1e-210"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d9b1e-211">DLL</span><span class="sxs-lookup"><span data-stu-id="d9b1e-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9b1e-212"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9b1e-212"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9b1e-213">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9b1e-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9b1e-214">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="d9b1e-214">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d9b1e-215">**глдепсфунк**</span><span class="sxs-lookup"><span data-stu-id="d9b1e-215">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="d9b1e-216">**глдравбуффер**</span><span class="sxs-lookup"><span data-stu-id="d9b1e-216">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="d9b1e-217">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="d9b1e-217">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="d9b1e-218">**гленд**</span><span class="sxs-lookup"><span data-stu-id="d9b1e-218">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d9b1e-219">**глжет**</span><span class="sxs-lookup"><span data-stu-id="d9b1e-219">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="d9b1e-220">**глпикселмап**</span><span class="sxs-lookup"><span data-stu-id="d9b1e-220">**glPixelMap**</span></span>](glpixelmap.md)
</dt> <dt>

[<span data-ttu-id="d9b1e-221">**глпикселсторе**</span><span class="sxs-lookup"><span data-stu-id="d9b1e-221">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="d9b1e-222">**глпикселтрансфер**</span><span class="sxs-lookup"><span data-stu-id="d9b1e-222">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="d9b1e-223">**глпикселзум**</span><span class="sxs-lookup"><span data-stu-id="d9b1e-223">**glPixelZoom**</span></span>](glpixelzoom.md)
</dt> <dt>

[<span data-ttu-id="d9b1e-224">**глрастерпос**</span><span class="sxs-lookup"><span data-stu-id="d9b1e-224">**glRasterPos**</span></span>](glrasterpos-functions.md)
</dt> <dt>

[<span data-ttu-id="d9b1e-225">**глреадбуффер**</span><span class="sxs-lookup"><span data-stu-id="d9b1e-225">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> <dt>

[<span data-ttu-id="d9b1e-226">**глреадпикселс**</span><span class="sxs-lookup"><span data-stu-id="d9b1e-226">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="d9b1e-227">**глстенЦилфунк**</span><span class="sxs-lookup"><span data-stu-id="d9b1e-227">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





