---
title: Структура D3DX11_EFFECT_TYPE_DESC (D3dx11effect. h)
description: Описывает тип переменной влияния.
ms.assetid: bf2aa5b7-c68c-42bb-ae70-2fe16f8669a4
keywords:
- D3DX11_EFFECT_TYPE_DESC структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_TYPE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f4e8af391fed5717f47bb4b80398129cb98ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914799"
---
# <a name="d3dx11_effect_type_desc-structure"></a>\_Структура D3DX11 \_ типа \_ эффектов

Описывает тип переменной влияния.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DX11_EFFECT_TYPE_DESC {
  LPCSTR                      TypeName;
  D3D10_SHADER_VARIABLE_CLASS Class;
  D3D10_SHADER_VARIABLE_TYPE  Type;
  UINT                        Elements;
  UINT                        Members;
  UINT                        Rows;
  UINT                        Columns;
  UINT                        PackedSize;
  UINT                        UnpackedSize;
  UINT                        Stride;
} D3DX11_EFFECT_TYPE_DESC;
```



## <a name="members"></a>Участники

<dl> <dt>

**Имени**
</dt> <dd>

Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Имя типа, например "float4" или "MyStruct".

</dd> <dt>

**Класс**
</dt> <dd>

Тип: **[ **\_ \_ \_ класс переменной шейдера D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**

</dd> <dd>

Класс переменных (см. [**раздел \_ \_ \_ класс переменных шейдера D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).

</dd> <dt>

**Тип**
</dt> <dd>

Тип: **[ **\_ \_ \_ тип переменной шейдера D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**

</dd> <dd>

Тип переменной (см. [**раздел \_ \_ \_ тип переменной шейдера D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).

</dd> <dt>

**Elements (XElement Dynamic Property)** (Elements (Динамическое свойство XElement))
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число элементов в этом типе (0, если не является массивом).

</dd> <dt>

**Члены**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число элементов (0, если структура не является структурой).

</dd> <dt>

**Строки**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число строк в этом типе (0, если не является числовым примитивом).

</dd> <dt>

**Столбцы**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число столбцов в этом типе (0, если не является числовым примитивом).

</dd> <dt>

**паккедсизе**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число байтов, необходимое для представления этого типа данных при тесном упаковке.

</dd> <dt>

**унпаккедсизе**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число байтов, занимаемых этим типом данных, при его размещении в буфере констант.

</dd> <dt>

**Stride**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число байтов для поиска элементов при их размещении в буфере констант.

</dd> </dl>

## <a name="remarks"></a>Примечания

D3DX11 \_ \_ тип эффектов \_ DESC используется с [ **ID3DX11EffectType:: DESC**](id3dx11effecttype-getdesc.md)

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Эффекты с 11 по структурам](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

