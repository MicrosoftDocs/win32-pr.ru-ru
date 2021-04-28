---
description: Структура D3DXPLANE (D3dx9math. h) — описывает плоскость.
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: Структура D3DXPLANE (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 3df0c94dbd49cf38d9230a2c5392df8497c64761
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115722"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a>Структура D3DXPLANE (D3dx9math. h)

Описывает плоскость.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a>Члены

<dl> <dt>

**конкретного**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Коэффициент обтравочной плоскости в уравнении общей плоскости. См. заметки.

</dd> <dt>

**b**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Коэффициент b плоскости обрезки в уравнении общей плоскости. См. заметки.

</dd> <dt>

**c**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Коэффициент на c для плоскости обрезки в уравнении общей плоскости. См. заметки.

</dd> <dt>

**d**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Коэффициент d плоскости обрезки в уравнении общей плоскости. См. заметки.

</dd> </dl>

## <a name="remarks"></a>Remarks

Члены структуры **D3DXPLANE** имеют форму уравнения «общая плоскость». Они помещаются в уравнение общей **плоскости, чтобы x**+ **b** y + **c** z + **d** w = 0.

Программисты C++ могут воспользоваться преимуществами перегрузки операторов и приведения типов с [**расширениями D3DXPLANE**](d3dxplane-extensions.md) , которые реализуют перегруженные конструкторы и операторы присваивания, унарные и бинарные (включая равенство).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
