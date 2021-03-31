---
description: Определяет константы, описывающие поддерживаемые режимы заливки.
ms.assetid: ba4e0c62-b496-427b-a324-2fb560d153ba
title: Перечисление D3DSHADEMODE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSHADEMODE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9950e0074bef7a7b0c211177b3902cd69e2e112c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354540"
---
# <a name="d3dshademode-enumeration"></a>Перечисление D3DSHADEMODE

Определяет константы, описывающие поддерживаемые режимы заливки.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DSHADEMODE { 
  D3DSHADE_FLAT         = 1,
  D3DSHADE_GOURAUD      = 2,
  D3DSHADE_PHONG        = 3,
  D3DSHADE_FORCE_DWORD  = 0x7fffffff
} D3DSHADEMODE, *LPD3DSHADEMODE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE \_ бемоль**
</dt> <dd>

Режим плоской заливки. Цвет и отражающий компонент первой вершины в треугольнике используются для определения цвета и отраженного компонента грани. Эти цвета остаются постоянными в пределах треугольника; то есть они не интерполируются. Отражающая альфа-составляющая интерполяция. См. заметки.

</dd> <dt>

<span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE метод \_ Гуро**
</dt> <dd>

Режим заливки Гуро. Цвет и отражающие компоненты грани определяются линейной интерполяцией между всеми тремя вершинами треугольника.

</dd> <dt>

<span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE \_ по методу Фонга**
</dt> <dd>

Не поддерживается.

</dd> <dt>

<span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Первая вершина треугольника для режима плоской заливки определяется следующим образом.

-   Для списка треугольников первая вершина треугольника i имеет значение \* 3.
-   Для полосы треугольника первая вершина треугольника i является вершиной i.
-   Для вентилятора треугольника первая вершина треугольника i — вершина i + 1.

Члены этого перечислимого типа определяют а также корректируются для \_ состояния отрисовки D3DRS шадемоде.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
