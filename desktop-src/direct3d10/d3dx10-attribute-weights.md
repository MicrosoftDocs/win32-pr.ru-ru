---
description: Структура D3DX10_ATTRIBUTE_WEIGHTS — задает атрибуты веса сетки.
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: Структура D3DX10_ATTRIBUTE_WEIGHTS (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_WEIGHTS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: ab163149493ad73f892a251a691ad82544d7f382
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094360"
---
# <a name="d3dx10_attribute_weights-structure"></a>\_ \_ Структура весовых коэффициентов атрибутов D3DX10

Задает атрибуты веса сетки.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DX10_ATTRIBUTE_WEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DX10_ATTRIBUTE_WEIGHTS, *LPD3DX10_ATTRIBUTE_WEIGHTS;
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

\_ \_ Тип веса атрибута LPD3DX определяется как указатель на \_ \_ структуру веса атрибута D3DX.


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
