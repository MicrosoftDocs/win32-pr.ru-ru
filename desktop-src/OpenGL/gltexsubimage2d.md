---
title: Функция glTexSubImage2D (GL. h)
description: Функция glTexSubImage2D указывает часть существующего одномерного изображения текстуры. Невозможно определить новую текстуру с помощью glTexSubImage2D.
ms.assetid: 2b6cb663-8e1d-4270-b8ba-5a8b43a2ece7
keywords:
- Функция glTexSubImage2D OpenGL
topic_type:
- apiref
api_name:
- glTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a0a59ae9e6724386cb2f7891a14e4bf9d4c1a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661822"
---
# <a name="gltexsubimage2d-function"></a><span data-ttu-id="b0e85-105">Функция glTexSubImage2D</span><span class="sxs-lookup"><span data-stu-id="b0e85-105">glTexSubImage2D function</span></span>

<span data-ttu-id="b0e85-106">Функция **glTexSubImage2D** указывает часть существующего одномерного изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="b0e85-106">The **glTexSubImage2D** function specifies a portion of an existing one-dimensional texture image.</span></span> <span data-ttu-id="b0e85-107">Невозможно определить новую текстуру с помощью **glTexSubImage2D**.</span><span class="sxs-lookup"><span data-stu-id="b0e85-107">You cannot define a new texture with **glTexSubImage2D**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0e85-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0e85-108">Syntax</span></span>


