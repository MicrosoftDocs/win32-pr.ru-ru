---
title: Функция Глпикселмапуив (GL. h)
description: Функция Глпикселмапуив устанавливает карты перемещения пикселей.
ms.assetid: dd0f7881-fdd1-49c2-b68c-21e2f9e5ecd2
keywords:
- Функция Глпикселмапуив OpenGL
topic_type:
- apiref
api_name:
- glPixelMapuiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e9b31398060e62fa14cd35afe4f8536dd78f963
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988785"
---
# <a name="glpixelmapuiv-function"></a><span data-ttu-id="39887-104">Функция Глпикселмапуив</span><span class="sxs-lookup"><span data-stu-id="39887-104">glPixelMapuiv function</span></span>

<span data-ttu-id="39887-105">Функция **глпикселмапуив** устанавливает карты перемещения пикселей.</span><span class="sxs-lookup"><span data-stu-id="39887-105">The **glPixelMapuiv** function sets up pixel transfer maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="39887-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39887-106">Syntax</span></span>


```C++
void WINAPI glPixelMapuiv(
         GLenum  map,
         GLsizei mapsize,
   const GLuint  *values
);
```



## <a name="parameters"></a><span data-ttu-id="39887-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="39887-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39887-108">*map*</span><span class="sxs-lookup"><span data-stu-id="39887-108">*map*</span></span> 
</dt> <dd>

<span data-ttu-id="39887-109">Имя символьной таблицы.</span><span class="sxs-lookup"><span data-stu-id="39887-109">A symbolic map name.</span></span> <span data-ttu-id="39887-110">Ниже приведены десять карт.</span><span class="sxs-lookup"><span data-stu-id="39887-110">The ten maps are as follows.</span></span>



