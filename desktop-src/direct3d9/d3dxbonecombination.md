---
description: Описывает подмножество сетки с одинаковой комбинацией атрибутов и костей.
ms.assetid: e6a4b3bb-d28d-44c2-a6df-f60f0412a70e
title: Структура D3DXBONECOMBINATION (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBONECOMBINATION
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 72d60b5c87d43763be4700ba7931c61c41cf0101d80390afb737c7f4afda83a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952494"
---
# <a name="d3dxbonecombination-structure"></a>Структура D3DXBONECOMBINATION

Описывает подмножество сетки с одинаковой комбинацией атрибутов и костей.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXBONECOMBINATION {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
  DWORD *BoneId;
} D3DXBONECOMBINATION, *LPD3DXBONECOMBINATION;
```



## <a name="members"></a>Члены

<dl> <dt>

**аттрибид**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Идентификатор таблицы атрибутов.

</dd> <dt>

**фацестарт**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Начальная поверхность.

</dd> <dt>

**фацекаунт**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Число лиц.

</dd> <dt>

**вертексстарт**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Начальная вершина.

</dd> <dt>

**вертекскаунт**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Число вершин.

</dd> <dt>

**бонеид**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

</dd> <dd>

Указатель на массив значений, который определяет каждую из костей, которые могут быть изображены в одном вызове рисования. Обратите внимание, что массив может иметь переменную длину для поддержки сочетаний костей переменной длины [**конверттоиндекседблендедмеш**](id3dxskininfo--converttoindexedblendedmesh.md).

Размер массива зависит от типа создаваемой сетки. Неиндексируемый размер массива сетки равен числу весов на вершину (Пмаксвертексинфл в [**конверттоблендедмеш**](id3dxskininfo--converttoblendedmesh.md)). Размер индексируемого массива сетки равен числу записей в палитре матрицы костей (Палеттесизе в [**конверттоиндекседблендедмеш**](id3dxskininfo--converttoindexedblendedmesh.md)).

</dd> </dl>

## <a name="remarks"></a>Remarks

Подмножество сетки, описываемой **D3DXBONECOMBINATION** , можно визуализировать в одном вызове рисования.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
