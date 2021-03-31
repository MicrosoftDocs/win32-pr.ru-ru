---
description: Создает сетку с переупорядоченными лицами и вершинами для оптимизации производительности рисования. Этот метод переупорядочивает существующую сетку.
ms.assetid: 2cdaf627-d1d3-44f0-a5ae-9023d4b0de45
title: 'Метод ID3DXMesh:: Оптимизеинплаце (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.OptimizeInplace
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f889e0d3754cc1321ffa59eba294038b87991489
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821428"
---
# <a name="id3dxmeshoptimizeinplace-method"></a><span data-ttu-id="bc798-104">Метод ID3DXMesh:: Оптимизеинплаце</span><span class="sxs-lookup"><span data-stu-id="bc798-104">ID3DXMesh::OptimizeInplace method</span></span>

<span data-ttu-id="bc798-105">Создает сетку с переупорядоченными лицами и вершинами для оптимизации производительности рисования.</span><span class="sxs-lookup"><span data-stu-id="bc798-105">Generates a mesh with reordered faces and vertices to optimize drawing performance.</span></span> <span data-ttu-id="bc798-106">Этот метод переупорядочивает существующую сетку.</span><span class="sxs-lookup"><span data-stu-id="bc798-106">This method reorders the existing mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc798-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc798-107">Syntax</span></span>


```C++
HRESULT OptimizeInplace(
  [in]        DWORD        Flags,
  [in]  const DWORD        *pAdjacencyIn,
  [out]       DWORD        *pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="bc798-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc798-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc798-109">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bc798-109">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc798-110">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc798-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc798-111">Сочетание одного или нескольких флагов [**D3DXMESHOPT**](./d3dxmeshopt.md) , определяющих тип выполняемой оптимизации.</span><span class="sxs-lookup"><span data-stu-id="bc798-111">Combination of one or more [**D3DXMESHOPT**](./d3dxmeshopt.md) flags, specifying the type of optimization to perform.</span></span>

</dd> <dt>

<span data-ttu-id="bc798-112">*паджаценциин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bc798-112">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc798-113">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="bc798-113">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bc798-114">Указатель на массив из трех DWORD на грань, указывающий три соседа для каждой грани в исходной сетке.</span><span class="sxs-lookup"><span data-stu-id="bc798-114">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="bc798-115">Если у границы нет смежных сторон, значение равно 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="bc798-115">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="bc798-116">*паджаценциаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bc798-116">*pAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc798-117">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc798-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bc798-118">Указатель на массив из трех DWORD на грань, указывающий три соседа для каждой грани в оптимизированной сетке.</span><span class="sxs-lookup"><span data-stu-id="bc798-118">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="bc798-119">Если у границы нет смежных сторон, значение равно 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="bc798-119">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="bc798-120">Если значение, заданное для этого аргумента, равно **null**, то не возвращаются смежные данные.</span><span class="sxs-lookup"><span data-stu-id="bc798-120">If the value supplied for this argument is **NULL**, adjacency data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="bc798-121">*пфацеремап* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bc798-121">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc798-122">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc798-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bc798-123">Массив DWORD, по одному на каждый из них, который определяет исходную сетку, соответствующую каждой грани в оптимизированной сетке.</span><span class="sxs-lookup"><span data-stu-id="bc798-123">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="bc798-124">Если значение, заданное для этого аргумента, равно **null**, данные сопоставления лиц не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="bc798-124">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="bc798-125">*ппвертексремап* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bc798-125">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc798-126">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc798-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="bc798-127">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) , который содержит DWORD для каждой вершины, указывающий, как новые вершины сопоставляются со старыми вершинами.</span><span class="sxs-lookup"><span data-stu-id="bc798-127">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="bc798-128">Такое перераспределение полезно, если необходимо изменить внешние данные на основе нового сопоставления вершин.</span><span class="sxs-lookup"><span data-stu-id="bc798-128">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="bc798-129">Если значение, заданное для этого аргумента, равно **null**, данные сопоставления вершин не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="bc798-129">If the value supplied for this argument is **NULL**, vertex remap data is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc798-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc798-130">Return value</span></span>

<span data-ttu-id="bc798-131">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bc798-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bc798-132">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="bc798-132">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bc798-133">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ Каннотаттрсорт, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bc798-133">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_CANNOTATTRSORT, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc798-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc798-134">Remarks</span></span>

<span data-ttu-id="bc798-135">Перед выполнением **ID3DXMesh:: оптимизеинплаце** приложение должно создать буфер соседа путем вызова [**ID3DXBaseMesh:: женератеаджаценци**](id3dxbasemesh--generateadjacency.md).</span><span class="sxs-lookup"><span data-stu-id="bc798-135">Before running **ID3DXMesh::OptimizeInplace**, an application must generate an adjacency buffer by calling [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span></span> <span data-ttu-id="bc798-136">В буфере соседка содержатся смежные данные, например список краев и сторон, расположенных рядом друг с другом.</span><span class="sxs-lookup"><span data-stu-id="bc798-136">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

> [!Note]  
> <span data-ttu-id="bc798-137">Этот метод завершится ошибкой, если в сетке используется буфер вершин совместно с другой сеткой, если только D3DXMESHOPT \_ игноревертс не установлен в флагах.</span><span class="sxs-lookup"><span data-stu-id="bc798-137">This method will fail if the mesh is sharing its vertex buffer with another mesh, unless the D3DXMESHOPT\_IGNOREVERTS is set in Flags.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bc798-138">Требования</span><span class="sxs-lookup"><span data-stu-id="bc798-138">Requirements</span></span>



| <span data-ttu-id="bc798-139">Требование</span><span class="sxs-lookup"><span data-stu-id="bc798-139">Requirement</span></span> | <span data-ttu-id="bc798-140">Значение</span><span class="sxs-lookup"><span data-stu-id="bc798-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc798-141">Header</span><span class="sxs-lookup"><span data-stu-id="bc798-141">Header</span></span><br/>  | <dl> <span data-ttu-id="bc798-142"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc798-142"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bc798-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bc798-143">Library</span></span><br/> | <dl> <span data-ttu-id="bc798-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc798-144"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bc798-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc798-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc798-146">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="bc798-146">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="bc798-147">**ID3DXMesh:: OPTIMIZE**</span><span class="sxs-lookup"><span data-stu-id="bc798-147">**ID3DXMesh::Optimize**</span></span>](id3dxmesh--optimize.md)
</dt> </dl>

 

 
