---
description: Определяет тип данных объявления вершины.
ms.assetid: 993fc7e4-4752-4bce-82d0-0a034fdc69c0
title: Перечисление D3DDECLTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3edb3f936772a7265c627f10eeb7aeb4f461701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354380"
---
# <a name="d3ddecltype-enumeration"></a>Перечисление D3DDECLTYPE

Определяет тип данных объявления вершины.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DDECLTYPE { 
  D3DDECLTYPE_FLOAT1     = 0,
  D3DDECLTYPE_FLOAT2     = 1,
  D3DDECLTYPE_FLOAT3     = 2,
  D3DDECLTYPE_FLOAT4     = 3,
  D3DDECLTYPE_D3DCOLOR   = 4,
  D3DDECLTYPE_UBYTE4     = 5,
  D3DDECLTYPE_SHORT2     = 6,
  D3DDECLTYPE_SHORT4     = 7,
  D3DDECLTYPE_UBYTE4N    = 8,
  D3DDECLTYPE_SHORT2N    = 9,
  D3DDECLTYPE_SHORT4N    = 10,
  D3DDECLTYPE_USHORT2N   = 11,
  D3DDECLTYPE_USHORT4N   = 12,
  D3DDECLTYPE_UDEC3      = 13,
  D3DDECLTYPE_DEC3N      = 14,
  D3DDECLTYPE_FLOAT16_2  = 15,
  D3DDECLTYPE_FLOAT16_4  = 16,
  D3DDECLTYPE_UNUSED     = 17
} D3DDECLTYPE, *LPD3DDECLTYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**D3DDECLTYPE \_ FLOAT1**
</dt> <dd>

Плавающее число одного компонента развернуто до (float, 0, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**D3DDECLTYPE \_ FLOAT2**
</dt> <dd>

Развернутое число с плавающей запятой двух компонентов (float, float, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**D3DDECLTYPE \_ FLOAT3**
</dt> <dd>

Три компонента с плавающей запятой, развернутые до (float, float, float, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**D3DDECLTYPE \_ FLOAT4**
</dt> <dd>

Четыре компонента с плавающей запятой, развернутые до (float, float, float, float).

</dd> <dt>

<span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**D3DDECLTYPE \_ D3DCOLOR**
</dt> <dd>

Четыре компонента Упакованные, неподписанные байты сопоставлены с 0 и 1 диапазоном. Входные данные — это [**D3DCOLOR**](d3dcolor.md) , который расширяется до порядка RGBA.

</dd> <dt>

<span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**D3DDECLTYPE \_ UBYTE4**
</dt> <dd>

4-компонентный байт без знака.

</dd> <dt>

<span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**D3DDECLTYPE \_ SHORT2**
</dt> <dd>

Два компонента, сокращенное число со знаком, расширенное до (значение, значение, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**D3DDECLTYPE \_ SHORT4**
</dt> <dd>

Четыре компонента, сокращенное число со знаком, расширенное до (значение, значение, значение, значение).

</dd> <dt>

<span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**D3DDECLTYPE \_ UBYTE4N**
</dt> <dd>

4-компонентный байт с каждым байтом, нормализованным путем деления на 255.0 f.

</dd> <dt>

<span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**D3DDECLTYPE \_ SHORT2N**
</dt> <dd>

Нормализованное, с двумя компонентами, со знаком, с короткой длиной, расширено до (первые короткие/32767.0, секунды Short/32767.0, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**D3DDECLTYPE \_ SHORT4N**
</dt> <dd>

Нормализованный, четыре компонента со знаком, короткий, расширенный (первый короткий/32767.0, второй короткий/32767.0, третий короткий/32767.0, четвертый короткий/32767.0).

</dd> <dt>

<span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**D3DDECLTYPE \_ USHORT2N**
</dt> <dd>

Нормализованное, с двумя компонентами, без знака, с расширенными значениями (первые короткие/65535.0, короткие короткие и 65535.0, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**D3DDECLTYPE \_ USHORT4N**
</dt> <dd>

Нормализованное, 4-компонентное, неподписанное короткое, расширенное до (первые короткие/65535.0, Second Short/65535.0, третья короткая/65535.0, четвертая короткая/65535.0).

</dd> <dt>

<span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**D3DDECLTYPE \_ UDEC3**
</dt> <dd>

Развернутый формат с тремя компонентами, без знака, 10 10 10 (значение, значение, значение, 1).

</dd> <dt>

<span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**D3DDECLTYPE \_ DEC3N**
</dt> <dd>

Формат трех компонентов, подписанный, 10 10 10, нормализован и расширен до (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE \_ FLOAT16 \_ 2**
</dt> <dd>

Два компонента, 16-разрядная, с плавающей точкой, развернутая до (значение, значение, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE \_ FLOAT16 \_ 4**
</dt> <dd>

Четыре компонента, 16-разрядная, с плавающей точкой, развернутая до (значение, значение, значение, значение).

</dd> <dt>

<span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**D3DDECLTYPE не \_ используется**
</dt> <dd>

Поле типа в объявлении не используется. Он предназначен для использования с D3DDECLMETHOD \_ UV и D3DDECLMETHOD \_ лукуппресамплед.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Данные вершин объявляются с помощью массива структур [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) . Каждый элемент массива содержит тип данных объявления вершины.

Используйте средство просмотра DirectX Caps Viewer (DXCapsViewer.exe), чтобы узнать, какие типы поддерживаются на вашем устройстве. Это средство можно получить и узнать о нем из пакета SDK DirectX. Сведения о пакете SDK для DirectX см. в разделе [где находится пакет DirectX SDK?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DDECLMETHOD**](./d3ddeclmethod.md)
</dt> </dl>

 

 
