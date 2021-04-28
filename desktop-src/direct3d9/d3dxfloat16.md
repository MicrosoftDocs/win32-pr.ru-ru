---
description: Структура D3DXFLOAT16 (D3dx9math. h) — описывает 16-разрядный вектор с плавающей точкой.
ms.assetid: f823a327-f07a-44e9-b58a-7865e11e80eb
title: Структура D3DXFLOAT16 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: dc878575de4338a2a399f329362d79ff2e7654f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094272"
---
# <a name="d3dxfloat16-structure-d3dx9mathh"></a>Структура D3DXFLOAT16 (D3dx9math. h)

Описывает 16-разрядный вектор с плавающей точкой.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXFLOAT16 {
  WORD Value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```



## <a name="members"></a>Члены

<dl> <dt>

**Значение**
</dt> <dd>

Тип: **[ **слово**](../winprog/windows-data-types.md)**

</dd> <dd>

16-разрядные данные.

</dd> </dl>

## <a name="remarks"></a>Remarks

Программисты C++ могут воспользоваться преимуществами перегрузки операторов и приведения типов с помощью [**расширений D3DXFLOAT16**](d3dxfloat16-extensions.md), реализующих перегруженные конструкторы и операторы присваивания, унарные и бинарные (включая равенство).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
