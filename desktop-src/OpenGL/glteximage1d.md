---
title: Функция glTexImage1D (GL. h)
description: Функция glTexImage1D указывает одномерный рисунок текстуры.
ms.assetid: 4f537b89-2ea2-4e2e-8c57-c372bf53f12c
keywords:
- Функция glTexImage1D OpenGL
topic_type:
- apiref
api_name:
- glTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1865d19c54b9c59654f07162d2480aa5b29c47f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071493"
---
# <a name="glteximage1d-function"></a><span data-ttu-id="8b15b-104">Функция glTexImage1D</span><span class="sxs-lookup"><span data-stu-id="8b15b-104">glTexImage1D function</span></span>

<span data-ttu-id="8b15b-105">Функция **glTexImage1D** указывает одномерный рисунок текстуры.</span><span class="sxs-lookup"><span data-stu-id="8b15b-105">The **glTexImage1D** function specifies a one-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b15b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b15b-106">Syntax</span></span>


```C++
void WINAPI glTexImage1D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLint   border,
         GLint   format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="8b15b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b15b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b15b-108">*target*</span><span class="sxs-lookup"><span data-stu-id="8b15b-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="8b15b-109">Целевая текстура.</span><span class="sxs-lookup"><span data-stu-id="8b15b-109">The target texture.</span></span> <span data-ttu-id="8b15b-110">Должен быть \_ \_ одномерной текстурой GL.</span><span class="sxs-lookup"><span data-stu-id="8b15b-110">Must be GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="8b15b-111">*level*</span><span class="sxs-lookup"><span data-stu-id="8b15b-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="8b15b-112">Номер уровня детализации.</span><span class="sxs-lookup"><span data-stu-id="8b15b-112">The level-of-detail number.</span></span> <span data-ttu-id="8b15b-113">Уровень 0 является базовым уровнем образа.</span><span class="sxs-lookup"><span data-stu-id="8b15b-113">Level 0 is the base image level.</span></span> <span data-ttu-id="8b15b-114">Уровень *n* — это *n*-ое изображение для сокращения mipmap.</span><span class="sxs-lookup"><span data-stu-id="8b15b-114">Level *n* is the *n* Th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="8b15b-115">*интерналформат*</span><span class="sxs-lookup"><span data-stu-id="8b15b-115">*internalformat*</span></span> 
</dt> <dd>

<span data-ttu-id="8b15b-116">Задает число компонентов цвета в текстуре.</span><span class="sxs-lookup"><span data-stu-id="8b15b-116">Specifies the number of color components in the texture.</span></span> <span data-ttu-id="8b15b-117">Значение должно быть равно 1, 2, 3 или 4 или одной из следующих символьных констант: GL \_ Alpha, GL \_ ALPHA4, GL \_ ALPHA8, GL \_ ALPHA12, GL \_ ALPHA16, \_ светимость GL, GL LUMINANCE4 \_ , GL \_ LUMINANCE8, GL \_ LUMINANCE12, GL \_ LUMINANCE16, GL \_ светимость \_ Alpha, GL LUMINANCE4 ALPHA4, GL LUMINANCE6 ALPHA2 \_ \_ \_ \_ , GL \_ LUMINANCE8 \_ ALPHA8, GL \_ LUMINANCE12 ALPHA4, \_ GL \_ LUMINANCE12 \_ ALPHA12, GL \_ LUMINANCE16 ALPHA16, "интенсивность GL", GL INTENSITY4 \_ \_ \_ , GL \_ INTENSITY8, GL \_ INTENSITY12, GL \_ INTENSITY16, GL \_ RGB, GL R3 \_ \_ G3 \_ B2, GL RGB4, \_ GL \_ RGB5, GL \_ RGB8, GL RGB10 \_ , \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ GL RGB12, GL, ГК, GL RGB16, GL, ГК RGBA2, GL RGBA4</span><span class="sxs-lookup"><span data-stu-id="8b15b-117">Must be 1, 2, 3, or 4, or one of the following symbolic constants: GL\_ALPHA, GL\_ALPHA4, GL\_ALPHA8, GL\_ALPHA12, GL\_ALPHA16, GL\_LUMINANCE, GL\_LUMINANCE4, GL\_LUMINANCE8, GL\_LUMINANCE12, GL\_LUMINANCE16, GL\_LUMINANCE\_ALPHA, GL\_LUMINANCE4\_ALPHA4, GL\_LUMINANCE6\_ALPHA2, GL\_LUMINANCE8\_ALPHA8, GL\_LUMINANCE12\_ALPHA4, GL\_LUMINANCE12\_ALPHA12, GL\_LUMINANCE16\_ALPHA16, GL\_INTENSITY, GL\_INTENSITY4, GL\_INTENSITY8, GL\_INTENSITY12, GL\_INTENSITY16, GL\_RGB, GL\_R3\_G3\_B2, GL\_RGB4, GL\_RGB5, GL\_RGB8, GL\_RGB10, GL\_RGB12, GL\_RGB16, GL\_RGBA, GL\_RGBA2, GL\_RGBA4, GL\_RGB5\_A1, GL\_RGBA8, GL\_RGB10\_A2, GL\_RGBA12, or GL\_RGBA16.</span></span>

</dd> <dt>

<span data-ttu-id="8b15b-118">*width*</span><span class="sxs-lookup"><span data-stu-id="8b15b-118">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="8b15b-119">Ширина изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="8b15b-119">The width of the texture image.</span></span> <span data-ttu-id="8b15b-120">Значение должно быть 2 *n* + 2 ( *border* ) для некоторого целого числа *n*.</span><span class="sxs-lookup"><span data-stu-id="8b15b-120">Must be 2 *n* + 2( *border* ) for some integer *n*.</span></span> <span data-ttu-id="8b15b-121">Высота изображения текстуры равна 1.</span><span class="sxs-lookup"><span data-stu-id="8b15b-121">The height of the texture image is 1.</span></span>

</dd> <dt>

<span data-ttu-id="8b15b-122">*цвета*</span><span class="sxs-lookup"><span data-stu-id="8b15b-122">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="8b15b-123">Ширина границы.</span><span class="sxs-lookup"><span data-stu-id="8b15b-123">The width of the border.</span></span> <span data-ttu-id="8b15b-124">Значение должно быть 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="8b15b-124">Must be either 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="8b15b-125">*format*</span><span class="sxs-lookup"><span data-stu-id="8b15b-125">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="8b15b-126">Формат точечных данных.</span><span class="sxs-lookup"><span data-stu-id="8b15b-126">The format of the pixel data.</span></span> <span data-ttu-id="8b15b-127">Можно предположить, что одно из девяти символьных значений.</span><span class="sxs-lookup"><span data-stu-id="8b15b-127">It can assume one of nine symbolic values.</span></span>



| <span data-ttu-id="8b15b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="8b15b-128">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="8b15b-129">Значение</span><span class="sxs-lookup"><span data-stu-id="8b15b-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="8b15b-130"><dt>**\_индекс цвета \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-130"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="8b15b-131">Каждый элемент — это одно значение, цветовой индекс.</span><span class="sxs-lookup"><span data-stu-id="8b15b-131">Each element is a single value, a color index.</span></span> <span data-ttu-id="8b15b-132">Он преобразуется в фиксированную точку (с неопределенным числом нулей справа от двоичной точки), сдвигаются влево или вправо, в зависимости от значения и знака \_ \_ сдвига индекса GL, и добавляется к \_ \_ смещению индекса GL (см. [**глпикселтрансфер**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="8b15b-132">It is converted to fixed point (with an unspecified number of 0 bits to the right of the binary point), shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="8b15b-133">Полученный индекс преобразуется в набор цветовых компонентов, использующих \_ пиксельную карту GL i в R, GL в виде таблицы с i по G, GL в виде пикселя на B, а также в таблице GL с приведением к \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ диапазону \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="8b15b-133">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="8b15b-134"><dt>**\_красный GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-134"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="8b15b-135">Каждый элемент является одним красным компонентом.</span><span class="sxs-lookup"><span data-stu-id="8b15b-135">Each element is a single red component.</span></span> <span data-ttu-id="8b15b-136">Он преобразуется в плавающую точку и собирается в элемент RGBA путем присоединения 0,0 для зеленого и синего и 1,0 для Alpha.</span><span class="sxs-lookup"><span data-stu-id="8b15b-136">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="8b15b-137">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. **глпикселтрансфер**).</span><span class="sxs-lookup"><span data-stu-id="8b15b-137">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="8b15b-138"><dt>**\_зеленый GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-138"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="8b15b-139">Каждый элемент является одним зеленым компонентом.</span><span class="sxs-lookup"><span data-stu-id="8b15b-139">Each element is a single green component.</span></span> <span data-ttu-id="8b15b-140">Он преобразуется в плавающую точку и собирается в элемент RGBA путем присоединения 0,0 для красного и синего и 1,0 для Alpha.</span><span class="sxs-lookup"><span data-stu-id="8b15b-140">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="8b15b-141">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. [**глпикселтрансфер**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="8b15b-141">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="8b15b-142"><dt>**\_синяя GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-142"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="8b15b-143">Каждый элемент является одним синим компонентом.</span><span class="sxs-lookup"><span data-stu-id="8b15b-143">Each element is a single blue component.</span></span> <span data-ttu-id="8b15b-144">Он преобразуется в плавающую точку и собирается в элемент RGBA путем присоединения 0,0 для красного и зеленого и 1,0 для Alpha.</span><span class="sxs-lookup"><span data-stu-id="8b15b-144">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="8b15b-145">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. **глпикселтрансфер**).</span><span class="sxs-lookup"><span data-stu-id="8b15b-145">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="8b15b-146"><dt>**\_альфа-канал GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-146"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="8b15b-147">Каждый элемент является одним красным компонентом.</span><span class="sxs-lookup"><span data-stu-id="8b15b-147">Each element is a single red component.</span></span> <span data-ttu-id="8b15b-148">Он преобразуется в плавающую точку и собирается в элемент RGBA путем присоединения 0,0 для красного, зеленого и синего цветов.</span><span class="sxs-lookup"><span data-stu-id="8b15b-148">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="8b15b-149">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. [**глпикселтрансфер**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="8b15b-149">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                      |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="8b15b-150"><dt>**RGB в формате GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-150"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="8b15b-151">Каждый элемент — это тройной RGB.</span><span class="sxs-lookup"><span data-stu-id="8b15b-151">Each element is an RGB triple.</span></span> <span data-ttu-id="8b15b-152">Он преобразуется в плавающую точку и собирается в элемент RGBA путем присоединения 1,0 для альфа.</span><span class="sxs-lookup"><span data-stu-id="8b15b-152">It is converted to floating point and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="8b15b-153">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. **глпикселтрансфер**).</span><span class="sxs-lookup"><span data-stu-id="8b15b-153">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="8b15b-154"><dt>**RGBA для GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-154"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="8b15b-155">Каждый элемент является полным элементом RGBA.</span><span class="sxs-lookup"><span data-stu-id="8b15b-155">Each element is a complete RGBA element.</span></span> <span data-ttu-id="8b15b-156">Он преобразуется в тип с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="8b15b-156">It is converted to floating point.</span></span> <span data-ttu-id="8b15b-157">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. **глпикселтрансфер**).</span><span class="sxs-lookup"><span data-stu-id="8b15b-157">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                                                                         |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="8b15b-158"><dt>**\_BGRа \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-158"><dt>**GL\_BGR\_EXT**</dt></span></span> </dl>                         | <span data-ttu-id="8b15b-159">Каждый пиксель — это группа из трех компонентов в следующем порядке: синий, зеленый, красный.</span><span class="sxs-lookup"><span data-stu-id="8b15b-159">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="8b15b-160">GL \_ BGR \_ ext предоставляет формат, соответствующий макету памяти, не зависящему от устройства Windows (DIB).</span><span class="sxs-lookup"><span data-stu-id="8b15b-160">GL\_BGR\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="8b15b-161">Поэтому приложения могут использовать те же данные, что и вызовы функций Windows, и вызовы функций OpenGL Pixel.</span><span class="sxs-lookup"><span data-stu-id="8b15b-161">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="8b15b-162"><dt>**\_BGRAа \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-162"><dt>**GL\_BGRA\_EXT**</dt></span></span> </dl>                      | <span data-ttu-id="8b15b-163">Каждый пиксель — это группа из четырех компонентов в следующем порядке: синий, зеленый, красный, альфа.</span><span class="sxs-lookup"><span data-stu-id="8b15b-163">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="8b15b-164">GL \_ BGRA \_ ext предоставляет формат, соответствующий макету памяти, не зависящему от устройства Windows (DIB).</span><span class="sxs-lookup"><span data-stu-id="8b15b-164">GL\_BGRA\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="8b15b-165">Поэтому приложения могут использовать те же данные, что и вызовы функций Windows, и вызовы функций OpenGL Pixel.</span><span class="sxs-lookup"><span data-stu-id="8b15b-165">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="8b15b-166"><dt>**\_светимость GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-166"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="8b15b-167">Каждый элемент является одним значением светимости.</span><span class="sxs-lookup"><span data-stu-id="8b15b-167">Each element is a single luminance value.</span></span> <span data-ttu-id="8b15b-168">Он преобразуется в плавающую точку, а затем собирается в элемент RGBA путем репликации значения светимости три раза для красного, зеленого и синего и присоединения 1,0 для альфа.</span><span class="sxs-lookup"><span data-stu-id="8b15b-168">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="8b15b-169">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. [**глпикселтрансфер**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="8b15b-169">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="8b15b-170"><dt>**\_ярко- \_ альфа-версия GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-170"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="8b15b-171">Каждый элемент является парой светимости или альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="8b15b-171">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="8b15b-172">Он преобразуется в плавающую точку, а затем собирается в элемент RGBA путем репликации значения светимости три раза для красного, зеленого и синего.</span><span class="sxs-lookup"><span data-stu-id="8b15b-172">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="8b15b-173">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. **глпикселтрансфер**).</span><span class="sxs-lookup"><span data-stu-id="8b15b-173">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="8b15b-174">*type*</span><span class="sxs-lookup"><span data-stu-id="8b15b-174">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="8b15b-175">Тип данных пикселя.</span><span class="sxs-lookup"><span data-stu-id="8b15b-175">The data type of the pixel data.</span></span> <span data-ttu-id="8b15b-176">Допустимы следующие символьные значения: \_ НЕподписанный \_ байт, байт GL, формат GL, формат GL \_ \_ \_ без знака \_ Short, краткое название GL \_ , \_ Неподписанное \_ целое число, значение GL \_ и тип \_ float.</span><span class="sxs-lookup"><span data-stu-id="8b15b-176">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="8b15b-177">*зависим*</span><span class="sxs-lookup"><span data-stu-id="8b15b-177">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="8b15b-178">Указатель на данные изображения в памяти.</span><span class="sxs-lookup"><span data-stu-id="8b15b-178">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b15b-179">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b15b-179">Return value</span></span>

<span data-ttu-id="8b15b-180">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8b15b-180">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8b15b-181">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="8b15b-181">Error codes</span></span>

<span data-ttu-id="8b15b-182">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="8b15b-182">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8b15b-183">Имя</span><span class="sxs-lookup"><span data-stu-id="8b15b-183">Name</span></span>                                                                                                  | <span data-ttu-id="8b15b-184">Значение</span><span class="sxs-lookup"><span data-stu-id="8b15b-184">Meaning</span></span>                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8b15b-185"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-185"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="8b15b-186">*целевой объект* не является \_ текстурой GL.</span><span class="sxs-lookup"><span data-stu-id="8b15b-186">*target* was not an GL\_TEXTURE.</span></span><br/>                                                                                                                                                                                    |
| <dl> <span data-ttu-id="8b15b-187"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-187"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="8b15b-188">*Формат* не является допустимой константой *формата* .</span><span class="sxs-lookup"><span data-stu-id="8b15b-188">*format* was not an accepted *format* constant.</span></span> <span data-ttu-id="8b15b-189">Принимаются только константы формата \_ , отличные от индекса трафарета GL \_ и \_ компонента глубины GL \_ .</span><span class="sxs-lookup"><span data-stu-id="8b15b-189">Only format constants other than GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT are accepted.</span></span> <span data-ttu-id="8b15b-190">Список возможных значений см. в описании параметра *Format* .</span><span class="sxs-lookup"><span data-stu-id="8b15b-190">See the parameter description of *format* for a list of possible values.</span></span><br/> |
| <dl> <span data-ttu-id="8b15b-191"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-191"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="8b15b-192">*тип* не является константой *типа* .</span><span class="sxs-lookup"><span data-stu-id="8b15b-192">*type* was not a *type* constant.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="8b15b-193"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-193"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="8b15b-194">*тип* — это \_ точечный рисунок и *Формат* , отличный от \_ индекса цвета GL \_ .</span><span class="sxs-lookup"><span data-stu-id="8b15b-194">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                        |
| <dl> <span data-ttu-id="8b15b-195"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-195"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="8b15b-196">*уровень* был меньше нуля или больше log2 *Max*, где *Max* было возвращено значение \_ максимального \_ размера текстуры GL \_ .</span><span class="sxs-lookup"><span data-stu-id="8b15b-196">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="8b15b-197"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-197"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="8b15b-198">*интерналформат* не был равен 1, 2, 3 или 4.</span><span class="sxs-lookup"><span data-stu-id="8b15b-198">*internalformat* was was not 1, 2, 3, or 4.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="8b15b-199"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="8b15b-200">*Ширина* была меньше нуля или больше 2 + ГК для \_ максимального \_ размера текстуры \_ или не может быть представлена 2 *n* + 2 (Border) для некоторого целого значения *n*.</span><span class="sxs-lookup"><span data-stu-id="8b15b-200">*width* was less than zero or greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or it could not be represented as 2 *n* + 2(border) for some integer value of *n*.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="8b15b-201"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-201"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="8b15b-202">*граница* не равна 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="8b15b-202">*border* was not 0 or 1.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="8b15b-203"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-203"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8b15b-204">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="8b15b-204">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                          |



## <a name="remarks"></a><span data-ttu-id="8b15b-205">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b15b-205">Remarks</span></span>

<span data-ttu-id="8b15b-206">Функция **glTexImage1D** указывает одномерный рисунок текстуры.</span><span class="sxs-lookup"><span data-stu-id="8b15b-206">The **glTexImage1D** function specifies a one-dimensional texture image.</span></span> <span data-ttu-id="8b15b-207">Текстурирование сопоставляет часть указанного *изображения текстуры* с каждым графическим примитивом, для которого включено текстурирование.</span><span class="sxs-lookup"><span data-stu-id="8b15b-207">Texturing maps a portion of a specified *texture image* onto each graphical primitive for which texturing is enabled.</span></span> <span data-ttu-id="8b15b-208">Одномерный текстурирование включается и отключается с помощью [**гленабле**](glenable.md) и **глдисабле** с аргументом GL \_ текстуры \_ 1d.</span><span class="sxs-lookup"><span data-stu-id="8b15b-208">One-dimensional texturing is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_TEXTURE\_1D.</span></span>

<span data-ttu-id="8b15b-209">Изображения текстуры определяются с помощью **glTexImage1D**.</span><span class="sxs-lookup"><span data-stu-id="8b15b-209">Texture images are defined with **glTexImage1D**.</span></span> <span data-ttu-id="8b15b-210">Аргументы описывают параметры изображения текстуры, такие как ширина, ширина границы, номер уровня детализации (см. [**глтекспараметер**](gltexparameter-functions.md)) и число предоставленных компонентов цвета.</span><span class="sxs-lookup"><span data-stu-id="8b15b-210">The arguments describe the parameters of the texture image, such as width, width of the border, level-of-detail number (see [**glTexParameter**](gltexparameter-functions.md)), and number of color components provided.</span></span> <span data-ttu-id="8b15b-211">Последние три аргумента описывают способ представления изображения в памяти.</span><span class="sxs-lookup"><span data-stu-id="8b15b-211">The last three arguments describe the way the image is represented in memory.</span></span> <span data-ttu-id="8b15b-212">Эти аргументы идентичны форматам пикселей, используемым для [**глдравпикселс**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="8b15b-212">These arguments are identical to the pixel formats used for [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="8b15b-213">Данные считываются из *пикселей* в виде последовательности символов со знаком или без знака, признака конца или длинной точки или значений с плавающей запятой одиночной точности, в зависимости от *типа*.</span><span class="sxs-lookup"><span data-stu-id="8b15b-213">Data is read from *pixels* as a sequence of signed or unsigned bytes, shorts or longs, or single-precision floating-point values, depending on *type*.</span></span> <span data-ttu-id="8b15b-214">Эти значения группируются в наборы из одного, двух, трех или четырех значений, в зависимости от *формата*, для формирования элементов.</span><span class="sxs-lookup"><span data-stu-id="8b15b-214">These values are grouped into sets of one, two, three, or four values, depending on *format*, to form elements.</span></span> <span data-ttu-id="8b15b-215">Если *тип* является \_ точечным рисунком GL, данные рассматриваются как строка неподписанных байтов (и *Формат* должен быть \_ \_ индексом GL).</span><span class="sxs-lookup"><span data-stu-id="8b15b-215">If *type* is GL\_BITMAP, the data is considered as a string of unsigned bytes (and *format* must be GL\_COLOR\_INDEX).</span></span> <span data-ttu-id="8b15b-216">Каждый байт данных обрабатывается как 8 1-разрядный, с побитовой сортировкой, определяемой GL \_ \_ ЛСБ, \_ первым (см. [**глпикселсторе**](glpixelstore-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="8b15b-216">Each data byte is treated as eight 1-bit elements, with bit ordering determined by GL\_UNPACK\_LSB\_FIRST (see [**glPixelStore**](glpixelstore-functions.md)).</span></span>

<span data-ttu-id="8b15b-217">Изображение текстуры может содержать до четырех компонентов на элемент текстуры в зависимости от *компонентов*.</span><span class="sxs-lookup"><span data-stu-id="8b15b-217">A texture image can have up to four components per texture element, depending on *components*.</span></span> <span data-ttu-id="8b15b-218">Рисунок текстуры с одним компонентом использует только красный компонент цвета RGBA, извлеченный из *пикселов*.</span><span class="sxs-lookup"><span data-stu-id="8b15b-218">A one-component texture image uses only the red component of the RGBA color extracted from *pixels*.</span></span> <span data-ttu-id="8b15b-219">В образе с двумя компонентами используются значения R и.</span><span class="sxs-lookup"><span data-stu-id="8b15b-219">A two-component image uses the R and A values.</span></span> <span data-ttu-id="8b15b-220">Изображение из трех компонентов использует значения R, G и B.</span><span class="sxs-lookup"><span data-stu-id="8b15b-220">A three-component image uses the R, G, and B values.</span></span> <span data-ttu-id="8b15b-221">Образ из четырех компонентов использует все компоненты RGBA.</span><span class="sxs-lookup"><span data-stu-id="8b15b-221">A four-component image uses all of the RGBA components.</span></span>

<span data-ttu-id="8b15b-222">Текстурирование не влияет на режим индексирования цветов.</span><span class="sxs-lookup"><span data-stu-id="8b15b-222">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="8b15b-223">Изображение текстуры может быть представлено теми же форматами данных, что и Пиксели в команде [**глдравпикселс**](gldrawpixels.md) , за исключением того, что \_ \_ нельзя использовать индекс трафарета GL и \_ компонент глубины GL \_ .</span><span class="sxs-lookup"><span data-stu-id="8b15b-223">The texture image can be represented by the same data formats as the pixels in a [**glDrawPixels**](gldrawpixels.md) command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="8b15b-224">Режимы [**глпикселсторе**](glpixelstore-functions.md) и [**глпикселтрансфер**](glpixeltransfer.md) влияют на изображения текстур точно так же, как они влияют на **глдравпикселс**.</span><span class="sxs-lookup"><span data-stu-id="8b15b-224">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="8b15b-225">Изображение текстуры с нулевой шириной обозначает текстуру со значением NULL.</span><span class="sxs-lookup"><span data-stu-id="8b15b-225">A texture image with zero width indicates the null texture.</span></span> <span data-ttu-id="8b15b-226">Если для уровня детализации 0 указана текстура null, то это так, как если бы текстурирование было отключено.</span><span class="sxs-lookup"><span data-stu-id="8b15b-226">If the null texture is specified for level-of-detail 0, it is as if texturing were disabled.</span></span>

<span data-ttu-id="8b15b-227">Следующие функции извлекают сведения, относящиеся к **глтексимажеид**:</span><span class="sxs-lookup"><span data-stu-id="8b15b-227">The following functions retrieve information related to **glTexImageID**:</span></span>

[<span data-ttu-id="8b15b-228">**глжеттексимаже**</span><span class="sxs-lookup"><span data-stu-id="8b15b-228">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="8b15b-229">[**глисенаблед**](glisenabled.md) с аргументом GL \_ текстура \_ 1d</span><span class="sxs-lookup"><span data-stu-id="8b15b-229">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="8b15b-230">Требования</span><span class="sxs-lookup"><span data-stu-id="8b15b-230">Requirements</span></span>



| <span data-ttu-id="8b15b-231">Требование</span><span class="sxs-lookup"><span data-stu-id="8b15b-231">Requirement</span></span> | <span data-ttu-id="8b15b-232">Значение</span><span class="sxs-lookup"><span data-stu-id="8b15b-232">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b15b-233">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b15b-233">Minimum supported client</span></span><br/> | <span data-ttu-id="8b15b-234">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8b15b-234">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8b15b-235">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b15b-235">Minimum supported server</span></span><br/> | <span data-ttu-id="8b15b-236">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8b15b-236">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8b15b-237">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8b15b-237">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b15b-238"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-238"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8b15b-239">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8b15b-239">Library</span></span><br/>                  | <dl> <span data-ttu-id="8b15b-240"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-240"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8b15b-241">DLL</span><span class="sxs-lookup"><span data-stu-id="8b15b-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b15b-242"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b15b-242"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b15b-243">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b15b-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b15b-244">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="8b15b-244">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8b15b-245">**глкопипикселс**</span><span class="sxs-lookup"><span data-stu-id="8b15b-245">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="8b15b-246">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="8b15b-246">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="8b15b-247">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="8b15b-247">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="8b15b-248">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="8b15b-248">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="8b15b-249">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="8b15b-249">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="8b15b-250">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="8b15b-250">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="8b15b-251">**гленд**</span><span class="sxs-lookup"><span data-stu-id="8b15b-251">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8b15b-252">**глфог**</span><span class="sxs-lookup"><span data-stu-id="8b15b-252">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="8b15b-253">**глжеттексимаже**</span><span class="sxs-lookup"><span data-stu-id="8b15b-253">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="8b15b-254">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="8b15b-254">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="8b15b-255">**глпикселсторе**</span><span class="sxs-lookup"><span data-stu-id="8b15b-255">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="8b15b-256">**глпикселтрансфер**</span><span class="sxs-lookup"><span data-stu-id="8b15b-256">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="8b15b-257">**глтексенв**</span><span class="sxs-lookup"><span data-stu-id="8b15b-257">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="8b15b-258">**глтексжен**</span><span class="sxs-lookup"><span data-stu-id="8b15b-258">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="8b15b-259">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="8b15b-259">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="8b15b-260">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="8b15b-260">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="8b15b-261">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="8b15b-261">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="8b15b-262">**глтекспараметер**</span><span class="sxs-lookup"><span data-stu-id="8b15b-262">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





