---
description: Определяет примитивы, поддерживаемые Direct3D.
ms.assetid: 89e697f9-02b9-4ae1-9e86-6178da0cb008
title: Перечисление D3DPRIMITIVETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRIMITIVETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a7406670b055a11f30a71677a88dc6230aecec8d7660d886b1d63f53e6e61566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527520"
---
# <a name="d3dprimitivetype-enumeration"></a>Перечисление D3DPRIMITIVETYPE

Определяет примитивы, поддерживаемые Direct3D.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DPRIMITIVETYPE { 
  D3DPT_POINTLIST      = 1,
  D3DPT_LINELIST       = 2,
  D3DPT_LINESTRIP      = 3,
  D3DPT_TRIANGLELIST   = 4,
  D3DPT_TRIANGLESTRIP  = 5,
  D3DPT_TRIANGLEFAN    = 6,
  D3DPT_FORCE_DWORD    = 0x7fffffff
} D3DPRIMITIVETYPE, *LPD3DPRIMITIVETYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DPT_POINTLIST"></span><span id="d3dpt_pointlist"></span>**D3DPT \_ поинтлист**
</dt> <dd>

Отображает вершины в виде коллекции изолированных точек. Это значение не поддерживается для индексированных примитивов.

</dd> <dt>

<span id="D3DPT_LINELIST"></span><span id="d3dpt_linelist"></span>**D3DPT \_ линелист**
</dt> <dd>

Отображает вершины в виде списка изолированных сегментов прямой линии.

</dd> <dt>

<span id="D3DPT_LINESTRIP"></span><span id="d3dpt_linestrip"></span>**D3DPT \_ линестрип**
</dt> <dd>

Отображает вершины в виде одной ломаной линии.

</dd> <dt>

<span id="D3DPT_TRIANGLELIST"></span><span id="d3dpt_trianglelist"></span>**D3DPT \_ трианглелист**
</dt> <dd>

Отображает указанные вершины как последовательность изолированных треугольников. Каждая группа из трех вершин определяет отдельный треугольник.

На возврат к обратной стороне влияет текущее состояние отображения "обмотка".

</dd> <dt>

<span id="D3DPT_TRIANGLESTRIP"></span><span id="d3dpt_trianglestrip"></span>**D3DPT \_ трианглестрип**
</dt> <dd>

Отображает вершины в виде полосы треугольника. Флаг отбора задних граней автоматически передается на треугольники с четным числом.

</dd> <dt>

<span id="D3DPT_TRIANGLEFAN"></span><span id="d3dpt_trianglefan"></span>**D3DPT \_ трианглефан**
</dt> <dd>

Отображает вершины в качестве вентилятора треугольника.

</dd> <dt>

<span id="D3DPT_FORCE_DWORD"></span><span id="d3dpt_force_dword"></span>**D3DPT \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

Использование [лент треугольников](triangle-strips.md) или вершинных [вентиляторов (Direct3D 9)](triangle-fans.md) зачастую более эффективно, чем использование списков треугольников, поскольку дублируется меньшее число вершин.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)
</dt> <dt>

[**IDirect3DDevice9::DrawIndexedPrimitiveUP**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)
</dt> <dt>

[**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)
</dt> <dt>

[**IDirect3DDevice9::DrawPrimitiveUP**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
</dt> </dl>

 

 
