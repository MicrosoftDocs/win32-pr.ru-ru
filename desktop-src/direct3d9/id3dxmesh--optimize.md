---
description: Создает новую сетку с переупорядоченными лицами и вершинами для оптимизации производительности рисования.
ms.assetid: 6a9bf7b9-2cb9-4b42-92d9-2a121ff79284
title: 'Метод ID3DXMesh:: optimize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7752e08236094d7038a5e77ac1a679f787305022
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000530"
---
# <a name="id3dxmeshoptimize-method"></a><span data-ttu-id="78c6c-103">Метод ID3DXMesh:: OPTIMIZE</span><span class="sxs-lookup"><span data-stu-id="78c6c-103">ID3DXMesh::Optimize method</span></span>

<span data-ttu-id="78c6c-104">Создает новую сетку с переупорядоченными лицами и вершинами для оптимизации производительности рисования.</span><span class="sxs-lookup"><span data-stu-id="78c6c-104">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="78c6c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78c6c-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in]            DWORD        Flags,
  [in]      const DWORD        *pAdjacencyIn,
  [in, out]       DWORD        *pAdjacencyOut,
  [in, out]       DWORD        *pFaceRemap,
  [out]           LPD3DXBUFFER *ppVertexRemap,
  [out]           LPD3DXMESH   *ppOptMesh
);
```



## <a name="parameters"></a><span data-ttu-id="78c6c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="78c6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78c6c-107">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78c6c-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78c6c-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78c6c-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78c6c-109">Указывает тип выполняемой оптимизации.</span><span class="sxs-lookup"><span data-stu-id="78c6c-109">Specifies the type of optimization to perform.</span></span> <span data-ttu-id="78c6c-110">Этому параметру можно присвоить сочетание из одного или нескольких флагов из [**D3DXMESHOPT**](./d3dxmeshopt.md) и [**D3DXMESH**](./d3dxmesh.md) (за исключением D3DXMESH \_ 32-разрядной версии, D3DXMESH с помощью \_ \_ WriteOnly и D3DXMESH \_ WRITEONLY).</span><span class="sxs-lookup"><span data-stu-id="78c6c-110">This parameter can be set to a combination of one or more flags from [**D3DXMESHOPT**](./d3dxmeshopt.md) and [**D3DXMESH**](./d3dxmesh.md) (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).</span></span>

</dd> <dt>

<span data-ttu-id="78c6c-111">*паджаценциин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78c6c-111">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78c6c-112">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="78c6c-112">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78c6c-113">Указатель на массив из трех DWORD на грань, указывающий три соседа для каждой грани в исходной сетке.</span><span class="sxs-lookup"><span data-stu-id="78c6c-113">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="78c6c-114">Если у границы нет смежных сторон, значение равно 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="78c6c-114">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="78c6c-115">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="78c6c-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="78c6c-116">*паджаценциаут* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="78c6c-116">*pAdjacencyOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78c6c-117">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="78c6c-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78c6c-118">Указатель на массив из трех DWORD на грань, указывающий три соседа для каждой грани в оптимизированной сетке.</span><span class="sxs-lookup"><span data-stu-id="78c6c-118">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="78c6c-119">Если у границы нет смежных сторон, значение равно 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="78c6c-119">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="78c6c-120">*пфацеремап* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="78c6c-120">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78c6c-121">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="78c6c-121">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78c6c-122">Массив DWORD, по одному на каждый из них, который определяет исходную сетку, соответствующую каждой грани в оптимизированной сетке.</span><span class="sxs-lookup"><span data-stu-id="78c6c-122">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="78c6c-123">Если значение, заданное для этого аргумента, равно **null**, данные сопоставления лиц не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="78c6c-123">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="78c6c-124">*ппвертексремап* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="78c6c-124">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78c6c-125">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="78c6c-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="78c6c-126">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) , который содержит DWORD для каждой вершины, указывающий, как новые вершины сопоставляются со старыми вершинами.</span><span class="sxs-lookup"><span data-stu-id="78c6c-126">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="78c6c-127">Такое перераспределение полезно, если необходимо изменить внешние данные на основе нового сопоставления вершин.</span><span class="sxs-lookup"><span data-stu-id="78c6c-127">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> <dt>

<span data-ttu-id="78c6c-128">*ппоптмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="78c6c-128">*ppOptMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78c6c-129">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="78c6c-129">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="78c6c-130">Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий оптимизированную сетку.</span><span class="sxs-lookup"><span data-stu-id="78c6c-130">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the optimized mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78c6c-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78c6c-131">Return value</span></span>

<span data-ttu-id="78c6c-132">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="78c6c-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="78c6c-133">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="78c6c-133">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="78c6c-134">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="78c6c-134">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="78c6c-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78c6c-135">Remarks</span></span>

<span data-ttu-id="78c6c-136">Этот метод создает новую сетку.</span><span class="sxs-lookup"><span data-stu-id="78c6c-136">This method generates a new mesh.</span></span> <span data-ttu-id="78c6c-137">Перед запуском optimize приложение должно создать буфер соседей путем вызова [**ID3DXBaseMesh:: женератеаджаценци**](id3dxbasemesh--generateadjacency.md).</span><span class="sxs-lookup"><span data-stu-id="78c6c-137">Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span></span> <span data-ttu-id="78c6c-138">В буфере соседка содержатся смежные данные, например список краев и сторон, расположенных рядом друг с другом.</span><span class="sxs-lookup"><span data-stu-id="78c6c-138">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

<span data-ttu-id="78c6c-139">Этот метод очень похож на метод [**ID3DXBaseMesh:: клонемеш**](id3dxbasemesh--clonemesh.md) , за исключением того, что он может выполнять оптимизацию при формировании нового клона сетки.</span><span class="sxs-lookup"><span data-stu-id="78c6c-139">This method is very similar to the [**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh.</span></span> <span data-ttu-id="78c6c-140">Выходная сетка наследует все параметры создания входной сетки.</span><span class="sxs-lookup"><span data-stu-id="78c6c-140">The output mesh inherits all of the creation parameters of the input mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="78c6c-141">Требования</span><span class="sxs-lookup"><span data-stu-id="78c6c-141">Requirements</span></span>



| <span data-ttu-id="78c6c-142">Требование</span><span class="sxs-lookup"><span data-stu-id="78c6c-142">Requirement</span></span> | <span data-ttu-id="78c6c-143">Значение</span><span class="sxs-lookup"><span data-stu-id="78c6c-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78c6c-144">Header</span><span class="sxs-lookup"><span data-stu-id="78c6c-144">Header</span></span><br/>  | <dl> <span data-ttu-id="78c6c-145"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="78c6c-145"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="78c6c-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="78c6c-146">Library</span></span><br/> | <dl> <span data-ttu-id="78c6c-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78c6c-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="78c6c-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78c6c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c6c-149">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="78c6c-149">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="78c6c-150">**ID3DXMesh:: Оптимизеинплаце**</span><span class="sxs-lookup"><span data-stu-id="78c6c-150">**ID3DXMesh::OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
