---
description: Хранит запись таблицы атрибутов.
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
ms.openlocfilehash: a842bbf41847f4b4e65c975e11f3e160cea1422d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703825"
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

## <a name="remarks"></a>Комментарии

Таблица атрибутов используется для поиска областей сетки, которые должны рисоваться с разными текстурами, состояниями рендеринга, материалами и т. д. Кроме того, приложение может использовать таблицу атрибутов для скрытия частей сетки, не рисуя заданный идентификатор атрибута (Аттрибид) при рисовании рамки.

Тип LPD3DXATTRIBUTERANGE определяется как указатель на структуру **D3DXATTRIBUTERANGE** .


```
typedef D3DXATTRIBUTERANGE* LPD3DXATTRIBUTERANGE;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