| <span data-ttu-id="39887-111">Значение</span><span class="sxs-lookup"><span data-stu-id="39887-111">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="39887-112">Значение</span><span class="sxs-lookup"><span data-stu-id="39887-112">Meaning</span></span>                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="GL_PIXEL_MAP_I_TO_I"></span><span id="gl_pixel_map_i_to_i"></span><dl> <span data-ttu-id="39887-113"><dt>**\_ \_ таблица с 1 \_ \_ по схеме \_ в ГК**</dt></span><span class="sxs-lookup"><span data-stu-id="39887-113"><dt>**GL\_PIXEL\_MAP\_I\_TO\_I**</dt></span></span> </dl> | <span data-ttu-id="39887-114">Сопоставляет цветовые индексы с цветными индексами.</span><span class="sxs-lookup"><span data-stu-id="39887-114">Maps color indexes to color indexes.</span></span><br/>       |
| <span id="GL_PIXEL_MAP_S_TO_S"></span><span id="gl_pixel_map_s_to_s"></span><dl> <span data-ttu-id="39887-115"><dt>**\_таблица с \_ 1 \_ \_ по в \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="39887-115"><dt>**GL\_PIXEL\_MAP\_S\_TO\_S**</dt></span></span> </dl> | <span data-ttu-id="39887-116">Сопоставляет индексы наборов элементов с индексами набора элементов.</span><span class="sxs-lookup"><span data-stu-id="39887-116">Maps stencil indexes to stencil indexes.</span></span><br/>   |
| <span id="GL_PIXEL_MAP_I_TO_R"></span><span id="gl_pixel_map_i_to_r"></span><dl> <span data-ttu-id="39887-117"><dt>**\_таблица с \_ 1 \_ по в главной таблице I \_ на \_ R**</dt></span><span class="sxs-lookup"><span data-stu-id="39887-117"><dt>**GL\_PIXEL\_MAP\_I\_TO\_R**</dt></span></span> </dl> | <span data-ttu-id="39887-118">Сопоставляет цветовые индексы с красными компонентами.</span><span class="sxs-lookup"><span data-stu-id="39887-118">Maps color indexes to red components.</span></span><br/>      |
| <span id="GL_PIXEL_MAP_I_TO_G"></span><span id="gl_pixel_map_i_to_g"></span><dl> <span data-ttu-id="39887-119"><dt>**\_ \_ таблица с 1 \_ \_ по схеме \_ в ГК**</dt></span><span class="sxs-lookup"><span data-stu-id="39887-119"><dt>**GL\_PIXEL\_MAP\_I\_TO\_G**</dt></span></span> </dl> | <span data-ttu-id="39887-120">Сопоставляет цветовые индексы с зелеными компонентами.</span><span class="sxs-lookup"><span data-stu-id="39887-120">Maps color indexes to green components.</span></span><br/>    |
| <span id="GL_PIXEL_MAP_I_TO_B"></span><span id="gl_pixel_map_i_to_b"></span><dl> <span data-ttu-id="39887-121"><dt>**\_таблица с \_ 1 \_ по в главной таблице I \_ на \_ B**</dt></span><span class="sxs-lookup"><span data-stu-id="39887-121"><dt>**GL\_PIXEL\_MAP\_I\_TO\_B**</dt></span></span> </dl> | <span data-ttu-id="39887-122">Сопоставляет цветные индексы с голубыми компонентами.</span><span class="sxs-lookup"><span data-stu-id="39887-122">Maps color indexes to blue components.</span></span><br/>     |
| <span id="GL_PIXEL_MAP_I_TO_A"></span><span id="gl_pixel_map_i_to_a"></span><dl> <span data-ttu-id="39887-123"><dt>**GL \_ \_ по схеме пикселей \_ I \_ в \_**</dt></span><span class="sxs-lookup"><span data-stu-id="39887-123"><dt>**GL\_PIXEL\_MAP\_I\_TO\_A**</dt></span></span> </dl> | <span data-ttu-id="39887-124">Сопоставляет цветовые индексы с альфа-компонентами.</span><span class="sxs-lookup"><span data-stu-id="39887-124">Maps color indexes to alpha components.</span></span><br/>    |
| <span id="GL_PIXEL_MAP_R_TO_R"></span><span id="gl_pixel_map_r_to_r"></span><dl> <span data-ttu-id="39887-125"><dt>**\_ \_ схема по схеме \_ в 1 пиксель \_ на \_ r**</dt></span><span class="sxs-lookup"><span data-stu-id="39887-125"><dt>**GL\_PIXEL\_MAP\_R\_TO\_R**</dt></span></span> </dl> | <span data-ttu-id="39887-126">Сопоставляет красные компоненты с красными компонентами.</span><span class="sxs-lookup"><span data-stu-id="39887-126">Maps red components to red components.</span></span><br/>     |
| <span id="GL_PIXEL_MAP_G_TO_G"></span><span id="gl_pixel_map_g_to_g"></span><dl> <span data-ttu-id="39887-127"><dt>**\_ \_ таблица с картой \_ \_ по g \_ в ГК**</dt></span><span class="sxs-lookup"><span data-stu-id="39887-127"><dt>**GL\_PIXEL\_MAP\_G\_TO\_G**</dt></span></span> </dl> | <span data-ttu-id="39887-128">Сопоставляет зеленые компоненты с зелеными компонентами.</span><span class="sxs-lookup"><span data-stu-id="39887-128">Maps green components to green components.</span></span><br/> |
| <span id="GL_PIXEL_MAP_B_TO_B"></span><span id="gl_pixel_map_b_to_b"></span><dl> <span data-ttu-id="39887-129"><dt>**\_схема "b" в главной точке \_ \_ \_ на \_ b**</dt></span><span class="sxs-lookup"><span data-stu-id="39887-129"><dt>**GL\_PIXEL\_MAP\_B\_TO\_B**</dt></span></span> </dl> | <span data-ttu-id="39887-130">Сопоставляет синие компоненты с голубыми компонентами.</span><span class="sxs-lookup"><span data-stu-id="39887-130">Maps blue components to blue components.</span></span><br/>   |
| <span id="GL_PIXEL_MAP_A_TO_A"></span><span id="gl_pixel_map_a_to_a"></span><dl> <span data-ttu-id="39887-131"><dt>**в \_ GL \_ пиксель \_ сопоставьте \_ a \_ с**</dt></span><span class="sxs-lookup"><span data-stu-id="39887-131"><dt>**GL\_PIXEL\_MAP\_A\_TO\_A**</dt></span></span> </dl> | <span data-ttu-id="39887-132">Сопоставляет альфа-компоненты с альфа-компонентами.</span><span class="sxs-lookup"><span data-stu-id="39887-132">Maps alpha components to alpha components.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="39887-133">*мапсизе*</span><span class="sxs-lookup"><span data-stu-id="39887-133">*mapsize*</span></span> 
</dt> <dd>

