---
description: Описывает поверхность рендеринга.
ms.assetid: cffa1555-1fa2-427d-8bcb-da0e61d82152
title: Структура D3DXRTS_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 3a0b52f258956f7b62734ca97cc5d1bf5ed00ac3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000353"
---
# <a name="d3dxrts_desc-structure"></a>\_Структура D3DXRTS DESC

Описывает поверхность рендеринга.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXRTS_DESC {
  UINT      Width;
  UINT      Height;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTS_DESC, *LPD3DXRTS_DESC;
```



## <a name="members"></a>Члены

<dl> <dt>

**Width**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ширина поверхности рендеринга в пикселях.

</dd> <dt>

**Height**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Высота поверхности рендеринга (в пикселях).

</dd> <dt>

**Формат**
</dt> <dd>

Тип: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Элемент перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий формат пикселей поверхности рендеринга.

</dd> <dt>

**депсстенЦил**
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

</dd> <dd>

Если **значение — true**, поверхность рендеринга поддерживает поверхность набора элементов глубины; в противном случае этому члену присваивается **значение false**.

</dd> <dt>

**депсстенЦилформат**
</dt> <dd>

Тип: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Если ДепсстенЦил имеет значение **true**, этот параметр является членом перечислимого типа [D3DFORMAT](d3dformat.md) , описывающим формат трафарета глубины области рендеринга.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9core. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**ID3DXRenderToSurface:: DESC**](id3dxrendertosurface--getdesc.md)
</dt> </dl>

 

 
