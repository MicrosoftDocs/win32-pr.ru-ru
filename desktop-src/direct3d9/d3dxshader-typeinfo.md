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
ms.openlocfilehash: 71b9cc893cdcfdc9802aca173627cd9da4f9ca4b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354713"
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

## <a name="remarks"></a>Комментарии

Сведения о типе являются частью [**D3DXSHADER \_ структмемберинфо**](d3dxshader-structmemberinfo.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHADER \_ константинфо**](d3dxshader-constantinfo.md)
</dt> </dl>

 

 