<span data-ttu-id="39887-134">Размер определяемой схемы.</span><span class="sxs-lookup"><span data-stu-id="39887-134">The size of the map being defined.</span></span>

</dd> <dt>

<span data-ttu-id="39887-135">*Значения*</span><span class="sxs-lookup"><span data-stu-id="39887-135">*values*</span></span> 
</dt> <dd>

<span data-ttu-id="39887-136">Массив значений *мапсизе* .</span><span class="sxs-lookup"><span data-stu-id="39887-136">An array of *mapsize* values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39887-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39887-137">Return value</span></span>

<span data-ttu-id="39887-138">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="39887-138">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="39887-139">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="39887-139">Error codes</span></span>

<span data-ttu-id="39887-140">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="39887-140">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="39887-141">Имя</span><span class="sxs-lookup"><span data-stu-id="39887-141">Name</span></span>                                                                                                  | <span data-ttu-id="39887-142">Значение</span><span class="sxs-lookup"><span data-stu-id="39887-142">Meaning</span></span>                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="39887-143"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="39887-143"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="39887-144">значение *Map* не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="39887-144">*map* was not an accepted value.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="39887-145"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="39887-145"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="39887-146">*мапсизе* был отрицательным или большим по сравнению с \_ \_ таблицей карт в формате GL \_ .</span><span class="sxs-lookup"><span data-stu-id="39887-146">*mapsize* was negative or larger than GL\_PIXEL\_MAP\_TABLE.</span></span> <br/>                                                                                                                                                   |
| <dl> <span data-ttu-id="39887-147"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="39887-147"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="39887-148">*Map* — это 1 \_ -я пиксельная схема, с i на 1, в главной таблице с s \_ \_ \_ \_ \_ \_ \_ \_ по \_ s, GL \_ пиксельных \_ карт \_ i \_ на \_ R, GL \_ x \_ Map \_ \_ с i по \_ G, GL \_ пиксельной \_ карте \_ i \_ в \_ B или GL \_ пиксельной \_ карте \_ i \_ в \_ , а *мапсизе* не является степенью двух.</span><span class="sxs-lookup"><span data-stu-id="39887-148">*map* was GL\_PIXEL\_MAP\_I\_TO\_I, GL\_PIXEL\_MAP\_S\_TO\_S, GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, or GL\_PIXEL\_MAP\_I\_TO\_A, and *mapsize* was not a power of two.</span></span> <br/> |
| <dl> <span data-ttu-id="39887-149"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="39887-149"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="39887-150">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="39887-150">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                                                                                     |



## <a name="remarks"></a><span data-ttu-id="39887-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39887-151">Remarks</span></span>

<span data-ttu-id="39887-152">Функция **глпикселмап** настраивает таблицы трансляции, или *сопоставления*, используемые [**глкопипикселс**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**глдравпикселс**](gldrawpixels.md), [**глреадпикселс**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)и [**glTexSubImage2D**](gltexsubimage2d.md).</span><span class="sxs-lookup"><span data-stu-id="39887-152">The **glPixelMap** function sets up translation tables, or *maps*, used by [**glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md), and [**glTexSubImage2D**](gltexsubimage2d.md).</span></span> <span data-ttu-id="39887-153">Использование этих сопоставлений описано полностью в разделе [**глпикселтрансфер**](glpixeltransfer.md) и частично в разделах, посвященных командам Image Pixel and текстуры.</span><span class="sxs-lookup"><span data-stu-id="39887-153">Use of these maps is described completely in the [**glPixelTransfer**](glpixeltransfer.md) topic, and partly in the topics for the pixel and texture image commands.</span></span> <span data-ttu-id="39887-154">В этом разделе описывается только спецификация карт.</span><span class="sxs-lookup"><span data-stu-id="39887-154">Only the specification of the maps is described in this topic.</span></span>

