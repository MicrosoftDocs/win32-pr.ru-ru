---
description: Тип объекта.
ms.assetid: ab405984-2ebc-4514-9400-bdb13676eda5
title: Перечисление D3DXPARAMETER_CLASS (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_CLASS
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: c42bfc9335c38de04ab484193a1e178a122f2210
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914700"
---
# <a name="d3dxparameter_class-enumeration"></a>\_Перечисление классов D3DXPARAMETER

Тип объекта.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DXPARAMETER_CLASS { 
  D3DXPC_SCALAR,
  D3DXPC_VECTOR,
  D3DXPC_MATRIX_ROWS,
  D3DXPC_MATRIX_COLUMNS,
  D3DXPC_OBJECT,
  D3DXPC_STRUCT,
  D3DXPC_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_CLASS, *LPD3DXPARAMETER_CLASS;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DXPC_SCALAR"></span><span id="d3dxpc_scalar"></span>**\_Скалярная D3DXPC**
</dt> <dd>

Константа является скалярной.

</dd> <dt>

<span id="D3DXPC_VECTOR"></span><span id="d3dxpc_vector"></span>**\_Вектор D3DXPC**
</dt> <dd>

Константа является вектором.

</dd> <dt>

<span id="D3DXPC_MATRIX_ROWS"></span><span id="d3dxpc_matrix_rows"></span>**D3DXPC \_ строк матрицы \_**
</dt> <dd>

Константа — это основная матрица строк.

</dd> <dt>

<span id="D3DXPC_MATRIX_COLUMNS"></span><span id="d3dxpc_matrix_columns"></span>**\_Столбцы матрицы D3DXPC \_**
</dt> <dd>

Константа — это основная матрица столбца.

</dd> <dt>

<span id="D3DXPC_OBJECT"></span><span id="d3dxpc_object"></span>**\_Объект D3DXPC**
</dt> <dd>

Константа — это либо текстура, либо шейдер, либо строка.

</dd> <dt>

<span id="D3DXPC_STRUCT"></span><span id="d3dxpc_struct"></span>**\_Структура D3DXPC**
</dt> <dd>

Константа является структурой.

</dd> <dt>

<span id="D3DXPC_FORCE_DWORD"></span><span id="d3dxpc_force_dword"></span>**D3DXPC \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md)
</dt> <dt>

[**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)
</dt> </dl>

 

 




