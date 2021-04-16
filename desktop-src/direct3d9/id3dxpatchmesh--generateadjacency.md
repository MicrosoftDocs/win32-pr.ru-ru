---
description: Создание списка границ сетки и исправлений, которые совместно используют каждое ребро.
ms.assetid: 024528c0-2c0d-4448-9b38-05cf8d6ffc63
title: 'Метод ID3DXPatchMesh:: Женератеаджаценци (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68de2a77b9d27391c57ec299ceb87d29166ee248
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424334"
---
# <a name="id3dxpatchmeshgenerateadjacency-method"></a><span data-ttu-id="bbc63-103">Метод ID3DXPatchMesh:: Женератеаджаценци</span><span class="sxs-lookup"><span data-stu-id="bbc63-103">ID3DXPatchMesh::GenerateAdjacency method</span></span>

<span data-ttu-id="bbc63-104">Создание списка границ сетки и исправлений, которые совместно используют каждое ребро.</span><span class="sxs-lookup"><span data-stu-id="bbc63-104">Generate a list of mesh edges and the patches that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbc63-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bbc63-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT fTolerance
);
```



## <a name="parameters"></a><span data-ttu-id="bbc63-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbc63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbc63-107">*фтолеранце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bbc63-107">*fTolerance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbc63-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bbc63-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bbc63-109">Указывает, что вершины, которые отличаются в положении на меньшее допустимое отклонение, должны рассматриваться как коинЦидент.</span><span class="sxs-lookup"><span data-stu-id="bbc63-109">Specifies that vertices that differ in position by less than the tolerance should be treated as coincident.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbc63-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bbc63-110">Return value</span></span>

<span data-ttu-id="bbc63-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bbc63-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bbc63-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="bbc63-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bbc63-113">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bbc63-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbc63-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bbc63-114">Remarks</span></span>

<span data-ttu-id="bbc63-115">После того как приложение создаст сведения о смежности для сетки, данные сетки можно оптимизировать для повышения производительности рисования.</span><span class="sxs-lookup"><span data-stu-id="bbc63-115">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span> <span data-ttu-id="bbc63-116">Этот метод определяет, какие исправления являются смежными (в пределах указанного допуска).</span><span class="sxs-lookup"><span data-stu-id="bbc63-116">This method determines which patches are adjacent (within the provided tolerance).</span></span> <span data-ttu-id="bbc63-117">Эта информация используется внутренним образом для оптимизации тесселяции.</span><span class="sxs-lookup"><span data-stu-id="bbc63-117">This information is used internally to optimize tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbc63-118">Требования</span><span class="sxs-lookup"><span data-stu-id="bbc63-118">Requirements</span></span>



| <span data-ttu-id="bbc63-119">Требование</span><span class="sxs-lookup"><span data-stu-id="bbc63-119">Requirement</span></span> | <span data-ttu-id="bbc63-120">Значение</span><span class="sxs-lookup"><span data-stu-id="bbc63-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc63-121">Header</span><span class="sxs-lookup"><span data-stu-id="bbc63-121">Header</span></span><br/>  | <dl> <span data-ttu-id="bbc63-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbc63-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bbc63-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bbc63-123">Library</span></span><br/> | <dl> <span data-ttu-id="bbc63-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bbc63-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bbc63-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bbc63-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbc63-126">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="bbc63-126">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="bbc63-127">**ID3DXPatchMesh:: OPTIMIZE**</span><span class="sxs-lookup"><span data-stu-id="bbc63-127">**ID3DXPatchMesh::Optimize**</span></span>](id3dxpatchmesh--optimize.md)
</dt> </dl>

 

 
