---
description: 'Метод ID3DXBaseMesh:: Женератеаджаценци — создает список границ сетки, а также список лиц, совместно использующих каждое ребро.'
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
ms.openlocfilehash: 783ed7ad61337e606793b9b467e4b17fddd7ecd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115462"
---
# <a name="id3dxbasemeshgenerateadjacency-method"></a><span data-ttu-id="db9a3-103">Метод ID3DXBaseMesh:: Женератеаджаценци</span><span class="sxs-lookup"><span data-stu-id="db9a3-103">ID3DXBaseMesh::GenerateAdjacency method</span></span>

<span data-ttu-id="db9a3-104">Создание списка границ сетки, а также списка лиц, совместно использующих каждое ребро.</span><span class="sxs-lookup"><span data-stu-id="db9a3-104">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="db9a3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db9a3-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT Epsilon,
  [in] DWORD *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="db9a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="db9a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db9a3-107">*Эпсилон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db9a3-107">*Epsilon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db9a3-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db9a3-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db9a3-109">Указывает, что вершины, отличающиеся от позиций меньше Эпсилон, должны рассматриваться как коинЦидент.</span><span class="sxs-lookup"><span data-stu-id="db9a3-109">Specifies that vertices that differ in position by less than epsilon should be treated as coincident.</span></span>

</dd> <dt>

<span data-ttu-id="db9a3-110">*паджаценци* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db9a3-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db9a3-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="db9a3-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="db9a3-112">Указатель на массив из трех DWORD на грань, который должен быть заполнен индексами смежных граней.</span><span class="sxs-lookup"><span data-stu-id="db9a3-112">Pointer to an array of three DWORDs per face to be filled with the indices of adjacent faces.</span></span> <span data-ttu-id="db9a3-113">Число байтов в этом массиве должно быть не менее 3 \* [**ID3DXBaseMesh:: жетнумфацес**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="db9a3-113">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db9a3-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db9a3-114">Return value</span></span>

<span data-ttu-id="db9a3-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db9a3-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db9a3-116">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="db9a3-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="db9a3-117">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="db9a3-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="db9a3-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="db9a3-118">Remarks</span></span>

<span data-ttu-id="db9a3-119">После того как приложение создаст сведения о смежности для сетки, данные сетки можно оптимизировать для повышения производительности рисования.</span><span class="sxs-lookup"><span data-stu-id="db9a3-119">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span>

<span data-ttu-id="db9a3-120">Порядок записей в смежном буфере определяется порядком индексов вершин в буфере индекса.</span><span class="sxs-lookup"><span data-stu-id="db9a3-120">The order of the entries in the adjacency buffer is determined by the order of the vertex indices in the index buffer.</span></span> <span data-ttu-id="db9a3-121">Смежный треугольник 0 всегда соответствует границе между индексами углов 0 и 1.</span><span class="sxs-lookup"><span data-stu-id="db9a3-121">The adjacent triangle 0 always corresponds to the edge between the indices of the corners 0 and 1.</span></span> <span data-ttu-id="db9a3-122">Смежный треугольник 1 всегда соответствует границе между индексами углов 1 и 2, а смежный треугольник 2 соответствует границе между индексами углов 2 и 0.</span><span class="sxs-lookup"><span data-stu-id="db9a3-122">The adjacent triangle 1 always corresponds to the edge between the indices of the corners 1 and 2 while the adjacent triangle 2 corresponds to the edge between the indices of the corners 2 and 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="db9a3-123">Требования</span><span class="sxs-lookup"><span data-stu-id="db9a3-123">Requirements</span></span>



| <span data-ttu-id="db9a3-124">Требование</span><span class="sxs-lookup"><span data-stu-id="db9a3-124">Requirement</span></span> | <span data-ttu-id="db9a3-125">Значение</span><span class="sxs-lookup"><span data-stu-id="db9a3-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db9a3-126">Header</span><span class="sxs-lookup"><span data-stu-id="db9a3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="db9a3-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="db9a3-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="db9a3-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="db9a3-128">Library</span></span><br/> | <dl> <span data-ttu-id="db9a3-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db9a3-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="db9a3-130">См. также</span><span class="sxs-lookup"><span data-stu-id="db9a3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db9a3-131">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="db9a3-131">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="db9a3-132">**ID3DXMesh:: OPTIMIZE**</span><span class="sxs-lookup"><span data-stu-id="db9a3-132">**ID3DXMesh::Optimize**</span></span>](id3dxmesh--optimize.md)
</dt> <dt>

[<span data-ttu-id="db9a3-133">**ID3DXMesh:: Оптимизеинплаце**</span><span class="sxs-lookup"><span data-stu-id="db9a3-133">**ID3DXMesh::OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
