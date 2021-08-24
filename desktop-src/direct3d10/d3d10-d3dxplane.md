---
description: Структура D3DXPLANE (D3DX10Math. h) — описывает плоскость.
ms.assetid: c6da7343-a4f3-4cac-855b-14bd70c0d3c2
title: Структура D3DXPLANE (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: ccdc8644f63bdb048f6caa97ef635165a11a4473f549214410558583c8f807c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754264"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a>Структура D3DXPLANE (D3DX10Math. h)

Описывает плоскость.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a>Члены

<dl> <dt>

**конкретного**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Коэффициент обтравочной плоскости в уравнении общей плоскости. См. заметки.

</dd> <dt>

**b**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Коэффициент b плоскости обрезки в уравнении общей плоскости. См. заметки.

</dd> <dt>

**c**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Коэффициент на c для плоскости обрезки в уравнении общей плоскости. См. заметки.

</dd> <dt>

**d**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Коэффициент d плоскости обрезки в уравнении общей плоскости. См. заметки.

</dd> </dl>

## <a name="remarks"></a>Remarks

Члены структуры **D3DXPLANE** имеют форму уравнения «общая плоскость». Они помещаются в уравнение общей плоскости, чтобы AX + by + CZ + DW = 0.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
