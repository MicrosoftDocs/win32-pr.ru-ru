---
title: Перечисление D3DX11_IMAGE_FILE_FORMAT (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Форматы файлов изображений, поддерживаемые функциями D3DX11Createxxx и D3DX11Savexxx.
ms.assetid: 89fa9ab8-3be0-4dc5-a533-94edb01df36a
keywords:
- Перечисление D3DX11_IMAGE_FILE_FORMAT Direct3D 11
- Указатель перечисления LPD3DX11_IMAGE_FILE_FORMAT Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_FILE_FORMAT
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 730ce59bb8a07f3fd8ef78bbeb27b4d01d198f7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987218"
---
# <a name="d3dx11_image_file_format-enumeration"></a><span data-ttu-id="8293a-106">\_ \_ Перечисление форматов файлов изображений D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="8293a-106">D3DX11\_IMAGE\_FILE\_FORMAT enumeration</span></span>

> [!Note]  
> <span data-ttu-id="8293a-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="8293a-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="8293a-108">Форматы файлов изображений, поддерживаемые функциями D3DX11Createxxx и D3DX11Savexxx.</span><span class="sxs-lookup"><span data-stu-id="8293a-108">Image file formats supported by D3DX11Createxxx and D3DX11Savexxx functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="8293a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8293a-109">Syntax</span></span>


```C++
typedef enum D3DX11_IMAGE_FILE_FORMAT { 
  D3DX11_IFF_BMP          = 0,
  D3DX11_IFF_JPG          = 1,
  D3DX11_IFF_PNG          = 3,
  D3DX11_IFF_DDS          = 4,
  D3DX11_IFF_TIFF         = 10,
  D3DX11_IFF_GIF          = 11,
  D3DX11_IFF_WMP          = 12,
  D3DX11_IFF_FORCE_DWORD  = 0x7fffffff
} D3DX11_IMAGE_FILE_FORMAT, *LPD3DX11_IMAGE_FILE_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="8293a-110">Константы</span><span class="sxs-lookup"><span data-stu-id="8293a-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8293a-111"><span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11 \_ одиночная \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="8293a-111"><span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11\_IFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="8293a-112">Формат файла точечного рисунка Windows (BMP).</span><span class="sxs-lookup"><span data-stu-id="8293a-112">Windows bitmap (BMP) file format.</span></span> <span data-ttu-id="8293a-113">Содержит заголовок, описывающий разрешение устройства, на котором создавался прямоугольник пикселей, размеры прямоугольника, размер массива битов, логическую палитру и массив битов, определяющих связь между пикселями в изображении точечного рисунка и записями в логической палитре.</span><span class="sxs-lookup"><span data-stu-id="8293a-113">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> <span data-ttu-id="8293a-114">Расширение файла для этого формата —. bmp.</span><span class="sxs-lookup"><span data-stu-id="8293a-114">The file extension for this format is .bmp.</span></span>

</dd> <dt>

<span data-ttu-id="8293a-115"><span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**D3DX11 \_ одиночная \_ JPG**</span><span class="sxs-lookup"><span data-stu-id="8293a-115"><span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**D3DX11\_IFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="8293a-116">Формат сжатых файлов в формате JPEG.</span><span class="sxs-lookup"><span data-stu-id="8293a-116">Joint Photographic Experts Group (JPEG) compressed file format.</span></span> <span data-ttu-id="8293a-117">Указывает сжатие переменных в 24-разрядном RGB-цвете и 8-битных изображениях изображений в формате TIFF с тегом оттенков серого.</span><span class="sxs-lookup"><span data-stu-id="8293a-117">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span> <span data-ttu-id="8293a-118">Расширение файла для этого формата — JPG.</span><span class="sxs-lookup"><span data-stu-id="8293a-118">The file extension for this format is .jpg.</span></span>

</dd> <dt>

<span data-ttu-id="8293a-119"><span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**D3DX11 \_ одиночная \_ PNG**</span><span class="sxs-lookup"><span data-stu-id="8293a-119"><span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**D3DX11\_IFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="8293a-120">Формат PNG-файла.</span><span class="sxs-lookup"><span data-stu-id="8293a-120">Portable Network Graphics (PNG) file format.</span></span> <span data-ttu-id="8293a-121">Нечастный формат точечного рисунка, использующий сжатие без потерь.</span><span class="sxs-lookup"><span data-stu-id="8293a-121">A non-proprietary bitmap format using lossless compression.</span></span> <span data-ttu-id="8293a-122">Расширение файла для этого формата —. png.</span><span class="sxs-lookup"><span data-stu-id="8293a-122">The file extension for this format is .png.</span></span>

</dd> <dt>

<span data-ttu-id="8293a-123"><span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11 \_ одиночная \_ DDS**</span><span class="sxs-lookup"><span data-stu-id="8293a-123"><span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11\_IFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="8293a-124">Формат файла поверхности DirectDraw (DDS).</span><span class="sxs-lookup"><span data-stu-id="8293a-124">DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="8293a-125">Сохраняет текстуры, текстуры тома и карты кубических сред, с уровнями mipmap и без него, а также с сжатием пикселов или без него.</span><span class="sxs-lookup"><span data-stu-id="8293a-125">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="8293a-126">Расширение файла для этого формата — DDS.</span><span class="sxs-lookup"><span data-stu-id="8293a-126">The file extension for this format is .dds.</span></span>

</dd> <dt>

<span data-ttu-id="8293a-127"><span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**D3DX11 \_ одиночная \_ TIFF**</span><span class="sxs-lookup"><span data-stu-id="8293a-127"><span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**D3DX11\_IFF\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="8293a-128">Формат файла изображения с тегами (TIFF).</span><span class="sxs-lookup"><span data-stu-id="8293a-128">Tagged Image File Format (TIFF).</span></span> <span data-ttu-id="8293a-129">Расширения файлов для этого формата: TIF и TIFF.</span><span class="sxs-lookup"><span data-stu-id="8293a-129">The file extensions for this format are .tif and .tiff.</span></span>

</dd> <dt>

<span data-ttu-id="8293a-130"><span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**D3DX11 \_ одиночная \_ GIF**</span><span class="sxs-lookup"><span data-stu-id="8293a-130"><span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**D3DX11\_IFF\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="8293a-131">Формат GIF.</span><span class="sxs-lookup"><span data-stu-id="8293a-131">Graphics Interchange Format (GIF).</span></span> <span data-ttu-id="8293a-132">Расширение файла для этого формата — GIF.</span><span class="sxs-lookup"><span data-stu-id="8293a-132">The file extension for this format is .gif.</span></span>

</dd> <dt>

<span data-ttu-id="8293a-133"><span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**D3DX11 \_ одиночная \_ WMP**</span><span class="sxs-lookup"><span data-stu-id="8293a-133"><span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**D3DX11\_IFF\_WMP**</span></span>
</dt> <dd>

<span data-ttu-id="8293a-134">Формат Фото Windows Media (WMP).</span><span class="sxs-lookup"><span data-stu-id="8293a-134">Windows Media Photo format (WMP).</span></span> <span data-ttu-id="8293a-135">Этот формат также известен как Фото HD и JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="8293a-135">This format is also known as HD Photo and JPEG XR.</span></span> <span data-ttu-id="8293a-136">Расширения файлов для этого формата:. hdp,. жкср и. формате WDP.</span><span class="sxs-lookup"><span data-stu-id="8293a-136">The file extensions for this format are .hdp, .jxr, and .wdp.</span></span>

<span data-ttu-id="8293a-137">Для правильной работы **D3DX11 \_ одиночная \_ WMP** требует инициализировать COM.</span><span class="sxs-lookup"><span data-stu-id="8293a-137">To work properly, **D3DX11\_IFF\_WMP** requires that you initialize COM.</span></span> <span data-ttu-id="8293a-138">Поэтому вызовите [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) или [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) в приложении перед вызовом D3DX.</span><span class="sxs-lookup"><span data-stu-id="8293a-138">Therefore, call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) in your application before you call D3DX.</span></span>

</dd> <dt>

<span data-ttu-id="8293a-139"><span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11 \_ одиночная \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8293a-139"><span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11\_IFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="8293a-140">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="8293a-140">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="8293a-141">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="8293a-141">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="8293a-142">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="8293a-142">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8293a-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="8293a-143">Remarks</span></span>

<span data-ttu-id="8293a-144">Дополнительные сведения о некоторых из этих форматов см. в разделе [Типы точечных рисунков (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .</span><span class="sxs-lookup"><span data-stu-id="8293a-144">See [Types of Bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="8293a-145">Требования</span><span class="sxs-lookup"><span data-stu-id="8293a-145">Requirements</span></span>



| <span data-ttu-id="8293a-146">Требование</span><span class="sxs-lookup"><span data-stu-id="8293a-146">Requirement</span></span> | <span data-ttu-id="8293a-147">Значение</span><span class="sxs-lookup"><span data-stu-id="8293a-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8293a-148">Header</span><span class="sxs-lookup"><span data-stu-id="8293a-148">Header</span></span><br/> | <dl> <span data-ttu-id="8293a-149"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="8293a-149"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8293a-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8293a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8293a-151">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="8293a-151">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

