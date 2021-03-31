---
description: Форматы файлов изображений, поддерживаемые функциями D3DXCreatexxx и D3DX10Savexxx.
ms.assetid: 39602f3c-5c91-4667-96d0-c3bdba712d88
title: Перечисление D3DX10_IMAGE_FILE_FORMAT (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_FILE_FORMAT
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: fba878a40f510cc5e76256161255e01deaa7ee04
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821372"
---
# <a name="d3dx10_image_file_format-enumeration"></a><span data-ttu-id="2b884-103">\_ \_ Перечисление форматов файлов изображений D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="2b884-103">D3DX10\_IMAGE\_FILE\_FORMAT enumeration</span></span>

<span data-ttu-id="2b884-104">Форматы файлов изображений, поддерживаемые функциями D3DXCreatexxx и D3DX10Savexxx.</span><span class="sxs-lookup"><span data-stu-id="2b884-104">Image file formats supported by D3DXCreatexxx and D3DX10Savexxx functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b884-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b884-105">Syntax</span></span>


```C++
typedef enum D3DX10_IMAGE_FILE_FORMAT { 
  D3DX10_IFF_BMP          = 0,
  D3DX10_IFF_JPG          = 1,
  D3DX10_IFF_PNG          = 3,
  D3DX10_IFF_DDS          = 4,
  D3DX10_IFF_TIFF         = 10,
  D3DX10_IFF_GIF          = 11,
  D3DX10_IFF_WMP          = 12,
  D3DX10_IFF_FORCE_DWORD  = 0x7fffffff
} D3DX10_IMAGE_FILE_FORMAT, *LPD3DX10_IMAGE_FILE_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="2b884-106">Константы</span><span class="sxs-lookup"><span data-stu-id="2b884-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2b884-107"><span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10 \_ одиночная \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="2b884-107"><span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10\_IFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="2b884-108">Формат файла точечного рисунка Windows (BMP).</span><span class="sxs-lookup"><span data-stu-id="2b884-108">Windows bitmap (BMP) file format.</span></span> <span data-ttu-id="2b884-109">Содержит заголовок, описывающий разрешение устройства, на котором создавался прямоугольник пикселей, размеры прямоугольника, размер массива битов, логическую палитру и массив битов, определяющих связь между пикселями в изображении точечного рисунка и записями в логической палитре.</span><span class="sxs-lookup"><span data-stu-id="2b884-109">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> <span data-ttu-id="2b884-110">Расширение файла для этого формата —. bmp.</span><span class="sxs-lookup"><span data-stu-id="2b884-110">The file extension for this format is .bmp.</span></span>

</dd> <dt>

<span data-ttu-id="2b884-111"><span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3DX10 \_ одиночная \_ JPG**</span><span class="sxs-lookup"><span data-stu-id="2b884-111"><span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3DX10\_IFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="2b884-112">Формат сжатых файлов в формате JPEG.</span><span class="sxs-lookup"><span data-stu-id="2b884-112">Joint Photographic Experts Group (JPEG) compressed file format.</span></span> <span data-ttu-id="2b884-113">Указывает сжатие переменных в 24-разрядном RGB-цвете и 8-битных изображениях изображений в формате TIFF с тегом оттенков серого.</span><span class="sxs-lookup"><span data-stu-id="2b884-113">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span> <span data-ttu-id="2b884-114">Расширение файла для этого формата — JPG.</span><span class="sxs-lookup"><span data-stu-id="2b884-114">The file extension for this format is .jpg.</span></span>

</dd> <dt>

<span data-ttu-id="2b884-115"><span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**D3DX10 \_ одиночная \_ PNG**</span><span class="sxs-lookup"><span data-stu-id="2b884-115"><span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**D3DX10\_IFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="2b884-116">Формат PNG-файла.</span><span class="sxs-lookup"><span data-stu-id="2b884-116">Portable Network Graphics (PNG) file format.</span></span> <span data-ttu-id="2b884-117">Нечастный формат точечного рисунка, использующий сжатие без потерь.</span><span class="sxs-lookup"><span data-stu-id="2b884-117">A non-proprietary bitmap format using lossless compression.</span></span> <span data-ttu-id="2b884-118">Расширение файла для этого формата —. png.</span><span class="sxs-lookup"><span data-stu-id="2b884-118">The file extension for this format is .png.</span></span>

</dd> <dt>

<span data-ttu-id="2b884-119"><span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10 \_ одиночная \_ DDS**</span><span class="sxs-lookup"><span data-stu-id="2b884-119"><span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10\_IFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="2b884-120">Формат файла поверхности DirectDraw (DDS).</span><span class="sxs-lookup"><span data-stu-id="2b884-120">DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="2b884-121">Сохраняет текстуры, текстуры тома и карты кубических сред, с уровнями mipmap и без него, а также с сжатием пикселов или без него.</span><span class="sxs-lookup"><span data-stu-id="2b884-121">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="2b884-122">Расширение файла для этого формата — DDS.</span><span class="sxs-lookup"><span data-stu-id="2b884-122">The file extension for this format is .dds.</span></span>

</dd> <dt>

<span data-ttu-id="2b884-123"><span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**D3DX10 \_ одиночная \_ TIFF**</span><span class="sxs-lookup"><span data-stu-id="2b884-123"><span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**D3DX10\_IFF\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="2b884-124">Формат файла изображения с тегами (TIFF).</span><span class="sxs-lookup"><span data-stu-id="2b884-124">Tagged Image File Format (TIFF).</span></span> <span data-ttu-id="2b884-125">Расширения файлов для этого формата: TIF и TIFF.</span><span class="sxs-lookup"><span data-stu-id="2b884-125">The file extensions for this format are .tif and .tiff.</span></span>

</dd> <dt>

<span data-ttu-id="2b884-126"><span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**D3DX10 \_ одиночная \_ GIF**</span><span class="sxs-lookup"><span data-stu-id="2b884-126"><span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**D3DX10\_IFF\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="2b884-127">Формат GIF. Расширение файла для этого формата — GIF.</span><span class="sxs-lookup"><span data-stu-id="2b884-127">Graphics Interchange Format (GIF).The file extension for this format is .gif.</span></span>

</dd> <dt>

<span data-ttu-id="2b884-128"><span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3DX10 \_ одиночная \_ WMP**</span><span class="sxs-lookup"><span data-stu-id="2b884-128"><span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3DX10\_IFF\_WMP**</span></span>
</dt> <dd>

<span data-ttu-id="2b884-129">Формат Фото Windows Media (WMP).</span><span class="sxs-lookup"><span data-stu-id="2b884-129">Windows Media Photo format (WMP).</span></span> <span data-ttu-id="2b884-130">Этот формат также известен как Фото HD и JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="2b884-130">This format is also known as HD Photo and JPEG XR.</span></span> <span data-ttu-id="2b884-131">Расширения файлов для этого формата:. hdp,. жкср и. формате WDP.</span><span class="sxs-lookup"><span data-stu-id="2b884-131">The file extensions for this format are .hdp, .jxr, and .wdp.</span></span>

<span data-ttu-id="2b884-132">Для правильной работы **D3DX10 \_ одиночная \_ WMP** требует инициализировать COM.</span><span class="sxs-lookup"><span data-stu-id="2b884-132">To work properly, **D3DX10\_IFF\_WMP** requires that you initialize COM.</span></span> <span data-ttu-id="2b884-133">Поэтому вызовите [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) или [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) в приложении перед вызовом D3DX.</span><span class="sxs-lookup"><span data-stu-id="2b884-133">Therefore, call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in your application before you call D3DX.</span></span>

</dd> <dt>

<span data-ttu-id="2b884-134"><span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10 \_ одиночная \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="2b884-134"><span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10\_IFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="2b884-135">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="2b884-135">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="2b884-136">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="2b884-136">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="2b884-137">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="2b884-137">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b884-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b884-138">Remarks</span></span>

<span data-ttu-id="2b884-139">Дополнительные сведения о некоторых из этих форматов см. в разделе [Типы точечных рисунков (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .</span><span class="sxs-lookup"><span data-stu-id="2b884-139">See [Types of Bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

<span data-ttu-id="2b884-140">D3DX10 использует компонент создания образов Windows для реализации большинства поддерживаемых типов файлов точечных рисунков.</span><span class="sxs-lookup"><span data-stu-id="2b884-140">D3DX10 makes use of the Windows Imaging Component to implement the majority of the supported bitmap file types.</span></span> <span data-ttu-id="2b884-141">Дополнительные сведения см. в статье [Общие сведения о компоненте Windows Imaging Component](https://msdn.microsoft.com/library/ms737408.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2b884-141">See [Windows Imaging Component Overview](https://msdn.microsoft.com/library/ms737408.aspx) for additional information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b884-142">Требования</span><span class="sxs-lookup"><span data-stu-id="2b884-142">Requirements</span></span>



| <span data-ttu-id="2b884-143">Требование</span><span class="sxs-lookup"><span data-stu-id="2b884-143">Requirement</span></span> | <span data-ttu-id="2b884-144">Значение</span><span class="sxs-lookup"><span data-stu-id="2b884-144">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b884-145">Header</span><span class="sxs-lookup"><span data-stu-id="2b884-145">Header</span></span><br/> | <dl> <span data-ttu-id="2b884-146"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b884-146"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b884-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b884-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b884-148">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="2b884-148">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 
