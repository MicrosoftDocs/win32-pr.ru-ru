---
description: Определяет тип базиса для поверхности исправления высокого порядка.
ms.assetid: 18c31c77-7ba3-449c-af4a-717b8c1dced1
title: Перечисление D3DBASISTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBASISTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7e166f56aa2625c868d3e2e2223efbb577e05bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157151"
---
# <a name="d3dbasistype-enumeration"></a>Перечисление D3DBASISTYPE

Определяет тип базиса для поверхности исправления высокого порядка.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DBASISTYPE { 
  D3DBASIS_BEZIER       = 0,
  D3DBASIS_BSPLINE      = 1,
  D3DBASIS_CATMULL_ROM  = 2,
  D3DBASIS_FORCE_DWORD  = 0x7fffffff
} D3DBASISTYPE, *LPD3DBASISTYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS \_ Безье**
</dt> <dd>

Входные вершины рассматриваются как ряд исправлений Безье. Указанное число вершин должно быть кратным 4. Части сетки, превышающие этот критерий, не будут подготавливаться к просмотру. Между подисправлениями в внутренней области, отображаемой каждым вызовом, подразумевается полная непрерывность. На результирующей поверхности гарантированно помещаются только вершины в углах каждого подобновления.

</dd> <dt>

<span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS \_ бсплине**
</dt> <dd>

Входные вершины обрабатываются как контрольные точки в области B-сплайна. Число отображаемых апертур меньше, чем число апертур в этом направлении. В общем случае созданная поверхность не содержит заданных вершин элемента управления.

</dd> <dt>

<span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS \_ катмулл \_ ROM**
</dt> <dd>

На основе интерполяции определяется поверхность, так что поверхность проходит через все указанные вершины входных вершин. В DirectX 8 это было D3DBASIS \_ интерполяцией.

</dd> <dt>

<span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Члены **D3DBASISTYPE** задают формулировку, который будет использоваться для вычисления примитива поверхности исправления высокого порядка во время тесселяции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**\_Сведения о D3DRECTPATCH**](d3drectpatch-info.md)
</dt> <dt>

[**\_Сведения о D3DTRIPATCH**](d3dtripatch-info.md)
</dt> </dl>

 

 