```C++
void WINAPI glTexSubImage2D(
         GLenum  target,
         GLint   level,
         GLint   xoffset,
         GLint   yoffset,
         GLsizei width,
         GLsizei height,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="b0e85-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0e85-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0e85-110">*target*</span><span class="sxs-lookup"><span data-stu-id="b0e85-110">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="b0e85-111">Целевая текстура.</span><span class="sxs-lookup"><span data-stu-id="b0e85-111">The target texture.</span></span> <span data-ttu-id="b0e85-112">Должно быть \_ 2D-текстура GL \_ .</span><span class="sxs-lookup"><span data-stu-id="b0e85-112">Must be GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="b0e85-113">*level*</span><span class="sxs-lookup"><span data-stu-id="b0e85-113">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="b0e85-114">Номер уровня детализации.</span><span class="sxs-lookup"><span data-stu-id="b0e85-114">The level-of-detail number.</span></span> <span data-ttu-id="b0e85-115">Уровень 0 — базовый образ.</span><span class="sxs-lookup"><span data-stu-id="b0e85-115">Level 0 is the base image.</span></span> <span data-ttu-id="b0e85-116">Уровень *n* — это *n*-ое изображение для сокращения mipmap.</span><span class="sxs-lookup"><span data-stu-id="b0e85-116">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="b0e85-117">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="b0e85-117">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="b0e85-118">Смещение шаг текселя в направлении *x* в пределах массива текстуры.</span><span class="sxs-lookup"><span data-stu-id="b0e85-118">A texel offset in the *x* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="b0e85-119">*йоффсет*</span><span class="sxs-lookup"><span data-stu-id="b0e85-119">*yoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="b0e85-120">Смещение шаг текселя в направлении *оси y* в пределах массива текстуры.</span><span class="sxs-lookup"><span data-stu-id="b0e85-120">A texel offset in the *y* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="b0e85-121">*width*</span><span class="sxs-lookup"><span data-stu-id="b0e85-121">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="b0e85-122">Ширина подизображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="b0e85-122">The width of the texture sub-image.</span></span>

</dd> <dt>

<span data-ttu-id="b0e85-123">*height*</span><span class="sxs-lookup"><span data-stu-id="b0e85-123">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="b0e85-124">Высота подизображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="b0e85-124">The height of the texture sub-image.</span></span>

</dd> <dt>

<span data-ttu-id="b0e85-125">*format*</span><span class="sxs-lookup"><span data-stu-id="b0e85-125">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="b0e85-126">Формат точечных данных.</span><span class="sxs-lookup"><span data-stu-id="b0e85-126">The format of the pixel data.</span></span> <span data-ttu-id="b0e85-127">Может принимать одно из следующих символьных значений.</span><span class="sxs-lookup"><span data-stu-id="b0e85-127">It can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="b0e85-128">Значение</span><span class="sxs-lookup"><span data-stu-id="b0e85-128">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="b0e85-129">Значение</span><span class="sxs-lookup"><span data-stu-id="b0e85-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="b0e85-130"><dt>**\_индекс цвета \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-130"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="b0e85-131">Каждый элемент — это одно значение, цветовой индекс.</span><span class="sxs-lookup"><span data-stu-id="b0e85-131">Each element is a single value, a color index.</span></span> <span data-ttu-id="b0e85-132">Он преобразуется в формат с фиксированной точкой (с неопределенным числом нулей справа от двоичной точки), сдвигая влево или вправо в зависимости от значения и знака \_ \_ сдвига индекса GL и добавления к \_ \_ смещению индекса GL (см. [**глпикселтрансфер**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="b0e85-132">It is converted to fixed point format (with an unspecified number of 0 bits to the right of the binary point), shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="b0e85-133">Полученный индекс преобразуется в набор цветовых компонентов, использующих \_ пиксельную карту GL i в R, GL в виде таблицы с i по G, GL в виде пикселя на B, а также в таблице GL с приведением к \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ диапазону \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="b0e85-133">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="b0e85-134"><dt>**\_красный GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-134"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="b0e85-135">Каждый элемент является одним красным компонентом.</span><span class="sxs-lookup"><span data-stu-id="b0e85-135">Each element is a single red component.</span></span> <span data-ttu-id="b0e85-136">Он преобразуется в формат с плавающей запятой и собираются в элемент RGBA путем присоединения 0,0 для зеленого и синего и 1,0 для Alpha.</span><span class="sxs-lookup"><span data-stu-id="b0e85-136">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="b0e85-137">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. **глпикселтрансфер**).</span><span class="sxs-lookup"><span data-stu-id="b0e85-137">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="b0e85-138"><dt>**\_зеленый GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-138"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="b0e85-139">Каждый элемент является одним зеленым компонентом.</span><span class="sxs-lookup"><span data-stu-id="b0e85-139">Each element is a single green component.</span></span> <span data-ttu-id="b0e85-140">Он преобразуется в формат с плавающей запятой и собираются в элемент RGBA путем присоединения 0,0 для красного и синего и 1,0 для Alpha.</span><span class="sxs-lookup"><span data-stu-id="b0e85-140">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="b0e85-141">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. [**глпикселтрансфер**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="b0e85-141">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="b0e85-142"><dt>**\_синяя GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-142"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="b0e85-143">Каждый элемент является одним синим компонентом.</span><span class="sxs-lookup"><span data-stu-id="b0e85-143">Each element is a single blue component.</span></span> <span data-ttu-id="b0e85-144">Он преобразуется в формат с плавающей запятой и собираются в элемент RGBA путем присоединения 0,0 для красного и зеленого и 1,0 для Alpha.</span><span class="sxs-lookup"><span data-stu-id="b0e85-144">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="b0e85-145">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. **глпикселтрансфер**).</span><span class="sxs-lookup"><span data-stu-id="b0e85-145">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="b0e85-146"><dt>**\_альфа-канал GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-146"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="b0e85-147">Каждый элемент является одним альфа-компонентом.</span><span class="sxs-lookup"><span data-stu-id="b0e85-147">Each element is a single alpha component.</span></span> <span data-ttu-id="b0e85-148">Он преобразуется в формат с плавающей запятой и собираются в элемент RGBA путем присоединения 0,0 для красного, зеленого и синего цветов.</span><span class="sxs-lookup"><span data-stu-id="b0e85-148">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="b0e85-149">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. [**глпикселтрансфер**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="b0e85-149">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                    |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="b0e85-150"><dt>**RGB в формате GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-150"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="b0e85-151">Каждый элемент — это тройной RGB.</span><span class="sxs-lookup"><span data-stu-id="b0e85-151">Each element is an RGB triple.</span></span> <span data-ttu-id="b0e85-152">Он преобразуется в формат с плавающей запятой и собираются в элемент RGBA путем присоединения 1,0 для альфа.</span><span class="sxs-lookup"><span data-stu-id="b0e85-152">It is converted to floating point format and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="b0e85-153">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. **глпикселтрансфер**).</span><span class="sxs-lookup"><span data-stu-id="b0e85-153">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="b0e85-154"><dt>**RGBA для GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-154"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="b0e85-155">Каждый элемент является полным элементом RGBA.</span><span class="sxs-lookup"><span data-stu-id="b0e85-155">Each element is a complete RGBA element.</span></span> <span data-ttu-id="b0e85-156">Он преобразуется в тип с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="b0e85-156">It is converted to floating point.</span></span> <span data-ttu-id="b0e85-157">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. **глпикселтрансфер**).</span><span class="sxs-lookup"><span data-stu-id="b0e85-157">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="b0e85-158"><dt>**\_светимость GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-158"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="b0e85-159">Каждый элемент является одним значением светимости.</span><span class="sxs-lookup"><span data-stu-id="b0e85-159">Each element is a single luminance value.</span></span> <span data-ttu-id="b0e85-160">Он преобразуется в формат с плавающей запятой, а затем собираются в элемент RGBA путем репликации значения светимости три раза для красного, зеленого и синего и присоединения 1,0 для альфа.</span><span class="sxs-lookup"><span data-stu-id="b0e85-160">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="b0e85-161">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. [**глпикселтрансфер**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="b0e85-161">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="b0e85-162"><dt>**\_ярко- \_ альфа-версия GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-162"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="b0e85-163">Каждый элемент является парой светимости или альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="b0e85-163">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="b0e85-164">Он преобразуется в формат с плавающей запятой, а затем собираются в элемент RGBA путем репликации значения светимости три раза для красного, зеленого и синего.</span><span class="sxs-lookup"><span data-stu-id="b0e85-164">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="b0e85-165">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. **глпикселтрансфер**).</span><span class="sxs-lookup"><span data-stu-id="b0e85-165">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="b0e85-166">*type*</span><span class="sxs-lookup"><span data-stu-id="b0e85-166">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="b0e85-167">Тип данных пикселя.</span><span class="sxs-lookup"><span data-stu-id="b0e85-167">The data type of the pixel data.</span></span> <span data-ttu-id="b0e85-168">Допустимы следующие символьные значения: \_ НЕподписанный \_ байт, байт GL, формат GL, формат GL \_ \_ \_ без знака \_ Short, краткое название GL \_ , \_ Неподписанное \_ целое число, значение GL \_ и тип \_ float.</span><span class="sxs-lookup"><span data-stu-id="b0e85-168">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="b0e85-169">*зависим*</span><span class="sxs-lookup"><span data-stu-id="b0e85-169">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="b0e85-170">Указатель на данные изображения в памяти.</span><span class="sxs-lookup"><span data-stu-id="b0e85-170">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0e85-171">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0e85-171">Return value</span></span>

<span data-ttu-id="b0e85-172">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b0e85-172">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b0e85-173">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b0e85-173">Error codes</span></span>

<span data-ttu-id="b0e85-174">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="b0e85-174">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b0e85-175">Имя</span><span class="sxs-lookup"><span data-stu-id="b0e85-175">Name</span></span>                                                                                                  | <span data-ttu-id="b0e85-176">Значение</span><span class="sxs-lookup"><span data-stu-id="b0e85-176">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b0e85-177"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-177"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b0e85-178">*целевой объект* не является \_ плоской текстурой GL \_ .</span><span class="sxs-lookup"><span data-stu-id="b0e85-178">*target* was not GL\_TEXTURE\_2D.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="b0e85-179"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-179"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b0e85-180">*Формат* не является допустимой константой.</span><span class="sxs-lookup"><span data-stu-id="b0e85-180">*format* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="b0e85-181"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-181"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b0e85-182">*тип* не является допустимой константой.</span><span class="sxs-lookup"><span data-stu-id="b0e85-182">*type* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="b0e85-183"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-183"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b0e85-184">*тип* — это \_ точечный рисунок и *Формат* , отличный от \_ индекса цвета GL \_ .</span><span class="sxs-lookup"><span data-stu-id="b0e85-184">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="b0e85-185"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-185"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="b0e85-186">*уровень* был меньше нуля или больше log2 *Max*, где *Max* было возвращено значение \_ максимального \_ размера текстуры GL \_ .</span><span class="sxs-lookup"><span data-stu-id="b0e85-186">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="b0e85-187"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-187"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="b0e85-188">*ксоффсет* был меньше-*b*; или *ксоффсет*  +  *Ширина* больше *w*  -  *b*; или *йоффсет* была меньше-*b*; или   +  *Высота* йоффсет была больше *h*  -  *b*, где *w* — Ширина текстуры GL, \_ \_ *h* — \_ Высота текстуры GL \_ , а *b* — ширина \_ границы текстуры текстуры \_ для изменяемого изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="b0e85-188">*xoffset* was less than -*b*; or *xoffset* + *width* was greater than *w* - *b*; or *yoffset* was less than -*b*; or *yoffset* + *height* was greater than *h* - *b*, where *w* is the GL\_TEXTURE\_WIDTH, *h* is the GL\_TEXTURE\_HEIGHT, and *b* is the width of the GL\_TEXTURE\_BORDER of the texture image being modified.</span></span> <br/> <span data-ttu-id="b0e85-189">Обратите внимание, что *w* и *h* имеют вдвое больше ширины границы.</span><span class="sxs-lookup"><span data-stu-id="b0e85-189">Note that *w* and *h* include twice the border width.</span></span><br/> |
| <dl> <span data-ttu-id="b0e85-190"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-190"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="b0e85-191">*Ширина* была меньше *b*, где *b* — ширина границы массива текстуры.</span><span class="sxs-lookup"><span data-stu-id="b0e85-191">*width* was was less than *b*, where *b* is the border width of the texture array.</span></span><br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="b0e85-192"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-192"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="b0e85-193">*граница* не равна нулю или 1.</span><span class="sxs-lookup"><span data-stu-id="b0e85-193">*border* was not zero or 1.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="b0e85-194"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-194"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b0e85-195">Массив текстуры не был определен предыдущей операцией **glTexImage2D** .</span><span class="sxs-lookup"><span data-stu-id="b0e85-195">The texture array was not defined by a previous **glTexImage2D** operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="b0e85-196"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-196"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b0e85-197">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b0e85-197">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                                                                                                                                                                                                        |



## <a name="remarks"></a><span data-ttu-id="b0e85-198">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0e85-198">Remarks</span></span>

<span data-ttu-id="b0e85-199">Двухмерный текстурирование для примитива включается с помощью [**гленабле**](glenable.md) и **глдисабле** с аргументом GL \_ текстуры \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="b0e85-199">Two-dimensional texturing for a primitive is enabled using [**glEnable**](glenable.md) and **glDisable** with the argument GL\_TEXTURE\_2D.</span></span> <span data-ttu-id="b0e85-200">Во время текстурирования часть указанного изображения текстуры сопоставляется с каждым включенным примитивом.</span><span class="sxs-lookup"><span data-stu-id="b0e85-200">During texturing, part of a specified texture image is mapped into each enabled primitive.</span></span> <span data-ttu-id="b0e85-201">Используйте функцию **glTexSubImage2D** для указания непрерывного подизображения существующего двухмерного изображения текстуры для текстурирования.</span><span class="sxs-lookup"><span data-stu-id="b0e85-201">You use the **glTexSubImage2D** function to specify a contiguous sub-image of an existing two-dimensional texture image for texturing.</span></span>

<span data-ttu-id="b0e85-202">Пикселей текстуры, на который ссылается *точка* , заменяет регион существующего массива текстуры на *x* индексов *ксоффсет* и *ксоффсет* + (*Width* 1) включительно и *y* индексов *йоффсет* и *йоффсет* + (*Высота* 1) включительно.</span><span class="sxs-lookup"><span data-stu-id="b0e85-202">The texels referenced by *pixels* replace a region of the existing texture array with *x* indexes of *xoffset* and *xoffset* + (*width* 1) inclusive and *y* indexes of *yoffset* and *yoffset* + (*height* 1) inclusive.</span></span> <span data-ttu-id="b0e85-203">Этот регион не может включать пикселей текстуры за пределами диапазона изначально заданного массива текстуры.</span><span class="sxs-lookup"><span data-stu-id="b0e85-203">This region cannot include any texels outside the range of the originally specified texture array.</span></span>

<span data-ttu-id="b0e85-204">Задание подобраза с нулевой *шириной* не влияет и не приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="b0e85-204">Specifying a sub-image with a *width* of zero has no effect and does not generate an error.</span></span>

<span data-ttu-id="b0e85-205">Текстурирование не влияет на режим индексирования цветов.</span><span class="sxs-lookup"><span data-stu-id="b0e85-205">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="b0e85-206">Как правило, изображения текстур могут быть представлены теми же форматами данных, что и Пиксели в команде [**глдравпикселс**](gldrawpixels.md) , за исключением того, что \_ \_ нельзя использовать индекс трафарета GL и \_ компонент глубины GL \_ .</span><span class="sxs-lookup"><span data-stu-id="b0e85-206">In general, texture images can be represented by the same data formats as the pixels in a [**glDrawPixels**](gldrawpixels.md) command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="b0e85-207">Режимы [**глпикселсторе**](glpixelstore-functions.md) и [**глпикселтрансфер**](glpixeltransfer.md) влияют на изображения текстур точно так же, как они влияют на **глдравпикселс**.</span><span class="sxs-lookup"><span data-stu-id="b0e85-207">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="b0e85-208">Следующие функции извлекают сведения, относящиеся к **glTexSubImage2D**:</span><span class="sxs-lookup"><span data-stu-id="b0e85-208">The following functions retrieve information related to **glTexSubImage2D**:</span></span>

[<span data-ttu-id="b0e85-209">**глжеттексимаже**</span><span class="sxs-lookup"><span data-stu-id="b0e85-209">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="b0e85-210">[**глисенаблед**](glisenabled.md) с аргументом GL \_ текстуры \_ 2D</span><span class="sxs-lookup"><span data-stu-id="b0e85-210">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="b0e85-211">Требования</span><span class="sxs-lookup"><span data-stu-id="b0e85-211">Requirements</span></span>



| <span data-ttu-id="b0e85-212">Требование</span><span class="sxs-lookup"><span data-stu-id="b0e85-212">Requirement</span></span> | <span data-ttu-id="b0e85-213">Значение</span><span class="sxs-lookup"><span data-stu-id="b0e85-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e85-214">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0e85-214">Minimum supported client</span></span><br/> | <span data-ttu-id="b0e85-215">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b0e85-215">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b0e85-216">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0e85-216">Minimum supported server</span></span><br/> | <span data-ttu-id="b0e85-217">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b0e85-217">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b0e85-218">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b0e85-218">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0e85-219"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-219"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b0e85-220">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b0e85-220">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0e85-221"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-221"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b0e85-222">DLL</span><span class="sxs-lookup"><span data-stu-id="b0e85-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0e85-223"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0e85-223"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0e85-224">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0e85-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0e85-225">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="b0e85-225">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="b0e85-226">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="b0e85-226">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="b0e85-227">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="b0e85-227">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="b0e85-228">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="b0e85-228">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="b0e85-229">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="b0e85-229">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="b0e85-230">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="b0e85-230">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="b0e85-231">**глфог**</span><span class="sxs-lookup"><span data-stu-id="b0e85-231">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="b0e85-232">**глжеттексимаже**</span><span class="sxs-lookup"><span data-stu-id="b0e85-232">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="b0e85-233">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="b0e85-233">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="b0e85-234">**глпикселсторе**</span><span class="sxs-lookup"><span data-stu-id="b0e85-234">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="b0e85-235">**глпикселтрансфер**</span><span class="sxs-lookup"><span data-stu-id="b0e85-235">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="b0e85-236">**глтексенв**</span><span class="sxs-lookup"><span data-stu-id="b0e85-236">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="b0e85-237">**глтексжен**</span><span class="sxs-lookup"><span data-stu-id="b0e85-237">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="b0e85-238">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="b0e85-238">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="b0e85-239">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="b0e85-239">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="b0e85-240">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="b0e85-240">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="b0e85-241">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="b0e85-241">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="b0e85-242">**глтекспараметер**</span><span class="sxs-lookup"><span data-stu-id="b0e85-242">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





