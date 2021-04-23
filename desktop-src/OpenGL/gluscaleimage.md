---
title: Функция Глускалеимаже (GLU. h)
description: Функция Глускалеимаже масштабирует изображение до произвольного размера.
ms.assetid: f47191e8-b22d-4f6a-949a-9c7782d6d338
keywords:
- Функция Глускалеимаже OpenGL
topic_type:
- apiref
api_name:
- gluScaleImage
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da95f1545996a83adeb27deaceb7fab6290005e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414712"
---
# <a name="gluscaleimage-function"></a><span data-ttu-id="4b5ae-104">Функция Глускалеимаже</span><span class="sxs-lookup"><span data-stu-id="4b5ae-104">gluScaleImage function</span></span>

<span data-ttu-id="4b5ae-105">Функция **глускалеимаже** масштабирует изображение до произвольного размера.</span><span class="sxs-lookup"><span data-stu-id="4b5ae-105">The **gluScaleImage** function scales an image to an arbitrary size.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b5ae-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b5ae-106">Syntax</span></span>


```C++
int WINAPI gluScaleImage(
         GLenum format,
         GLint  widthin,
         GLint  heightin,
         GLenum typein,
   const void   *datain,
         GLint  widthout,
         GLint  heightout,
         GLenum typeout,
         void   *dataout
);
```



## <a name="parameters"></a><span data-ttu-id="4b5ae-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b5ae-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b5ae-108">*format*</span><span class="sxs-lookup"><span data-stu-id="4b5ae-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="4b5ae-109">Формат точечных данных.</span><span class="sxs-lookup"><span data-stu-id="4b5ae-109">The format of the pixel data.</span></span> <span data-ttu-id="4b5ae-110">Следующие символьные значения являются допустимыми: \_ индекс цвета GL \_ , \_ индекс трафарета GL, \_ \_ компонент глубины GL \_ , \_ красный, \_ зеленый \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ , GL, GL, GL, ГК, GL, ГК, GL, GL</span><span class="sxs-lookup"><span data-stu-id="4b5ae-110">The following symbolic values are valid: GL\_COLOR\_INDEX, GL\_STENCIL\_INDEX, GL\_DEPTH\_COMPONENT, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, and GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="4b5ae-111">*ширина*</span><span class="sxs-lookup"><span data-stu-id="4b5ae-111">*widthin*</span></span> 
</dt> <dd>

<span data-ttu-id="4b5ae-112">Ширина масштабируемого исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="4b5ae-112">The width of the source image that is scaled.</span></span>

</dd> <dt>

<span data-ttu-id="4b5ae-113">*Высота*</span><span class="sxs-lookup"><span data-stu-id="4b5ae-113">*heightin*</span></span> 
</dt> <dd>

<span data-ttu-id="4b5ae-114">Высота масштабированного исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="4b5ae-114">The height of the source image that is scaled.</span></span>

</dd> <dt>

<span data-ttu-id="4b5ae-115">*Тип*</span><span class="sxs-lookup"><span data-stu-id="4b5ae-115">*typein*</span></span> 
</dt> <dd>

<span data-ttu-id="4b5ae-116">Тип данных для *данных*.</span><span class="sxs-lookup"><span data-stu-id="4b5ae-116">The data type for *datain*.</span></span> <span data-ttu-id="4b5ae-117">Значение должно быть одним из следующих: \_ НЕподписанный \_ байт, байт ГК \_ , \_ точечный рисунок GL, GL \_ без знака \_ Short, краткое название GL, \_ \_ Неподписанное \_ целое число без знака, GL \_ или GL \_ .</span><span class="sxs-lookup"><span data-stu-id="4b5ae-117">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="4b5ae-118">*данные*</span><span class="sxs-lookup"><span data-stu-id="4b5ae-118">*datain*</span></span> 
</dt> <dd>

<span data-ttu-id="4b5ae-119">Указатель на исходное изображение.</span><span class="sxs-lookup"><span data-stu-id="4b5ae-119">A pointer to the source image.</span></span>

</dd> <dt>

<span data-ttu-id="4b5ae-120">*ширина*</span><span class="sxs-lookup"><span data-stu-id="4b5ae-120">*widthout*</span></span> 
</dt> <dd>

<span data-ttu-id="4b5ae-121">Ширина конечного изображения.</span><span class="sxs-lookup"><span data-stu-id="4b5ae-121">The width of the destination image.</span></span>

</dd> <dt>

<span data-ttu-id="4b5ae-122">*Высота*</span><span class="sxs-lookup"><span data-stu-id="4b5ae-122">*heightout*</span></span> 
</dt> <dd>

<span data-ttu-id="4b5ae-123">Высота конечного изображения.</span><span class="sxs-lookup"><span data-stu-id="4b5ae-123">The height of the destination image.</span></span>

