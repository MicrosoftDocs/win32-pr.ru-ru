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
# <a name="d3dx10_mesh-enumeration"></a><span data-ttu-id="930c9-103">Перечисление D3DX10 в \_ сетке</span><span class="sxs-lookup"><span data-stu-id="930c9-103">D3DX10\_MESH enumeration</span></span>

<span data-ttu-id="930c9-104">Флаги, используемые для указания параметров создания сетки.</span><span class="sxs-lookup"><span data-stu-id="930c9-104">Flags used to specify creation options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="930c9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="930c9-105">Syntax</span></span>


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a><span data-ttu-id="930c9-106">Константы</span><span class="sxs-lookup"><span data-stu-id="930c9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="930c9-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10 \_ сеть \_ 32 \_ бит**</span><span class="sxs-lookup"><span data-stu-id="930c9-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10\_MESH\_32\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="930c9-108">Сетка имеет 32-разрядные индексы вместо 16-разрядных индексов.</span><span class="sxs-lookup"><span data-stu-id="930c9-108">The mesh has 32-bit indices instead of 16-bit indices.</span></span> <span data-ttu-id="930c9-109">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="930c9-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="930c9-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**\_Соседство по D3DX10 сети \_ GS \_**</span><span class="sxs-lookup"><span data-stu-id="930c9-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3DX10\_MESH\_GS\_ADJACENCY**</span></span>
</dt> <dd>

<span data-ttu-id="930c9-111">Сигнализирует, что сетка содержит данные о соотношении вершин шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="930c9-111">Signals that the mesh contains geometry shader adjacency data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="930c9-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="930c9-112">Remarks</span></span>

<span data-ttu-id="930c9-113">32-разрядная сеть (D3DXMESH \_ 32 бита) теоретически может поддерживать (2 ³ ²) — 1 лица и вершины.</span><span class="sxs-lookup"><span data-stu-id="930c9-113">A 32-bit mesh (D3DXMESH\_32BIT) can theoretically support (2³²)-1 faces and vertices.</span></span> <span data-ttu-id="930c9-114">Однако выделение памяти для сетки, которая велика в 32-разрядной операционной системе, не является практичной.</span><span class="sxs-lookup"><span data-stu-id="930c9-114">However, allocating memory for a mesh that large on a 32-bit operating system is not practical.</span></span>

## <a name="requirements"></a><span data-ttu-id="930c9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="930c9-115">Requirements</span></span>



| <span data-ttu-id="930c9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="930c9-116">Requirement</span></span> | <span data-ttu-id="930c9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="930c9-117">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="930c9-118">Header</span><span class="sxs-lookup"><span data-stu-id="930c9-118">Header</span></span><br/> | <dl> <span data-ttu-id="930c9-119"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="930c9-119"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="930c9-120">См. также</span><span class="sxs-lookup"><span data-stu-id="930c9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="930c9-121">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="930c9-121">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




