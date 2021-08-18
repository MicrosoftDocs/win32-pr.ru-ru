---
description: Структура D3DXCOLOR (D3dx9math. h) — описывает значения цвета.
ms.assetid: 53d3176a-f727-498e-8bea-0e30e0a1c66e
title: Структура D3DXCOLOR (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 28f170814988317cd1cdf3300e4cbb3c2a97fa0fac7a43b2231767914a9b103a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988724"
---
# <a name="d3dxcolor-structure-d3dx9mathh"></a>Структура D3DXCOLOR (D3dx9math. h)

Описывает значения цвета.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXCOLOR {
  FLOAT r;
  FLOAT g;
  FLOAT b;
  FLOAT a;
} D3DXCOLOR, *LPD3DXCOLOR;
```



## <a name="members"></a>Члены

<dl> <dt>

**r**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Красный компонент цвета.

</dd> <dt>

**g**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Зеленый компонент цвета.

</dd> <dt>

**b**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Синий компонент цвета.

</dd> <dt>

**конкретного**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Альфа-компонент цвета.

</dd> </dl>

## <a name="remarks"></a>Remarks

Программисты C++ могут воспользоваться преимуществами перегрузки операторов и приведения типов с [**расширениями D3DXCOLOR**](d3dxcolor-extensions.md), которые реализуют перегруженные конструкторы, а также операторы присваивания, унарные и бинарные (включая равенство).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