</dd> <dt>

<span data-ttu-id="4b5ae-124">*Тип*</span><span class="sxs-lookup"><span data-stu-id="4b5ae-124">*typeout*</span></span> 
</dt> <dd>

<span data-ttu-id="4b5ae-125">Тип данных для *данных*.</span><span class="sxs-lookup"><span data-stu-id="4b5ae-125">The data type for *dataout*.</span></span> <span data-ttu-id="4b5ae-126">Значение должно быть одним из следующих: \_ НЕподписанный \_ байт, байт ГК \_ , \_ точечный рисунок GL, GL \_ без знака \_ Short, краткое название GL, \_ \_ Неподписанное \_ целое число без знака, GL \_ или GL \_ .</span><span class="sxs-lookup"><span data-stu-id="4b5ae-126">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="4b5ae-127">*данные*</span><span class="sxs-lookup"><span data-stu-id="4b5ae-127">*dataout*</span></span> 
</dt> <dd>

<span data-ttu-id="4b5ae-128">Указатель на изображение назначения.</span><span class="sxs-lookup"><span data-stu-id="4b5ae-128">A pointer to the destination image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b5ae-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b5ae-129">Return value</span></span>

<span data-ttu-id="4b5ae-130">Если вызов функции заканчивается удачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="4b5ae-130">If the function succeeds, the return value is zero.</span></span>

<span data-ttu-id="4b5ae-131">Если функция завершается ошибкой, возвращаемое значение является кодом ошибки GLU (см. [**глуеррорстринг**](gluerrorstring.md)).</span><span class="sxs-lookup"><span data-stu-id="4b5ae-131">If the function fails, the return value is a GLU error code (see [**gluErrorString**](gluerrorstring.md)).</span></span>

## <a name="remarks"></a><span data-ttu-id="4b5ae-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b5ae-132">Remarks</span></span>

<span data-ttu-id="4b5ae-133">Функция **глускалеимаже** масштабирует изображение пикселя с помощью соответствующих режимов хранилища пикселей для распаковки данных из исходного изображения и упаковки данных в целевое изображение.</span><span class="sxs-lookup"><span data-stu-id="4b5ae-133">The **gluScaleImage** function scales a pixel image using the appropriate pixel store modes to unpack data from the source image and pack data into the destination image.</span></span>

<span data-ttu-id="4b5ae-134">При сжатии изображения **глускалеимаже** использует фильтр Box для выборки исходного изображения и создания пикселов для конечного изображения.</span><span class="sxs-lookup"><span data-stu-id="4b5ae-134">When shrinking an image, **gluScaleImage** uses a box filter to sample the source image and create pixels for the destination image.</span></span> <span data-ttu-id="4b5ae-135">При увеличении изображения пиксели из исходного изображения линейно интерполируются для создания конечного изображения.</span><span class="sxs-lookup"><span data-stu-id="4b5ae-135">When magnifying an image, the pixels from the source image are linearly interpolated to create the destination image.</span></span>

<span data-ttu-id="4b5ae-136">Описание допустимых значений для параметров *Format*, *Type* и *Type* , см. в разделе [**глреадпикселс**](glreadpixels.md).</span><span class="sxs-lookup"><span data-stu-id="4b5ae-136">For a description of the acceptable values for the *format*, *typein*, and *typeout* parameters, see [**glReadPixels**](glreadpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b5ae-137">Требования</span><span class="sxs-lookup"><span data-stu-id="4b5ae-137">Requirements</span></span>



| <span data-ttu-id="4b5ae-138">Требование</span><span class="sxs-lookup"><span data-stu-id="4b5ae-138">Requirement</span></span> | <span data-ttu-id="4b5ae-139">Значение</span><span class="sxs-lookup"><span data-stu-id="4b5ae-139">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4b5ae-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b5ae-140">Minimum supported client</span></span><br/> | <span data-ttu-id="4b5ae-141">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4b5ae-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4b5ae-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b5ae-142">Minimum supported server</span></span><br/> | <span data-ttu-id="4b5ae-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4b5ae-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4b5ae-144">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4b5ae-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b5ae-145"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b5ae-145"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="4b5ae-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4b5ae-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="4b5ae-147"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b5ae-147"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4b5ae-148">DLL</span><span class="sxs-lookup"><span data-stu-id="4b5ae-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b5ae-149"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b5ae-149"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b5ae-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b5ae-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b5ae-151">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="4b5ae-151">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="4b5ae-152">**глреадпикселс**</span><span class="sxs-lookup"><span data-stu-id="4b5ae-152">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="4b5ae-153">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="4b5ae-153">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="4b5ae-154">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="4b5ae-154">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="4b5ae-155">**глуеррорстринг**</span><span class="sxs-lookup"><span data-stu-id="4b5ae-155">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> </dl>

 

 





