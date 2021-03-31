---
description: Структура данных сетки.
ms.assetid: 9164b956-95b7-4bc0-bf7e-feed2e3b4a2b
title: Структура D3DXMESHDATA (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHDATA
api_type:
- HeaderDef
api_location:
- D3dx9anim.h
ms.openlocfilehash: 785284ba1330c957813a099eb6cf1c74521d3c90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354173"
---
# <a name="d3dxmeshdata-structure"></a>Структура D3DXMESHDATA

Структура данных сетки.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXMESHDATA {
  D3DXMESHDATATYPE Type;
  union {
    LPD3DXMESH      pMesh;
    LPD3DXPATCHMESH pPatchMesh;
  };
} D3DXMESHDATA, *LPD3DXMESHDATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**Тип**
</dt> <dd>

Тип: **[ **D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)**

</dd> <dd>

Определяет тип данных сетки. См. [**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md).

</dd> <dt>

**пмеш**
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

</dd> <dd>

Указатель на сетку. См. [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

**ппатчмеш**
</dt> <dd>

Тип: **LPD3DXPATCHMESH**

</dd> <dd>

Указатель на сетку исправлений. См. [**ID3DXPatchMesh**](id3dxpatchmesh.md).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXMESHCONTAINER**](d3dxmeshcontainer.md)
</dt> </dl>

 

 
