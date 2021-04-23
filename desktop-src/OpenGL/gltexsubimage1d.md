---
title: Функция glTexSubImage1D (GL. h)
description: Функция glTexSubImage1D указывает часть существующего одномерного изображения текстуры. Невозможно определить новую текстуру с помощью glTexSubImage1D.
ms.assetid: e5fcb1a3-96f8-47a6-a9a7-0061faaaa6ac
keywords:
- Функция glTexSubImage1D OpenGL
topic_type:
- apiref
api_name:
- glTexSubImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe5510221b738a81f428f9e982a2f9bb2c23588
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801625"
---
# <a name="gltexsubimage1d-function"></a><span data-ttu-id="cbd6e-105">Функция glTexSubImage1D</span><span class="sxs-lookup"><span data-stu-id="cbd6e-105">glTexSubImage1D function</span></span>

<span data-ttu-id="cbd6e-106">Функция **glTexSubImage1D** указывает часть существующего одномерного изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-106">The **glTexSubImage1D** function specifies a portion of an existing one-dimensional texture image.</span></span> <span data-ttu-id="cbd6e-107">Невозможно определить новую текстуру с помощью **glTexSubImage1D**.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-107">You cannot define a new texture with **glTexSubImage1D**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbd6e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbd6e-108">Syntax</span></span>


