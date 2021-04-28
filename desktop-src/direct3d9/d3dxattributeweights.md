---
description: Структура D3DXATTRIBUTEWEIGHTS — определяет атрибуты веса сетки.
ms.assetid: 8901a0fe-e38a-4045-8e8d-584be2620cc3
title: Структура D3DXATTRIBUTEWEIGHTS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTEWEIGHTS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7a833d2a58db0f434f836126926e461cd2ee3ea0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115972"
---
# <a name="d3dxattributeweights-structure"></a>Структура D3DXATTRIBUTEWEIGHTS

Задает атрибуты веса сетки.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXATTRIBUTEWEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DXATTRIBUTEWEIGHTS, *LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="members"></a>Члены

<dl> <dt>

**Позиция**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Положение.

</dd> <dt>

**Граница**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Вес смешения.

</dd> <dt>

**Обычный**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Нормальный.

</dd> <dt>

**Диффузное**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Рассеянное значение освещения.

</dd> <dt>

**Отражающее**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Значение отраженного освещения.

</dd> <dt>

**текскурд**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Восемь координат текстуры.

</dd> <dt>

**Тангенс**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Тангенс.

</dd> <dt>

**бинормал**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Бинормал.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура описывает, как операция упрощения будет учитывать данные вершин при вычислении относительных затрат между свертыванием краев. Например, если значение обычного поля равно 0,0, то при вычислении ошибки для сворачивания операция упрощения будет игнорировать компонент нормали вершины. Однако если значение обычного поля равно 1,0, то операция упрощения будет использовать компонент нормали вершины. Если значение обычного поля равно 2,0, удваивается количество ошибок. Если значение обычного поля равно 4,0, то число ошибок и т. д.

Тип LPD3DXATTRIBUTEWEIGHTS определяется как указатель на структуру **D3DXATTRIBUTEWEIGHTS** .


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSimplifyMesh**](d3dxsimplifymesh.md)
</dt> </dl>

 

 