<span data-ttu-id="39887-155">Параметр *Map* — это имя символьной карты, указывающее один из десяти сопоставлений, которые нужно задать.</span><span class="sxs-lookup"><span data-stu-id="39887-155">The *map* parameter is a symbolic map name, indicating one of ten maps to set.</span></span> <span data-ttu-id="39887-156">Параметр *мапсизе* задает количество записей на карте, а *значения* — указатель на массив значений *мапсизе* Map.</span><span class="sxs-lookup"><span data-stu-id="39887-156">The *mapsize* parameter specifies the number of entries in the map, and *values* is a pointer to an array of *mapsize* map values.</span></span>

<span data-ttu-id="39887-157">Записи в сопоставлении могут быть указаны в виде чисел с плавающей запятой одиночной точности, коротких целых чисел без знака или длинных целых чисел без знака.</span><span class="sxs-lookup"><span data-stu-id="39887-157">The entries in a map can be specified as single-precision floating-point numbers, unsigned short integers, or unsigned long integers.</span></span> <span data-ttu-id="39887-158">Карты, в которых хранятся значения цветовых компонентов (все, кроме GL с \_ \_ сопоставлением 1 \_ и 1, а также в \_ \_ GL \_ пиксельных \_ карт \_ \_ \_ ), сохраняют свои значения в формате с плавающей запятой с неопределенным значением мантисса и размером экспоненты.</span><span class="sxs-lookup"><span data-stu-id="39887-158">Maps that store color component values (all but GL\_PIXEL\_MAP\_I\_TO\_I and GL\_PIXEL\_MAP\_S\_TO\_S) retain their values in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="39887-159">Значения с плавающей запятой, заданные [**глпикселмапфв**](glpixelmap.md) , преобразуются непосредственно во внутренний формат с плавающей запятой этих сопоставлений, а затем записываются в диапазон \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="39887-159">Floating-point values specified by [**glPixelMapfv**](glpixelmap.md) are converted directly to the internal floating-point format of these maps, and then clamped to the range \[0,1\].</span></span> <span data-ttu-id="39887-160">Целочисленные значения без знака, заданные **глпикселмапусв** и **глпикселмапуив** , преобразуются линейно таким, что максимальное представимое целое число сопоставляется с 1,0, а нулевое сопоставляется с 0,0.</span><span class="sxs-lookup"><span data-stu-id="39887-160">Unsigned integer values specified by **glPixelMapusv** and **glPixelMapuiv** are converted linearly such that the largest representable integer maps to 1.0, and zero maps to 0.0.</span></span>

<span data-ttu-id="39887-161">Карты, в которых хранятся индексы, GL с картой по схеме в формате "i" и "звезда" \_ \_ \_ \_ \_ \_ \_ , сопоставлены с s \_ \_ \_ , сохраняют свои значения в форматах с фиксированной запятой с неопределенным числом битов справа от двоичной точки.</span><span class="sxs-lookup"><span data-stu-id="39887-161">Maps that store indexes, GL\_PIXEL\_MAP\_I\_TO\_I and GL\_PIXEL\_MAP\_S\_TO\_S, retain their values in fixed-point format, with an unspecified number of bits to the right of the binary point.</span></span> <span data-ttu-id="39887-162">Значения с плавающей запятой, заданные [**глпикселмапфв**](glpixelmap.md) , преобразуются непосредственно во внутренний формат с фиксированной запятой этих сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="39887-162">Floating-point values specified by [**glPixelMapfv**](glpixelmap.md) are converted directly to the internal fixed-point format of these maps.</span></span> <span data-ttu-id="39887-163">Целочисленные значения без знака, заданные **глпикселмапусв** и **глпикселмапуив** , задают целочисленные значения, а все нули справа от двоичной точки.</span><span class="sxs-lookup"><span data-stu-id="39887-163">Unsigned integer values specified by **glPixelMapusv** and **glPixelMapuiv** specify integer values, with all zeros to the right of the binary point.</span></span>

