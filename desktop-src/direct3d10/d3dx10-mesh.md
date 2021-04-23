---
description: Флаги, используемые для указания параметров создания сетки.
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
ms.openlocfilehash: c2387024512a42c0a9e06ac1818b0282121cd0eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674751"
---
# <a name="d3dx10_mesh-enumeration"></a><span data-ttu-id="53409-103">Перечисление D3DX10 в \_ сетке</span><span class="sxs-lookup"><span data-stu-id="53409-103">D3DX10\_MESH enumeration</span></span>

<span data-ttu-id="53409-104">Флаги, используемые для указания параметров создания сетки.</span><span class="sxs-lookup"><span data-stu-id="53409-104">Flags used to specify creation options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="53409-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53409-105">Syntax</span></span>


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a><span data-ttu-id="53409-106">Константы</span><span class="sxs-lookup"><span data-stu-id="53409-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="53409-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10 \_ сеть \_ 32 \_ бит**</span><span class="sxs-lookup"><span data-stu-id="53409-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10\_MESH\_32\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="53409-108">Сетка имеет 32-разрядные индексы вместо 16-разрядных индексов.</span><span class="sxs-lookup"><span data-stu-id="53409-108">The mesh has 32-bit indices instead of 16-bit indices.</span></span> <span data-ttu-id="53409-109">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="53409-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="53409-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**\_Соседство по D3DX10 сети \_ GS \_**</span><span class="sxs-lookup"><span data-stu-id="53409-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3DX10\_MESH\_GS\_ADJACENCY**</span></span>
</dt> <dd>

<span data-ttu-id="53409-111">Сигнализирует, что сетка содержит данные о соотношении вершин шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="53409-111">Signals that the mesh contains geometry shader adjacency data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53409-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53409-112">Remarks</span></span>

<span data-ttu-id="53409-113">32-разрядная сеть (D3DXMESH \_ 32 бита) теоретически может поддерживать (2 ³ ²) — 1 лица и вершины.</span><span class="sxs-lookup"><span data-stu-id="53409-113">A 32-bit mesh (D3DXMESH\_32BIT) can theoretically support (2³²)-1 faces and vertices.</span></span> <span data-ttu-id="53409-114">Однако выделение памяти для сетки, которая велика в 32-разрядной операционной системе, не является практичной.</span><span class="sxs-lookup"><span data-stu-id="53409-114">However, allocating memory for a mesh that large on a 32-bit operating system is not practical.</span></span>

## <a name="requirements"></a><span data-ttu-id="53409-115">Требования</span><span class="sxs-lookup"><span data-stu-id="53409-115">Requirements</span></span>



| <span data-ttu-id="53409-116">Требование</span><span class="sxs-lookup"><span data-stu-id="53409-116">Requirement</span></span> | <span data-ttu-id="53409-117">Значение</span><span class="sxs-lookup"><span data-stu-id="53409-117">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53409-118">Header</span><span class="sxs-lookup"><span data-stu-id="53409-118">Header</span></span><br/> | <dl> <span data-ttu-id="53409-119"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="53409-119"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53409-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53409-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53409-121">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="53409-121">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




