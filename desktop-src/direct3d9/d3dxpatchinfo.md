---
description: Структура, содержащая атрибуты сетки исправлений.
ms.assetid: aaea69c9-2d33-46e8-bc26-95daf65abf50
title: Структура D3DXPATCHINFO (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 8628cc27a0223580aa1f8072750f4c31a176533e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354143"
---
# <a name="d3dxpatchinfo-structure"></a>Структура D3DXPATCHINFO

Структура, содержащая атрибуты сетки исправлений.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXPATCHINFO {
  D3DXPATCHMESHTYPE PatchType;
  D3DDEGREETYPE     Degree;
  D3DBASISTYPE      Basis;
} D3DXPATCHINFO, *LPD3DXPATCHINFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**патчтипе**
</dt> <dd>

Тип: **[ **D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**

</dd> <dd>

Тип исправления. Сведения о типах исправлений см. в разделе [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md).

</dd> <dt>

**Градус**
</dt> <dd>

Тип: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Степень кривых, используемая для создания исправления. Дополнительные сведения о поддерживаемых градусах см. в разделе [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

**База**
</dt> <dd>

Тип: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Тип кривой, используемой для создания исправления. Сведения о поддерживаемых типах базисов см. в разделе [**D3DBASISTYPE**](./d3dbasistype.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Сетка — это набор лиц, каждый из которых описывается простым многоугольником. Объекты можно создать, подключив несколько сеток друг к другу. Сетка исправлений создается на основе исправлений. Исправление — это 4-сторонняя фигура геометрии, созданная на основе кривых. Тип используемой кривой и порядок кривой могут быть различными, чтобы поверхность исправления соответствовала любой фигуре поверхности.

Поддерживаются следующие типы комбинаций исправлений:



| Тип исправления | Основа       | Градус |
|------------|-------------|--------|
| Прямоугольник  | Безье      | 2, 3, 5  |
| Прямоугольник  | B-сплайн    | 2, 3, 5  |
| Прямоугольник  | Catmull-Rom | 3      |
| Triangle   | Безье      | 2, 3, 5  |
| N-исправление    | Недоступно         | 3      |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**\_Сведения о D3DRECTPATCH**](d3drectpatch-info.md)
</dt> <dt>

[**\_Сведения о D3DTRIPATCH**](d3dtripatch-info.md)
</dt> <dt>

[**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