<span data-ttu-id="39887-164">В следующей таблице показаны начальные размеры и значения для каждого из карт.</span><span class="sxs-lookup"><span data-stu-id="39887-164">The following table shows the initial sizes and values for each of the maps.</span></span> <span data-ttu-id="39887-165">Карты, индексируемые по цвету или индексам наборов элементов, должны иметь *мапсизе* = 2 ^ *n* для некоторых *n* или результаты не определены.</span><span class="sxs-lookup"><span data-stu-id="39887-165">Maps that are indexed by either color or stencil indexes must have *mapsize* = 2 ^ *n* for some *n* or results are undefined.</span></span> <span data-ttu-id="39887-166">Максимально допустимый размер для каждой схемы зависит от реализации и может быть определен путем вызова **глжет** с аргументом GL \_ Max \_ пиксельная \_ \_ Таблица карт.</span><span class="sxs-lookup"><span data-stu-id="39887-166">The maximum allowable size for each map depends on the implementation and can be determined by calling **glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE.</span></span> <span data-ttu-id="39887-167">Одно максимальное значение применяется ко всем картам и по крайней мере 32.</span><span class="sxs-lookup"><span data-stu-id="39887-167">The single maximum applies to all maps, and it is at least 32.</span></span>



| <span data-ttu-id="39887-168">Карта</span><span class="sxs-lookup"><span data-stu-id="39887-168">Map</span></span>                      | <span data-ttu-id="39887-169">Индекс уточняющего запроса</span><span class="sxs-lookup"><span data-stu-id="39887-169">Lookup Index</span></span>  | <span data-ttu-id="39887-170">Значение уточняющего запроса</span><span class="sxs-lookup"><span data-stu-id="39887-170">Lookup Value</span></span>  | <span data-ttu-id="39887-171">Начальный размер</span><span class="sxs-lookup"><span data-stu-id="39887-171">Initial Size</span></span> | <span data-ttu-id="39887-172">Начальное значение</span><span class="sxs-lookup"><span data-stu-id="39887-172">Initial Value</span></span> |
|--------------------------|---------------|---------------|--------------|---------------|
| <span data-ttu-id="39887-173">\_ \_ таблица с 1 \_ \_ по схеме \_ в ГК</span><span class="sxs-lookup"><span data-stu-id="39887-173">GL\_PIXEL\_MAP\_I\_TO\_I</span></span> | <span data-ttu-id="39887-174">цветовой индекс</span><span class="sxs-lookup"><span data-stu-id="39887-174">color index</span></span>   | <span data-ttu-id="39887-175">цветовой индекс</span><span class="sxs-lookup"><span data-stu-id="39887-175">color index</span></span>   | <span data-ttu-id="39887-176">1</span><span class="sxs-lookup"><span data-stu-id="39887-176">1</span></span>            | <span data-ttu-id="39887-177">0,0</span><span class="sxs-lookup"><span data-stu-id="39887-177">0.0</span></span>           |
| <span data-ttu-id="39887-178">\_таблица с \_ 1 \_ \_ по в \_ GL</span><span class="sxs-lookup"><span data-stu-id="39887-178">GL\_PIXEL\_MAP\_S\_TO\_S</span></span> | <span data-ttu-id="39887-179">индекс набора элементов</span><span class="sxs-lookup"><span data-stu-id="39887-179">stencil index</span></span> | <span data-ttu-id="39887-180">индекс набора элементов</span><span class="sxs-lookup"><span data-stu-id="39887-180">stencil index</span></span> | <span data-ttu-id="39887-181">1</span><span class="sxs-lookup"><span data-stu-id="39887-181">1</span></span>            | <span data-ttu-id="39887-182">0,0</span><span class="sxs-lookup"><span data-stu-id="39887-182">0.0</span></span>           |
| <span data-ttu-id="39887-183">\_таблица с \_ 1 \_ по в главной таблице I \_ на \_ R</span><span class="sxs-lookup"><span data-stu-id="39887-183">GL\_PIXEL\_MAP\_I\_TO\_R</span></span> | <span data-ttu-id="39887-184">цветовой индекс</span><span class="sxs-lookup"><span data-stu-id="39887-184">color index</span></span>   | <span data-ttu-id="39887-185">R</span><span class="sxs-lookup"><span data-stu-id="39887-185">R</span></span>             | <span data-ttu-id="39887-186">1</span><span class="sxs-lookup"><span data-stu-id="39887-186">1</span></span>            | <span data-ttu-id="39887-187">0,0</span><span class="sxs-lookup"><span data-stu-id="39887-187">0.0</span></span>           |
| <span data-ttu-id="39887-188">\_ \_ таблица с 1 \_ \_ по схеме \_ в ГК</span><span class="sxs-lookup"><span data-stu-id="39887-188">GL\_PIXEL\_MAP\_I\_TO\_G</span></span> | <span data-ttu-id="39887-189">цветовой индекс</span><span class="sxs-lookup"><span data-stu-id="39887-189">color index</span></span>   | <span data-ttu-id="39887-190">G</span><span class="sxs-lookup"><span data-stu-id="39887-190">G</span></span>             | <span data-ttu-id="39887-191">1</span><span class="sxs-lookup"><span data-stu-id="39887-191">1</span></span>            | <span data-ttu-id="39887-192">0,0</span><span class="sxs-lookup"><span data-stu-id="39887-192">0.0</span></span>           |
| <span data-ttu-id="39887-193">\_таблица с \_ 1 \_ по в главной таблице I \_ на \_ B</span><span class="sxs-lookup"><span data-stu-id="39887-193">GL\_PIXEL\_MAP\_I\_TO\_B</span></span> | <span data-ttu-id="39887-194">цветовой индекс</span><span class="sxs-lookup"><span data-stu-id="39887-194">color index</span></span>   | <span data-ttu-id="39887-195">B</span><span class="sxs-lookup"><span data-stu-id="39887-195">B</span></span>             | <span data-ttu-id="39887-196">1</span><span class="sxs-lookup"><span data-stu-id="39887-196">1</span></span>            | <span data-ttu-id="39887-197">0,0</span><span class="sxs-lookup"><span data-stu-id="39887-197">0.0</span></span>           |
| <span data-ttu-id="39887-198">GL \_ \_ по схеме пикселей \_ I \_ в \_</span><span class="sxs-lookup"><span data-stu-id="39887-198">GL\_PIXEL\_MAP\_I\_TO\_A</span></span> | <span data-ttu-id="39887-199">цветовой индекс</span><span class="sxs-lookup"><span data-stu-id="39887-199">color index</span></span>   | <span data-ttu-id="39887-200">Объект</span><span class="sxs-lookup"><span data-stu-id="39887-200">A</span></span>             | <span data-ttu-id="39887-201">1</span><span class="sxs-lookup"><span data-stu-id="39887-201">1</span></span>            | <span data-ttu-id="39887-202">0,0</span><span class="sxs-lookup"><span data-stu-id="39887-202">0.0</span></span>           |
| <span data-ttu-id="39887-203">\_ \_ схема по схеме \_ в 1 пиксель \_ на \_ r</span><span class="sxs-lookup"><span data-stu-id="39887-203">GL\_PIXEL\_MAP\_R\_TO\_R</span></span> | <span data-ttu-id="39887-204">R</span><span class="sxs-lookup"><span data-stu-id="39887-204">R</span></span>             | <span data-ttu-id="39887-205">R</span><span class="sxs-lookup"><span data-stu-id="39887-205">R</span></span>             | <span data-ttu-id="39887-206">1</span><span class="sxs-lookup"><span data-stu-id="39887-206">1</span></span>            | <span data-ttu-id="39887-207">0,0</span><span class="sxs-lookup"><span data-stu-id="39887-207">0.0</span></span>           |
| <span data-ttu-id="39887-208">\_ \_ таблица с картой \_ \_ по g \_ в ГК</span><span class="sxs-lookup"><span data-stu-id="39887-208">GL\_PIXEL\_MAP\_G\_TO\_G</span></span> | <span data-ttu-id="39887-209">G</span><span class="sxs-lookup"><span data-stu-id="39887-209">G</span></span>             | <span data-ttu-id="39887-210">G</span><span class="sxs-lookup"><span data-stu-id="39887-210">G</span></span>             | <span data-ttu-id="39887-211">1</span><span class="sxs-lookup"><span data-stu-id="39887-211">1</span></span>            | <span data-ttu-id="39887-212">0,0</span><span class="sxs-lookup"><span data-stu-id="39887-212">0.0</span></span>           |
| <span data-ttu-id="39887-213">\_схема "b" в главной точке \_ \_ \_ на \_ b</span><span class="sxs-lookup"><span data-stu-id="39887-213">GL\_PIXEL\_MAP\_B\_TO\_B</span></span> | <span data-ttu-id="39887-214">B</span><span class="sxs-lookup"><span data-stu-id="39887-214">B</span></span>             | <span data-ttu-id="39887-215">B</span><span class="sxs-lookup"><span data-stu-id="39887-215">B</span></span>             | <span data-ttu-id="39887-216">1</span><span class="sxs-lookup"><span data-stu-id="39887-216">1</span></span>            | <span data-ttu-id="39887-217">0,0</span><span class="sxs-lookup"><span data-stu-id="39887-217">0.0</span></span>           |
| <span data-ttu-id="39887-218">в \_ GL \_ пиксель \_ сопоставьте \_ a \_ с</span><span class="sxs-lookup"><span data-stu-id="39887-218">GL\_PIXEL\_MAP\_A\_TO\_A</span></span> | <span data-ttu-id="39887-219">Объект</span><span class="sxs-lookup"><span data-stu-id="39887-219">A</span></span>             | <span data-ttu-id="39887-220">Объект</span><span class="sxs-lookup"><span data-stu-id="39887-220">A</span></span>             | <span data-ttu-id="39887-221">1</span><span class="sxs-lookup"><span data-stu-id="39887-221">1</span></span>            | <span data-ttu-id="39887-222">0,0</span><span class="sxs-lookup"><span data-stu-id="39887-222">0.0</span></span>           |



 

