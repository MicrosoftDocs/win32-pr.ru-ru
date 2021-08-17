---
description: Определяет прямоугольник.
ms.assetid: a8590411-fd34-4048-a41f-b4155d955573
title: Структура D3DRECT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 5e202ae058cdc30b79e2cc579a064b597d0013f7447e70f0fd6d996d9740a830
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732288"
---
# <a name="d3drect-structure"></a>Структура D3DRECT

Определяет прямоугольник.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DRECT {
  LONG x1;
  LONG y1;
  LONG x2;
  LONG y2;
} D3DRECT;
```



## <a name="members"></a>Члены

<dl> <dt>

**x1**
</dt> <dd>

Тип: **[ **Long**](../winprog/windows-data-types.md)**

</dd> <dd>

Координата по оси X верхнего левого угла прямоугольника.

</dd> <dt>

**Y1**
</dt> <dd>

Тип: **[ **Long**](../winprog/windows-data-types.md)**

</dd> <dd>

Координата по оси Y верхнего левого угла прямоугольника.

</dd> <dt>

**штук**
</dt> <dd>

Тип: **[ **Long**](../winprog/windows-data-types.md)**

</dd> <dd>

Координата по оси x правого нижнего угла прямоугольника.

</dd> <dt>

**Y2**
</dt> <dd>

Тип: **[ **Long**](../winprog/windows-data-types.md)**

</dd> <dd>

Координата по оси y правого нижнего угла прямоугольника.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)
</dt> </dl>

 

 
