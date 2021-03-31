---
description: Описывает режим экрана.
ms.assetid: e83c03ee-2067-45c9-8fd8-8c4db5558df4
title: Структура D3DDISPLAYMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8bf73899742f02a9682a3a27319768db894fd682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157155"
---
# <a name="d3ddisplaymode-structure"></a>Структура D3DDISPLAYMODE

Описывает режим экрана.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DDISPLAYMODE {
  UINT      Width;
  UINT      Height;
  UINT      RefreshRate;
  D3DFORMAT Format;
} D3DDISPLAYMODE, *LPD3DDISPLAYMODE;
```



## <a name="members"></a>Члены

<dl> <dt>

**Width**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ширина экрана (в пикселях).

</dd> <dt>

**Height**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Высота экрана (в пикселях).

</dd> <dt>

**рефрешрате**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Частота обновления. Значение 0 указывает на адаптер по умолчанию.

</dd> <dt>

**Формат**
</dt> <dd>

Тип: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Элемент перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий формат поверхности режима отображения.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**енумадаптермодес**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)
</dt> <dt>

[**жетадаптердисплаймоде**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode)
</dt> <dt>

[**жетдисплаймоде**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode)
</dt> </dl>

 

 
