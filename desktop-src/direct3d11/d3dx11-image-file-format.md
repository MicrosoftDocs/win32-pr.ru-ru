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
# <a name="d3dx11_image_file_format-enumeration"></a>\_ \_ Перечисление форматов файлов изображений D3DX11 \_

> [!Note]  
> Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.

 

Форматы файлов изображений, поддерживаемые функциями D3DX11Createxxx и D3DX11Savexxx.

## <a name="syntax"></a>Синтаксис


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



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11 \_ одиночная \_ BMP**
</dt> <dd>

Формат файла точечного рисунка Windows (BMP). Содержит заголовок, описывающий разрешение устройства, на котором создавался прямоугольник пикселей, размеры прямоугольника, размер массива битов, логическую палитру и массив битов, определяющих связь между пикселями в изображении точечного рисунка и записями в логической палитре. Расширение файла для этого формата —. bmp.

</dd> <dt>

<span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**D3DX11 \_ одиночная \_ JPG**
</dt> <dd>

Формат сжатых файлов в формате JPEG. Указывает сжатие переменных в 24-разрядном RGB-цвете и 8-битных изображениях изображений в формате TIFF с тегом оттенков серого. Расширение файла для этого формата — JPG.

</dd> <dt>

<span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**D3DX11 \_ одиночная \_ PNG**
</dt> <dd>

Формат PNG-файла. Нечастный формат точечного рисунка, использующий сжатие без потерь. Расширение файла для этого формата —. png.

</dd> <dt>

<span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11 \_ одиночная \_ DDS**
</dt> <dd>

Формат файла поверхности DirectDraw (DDS). Сохраняет текстуры, текстуры тома и карты кубических сред, с уровнями mipmap и без него, а также с сжатием пикселов или без него. Расширение файла для этого формата — DDS.

</dd> <dt>

<span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**D3DX11 \_ одиночная \_ TIFF**
</dt> <dd>

Формат файла изображения с тегами (TIFF). Расширения файлов для этого формата: TIF и TIFF.

</dd> <dt>

<span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**D3DX11 \_ одиночная \_ GIF**
</dt> <dd>

Формат GIF. Расширение файла для этого формата — GIF.

</dd> <dt>

<span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**D3DX11 \_ одиночная \_ WMP**
</dt> <dd>

Формат Фото Windows Media (WMP). Этот формат также известен как Фото HD и JPEG XR. Расширения файлов для этого формата:. hdp,. жкср и. формате WDP.

Для правильной работы **D3DX11 \_ одиночная \_ WMP** требует инициализировать COM. Поэтому вызовите [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) или [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) в приложении перед вызовом D3DX.

</dd> <dt>

<span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11 \_ одиночная \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Примечания

Дополнительные сведения о некоторых из этих форматов см. в разделе [Типы точечных рисунков (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

