---
title: Функция gluBuild1DMipmaps (GLU. h)
description: Функция gluBuild1DMipmaps создает 1-D MIP-карты.
ms.assetid: 52ed924f-7a72-4458-b1b8-8e5d3021f60a
keywords:
- Функция gluBuild1DMipmaps OpenGL
topic_type:
- apiref
api_name:
- gluBuild1DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 089357488c7eae18e26258018473e9008fb29d24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672596"
---
# <a name="glubuild1dmipmaps-function"></a><span data-ttu-id="2b267-104">Функция gluBuild1DMipmaps</span><span class="sxs-lookup"><span data-stu-id="2b267-104">gluBuild1DMipmaps function</span></span>

<span data-ttu-id="2b267-105">Функция **gluBuild1DMipmaps** создает 1-D MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="2b267-105">The **gluBuild1DMipmaps** function creates 1-D mipmaps.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b267-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b267-106">Syntax</span></span>


```C++
void WINAPI gluBuild1DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a><span data-ttu-id="2b267-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b267-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b267-108">*target*</span><span class="sxs-lookup"><span data-stu-id="2b267-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="2b267-109">Целевая текстура.</span><span class="sxs-lookup"><span data-stu-id="2b267-109">The target texture.</span></span> <span data-ttu-id="2b267-110">Должен быть \_ \_ одномерной текстурой GL.</span><span class="sxs-lookup"><span data-stu-id="2b267-110">Must be GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="2b267-111">*компонента*</span><span class="sxs-lookup"><span data-stu-id="2b267-111">*components*</span></span> 
</dt> <dd>

<span data-ttu-id="2b267-112">Число компонентов цвета в текстуре.</span><span class="sxs-lookup"><span data-stu-id="2b267-112">The number of color components in the texture.</span></span> <span data-ttu-id="2b267-113">Должно быть равно 1, 2, 3 или 4.</span><span class="sxs-lookup"><span data-stu-id="2b267-113">Must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="2b267-114">*width*</span><span class="sxs-lookup"><span data-stu-id="2b267-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="2b267-115">Ширина изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="2b267-115">The width of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="2b267-116">*format*</span><span class="sxs-lookup"><span data-stu-id="2b267-116">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="2b267-117">Формат точечных данных.</span><span class="sxs-lookup"><span data-stu-id="2b267-117">The format of the pixel data.</span></span> <span data-ttu-id="2b267-118">Допустимы следующие значения: " \_ индекс цвета GL" \_ , " \_ Красная \_ \_ строка \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ ", "красный", "зеленый", "синий", "голубой", "GL", "красное", "GL", "GL", "BGR", "Расш.</span><span class="sxs-lookup"><span data-stu-id="2b267-118">The following values are valid: GL\_COLOR\_INDEX, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, or GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="2b267-119">*type*</span><span class="sxs-lookup"><span data-stu-id="2b267-119">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="2b267-120">Тип данных для *данных*.</span><span class="sxs-lookup"><span data-stu-id="2b267-120">The data type for *data*.</span></span> <span data-ttu-id="2b267-121">Допустимы следующие значения: \_ НЕподписанный байт, байт GL, формат GL, формат GL \_ \_ \_ \_ без знака \_ Short, краткое название GL, \_ \_ Неподписанное целое число без знака, значение GL, \_ \_ а также тип \_ float.</span><span class="sxs-lookup"><span data-stu-id="2b267-121">The following values are valid: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="2b267-122">*data*</span><span class="sxs-lookup"><span data-stu-id="2b267-122">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="2b267-123">Указатель на данные изображения в памяти.</span><span class="sxs-lookup"><span data-stu-id="2b267-123">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b267-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b267-124">Return value</span></span>

<span data-ttu-id="2b267-125">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2b267-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b267-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b267-126">Remarks</span></span>

<span data-ttu-id="2b267-127">Функция **gluBuild1DMipmaps** получает входной образ и создает все образы mipmap (с помощью [**глускалеимаже**](gluscaleimage.md)), чтобы входной образ можно было использовать в качестве изображения текстуры мипмаппед.</span><span class="sxs-lookup"><span data-stu-id="2b267-127">The **gluBuild1DMipmaps** function obtains the input image and generates all mipmap images (using [**gluScaleImage**](gluscaleimage.md)) so that the input image can be used as a mipmapped texture image.</span></span> <span data-ttu-id="2b267-128">Затем вызывается функция [**glTexImage1D**](glteximage1d.md) для загрузки каждого изображения.</span><span class="sxs-lookup"><span data-stu-id="2b267-128">The [**glTexImage1D**](glteximage1d.md) function is then called to load each of the images.</span></span> <span data-ttu-id="2b267-129">Если ширина входного изображения не является степенью двух, то изображение масштабируется до ближайшей степени числа двух перед созданием MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="2b267-129">If the width of the input image is not a power of two, then the image is scaled to the nearest power of two before the mipmaps are generated.</span></span>

<span data-ttu-id="2b267-130">Возвращаемое значение, равное нулю, указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="2b267-130">A return value of zero indicates success.</span></span> <span data-ttu-id="2b267-131">В противном случае возвращается код ошибки GLU (см. [**глуеррорстринг**](gluerrorstring.md)).</span><span class="sxs-lookup"><span data-stu-id="2b267-131">Otherwise, a GLU error code is returned (see [**gluErrorString**](gluerrorstring.md)).</span></span>

<span data-ttu-id="2b267-132">Описание допустимых значений параметра *Format* см. в разделе **glTexImage1D**.</span><span class="sxs-lookup"><span data-stu-id="2b267-132">For a description of the acceptable values for the *format* parameter, see **glTexImage1D**.</span></span> <span data-ttu-id="2b267-133">Описание допустимых значений параметра *типа* см. в разделе [**глдравпикселс**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="2b267-133">For a description of the acceptable values for the *type* parameter, see [**glDrawPixels**](gldrawpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b267-134">Требования</span><span class="sxs-lookup"><span data-stu-id="2b267-134">Requirements</span></span>



| <span data-ttu-id="2b267-135">Требование</span><span class="sxs-lookup"><span data-stu-id="2b267-135">Requirement</span></span> | <span data-ttu-id="2b267-136">Значение</span><span class="sxs-lookup"><span data-stu-id="2b267-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2b267-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b267-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2b267-138">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2b267-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2b267-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b267-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2b267-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2b267-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2b267-141">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2b267-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b267-142"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b267-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="2b267-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2b267-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="2b267-144"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b267-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2b267-145">DLL</span><span class="sxs-lookup"><span data-stu-id="2b267-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b267-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b267-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b267-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b267-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b267-148">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="2b267-148">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="2b267-149">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="2b267-149">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="2b267-150">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="2b267-150">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="2b267-151">**глускалеимаже**</span><span class="sxs-lookup"><span data-stu-id="2b267-151">**gluScaleImage**</span></span>](gluscaleimage.md)
</dt> </dl>

 

 





