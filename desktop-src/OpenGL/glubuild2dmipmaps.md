---
title: Функция gluBuild2DMipmaps (GLU. h)
description: Функция gluBuild2DMipmaps создает 2-D MIP-карты.
ms.assetid: ea19a9b0-baf7-436f-afd5-609bc364b3ba
keywords:
- Функция gluBuild2DMipmaps OpenGL
topic_type:
- apiref
api_name:
- gluBuild2DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92402792e41701711e99f469ead67410d6a8c1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988356"
---
# <a name="glubuild2dmipmaps-function"></a><span data-ttu-id="7a03b-104">Функция gluBuild2DMipmaps</span><span class="sxs-lookup"><span data-stu-id="7a03b-104">gluBuild2DMipmaps function</span></span>

<span data-ttu-id="7a03b-105">Функция **gluBuild2DMipmaps** создает 2-D MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="7a03b-105">The **gluBuild2DMipmaps** function creates 2-D mipmaps.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a03b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a03b-106">Syntax</span></span>


```C++
void WINAPI gluBuild2DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLInt  height,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a><span data-ttu-id="7a03b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a03b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a03b-108">*target*</span><span class="sxs-lookup"><span data-stu-id="7a03b-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="7a03b-109">Целевая текстура.</span><span class="sxs-lookup"><span data-stu-id="7a03b-109">The target texture.</span></span> <span data-ttu-id="7a03b-110">Должно быть \_ 2D-текстура GL \_ .</span><span class="sxs-lookup"><span data-stu-id="7a03b-110">Must be GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="7a03b-111">*компонента*</span><span class="sxs-lookup"><span data-stu-id="7a03b-111">*components*</span></span> 
</dt> <dd>

<span data-ttu-id="7a03b-112">Число компонентов цвета в текстуре.</span><span class="sxs-lookup"><span data-stu-id="7a03b-112">The number of color components in the texture.</span></span> <span data-ttu-id="7a03b-113">Должно быть равно 1, 2, 3 или 4.</span><span class="sxs-lookup"><span data-stu-id="7a03b-113">Must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="7a03b-114">*width*</span><span class="sxs-lookup"><span data-stu-id="7a03b-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="7a03b-115">Ширина изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="7a03b-115">The width of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="7a03b-116">*height*</span><span class="sxs-lookup"><span data-stu-id="7a03b-116">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="7a03b-117">Высота изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="7a03b-117">The height of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="7a03b-118">*format*</span><span class="sxs-lookup"><span data-stu-id="7a03b-118">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="7a03b-119">Формат точечных данных.</span><span class="sxs-lookup"><span data-stu-id="7a03b-119">The format of the pixel data.</span></span> <span data-ttu-id="7a03b-120">Должно быть одним из следующих: индекс цвета GL, красный, зеленый, GL, GL, ГК, красное, GL, GL, GL, ГК, BGR ext, GL, BGRA, GL или цветная \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ светимость GL \_ .</span><span class="sxs-lookup"><span data-stu-id="7a03b-120">Must be one of the following: GL\_COLOR\_INDEX, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, or GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="7a03b-121">*type*</span><span class="sxs-lookup"><span data-stu-id="7a03b-121">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="7a03b-122">Тип данных для *данных*.</span><span class="sxs-lookup"><span data-stu-id="7a03b-122">The data type for *data*.</span></span> <span data-ttu-id="7a03b-123">Значение должно быть одним из следующих: \_ НЕподписанный \_ байт, байт ГК \_ , \_ точечный рисунок GL, GL \_ без знака \_ Short, краткое название GL, \_ \_ Неподписанное \_ целое число без знака, GL \_ или GL \_ .</span><span class="sxs-lookup"><span data-stu-id="7a03b-123">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="7a03b-124">*data*</span><span class="sxs-lookup"><span data-stu-id="7a03b-124">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="7a03b-125">Указатель на данные изображения в памяти.</span><span class="sxs-lookup"><span data-stu-id="7a03b-125">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a03b-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a03b-126">Return value</span></span>

<span data-ttu-id="7a03b-127">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7a03b-127">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a03b-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a03b-128">Remarks</span></span>

<span data-ttu-id="7a03b-129">Функция **gluBuild2DMipmaps** получает входной образ и создает все образы mipmap (с помощью [**глускалеимаже**](gluscaleimage.md)), поэтому входной образ можно использовать в качестве изображения текстуры мипмаппед.</span><span class="sxs-lookup"><span data-stu-id="7a03b-129">The **gluBuild2DMipmaps** function obtains the input image and generates all mipmap images (using [**gluScaleImage**](gluscaleimage.md)) so the input image can be used as a mipmapped texture image.</span></span> <span data-ttu-id="7a03b-130">Чтобы загрузить каждое изображение, вызовите [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="7a03b-130">To load each of the images, call [**glTexImage2D**](glteximage2d.md).</span></span> <span data-ttu-id="7a03b-131">Если размеры входного изображения не являются степенями двух, то изображение масштабируется таким образом, чтобы ширина и высота были степенями двух до создания MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="7a03b-131">If the dimensions of the input image are not powers of two, then the image is scaled so that both the width and height are powers of two before the mipmaps are generated.</span></span>

<span data-ttu-id="7a03b-132">Возвращаемое значение, равное нулю, указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="7a03b-132">A return value of zero indicates success.</span></span> <span data-ttu-id="7a03b-133">В противном случае возвращается код ошибки GLU (см. [**глуеррорстринг**](gluerrorstring.md)).</span><span class="sxs-lookup"><span data-stu-id="7a03b-133">Otherwise, a GLU error code is returned (see [**gluErrorString**](gluerrorstring.md)).</span></span>

<span data-ttu-id="7a03b-134">Описание допустимых значений параметра *Format* см. в разделе **glTexImage2D**.</span><span class="sxs-lookup"><span data-stu-id="7a03b-134">For a description of the acceptable values for the *format* parameter, see **glTexImage2D**.</span></span> <span data-ttu-id="7a03b-135">Описание допустимых значений для *типа* см. в разделе [**глдравпикселс**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="7a03b-135">For a description of the acceptable values for *type*, see [**glDrawPixels**](gldrawpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a03b-136">Требования</span><span class="sxs-lookup"><span data-stu-id="7a03b-136">Requirements</span></span>



| <span data-ttu-id="7a03b-137">Требование</span><span class="sxs-lookup"><span data-stu-id="7a03b-137">Requirement</span></span> | <span data-ttu-id="7a03b-138">Значение</span><span class="sxs-lookup"><span data-stu-id="7a03b-138">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7a03b-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a03b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7a03b-140">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7a03b-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7a03b-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a03b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7a03b-142">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7a03b-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7a03b-143">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7a03b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a03b-144"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a03b-144"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="7a03b-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7a03b-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="7a03b-146"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a03b-146"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7a03b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="7a03b-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a03b-148"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a03b-148"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a03b-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a03b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a03b-150">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="7a03b-150">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="7a03b-151">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="7a03b-151">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="7a03b-152">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="7a03b-152">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="7a03b-153">**глускалеимаже**</span><span class="sxs-lookup"><span data-stu-id="7a03b-153">**gluScaleImage**</span></span>](gluscaleimage.md)
</dt> </dl>

 

 





