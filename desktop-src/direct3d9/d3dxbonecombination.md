---
description: Описывает подмножество сетки с одинаковой комбинацией атрибутов и костей.
ms.assetid: e6a4b3bb-d28d-44c2-a6df-f60f0412a70e
title: Структура D3DXBONECOMBINATION (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBONECOMBINATION
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 3553ba37d0d9376fa5912143fb58849f03c5a83a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081881"
---
# <a name="d3dxbonecombination-structure"></a><span data-ttu-id="5ffb4-103">Структура D3DXBONECOMBINATION</span><span class="sxs-lookup"><span data-stu-id="5ffb4-103">D3DXBONECOMBINATION structure</span></span>

<span data-ttu-id="5ffb4-104">Описывает подмножество сетки с одинаковой комбинацией атрибутов и костей.</span><span class="sxs-lookup"><span data-stu-id="5ffb4-104">Describes a subset of the mesh that has the same attribute and bone combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ffb4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ffb4-105">Syntax</span></span>


```C++
typedef struct D3DXBONECOMBINATION {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
  DWORD *BoneId;
} D3DXBONECOMBINATION, *LPD3DXBONECOMBINATION;
```



## <a name="members"></a><span data-ttu-id="5ffb4-106">Члены</span><span class="sxs-lookup"><span data-stu-id="5ffb4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5ffb4-107">**аттрибид**</span><span class="sxs-lookup"><span data-stu-id="5ffb4-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="5ffb4-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ffb4-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5ffb4-109">Идентификатор таблицы атрибутов.</span><span class="sxs-lookup"><span data-stu-id="5ffb4-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="5ffb4-110">**фацестарт**</span><span class="sxs-lookup"><span data-stu-id="5ffb4-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="5ffb4-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ffb4-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5ffb4-112">Начальная поверхность.</span><span class="sxs-lookup"><span data-stu-id="5ffb4-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="5ffb4-113">**фацекаунт**</span><span class="sxs-lookup"><span data-stu-id="5ffb4-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="5ffb4-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ffb4-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5ffb4-115">Число лиц.</span><span class="sxs-lookup"><span data-stu-id="5ffb4-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="5ffb4-116">**вертексстарт**</span><span class="sxs-lookup"><span data-stu-id="5ffb4-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="5ffb4-117">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ffb4-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5ffb4-118">Начальная вершина.</span><span class="sxs-lookup"><span data-stu-id="5ffb4-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="5ffb4-119">**вертекскаунт**</span><span class="sxs-lookup"><span data-stu-id="5ffb4-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="5ffb4-120">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ffb4-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5ffb4-121">Число вершин.</span><span class="sxs-lookup"><span data-stu-id="5ffb4-121">Vertex count.</span></span>

</dd> <dt>

<span data-ttu-id="5ffb4-122">**бонеид**</span><span class="sxs-lookup"><span data-stu-id="5ffb4-122">**BoneId**</span></span>
</dt> <dd>

<span data-ttu-id="5ffb4-123">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ffb4-123">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="5ffb4-124">Указатель на массив значений, который определяет каждую из костей, которые могут быть изображены в одном вызове рисования.</span><span class="sxs-lookup"><span data-stu-id="5ffb4-124">Pointer to an array of values that identify each of the bones that can be drawn in a single drawing call.</span></span> <span data-ttu-id="5ffb4-125">Обратите внимание, что массив может иметь переменную длину для поддержки сочетаний костей переменной длины [**конверттоиндекседблендедмеш**](id3dxskininfo--converttoindexedblendedmesh.md).</span><span class="sxs-lookup"><span data-stu-id="5ffb4-125">Note that the array can be of variable length to accommodate variable length bone combinations of [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md).</span></span>

<span data-ttu-id="5ffb4-126">Размер массива зависит от типа создаваемой сетки.</span><span class="sxs-lookup"><span data-stu-id="5ffb4-126">The size of the array varies based on the type of mesh generated.</span></span> <span data-ttu-id="5ffb4-127">Неиндексируемый размер массива сетки равен числу весов на вершину (Пмаксвертексинфл в [**конверттоблендедмеш**](id3dxskininfo--converttoblendedmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="5ffb4-127">A non-indexed mesh array size is equal to the number of weights per vertex (pMaxVertexInfl in [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)).</span></span> <span data-ttu-id="5ffb4-128">Размер индексируемого массива сетки равен числу записей в палитре матрицы костей (Палеттесизе в [**конверттоиндекседблендедмеш**](id3dxskininfo--converttoindexedblendedmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="5ffb4-128">An indexed mesh array size is equal to the number of bone matrix palette entries (paletteSize in [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ffb4-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ffb4-129">Remarks</span></span>

<span data-ttu-id="5ffb4-130">Подмножество сетки, описываемой **D3DXBONECOMBINATION** , можно визуализировать в одном вызове рисования.</span><span class="sxs-lookup"><span data-stu-id="5ffb4-130">The subset of the mesh described by **D3DXBONECOMBINATION** can be rendered in a single drawing call.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ffb4-131">Требования</span><span class="sxs-lookup"><span data-stu-id="5ffb4-131">Requirements</span></span>



| <span data-ttu-id="5ffb4-132">Требование</span><span class="sxs-lookup"><span data-stu-id="5ffb4-132">Requirement</span></span> | <span data-ttu-id="5ffb4-133">Значение</span><span class="sxs-lookup"><span data-stu-id="5ffb4-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ffb4-134">Header</span><span class="sxs-lookup"><span data-stu-id="5ffb4-134">Header</span></span><br/> | <dl> <span data-ttu-id="5ffb4-135"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ffb4-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ffb4-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ffb4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ffb4-137">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="5ffb4-137">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
