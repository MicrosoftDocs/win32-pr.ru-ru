---
description: Описывает данные, содержащиеся в перечислении.
ms.assetid: 6d494fe6-fcd5-4e71-939c-257978b41499
title: Перечисление D3DXPARAMETER_TYPE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 2d342e664aac81cf337cde2de7669c94a4ac6c94ce85c564a29da1f38dd93bd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096194"
---
# <a name="d3dxparameter_type-enumeration"></a>\_Перечисление типов D3DXPARAMETER

Описывает данные, содержащиеся в перечислении.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DXPARAMETER_TYPE { 
  D3DXPT_VOID,
  D3DXPT_BOOL,
  D3DXPT_INT,
  D3DXPT_FLOAT,
  D3DXPT_STRING,
  D3DXPT_TEXTURE,
  D3DXPT_TEXTURE1D,
  D3DXPT_TEXTURE2D,
  D3DXPT_TEXTURE3D,
  D3DXPT_TEXTURECUBE,
  D3DXPT_SAMPLER,
  D3DXPT_SAMPLER1D,
  D3DXPT_SAMPLER2D,
  D3DXPT_SAMPLER3D,
  D3DXPT_SAMPLERCUBE,
  D3DXPT_PIXELSHADER,
  D3DXPT_VERTEXSHADER,
  D3DXPT_PIXELFRAGMENT,
  D3DXPT_VERTEXFRAGMENT,
  D3DXPT_UNSUPPORTED,
  D3DXPT_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_TYPE, *LPD3DXPARAMETER_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT \_ void**
</dt> <dd>

Параметр является указателем void.

</dd> <dt>

<span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**\_Bool D3DXPT**
</dt> <dd>

Параметр является логическим. Любое ненулевое значение, переданное в [**ID3DXConstantTable:: сетбул**](id3dxconstanttable--setbool.md), [**ID3DXConstantTable:: сетбуларрай**](id3dxconstanttable--setboolarray.md), [**ID3DXConstantTable:: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable:: сетвектор**](id3dxconstanttable--setvector.md)или [**ID3DXConstantTable:: СЕТВЕКТОРАРРАЙ**](id3dxconstanttable--setvectorarray.md) , будет сопоставлено с 1 (true) перед записью в таблицу констант. в противном случае в таблице констант будет задано значение 0.

</dd> <dt>

<span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT \_ int**
</dt> <dd>

Параметр является целым числом. Любые значения с плавающей запятой, передаваемые в [**ID3DXConstantTable:: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable:: сетвектор**](id3dxconstanttable--setvector.md)или [**ID3DXConstantTable:: сетвектораррай**](id3dxconstanttable--setvectorarray.md) , будут округляться (до нуля десятичных разрядов) перед их записью в таблицу констант.

</dd> <dt>

<span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT \_ float**
</dt> <dd>

Параметр является числом с плавающей запятой.

</dd> <dt>

<span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**\_Строка D3DXPT**
</dt> <dd>

Параметр является строкой.

</dd> <dt>

<span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**\_Текстура D3DXPT**
</dt> <dd>

Параметр является текстурой.

</dd> <dt>

<span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT \_ TEXTURE1D**
</dt> <dd>

Параметр является текстурой 1D.

</dd> <dt>

<span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT \_ TEXTURE2D**
</dt> <dd>

Параметр является двухмерной текстурой.

</dd> <dt>

<span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**D3DXPT \_ TEXTURE3D**
</dt> <dd>

Параметр является трехмерной текстурой.

</dd> <dt>

<span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT \_ текстурекубе**
</dt> <dd>

Параметр является текстурой Куба.

</dd> <dt>

<span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**\_Образец D3DXPT**
</dt> <dd>

Параметр — это образец.

</dd> <dt>

<span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT \_ SAMPLER1D**
</dt> <dd>

Параметр является одномерной выборкой.

</dd> <dt>

<span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT \_ SAMPLER2D**
</dt> <dd>

Параметр — это 2D-образец.

</dd> <dt>

<span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT \_ SAMPLER3D**
</dt> <dd>

Параметр представляет собой трехмерный образец.

</dd> <dt>

<span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT \_ самплеркубе**
</dt> <dd>

Параметр — это образец куба.

</dd> <dt>

<span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT \_ PIXELSHADER**
</dt> <dd>

Параметр — это построитель текстуры.

</dd> <dt>

<span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT \_ вертексшадер**
</dt> <dd>

Параметр является шейдером вершин.

</dd> <dt>

<span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT \_ пикселфрагмент**
</dt> <dd>

Параметр является фрагментом шейдера пикселей.

</dd> <dt>

<span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT \_ вертексфрагмент**
</dt> <dd>

Параметр является фрагментом шейдера вершин.

</dd> <dt>

<span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT \_ не поддерживается**
</dt> <dd>

Параметр не поддерживается.

</dd> <dt>

<span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md)
</dt> <dt>

[**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)
</dt> </dl>

 

 




