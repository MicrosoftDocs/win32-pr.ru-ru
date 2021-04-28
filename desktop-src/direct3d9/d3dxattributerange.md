---
description: Структура D3DXATTRIBUTERANGE — сохраняет запись в таблице атрибутов.
ms.assetid: b9f13b12-35ba-4e4c-93ac-3dd44d611b47
title: Структура D3DXATTRIBUTERANGE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTERANGE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7dfdf15f653fda77b1ca8c9a14cd32decee9658e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116012"
---
# <a name="d3dxattributerange-structure"></a><span data-ttu-id="172cb-103">Структура D3DXATTRIBUTERANGE</span><span class="sxs-lookup"><span data-stu-id="172cb-103">D3DXATTRIBUTERANGE structure</span></span>

<span data-ttu-id="172cb-104">Хранит запись таблицы атрибутов.</span><span class="sxs-lookup"><span data-stu-id="172cb-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="172cb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="172cb-105">Syntax</span></span>


```C++
typedef struct D3DXATTRIBUTERANGE {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
} D3DXATTRIBUTERANGE, *LPD3DXATTRIBUTERANGE;
```



## <a name="members"></a><span data-ttu-id="172cb-106">Члены</span><span class="sxs-lookup"><span data-stu-id="172cb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="172cb-107">**аттрибид**</span><span class="sxs-lookup"><span data-stu-id="172cb-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="172cb-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="172cb-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="172cb-109">Идентификатор таблицы атрибутов.</span><span class="sxs-lookup"><span data-stu-id="172cb-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="172cb-110">**фацестарт**</span><span class="sxs-lookup"><span data-stu-id="172cb-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="172cb-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="172cb-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="172cb-112">Начальная поверхность.</span><span class="sxs-lookup"><span data-stu-id="172cb-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="172cb-113">**фацекаунт**</span><span class="sxs-lookup"><span data-stu-id="172cb-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="172cb-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="172cb-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="172cb-115">Число лиц.</span><span class="sxs-lookup"><span data-stu-id="172cb-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="172cb-116">**вертексстарт**</span><span class="sxs-lookup"><span data-stu-id="172cb-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="172cb-117">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="172cb-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="172cb-118">Начальная вершина.</span><span class="sxs-lookup"><span data-stu-id="172cb-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="172cb-119">**вертекскаунт**</span><span class="sxs-lookup"><span data-stu-id="172cb-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="172cb-120">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="172cb-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="172cb-121">Число вершин.</span><span class="sxs-lookup"><span data-stu-id="172cb-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="172cb-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="172cb-122">Remarks</span></span>

<span data-ttu-id="172cb-123">Таблица атрибутов используется для поиска областей сетки, которые должны рисоваться с разными текстурами, состояниями рендеринга, материалами и т. д.</span><span class="sxs-lookup"><span data-stu-id="172cb-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="172cb-124">Кроме того, приложение может использовать таблицу атрибутов для скрытия частей сетки, не рисуя заданный идентификатор атрибута (Аттрибид) при рисовании рамки.</span><span class="sxs-lookup"><span data-stu-id="172cb-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="172cb-125">Тип LPD3DXATTRIBUTERANGE определяется как указатель на структуру **D3DXATTRIBUTERANGE** .</span><span class="sxs-lookup"><span data-stu-id="172cb-125">The LPD3DXATTRIBUTERANGE type is defined as a pointer to the **D3DXATTRIBUTERANGE** structure.</span></span>


```
typedef D3DXATTRIBUTERANGE* LPD3DXATTRIBUTERANGE;
```



## <a name="requirements"></a><span data-ttu-id="172cb-126">Требования</span><span class="sxs-lookup"><span data-stu-id="172cb-126">Requirements</span></span>



| <span data-ttu-id="172cb-127">Требование</span><span class="sxs-lookup"><span data-stu-id="172cb-127">Requirement</span></span> | <span data-ttu-id="172cb-128">Значение</span><span class="sxs-lookup"><span data-stu-id="172cb-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="172cb-129">Header</span><span class="sxs-lookup"><span data-stu-id="172cb-129">Header</span></span><br/> | <dl> <span data-ttu-id="172cb-130"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="172cb-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="172cb-131">См. также</span><span class="sxs-lookup"><span data-stu-id="172cb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="172cb-132">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="172cb-132">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
