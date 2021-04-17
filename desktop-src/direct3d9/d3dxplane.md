---
description: Описывает плоскость.
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
ms.openlocfilehash: 260f9555313aea3443f0728f2b50189228429803
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713463"
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

## <a name="remarks"></a>Комментарии

Члены структуры **D3DXPLANE** имеют форму уравнения «общая плоскость». Они помещаются в уравнение общей **плоскости, чтобы x**+ **b** y + **c** z + **d** w = 0.

Программисты C++ могут воспользоваться преимуществами перегрузки операторов и приведения типов с [**расширениями D3DXPLANE**](d3dxplane-extensions.md) , которые реализуют перегруженные конструкторы и операторы присваивания, унарные и бинарные (включая равенство).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
