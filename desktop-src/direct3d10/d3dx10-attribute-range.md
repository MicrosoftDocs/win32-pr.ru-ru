---
description: Структура D3DX10_ATTRIBUTE_RANGE — хранит запись таблицы атрибутов.
ms.assetid: 81c77dc9-e078-46a1-a435-4b241e36ec13
title: Структура D3DX10_ATTRIBUTE_RANGE (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_RANGE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 3e2954483da53c77ebef57f9cf2de104734caba2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094372"
---
# <a name="d3dx10_attribute_range-structure"></a><span data-ttu-id="6b93f-103">\_ \_ Структура диапазона атрибутов D3DX10</span><span class="sxs-lookup"><span data-stu-id="6b93f-103">D3DX10\_ATTRIBUTE\_RANGE structure</span></span>

<span data-ttu-id="6b93f-104">Хранит запись таблицы атрибутов.</span><span class="sxs-lookup"><span data-stu-id="6b93f-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b93f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b93f-105">Syntax</span></span>


```C++
typedef struct D3DX10_ATTRIBUTE_RANGE {
  UINT AttribId;
  UINT FaceStart;
  UINT FaceCount;
  UINT VertexStart;
  UINT VertexCount;
} D3DX10_ATTRIBUTE_RANGE, *LPD3DX10_ATTRIBUTE_RANGE;
```



## <a name="members"></a><span data-ttu-id="6b93f-106">Члены</span><span class="sxs-lookup"><span data-stu-id="6b93f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6b93f-107">**аттрибид**</span><span class="sxs-lookup"><span data-stu-id="6b93f-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="6b93f-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b93f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6b93f-109">Идентификатор таблицы атрибутов.</span><span class="sxs-lookup"><span data-stu-id="6b93f-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="6b93f-110">**фацестарт**</span><span class="sxs-lookup"><span data-stu-id="6b93f-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="6b93f-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b93f-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6b93f-112">Начальная поверхность.</span><span class="sxs-lookup"><span data-stu-id="6b93f-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="6b93f-113">**фацекаунт**</span><span class="sxs-lookup"><span data-stu-id="6b93f-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="6b93f-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b93f-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6b93f-115">Число лиц.</span><span class="sxs-lookup"><span data-stu-id="6b93f-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="6b93f-116">**вертексстарт**</span><span class="sxs-lookup"><span data-stu-id="6b93f-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="6b93f-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b93f-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6b93f-118">Начальная вершина.</span><span class="sxs-lookup"><span data-stu-id="6b93f-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="6b93f-119">**вертекскаунт**</span><span class="sxs-lookup"><span data-stu-id="6b93f-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="6b93f-120">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b93f-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6b93f-121">Число вершин.</span><span class="sxs-lookup"><span data-stu-id="6b93f-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b93f-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="6b93f-122">Remarks</span></span>

<span data-ttu-id="6b93f-123">Таблица атрибутов используется для поиска областей сетки, которые должны рисоваться с разными текстурами, состояниями рендеринга, материалами и т. д.</span><span class="sxs-lookup"><span data-stu-id="6b93f-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="6b93f-124">Кроме того, приложение может использовать таблицу атрибутов для скрытия частей сетки, не рисуя заданный идентификатор атрибута (Аттрибид) при рисовании рамки.</span><span class="sxs-lookup"><span data-stu-id="6b93f-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="6b93f-125">\_ \_ Тип диапазона атрибута LPD3DX определяется как указатель на \_ \_ структуру диапазона атрибутов D3DX.</span><span class="sxs-lookup"><span data-stu-id="6b93f-125">The LPD3DX\_ATTRIBUTE\_RANGE type is defined as a pointer to the D3DX\_ATTRIBUTE\_RANGE structure.</span></span>


```
typedef D3DX_ATTRIBUTE_RANGE* LPD3DX_ATTRIBUTE_RANGE;
```



## <a name="requirements"></a><span data-ttu-id="6b93f-126">Требования</span><span class="sxs-lookup"><span data-stu-id="6b93f-126">Requirements</span></span>



| <span data-ttu-id="6b93f-127">Требование</span><span class="sxs-lookup"><span data-stu-id="6b93f-127">Requirement</span></span> | <span data-ttu-id="6b93f-128">Значение</span><span class="sxs-lookup"><span data-stu-id="6b93f-128">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6b93f-129">Header</span><span class="sxs-lookup"><span data-stu-id="6b93f-129">Header</span></span><br/> | <dl> <span data-ttu-id="6b93f-130"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b93f-130"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b93f-131">См. также</span><span class="sxs-lookup"><span data-stu-id="6b93f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b93f-132">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="6b93f-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
