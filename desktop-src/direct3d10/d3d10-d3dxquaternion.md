---
description: Описывает кватернион.
ms.assetid: e6cb45b2-3132-4315-b02d-a3dfc444f8cc
title: Структура D3DXQUATERNION (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQUATERNION
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 405e48c99d7298708af193016930a8defdf9d600
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355330"
---
# <a name="d3dxquaternion-structure-d3dx10mathh"></a>Структура D3DXQUATERNION (D3DX10Math. h)

Описывает кватернион.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a>Члены

<dl> <dt>

**x**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Компонент x.

</dd> <dt>

**y**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Компонент y.

</dd> <dt>

**гармошкой**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Компонент z.

</dd> <dt>

**w**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Компонент w-Component.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Кватернион добавляет четвертый элемент к \[ значениям x, y, z \] , определяющим вектор, что приводит к произвольным векторам 4d. Однако ниже показано, как каждый элемент единичного кватерниона связан с поворотом по оси (где q представляет единицу кватерниона (x, y, z, w), ось нормализована, а тета — желаемый поворот CCW по оси):


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