<span data-ttu-id="39887-223">Следующие функции извлекают сведения, относящиеся к **глпикселмап**:</span><span class="sxs-lookup"><span data-stu-id="39887-223">The following functions retrieve information related to **glPixelMap**:</span></span>

<span data-ttu-id="39887-224">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ пиксель \_ Map \_ i \_ , \_ \_ Размер</span><span class="sxs-lookup"><span data-stu-id="39887-224">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PIXEL\_MAP\_I\_TO\_I\_SIZE</span></span>

<span data-ttu-id="39887-225">**глжет** с аргументом \_ GL \_ пиксель \_ Map \_ с \_ \_ размером s</span><span class="sxs-lookup"><span data-stu-id="39887-225">**glGet** with argument GL\_PIXEL\_MAP\_S\_TO\_S\_SIZE</span></span>

<span data-ttu-id="39887-226">**глжет** с аргументом \_ GL \_ пиксель \_ Map \_ с I на \_ R \_ size</span><span class="sxs-lookup"><span data-stu-id="39887-226">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_R\_SIZE</span></span>

<span data-ttu-id="39887-227">**глжет** с аргументом GL \_ пиксель \_ Map \_ I \_ на \_ G \_ size</span><span class="sxs-lookup"><span data-stu-id="39887-227">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_G\_SIZE</span></span>

