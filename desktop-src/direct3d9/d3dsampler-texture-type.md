---
description: Определяет типы текстур образца для шейдеров вершин.
ms.assetid: 8e9923f9-6f30-45e5-a557-f26d441a534d
title: Перечисление D3DSAMPLER_TEXTURE_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLER_TEXTURE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 337e8b25a8ec8389a6252fb48582128c601730ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424330"
---
# <a name="d3dsampler_texture_type-enumeration"></a>\_ \_ Перечисление типов текстур D3DSAMPLER

Определяет типы текстур образца для шейдеров вершин.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DSAMPLER_TEXTURE_TYPE { 
  D3DSTT_UNKNOWN,
  D3DSTT_2D,
  D3DSTT_CUBE,
  D3DSTT_VOLUME,
  D3DSTT_FORCE_DWORD
} D3DSAMPLER_TEXTURE_TYPE, *LPD3DSAMPLER_TEXTURE_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT \_ неизвестный**
</dt> <dd>

Неинициализированное значение. Значение этого элемента равно 0 &lt; &lt; D3DSP \_ TEXTURETYPE \_ SHIFT.

</dd> <dt>

<span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT \_ 2D**
</dt> <dd>

Объявление двухмерной текстуры. Значение этого элемента равно 2 &lt; &lt; D3DSP \_ TEXTURETYPE \_ SHIFT.

</dd> <dt>

<span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**\_Куб D3DSTT**
</dt> <dd>

Объявление текстуры Куба. Значение этого элемента равно 3 &lt; &lt; D3DSP \_ TEXTURETYPE \_ SHIFT.

</dd> <dt>

<span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**\_Том D3DSTT**
</dt> <dd>

Объявление текстуры тома. Значение этого элемента равно 4 &lt; &lt; D3DSP \_ TEXTURETYPE \_ SHIFT.

</dd> <dt>

<span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




