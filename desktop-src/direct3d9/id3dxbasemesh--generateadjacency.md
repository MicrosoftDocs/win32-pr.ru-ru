---
description: Создание списка границ сетки, а также списка лиц, совместно использующих каждое ребро.
ms.assetid: 9d52290f-1c9e-43a7-b239-35cd54e36466
title: 'Метод ID3DXBaseMesh:: Женератеаджаценци (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5b1d304878a4977bb14d6ef98ad7256b6c3181f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424462"
---
# <a name="id3dxbasemeshgenerateadjacency-method"></a><span data-ttu-id="68b72-103">Метод ID3DXBaseMesh:: Женератеаджаценци</span><span class="sxs-lookup"><span data-stu-id="68b72-103">ID3DXBaseMesh::GenerateAdjacency method</span></span>

<span data-ttu-id="68b72-104">Создание списка границ сетки, а также списка лиц, совместно использующих каждое ребро.</span><span class="sxs-lookup"><span data-stu-id="68b72-104">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="68b72-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68b72-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT Epsilon,
  [in] DWORD *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="68b72-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="68b72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68b72-107">*Эпсилон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68b72-107">*Epsilon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68b72-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68b72-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68b72-109">Указывает, что вершины, отличающиеся от позиций меньше Эпсилон, должны рассматриваться как коинЦидент.</span><span class="sxs-lookup"><span data-stu-id="68b72-109">Specifies that vertices that differ in position by less than epsilon should be treated as coincident.</span></span>

</dd> <dt>

<span data-ttu-id="68b72-110">*паджаценци* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68b72-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68b72-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="68b72-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="68b72-112">Указатель на массив из трех DWORD на грань, который должен быть заполнен индексами смежных граней.</span><span class="sxs-lookup"><span data-stu-id="68b72-112">Pointer to an array of three DWORDs per face to be filled with the indices of adjacent faces.</span></span> <span data-ttu-id="68b72-113">Число байтов в этом массиве должно быть не менее 3 \* [**ID3DXBaseMesh:: жетнумфацес**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="68b72-113">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68b72-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68b72-114">Return value</span></span>

<span data-ttu-id="68b72-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="68b72-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="68b72-116">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="68b72-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="68b72-117">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="68b72-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="68b72-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68b72-118">Remarks</span></span>

<span data-ttu-id="68b72-119">После того как приложение создаст сведения о смежности для сетки, данные сетки можно оптимизировать для повышения производительности рисования.</span><span class="sxs-lookup"><span data-stu-id="68b72-119">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span>

<span data-ttu-id="68b72-120">Порядок записей в смежном буфере определяется порядком индексов вершин в буфере индекса.</span><span class="sxs-lookup"><span data-stu-id="68b72-120">The order of the entries in the adjacency buffer is determined by the order of the vertex indices in the index buffer.</span></span> <span data-ttu-id="68b72-121">Смежный треугольник 0 всегда соответствует границе между индексами углов 0 и 1.</span><span class="sxs-lookup"><span data-stu-id="68b72-121">The adjacent triangle 0 always corresponds to the edge between the indices of the corners 0 and 1.</span></span> <span data-ttu-id="68b72-122">Смежный треугольник 1 всегда соответствует границе между индексами углов 1 и 2, а смежный треугольник 2 соответствует границе между индексами углов 2 и 0.</span><span class="sxs-lookup"><span data-stu-id="68b72-122">The adjacent triangle 1 always corresponds to the edge between the indices of the corners 1 and 2 while the adjacent triangle 2 corresponds to the edge between the indices of the corners 2 and 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="68b72-123">Требования</span><span class="sxs-lookup"><span data-stu-id="68b72-123">Requirements</span></span>



| <span data-ttu-id="68b72-124">Требование</span><span class="sxs-lookup"><span data-stu-id="68b72-124">Requirement</span></span> | <span data-ttu-id="68b72-125">Значение</span><span class="sxs-lookup"><span data-stu-id="68b72-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68b72-126">Header</span><span class="sxs-lookup"><span data-stu-id="68b72-126">Header</span></span><br/>  | <dl> <span data-ttu-id="68b72-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="68b72-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="68b72-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="68b72-128">Library</span></span><br/> | <dl> <span data-ttu-id="68b72-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68b72-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="68b72-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68b72-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68b72-131">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="68b72-131">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="68b72-132">**ID3DXMesh:: OPTIMIZE**</span><span class="sxs-lookup"><span data-stu-id="68b72-132">**ID3DXMesh::Optimize**</span></span>](id3dxmesh--optimize.md)
</dt> <dt>

[<span data-ttu-id="68b72-133">**ID3DXMesh:: Оптимизеинплаце**</span><span class="sxs-lookup"><span data-stu-id="68b72-133">**ID3DXMesh::OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
