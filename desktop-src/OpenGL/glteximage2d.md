---
title: Функция glTexImage2D (GL. h)
description: Функция glTexImage2D указывает изображение двухмерной текстуры.
ms.assetid: e8b9c692-5239-47de-86eb-80c247c60e1d
keywords:
- Функция glTexImage2D OpenGL
topic_type:
- apiref
api_name:
- glTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ba2d5bc6f966d9b10c0dadccb221086e64de827
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661995"
---
# <a name="glteximage2d-function"></a><span data-ttu-id="fefac-104">Функция glTexImage2D</span><span class="sxs-lookup"><span data-stu-id="fefac-104">glTexImage2D function</span></span>

<span data-ttu-id="fefac-105">Функция **glTexImage2D** указывает изображение двухмерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="fefac-105">The **glTexImage2D** function specifies a two-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="fefac-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fefac-106">Syntax</span></span>


```C++
void WINAPI glTexImage2D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLsizei height,
         GLint   border,
         GLint   format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="fefac-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fefac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fefac-108">*target*</span><span class="sxs-lookup"><span data-stu-id="fefac-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="fefac-109">Целевая текстура.</span><span class="sxs-lookup"><span data-stu-id="fefac-109">The target texture.</span></span> <span data-ttu-id="fefac-110">Должно быть \_ 2D-текстура GL \_ .</span><span class="sxs-lookup"><span data-stu-id="fefac-110">Must be GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="fefac-111">*level*</span><span class="sxs-lookup"><span data-stu-id="fefac-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="fefac-112">Номер уровня детализации.</span><span class="sxs-lookup"><span data-stu-id="fefac-112">The level-of-detail number.</span></span> <span data-ttu-id="fefac-113">Уровень 0 является базовым уровнем образа.</span><span class="sxs-lookup"><span data-stu-id="fefac-113">Level 0 is the base image level.</span></span> <span data-ttu-id="fefac-114">Уровень *n* — это *n* -ое изображение для сокращения mipmap.</span><span class="sxs-lookup"><span data-stu-id="fefac-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="fefac-115">*интерналформат*</span><span class="sxs-lookup"><span data-stu-id="fefac-115">*internalformat*</span></span> 
</dt> <dd>

<span data-ttu-id="fefac-116">Число компонентов цвета в текстуре.</span><span class="sxs-lookup"><span data-stu-id="fefac-116">The number of color components in the texture.</span></span> <span data-ttu-id="fefac-117">Значение должно быть равно 1, 2, 3 или 4 или одной из следующих символьных констант: GL \_ Alpha, GL \_ ALPHA4, GL \_ ALPHA8, GL \_ ALPHA12, GL \_ ALPHA16, \_ светимость GL, GL LUMINANCE4 \_ , GL \_ LUMINANCE8, GL \_ LUMINANCE12, GL \_ LUMINANCE16, GL \_ светимость \_ Alpha, GL LUMINANCE4 ALPHA4, GL LUMINANCE6 ALPHA2 \_ \_ \_ \_ , GL \_ LUMINANCE8 \_ ALPHA8, GL \_ LUMINANCE12 ALPHA4, \_ GL \_ LUMINANCE12 \_ ALPHA12, GL \_ LUMINANCE16 ALPHA16, ная \_ интенсивность GL, GL INTENSITY4 \_ \_ , GL \_ INTENSITY8, GL \_ INTENSITY12, GL \_ INTENSITY16, GL \_ R3 \_ G3 \_ B2, GL \_ RGB, GL RGB4, \_ GL \_ RGB5, GL \_ RGB8, GL RGB10, \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ GL RGB12, GL, ГК, GL RGB16 и GL RGBA2, GL RGBA4.</span><span class="sxs-lookup"><span data-stu-id="fefac-117">Must be 1, 2, 3, or 4, or one of the following symbolic constants: GL\_ALPHA, GL\_ALPHA4, GL\_ALPHA8, GL\_ALPHA12, GL\_ALPHA16, GL\_LUMINANCE, GL\_LUMINANCE4, GL\_LUMINANCE8, GL\_LUMINANCE12, GL\_LUMINANCE16, GL\_LUMINANCE\_ALPHA, GL\_LUMINANCE4\_ALPHA4, GL\_LUMINANCE6\_ALPHA2, GL\_LUMINANCE8\_ALPHA8, GL\_LUMINANCE12\_ALPHA4, GL\_LUMINANCE12\_ALPHA12, GL\_LUMINANCE16\_ALPHA16, GL\_INTENSITY, GL\_INTENSITY4, GL\_INTENSITY8, GL\_INTENSITY12, GL\_INTENSITY16, GL\_R3\_G3\_B2, GL\_RGB, GL\_RGB4, GL\_RGB5, GL\_RGB8, GL\_RGB10, GL\_RGB12, GL\_RGB16, GL\_RGBA, GL\_RGBA2, GL\_RGBA4, GL\_RGB5\_A1, GL\_RGBA8, GL\_RGB10\_A2, GL\_RGBA12, or GL\_RGBA16.</span></span>

</dd> <dt>

<span data-ttu-id="fefac-118">*width*</span><span class="sxs-lookup"><span data-stu-id="fefac-118">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="fefac-119">Ширина изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="fefac-119">The width of the texture image.</span></span> <span data-ttu-id="fefac-120">Значение должно быть 2 *n* + 2 (*border*) для некоторого целого числа *n*.</span><span class="sxs-lookup"><span data-stu-id="fefac-120">Must be 2 *n* + 2(*border*) for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="fefac-121">*height*</span><span class="sxs-lookup"><span data-stu-id="fefac-121">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="fefac-122">Высота изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="fefac-122">The height of the texture image.</span></span> <span data-ttu-id="fefac-123">Значение должно быть 2 *<sup>м</sup>* + 2 (*граница*) для некоторого целого числа *m*.</span><span class="sxs-lookup"><span data-stu-id="fefac-123">Must be 2 *<sup>m</sup>* + 2(*border*) for some integer *m*.</span></span>

</dd> <dt>

<span data-ttu-id="fefac-124">*цвета*</span><span class="sxs-lookup"><span data-stu-id="fefac-124">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="fefac-125">Ширина границы.</span><span class="sxs-lookup"><span data-stu-id="fefac-125">The width of the border.</span></span> <span data-ttu-id="fefac-126">Значение должно быть 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="fefac-126">Must be either 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="fefac-127">*format*</span><span class="sxs-lookup"><span data-stu-id="fefac-127">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="fefac-128">Формат точечных данных.</span><span class="sxs-lookup"><span data-stu-id="fefac-128">The format of the pixel data.</span></span> <span data-ttu-id="fefac-129">Можно предположить, что одно из девяти символьных значений.</span><span class="sxs-lookup"><span data-stu-id="fefac-129">It can assume one of nine symbolic values.</span></span>



| <span data-ttu-id="fefac-130">Значение</span><span class="sxs-lookup"><span data-stu-id="fefac-130">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="fefac-131">Значение</span><span class="sxs-lookup"><span data-stu-id="fefac-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="fefac-132"><dt>**\_индекс цвета \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-132"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="fefac-133">Каждый элемент — это одно значение, цветовой индекс.</span><span class="sxs-lookup"><span data-stu-id="fefac-133">Each element is a single value, a color index.</span></span> <span data-ttu-id="fefac-134">Он преобразуется в фиксированную точку (с неопределенным числом нулей справа от двоичной точки), сдвигая влево или вправо в зависимости от значения и знака смещения \_ индекса GL \_ и добавления к \_ \_ смещению индекса GL (см. [**глпикселтрансфер**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="fefac-134">It is converted to fixed point (with an unspecified number of 0 bits to the right of the binary point), shifted left or right depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="fefac-135">Полученный индекс преобразуется в набор цветовых компонентов, использующих \_ пиксельную карту GL i в R, GL в виде таблицы с i по G, GL в виде пикселя на B, а также в таблице GL с приведением к \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ диапазону \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="fefac-135">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="fefac-136"><dt>**\_красный GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-136"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="fefac-137">Каждый элемент является одним красным компонентом.</span><span class="sxs-lookup"><span data-stu-id="fefac-137">Each element is a single red component.</span></span> <span data-ttu-id="fefac-138">Он преобразуется в плавающую точку и собирается в элемент RGBA путем присоединения 0,0 для зеленого и синего и 1,0 для Alpha.</span><span class="sxs-lookup"><span data-stu-id="fefac-138">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="fefac-139">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. **глпикселтрансфер**).</span><span class="sxs-lookup"><span data-stu-id="fefac-139">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                               |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="fefac-140"><dt>**\_зеленый GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-140"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="fefac-141">Каждый элемент является одним зеленым компонентом.</span><span class="sxs-lookup"><span data-stu-id="fefac-141">Each element is a single green component.</span></span> <span data-ttu-id="fefac-142">Он преобразуется в плавающую точку и собирается в элемент RGBA путем присоединения 0,0 для красного и синего и 1,0 для Alpha.</span><span class="sxs-lookup"><span data-stu-id="fefac-142">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="fefac-143">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. [**глпикселтрансфер**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="fefac-143">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                        |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="fefac-144"><dt>**\_синяя GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-144"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="fefac-145">Каждый элемент является одним синим компонентом.</span><span class="sxs-lookup"><span data-stu-id="fefac-145">Each element is a single blue component.</span></span> <span data-ttu-id="fefac-146">Он преобразуется в плавающую точку и собирается в элемент RGBA путем присоединения 0,0 для красного и зеленого и 1,0 для Alpha.</span><span class="sxs-lookup"><span data-stu-id="fefac-146">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="fefac-147">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. **глпикселтрансфер**).</span><span class="sxs-lookup"><span data-stu-id="fefac-147">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                               |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="fefac-148"><dt>**\_альфа-канал GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-148"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="fefac-149">Каждый элемент является одним красным компонентом.</span><span class="sxs-lookup"><span data-stu-id="fefac-149">Each element is a single red component.</span></span> <span data-ttu-id="fefac-150">Он преобразуется в плавающую точку и собирается в элемент RGBA путем присоединения 0,0 для красного, зеленого и синего цветов.</span><span class="sxs-lookup"><span data-stu-id="fefac-150">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="fefac-151">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. [**глпикселтрансфер**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="fefac-151">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                     |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="fefac-152"><dt>**RGB в формате GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-152"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="fefac-153">Каждый элемент — это тройной RGB.</span><span class="sxs-lookup"><span data-stu-id="fefac-153">Each element is an RGB triple.</span></span> <span data-ttu-id="fefac-154">Он преобразуется в плавающую точку и собирается в элемент RGBA путем присоединения 1,0 для альфа.</span><span class="sxs-lookup"><span data-stu-id="fefac-154">It is converted to floating point and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="fefac-155">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. **глпикселтрансфер**).</span><span class="sxs-lookup"><span data-stu-id="fefac-155">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="fefac-156"><dt>**RGBA для GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-156"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="fefac-157">Каждый элемент является полным элементом RGBA.</span><span class="sxs-lookup"><span data-stu-id="fefac-157">Each element is a complete RGBA element.</span></span> <span data-ttu-id="fefac-158">Он преобразуется в тип с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="fefac-158">It is converted to floating point.</span></span> <span data-ttu-id="fefac-159">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. [**глпикселтрансфер**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="fefac-159">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="fefac-160"><dt>**\_BGRа \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-160"><dt>**GL\_BGR\_EXT**</dt></span></span> </dl>                         | <span data-ttu-id="fefac-161">Каждый пиксель — это группа из трех компонентов в следующем порядке: синий, зеленый, красный.</span><span class="sxs-lookup"><span data-stu-id="fefac-161">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="fefac-162">GL \_ BGR \_ ext предоставляет формат, соответствующий макету памяти, не зависящему от устройства Windows (DIB).</span><span class="sxs-lookup"><span data-stu-id="fefac-162">GL\_BGR\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="fefac-163">Поэтому приложения могут использовать те же данные, что и вызовы функций Windows, и вызовы функций OpenGL Pixel.</span><span class="sxs-lookup"><span data-stu-id="fefac-163">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="fefac-164"><dt>**\_BGRAа \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-164"><dt>**GL\_BGRA\_EXT**</dt></span></span> </dl>                      | <span data-ttu-id="fefac-165">Каждый пиксель — это группа из четырех компонентов в следующем порядке: синий, зеленый, красный, альфа.</span><span class="sxs-lookup"><span data-stu-id="fefac-165">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span> <span data-ttu-id="fefac-166">GL \_ BGRA \_ ext предоставляет формат, соответствующий макету памяти, не зависящему от устройства Windows (DIB).</span><span class="sxs-lookup"><span data-stu-id="fefac-166">GL\_BGRA\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="fefac-167">Поэтому приложения могут использовать те же данные, что и вызовы функций Windows, и вызовы функций OpenGL Pixel.</span><span class="sxs-lookup"><span data-stu-id="fefac-167">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="fefac-168"><dt>**\_светимость GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-168"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="fefac-169">Каждый элемент является одним значением светимости.</span><span class="sxs-lookup"><span data-stu-id="fefac-169">Each element is a single luminance value.</span></span> <span data-ttu-id="fefac-170">Он преобразуется в плавающую точку, а затем собирается в элемент RGBA путем репликации значения светимости три раза для красного, зеленого и синего и присоединения 1,0 для альфа.</span><span class="sxs-lookup"><span data-stu-id="fefac-170">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="fefac-171">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. **глпикселтрансфер**).</span><span class="sxs-lookup"><span data-stu-id="fefac-171">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                         |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="fefac-172"><dt>**\_ярко- \_ альфа-версия GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-172"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="fefac-173">Каждый элемент является парой светимости или альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="fefac-173">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="fefac-174">Он преобразуется в плавающую точку, а затем собирается в элемент RGBA путем репликации значения светимости три раза для красного, зеленого и синего.</span><span class="sxs-lookup"><span data-stu-id="fefac-174">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="fefac-175">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. [**глпикселтрансфер**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="fefac-175">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="fefac-176">*type*</span><span class="sxs-lookup"><span data-stu-id="fefac-176">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="fefac-177">Тип данных пикселя.</span><span class="sxs-lookup"><span data-stu-id="fefac-177">The data type of the pixel data.</span></span> <span data-ttu-id="fefac-178">Допустимы следующие символьные значения: \_ НЕподписанный \_ байт, байт GL, формат GL, формат GL \_ \_ \_ без знака \_ Short, краткое название GL \_ , \_ Неподписанное \_ целое число, значение GL \_ и тип \_ float.</span><span class="sxs-lookup"><span data-stu-id="fefac-178">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="fefac-179">*зависим*</span><span class="sxs-lookup"><span data-stu-id="fefac-179">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="fefac-180">Указатель на данные изображения в памяти.</span><span class="sxs-lookup"><span data-stu-id="fefac-180">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fefac-181">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fefac-181">Return value</span></span>

<span data-ttu-id="fefac-182">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="fefac-182">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fefac-183">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="fefac-183">Error codes</span></span>

<span data-ttu-id="fefac-184">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="fefac-184">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fefac-185">Имя</span><span class="sxs-lookup"><span data-stu-id="fefac-185">Name</span></span>                                                                                                  | <span data-ttu-id="fefac-186">Значение</span><span class="sxs-lookup"><span data-stu-id="fefac-186">Meaning</span></span>                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fefac-187"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-187"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="fefac-188">*целевой объект* не был \_ 2D-текстурой GL \_ .</span><span class="sxs-lookup"><span data-stu-id="fefac-188">*target* was not an GL\_TEXTURE\_2D.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="fefac-189"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-189"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="fefac-190">*Формат* не является допустимой константой *формата* .</span><span class="sxs-lookup"><span data-stu-id="fefac-190">*format* was not an accepted *format* constant.</span></span> <span data-ttu-id="fefac-191">Принимаются только константы формата \_ , отличные от индекса трафарета GL \_ и \_ компонента глубины GL \_ .</span><span class="sxs-lookup"><span data-stu-id="fefac-191">Only format constants other than GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT are accepted.</span></span> <span data-ttu-id="fefac-192">Список возможных значений см. в описании параметра *Format* .</span><span class="sxs-lookup"><span data-stu-id="fefac-192">See the parameter description of *format* for a list of possible values.</span></span><br/> |
| <dl> <span data-ttu-id="fefac-193"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-193"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="fefac-194">*тип* не является константой *типа* .</span><span class="sxs-lookup"><span data-stu-id="fefac-194">*type* was not a *type* constant.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="fefac-195"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-195"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="fefac-196">*тип* — это \_ точечный рисунок и *Формат* , отличный от \_ индекса цвета GL \_ .</span><span class="sxs-lookup"><span data-stu-id="fefac-196">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                        |
| <dl> <span data-ttu-id="fefac-197"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-197"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="fefac-198">*уровень* был меньше нуля или больше log2 *Max*, где *Max* было возвращено значение \_ максимального \_ размера текстуры GL \_ .</span><span class="sxs-lookup"><span data-stu-id="fefac-198">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="fefac-199"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="fefac-200">*интерналформат* не был равен 1, 2, 3 или 4.</span><span class="sxs-lookup"><span data-stu-id="fefac-200">*internalformat* was was not 1, 2, 3, or 4.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="fefac-201"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-201"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="fefac-202">*Ширина* или высота была меньше нуля или больше 2 + ГК \_ \_ для максимального размера текстуры \_ или не может быть представлена 2 *n* + 2 (Border) для некоторого целого значения *n*.</span><span class="sxs-lookup"><span data-stu-id="fefac-202">*width* or height was less than zero or greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or it could not be represented as 2 *n* + 2(border) for some integer value of *n*.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="fefac-203"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-203"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="fefac-204">*граница* не равна 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="fefac-204">*border* was not 0 or 1.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="fefac-205"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-205"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fefac-206">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="fefac-206">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                          |



## <a name="remarks"></a><span data-ttu-id="fefac-207">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fefac-207">Remarks</span></span>

<span data-ttu-id="fefac-208">Функция **glTexImage2D** указывает изображение двухмерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="fefac-208">The **glTexImage2D** function specifies a two-dimensional texture image.</span></span> <span data-ttu-id="fefac-209">Текстурирование сопоставляет часть указанного *изображения текстуры* с каждым графическим примитивом, для которого включено текстурирование.</span><span class="sxs-lookup"><span data-stu-id="fefac-209">Texturing maps a portion of a specified *texture image* onto each graphical primitive for which texturing is enabled.</span></span> <span data-ttu-id="fefac-210">Двухмерный текстурирование включается и отключается с помощью [**гленабле**](glenable.md) и **глдисабле** с аргументом GL \_ текстуры \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="fefac-210">Two-dimensional texturing is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_TEXTURE\_2D.</span></span>

<span data-ttu-id="fefac-211">Изображения текстуры определяются с помощью **glTexImage2D**.</span><span class="sxs-lookup"><span data-stu-id="fefac-211">Texture images are defined with **glTexImage2D**.</span></span> <span data-ttu-id="fefac-212">Аргументы описывают параметры изображения текстуры, такие как высота, ширина, ширина границы, номер уровня детализации (см. [**глтекспараметер**](gltexparameter-functions.md)) и число предоставленных компонентов цвета.</span><span class="sxs-lookup"><span data-stu-id="fefac-212">The arguments describe the parameters of the texture image, such as height, width, width of the border, level-of-detail number (see [**glTexParameter**](gltexparameter-functions.md)), and number of color components provided.</span></span> <span data-ttu-id="fefac-213">Последние три аргумента описывают способ представления изображения в памяти.</span><span class="sxs-lookup"><span data-stu-id="fefac-213">The last three arguments describe the way the image is represented in memory.</span></span> <span data-ttu-id="fefac-214">Эти аргументы идентичны форматам пикселей, используемым для [**глдравпикселс**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="fefac-214">These arguments are identical to the pixel formats used for [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="fefac-215">Данные считываются из *пикселей* в виде последовательности символов со знаком или без знака, признака конца или длинной точки или значений с плавающей запятой одиночной точности, в зависимости от *типа*.</span><span class="sxs-lookup"><span data-stu-id="fefac-215">Data is read from *pixels* as a sequence of signed or unsigned bytes, shorts or longs, or single-precision floating-point values, depending on *type*.</span></span> <span data-ttu-id="fefac-216">Эти значения группируются в наборы из одного, двух, трех или четырех значений, в зависимости от *формата*, для формирования элементов.</span><span class="sxs-lookup"><span data-stu-id="fefac-216">These values are grouped into sets of one, two, three, or four values, depending on *format*, to form elements.</span></span> <span data-ttu-id="fefac-217">Если *тип* является \_ точечным рисунком GL, данные рассматриваются как строка неподписанных байтов (и *Формат* должен быть \_ \_ индексом GL).</span><span class="sxs-lookup"><span data-stu-id="fefac-217">If *type* is GL\_BITMAP, the data is considered as a string of unsigned bytes (and *format* must be GL\_COLOR\_INDEX).</span></span> <span data-ttu-id="fefac-218">Каждый байт данных обрабатывается как 8 1-разрядный, с побитовой сортировкой, определяемой GL \_ \_ ЛСБ, \_ первым (см. [**глпикселсторе**](glpixelstore-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="fefac-218">Each data byte is treated as eight 1-bit elements, with bit ordering determined by GL\_UNPACK\_LSB\_FIRST (see [**glPixelStore**](glpixelstore-functions.md)).</span></span> <span data-ttu-id="fefac-219">Описание допустимых значений параметра *типа* см. в разделе [**глдравпикселс**](gldrawpixels.md) .</span><span class="sxs-lookup"><span data-stu-id="fefac-219">Please see [**glDrawPixels**](gldrawpixels.md) for a description of the acceptable values for the *type* parameter.</span></span>

<span data-ttu-id="fefac-220">Изображение текстуры может содержать до четырех компонентов на элемент текстуры в зависимости от *компонентов*.</span><span class="sxs-lookup"><span data-stu-id="fefac-220">A texture image can have up to four components per texture element, depending on *components*.</span></span> <span data-ttu-id="fefac-221">Рисунок текстуры с одним компонентом использует только красный компонент цвета RGBA, извлеченный из *пикселов*.</span><span class="sxs-lookup"><span data-stu-id="fefac-221">A one-component texture image uses only the red component of the RGBA color extracted from *pixels*.</span></span> <span data-ttu-id="fefac-222">В образе с двумя компонентами используются значения R и.</span><span class="sxs-lookup"><span data-stu-id="fefac-222">A two-component image uses the R and A values.</span></span> <span data-ttu-id="fefac-223">Изображение из трех компонентов использует значения R, G и B.</span><span class="sxs-lookup"><span data-stu-id="fefac-223">A three-component image uses the R, G, and B values.</span></span> <span data-ttu-id="fefac-224">Образ из четырех компонентов использует все компоненты RGBA.</span><span class="sxs-lookup"><span data-stu-id="fefac-224">A four-component image uses all of the RGBA components.</span></span>

<span data-ttu-id="fefac-225">Текстурирование не влияет на режим индексирования цветов.</span><span class="sxs-lookup"><span data-stu-id="fefac-225">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="fefac-226">Изображение текстуры может быть представлено теми же форматами данных, что и Пиксели в команде **глдравпикселс** , за исключением того, что \_ \_ нельзя использовать индекс трафарета GL и \_ компонент глубины GL \_ .</span><span class="sxs-lookup"><span data-stu-id="fefac-226">The texture image can be represented by the same data formats as the pixels in a **glDrawPixels** command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="fefac-227">Режимы [**глпикселсторе**](glpixelstore-functions.md) и [**глпикселтрансфер**](glpixeltransfer.md) влияют на изображения текстур точно так же, как они влияют на **глдравпикселс**.</span><span class="sxs-lookup"><span data-stu-id="fefac-227">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="fefac-228">Изображение текстуры с нулевой высотой или шириной обозначает текстуру со значением NULL.</span><span class="sxs-lookup"><span data-stu-id="fefac-228">A texture image with zero height or width indicates the null texture.</span></span> <span data-ttu-id="fefac-229">Если для уровня детализации 0 указана текстура null, то это так, как если бы текстурирование было отключено.</span><span class="sxs-lookup"><span data-stu-id="fefac-229">If the null texture is specified for level-of-detail 0, it is as if texturing were disabled.</span></span>

<span data-ttu-id="fefac-230">Следующие функции извлекают сведения, относящиеся к **glTexImage2D**:</span><span class="sxs-lookup"><span data-stu-id="fefac-230">The following functions retrieve information related to **glTexImage2D**:</span></span>

[<span data-ttu-id="fefac-231">**глжеттексимаже**</span><span class="sxs-lookup"><span data-stu-id="fefac-231">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="fefac-232">[**глисенаблед**](glisenabled.md) с аргументом GL \_ текстуры \_ 2D</span><span class="sxs-lookup"><span data-stu-id="fefac-232">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="fefac-233">Требования</span><span class="sxs-lookup"><span data-stu-id="fefac-233">Requirements</span></span>



| <span data-ttu-id="fefac-234">Требование</span><span class="sxs-lookup"><span data-stu-id="fefac-234">Requirement</span></span> | <span data-ttu-id="fefac-235">Значение</span><span class="sxs-lookup"><span data-stu-id="fefac-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fefac-236">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fefac-236">Minimum supported client</span></span><br/> | <span data-ttu-id="fefac-237">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fefac-237">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fefac-238">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fefac-238">Minimum supported server</span></span><br/> | <span data-ttu-id="fefac-239">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fefac-239">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fefac-240">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fefac-240">Header</span></span><br/>                   | <dl> <span data-ttu-id="fefac-241"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-241"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fefac-242">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fefac-242">Library</span></span><br/>                  | <dl> <span data-ttu-id="fefac-243"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-243"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fefac-244">DLL</span><span class="sxs-lookup"><span data-stu-id="fefac-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fefac-245"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fefac-245"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fefac-246">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fefac-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fefac-247">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="fefac-247">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fefac-248">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="fefac-248">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="fefac-249">**гленд**</span><span class="sxs-lookup"><span data-stu-id="fefac-249">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fefac-250">**глфог**</span><span class="sxs-lookup"><span data-stu-id="fefac-250">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="fefac-251">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="fefac-251">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="fefac-252">**глпикселсторе**</span><span class="sxs-lookup"><span data-stu-id="fefac-252">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="fefac-253">**глпикселтрансфер**</span><span class="sxs-lookup"><span data-stu-id="fefac-253">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="fefac-254">**глтексенв**</span><span class="sxs-lookup"><span data-stu-id="fefac-254">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="fefac-255">**глтексжен**</span><span class="sxs-lookup"><span data-stu-id="fefac-255">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="fefac-256">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="fefac-256">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="fefac-257">**глтекспараметер**</span><span class="sxs-lookup"><span data-stu-id="fefac-257">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