<span data-ttu-id="39887-228">**глжет** с аргументом GL \_ пиксель \_ Map \_ I \_ на \_ B \_ size</span><span class="sxs-lookup"><span data-stu-id="39887-228">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_B\_SIZE</span></span>

<span data-ttu-id="39887-229">**глжет** с аргументом GL \_ пиксель \_ Map \_ I \_ на \_ \_ Размер</span><span class="sxs-lookup"><span data-stu-id="39887-229">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_A\_SIZE</span></span>

<span data-ttu-id="39887-230">**глжет** с аргументом GL \_ пиксель \_ Map \_ r \_ to \_ r \_ size</span><span class="sxs-lookup"><span data-stu-id="39887-230">**glGet** with argument GL\_PIXEL\_MAP\_R\_TO\_R\_SIZE</span></span>

<span data-ttu-id="39887-231">**глжет** с аргументом GL \_ пиксель \_ Map \_ g \_ к \_ g \_ size</span><span class="sxs-lookup"><span data-stu-id="39887-231">**glGet** with argument GL\_PIXEL\_MAP\_G\_TO\_G\_SIZE</span></span>

<span data-ttu-id="39887-232">**глжет** с аргументом GL \_ пиксель \_ Map \_ b \_ к \_ b \_ size</span><span class="sxs-lookup"><span data-stu-id="39887-232">**glGet** with argument GL\_PIXEL\_MAP\_B\_TO\_B\_SIZE</span></span>

