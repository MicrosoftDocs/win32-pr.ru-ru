---
description: Определяет тип данных сетки, имеющихся в D3DXMESHDATA.
ms.assetid: e5324f85-17cc-46a7-886a-c8f3464baade
title: Перечисление D3DXMESHDATATYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHDATATYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 9dea67984992e4bb26cd9e2613013169b1ff097d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694146"
---
# <a name="d3dxmeshdatatype-enumeration"></a>Перечисление D3DXMESHDATATYPE

Определяет тип данных сетки, имеющихся в [**D3DXMESHDATA**](d3dxmeshdata.md).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DXMESHDATATYPE { 
  D3DXMESHTYPE_MESH         = 0x001,
  D3DXMESHTYPE_PATCHMESH    = 0x003,
  D3DXMESHTYPE_FORCE_DWORD  = 0x7fffffff
} D3DXMESHDATATYPE, *LPD3DXMESHDATATYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DXMESHTYPE_MESH"></span><span id="d3dxmeshtype_mesh"></span>**\_Сетка D3DXMESHTYPE**
</dt> <dd>

Тип данных — это сетка. См. [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

<span id="D3DXMESHTYPE_PATCHMESH"></span><span id="d3dxmeshtype_patchmesh"></span>**D3DXMESHTYPE \_ патчмеш**
</dt> <dd>

Тип данных — это сетка исправлений. См. [**ID3DXPatchMesh**](id3dxpatchmesh.md).

</dd> <dt>

<span id="D3DXMESHTYPE_FORCE_DWORD"></span><span id="d3dxmeshtype_force_dword"></span>**D3DXMESHTYPE \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXMESHDATA**](d3dxmeshdata.md)
</dt> </dl>

 

 




