---
description: Структура D3DXWELDEPSILONS. задает значения допуска для каждого компонента вершины при сравнении вершин, чтобы определить, достаточно ли они, чтобы их можно было использовать одновременно.
ms.assetid: 534903da-ff65-4629-9be9-66c9daed6ef5
title: Структура D3DXWELDEPSILONS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWELDEPSILONS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: bb11e6f5481b1adf7cc1bac58edf40d4ac770e92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115502"
---
# <a name="d3dxweldepsilons-structure"></a>Структура D3DXWELDEPSILONS

Задает значения допуска для каждого компонента вершины при сравнении вершин, чтобы определить, достаточно ли они, чтобы они были связаны друг с другом.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DXWELDEPSILONS {
  FLOAT Position;
  FLOAT BlendWeights;
  FLOAT Normal;
  FLOAT PSize;
  FLOAT Specular;
  FLOAT Diffuse;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
  FLOAT TessFactor;
} D3DXWELDEPSILONS, *LPD3DXWELDEPSILONS;
```



## <a name="members"></a>Члены

<dl> <dt>

**Позиция**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Положение

</dd> <dt>

**блендвеигхтс**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Вес смешения

</dd> <dt>

**Обычный**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Норм.

</dd> <dt>

**псизе**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Значение размера точки

</dd> <dt>

**Отражающее**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Значение отраженного освещения

</dd> <dt>

**Диффузное**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Рассеянное значение освещения

</dd> <dt>

**текскурд**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Восемь координат текстуры

</dd> <dt>

**Тангенс**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Тангенс

</dd> <dt>

**бинормал**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

бинормал

</dd> <dt>

**тессфактор**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Фактор тесселяции

</dd> </dl>

## <a name="remarks"></a>Remarks

Тип LPD3DXWELDEPSILONS определяется как указатель на структуру **D3DXWELDEPSILONS** .


```
typedef D3DXWELDEPSILONS *LPD3DXWELDEPSILONS;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXWeldVertices**](d3dxweldvertices.md)
</dt> </dl>

 

 