<span data-ttu-id="39887-233">**глжет** с аргументом GL \_ пиксель \_ сопоставьте \_ a \_ с \_ \_ размером</span><span class="sxs-lookup"><span data-stu-id="39887-233">**glGet** with argument GL\_PIXEL\_MAP\_A\_TO\_A\_SIZE</span></span>

<span data-ttu-id="39887-234">**глжет** с аргументом GL \_ максимальный размер \_ \_ \_ таблицы карт</span><span class="sxs-lookup"><span data-stu-id="39887-234">**glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE</span></span>

## <a name="requirements"></a><span data-ttu-id="39887-235">Требования</span><span class="sxs-lookup"><span data-stu-id="39887-235">Requirements</span></span>



| <span data-ttu-id="39887-236">Требование</span><span class="sxs-lookup"><span data-stu-id="39887-236">Requirement</span></span> | <span data-ttu-id="39887-237">Значение</span><span class="sxs-lookup"><span data-stu-id="39887-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39887-238">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39887-238">Minimum supported client</span></span><br/> | <span data-ttu-id="39887-239">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="39887-239">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="39887-240">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39887-240">Minimum supported server</span></span><br/> | <span data-ttu-id="39887-241">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="39887-241">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="39887-242">Заголовок</span><span class="sxs-lookup"><span data-stu-id="39887-242">Header</span></span><br/>                   | <dl> <span data-ttu-id="39887-243"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="39887-243"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="39887-244">Библиотека</span><span class="sxs-lookup"><span data-stu-id="39887-244">Library</span></span><br/>                  | <dl> <span data-ttu-id="39887-245"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39887-245"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="39887-246">DLL</span><span class="sxs-lookup"><span data-stu-id="39887-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39887-247"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39887-247"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39887-248">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39887-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39887-249">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="39887-249">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="39887-250">**глкопипикселс**</span><span class="sxs-lookup"><span data-stu-id="39887-250">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="39887-251">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="39887-251">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="39887-252">**гленд**</span><span class="sxs-lookup"><span data-stu-id="39887-252">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="39887-253">**глпикселсторе**</span><span class="sxs-lookup"><span data-stu-id="39887-253">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="39887-254">**глпикселтрансфер**</span><span class="sxs-lookup"><span data-stu-id="39887-254">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="39887-255">**глреадпикселс**</span><span class="sxs-lookup"><span data-stu-id="39887-255">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="39887-256">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="39887-256">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="39887-257">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="39887-257">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





