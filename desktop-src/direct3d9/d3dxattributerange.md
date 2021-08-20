---
description: Структура D3DXATTRIBUTERANGE — сохраняет запись в таблице атрибутов.
ms.assetid: b9f13b12-35ba-4e4c-93ac-3dd44d611b47
title: Структура D3DXATTRIBUTERANGE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTERANGE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 73fe2214b2c1b8acb1bc657bd41803c425b4c86f34d022d6367c3011eebd6d50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526812"
---
# <a name="d3dxattributerange-structure"></a>Структура D3DXATTRIBUTERANGE

Хранит запись таблицы атрибутов.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXATTRIBUTERANGE {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
} D3DXATTRIBUTERANGE, *LPD3DXATTRIBUTERANGE;
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

</dd> </dl>

## <a name="remarks"></a>Remarks

Таблица атрибутов используется для поиска областей сетки, которые должны рисоваться с разными текстурами, состояниями рендеринга, материалами и т. д. Кроме того, приложение может использовать таблицу атрибутов для скрытия частей сетки, не рисуя заданный идентификатор атрибута (Аттрибид) при рисовании рамки.

Тип LPD3DXATTRIBUTERANGE определяется как указатель на структуру **D3DXATTRIBUTERANGE** .


```
typedef D3DXATTRIBUTERANGE* LPD3DXATTRIBUTERANGE;
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
