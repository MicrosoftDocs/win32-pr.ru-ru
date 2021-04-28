---
description: D3DX10_MESH перечисление — флаги, используемые для указания параметров создания сетки.
ms.assetid: 1a5a6b3f-34f4-4338-9ffe-8f95f6f0c385
title: Перечисление D3DX10_MESH (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 2659783b0443396508465f9498eec86950f825bc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105442"
---
# <a name="d3dx10_mesh-enumeration"></a>Перечисление D3DX10 в \_ сетке

Флаги, используемые для указания параметров создания сетки.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10 \_ сеть \_ 32 \_ бит**
</dt> <dd>

Сетка имеет 32-разрядные индексы вместо 16-разрядных индексов. См. заметки.

</dd> <dt>

<span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**\_Соседство по D3DX10 сети \_ GS \_**
</dt> <dd>

Сигнализирует, что сетка содержит данные о соотношении вершин шейдера Geometry.

</dd> </dl>

## <a name="remarks"></a>Remarks

32-разрядная сеть (D3DXMESH \_ 32 бита) теоретически может поддерживать (2 ³ ²) — 1 лица и вершины. Однако выделение памяти для сетки, которая велика в 32-разрядной операционной системе, не является практичной.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Перечисления D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




