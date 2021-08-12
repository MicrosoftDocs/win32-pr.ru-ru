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
ms.openlocfilehash: c6f1c204dfe674a2c2db995e158891ea03ca571b00c0fc4f49f4e52884042c34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526068"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
