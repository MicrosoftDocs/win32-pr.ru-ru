---
description: Вспомогательная структура, содержащая сведения о типе элемента.
ms.assetid: 5580122d-c700-4632-8fcf-903519f2429e
title: Структура D3DXSHADER_TYPEINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_TYPEINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 2bd62cfc3531442f815a16148e23c281735f29e7097e5aa2b55fb03b0c0341c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731272"
---
# <a name="d3dxshader_typeinfo-structure"></a>\_Структура TYPEINFO D3DXSHADER

Вспомогательная структура, содержащая сведения о типе элемента.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXSHADER_TYPEINFO {
  WORD  Class;
  WORD  Type;
  WORD  Rows;
  WORD  Columns;
  WORD  Elements;
  WORD  StructMembers;
  DWORD StructMemberInfo;
} D3DXSHADER_TYPEINFO, *LPD3DXSHADER_TYPEINFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**Класс**
</dt> <dd>

Тип: **[ **слово**](../winprog/windows-data-types.md)**

</dd> <dd>

Тип объекта шейдера. См. раздел [**\_ класс D3DXPARAMETER**](./d3dxparameter-class.md).

</dd> <dt>

**Тип**
</dt> <dd>

Тип: **[ **слово**](../winprog/windows-data-types.md)**

</dd> <dd>

Тип данных. См. раздел [**\_ тип D3DXPARAMETER**](./d3dxparameter-type.md).

</dd> <dt>

**Строки**
</dt> <dd>

Тип: **[ **слово**](../winprog/windows-data-types.md)**

</dd> <dd>

Число строк матрицы (матрицы).

</dd> <dt>

**Столбцы**
</dt> <dd>

Тип: **[ **слово**](../winprog/windows-data-types.md)**

</dd> <dd>

Число столбцов (векторов и матриц).

</dd> <dt>

**Elements (XElement Dynamic Property)** (Elements (Динамическое свойство XElement))
</dt> <dd>

Тип: **[ **слово**](../winprog/windows-data-types.md)**

</dd> <dd>

Измерение массива.

</dd> <dt>

**структмемберс**
</dt> <dd>

Тип: **[ **слово**](../winprog/windows-data-types.md)**

</dd> <dd>

Число элементов структуры.

</dd> <dt>

**структмемберинфо**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Массив сведений о члене структуры, D3DXSHADER \_ структмемберинфо \[ *структмемберс* \] . См. раздел [**D3DXSHADER \_ структмемберинфо**](d3dxshader-structmemberinfo.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Сведения о типе являются частью [**D3DXSHADER \_ структмемберинфо**](d3dxshader-structmemberinfo.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHADER \_ константинфо**](d3dxshader-constantinfo.md)
</dt> </dl>

 

 
