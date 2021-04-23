---
title: Функция Глколортабликст (GL. h)
description: Функция Глколортабликст определяет формат и размер палитры для целевых цветных текстур.
ms.assetid: f3d7b1a1-97a5-47ef-a0ca-5e58acb86bb4
keywords:
- Функция Глколортабликст OpenGL
topic_type:
- apiref
api_name:
- glColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0d5fd5c848e787f480e3e1893b9b25e4bbd3de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802807"
---
# <a name="glcolortableext-function"></a><span data-ttu-id="14bf3-104">Функция Глколортабликст</span><span class="sxs-lookup"><span data-stu-id="14bf3-104">glColorTableEXT function</span></span>

<span data-ttu-id="14bf3-105">Функция **глколортабликст** определяет формат и размер палитры для целевых цветных текстур.</span><span class="sxs-lookup"><span data-stu-id="14bf3-105">The **glColorTableEXT** function specifies the format and size of a palette for targeted paletted textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="14bf3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14bf3-106">Syntax</span></span>


```C++
void WINAPI glColorTableEXT(
         GLenum  target,
         GLenum  internalFormat,
         GLsizei width,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a><span data-ttu-id="14bf3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="14bf3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14bf3-108">*target*</span><span class="sxs-lookup"><span data-stu-id="14bf3-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="14bf3-109">Целевая текстура, для которой изменилась палитра.</span><span class="sxs-lookup"><span data-stu-id="14bf3-109">The target texture that is to have its palette changed.</span></span> <span data-ttu-id="14bf3-110">Должен быть ТЕКСТУРой \_ 1d, \_ 2D текстуры, \_ одномерной текстуры-посредника \_ или \_ 2D-текстурной текстуры \_ .</span><span class="sxs-lookup"><span data-stu-id="14bf3-110">Must be TEXTURE\_1D, TEXTURE\_2D, PROXY\_TEXTURE\_1D, or PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="14bf3-111">*интерналформат*</span><span class="sxs-lookup"><span data-stu-id="14bf3-111">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="14bf3-112">Внутренний формат и разрешение палитры.</span><span class="sxs-lookup"><span data-stu-id="14bf3-112">The internal format and resolution of the palette.</span></span> <span data-ttu-id="14bf3-113">Этот параметр может принимать одно из следующих символьных значений.</span><span class="sxs-lookup"><span data-stu-id="14bf3-113">This parameter can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="14bf3-114">Константа</span><span class="sxs-lookup"><span data-stu-id="14bf3-114">Constant</span></span>       | <span data-ttu-id="14bf3-115">Базовый формат</span><span class="sxs-lookup"><span data-stu-id="14bf3-115">Base Format</span></span> | <span data-ttu-id="14bf3-116">Биты R</span><span class="sxs-lookup"><span data-stu-id="14bf3-116">R Bits</span></span> | <span data-ttu-id="14bf3-117">Биты G</span><span class="sxs-lookup"><span data-stu-id="14bf3-117">G Bits</span></span> | <span data-ttu-id="14bf3-118">B бит</span><span class="sxs-lookup"><span data-stu-id="14bf3-118">B Bits</span></span> | <span data-ttu-id="14bf3-119">Биты</span><span class="sxs-lookup"><span data-stu-id="14bf3-119">A Bits</span></span> |
|----------------|-------------|--------|--------|--------|--------|
| <span data-ttu-id="14bf3-120">GL \_ R3 \_ G3 \_ B2</span><span class="sxs-lookup"><span data-stu-id="14bf3-120">GL\_R3\_G3\_B2</span></span> | <span data-ttu-id="14bf3-121">RGB в формате GL \_</span><span class="sxs-lookup"><span data-stu-id="14bf3-121">GL\_RGB</span></span>     | <span data-ttu-id="14bf3-122">3</span><span class="sxs-lookup"><span data-stu-id="14bf3-122">3</span></span>      | <span data-ttu-id="14bf3-123">3</span><span class="sxs-lookup"><span data-stu-id="14bf3-123">3</span></span>      | <span data-ttu-id="14bf3-124">2</span><span class="sxs-lookup"><span data-stu-id="14bf3-124">2</span></span>      |        |
| <span data-ttu-id="14bf3-125">\_RGB4 GL</span><span class="sxs-lookup"><span data-stu-id="14bf3-125">GL\_RGB4</span></span>       | <span data-ttu-id="14bf3-126">RGB в формате GL \_</span><span class="sxs-lookup"><span data-stu-id="14bf3-126">GL\_RGB</span></span>     | <span data-ttu-id="14bf3-127">4</span><span class="sxs-lookup"><span data-stu-id="14bf3-127">4</span></span>      | <span data-ttu-id="14bf3-128">4</span><span class="sxs-lookup"><span data-stu-id="14bf3-128">4</span></span>      | <span data-ttu-id="14bf3-129">4</span><span class="sxs-lookup"><span data-stu-id="14bf3-129">4</span></span>      |        |
| <span data-ttu-id="14bf3-130">\_RGB5 GL</span><span class="sxs-lookup"><span data-stu-id="14bf3-130">GL\_RGB5</span></span>       | <span data-ttu-id="14bf3-131">RGB в формате GL \_</span><span class="sxs-lookup"><span data-stu-id="14bf3-131">GL\_RGB</span></span>     | <span data-ttu-id="14bf3-132">5</span><span class="sxs-lookup"><span data-stu-id="14bf3-132">5</span></span>      | <span data-ttu-id="14bf3-133">5</span><span class="sxs-lookup"><span data-stu-id="14bf3-133">5</span></span>      | <span data-ttu-id="14bf3-134">5</span><span class="sxs-lookup"><span data-stu-id="14bf3-134">5</span></span>      |        |
| <span data-ttu-id="14bf3-135">\_RGB8 GL</span><span class="sxs-lookup"><span data-stu-id="14bf3-135">GL\_RGB8</span></span>       | <span data-ttu-id="14bf3-136">RGB в формате GL \_</span><span class="sxs-lookup"><span data-stu-id="14bf3-136">GL\_RGB</span></span>     | <span data-ttu-id="14bf3-137">8</span><span class="sxs-lookup"><span data-stu-id="14bf3-137">8</span></span>      | <span data-ttu-id="14bf3-138">8</span><span class="sxs-lookup"><span data-stu-id="14bf3-138">8</span></span>      | <span data-ttu-id="14bf3-139">8</span><span class="sxs-lookup"><span data-stu-id="14bf3-139">8</span></span>      |        |
| <span data-ttu-id="14bf3-140">\_RGB10 GL</span><span class="sxs-lookup"><span data-stu-id="14bf3-140">GL\_RGB10</span></span>      | <span data-ttu-id="14bf3-141">RGB в формате GL \_</span><span class="sxs-lookup"><span data-stu-id="14bf3-141">GL\_RGB</span></span>     | <span data-ttu-id="14bf3-142">10</span><span class="sxs-lookup"><span data-stu-id="14bf3-142">10</span></span>     | <span data-ttu-id="14bf3-143">10</span><span class="sxs-lookup"><span data-stu-id="14bf3-143">10</span></span>     | <span data-ttu-id="14bf3-144">10</span><span class="sxs-lookup"><span data-stu-id="14bf3-144">10</span></span>     |        |
| <span data-ttu-id="14bf3-145">\_RGB12 GL</span><span class="sxs-lookup"><span data-stu-id="14bf3-145">GL\_RGB12</span></span>      | <span data-ttu-id="14bf3-146">RGB в формате GL \_</span><span class="sxs-lookup"><span data-stu-id="14bf3-146">GL\_RGB</span></span>     | <span data-ttu-id="14bf3-147">12</span><span class="sxs-lookup"><span data-stu-id="14bf3-147">12</span></span>     | <span data-ttu-id="14bf3-148">12</span><span class="sxs-lookup"><span data-stu-id="14bf3-148">12</span></span>     | <span data-ttu-id="14bf3-149">12</span><span class="sxs-lookup"><span data-stu-id="14bf3-149">12</span></span>     |        |
| <span data-ttu-id="14bf3-150">\_RGB16 GL</span><span class="sxs-lookup"><span data-stu-id="14bf3-150">GL\_RGB16</span></span>      | <span data-ttu-id="14bf3-151">RGB в формате GL \_</span><span class="sxs-lookup"><span data-stu-id="14bf3-151">GL\_RGB</span></span>     | <span data-ttu-id="14bf3-152">16</span><span class="sxs-lookup"><span data-stu-id="14bf3-152">16</span></span>     | <span data-ttu-id="14bf3-153">16</span><span class="sxs-lookup"><span data-stu-id="14bf3-153">16</span></span>     | <span data-ttu-id="14bf3-154">16</span><span class="sxs-lookup"><span data-stu-id="14bf3-154">16</span></span>     |        |
| <span data-ttu-id="14bf3-155">\_RGBA2 GL</span><span class="sxs-lookup"><span data-stu-id="14bf3-155">GL\_RGBA2</span></span>      | <span data-ttu-id="14bf3-156">RGBA для GL \_</span><span class="sxs-lookup"><span data-stu-id="14bf3-156">GL\_RGBA</span></span>    | <span data-ttu-id="14bf3-157">2</span><span class="sxs-lookup"><span data-stu-id="14bf3-157">2</span></span>      | <span data-ttu-id="14bf3-158">2</span><span class="sxs-lookup"><span data-stu-id="14bf3-158">2</span></span>      | <span data-ttu-id="14bf3-159">2</span><span class="sxs-lookup"><span data-stu-id="14bf3-159">2</span></span>      | <span data-ttu-id="14bf3-160">2</span><span class="sxs-lookup"><span data-stu-id="14bf3-160">2</span></span>      |
| <span data-ttu-id="14bf3-161">\_RGBA4 GL</span><span class="sxs-lookup"><span data-stu-id="14bf3-161">GL\_RGBA4</span></span>      | <span data-ttu-id="14bf3-162">RGBA для GL \_</span><span class="sxs-lookup"><span data-stu-id="14bf3-162">GL\_RGBA</span></span>    | <span data-ttu-id="14bf3-163">4</span><span class="sxs-lookup"><span data-stu-id="14bf3-163">4</span></span>      | <span data-ttu-id="14bf3-164">4</span><span class="sxs-lookup"><span data-stu-id="14bf3-164">4</span></span>      | <span data-ttu-id="14bf3-165">4</span><span class="sxs-lookup"><span data-stu-id="14bf3-165">4</span></span>      | <span data-ttu-id="14bf3-166">4</span><span class="sxs-lookup"><span data-stu-id="14bf3-166">4</span></span>      |
| <span data-ttu-id="14bf3-167">GL \_ RGB5 \_ a1</span><span class="sxs-lookup"><span data-stu-id="14bf3-167">GL\_RGB5\_A1</span></span>   | <span data-ttu-id="14bf3-168">RGBA для GL \_</span><span class="sxs-lookup"><span data-stu-id="14bf3-168">GL\_RGBA</span></span>    | <span data-ttu-id="14bf3-169">5</span><span class="sxs-lookup"><span data-stu-id="14bf3-169">5</span></span>      | <span data-ttu-id="14bf3-170">5</span><span class="sxs-lookup"><span data-stu-id="14bf3-170">5</span></span>      | <span data-ttu-id="14bf3-171">5</span><span class="sxs-lookup"><span data-stu-id="14bf3-171">5</span></span>      | <span data-ttu-id="14bf3-172">1</span><span class="sxs-lookup"><span data-stu-id="14bf3-172">1</span></span>      |
| <span data-ttu-id="14bf3-173">\_RGBA8 GL</span><span class="sxs-lookup"><span data-stu-id="14bf3-173">GL\_RGBA8</span></span>      | <span data-ttu-id="14bf3-174">RGBA для GL \_</span><span class="sxs-lookup"><span data-stu-id="14bf3-174">GL\_RGBA</span></span>    | <span data-ttu-id="14bf3-175">8</span><span class="sxs-lookup"><span data-stu-id="14bf3-175">8</span></span>      | <span data-ttu-id="14bf3-176">8</span><span class="sxs-lookup"><span data-stu-id="14bf3-176">8</span></span>      | <span data-ttu-id="14bf3-177">8</span><span class="sxs-lookup"><span data-stu-id="14bf3-177">8</span></span>      | <span data-ttu-id="14bf3-178">8</span><span class="sxs-lookup"><span data-stu-id="14bf3-178">8</span></span>      |
| <span data-ttu-id="14bf3-179">GL \_ RG10 \_ a2</span><span class="sxs-lookup"><span data-stu-id="14bf3-179">GL\_RG10\_A2</span></span>   | <span data-ttu-id="14bf3-180">RGBA для GL \_</span><span class="sxs-lookup"><span data-stu-id="14bf3-180">GL\_RGBA</span></span>    | <span data-ttu-id="14bf3-181">10</span><span class="sxs-lookup"><span data-stu-id="14bf3-181">10</span></span>     | <span data-ttu-id="14bf3-182">10</span><span class="sxs-lookup"><span data-stu-id="14bf3-182">10</span></span>     | <span data-ttu-id="14bf3-183">10</span><span class="sxs-lookup"><span data-stu-id="14bf3-183">10</span></span>     | <span data-ttu-id="14bf3-184">2</span><span class="sxs-lookup"><span data-stu-id="14bf3-184">2</span></span>      |
| <span data-ttu-id="14bf3-185">\_RGB12 GL</span><span class="sxs-lookup"><span data-stu-id="14bf3-185">GL\_RGB12</span></span>      | <span data-ttu-id="14bf3-186">RGBA для GL \_</span><span class="sxs-lookup"><span data-stu-id="14bf3-186">GL\_RGBA</span></span>    | <span data-ttu-id="14bf3-187">12</span><span class="sxs-lookup"><span data-stu-id="14bf3-187">12</span></span>     | <span data-ttu-id="14bf3-188">12</span><span class="sxs-lookup"><span data-stu-id="14bf3-188">12</span></span>     | <span data-ttu-id="14bf3-189">12</span><span class="sxs-lookup"><span data-stu-id="14bf3-189">12</span></span>     | <span data-ttu-id="14bf3-190">12</span><span class="sxs-lookup"><span data-stu-id="14bf3-190">12</span></span>     |
| <span data-ttu-id="14bf3-191">\_RGBA16 GL</span><span class="sxs-lookup"><span data-stu-id="14bf3-191">GL\_RGBA16</span></span>     | <span data-ttu-id="14bf3-192">RGBA для GL \_</span><span class="sxs-lookup"><span data-stu-id="14bf3-192">GL\_RGBA</span></span>    | <span data-ttu-id="14bf3-193">16</span><span class="sxs-lookup"><span data-stu-id="14bf3-193">16</span></span>     | <span data-ttu-id="14bf3-194">16</span><span class="sxs-lookup"><span data-stu-id="14bf3-194">16</span></span>     | <span data-ttu-id="14bf3-195">16</span><span class="sxs-lookup"><span data-stu-id="14bf3-195">16</span></span>     | <span data-ttu-id="14bf3-196">16</span><span class="sxs-lookup"><span data-stu-id="14bf3-196">16</span></span>     |



 

</dd> <dt>

<span data-ttu-id="14bf3-197">*width*</span><span class="sxs-lookup"><span data-stu-id="14bf3-197">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="14bf3-198">Размер палитры.</span><span class="sxs-lookup"><span data-stu-id="14bf3-198">The size of the palette.</span></span> <span data-ttu-id="14bf3-199">Для некоторого целого числа *n* должно быть 2n = 1.</span><span class="sxs-lookup"><span data-stu-id="14bf3-199">Must be 2n = 1 for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="14bf3-200">*format*</span><span class="sxs-lookup"><span data-stu-id="14bf3-200">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="14bf3-201">Формат точечных данных.</span><span class="sxs-lookup"><span data-stu-id="14bf3-201">The format of the pixel data.</span></span> <span data-ttu-id="14bf3-202">Допустимы следующие символьные константы.</span><span class="sxs-lookup"><span data-stu-id="14bf3-202">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="14bf3-203">Значение</span><span class="sxs-lookup"><span data-stu-id="14bf3-203">Value</span></span></th>
<th><span data-ttu-id="14bf3-204">Значение</span><span class="sxs-lookup"><span data-stu-id="14bf3-204">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="14bf3-205"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14bf3-205"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="14bf3-206">Каждый пиксель — это группа из четырех компонентов в следующем порядке: красный, зеленый, синий, альфа.</span><span class="sxs-lookup"><span data-stu-id="14bf3-206">Each pixel is a group of four components in this order: red, green, blue, alpha.</span></span> <span data-ttu-id="14bf3-207">Формат RGBA определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="14bf3-207">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="14bf3-208">Функция <strong>глколортабликст</strong> преобразует значения с плавающей запятой непосредственно во внутренний формат с неуказанной точностью.</span><span class="sxs-lookup"><span data-stu-id="14bf3-208">The <strong>glColorTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="14bf3-209">Целочисленные значения со знаком сопоставляются по внутреннему формату, так что наиболее положительное целочисленное значение, которое можно отобразить, сопоставляется с 1,0, а наиболее отрицательное целочисленное значение — в-1,0.</span><span class="sxs-lookup"><span data-stu-id="14bf3-209">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable integer value maps to -1.0.</span></span> <span data-ttu-id="14bf3-210">Целочисленные данные без знака сопоставлены аналогичным образом: максимальное целочисленное значение сопоставляется с 1,0, а нулевое сопоставляется с 0,0.</span><span class="sxs-lookup"><span data-stu-id="14bf3-210">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="14bf3-211">Функция <strong>глколортабликст</strong> умножает результирующие значения цвета на GL_c_SCALE и добавляет их в GL_c_BIAS, где <em>c</em> — красный, зеленый, синий и альфа-канал для соответствующих компонентов цвета.</span><span class="sxs-lookup"><span data-stu-id="14bf3-211">The <strong>glColorTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="14bf3-212">Результаты записываются в диапазон [0, 1].</span><span class="sxs-lookup"><span data-stu-id="14bf3-212">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="14bf3-213">Если GL_MAP_COLOR имеет <strong>значение true</strong>, <strong>глколортабликст</strong> масштабирует каждый компонент цвета по размеру таблицы подстановки GL_PIXEL_MAP_c_TO_c, а затем заменяет компонент на значение, на которое он ссылается в этой таблице. <em>c</em> — R, G, B или A соответственно.</span><span class="sxs-lookup"><span data-stu-id="14bf3-213">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glColorTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="14bf3-214">Функция <strong>глколортабликст</strong> преобразует итоговые цвета RGBA в фрагменты, присоединяя текущую координату <em>z</em>-координаты и координаты текстуры к каждому пикселю, а затем присвоив координаты <em>x</em> и <em>y</em> для <em>n</em>-го фрагмента, такого как<em>x</em>?</span><span class="sxs-lookup"><span data-stu-id="14bf3-214">The <strong>glColorTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment such that<em>x</em>?</span></span><span data-ttu-id="14bf3-215"> = <em>Ширина</em> <em>x</em><sub>r</sub> + <em>n</em></span><span class="sxs-lookup"><span data-stu-id="14bf3-215"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="14bf3-216"><em></em>&?</span><span class="sxs-lookup"><span data-stu-id="14bf3-216"><em></em>y?</span></span><span data-ttu-id="14bf3-217"> = <em>y</em><sub></sub> +<em>n/Ширина</em></span><span class="sxs-lookup"><span data-stu-id="14bf3-217"> = <em>y</em><sub>r</sub> +<em>n / width</em></span></span><br/> <span data-ttu-id="14bf3-218">где (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) — Текущая разточечная координата.</span><span class="sxs-lookup"><span data-stu-id="14bf3-218">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="14bf3-219">Затем эти фрагменты пикселов обрабатываются так же, как фрагменты, созданные с помощью растровых точек, линий или многоугольников.</span><span class="sxs-lookup"><span data-stu-id="14bf3-219">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="14bf3-220">Функция <strong>глколортабликст</strong> применяет сопоставление текстур, туман и все операции фрагментов перед записью фрагментов в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="14bf3-220">The <strong>glColorTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="14bf3-221"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14bf3-221"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="14bf3-222">Каждый пиксель является одним красным компонентом.</span><span class="sxs-lookup"><span data-stu-id="14bf3-222">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="14bf3-223">Функция <strong>глколортабликст</strong> преобразует этот компонент во внутренний формат точно так же, как красный компонент в пикселе RGBA, а затем преобразует его в пиксель RGBA с зеленым и синим значением 0,0, а альфа-канал — в значение 1,0.</span><span class="sxs-lookup"><span data-stu-id="14bf3-223">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="14bf3-224">После этого преобразования пиксел обрабатывается так же, как если бы он был считан как пиксель RGBA.</span><span class="sxs-lookup"><span data-stu-id="14bf3-224">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="14bf3-225"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14bf3-225"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="14bf3-226">Каждый пиксель является одним зеленым компонентом.</span><span class="sxs-lookup"><span data-stu-id="14bf3-226">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="14bf3-227">Функция <strong>глколортабликст</strong> преобразует этот компонент во внутренний формат таким же образом, как и зеленый компонент в пиксельном виде, а затем преобразует его в пиксель RGBA с красным и синим значением в 0,0, а альфа-канал — в значение 1,0.</span><span class="sxs-lookup"><span data-stu-id="14bf3-227">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="14bf3-228">После этого преобразования пиксел обрабатывается так же, как если бы он был считан как пиксель RGBA.</span><span class="sxs-lookup"><span data-stu-id="14bf3-228">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="14bf3-229"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14bf3-229"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="14bf3-230">Каждый пиксель является одним синим компонентом.</span><span class="sxs-lookup"><span data-stu-id="14bf3-230">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="14bf3-231">Функция <strong>глколортабликст</strong> преобразует этот компонент во внутренний формат точно таким же образом, как и синий компонент в пикселе RGBA, а затем преобразует его в пиксель RGBA с красным и зеленым значением, равным 0,0, а альфа-канал — 1,0.</span><span class="sxs-lookup"><span data-stu-id="14bf3-231">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="14bf3-232">После этого преобразования пиксел обрабатывается так же, как если бы он был считан как пиксель RGBA.</span><span class="sxs-lookup"><span data-stu-id="14bf3-232">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="14bf3-233"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14bf3-233"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="14bf3-234">Каждый пиксель является одним компонентом альфа.</span><span class="sxs-lookup"><span data-stu-id="14bf3-234">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="14bf3-235">Функция <strong>глколортабликст</strong> преобразует этот компонент во внутренний формат точно так же, как альфа-компонент в пиксельном пикселе RGBA, а затем преобразует его в пиксель RGBA с красным, зеленым и синим установленным значением 0,0.</span><span class="sxs-lookup"><span data-stu-id="14bf3-235">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="14bf3-236">После этого преобразования пиксел обрабатывается так же, как если бы он был считан как пиксель RGBA.</span><span class="sxs-lookup"><span data-stu-id="14bf3-236">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="14bf3-237"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14bf3-237"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="14bf3-238">Каждый пиксель — это группа из трех компонентов в следующем порядке: красный, зеленый, синий.</span><span class="sxs-lookup"><span data-stu-id="14bf3-238">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="14bf3-239">Функция <strong>глколортабликст</strong> преобразует каждый компонент во внутренний формат точно так же, как красный, зеленый и синий компоненты на пиксель RGBA.</span><span class="sxs-lookup"><span data-stu-id="14bf3-239">The <strong>glColorTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="14bf3-240">Тройной цвет преобразуется в пиксель RGBA с альфа-составляющей, равным 1,0.</span><span class="sxs-lookup"><span data-stu-id="14bf3-240">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="14bf3-241">После этого преобразования пиксел обрабатывается так же, как если бы он был считан как пиксель RGBA.</span><span class="sxs-lookup"><span data-stu-id="14bf3-241">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="14bf3-242"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14bf3-242"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="14bf3-243">Каждый пиксель — это группа из трех компонентов в следующем порядке: синий, зеленый, красный.</span><span class="sxs-lookup"><span data-stu-id="14bf3-243">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="14bf3-244">GL_BGR_EXT предоставляет формат, соответствующий макету памяти, не зависящему от устройства Windows (DIB).</span><span class="sxs-lookup"><span data-stu-id="14bf3-244">GL_BGR_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="14bf3-245">Поэтому приложения могут использовать те же данные, что и вызовы функций Windows, и вызовы функций OpenGL Pixel.</span><span class="sxs-lookup"><span data-stu-id="14bf3-245">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="14bf3-246"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14bf3-246"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="14bf3-247">Каждый пиксель — это группа из четырех компонентов в следующем порядке: синий, зеленый, красный, альфа.</span><span class="sxs-lookup"><span data-stu-id="14bf3-247">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="14bf3-248">GL_BGRA_EXT предоставляет формат, соответствующий макету памяти, не зависящему от устройства Windows (DIB).</span><span class="sxs-lookup"><span data-stu-id="14bf3-248">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="14bf3-249">Поэтому приложения могут использовать те же данные, что и вызовы функций Windows, и вызовы функций OpenGL Pixel.</span><span class="sxs-lookup"><span data-stu-id="14bf3-249">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="14bf3-250">*type*</span><span class="sxs-lookup"><span data-stu-id="14bf3-250">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="14bf3-251">Тип данных для *данных*.</span><span class="sxs-lookup"><span data-stu-id="14bf3-251">The data type for *data*.</span></span> <span data-ttu-id="14bf3-252">Следующие символьные константы принимаются: Byte без знака, формат GL, неподписанный байт, формат GL, Short, GL без знака, GL \_ \_ \_ \_ \_ \_ \_ \_ \_ int и GL с \_ плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="14bf3-252">The following symbolic constants are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

<span data-ttu-id="14bf3-253">В следующей таблице приведены значения допустимых констант для параметра *типа* .</span><span class="sxs-lookup"><span data-stu-id="14bf3-253">The following table summarizes the meaning of the valid constants for the *type* parameter.</span></span>



| <span data-ttu-id="14bf3-254">Значение</span><span class="sxs-lookup"><span data-stu-id="14bf3-254">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="14bf3-255">Значение</span><span class="sxs-lookup"><span data-stu-id="14bf3-255">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="14bf3-256"><dt>**\_байт без знака GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14bf3-256"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="14bf3-257">8-разрядное целое число без знака</span><span class="sxs-lookup"><span data-stu-id="14bf3-257">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="14bf3-258"><dt>**\_байт GL**</dt></span><span class="sxs-lookup"><span data-stu-id="14bf3-258"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="14bf3-259">8-разрядное целое число со знаком</span><span class="sxs-lookup"><span data-stu-id="14bf3-259">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="14bf3-260"><dt>**\_ \_ сокращенный формат GL без знака**</dt></span><span class="sxs-lookup"><span data-stu-id="14bf3-260"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="14bf3-261">16-разрядное целое число без знака</span><span class="sxs-lookup"><span data-stu-id="14bf3-261">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="14bf3-262"><dt>**\_Краткая GL**</dt></span><span class="sxs-lookup"><span data-stu-id="14bf3-262"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="14bf3-263">16-разрядное целое число со знаком</span><span class="sxs-lookup"><span data-stu-id="14bf3-263">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="14bf3-264"><dt>**\_целое число без знака GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14bf3-264"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="14bf3-265">32-разрядное целое число без знака</span><span class="sxs-lookup"><span data-stu-id="14bf3-265">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="14bf3-266"><dt>**тип в GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14bf3-266"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="14bf3-267">32-разрядное целое число</span><span class="sxs-lookup"><span data-stu-id="14bf3-267">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="14bf3-268"><dt>**с \_ плавающей запятой**</dt></span><span class="sxs-lookup"><span data-stu-id="14bf3-268"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="14bf3-269">Число одинарной точности с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="14bf3-269">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="14bf3-270">*data*</span><span class="sxs-lookup"><span data-stu-id="14bf3-270">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="14bf3-271">Указатель на данные текстуры с палитрой.</span><span class="sxs-lookup"><span data-stu-id="14bf3-271">A pointer to the paletted texture data.</span></span> <span data-ttu-id="14bf3-272">Для записи палитры данные обрабатываются как отдельные пиксели в палитре одномерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="14bf3-272">The data is treated as single pixels of a 1-D texture palette entry for a palette entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14bf3-273">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14bf3-273">Return value</span></span>

<span data-ttu-id="14bf3-274">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="14bf3-274">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="14bf3-275">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="14bf3-275">Error codes</span></span>

<span data-ttu-id="14bf3-276">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="14bf3-276">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="14bf3-277">Имя</span><span class="sxs-lookup"><span data-stu-id="14bf3-277">Name</span></span>                                                                                                  | <span data-ttu-id="14bf3-278">Значение</span><span class="sxs-lookup"><span data-stu-id="14bf3-278">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="14bf3-279"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="14bf3-279"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="14bf3-280">значение *Width* было недопустимым целым числом.</span><span class="sxs-lookup"><span data-stu-id="14bf3-280">*width* was an invalid integer.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="14bf3-281"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="14bf3-281"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="14bf3-282">*целевой объект*, *интерналформат*, *Формат* или *тип* не являются допустимыми значениями.</span><span class="sxs-lookup"><span data-stu-id="14bf3-282">*target*, *internalFormat*, *format*, or *type* was not an accepted value.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="14bf3-283"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="14bf3-283"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="14bf3-284">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="14bf3-284">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="14bf3-285">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14bf3-285">Remarks</span></span>

<span data-ttu-id="14bf3-286">Палитры текстур определяются палитрой цветов и набором данных изображения, состоящим из индексов для цветовых записей палитры (таблица цветов).</span><span class="sxs-lookup"><span data-stu-id="14bf3-286">Paletted textures are defined with a palette of colors and a set of image data that is composed of indexes to color entries of a palette (a color table).</span></span>

<span data-ttu-id="14bf3-287">Функция **глколортабликст** задает палитру текстуры для целевой текстуры.</span><span class="sxs-lookup"><span data-stu-id="14bf3-287">The **glColorTableEXT** function specifies the texture palette of a targeted texture.</span></span> <span data-ttu-id="14bf3-288">Он принимает *данные* из памяти и преобразует данные так, как если бы каждая запись палитры была одиночным пикселем одномерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="14bf3-288">It takes the *data* from memory and converts the data as if each palette entry is a single pixel of a 1-D texture.</span></span> <span data-ttu-id="14bf3-289">Функция **глколортабликст** выполняет распаковку и преобразование данных и преобразует их во внутренний формат, который соответствует заданному *формату* максимально точно.</span><span class="sxs-lookup"><span data-stu-id="14bf3-289">The **glColorTableEXT** function unpacks and converts the data and translates it into an internal format that matches the given *format* as closely as possible.</span></span>

<span data-ttu-id="14bf3-290">Если *Ширина* палитры больше, чем диапазон индексов цветов в данных текстуры, некоторые записи в палитре не используются.</span><span class="sxs-lookup"><span data-stu-id="14bf3-290">If a palette's *width* is greater than the range of the color indexes in the texture data, some of the palette entries are unused.</span></span> <span data-ttu-id="14bf3-291">Если *Ширина* палитры меньше, чем диапазон индексов цветов в данных текстуры, наиболее значимые биты данных текстуры игнорируются, и при доступе к палитре используются только соответствующие количество битов в индексе.</span><span class="sxs-lookup"><span data-stu-id="14bf3-291">If a palette's *width* is less than the range of the color indexes in the texture data, the most significant bits of the texture data are ignored and only the appropriate number of bits in the index are used when accessing the palette.</span></span> <span data-ttu-id="14bf3-292">При указании *целевого объекта* прокси с помощью текстуры прокси-сервера \_ \_ 1d или \_ 2D-текстуры \_ на палитре текстуры будет изменен размер, а ее параметры задаются, но данные не передаются или к которым осуществляется доступ.</span><span class="sxs-lookup"><span data-stu-id="14bf3-292">When you specify a proxy *target* using PROXY\_TEXTURE\_1D or PROXY\_TEXTURE\_2D, the palette of the proxy texture is resized and its parameters are set but no data is transferred or accessed.</span></span>

<span data-ttu-id="14bf3-293">Если параметр *Target* имеет значение \_ текстуры прокси-сервера \_ 1d или 2D-текстура \_ ГК \_ \_ \_ , а реализация не поддерживает значения, указанные для *формата* или *ширины*, **глколортабликст** может не создать запрошенную таблицу цветов.</span><span class="sxs-lookup"><span data-stu-id="14bf3-293">When the *target* parameter is GL\_PROXY\_TEXTURE\_1D or GL\_PROXY\_TEXTURE\_2D, and the implementation does not support the values specified for either *format* or *width*, **glColorTableEXT** can fail to create the requested color table.</span></span> <span data-ttu-id="14bf3-294">В этом случае таблица цветов пуста, и все полученные параметры будут равны нулю.</span><span class="sxs-lookup"><span data-stu-id="14bf3-294">In this case, the color table is empty and all parameters retrieved will be zero.</span></span> <span data-ttu-id="14bf3-295">Можно определить, поддерживает ли OpenGL определенный формат и размер цветовой таблицы, вызвав **глколортабликст** с целевым объектом-посредником, а затем вызвав [**глжетколортаблепараметеривекст**](glgetcolortableparameterivext.md) или [**глжетколортаблепараметерфвекст**](glgetcolortableparameterfvext.md) , чтобы определить, совпадает ли параметр Width, заданный **глколортабликст**.</span><span class="sxs-lookup"><span data-stu-id="14bf3-295">You can determine whether OpenGL supports a particular color table format and size by calling **glColorTableEXT** with a proxy target, and then calling [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) or [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) to determine whether the width parameter matches that set by **glColorTableEXT**.</span></span> <span data-ttu-id="14bf3-296">Если полученная ширина равна нулю, запрос на таблицу цветов с помощью **глколортабле** не выполнен.</span><span class="sxs-lookup"><span data-stu-id="14bf3-296">If the retrieved width is zero, the color table request by **glColorTable** failed.</span></span> <span data-ttu-id="14bf3-297">Если полученная ширина не равна нулю, можно вызвать **глколортабле** с реальной целью с текстурой \_ 1d или 2D-текстурой, \_ чтобы задать таблицу цветов.</span><span class="sxs-lookup"><span data-stu-id="14bf3-297">If the retrieved width is not zero, you can call **glColorTable** with the real target with TEXTURE\_1D or TEXTURE\_2D to set the color table.</span></span>

> [!Note]  
> <span data-ttu-id="14bf3-298">Функция **глколортабликст** — это функция расширения, которая не является частью стандартной библиотеки OpenGL, но является частью расширения текстуры с помощью \_ палитры типа "Расш \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="14bf3-298">The **glColorTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="14bf3-299">Чтобы проверить, поддерживает ли ваша реализация OpenGL **глколортабликст**, вызовите [**глжетстринг**](glgetstring.md)( \_ расширения GL).</span><span class="sxs-lookup"><span data-stu-id="14bf3-299">To check whether your implementation of OpenGL supports **glColorTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="14bf3-300">Если он возвращает \_ \_ текстуру с Многоцветовой палитрой GL \_ , поддерживается **глколортабликст** .</span><span class="sxs-lookup"><span data-stu-id="14bf3-300">If it returns GL\_EXT\_paletted\_texture, **glColorTableEXT** is supported.</span></span> <span data-ttu-id="14bf3-301">Чтобы получить адрес функции расширения, вызовите [**вглжетпрокаддресс**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="14bf3-301">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

 

<span data-ttu-id="14bf3-302">Для получения фактических данных таблицы цветов, указанных функцией **глколортабликст** , вызовите [**глжетколортабликст**](glgetcolortableext.md).</span><span class="sxs-lookup"><span data-stu-id="14bf3-302">To retrieve the actual color table data specified by the **glColorTableEXT** function, call [**glGetColorTableEXT**](glgetcolortableext.md).</span></span> <span data-ttu-id="14bf3-303">Чтобы получить параметры, такие как *Ширина* и *Формат* таблицы цветов, указанной функцией **Глколортабликст** , вызовите функцию **глжетколортаблепараметеривекст** или **глжетколортаблепараметерфвекст** .</span><span class="sxs-lookup"><span data-stu-id="14bf3-303">To retrieve the parameters, such as *width* and *format*, of the color table specified by the **glColorTableEXT** function, call the **glGetColorTableParameterivEXT** or **glGetColorTableParameterfvEXT** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="14bf3-304">Требования</span><span class="sxs-lookup"><span data-stu-id="14bf3-304">Requirements</span></span>



| <span data-ttu-id="14bf3-305">Требование</span><span class="sxs-lookup"><span data-stu-id="14bf3-305">Requirement</span></span> | <span data-ttu-id="14bf3-306">Значение</span><span class="sxs-lookup"><span data-stu-id="14bf3-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="14bf3-307">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14bf3-307">Minimum supported client</span></span><br/> | <span data-ttu-id="14bf3-308">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="14bf3-308">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="14bf3-309">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14bf3-309">Minimum supported server</span></span><br/> | <span data-ttu-id="14bf3-310">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="14bf3-310">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="14bf3-311">Заголовок</span><span class="sxs-lookup"><span data-stu-id="14bf3-311">Header</span></span><br/>                   | <dl> <span data-ttu-id="14bf3-312"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="14bf3-312"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14bf3-313">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14bf3-313">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14bf3-314">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="14bf3-314">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="14bf3-315">**глколорсубтабликст**</span><span class="sxs-lookup"><span data-stu-id="14bf3-315">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="14bf3-316">**гленд**</span><span class="sxs-lookup"><span data-stu-id="14bf3-316">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="14bf3-317">**глжетколортабликст**</span><span class="sxs-lookup"><span data-stu-id="14bf3-317">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="14bf3-318">**глжетколортаблепараметерфвекст**</span><span class="sxs-lookup"><span data-stu-id="14bf3-318">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="14bf3-319">**глжетколортаблепараметеривекст**</span><span class="sxs-lookup"><span data-stu-id="14bf3-319">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="14bf3-320">**вглжетпрокаддресс**</span><span class="sxs-lookup"><span data-stu-id="14bf3-320">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





