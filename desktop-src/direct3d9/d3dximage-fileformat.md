---
description: Описывает поддерживаемые форматы файлов изображений. Описания этих форматов см. в разделе Примечания.
ms.assetid: 245a0052-f156-44ad-ab46-3677a818167e
title: Перечисление D3DXIMAGE_FILEFORMAT (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_FILEFORMAT
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: 3b1195e7503ff32e92cdbafde941b811dcf86427
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354830"
---
# <a name="d3dximage_fileformat-enumeration"></a><span data-ttu-id="4a521-104">\_Перечисление FILEFORMAT D3DXIMAGE</span><span class="sxs-lookup"><span data-stu-id="4a521-104">D3DXIMAGE\_FILEFORMAT enumeration</span></span>

<span data-ttu-id="4a521-105">Описывает поддерживаемые форматы файлов изображений.</span><span class="sxs-lookup"><span data-stu-id="4a521-105">Describes the supported image file formats.</span></span> <span data-ttu-id="4a521-106">Описания этих форматов см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="4a521-106">See Remarks for descriptions of these formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a521-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a521-107">Syntax</span></span>


```C++
typedef enum D3DXIMAGE_FILEFORMAT { 
  D3DXIFF_BMP          = 0,
  D3DXIFF_JPG          = 1,
  D3DXIFF_TGA          = 2,
  D3DXIFF_PNG          = 3,
  D3DXIFF_DDS          = 4,
  D3DXIFF_PPM          = 5,
  D3DXIFF_DIB          = 6,
  D3DXIFF_HDR          = 7,
  D3DXIFF_PFM          = 8,
  D3DXIFF_FORCE_DWORD  = 0x7fffffff
} D3DXIMAGE_FILEFORMAT, *LPD3DXIMAGE_FILEFORMAT;
```



## <a name="constants"></a><span data-ttu-id="4a521-108">Константы</span><span class="sxs-lookup"><span data-stu-id="4a521-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4a521-109"><span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="4a521-109"><span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="4a521-110">Формат файла точечного рисунка Windows (BMP).</span><span class="sxs-lookup"><span data-stu-id="4a521-110">Windows bitmap (BMP) file format.</span></span>

</dd> <dt>

<span data-ttu-id="4a521-111"><span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF \_ JPG**</span><span class="sxs-lookup"><span data-stu-id="4a521-111"><span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="4a521-112">Формат сжатых файлов в формате JPEG.</span><span class="sxs-lookup"><span data-stu-id="4a521-112">Joint Photographics Experts Group (JPEG) compressed file format.</span></span>

</dd> <dt>

<span data-ttu-id="4a521-113"><span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF \_ TGA**</span><span class="sxs-lookup"><span data-stu-id="4a521-113"><span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF\_TGA**</span></span>
</dt> <dd>

<span data-ttu-id="4a521-114">Формат файла изображения формат (Targa или TGA).</span><span class="sxs-lookup"><span data-stu-id="4a521-114">Truevision (Targa, or TGA) image file format.</span></span>

</dd> <dt>

<span data-ttu-id="4a521-115"><span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**D3DXIFF \_ PNG**</span><span class="sxs-lookup"><span data-stu-id="4a521-115"><span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**D3DXIFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="4a521-116">Формат PNG-файла.</span><span class="sxs-lookup"><span data-stu-id="4a521-116">Portable Network Graphics (PNG) file format.</span></span>

</dd> <dt>

<span data-ttu-id="4a521-117"><span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF \_ DDS**</span><span class="sxs-lookup"><span data-stu-id="4a521-117"><span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="4a521-118">Формат файла поверхности DirectDraw (DDS).</span><span class="sxs-lookup"><span data-stu-id="4a521-118">DirectDraw surface (DDS) file format.</span></span>

</dd> <dt>

<span data-ttu-id="4a521-119"><span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF \_ стр/мин**</span><span class="sxs-lookup"><span data-stu-id="4a521-119"><span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF\_PPM**</span></span>
</dt> <dd>

<span data-ttu-id="4a521-120">Переносимый формат файла пиксмап (PPM).</span><span class="sxs-lookup"><span data-stu-id="4a521-120">Portable pixmap (PPM) file format.</span></span>

</dd> <dt>

<span data-ttu-id="4a521-121"><span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**D3DXIFF \_ DIB**</span><span class="sxs-lookup"><span data-stu-id="4a521-121"><span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**D3DXIFF\_DIB**</span></span>
</dt> <dd>

<span data-ttu-id="4a521-122">Формат файлов DIB, не зависящий от устройства Windows.</span><span class="sxs-lookup"><span data-stu-id="4a521-122">Windows device-independent bitmap (DIB) file format.</span></span>

</dd> <dt>

<span data-ttu-id="4a521-123"><span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**D3DXIFF \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="4a521-123"><span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**D3DXIFF\_HDR**</span></span>
</dt> <dd>

<span data-ttu-id="4a521-124">Формат файла с высоким динамическим диапазоном (HDR).</span><span class="sxs-lookup"><span data-stu-id="4a521-124">High dynamic range (HDR) file format.</span></span>

</dd> <dt>

<span data-ttu-id="4a521-125"><span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF \_ ПФМ**</span><span class="sxs-lookup"><span data-stu-id="4a521-125"><span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF\_PFM**</span></span>
</dt> <dd>

<span data-ttu-id="4a521-126">Формат файла переносимой таблицы с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="4a521-126">Portable float map file format.</span></span>

</dd> <dt>

<span data-ttu-id="4a521-127"><span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4a521-127"><span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="4a521-128">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="4a521-128">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="4a521-129">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="4a521-129">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="4a521-130">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="4a521-130">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a521-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a521-131">Remarks</span></span>

<span data-ttu-id="4a521-132">Функции, которые начинаются с D3DXLoadxxx, поддерживают все перечисленные форматы.</span><span class="sxs-lookup"><span data-stu-id="4a521-132">Functions that begin with D3DXLoadxxx support all of the formats listed.</span></span> <span data-ttu-id="4a521-133">Функции, которые начинаются с D3DXSavexxx, поддерживают все перечисленные форматы, кроме форматов формат (TGA) и Portable пиксмап (стр. ppm).</span><span class="sxs-lookup"><span data-stu-id="4a521-133">Functions that begin with D3DXSavexxx support all of the formats listed except the Truevision (.tga) and portable pixmap (.ppm) formats.</span></span>

<span data-ttu-id="4a521-134">В следующей таблице перечислены доступные форматы входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4a521-134">The following table lists the available input and output formats.</span></span>



| <span data-ttu-id="4a521-135">Расширение файла</span><span class="sxs-lookup"><span data-stu-id="4a521-135">File Extension</span></span> | <span data-ttu-id="4a521-136">Описание</span><span class="sxs-lookup"><span data-stu-id="4a521-136">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a521-137">BMP</span><span class="sxs-lookup"><span data-stu-id="4a521-137">.bmp</span></span>           | <span data-ttu-id="4a521-138">Формат точечного рисунка Windows.</span><span class="sxs-lookup"><span data-stu-id="4a521-138">Windows bitmap format.</span></span> <span data-ttu-id="4a521-139">Содержит заголовок, описывающий разрешение устройства, на котором создавался прямоугольник пикселей, размеры прямоугольника, размер массива битов, логическую палитру и массив битов, определяющих связь между пикселями в изображении точечного рисунка и записями в логической палитре.</span><span class="sxs-lookup"><span data-stu-id="4a521-139">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> |
| <span data-ttu-id="4a521-140">DDS</span><span class="sxs-lookup"><span data-stu-id="4a521-140">.dds</span></span>           | <span data-ttu-id="4a521-141">Формат файла поверхности DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="4a521-141">DirectDraw Surface file format.</span></span> <span data-ttu-id="4a521-142">Сохраняет текстуры, текстуры тома и карты кубических сред, с уровнями mipmap и без него, а также с сжатием пикселов или без него.</span><span class="sxs-lookup"><span data-stu-id="4a521-142">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="4a521-143">См. раздел [DDS](../direct3ddds/dx-graphics-dds.md).</span><span class="sxs-lookup"><span data-stu-id="4a521-143">See [DDS](../direct3ddds/dx-graphics-dds.md).</span></span>                                                                                                                                       |
| <span data-ttu-id="4a521-144">DIB</span><span class="sxs-lookup"><span data-stu-id="4a521-144">.dib</span></span>           | <span data-ttu-id="4a521-145">Формат DIB Windows.</span><span class="sxs-lookup"><span data-stu-id="4a521-145">Windows DIB.</span></span> <span data-ttu-id="4a521-146">Содержит массив битов, Объединенных с структурами, которые задают ширину и высоту растрового изображения, цветовой формат устройства, на котором было создано изображение, и разрешение устройства, которое использовалось для создания этого изображения.</span><span class="sxs-lookup"><span data-stu-id="4a521-146">Contains an array of bits combined with structures that specify width and height of the bitmapped image, color format of the device where the image was created, and resolution of the device used to create that image.</span></span>                                                                                                              |
| <span data-ttu-id="4a521-147">. HDR</span><span class="sxs-lookup"><span data-stu-id="4a521-147">.hdr</span></span>           | <span data-ttu-id="4a521-148">Формат HDR.</span><span class="sxs-lookup"><span data-stu-id="4a521-148">HDR format.</span></span> <span data-ttu-id="4a521-149">Кодирует каждый пиксель как РГБЕ 32-разрядный цвет с 8 битами для красного, зеленого и синего, а также общий 8-разрядный показатель степени.</span><span class="sxs-lookup"><span data-stu-id="4a521-149">Encodes each pixel as an RGBE 32-bit color, with 8 bits of mantissa for red, green, and blue, and a shared 8-bit exponent.</span></span> <span data-ttu-id="4a521-150">Каждый канал по отдельности сжимается с помощью кодирования длины выполнения (RLE).</span><span class="sxs-lookup"><span data-stu-id="4a521-150">Each channel is separately compressed with run-length encoding (RLE).</span></span>                                                                                                                                       |
| <span data-ttu-id="4a521-151">.jpg</span><span class="sxs-lookup"><span data-stu-id="4a521-151">.jpg</span></span>           | <span data-ttu-id="4a521-152">Стандарт JPEG.</span><span class="sxs-lookup"><span data-stu-id="4a521-152">JPEG standard.</span></span> <span data-ttu-id="4a521-153">Указывает сжатие переменных в 24-разрядном RGB-цвете и 8-битных изображениях изображений в формате TIFF с тегом оттенков серого.</span><span class="sxs-lookup"><span data-stu-id="4a521-153">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="4a521-154">. ПФМ</span><span class="sxs-lookup"><span data-stu-id="4a521-154">.pfm</span></span>           | <span data-ttu-id="4a521-155">Формат переносимой схемы float.</span><span class="sxs-lookup"><span data-stu-id="4a521-155">Portable float map format.</span></span> <span data-ttu-id="4a521-156">Необработанный формат изображения с плавающей точкой без сжатия.</span><span class="sxs-lookup"><span data-stu-id="4a521-156">A raw floating point image format, without any compression.</span></span> <span data-ttu-id="4a521-157">В заголовке файла указываются ширина, высота, монохромный цвет и порядок слов в машинном образах.</span><span class="sxs-lookup"><span data-stu-id="4a521-157">The file header specifies image width, height, monochrome or color, and machine word order.</span></span> <span data-ttu-id="4a521-158">Пиксельные данные хранятся как 32-разрядные значения с плавающей запятой, с 3 значениями на пиксель для цвета и одним значением на пиксель для монохромных.</span><span class="sxs-lookup"><span data-stu-id="4a521-158">Pixel data is stored as 32-bit floating point values, with 3 values per pixel for color, and one value per pixel for monochrome.</span></span>                                |
| <span data-ttu-id="4a521-159">.png</span><span class="sxs-lookup"><span data-stu-id="4a521-159">.png</span></span>           | <span data-ttu-id="4a521-160">Формат PNG.</span><span class="sxs-lookup"><span data-stu-id="4a521-160">PNG format.</span></span> <span data-ttu-id="4a521-161">Нечастный формат точечного рисунка, использующий сжатие без потерь.</span><span class="sxs-lookup"><span data-stu-id="4a521-161">A non-proprietary bitmap format using lossless compression.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="4a521-162">стр/мин</span><span class="sxs-lookup"><span data-stu-id="4a521-162">.ppm</span></span>           | <span data-ttu-id="4a521-163">Переносимый формат Пиксмап.</span><span class="sxs-lookup"><span data-stu-id="4a521-163">Portable Pixmap format.</span></span> <span data-ttu-id="4a521-164">Формат двоичного файла или формата ASCII для цветовых изображений, включающий высоту и ширину изображения, а также максимальное значение компонента цвета.</span><span class="sxs-lookup"><span data-stu-id="4a521-164">A binary or ASCII file format for color images that includes image height and width and the maximum color component value.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="4a521-165">TGA</span><span class="sxs-lookup"><span data-stu-id="4a521-165">.tga</span></span>           | <span data-ttu-id="4a521-166">Формат графического адаптера Targa или формат.</span><span class="sxs-lookup"><span data-stu-id="4a521-166">Targa or Truevision Graphics Adapter format.</span></span> <span data-ttu-id="4a521-167">Поддерживает глубину 8, 15, 16, 24 и 32 бит, включая 8-разрядную серую шкалу, и содержит необязательные данные цветовой палитры, данные об источнике изображения (x, y) и размере, а также данные пикселей.</span><span class="sxs-lookup"><span data-stu-id="4a521-167">Supports depths of 8, 15, 16, 24, and 32 bits, including 8-bit gray scale, and contains optional color palette data, image (x, y) origin and size data, and pixel data.</span></span>                                                                                                                               |



 

<span data-ttu-id="4a521-168">Дополнительные сведения о некоторых из этих форматов см. в разделе [Типы точечных рисунков](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .</span><span class="sxs-lookup"><span data-stu-id="4a521-168">See [Types of Bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a521-169">Требования</span><span class="sxs-lookup"><span data-stu-id="4a521-169">Requirements</span></span>



| <span data-ttu-id="4a521-170">Требование</span><span class="sxs-lookup"><span data-stu-id="4a521-170">Requirement</span></span> | <span data-ttu-id="4a521-171">Значение</span><span class="sxs-lookup"><span data-stu-id="4a521-171">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a521-172">Header</span><span class="sxs-lookup"><span data-stu-id="4a521-172">Header</span></span><br/> | <dl> <span data-ttu-id="4a521-173"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a521-173"><dt>D3dx9tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a521-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a521-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a521-175">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="4a521-175">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