```C++
void WINAPI glTexSubImage1D(
         GLenum  target,
         GLint   level,
         GLint   xoffset,
         GLsizei width,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="cbd6e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbd6e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbd6e-110">*target*</span><span class="sxs-lookup"><span data-stu-id="cbd6e-110">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="cbd6e-111">Целевая текстура.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-111">The target texture.</span></span> <span data-ttu-id="cbd6e-112">Должен быть \_ \_ одномерной текстурой GL.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-112">Must be GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="cbd6e-113">*level*</span><span class="sxs-lookup"><span data-stu-id="cbd6e-113">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="cbd6e-114">Номер уровня детализации.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-114">The level-of-detail number.</span></span> <span data-ttu-id="cbd6e-115">Уровень 0 — базовый образ.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-115">Level 0 is the base image.</span></span> <span data-ttu-id="cbd6e-116">Уровень *n* — это *n*-ое изображение для сокращения mipmap.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-116">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="cbd6e-117">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="cbd6e-117">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="cbd6e-118">Смещение шаг текселя в направлении *x* в пределах массива текстуры.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-118">A texel offset in the *x* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="cbd6e-119">*width*</span><span class="sxs-lookup"><span data-stu-id="cbd6e-119">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="cbd6e-120">Ширина подизображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-120">The width of the texture sub-image.</span></span>

</dd> <dt>

<span data-ttu-id="cbd6e-121">*format*</span><span class="sxs-lookup"><span data-stu-id="cbd6e-121">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="cbd6e-122">Формат точечных данных.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-122">The format of the pixel data.</span></span> <span data-ttu-id="cbd6e-123">Этот параметр может принимать одно из следующих символьных значений.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-123">This parameter can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="cbd6e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="cbd6e-124">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="cbd6e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="cbd6e-125">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="cbd6e-126"><dt>**\_индекс цвета \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-126"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="cbd6e-127">Каждый элемент — это одно значение, цветовой индекс.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-127">Each element is a single value, a color index.</span></span> <span data-ttu-id="cbd6e-128">Он преобразуется в формат с фиксированной точкой (с неопределенным числом нулей справа от двоичной точки), сдвигая влево или вправо в зависимости от значения и знака \_ \_ сдвига индекса GL и добавления к \_ \_ смещению индекса GL (см. [**глпикселтрансфер**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="cbd6e-128">It is converted to fixed point format (with an unspecified number of 0 bits to the right of the binary point), shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="cbd6e-129">Полученный индекс преобразуется в набор цветовых компонентов, использующих \_ пиксельную карту GL i в R, GL в виде таблицы с i по G, GL в виде пикселя на B, а также в таблице GL с приведением к \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ диапазону \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="cbd6e-129">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="cbd6e-130"><dt>**\_красный GL**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-130"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="cbd6e-131">Каждый элемент является одним красным компонентом.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-131">Each element is a single red component.</span></span> <span data-ttu-id="cbd6e-132">Он преобразуется в формат с плавающей запятой и собираются в элемент RGBA путем присоединения 0,0 для зеленого и синего и 1,0 для Alpha.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-132">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="cbd6e-133">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. **глпикселтрансфер**).</span><span class="sxs-lookup"><span data-stu-id="cbd6e-133">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="cbd6e-134"><dt>**\_зеленый GL**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-134"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="cbd6e-135">Каждый элемент является одним зеленым компонентом.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-135">Each element is a single green component.</span></span> <span data-ttu-id="cbd6e-136">Он преобразуется в формат с плавающей запятой и собираются в элемент RGBA путем присоединения 0,0 для красного и синего и 1,0 для Alpha.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-136">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="cbd6e-137">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. [**глпикселтрансфер**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="cbd6e-137">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="cbd6e-138"><dt>**\_синяя GL**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-138"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="cbd6e-139">Каждый элемент является одним синим компонентом.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-139">Each element is a single blue component.</span></span> <span data-ttu-id="cbd6e-140">Он преобразуется в формат с плавающей запятой и собираются в элемент RGBA путем присоединения 0,0 для красного и зеленого и 1,0 для Alpha.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-140">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="cbd6e-141">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. **глпикселтрансфер**).</span><span class="sxs-lookup"><span data-stu-id="cbd6e-141">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="cbd6e-142"><dt>**\_альфа-канал GL**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-142"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="cbd6e-143">Каждый элемент является одним альфа-компонентом.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-143">Each element is a single alpha component.</span></span> <span data-ttu-id="cbd6e-144">Он преобразуется в формат с плавающей запятой и собираются в элемент RGBA путем присоединения 0,0 для красного, зеленого и синего цветов.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-144">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="cbd6e-145">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. [**глпикселтрансфер**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="cbd6e-145">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                    |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="cbd6e-146"><dt>**RGB в формате GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-146"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="cbd6e-147">Каждый элемент — это тройной RGB.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-147">Each element is an RGB triple.</span></span> <span data-ttu-id="cbd6e-148">Он преобразуется в плавающую точку и собирается в элемент RGBA путем присоединения 1,0 для альфа.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-148">It is converted to floating point and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="cbd6e-149">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. **глпикселтрансфер**).</span><span class="sxs-lookup"><span data-stu-id="cbd6e-149">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                            |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="cbd6e-150"><dt>**RGBA для GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-150"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="cbd6e-151">Каждый элемент является полным элементом RGBA.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-151">Each element is a complete RGBA element.</span></span> <span data-ttu-id="cbd6e-152">Он преобразуется в формат с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-152">It is converted to floating point format.</span></span> <span data-ttu-id="cbd6e-153">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. **глпикселтрансфер**).</span><span class="sxs-lookup"><span data-stu-id="cbd6e-153">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                                                                         |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="cbd6e-154"><dt>**\_светимость GL**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-154"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="cbd6e-155">Каждый элемент является одним значением светимости.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-155">Each element is a single luminance value.</span></span> <span data-ttu-id="cbd6e-156">Он преобразуется в формат с плавающей запятой, а затем собираются в элемент RGBA путем репликации значения светимости три раза для красного, зеленого и синего и присоединения 1,0 для альфа.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-156">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="cbd6e-157">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. [**глпикселтрансфер**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="cbd6e-157">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="cbd6e-158"><dt>**\_ярко- \_ альфа-версия GL**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-158"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="cbd6e-159">Каждый элемент является парой светимости или альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-159">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="cbd6e-160">Он преобразуется в формат с плавающей запятой, а затем собираются в элемент RGBA путем репликации значения светимости три раза для красного, зеленого и синего.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-160">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="cbd6e-161">Затем каждый компонент умножается на коэффициент масштабирования со знаком «GL \_ c \_ », добавленный к смещению «смещение на языке c» со знаком, а также в \_ \_ диапазон \[ 0, 1 \] (см. **глпикселтрансфер**).</span><span class="sxs-lookup"><span data-stu-id="cbd6e-161">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="cbd6e-162">*type*</span><span class="sxs-lookup"><span data-stu-id="cbd6e-162">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="cbd6e-163">Тип данных пикселя.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-163">The data type of the pixel data.</span></span> <span data-ttu-id="cbd6e-164">Допустимы следующие символьные значения: \_ НЕподписанный \_ байт, байт GL, формат GL, формат GL \_ \_ \_ без знака \_ Short, краткое название GL \_ , \_ Неподписанное \_ целое число, значение GL \_ и тип \_ float.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-164">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="cbd6e-165">*зависим*</span><span class="sxs-lookup"><span data-stu-id="cbd6e-165">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="cbd6e-166">Указатель на данные изображения в памяти.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-166">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbd6e-167">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbd6e-167">Return value</span></span>

<span data-ttu-id="cbd6e-168">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-168">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cbd6e-169">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="cbd6e-169">Error codes</span></span>

<span data-ttu-id="cbd6e-170">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-170">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="cbd6e-171">Имя</span><span class="sxs-lookup"><span data-stu-id="cbd6e-171">Name</span></span>                                                                                                  | <span data-ttu-id="cbd6e-172">Значение</span><span class="sxs-lookup"><span data-stu-id="cbd6e-172">Meaning</span></span>                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cbd6e-173"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-173"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="cbd6e-174">*целевой объект* не был GL \_ текстуры \_ 1d.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-174">*target* was not GL\_TEXTURE\_1D.</span></span><br/>                                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="cbd6e-175"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-175"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="cbd6e-176">*Формат* не является допустимой константой.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-176">*format* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="cbd6e-177"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-177"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="cbd6e-178">*тип* не является допустимой константой.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-178">*type* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="cbd6e-179"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-179"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="cbd6e-180">*тип* — это \_ точечный рисунок и *Формат* , отличный от \_ индекса цвета GL \_ .</span><span class="sxs-lookup"><span data-stu-id="cbd6e-180">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="cbd6e-181"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-181"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="cbd6e-182">*уровень* был меньше нуля или больше log2 *Max*, где *Max* было возвращено значение \_ максимального \_ размера текстуры GL \_ .</span><span class="sxs-lookup"><span data-stu-id="cbd6e-182">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="cbd6e-183"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-183"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="cbd6e-184">*ксоффсет* меньше *b*, или   +  *Ширина* смещения больше *WB*, где *w* — \_ Ширина текстуры GL \_ , а *b* — ширина \_ границы текстуры текстуры \_ для изменяемого изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-184">*xoffset* was less than *b*, or *offset* + *width* was greater than *wb*, where *w* is the GL\_TEXTURE\_WIDTH, and *b* is the width of the GL\_TEXTURE\_BORDER of the texture image being modified.</span></span><br/> <span data-ttu-id="cbd6e-185">Обратите внимание, что *w* включает в себя вдвое ширину границы.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-185">Note that *w* includes twice the border width.</span></span><br/> |
| <dl> <span data-ttu-id="cbd6e-186"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-186"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="cbd6e-187">*Ширина* была меньше *b*, где *b* — ширина границы массива текстуры.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-187">*width* was was less than *b*, where *b* is the border width of the texture array.</span></span><br/>                                                                                                                                                                            |
| <dl> <span data-ttu-id="cbd6e-188"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-188"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="cbd6e-189">*граница* не равна нулю или 1.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-189">*border* was not zero or 1.</span></span><br/>                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="cbd6e-190"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-190"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="cbd6e-191">Массив тексуре не был определен предыдущей операцией **glTexImage1D** .</span><span class="sxs-lookup"><span data-stu-id="cbd6e-191">The texure array was not defined by a previous **glTexImage1D** operation.</span></span><br/>                                                                                                                                                                                    |
| <dl> <span data-ttu-id="cbd6e-192"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-192"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="cbd6e-193">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="cbd6e-193">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="cbd6e-194">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cbd6e-194">Remarks</span></span>

<span data-ttu-id="cbd6e-195">Одномерный текстурирование для примитива включается с помощью [**гленабле**](glenable.md) и **глдисабле** с аргументом GL \_ текстуры \_ 1d.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-195">One-dimensional texturing for a primitive is enabled using [**glEnable**](glenable.md) and **glDisable** with the argument GL\_TEXTURE\_1D.</span></span> <span data-ttu-id="cbd6e-196">Во время текстурирования часть указанного изображения текстуры сопоставляется с каждым включенным примитивом.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-196">During texturing, part of a specified texture image is mapped into each enabled primitive.</span></span> <span data-ttu-id="cbd6e-197">Используйте функцию **glTexSubImage1D** для указания непрерывного подобраза существующего одномерного изображения текстуры для текстурирования.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-197">You use the **glTexSubImage1D** function to specify a contiguous sub-image of an existing one-dimensional texture image for texturing.</span></span>

<span data-ttu-id="cbd6e-198">Пикселей текстуры, на который ссылается *точка* , заменяет область существующего массива текстуры на *x* индексов *ксоффсет* и *ксоффсет* + (*Width* 1) включительно.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-198">The texels referenced by *pixels* replace a region of the existing texture array with *x* indexes of *xoffset* and *xoffset* + (*width* 1) inclusive.</span></span> <span data-ttu-id="cbd6e-199">Этот регион не может включать пикселей текстуры за пределами диапазона изначально заданного массива текстуры.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-199">This region cannot include any texels outside the range of the originally specified texture array.</span></span>

<span data-ttu-id="cbd6e-200">Задание подобраза с нулевой *шириной* не влияет и не приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-200">Specifying a sub-image with a *width* of zero has no effect and does not generate an error.</span></span>

<span data-ttu-id="cbd6e-201">Текстурирование не влияет на режим индексирования цветов.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-201">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="cbd6e-202">Как правило, изображения текстур могут быть представлены теми же форматами данных, что и Пиксели в команде [**глдравпикселс**](gldrawpixels.md) , за исключением того, что \_ \_ нельзя использовать индекс трафарета GL и \_ компонент глубины GL \_ .</span><span class="sxs-lookup"><span data-stu-id="cbd6e-202">In general, texture images can be represented by the same data formats as the pixels in a [**glDrawPixels**](gldrawpixels.md) command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="cbd6e-203">Режимы [**глпикселсторе**](glpixelstore-functions.md) и [**глпикселтрансфер**](glpixeltransfer.md) влияют на изображения текстур точно так же, как они влияют на **глдравпикселс**.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-203">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="cbd6e-204">Следующие функции извлекают сведения, относящиеся к **glTexSubImage1D**:</span><span class="sxs-lookup"><span data-stu-id="cbd6e-204">The following functions retrieve information related to **glTexSubImage1D**:</span></span>

[<span data-ttu-id="cbd6e-205">**глжеттексимаже**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-205">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="cbd6e-206">[**глисенаблед**](glisenabled.md) с аргументом GL \_ текстура \_ 1d</span><span class="sxs-lookup"><span data-stu-id="cbd6e-206">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="cbd6e-207">Требования</span><span class="sxs-lookup"><span data-stu-id="cbd6e-207">Requirements</span></span>



| <span data-ttu-id="cbd6e-208">Требование</span><span class="sxs-lookup"><span data-stu-id="cbd6e-208">Requirement</span></span> | <span data-ttu-id="cbd6e-209">Значение</span><span class="sxs-lookup"><span data-stu-id="cbd6e-209">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbd6e-210">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cbd6e-210">Minimum supported client</span></span><br/> | <span data-ttu-id="cbd6e-211">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cbd6e-211">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cbd6e-212">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cbd6e-212">Minimum supported server</span></span><br/> | <span data-ttu-id="cbd6e-213">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cbd6e-213">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cbd6e-214">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cbd6e-214">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbd6e-215"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-215"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cbd6e-216">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cbd6e-216">Library</span></span><br/>                  | <dl> <span data-ttu-id="cbd6e-217"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-217"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cbd6e-218">DLL</span><span class="sxs-lookup"><span data-stu-id="cbd6e-218">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbd6e-219"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbd6e-219"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbd6e-220">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbd6e-220">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbd6e-221">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-221">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="cbd6e-222">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-222">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="cbd6e-223">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-223">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="cbd6e-224">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-224">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="cbd6e-225">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-225">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="cbd6e-226">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-226">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="cbd6e-227">**глфог**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-227">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="cbd6e-228">**глжеттексимаже**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-228">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="cbd6e-229">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-229">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="cbd6e-230">**глпикселсторе**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-230">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="cbd6e-231">**глпикселтрансфер**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-231">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="cbd6e-232">**глтексенв**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-232">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="cbd6e-233">**глтексжен**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-233">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="cbd6e-234">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-234">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="cbd6e-235">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-235">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="cbd6e-236">**глтекспараметер**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-236">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> <dt>

[<span data-ttu-id="cbd6e-237">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-237">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





