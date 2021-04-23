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
# <a name="d3dxmeshdata-structure"></a><span data-ttu-id="03e0a-103">Структура D3DXMESHDATA</span><span class="sxs-lookup"><span data-stu-id="03e0a-103">D3DXMESHDATA structure</span></span>

<span data-ttu-id="03e0a-104">Структура данных сетки.</span><span class="sxs-lookup"><span data-stu-id="03e0a-104">Mesh data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="03e0a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03e0a-105">Syntax</span></span>


```C++
typedef struct D3DXMESHDATA {
  D3DXMESHDATATYPE Type;
  union {
    LPD3DXMESH      pMesh;
    LPD3DXPATCHMESH pPatchMesh;
  };
} D3DXMESHDATA, *LPD3DXMESHDATA;
```



## <a name="members"></a><span data-ttu-id="03e0a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="03e0a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="03e0a-107">**Тип**</span><span class="sxs-lookup"><span data-stu-id="03e0a-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="03e0a-108">Тип: **[ **D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)**</span><span class="sxs-lookup"><span data-stu-id="03e0a-108">Type: **[**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="03e0a-109">Определяет тип данных сетки.</span><span class="sxs-lookup"><span data-stu-id="03e0a-109">Defines the mesh data type.</span></span> <span data-ttu-id="03e0a-110">См. [**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md).</span><span class="sxs-lookup"><span data-stu-id="03e0a-110">See [**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md).</span></span>

</dd> <dt>

<span data-ttu-id="03e0a-111">**пмеш**</span><span class="sxs-lookup"><span data-stu-id="03e0a-111">**pMesh**</span></span>
</dt> <dd>

<span data-ttu-id="03e0a-112">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="03e0a-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

</dd> <dd>

<span data-ttu-id="03e0a-113">Указатель на сетку.</span><span class="sxs-lookup"><span data-stu-id="03e0a-113">Pointer to a mesh.</span></span> <span data-ttu-id="03e0a-114">См. [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="03e0a-114">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="03e0a-115">**ппатчмеш**</span><span class="sxs-lookup"><span data-stu-id="03e0a-115">**pPatchMesh**</span></span>
</dt> <dd>

<span data-ttu-id="03e0a-116">Тип: **LPD3DXPATCHMESH**</span><span class="sxs-lookup"><span data-stu-id="03e0a-116">Type: **LPD3DXPATCHMESH**</span></span>

</dd> <dd>

<span data-ttu-id="03e0a-117">Указатель на сетку исправлений.</span><span class="sxs-lookup"><span data-stu-id="03e0a-117">Pointer to a patch mesh.</span></span> <span data-ttu-id="03e0a-118">См. [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span><span class="sxs-lookup"><span data-stu-id="03e0a-118">See [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03e0a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="03e0a-119">Requirements</span></span>



| <span data-ttu-id="03e0a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="03e0a-120">Requirement</span></span> | <span data-ttu-id="03e0a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="03e0a-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03e0a-122">Header</span><span class="sxs-lookup"><span data-stu-id="03e0a-122">Header</span></span><br/> | <dl> <span data-ttu-id="03e0a-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="03e0a-123"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03e0a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03e0a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03e0a-125">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="03e0a-125">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="03e0a-126">**D3DXMESHCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="03e0a-126">**D3DXMESHCONTAINER**</span></span>](d3dxmeshcontainer.md)
</dt> </dl>

 

 
